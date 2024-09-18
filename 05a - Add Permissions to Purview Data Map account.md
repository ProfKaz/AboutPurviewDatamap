## Adding SQL permissions to your MIcrosoft Purview Data Map account

![image](https://github.com/user-attachments/assets/94d003e2-5d65-4b4b-be96-d623af84ae9d)

![image](https://github.com/user-attachments/assets/ed666f01-3ae9-4b98-8ed0-5a5cc4fdc8c8)

To use lineage capabilitites you need to give db_owner permissions
```SQL
CREATE USER [Your Purview Account] FROM EXTERNAL PROVIDER  
GO  
EXEC sp_addrolemember 'db_owner', [Your Purview Account] 
GO
```

To only scan your data with Microsoft Purview Data Mapa you need to assign only database data reader permission
```SQL
CREATE USER [Your Purview Account] FROM EXTERNAL PROVIDER  
GO  
EXEC sp_addrolemember 'db_datareader', [Your Purview Account] 
GO
```

![image](https://github.com/user-attachments/assets/7cd9076a-7b7d-4153-90b0-bbf5381fee22)
