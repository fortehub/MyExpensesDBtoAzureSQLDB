# MyExpensesDBtoAzureSQLDB

**IV. Assess and Migrate databases using Data Migration Assistant**
<br/>
<br/>

**Resources**
------------------------------------------------------------------------------------------------------------------------------------

[Overview of Data Migration Assistant](https://docs.microsoft.com/en-us/sql/dma/dma-overview?view=sql-server-ver15) <br/>
[Perform a SQL Server migration assessment with Data Migration Assistant](https://docs.microsoft.com/en-us/sql/dma/dma-assesssqlonprem?view=sql-server-ver15) <br/>
[Migrating SQL workloads to Microsoft Azure: Assessment and Migration Tools](https://www.sqlshack.com/migrating-sql-workloads-to-microsoft-azure-assessment-and-migration-tools/)<br/>
<br/>

**Prerequisites**
------------------------------------------------------------------------------------------------------------------------------------

1. Download first migration assistant, [Microsoft® Data Migration](https://www.microsoft.com/en-us/download/details.aspx?id=53595).
2. Follow the installation instructions here, [Migrating SQL workloads to Microsoft Azure: Assessment and Migration Tools](https://www.sqlshack.com/migrating-sql-workloads-to-microsoft-azure-assessment-and-migration-tools/)
3. For safety, Perform Database Full Backup first. To backup perform the following:

```T-SQL
BACKUP DATABASE MyExpensesDB
TO  DISK = N'D:\MSSQL\Backups\MyExpensesDBFullBackup_03142022.bak' 
WITH NOFORMAT, NOINIT,  NAME = N'MyExpensesDB-Full Database Backup',
SKIP, NOREWIND, NOUNLOAD,  STATS = 10, CHECKSUM
GO
```

![image](https://user-images.githubusercontent.com/95063830/158097761-a8d71254-92e3-4ebb-9554-416d05a54b0a.png)
<br/>

**Assess and Migrate**
------------------------------------------------------------------------------------------------------------------------------------

1. Open the Data Migration Assistant app, then Select the **New** (+) icon, and then select the **Migration** project type.
2. Set the source and target server type. <br/>
&ensp;If you're upgrading your on-premises SQL Server instance to a modern on-premises SQL Server instance or to SQL Server hosted on an Azure VM, set the source and target server type to **SQL Server**. If you're migrating to Azure SQL Database, instead set the target server type to **Azure SQL Database**. Follow the image below.

![image](https://user-images.githubusercontent.com/95063830/158098604-83c55b51-0c4a-478a-a55d-cc349defc1ff.png)

3. Click **Create**.
4. At the **Select Source** section, type the source's server name. Follow the image below, then click **Connect**.

![image](https://user-images.githubusercontent.com/95063830/158098760-db3c50b9-14c6-41b7-8cf2-4536937c8d7e.png)

5. Check the **Assess database before migration?**. Then click **Next**.

![image](https://user-images.githubusercontent.com/95063830/158098836-452ce041-974c-40f9-a266-20060d005a75.png)

6. At the **Select Target** section, type correct the target server's **server name, authentication type, & the credentials**. Follow the image below, then click **Connect**.

![image](https://user-images.githubusercontent.com/95063830/158102016-75d934f5-61ff-4588-9156-bcb56658f7a6.png)

7. Click **Next**.

![image](https://user-images.githubusercontent.com/95063830/158102076-cc248be5-fe51-40ef-b832-4cac65c98eaa.png)

8. At the **Select Objects**, check All the Schema objects from source database that needs to migrate. Follow the image below. Then click, **Generate SQL script**. 

![image](https://user-images.githubusercontent.com/95063830/158102435-73f7c003-7032-4141-ae3b-21ae8e54c1ea.png)

9. At the **Script & Deploy Schema** section, double of there are no assessment issues. If there's not, click the **Deploy Schema**.

![image](https://user-images.githubusercontent.com/95063830/158102596-8b1537ef-55b5-4f83-861a-db95e9662339.png)

10. After a successful deployment, click **Migrate Data**.

![image](https://user-images.githubusercontent.com/95063830/158102648-77dbe9e8-8925-42b0-93eb-4b798d1aede6.png)

12. At the **Select tables** section, check all the tables, then click **Start data migration**.

![image](https://user-images.githubusercontent.com/95063830/158102722-9e5852fe-25c6-424d-945f-1be3a88edd9d.png)

13. Data migration successful!

![image](https://user-images.githubusercontent.com/95063830/158102795-c875e61a-557e-4457-b40d-7314807e2afb.png)

14. Open SSMS or Azure Data Studio, and connect to MyExpensesDB on Azure SQL DB and verify by querying data.

![image](https://user-images.githubusercontent.com/95063830/158103060-cf691c41-03c3-4d52-b037-ac516fefe399.png)

15. Connected and queried successfully.

![image](https://user-images.githubusercontent.com/95063830/158103164-63106aea-07c7-48b9-8d26-c8e8f7380a7f.png)


**Next Stage**
------------------------------------------------------------------------------------------------------------------------------------

**V. Connect Application to the Azure SQL Database**










