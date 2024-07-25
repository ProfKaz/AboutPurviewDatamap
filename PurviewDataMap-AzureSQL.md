## To connect Purview Data Map to Azure SQL

![image](https://github.com/user-attachments/assets/cc0f7b2b-430d-4f31-ba02-c66ac7c845a4)

![image](https://github.com/user-attachments/assets/c0a90972-8324-46ae-9af9-5d078f41941a)

## At SQL Configuration

![image](https://github.com/user-attachments/assets/edbe1469-3cea-470a-a34a-33022d9d20c8)

```SQL
CREATE USER [Your Purview Account] FROM EXTERNAL PROVIDER  
GO  
EXEC sp_addrolemember 'db_owner', [Your Purview Account] 
GO
```

![image](https://github.com/user-attachments/assets/90d40311-eae3-4376-88f4-0de227a8eae0)
