## Azure Blob Storage integration

In this section, we’ll walk through the steps required to enable Microsoft Purview Data Map to scan your Azure Blob Storage environment.

To successfully integrate Azure Blob Storage with Purview, follow these steps:
1. **[Set Up a Storage Account](Additional%20Information/CreateAndUseAzureStorageAccount.md) :** Ensure you have an Azure Storage Account that supports Blob Storage. This account will house the blobs that you wish to scan and manage using Purview.
2. **[Assign Permissions](04a%20-%20Add%20Permissions%20to%20Purview%20Data%20Map%20account.md) :** Grant the appropriate permissions at the Storage Account level to your Microsoft Purview account. The Purview account will need read access to the Blob Storage for successful scanning. You can achieve this by assigning the Storage Blob Data Reader role to the Purview-managed identity or service principal.
3. **[Register Azure Blob Storage in Microsoft Purview Data Map](04b%20-%20Register%20Azure%20Blob%20Storage%20to%20Scan.md) :** After permissions are set, go to the Microsoft Purview portal, navigate to the Data Map, and register your Azure Blob Storage as a data source. During registration, you’ll provide necessary details such as the Storage Account name and the access method.

<br>
<p align="center">
<img src="https://github.com/user-attachments/assets/6ea66a05-234f-44a7-958e-328e34708794" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map scan Azure Blob Storage</p>

<br><br>
