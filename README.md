# Welcome to About Microsoft Purview Data Map

In this page I'll try to explain in an easy way how to set and configure the different conntectors.

We will show how to resolve this common scenario:
![image](https://github.com/user-attachments/assets/4d7be607-d3a8-4f97-a0b2-b0f5e7b7e692)

In the previous image we can see that we have:
- On-premises SQL
- Azure SQL using private endpoints
- Azure SQL using public access
- Azure Storage Blob using private endpoints
- Azure SQL using public access

Some capabilities that we will need to use are:
- Integration runtime
- Managed Virtual Network
- Azure Key-vault
- Azure Storage Accounts
- Some SQL commands

When you arrive for first time to Purview Portal it's possible that you cannot see Data Map option.

![image](https://github.com/user-attachments/assets/20d8b1b2-d625-4768-9fe2-606fcccaa4f3)

[Configure your Microsoft Purview Account](AboutPurviewDatamap/MicrosoftPurviewAccount.md)

After the account is created you will be able to see the option under Purview Portal

![image](https://github.com/user-attachments/assets/9d725627-6ee5-4884-bf3e-90672149de86)

Now we can go to the [Purview Portal](https://purview.microsoft.com) and start with this trip to [configure Purview Data Map](PurviewPortalConfiguration.md)
