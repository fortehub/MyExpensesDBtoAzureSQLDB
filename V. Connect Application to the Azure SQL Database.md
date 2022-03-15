# MyExpensesDBtoAzureSQLDB

**V. Connect Application to the Azure SQL Database**
<br/>
<br/>


**Connect Excel to Azure SQL DB**
------------------------------------------------------------------------------------------------------------------------------------
We will connect now Excel with Devart add-ins to Azure SQL Db.

1. Open Excel, go to **Devart** section. Click **Get Data**

![image](https://user-images.githubusercontent.com/95063830/158174289-587f6246-ae03-4a7c-a00d-6175bdd88683.png)

2. Click **Back** and replace the connection properties. After replacing, click **Test Connection**. Click Next to proceed.

![image](https://user-images.githubusercontent.com/95063830/158174905-076aef2a-04fe-4742-90df-e38ad305e08d.png)

![image](https://user-images.githubusercontent.com/95063830/158174963-9e5edb36-37ae-4141-9593-61cb2cc5131d.png)

3. Replace the number of rows to any number more than 10, then click **Finish**. Now we are connected on Azure SQL DB.

![image](https://user-images.githubusercontent.com/95063830/158175177-f395fc14-ffa5-4600-81dc-ccfb90dae4ca.png)


**Connect PowerBI to Azure SQL DB**
------------------------------------------------------------------------------------------------------------------------------------
We will reconnect our PowerBI from local SQL Server to Azure SQL DB.

1. Open previously created reports.
2. At the **Field** section, right click on one of the field's entry and select **Edit query**.

![image](https://user-images.githubusercontent.com/95063830/158176082-e2144c39-9023-4f1d-9060-29291c5eb80a.png)

3. At the **Power Query Editor**, click **Data Source settings**.

![image](https://user-images.githubusercontent.com/95063830/158176638-9a0b5c66-ae3b-42c4-ae29-f38541bf3b78.png)

4. At the **Data source settings** window, click **Change Source**.

![image](https://user-images.githubusercontent.com/95063830/158176789-c54753b4-6096-447e-ad27-34288a76d9ed.png)

5. Change the **Server** connection, then click **OK**.

![image](https://user-images.githubusercontent.com/95063830/158177040-df1bb260-f1b3-4744-b6e2-337c7233eafb.png)

6. At the **Data source settings** window again, click **Edit Permissions**. At the **Edit Permissions** box, click **Edit** under **Credentials**.

![image](https://user-images.githubusercontent.com/95063830/158177244-9633ef6e-0415-4849-af19-010b0c78315f.png)

7. Replace the credential on the **Database** section, then click **Save**.

![image](https://user-images.githubusercontent.com/95063830/158177361-ee4fb36d-d841-4f2c-8231-ae43d798efc4.png)

8. To apply the changes, click **Close & Apply** button.

![image](https://user-images.githubusercontent.com/95063830/158181096-2b09a93f-7a4b-4ffd-bbc2-f0da62857a26.png)

9. Click **Run**.

![image](https://user-images.githubusercontent.com/95063830/158181164-4542195d-486f-4fb5-b4e8-7df56977b249.png)

PowerBI is connected now on Azure SQL Database.

![image](https://user-images.githubusercontent.com/95063830/158181311-ca8a30b0-4eba-4cc0-9e5a-c6c4992e20ab.png)


**Connect PowerShell script to Azure SQL DB**
------------------------------------------------------------------------------------------------------------------------------------
This is the original content of our PowerShell script:

![image](https://user-images.githubusercontent.com/95063830/158324076-e39517bd-5e63-420e-a646-cf6145685bb5.png)

Now we have to change the connection string. At the **Overview** of Azure SQL Database, click the **Connection Strings**. You will be prompted with the connection string of your Azure SQL DB.

Copy and apply this new connection string to our PowerShell script. Please input the database password, then save your work.

![image](https://user-images.githubusercontent.com/95063830/158324723-57c6990d-4c58-466c-aa92-5d947942e13e.png)

Connection string applied. Now it should be able to connect to our Azure SQL Database.


**Next Stage**
------------------------------------------------------------------------------------------------------------------------------------

**VI. Additional Configuration**
