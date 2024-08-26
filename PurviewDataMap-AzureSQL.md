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

```SQL
CREATE USER [Your Purview Account] FROM EXTERNAL PROVIDER  
GO  
EXEC sp_addrolemember 'db_datareader', [Your Purview Account] 
GO
```

![image](https://github.com/user-attachments/assets/90d40311-eae3-4376-88f4-0de227a8eae0)

![image](https://github.com/user-attachments/assets/b3890cee-4002-4182-aa69-0146dfe296ff)

![image](https://github.com/user-attachments/assets/5c9a1063-211e-4035-b392-825a5ee9bcd5)

![image](https://github.com/user-attachments/assets/50453e22-e643-4c13-a913-5675dbf0ce53)

![image](https://github.com/user-attachments/assets/c1a6f39f-54a5-451f-8b25-6f1d3174dcf7)

![image](https://github.com/user-attachments/assets/39faaea9-1990-4568-97ef-c04693c90f77)
