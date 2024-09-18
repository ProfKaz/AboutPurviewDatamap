## Registering your SQL On-Premises in Microsoft Purview Data Map

After completing the previous steps, you should have the following components ready:
- **[Azure Key Vault](03a%20-%20Azure%20Key%20Vault.md) :** Configured to securely store your SQL credentials.
- **[Microsoft Purview Integration Runtime](03b%20-%20IntegrationRuntime.md):** Set up as a bridge for Microsoft Purview Data Map to access your SQL Server on-premises.
- **[SQL on-premises Permissions](03c%20-%20Configure%20SQL%20on-premises.md):** Configured with a SQL account for Microsoft Purview Data Map.

Now, let's move forward with registering your SQL on-premises server in Purview Data Map to enable secure data scanning and management.

<br>
<details>
<summary>01 - Steps to Register SQL Server in Microsoft Purview Data Map</summary>
<br>
  
Steps to Register SQL Server in Microsoft Purview Data Map:
1. Navigate to the **Data Map** in the  [Microsoft Purview Portal](https://purview.microsoft.com).
2. Select **Data sources** on the left side.
3. Under **Register data source**, search for and select **SQL Server**.
4. Obtain the **Fully-Qualified Domain Name (FQDN)** of your SQL on-premises server from the **About** menu under **Settings**.
5. In the next step, provide the following information:
  - **Data source name:** Enter a descriptive name, such as the server name.
  - **Server endpoint:** Input the FQDN from your SQL Server.
  - **Domain:** Select an existing domain or one created in [Step 2](02%20-%20PurviewPortalConfiguration.md) of this guide.
  - **Collection:** Choose the collection previously created in [Step 2](02%20-%20PurviewPortalConfiguration.md) of this guide.
6. Press **Register**
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/d2095ec5-8238-4fed-9599-a382c8c7ab57" width="650"></p>
<p align="center">Microsoft Purview Data Map, Register.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/89f4d9c7-f161-4c35-a24f-761b1a86874b" width="650"></p>
<p align="center">Microsoft Purview Data Map, Register data source.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/2ebb8c52-832e-4fd4-bdc0-cd76c1b6691f" width="650"></p>
<p align="center">Microsoft Purview Data Map, Select SQL Server.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/02c016fa-3f1e-4c65-a8e2-171d9dd2b3c9" width="650"></p>
<p align="center">SQL Server get Full-Qualified Domain Name.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/dc4f59de-cd01-4183-afcb-46249fccfa04" width="650"></p>
<p align="center">Microsoft Purview Data Map, register SQL server.</p>
<br>

</details>
<br>

<details>
<summary>02 - Setting up the Scan Service for SQL On-Premises</summary>
<br>

Setting Up the Scan Service for SQL On-Premises:
1. Press the scan icon (a small circular blue icon).
2. Complete the following information:
  - **Name:** Use the default name or enter a custom one.
  - **Connect with integration runtime:** Select the runtime configured in [Step 3](03b%20-%20IntegrationRuntime.md).
  - **Server endpoint:** This will default to the SQL Server FQDN.
  - **Database name:** Leave blank to scan all databases or specify a database to scan.
  - **Enable** logging for scan monitoring.
  - **Domain:** This will be selected by default.
  - **Collection:** Select the collection created in [Step 2](02%20-%20PurviewPortalConfiguration.md).
3. Press **test connection** to validate your configuration and then **Continue**.
4. **Scope your scan:** Optionally, select specific tables or reduce the scope of the scan.
5. **Select a scan rule set:** Choose the default SqlServer rule set.
6. **Set a scan trigger:** Schedule your scan. For example, set it to run on the 1st day of each month.
7. Press **Save and Run**. If you do not want to run the scan immediately, click the arrow next to the button and select **Save** only.

After completing these steps, you can monitor the scan progress and view the results once the process is complete.
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/9763a1cd-e1ad-44e5-946f-4a93845f7e90" width="650"></p>
<p align="center">Microsoft Purview Data Map, Set scan.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/28f82076-fe00-46d5-93df-9e9fd0218de4" width="300"></p>
<p align="center">Microsoft Purview Data Map, Configure scan.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/ec576202-975f-4dc2-9076-f06b67816b42" width="300"></p>
<p align="center">Microsoft Purview Data Map, Scope scan.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/169000c1-0970-4176-afc6-e81c9c37afec" width="300"></p>
<p align="center">Microsoft Purview Data Map, Select a scan rule set.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/1e5cd23f-88ed-42a6-bb26-f2f5baad7c9e" width="300"></p>
<p align="center">Microsoft Purview Data Map, Schedule the scan process.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/13cc739c-5858-4c0f-a60a-76f9bc688ef0" width="300"></p>
<p align="center">Microsoft Purview Data Map, Establish schedule.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/28c8f447-94cf-4504-a6e1-bd561a1ac34c" width="300"></p>
<p align="center">Microsoft Purview Data Map, Review, Save and Run.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/cfc658dd-f6c2-403a-889c-11a5fdedb5e7" width="650"></p>
<p align="center">Microsoft Purview Data Map, Scanning process.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/845674de-d21d-4983-b142-e5fef4394c9c" width="650"></p>
<p align="center">Microsoft Purview Data Map, Scanning completed</p>
<br>

</details>
<br>
<br>
