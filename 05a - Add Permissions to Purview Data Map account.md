## Assigning the db_datareader Role to Microsoft Purview Account

In this step, we will grant the Microsoft Purview account the necessary permissions to scan the Azure SQL Database by assigning the db_datareader role. This role enables Purview to read all the data from the target database during the scan process.
1. **Connect to the Azure SQL Database :** Use Azure SQL Database Query Editor to connect to your database.
2. **Grant the db_datareader Role :** Execute the following SQL query to assign the db_datareader role to the Microsoft Purview account:
> To use lineage capabilitites you need to give db_owner permissions
```SQL
CREATE USER [Your Purview Account] FROM EXTERNAL PROVIDER  
GO  
EXEC sp_addrolemember 'db_owner', [Your Purview Account] 
GO
```

> To only scan your data with Microsoft Purview Data Mapa you need to assign only database data reader permission
```SQL
CREATE USER [Your Purview Account] FROM EXTERNAL PROVIDER  
GO  
EXEC sp_addrolemember 'db_datareader', [Your Purview Account] 
GO
```
> [!NOTE]
> Replace [Your Purview Account] with the actual name of your Microsoft Purview account.
3. **Verify the Role Assignment :** After executing the query, verify that the Purview account has been successfully assigned the db_datareader role.

By assigning this role, you ensure that Microsoft Purview Data Map can connect to the database and scan its contents.

Below are images to guide you through these steps visually.

<br>
<p align="center">
<img src="https://github.com/user-attachments/assets/94d003e2-5d65-4b4b-be96-d623af84ae9d" WIDTH="650"></p>
<p align="center">Azure SQL Database, connect to Query editor.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/ed666f01-3ae9-4b98-8ed0-5a5cc4fdc8c8" WIDTH="650"></p>
<p align="center">Azure SQL Database, New Query.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/7cd9076a-7b7d-4153-90b0-bbf5381fee22" WIDTH="650"></p>
<p align="center">Azure SQL Database, Set "db_datareader" role to Microsoft Purview account.</p>
<br>

<br><br>
