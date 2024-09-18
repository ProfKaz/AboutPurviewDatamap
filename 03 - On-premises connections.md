## On-premises integration

In this section, we will outline the steps required to enable Microsoft Purview Data Map to scan your SQL on-premises environment.

To accomplish this, you will need to implement the following:
1. **[Azure Key Vault](03a%20-%20Azure%20Key%20Vault.md) :** Used to securely store SQL credentials (both SQL and Windows authentication).
2. **[Microsoft Purview Integration Runtime](03b%20-%20IntegrationRuntime.md) :** Install a dedicated server or cluster (in production) to run the Integration Runtime, which enables Microsoft Purview Data Map to access your on-premises SQL servers.
3. **[SQL Permissions](03c%20-%20Configure%20SQL%20on-premises.md) :** Create or assign an account to your SQL Servers or Databases with at least the db_datareader role, ensuring the ability to read and scan data.
4. **[Purview Connection](03d%20-%20Add%20SQL%20On-premises%20to%20DataMap.md) :** Connect the SQL servers to Microsoft Purview Data Map via the Integration Runtime, using the credentials securely stored in Azure Key Vault.
<br>
<p align="center">
<img src="https://github.com/user-attachments/assets/aabcb862-cc68-4db1-ac14-38d05476f6c5" WIDTH="700"></p>
<p align="center">Microsoft Purview Data Map scan SQL On-premises</p>

<br>
