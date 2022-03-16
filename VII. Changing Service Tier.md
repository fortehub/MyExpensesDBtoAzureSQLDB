# MyExpensesDBtoAzureSQLDB

**VII. Changing Service Tier**
<br/>
<br/>

I was kinda surprised by the amount of charges accumulated within 3 days of using a 1 VCore/ 1 GB storage serverless Azure SQL Databases. 

![image](https://user-images.githubusercontent.com/95063830/158503291-32d4318b-c67f-462c-b2c7-4f046b2b9f2d.png)

So we will going to chnage the Service Tier from General Purpose to DTU-Based (Basic).

1. Go to the SQL Database page. Navigate to **Setting** then **Compute + Storage**.
2. At the **Service Tier** portion, change the Service Tier to DTU-Based (Basic).

![image](https://user-images.githubusercontent.com/95063830/158503834-28bc7b49-316e-49ae-acfd-5186d9fe42d7.png)

3. Click **Apply**. Wait for the changes to applied.

![image](https://user-images.githubusercontent.com/95063830/158504099-d63f0fa2-3c5b-4dcc-9745-9a9cc0c1f576.png)

![image](https://user-images.githubusercontent.com/95063830/158504190-29fb7b8b-a7fa-432d-a9ef-d3d0aa193e61.png)

Success!

![image](https://user-images.githubusercontent.com/95063830/158506297-fa369d34-7114-4bdf-a7d3-a389ae181938.png)

This service tier has a fix amount of 4.99 USD per month. So let see what will be my upcoming charges is.

![image](https://user-images.githubusercontent.com/95063830/158506432-a54a5b3a-b107-40d1-bd0b-d013e4630f8d.png)
