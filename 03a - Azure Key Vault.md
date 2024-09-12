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

In general the steps are:
1. Go to the Azure Portal.
2. Search for Key Vaults and click Create.
3. Fill in the necessary details:
   - Subscription: Select your subscription.
   - Resource Group: Choose an existing one or create a new one.
   - Key Vault Name: Provide a unique name.
   - Region: Select your region.
4. Click Review + Create, and after validation, click Create.

You can see the images below to drive to you through the process. 

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

![image](https://github.com/user-attachments/assets/d0a243bf-98e6-4b3f-841e-ba705d47e4de)

![image](https://github.com/user-attachments/assets/42eb76fb-3362-4f4b-a261-82cb007265d9)

![image](https://github.com/user-attachments/assets/5300f4f8-0916-440a-887f-e3e8b1f6c504)

![image](https://github.com/user-attachments/assets/a9b8ab88-7ed1-4daf-bda1-33c8c8140e26)

![image](https://github.com/user-attachments/assets/4ae4e801-f95d-4d31-8551-52748061f750)

![image](https://github.com/user-attachments/assets/f3d4a3e9-d540-467f-9cec-65a6d5be6a9f)

</details>

<br>

<details>
<summary>Storing SQL On-Premises Credentials in Azure Key Vault</summary>

![image](https://github.com/user-attachments/assets/6dfee81b-b4f6-48a2-aa5f-aa999d70b696)

![image](https://github.com/user-attachments/assets/4cc42366-086d-4b95-85f1-0db204a9b4c8)

![image](https://github.com/user-attachments/assets/f76021d6-2e4d-4e83-a8a0-46e36af131bf)

![image](https://github.com/user-attachments/assets/bdc83629-44c9-4bcd-a047-212f18a4bd7a)

![image](https://github.com/user-attachments/assets/e1c1f140-63d2-4c2b-91b9-2a27698a8f2c)

</details>

<br>

<details>
<summary>Integrating Azure Key Vault with Microsoft Purview Data Map</summary>

![image](https://github.com/user-attachments/assets/8476e0d6-f4c3-4cfe-8aab-3a6701687444)

![image](https://github.com/user-attachments/assets/34e684b6-bbc0-4c21-9632-102fbf03c8b4)

![image](https://github.com/user-attachments/assets/f9598588-f71c-4d86-a98f-a568609de7a4)

![image](https://github.com/user-attachments/assets/ec80dad1-04bf-4176-b8d1-21a8e9eba8b7)

</details>

<br><br>
