# Go through baby steps

In this section I'll drive to you through all the procees to accomplish our final goal, explained in the [Readme](README.md) file.

Let's go:

1. You need to create a [Microsoft Purview Account](01%20-%20MicrosoftPurviewAccount.md) to have access to the Data Map option under Microsoft Purview portal.
2. Then we will need to access to the [Data Map](02%20-%20PurviewPortalConfiguration.md) feature to start configuring our environment
3. To access to our SQL on-premises:
   - Configure [Azure Key-Vault](03a%20-%20AzureKeyVault.md) to store our credentials, no matter if you use SQL or Windows Authentication at Key vault we will store the password for that account.
   - We will need to install and [configure Integration Runtime Agent](03b%20-%20IntegrationRuntime.md) this configuration permit to Purview Data Map to touch our on-premises SQL Servers
   - 
4. To access to our Azure Blob Storage:
   - In case of public or private endpoint we need to add the permisssion in the Azure Storage Account
   - In case of Public Access
5. 

