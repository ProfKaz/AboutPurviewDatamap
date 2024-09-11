# Welcome to all about Microsoft Purview Data Map

In this guide, I aim to provide a clear and straightforward explanation of how to set up and configure the various connectors available in Microsoft Purview Data Map. These connectors allow Microsoft Purview to seamlessly integrate with a wide range of data sources, ensuring comprehensive data discovery, classification, and governance.

We will walk through a common real-world scenario where Microsoft Purview is used to scan and manage data across different environments, including cloud-based and on-premises systems. Throughout this guide, you will learn:

- How to configure connectors for different data sources.
- How to handle authentication and permissions for secure access.
- How to troubleshoot common issues during the setup.

By the end of this section, you will have a solid understanding of how to integrate and manage your data sources within Microsoft Purview, enabling efficient and secure data governance across your organization.

We will demonstrate how to address this common scenario:
<p align="center">
<img src="https://github.com/user-attachments/assets/3c509726-3667-40f9-b6b8-d3558450de37" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map main scenario</p>

In the previous image, we can observe that we have:
- On-premises SQL
- Azure SQL using private endpoints
- Azure SQL using public access
- Azure Storage Blob using private endpoints
- Azure Storage Blob using public access

Some capabilities that we will need to use are:
- [Microsoft Integration Runtime](https://www.microsoft.com/en-us/download/details.aspx?id=39717)
- Managed Virtual Network
- Azure Key-vault
- Azure Storage Accounts
- Some SQL commands

When you arrive for first time to Purview Portal it's possible that you cannot see Data Map option.
<p align="center">
<img src="https://github.com/user-attachments/assets/20d8b1b2-d625-4768-9fe2-606fcccaa4f3" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map Portal</p>

[Getting Started with Configuring Microsoft Purview Data Map](00%20-%20Step%20by%20Step.md)

After the account is created you will be able to see the option under Purview Portal

<p align="center">
<img src="https://github.com/user-attachments/assets/9d725627-6ee5-4884-bf3e-90672149de86" WIDTH="650"></p>
<p align="center">Microsoft Purview Data Map access menu</p>

Now we can go to the [Purview Portal](https://purview.microsoft.com) and start with this trip to configure Purview Data Map.

<br>
<br>
