## Microsoft Integration Runtime for Accessing SQL On-Premises

To enable Microsoft Purview Data Map to access SQL on-premises, you need to install Microsoft Integration Runtime. This acts as a proxy or bridge, allowing secure communication between Purview and your on-premises SQL servers.

<p align="center">
<img src="https://github.com/user-attachments/assets/b5cc3033-56e8-4934-9b65-394e24f0191f" width="650"></p>
<p align="center">Microsoft Purview Data Map and Microsoft Integration Runtime</p>

<br>

<details>
<summary>01 - Setting Up the Microsoft Integration Runtime Agent</summary>
<br>

To configure Microsoft Integration Runtime for accessing SQL on-premises, follow these steps:
1. Connect to [Microsoft Purview Portal](https://purview.microsoft.com) and navigate to **Data Map**.
2. Expand **Source Management** and select **Integration runtimes**
3. Click **+ New**
4. In the pane on the right, select **Self-Hosted** and click **Continue**.
5. Complete the required information:
   - **Integration runtime name:** Enter a clear and descriptive name.
   - Description: (Optional) While not mandatory, adding a description can be helpful for future reference.
6. Leave the remaining options as default and click **Create**.
7. To finalize this part of the setup:
   - Download the [Microsoft Purview Integration Runtime](https://www.microsoft.com/en-us/download/details.aspx?id=105539) to install it locally (more details in the next section).
   - Save one of the **keys**, as it will be required in a later step.
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/c00923a6-69e5-4ea9-83c3-87d50f356e3f" width="650"></p>
<p align="center">Microsoft Purview Portal.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/e512596b-c4ed-42ec-8cb1-f063647c188d" width="650"></p>
<p align="center">Microsoft Purview Data Map console.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/8bb88ab0-26f3-4a73-a480-5802caf7330e" width="650"></p>
<p align="center">Microsoft Purview Data Map, Integration runtimes.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/8f7781f1-078e-4827-ba1c-efc60f4e8854" width="650"></p>
<p align="center">Microsoft Purview Data Map, New integration runtimes.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/87ba8df1-9d1a-4651-89fc-1efd1db9b67a" width="650"></p>
<p align="center">Microsoft Purview Data Map, New integration runtimes configuration.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/9f0c4e18-1ce0-454d-9df3-db02749b774b" width="650"></p>
<p align="center">Microsoft Purview Data Map, Integration runtimes configuration.</p>
<br>

</details>

<br>

<details>
<summary>02 - Downloading and Installing the Microsoft Purview Integration Runtime Agent</summary>
<br>

To install the Microsoft Purview Integration Runtime, follow these steps:
1. Download the latest version of [Microsoft Purview Integration Runtime](https://www.microsoft.com/en-us/download/details.aspx?id=105539) from the official Microsoft website.
2. Run the installer by double-clicking the downloaded file.
3. Follow the prompts and select the default configuration settings during installation.
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/401a4d12-5263-400f-93a0-cb5be5c00f10" width="650"></p>
<p align="center">Download Microsoft Purview Integration Runtime.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/a804673e-237d-4cdc-96bc-ffe174b21475" width="650"></p>
<p align="center">Download Microsoft Purview Integration Runtime, choose the latest version.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/ce812ebf-a531-449e-8a15-a328a0690bc8" width="650"></p>
<p align="center">Microsoft Purview Integration Runtime, installer downloaded.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/b1dc0495-887b-4471-a438-6dc50f6fcd44" width="650"></p>
<p align="center">Microsoft Purview Integration Runtime, executing installer.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/b3e8055c-847d-4c88-a413-6627c117164b" width="300"></p>
<p align="center">Microsoft Purview Integration Runtime installation, End-User License Agreement.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/32e5b76d-c851-4140-8ff9-5583f7c1423f" width="300"></p>
<p align="center">Microsoft Purview Integration Runtime installation, Destination Folder.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/e6035c21-4187-4e93-a00b-80bd82c02580" width="300"></p>
<p align="center">Microsoft Purview Integration Runtime installation, Install.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/e12c652a-bbe8-4778-b805-a153c737e1c9" width="300"></p>
<p align="center">Microsoft Purview Integration Runtime installation, Installation progress.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/edbed469-8765-45ea-a89b-c2a4d7b32e6e" width="300"></p>
<p align="center">Microsoft Purview Integration Runtime installation, Installation completed.</p>
<br>

</details>

<br>

<details>
<summary>03 - Configuring Microsoft Integration Runtime agent</summary>
<br>

To configure the Microsoft Purview Integration Runtime, follow these steps:
1. Open the **Windows menu**, search for **Microsoft Integration Runtime Configuration Manager**, and launch the application.
2. On the first run, you will need to enter the key you saved earlier during setup.
   - If you don’t have the key, you can retrieve it from Microsoft Purview Data Map under Source Management → Integration Runtimes (see the image below for reference).
4. Enter the key and click **Register**
5. In the next window, choose whether to enable the option **"Enable remote access from intranet"**.
6. Click **Finish**.
7. Once the configuration is validated, you should see a confirmation message indicating that the Integration Runtime is **successfully** connected.
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/954ba7db-d729-484e-bbcb-1d39d0b8e4f0" width="650"></p>
<p align="center">Microsoft Purview Integration Runtime, First run.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/ea3e9b67-4651-47e6-a8c6-d61cd0472132" width="650"></p>
<p align="center">Microsoft Purview Integration Runtime, Get Integration runtime key.</p>
<br>


<p align="center">
<img src="https://github.com/user-attachments/assets/655ada04-5bdf-4fcc-9325-befaeeb1d7ba" width="650"></p>
<p align="center">Microsoft Purview Integration Runtime, Set Integration runtime key.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/6af59667-a723-4ce7-8c15-b6b6cca21321" width="400"></p>
<p align="center">Microsoft Purview Integration Runtime, Finish configuration.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/3c2d8d43-bd80-4ea7-b2f4-ead0c239ffe3" width="400"></p>
<p align="center">Microsoft Purview Integration Runtime, Registering process.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/2278bc59-2f39-443e-9a36-fb1d38ac777f" width="400"></p>
<p align="center">Microsoft Purview Integration Runtime, Registration sucesfully.</p>
<br>

</details>

<br>

<details>
<summary>04 - Validating Microsoft Integration Runtime agent status</summary>
<br>

To check the correct deploy for Microsoft Purview Integration Runtime, follow these steps:
1. Connect to [Microsoft Purview Portal](https://purview.microsoft.com) and navigate to **Data Map**.
2. Expand **Source Management** and select **Integration runtimes**
3. If it's required, click **Refresh** to update the status.
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/166fa35d-6ea1-4fbd-9ea7-8320b99c06cc" width="650"></p>
<p align="center">Microsoft Purview Data Map, Integration Runtime refresh status.</p>
<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/f68f51e0-5631-4267-ace8-ce620e701124" width="650"></p>
<p align="center">Microsoft Purview Data Map, Integration Runtime status running.</p>
<br>

</details>

<br><br>
