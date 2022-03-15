# MyExpensesDBtoAzureSQLDB

**VI. Additional Configuration**
<br/>
<br/>

**Resources**
------------------------------------------------------------------------------------------------------------------------------------
[Lock resources to prevent unexpected changes](https://docs.microsoft.com/en-us/azure/governance/blueprints/concepts/resource-locking)  <br/>
[Understand resource locking in Azure Blueprints](https://docs.microsoft.com/en-us/azure/governance/blueprints/concepts/resource-locking) <br/>


**Add Locks**
------------------------------------------------------------------------------------------------------------------------------------
We will add CanNotDelete lock on the resource group where MyExpensesDB database resided.

1. Go to the **Resource Group**. Select **Locks** on **Settings** section.

![image](https://user-images.githubusercontent.com/95063830/158326108-408d1dc1-a313-4ee1-9ce8-ebce0bcc73a2.png)

2. Click **Add**.
3. Provide **Lock Name**, **Notes** and select **Delete** for **Lock Type. Then click **OK**.

![image](https://user-images.githubusercontent.com/95063830/158326405-0214c718-9ca1-4c34-8b29-aa77341bde78.png)

Lock created!

![image](https://user-images.githubusercontent.com/95063830/158326465-cf1db715-9ac6-4322-b959-ec1f0e86c468.png)

4. Go to MyExpensesDB page. Select **Locks** on **Settings** section and click **Refresh**. The database also inherit the lock.

![image](https://user-images.githubusercontent.com/95063830/158326641-042f9b43-92d6-4cad-993c-6148963fc8c4.png)


**Resources**
------------------------------------------------------------------------------------------------------------------------------------
[Use tags to organize your Azure resources and management hierarchy](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/tag-resources?tabs=json)  <br/>
[Define your tagging strategy](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/resource-tagging)  <br/>


**Add Tag to MyExpensesDB**
------------------------------------------------------------------------------------------------------------------------------------
We forgot to add tag to our Databases.

1. Go to **SQL Databases** page. 
2. Click the 3 dot on the left most side of the database entry. Select **Edit tags**.

![image](https://user-images.githubusercontent.com/95063830/158327335-95c36be7-a960-4171-9ae6-113bbe28c88f.png)

3. Add the Tags that you want. Then clic **Save**.

![image](https://user-images.githubusercontent.com/95063830/158327463-060a99ea-71c2-45d0-8011-97401ab46039.png)




