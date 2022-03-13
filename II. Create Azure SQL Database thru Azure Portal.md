# MyExpensesDBtoAzureSQLDB

**II. Create Azure SQL Database thru Azure Portal**
<br/>
<br/>

**Create a single database**
------------------------------------------------------------------------------------------------------------------------------------

1. Browse to the [Select SQL Deployment option](https://portal.azure.com/#create/Microsoft.AzureSQL) page.
2. Under **SQL databases**, leave **Resource type** set to **Single database**, and select **Create**.

![image](https://user-images.githubusercontent.com/95063830/158052782-2a1bb39d-9f08-474b-9354-3c6669390793.png)

3. On the **Basics** tab of the **Create SQL Database** form, under Project details, select the desired **Azure Subscription**.
4. For **Resource group**, select **Create new**, enter **myexpensesdbrg**, and select **OK**.
5. For **Database name**, enter **MyExpensesDB**.
6. For Server, select Create new, and fill out the New server form with the following values:

i. **Server name**: Enter **_myexpensesdbazsqlserver_**, and add some characters for uniqueness. We can't provide an exact server name to use because server names must be globally unique for all servers in Azure, not just unique within a subscription. So enter something like mysqlserver12345, and the portal lets you know if it's available or not.            <br/>
ii. **Server admin login**: Enter **_azuresqladmin_**.      <br/>
iii. **Password**: Enter a password that meets requirements, and enter it again in the Confirm password field.      <br/>
iv. **Location**: Select East Asia from the dropdown list.   <br/>
v. **Backup storage redundancy**: Locally-redundant backup storage  <br/>

![image](https://user-images.githubusercontent.com/95063830/158053049-9c70c1c5-4153-4da4-8868-1607534f29ff.png)

Select **OK**.

7. Leave **Want to use SQL elastic pool** set to **No**.
8. Under **Compute + storag**e, select **Configure database**.
9. This quickstart uses a serverless database, so select **Serverles**, **Max vCores** to **1** only, **Auto-Pause delay** to **1 Hour**, **Data Max Size** to **1** GB only, and then select** Apply**. Take note of the **Cost summary**. We will monitor that in the upcoming days.

![image](https://user-images.githubusercontent.com/95063830/158053213-4e1c1312-9eca-4923-a661-7747a6b3ea2d.png)

10. Select **Next: Networkin** at the bottom of the page.

![image](https://user-images.githubusercontent.com/95063830/158053342-99fea09d-aafc-4533-929b-90058af110db.png)

11. On the **Networking tab**, for **Connectivity method**, select **Public endpoint**.

12. For **Firewall rules**, set **Add current client IP address** to **Yes**. Leave **Allow Azure services and resources to access this server** set to **No**. Leave also the **Connection Policy** to **Default**. For the **Encrypted connections**, leave it to **TLS 1.2**. Skip **Security** section, we will all the default settings.
13. Select Next: Additional settings at the top of the page.

![image](https://user-images.githubusercontent.com/95063830/158053553-08f76bd1-14ac-4a23-ac2f-42aac9f400d4.png)

14. On the **Additional settings** tab, in the **Data source** section, for Use existing data, select **None**. 
15. No changes for **Database collation**
16. Optionally, set the maintenance window so planned maintenance is performed at the best time for your database.
17. Select **Next: Tags**

![image](https://user-images.githubusercontent.com/95063830/158053732-655cacc7-3b9d-49e5-9c5e-eeae0696b0b1.png)

18. Follow the value below and Select **Review + create** at the bottom of the page:

![image](https://user-images.githubusercontent.com/95063830/158053763-4478bc15-1603-4de7-9ab5-63f1e1fc18d6.png)

19. Optionally, you can download the ARM template by selecting the **Download a template for automation** at the bottom of the page. It will take a time to create this resource.

![image](https://user-images.githubusercontent.com/95063830/158053850-885c61a3-821a-4470-9d31-a40851d82c93.png)

20. Deployment complete! Select **Go to Resource**

![image](https://user-images.githubusercontent.com/95063830/158053991-f698098d-e0d8-4b81-b301-539f85d5f2d5.png)

![image](https://user-images.githubusercontent.com/95063830/158054030-2a3b3b92-095b-4007-9239-9148e697245d.png)


For more informationa about resource group creation, go to [Quickstart: Create an Azure SQL Database single database](https://docs.microsoft.com/en-us/azure/azure-sql/database/single-database-create-quickstart?tabs=azure-portal)


**Next Stage**
------------------------------------------------------------------------------------------------------------------------------------

[**III. Create Azure SQL Database thru AZ PowerShell cmdlet**](https://github.com/fortehub/MyExpensesDBtoAzureSQLDB/blob/2f8c761d87ce8b83558bc068d68e00e6cd1c7019/III.%20Create%20Azure%20SQL%20Database%20thru%20AZ%20PowerShell%20cmdlet.md)
