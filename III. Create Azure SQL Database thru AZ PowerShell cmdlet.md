# MyExpensesDBtoAzureSQLDB

**III. Create Azure SQL Database thru AZ PowerShell cmdlet**
<br/>
<br/>

**Resources**
------------------------------------------------------------------------------------------------------------------------------------
[Create a single database](https://docs.microsoft.com/en-us/azure/azure-sql/database/single-database-create-quickstart?tabs=azure-powershell) <br/>
[Use PowerShell to create a single database and configure a server-level firewall rule](https://docs.microsoft.com/en-us/azure/azure-sql/database/scripts/create-and-configure-database-powershell?toc=/powershell/module/toc.json)
<br/>
<br/>

**Create a single database**
------------------------------------------------------------------------------------------------------------------------------------
You can create a resource group, server, and single database using Windows PowerShell thru Azure Cloud Shell or installed the Az PowerShell module on your PC. For the more info about how to install Azure Az PowerShell module, go to [Install the Azure Az PowerShell module](https://docs.microsoft.com/en-us/powershell/azure/install-az-ps?view=azps-7.3.0).
<br/>

**Connect to your Azure Account** <br/>
Open PowerShell application and type the following cmdlet:

```PowerShell
Connect-AzAccount
```
You will be prompted to your web browser to login your Azure account.
<br/>

**Set parameter values & create the resources**<br/>
The following values are used in subsequent commands to create the database and required resources. Server names need to be globally unique across all of Azure so the Get-Random cmdlet is used to create the server name. Replace the 0.0.0.0 values in the ip address range to match your specific environment.

```
# Connect-AzAccount
Connect-AzAccount
# The SubscriptionId in which to create these objects
$SubscriptionId = 'InsertYourSubscriptionIdHere'

# Set the resource group name and location for your server
$resourceGroupName = "myexpensesdbrg"
$location = "eastasia"

# Set an admin login and password for your server
$adminSqlLogin = "azuresqladmin"
$password = "InsertYourPasswordHere"

# Set server name - the logical server name has to be unique in the system
$serverName = "myexpensesdbazsqlserver"

# The sample database name
$databaseName = "MyExpensesDB"

# The ip address range that you want to allow to access your server
$startIp = "InsertYourIPHere"
$endIp = "InsertYourIPHere"

# Set the Compute model
$model = "Serverless"

# BackupStorageRedundancy
$storage = "Local"

# Create Firewall Rule Name
$firewallname = "AllowAllWindowsAzureIps"

# Set auto-pause
$pause = 60

# Set compute model
$cmodel = "Serverless"

#Set Computer Generation
$gen = "Gen5"

#Set Edition
$edith = "GeneralPurpose"

#Set max virtual core
$mxvcore = 1

#Set database size
$dbsize = 1073741824

# Set subscription 
Set-AzContext -SubscriptionId $subscriptionId 


#Creating the resources
Write-host "Creating priamry SQL server..."
# Create a server with a system wide unique server name
$server = New-AzSqlServer -ResourceGroupName $resourceGroupName `
    -ServerName $serverName `
    -Location $location `
    -SqlAdministratorCredentials $(New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $adminSqlLogin, $(ConvertTo-SecureString -String $password -AsPlainText -Force))
$server


# Create a server firewall rule that allows access from the specified IP range
$serverFirewallRule = New-AzSqlServerFirewallRule -ResourceGroupName $resourceGroupName `
    -ServerName $serverName `
    -FirewallRuleName $firewallname -StartIpAddress $startIp -EndIpAddress $endIp
$serverFirewallRule


$database = New-AzSqlDatabase  -ResourceGroupName $resourceGroupName `
    -ServerName $serverName `
    -DatabaseName $databaseName `
	-AutoPauseDelayInMinutes $pause `
	-BackupStorageRedundancy $storage `
	-ComputeModel $cmodel `
	-ComputeGeneration $gen `
	-Edition $edith `
	-VCore $mxvcore `
	-MaxSizeBytes $dbsize 
$database

```

MyExpensesDB on Azure SQL Database successfully deployed!

![image](https://user-images.githubusercontent.com/95063830/158060500-692dbf66-2ead-4862-b5a6-bdb6d3c7f011.png)


**Next Stage**
------------------------------------------------------------------------------------------------------------------------------------

**IV. Assess and Migrate databases using Data Migration Assistant**
