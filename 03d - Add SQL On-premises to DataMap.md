## Registering your SQL On-Premises in Microsoft Purview Data Map

After completing the previous steps, you should have the following components ready:
- Azure Key Vault configured to securely store your SQL credentials.
- Microsoft Integration Runtime set up as a bridge to allow Microsoft Purview Data Map to access your SQL Server on-premises.
- SQL On-Premises configured with a SQL account specifically for use by Microsoft Purview Data Map.

Now, let's proceed with registering your SQL on-premises server in Purview Data Map to enable secure data scanning and management.

To achieve this, we will need to follow these steps:
- Go to **Data Map** menu under [Microsoft Purview Portal](https://purview.microsoft.com)
- Select **Data sources** at left side
- Under **Register data source** look for ansd select **SQL Server**
- You will need to get the Fully-Qualified Domain Name (FQDN) from your SQL server on-premises, you can get from about menu under Settings
- In the next step you will need to set:
  - Data source name: Can be any name to easy identify the server, you can use the same server name
  - Server endpoint: you need to add here the FQDN from your SQL Server
  - Domain: You can use the existing one, or anyone previously created in the point 02 of this guide.
  - Collection: This was previously created at the step 02 on this guide.
  - Press **Register**
The next step is establish a scan service for your SQL server on-premises, to do that you need to:
- Press the scan icon, a small circular blue icon
- To register you need to complete these information:
  - Name: can be used the default assigned or any name
  - Connect with integration runtime: here we need to select the same configured on the step 03
  - Server endpoint: is selected by default and correspond to the SQL Server FQDN
  - Database name: If you leave this value on blank all the databases will be scanned, or you can set ths specific datbase that you want to scan
  - Check Enable logging for scan monitor
  - Domain: is selected by default
  - Collection: This was previously created at the step 02 on this guide.
- Press test connection to validate your configuration and then Continue
- 

<br>
<details>
<summary>Register your SQL server</summary>

![image](https://github.com/user-attachments/assets/d2095ec5-8238-4fed-9599-a382c8c7ab57)

![image](https://github.com/user-attachments/assets/89f4d9c7-f161-4c35-a24f-761b1a86874b)

![image](https://github.com/user-attachments/assets/2ebb8c52-832e-4fd4-bdc0-cd76c1b6691f)

![image](https://github.com/user-attachments/assets/02c016fa-3f1e-4c65-a8e2-171d9dd2b3c9)

![image](https://github.com/user-attachments/assets/dc4f59de-cd01-4183-afcb-46249fccfa04)

</details>
<br>

<details>
<summary>Establish a scan process for your data</summary>

![image](https://github.com/user-attachments/assets/9763a1cd-e1ad-44e5-946f-4a93845f7e90)

![image](https://github.com/user-attachments/assets/28f82076-fe00-46d5-93df-9e9fd0218de4)

![image](https://github.com/user-attachments/assets/ec576202-975f-4dc2-9076-f06b67816b42)

![image](https://github.com/user-attachments/assets/169000c1-0970-4176-afc6-e81c9c37afec)

![image](https://github.com/user-attachments/assets/1e5cd23f-88ed-42a6-bb26-f2f5baad7c9e)

![image](https://github.com/user-attachments/assets/13cc739c-5858-4c0f-a60a-76f9bc688ef0)

![image](https://github.com/user-attachments/assets/28c8f447-94cf-4504-a6e1-bd561a1ac34c)

![image](https://github.com/user-attachments/assets/cfc658dd-f6c2-403a-889c-11a5fdedb5e7)

![image](https://github.com/user-attachments/assets/845674de-d21d-4983-b142-e5fef4394c9c)

</details>
<br>
<br>
