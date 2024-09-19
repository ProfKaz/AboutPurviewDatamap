## To start Scanning an Azure Blob Storage with Microsoft Purview

To successfully scan an Azure Blob Storage using Microsoft Purview, follow these steps:
1. Open Storage Accounts in the Azure Portal.
2. Select the Storage Account that contains the Blob Storage you wish to scan.
3. Navigate to Access Control (IAM) from the left-hand menu.
4. Click **+ Add** and select **Add role assignment**.
5. In the role selection window, search for **Storage Blob Data Reader**, and select it.
6. Under the Members section, click Select members.
7. Search for your Microsoft Purview account (this could be the managed identity or service principal you’ve set up) and select it.
8. Complete the process by reviewing your selections and clicking **Review + Assign**.

Below is a visual guide to assist you in completing these steps.
<br>

<details>
<summary>Adding Azure Storage Blob Data Reader role to your Microsoft Purview account</summary>

<br>
<p align="center">
<img src="https://github.com/user-attachments/assets/bb760243-decd-467f-b668-a712a5749631" WIDTH="650"></p>
<p align="center">Azure Portal, Search Storage account.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/e845ae4e-0f5e-4b06-928a-3dc837d7a308" WIDTH="650"></p>
<p align="center">Storage accounts, select storage account.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/f880e66b-efa0-4de3-bdf3-e850c9866ea2" WIDTH="650"></p>
<p align="center">Storage account, select Access Control (IAM).</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/1af6d8b7-0e08-4342-873b-b06a1719719c" WIDTH="650"></p>
<p align="center">Storage account, Add role assignment.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/0d05eb77-065b-4095-858d-e313bb138b4a" WIDTH="650"></p>
<p align="center">Storage account, select Storage Blob Data Reader role.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/aeb254ad-f9ab-46a4-8a54-9bb1d8f33298" WIDTH="650"></p>
<p align="center">Storage account, select member to assign role.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/3d11bc70-2f78-4850-a267-2c1b482e1e4e" WIDTH="650"></p>
<p align="center">Storage account, Microsoft Purview Data Map account selected.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/12de4803-8458-4ba9-814f-c312e32d3c36" WIDTH="650"></p>
<p align="center">Storage account, Review and Assign role.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/528c403b-6d6a-4c03-b4f4-68d6af072c06" WIDTH="650"></p>
<p align="center">Storage account, Review and Assign role.</p>
<br>

</details>

<br><br>
