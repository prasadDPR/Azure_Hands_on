# AzureSQLdatabase_connect_via_SSMS
Connect Azure SQL Database using SQL Server Management Studio (SSMS) involves a few steps. Here's a guide on how to establish the connection:

### Prerequisites:
1. **Azure SQL Database:** Ensure that you have an Azure SQL Database provisioned and accessible in your Azure portal.
  
2. **SQL Server Management Studio (SSMS):** Have SSMS installed on your local machine. You can download it from the Microsoft website.

![SQLdatabase](https://github.com/prasadDPR/AzureSQLdatabase_connect_via_SSMS/assets/121819069/5b4b9baf-0ab6-4ffe-8af2-e9cf3f890a9f)

### Steps to Connect:

1. **Get Connection Details:**
   - Go to the Azure Portal.
   - Navigate to your Azure SQL Database resource.
   - Go to "Overview" or "Connection Strings" to get the server name, database name, and authentication details (username/password or Azure AD authentication).

2. **Open SQL Server Management Studio:**
   - Launch SQL Server Management Studio on your local machine.

3. **Connect to Azure SQL Database:**
   - Open SSMS.
   - In the "Connect to Server" dialog:
     - **Server type:** Choose "Database Engine."
     - **Server name:** Enter the server name of your Azure SQL Database (usually ends with ".database.windows.net").
     - **Authentication:** Select the appropriate authentication method (SQL Server Authentication or Azure Active Directory).
     - **Login:** Enter your username for SQL Server Authentication or select the Azure AD account if using Azure AD authentication.
     - **Password:** Enter your password if using SQL Server Authentication.
       
![SSMS Login](https://github.com/prasadDPR/AzureSQLdatabase_connect_via_SSMS/assets/121819069/bbeba002-2456-4bbf-9a92-81fde6ad52e9)

4. **Establish Connection:**
   - Click "Connect" to establish a connection between SSMS and your Azure SQL Database.
  
![SSMS](https://github.com/prasadDPR/AzureSQLdatabase_connect_via_SSMS/assets/121819069/fcda1b46-46aa-4112-ba28-3be4fa8b1abe)

### Troubleshooting Tips:

- Ensure that your machine's firewall allows outbound connections to Azure SQL Database.
- Double-check the server name, login credentials, and authentication method for accuracy.
- For Azure AD authentication, ensure that the Azure AD user has appropriate permissions on the Azure SQL Database.
- If encountering connection issues, check the Azure portal for any service health advisories or firewall settings that might restrict access.

Once connected, you can use SSMS to manage and interact with your Azure SQL Database, execute queries, create tables, and perform administrative tasks just as you would with an on-premises SQL Server instance.
