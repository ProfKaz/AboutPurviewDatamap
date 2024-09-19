## Azure SQL Database Integration

In this section, we’ll walk through the steps required to enable Microsoft Purview Data Map to scan your **Azure SQL Database**.

To achieve this, follow these steps:
1. **[Set Up an Azure SQL Server and Database](Additional%20Information/CreateAzureSQLServerAndSampleDataBase.md) :** Ensure you have an **Azure SQL Server** configured, along with the **Azure SQL Database** that you want to scan. The SQL Server acts as the host for your database.
2. **[Assign Permissions](05a%20-%20Add%20Permissions%20to%20Purview%20Data%20Map%20account.md) :** Grant the necessary permissions to your **Microsoft Purview account** at the **Azure SQL Database** level. This involves assigning the **db_datareader** role to the Purview-managed identity, which will allow Purview to read and scan the data in your **Azure SQL Database**.
3. **[Register Azure SQL Database in Microsoft Purview Data Map](05b%20-%20Register%20Azure%20SQL%20Database%20to%20Scan.md) :** Once permissions are set, go to the Microsoft Purview portal, access the Data Map, and register your Azure SQL Database as a data source. Provide details like the server name, database name, and the authentication method.

<br>
<p align="center">
<img src="https://github.com/user-attachments/assets/c85218f5-1497-4299-aa96-ffe6c9c2a1b1" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map scan Azure SQL Database.</p>

<br><br>
