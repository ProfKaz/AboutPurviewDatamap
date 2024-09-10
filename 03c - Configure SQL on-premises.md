## Configuring SQL On-premises to be accessed by Purview Data Map.

In this step, a SQL or Windows account must be configured for Microsoft Purview Data Map to use during the scan process. For this exercise, we will create a SQL account named "DataMap" and set a password. This password will later be securely stored in Step 03a under "Set SQL Authentication", where it will be used by Purview to authenticate and perform the scans.

The necessary permission for Microsoft Purview Data Map to execute the scan process is db_datareader. This role allows Purview to read all data from the targeted database during the scan.

In this step we will use Microsoft SQL Server management Studio to add a new account and set the permissions accordint to the images below. 

<p align="center">
<img src="https://github.com/user-attachments/assets/e372e357-130b-4ea6-af55-711d154d35b8" width="700"></p>
<p align="center">Microsoft SQL Server Management Studio, adding SQL account</p>

<br><br>

<p align="center">
<img src="https://github.com/user-attachments/assets/27b1218d-3b11-4fec-bc05-2e9e35f71740" width="700"></p>
<p align="center">Microsoft SQL Server Management Studio, setting db_datareader permission</p>

<br>
