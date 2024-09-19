## Registering an Azure Blob Storage in Purview Data Map

### Steps to Register Azure Blob Storage in Microsoft Purview Data Map:

1. Navigate to the Data Map in the Microsoft Purview Portal.
2. Select Data sources on the left side.
3. Under Register data source, search for and select **Azure Blob Storage**.
4. In the next step, provide the following information:
   - **Data source name:** Enter a descriptive name, such as the server name.
   - **Storage account name:** Select the proper Storage account that you want to scan.
   - **Endpoint:** Is selected automatically based in your Storage account previosuly defined.
   - **Domain:** Select an existing domain or one created in [Step 2](02%20-%20PurviewPortalConfiguration.md) of this guide.
   - **Collection:** Choose the collection previously created in [Step 2](02%20-%20PurviewPortalConfiguration.md) of this guide.
   - Press Register

### Setting Up the Scan Service for Azure Blob Storage:

1. Press the scan icon (a small circular blue icon).
2. Complete the following information:
   - **Name:** Use the default name or enter a custom one.
   - **Connect with integration runtime:** Use the default selection, except if you are using [Private Enpoint](06%20-%20Connect%20Microsoft%20Purview%20Data%20Map%20to%20Private%20Endpoint.md) in that case select the right one.
   - **Credential:** Use Microsoft Purview MSI (system). 
   - **Scan level:** Use the default selection.
   - **Domain:** This will be selected by default.
   - **Collection:** Select the collection created in [Step 2](02%20-%20PurviewPortalConfiguration.md).
3. Press test connection to validate your configuration and then Continue.
4. Scope your scan: Optionally, select specific containers to reduce the scope of the scan.
5. Select a scan rule set: Choose the default AzureStorage rule set.
6. Set a scan trigger: Schedule your scan. For example, set it to run daily.
7. Press Save and Run. If you do not want to run the scan immediately, click the arrow next to the button and select Save only.

After completing these steps, you can monitor the scan progress and view the results once the process is complete. 

<details>
<summary>01 - Steps to Register Azure Blob Storage in Microsoft Purview Data Map.</summary>
<br>
<p align="center">
<img src="https://github.com/user-attachments/assets/2b0cda3d-08f2-4d40-9cdf-6af390c98fa2" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Data sources.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/6e2bab55-e356-4b50-9644-11272af3b4a0" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Register data sources.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/0aeb3d6c-04d7-4ff6-9440-dfcf34ff21a6" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Select Azure Blob Storage.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/734a79f3-350b-40e2-aa7d-808d0e77a869" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Register data source (Azure Blob Storage).</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/6161f26e-74cf-4967-b66e-bd681ff23679" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Complete with your Azure Blob Storage information.</p>
<br>
</details>

<br>

<details>
<summary>02 - Setting Up the Scan Service for Azure Blob Storage.</summary>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/387089d4-f731-4b22-ab36-18f38f7b1efd" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Select the Scan button.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/931d9b8c-d0ac-4943-aada-10abd910e075" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Configure Scan settings.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/3355c2bf-49fb-4b18-8cb2-5f047061a50e" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Test connection to your Azure Blob Storage.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/8990826a-cfe5-41ff-a77a-995baf591d90" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Test connection successful.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/695b9547-4d2e-48d4-ab62-b5382187a700" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Scope your scan.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/b6278bae-d9ac-4b6a-9a9a-b9f76cc12f49" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Select a scan rule set.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/20a26605-cfe0-406a-a2af-69a1cc80521d" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Set a scan trigger.</p>
<br>


<p align="center">
<img src="https://github.com/user-attachments/assets/3dddf0ac-1f2a-4118-8d7a-590375f4d3b6" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Save and run.</p>
<br>


<p align="center">
<img src="https://github.com/user-attachments/assets/627086fa-82d6-4743-8c21-029dfae5f381" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Scan progress.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/046d366e-f790-46f5-9da2-7557f5b74991" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map, Scan completed.</p>
<br>

</details>

<br><br>
