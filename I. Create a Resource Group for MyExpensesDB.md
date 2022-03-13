# MyExpensesDBtoAzureSQLDB

**I. Create a Resource Group for MyExpensesDB**
<br/>
<br/>

**Overview**
------------------------------------------------------------------------------------------------------------------------------------
We can use the Azure Cloudshell, AZ PowerShell & so on, to create an Azure Resource Group. Here for simplicity we will create a resource group thru Azure Portal


**Create resource groups**
------------------------------------------------------------------------------------------------------------------------------------

1. Sign in to the Azure portal (https://portal.azure.com/#home)
2. Select **Resource groups**

![image](https://user-images.githubusercontent.com/95063830/158051294-ac51529a-1c6d-4a24-a8ef-0cf9ab4797f3.png)

3. Select **Create**.
4. Enter the following values:

  **Subscription:** Select your Azure subscription.

  **Resource group:** myexpensesdbrg

  **Region:** East Asia
  
![image](https://user-images.githubusercontent.com/95063830/158051524-91a157ad-9747-472e-a96d-3a83b29f1c58.png)

5. Select **Next: Tags**
6. Follow the Name and values below, then Select **Review + create**

![image](https://user-images.githubusercontent.com/95063830/158051586-fbf908e1-e4ea-48d7-9588-4a267b520a6b.png)

7. Select **Create**. It takes a few seconds to create a resource group.

8. Select Refresh from the top menu to refresh the resource group list, and then select the newly created resource group to open it. Or select **Notification**(the bell icon) from the top, and then select **Go to resource group** to open the newly created resource group.

![image](https://user-images.githubusercontent.com/95063830/158051667-0149a710-349e-4f94-85de-cc71b20ab5ea.png)


**List resource groups**
------------------------------------------------------------------------------------------------------------------------------------

1. Sign in to the Azure portal (https://portal.azure.com/#home)
2. To list the resource groups, select **Resource groups**

![image](https://user-images.githubusercontent.com/95063830/158051764-5054d265-887b-44e4-975f-2412d25511ff.png)

3. To customize the information displayed for the resource groups, select **Edit columns**. The following screenshot shows the addition columns you could add to the display:

![image](https://user-images.githubusercontent.com/95063830/158051786-0db2fd55-07ee-4bb4-9c60-79b088f261f4.png)


**Open resource groups**
------------------------------------------------------------------------------------------------------------------------------------
1. Sign in to the Azure portal (https://portal.azure.com/#home)
2. Select Resource groups.
3. Select the resource group you want to open.

For more informationa about resource group creation, go to https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/manage-resource-groups-portal


**Next Stage**
------------------------------------------------------------------------------------------------------------------------------------

**II. Create Azure SQL Database thru Azure Portal**
