## Let’s Walk Through This Step by Step

In this section, I'll guide you through the entire process to achieve our final goal, as outlined in the  [Readme](README.md) file.

Ready? Let’s go!

1. **[Create a Microsoft Purview Account](01%20-%20MicrosoftPurviewAccount.md) :** This is your first step. Once you have your Purview account, you'll have access to the Data Map option within the Purview portal, which is where the magic happens.
2. **[Access the Data Map feature](02%20-%20PurviewPortalConfiguration.md) :** After setting up your account, it's time to dive into the Data Map feature to start configuring your environment.
3. **[Accessing SQL On-Premises](03%20-%20On-premises%20connections.md)** To connect your on-premises SQL servers to Purview, we need a few components in place:
   - **[Azure Key Vault](03a%20-%20Azure%20Key%20Vault.md) :** This will securely store SQL credentials, whether you're using SQL or Windows authentication.
   - **[Microsoft Purview Integration Runtime](03b%20-%20IntegrationRuntime.md) :** Set up a dedicated server or a cluster (for production environments) to install and run the Integration Runtime. This is the bridge that allows Purview Data Map to reach your on-premises SQL servers.
   - **[SQL Permissions](03c%20-%20Configure%20SQL%20on-premises.md) :** Make sure you create or assign an account in your SQL Servers or Databases with at least the **db_datareader** role. Without this, scanning and reading the data just won’t happen!
   - **[Purview Connection](03d%20-%20Add%20SQL%20On-premises%20to%20DataMap.md) :** Now comes the fun part—connecting **SQL servers** to **Microsoft Purview Data Map** through the **Integration Runtime** using the credentials you've securely stored in **Azure Key Vault**.
4. **[Accessing Azure Blob Storage](04%20-%20Azure%20Blob%20Storage.md)** Let’s not forget about your Blob Storage:
   - First, **[add permissions](04a%20-%20Add%20Permissions%20to%20Purview%20Data%20Map%20account.md)** to allow Purview Data Map to access and read from your Blob storage.
   - Then, **[register](04b%20-%20Register%20Azure%20Blob%20Storage%20to%20Scan.md)** the Blob Storage within Purview Data Map and start scanning!
5. **[Accessing Azure SQL Database](05%20-%20Azure%20SQL%20Database.md)** Similar steps apply for your Azure SQL Database:
   - **[Grant permissions](05a%20-%20Add%20Permissions%20to%20Purview%20Data%20Map%20account.md)** to let Purview access and read from your database.
   - Once permissions are set, **[register](05b%20-%20Register%20Azure%20SQL%20Database%20to%20Scan.md)** your Azure SQL Database in Purview and kick off the scan!
6. Using **[Private Endpoints with Microsoft Purview Data Map]()** If you want to leverage Private Endpoints, there are a few more steps:
   - Configuring Managed Virtual Network
   - Connect to your Azure Blob Storage Private Endpoint
   - Connect to your Azure SQL Database Private Endpoint

<br><br>
