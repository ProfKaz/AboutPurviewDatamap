## Configuring Azure Key Vault to Store and Manage Passwords

In this section, we will walk through the steps required to configure Azure Key Vault, assign permissions for managing credentials, and grant Microsoft Purview access to retrieve and use those credentials.

Azure Key Vault is a service designed to securely store sensitive information such as passwords, API keys, certificates, and secrets, ensuring data protection through encryption and controlled access.

We will cover:

- Configuring Azure Key Vault
- Assigning the necessary permissions to manage credentials
- Granting access to Microsoft Purview so it can securely use the stored information

>[!NOTE]
> Ensure you have an Azure subscription and required permissions to create resources

<p align="center">
<img src="https://github.com/user-attachments/assets/496be512-c9f1-4f29-8175-6ced5ef86357" width="650"></p>
<p align="center">Microsoft Purview Data Map and Azure Key Vault to store SQL On-premises passwords.</p>

<br>

<details>
<summary>01 - Creating an Azure Key Vault</summary>
<br>

Follow these general steps to create an Azure Key Vault:
1. Go to the [Azure Portal](https://portal.azure.com).
2. Search for **Key Vaults** and click Create.
3. Fill in the necessary details:
   - Subscription: Select your subscription.
   - Resource Group: Choose an existing one or create a new one.
   - Key Vault Name: Provide a unique name for your Key Vault.
   - Region: Select the appropriate region for your resources.
4. Click **Review + Create**, and after validation, click **Create**.

For a visual walkthrough, refer to the images below that will guide you step by step through the process. 

<p align="center">
<img src="https://github.com/user-attachments/assets/8e61d13a-742f-4d92-94e4-37fde8c5bba7" width="650"></p>
<p align="center">Azure Portal.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/fc41c77a-149f-490a-b62c-5d8ea33425c5" width="650"></p>
<p align="center">Search for Key Vaults.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/7b3739b2-02ae-44f3-befa-074edcb224fa" width="650"></p>
<p align="center">Create a new Key vault.</p>
<br>


<p align="center">
<img src="https://github.com/user-attachments/assets/7bb432a3-db90-4630-b977-769509b3dbad" width="650"></p>
<p align="center">Fill in the necessary details.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/6af97abb-eb6d-4d65-846c-f7aecd26a23d" width="650"></p>
<p align="center">Access configuration.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/ff67f99a-a2dd-4b91-92e8-cf8b61fbb33a" width="650"></p>
<p align="center">Network configuration.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/61ba0767-d879-4789-9650-1d59f81559b9" width="650"></p>
<p align="center">Review and Create.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/27f44682-e57d-41cf-8c15-c15db26cc844" width="650"></p>
<p align="center">Deployment progress.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/01d955e7-b370-4fcc-8c0f-90fab8fb0dda" width="650"></p>
<p align="center">Deployment completed.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/a6570a1e-e761-4ed8-8120-96d954e98685" width="650"></p>
<p align="center">Key Vault main interface.</p>
<br>

</details>

<br>

<details>
<summary>02 - Adding Permissions to Azure Key Vault for Credential Management</summary>
<br>

In this step, we will assign the **Key Vault Administrator** role to your account, which is necessary for securely storing SQL Server on-premises credentials in Azure Key Vault. To do this, follow these steps:
1. In the **Key Vault console**, navigate to **Access control (IAM)**.
2. Click **+ Add** and select **Add role assignment**.
3. Choose **Key Vault Administrator**, then click **Next**.
4. Click **+ Select memebers**.
5. In the right-hand menu, search for your account and select it to assign the administrator role.
6. Finally, press **Review + assign** twice to complete the process.

For a visual walkthrough, refer to the images below that will guide you step by step through the process.
   
<br>
   
<p align="center">
<img src="https://github.com/user-attachments/assets/c342f048-88d9-4e5b-8c42-4ba07154d9e6" width="650"></p>
<p align="center">Key Vault Access control (IAM) menu.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/6520a378-d8b6-4547-855b-801b61f2c7bb" width="650"></p>
<p align="center">Key Vault, Add role assignment (Key Vault Admimnistrator).</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/06a5bc8f-9ea3-4e15-a57d-b0e4d117c11d" width="650"></p>
<p align="center">Key Vault, Select members to assign role.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/0f48afb6-4fb7-4ae0-9982-5911b2f48a71" width="650"></p>
<p align="center">Key Vault, Search for the users.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/d0525a29-c52c-40cd-a26c-e2d9908d3aa3" width="650"></p>
<p align="center">Key Vault, Review and assign.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/ac3f3895-4e71-46c1-b6b4-cf501718fb97" width="650"></p>
<p align="center">Key Vault, Assign summary.</p>
<br>

</details>

<br>

<details>
<summary>03 - Granting Microsoft Purview Data Map Access to Azure Key Vault</summary>
<br>

In this step, we will assign the **Key Vault Secrets User** role to your account. This role is required to allow Microsoft Purview Data Map to access and retrieve credentials stored in Azure Key Vault. To do this, follow these steps
1. In the **Key Vault console**, navigate to **Access control (IAM)**.
2. Click **+ Add** and select **Add role assignment**.
3. Choose **Key Vault Secrets User**, then click **Next**.
4. Click **+ Select memebers**.
5. In the right-hand menu, search for the Microsoft Purview Account created during [Step 01](01%20-%20MicrosoftPurviewAccount.md) and select it to assign the administrator role.
6. Finally, press **Review + assign** twice to complete the process.

For a visual walkthrough, refer to the images below that will guide you step by step through the process.

<br>
   
<p align="center">
<img src="https://github.com/user-attachments/assets/d0a243bf-98e6-4b3f-841e-ba705d47e4de" width="650"></p>
<p align="center">Key Vault Access control (IAM) menu.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/42eb76fb-3362-4f4b-a261-82cb007265d9" width="650"></p>
<p align="center">Key Vault, Add role assignment (Key Vault Secrets User).</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/5300f4f8-0916-440a-887f-e3e8b1f6c504" width="650"></p>
<p align="center">Key Vault, Select members to assign role.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/a9b8ab88-7ed1-4daf-bda1-33c8c8140e26" width="650"></p>
<p align="center">Key Vault, Search for the Microsoft Purview Account.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/4ae4e801-f95d-4d31-8551-52748061f750" width="650"></p>
<p align="center">Key Vault, Review and assign.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/f3d4a3e9-d540-467f-9cec-65a6d5be6a9f" width="650"></p>
<p align="center">Key Vault, Assign summary.</p>
<br>

</details>

<br>

<details>
<summary>04 - Storing SQL On-Premises passwords in Azure Key Vault for Use with Microsoft Purview Data Map</summary>
<br>

With all the necessary permissions assigned, we can now proceed to store the passwords required for **Microsoft Purview Data Map**. In this case, we will store the password created in [Step 03c](03c%20-%20Configure%20SQL%20on-premises.md) of this guide. To store the password in **Azure Key Vault**, follow these steps:
1. In the **Key Vault console**, expand **Objects** and navigate to **Secrets**.
2. Click **+ Generate/Import**
3. Fill in the necessary details:
   - **Upload options:** Keep Manual as the default setting.
   - **Name:** Provide a clear and descriptive name for the secret. This name will be referenced later in the final step of this section.
   - **Secret value:** Enter your SQL account password (the same one created in [Step 03c](03c%20-%20Configure%20SQL%20on-premises.md)).
   - Leave the remaining options as is and click **Create**.

<br>
   
<p align="center">
<img src="https://github.com/user-attachments/assets/48b7831d-3761-4dc7-b26b-8ba674c80812" width="650"></p>
<p align="center">Key Vault console.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/4cc42366-086d-4b95-85f1-0db204a9b4c8" width="650"></p>
<p align="center">Key Vault Secrets menu.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/f76021d6-2e4d-4e83-a8a0-46e36af131bf" width="650"></p>
<p align="center">Key Vault, Create a secret.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/bdc83629-44c9-4bcd-a047-212f18a4bd7a" width="650"></p>
<p align="center">Key Vault, fulfil the information required.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/e1c1f140-63d2-4c2b-91b9-2a27698a8f2c" width="650"></p>
<p align="center">Key Vault, secret created.</p>
<br>

</details>

<br>


<details>
<summary>05 - Connecting Microsoft Purview Data Map to Azure Key Vault</summary>
<br>

To start using the credentials stored in Azure Key Vault, follow these steps
1. In **Microsoft Purview Data Map**, expand **Source management** and navigate to **Credentials**.
2. Click **Manage Key Vault connections**
3. In the pane on the right, Click **+ New** and fill in the required details:
   - **Name:** Enter a clear and descriptive name
   - **Description:**(Optional) While not mandatory, providing a description can be helpful for future reference.
   - **Select a domain:** Use the domain created in [Step 02](02%20-%20PurviewPortalConfiguration.md).
   - **Azure subscription:** Select the subscription where the Key Vault was created, or keep All to view all available options.
   - **Key Vault name:** Select the Key Vault name created earlier in this section.
4. Click **Create**
5. After completing the setup, click **Close**.

<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/35e83205-c6d7-4a69-96c7-794e5a51e889" width="650"></p>
<p align="center">Microsoft Purview Data Map, Credentials menu.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/99fb5500-2a81-4cbf-8800-3128089c1fe5" width="650"></p>
<p align="center">Microsoft Purview Data Map, Manage Key Vault connections.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/3d3515af-d31d-4f86-936d-fa8c39ac1525" width="650"></p>
<p align="center">Microsoft Purview Data Map, New Key Vault.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/8b4c9f8b-ef40-4ba6-b305-a3ae9a024ea2" width="650"></p>
<p align="center">Microsoft Purview Data Map, Adding Key Vault values.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/2cca9c8e-53c3-45d3-899a-f9718be8bffa" width="650"></p>
<p align="center">Microsoft Purview Data Map, Key Vault connection created</p>
<br>

</details>

<br>

<details>
<summary>06 - Connecting Microsoft Purview Data Map to Azure Key Vault for Password Access</summary>
<br>

In this final step, we will establish the connection between Microsoft Purview Data Map and Azure Key Vault to securely access the stored passwords. To achieve this, follow these steps:
1. In **Microsoft Purview Data Map**, expand **Source management** and navigate to **Credentials**.
2. Click **+ New**
3. In the pane on the right, fill in the required details:
   - **Name:** Enter a clear and descriptive name.
   - **Description:**(Optional) While not mandatory, providing a description can be helpful for future reference.
   - **Select a domain:** Use the domain created in [Step 02](02%20-%20PurviewPortalConfiguration.md).
   - **Authentication method:** Choose **SQL Authentication**.
   - **User name:** Enter the username set in [Step 03c](03c%20-%20Configure%20SQL%20on-premises.md).
   - **Key Vault connection:** Select the connection created earlier in this section.
   - **Secret name:** Enter the secret name used when storing the SQL password in Key Vault.
   - **Secret version:** Leave this field blank unless you have multiple versions for a same Secret name.
4. Click **Create**.

<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/8476e0d6-f4c3-4cfe-8aab-3a6701687444" width="650"></p>
<p align="center">Microsoft Purview Data Map, Credentials menu.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/34e684b6-bbc0-4c21-9632-102fbf03c8b4" width="650"></p>
<p align="center">Microsoft Purview Data Map,  New credentials.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/f9598588-f71c-4d86-a98f-a568609de7a4" width="650"></p>
<p align="center">Microsoft Purview Data Map, Adding your SQL Server on-premises credentials.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/ec80dad1-04bf-4176-b8d1-21a8e9eba8b7" width="650"></p>
<p align="center">Microsoft Purview Data Map, New credential created.</p>
<br>

</details>

<br><br>
