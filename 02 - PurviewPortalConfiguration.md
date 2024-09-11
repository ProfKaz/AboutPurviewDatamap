## New Microsoft Purview Portal

You can access to Data Map through the [New Microsoft Purview Portal](https://purview.microsoft.com)

### Values used in this implementation
```JSON
{
  "Microsoft Purview Account" : "KazDemosDataMap",
  "Storage Account(for Azure RBAC)" : "storagedisk0001",
  "storagedisk0001 - Blob Container" : "demofolder",
  "Storage Account(for Key Vault)" : "storagedisk0002",
  "storagedisk0002 - Blob Container" : "demofolder",
  "Key vault" : "DataMapKeys",
  "Managed Identities" : "ManagedIdentityDataMap"
}
```

### Azure services used in this implementation

In this implementation, we focus on using **Azure RBAC** to simplify identity management. The only exception is for **SQL on-premises**, where we will use passwords, which will be securely stored in **Azure Key Vault**.

> If you want to use Purview Data Map using only Azure Role-Based Access Control these are required:
- Microsoft Purview accounts
- Azure SQL
- Storage accounts

> If you want to use Purview Data Map to scan SQL servers on-premises, you will need additional service:
- Key vaults

<p align="center">
<img src="https://github.com/user-attachments/assets/cbea0e7e-f4e7-4990-bf85-b139b48fbc88" width="650"></p>
<p align="center">Microsoft Purview Data Map</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/1dd0b2dd-c4f6-4dc8-a5a5-fc48fa46e2b8" width="650"></p>
<p align="center">Microsoft Purview Data Map, Domains menu</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/0ea8799b-c0fa-4361-9f81-5765f3c3caef" width="650"></p>
<p align="center">Microsoft Purview Data Map, New collection</p>
<br>

We will create New Collections for:
- Azure Blob Storage
- Azure SQL DB
- SQL Server on-premises

<br><br>
