## Finalizing Azure SQL Database Permissions
After completing the previous steps, you should now have the following component configured:

1. **[Azure SQL Database Permissions](05a%20-%20Add%20Permissions%20to%20Purview%20Data%20Map%20account.md) :** Your **Microsoft Purview account** has been successfully assigned the **db_datareader** role, allowing it to read and scan data from the database..

Now that permissions are in place, let’s proceed with registering your Azure SQL Database in the Microsoft Purview Data Map. This will allow you to enable secure data scanning and management.

<br>
<details>
<summary>01 - Steps to Register Azure SQL Database in Microsoft Purview Data Map</summary>
<br>
  
Steps to Register Azure SQL Database in Microsoft Purview Data Map:
1. Navigate to the **Data Map** in the  [Microsoft Purview Portal](https://purview.microsoft.com).
2. Select **Data sources** on the left side.
3. Under **Register data source**, search for and select **Azure SQL Database**.
4. In the next step, provide the following information:
  - **Data source name:** Enter a descriptive name, such as the server name.
  - **Server name:** Select your Azure SQL Server that you want to scan-
  - **Endpoint:** Is added automatically.
  - **Domain:** Select an existing domain or one created in [Step 2](02%20-%20PurviewPortalConfiguration.md) of this guide.
  - **Collection:** Choose the collection previously created in [Step 2](02%20-%20PurviewPortalConfiguration.md) of this guide.
5. Press **Register**
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/11af5456-c51f-4ed3-8663-044c38131986" width="650"></p>
<p align="center">Microsoft Purview Data Map, Register.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/5b29a89c-db2d-4620-9442-165db1a3fd9c" width="650"></p>
<p align="center">Microsoft Purview Data Map, Register data source.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/3edbddb7-03e1-4dab-b8dd-3ed4c4538a02" width="650"></p>
<p align="center">Microsoft Purview Data Map, Select Azure SQL Database.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/e8c644de-7a32-45ae-b80d-9f1b545d6ff4" width="650"></p>
<p align="center">Microsoft Purview Data Map, Register.</p>
<br>
</details>

<br>

<details>
<summary>02 - Setting up the Scan Service for your Azure SQL Database</summary>
<br>

Setting Up the Scan Service for Azure SQL Database:
1. Press the scan icon (a small circular blue icon).
2. Complete the following information:
  - **Name:** Use the default name or enter a custom one.
  - **Connect with integration runtime:** Use the default selection, except if you are using [Private Enpoint](06%20-%20Connect%20Microsoft%20Purview%20Data%20Map%20to%20Private%20Endpoint.md) in that case select the right one.
  - **Server endpoint:** This will default to the Azure SQL Server.
  - **Select database:** Leave From Azure subscription selected.
  - **Database name:** Select the Azure SQL Database to be scanned.
  - **Credential:** Leave Microsoft Purview MSI (system) selected.
  - **Lineage extraction (preview):** Set turned off.
  - **Scan level** Use the default value.
  - **Domain:** This will be selected by default.
  - **Collection:** Select the collection created in [Step 2](02%20-%20PurviewPortalConfiguration.md).
3. Press **test connection** to validate your configuration and then **Continue**.
4. **Scope your scan:** Optionally, select specific tables or reduce the scope of the scan.
5. **Select a scan rule set:** Choose the default AzureSqlDatabase rule set.
6. **Set a scan trigger:** Schedule your scan. For example, set it to run weekly on Sunday.
7. Press **Save and Run**. If you do not want to run the scan immediately, click the arrow next to the button and select **Save** only.

After completing these steps, you can monitor the scan progress and view the results once the process is complete.
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/df45d234-6b6c-464b-b884-688c2be91e4c" width="650"></p>
<p align="center">Microsoft Purview Data Map, Select Scan.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/557fffb9-19e5-4f41-82f6-34dea50e86ff" width="650"></p>
<p align="center">Microsoft Purview Data Map, Complete information required.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/a06303ae-5c46-4f15-8978-9aea774709ba" width="650"></p>
<p align="center">Microsoft Purview Data Map, Test connection.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/6e23ba65-7271-4614-bcae-705fad3458ab" width="650"></p>
<p align="center">Microsoft Purview Data Map, Scope your scan.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/55bb7e16-3bae-4c62-952b-5e85f7c3dd2e" width="650"></p>
<p align="center">Microsoft Purview Data Map, Select a scan rule set.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/25d2dc50-27cc-4ed3-a60c-6b31d2601b71" width="650"></p>
<p align="center">Microsoft Purview Data Map, Set a scan trigger.</p>
<br>


<p align="center">
<img src="https://github.com/user-attachments/assets/fc423a0e-9257-41b1-a661-65224496ca42" width="650"></p>
<p align="center">Microsoft Purview Data Map, Review your scan.</p>
<br>


<p align="center">
<img src="https://github.com/user-attachments/assets/2e55acee-86fe-4fa3-b44d-ebd076deae3f" width="650"></p>
<p align="center">Microsoft Purview Data Map, View details.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/1a6f1e8f-6984-437e-814f-cb9e27539dc2" width="650"></p>
<p align="center">Microsoft Purview Data Map, Scan queued.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/c73da4e4-92eb-49f5-9c4e-7005ed25c0e4" width="650"></p>
<p align="center">Microsoft Purview Data Map, Scan in progress.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/ab896ec7-e1e7-45c8-b48f-7faa67f769d6" width="650"></p>
<p align="center">Microsoft Purview Data Map, Scan completed.</p>
<br>
</details>

<br><br>
