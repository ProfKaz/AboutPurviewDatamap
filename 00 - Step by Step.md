## Let's walk through this process step by step

In this section I'll drive to you through all the procees to accomplish our final goal, explained in the [Readme](README.md) file.

Let's go:

1. You need to create a [Microsoft Purview Account](01%20-%20MicrosoftPurviewAccount.md) to have access to the Data Map option under Microsoft Purview portal.
2. Then we will need to access to the [Data Map](02%20-%20PurviewPortalConfiguration.md) feature to start configuring our environment
3. To access to our SQL on-premises:
   - **[Azure Key Vault](03a%20-%20Azure%20Key%20Vault.md) :** Used to securely store SQL credentials (both SQL and Windows authentication).
   - **[Microsoft Integration Runtime](03b%20-%20IntegrationRuntime.md) :** Install a dedicated server or cluster (in production) to run the Integration Runtime, which enables Microsoft Purview Data Map to access your on-premises SQL servers.
   - **[SQL Permissions](03c%20-%20Configure%20SQL%20on-premises.md) :** Create or assign an account to your SQL Servers or Databases with at least the db_datareader role, ensuring the ability to read and scan data.
   - **[Purview Connection](03d%20-%20Add%20SQL%20On-premises%20to%20DataMap.md) :** Connect the SQL servers to Microsoft Purview Data Map via the Integration Runtime, using the credentials securely stored in Azure Key Vault.
4. To access to our Azure Blob Storage:
   - In case of public or private endpoint we need to add the permisssion in the Azure Storage Account
   - In case of Public Access
   - Configure
   - Register Azure Blob Storage
   - 
5. 

