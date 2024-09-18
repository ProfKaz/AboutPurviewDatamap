# Troubleshooting

## SQL on-premises
If you are testing this configuration using a just installed SQL Server you need to enable some configuration to have access to the SQL

![image](https://github.com/user-attachments/assets/d430127f-f6ae-4f48-abf8-fc7aa3e18c23)

## Connect to Azure SQL Database

If you are not able to connect from Azure Portal to the Query Editor
![image](https://github.com/user-attachments/assets/c2523825-34c9-41e6-89fa-91ad6ef2a5fd)

![image](https://github.com/user-attachments/assets/377a7d30-cfcb-4cf6-a9bc-0095c02c2707)

![image](https://github.com/user-attachments/assets/5acd3b5b-f2ac-4963-8c2f-af50d1a7dcd9)

![image](https://github.com/user-attachments/assets/0854575c-e8ea-4761-8d83-8e87a9e4459f)

![image](https://github.com/user-attachments/assets/dcaa9930-3d39-46b6-88a5-e87c686fe57e)

## SQL Connection

![image](https://github.com/user-attachments/assets/6ec8d236-d33d-42dc-82a7-9ca02b072e59)

```SQL
CREATE USER [Your Purview Account] FROM EXTERNAL PROVIDER  
GO  
EXEC sp_addrolemember 'db_owner', [Your Purview Account] 
GO
```

![image](https://github.com/user-attachments/assets/90d40311-eae3-4376-88f4-0de227a8eae0)

![image](https://github.com/user-attachments/assets/b93b2d72-1d5d-4ed4-b2ec-122db2511808)
