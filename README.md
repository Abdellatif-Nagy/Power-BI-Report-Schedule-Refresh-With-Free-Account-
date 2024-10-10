# Power-BI-Report-Schedule-Refresh-With-Free-Account-

This guide outlines the steps to automate the connection between an Excel file at your computer and Power BI using Google Drive for PC and Power BI's web connector. By the end of this process, you'll be able to schedule a refresh in Power BI to automatically pull updated data from Google Sheets.

__Steps:__

**1. Download Google Drive for PC:**

Download and install Google Drive for PC.
Follow the installation process and login with your Google account.

__2. Create Your Excel File and Sync with Google Drive__

Create or move your Excel file into a folder on your computer.
Right-click on the folder and enable syncing with Google Drive. This will ensure that any changes made to the file are reflected in Google Drive.

__3. Copy the Link of the Excel File__

Open the synced file in Google Drive (accessible via your browser).
Copy the link to the Excel file by clicking the "Share" button and setting the permissions as needed (make sure the file is accessible via a link).

__4. Identify the File ID__

In the URL of the Excel file, locate the File ID. The File ID is the part of the URL between /d/ and /edit.
Example:
https://docs.google.com/spreadsheets/d/FILE_ID_HERE/edit

__5. Build the Connection URL__

Use the following URL format to connect Power BI to your Excel file:
https://docs.google.com/spreadsheets/d/<Sheet_ID>/gviz/tq?tqx=out:csv

Replace <Sheet_ID> with the actual File ID from Step 4.

__6. Connect to Excel in Power BI__

Open Power BI and go to Get Data.
Choose Web as the data source.
Enter the URL from Step 5 into the Web connector and load the data.

__7. Publish the Power BI Report__

After finishing the report creation in Power BI, click Publish.
Choose your workspace to publish the report.

__8. Edit Credentials for the Data Source__

Go to My Workspace in Power BI Service (Power BI in your browser).
Under Datasets, locate the published report and click the Settings gear icon.
In Data Source Credentials, click Edit Credentials.

__9. Sign in to Your Google Account__

Sign in with the Google account that has access to the Excel file.

__10. Schedule a Refresh for the Dataset__

Once the credentials are verified, navigate to the Scheduled Refresh tab in the dataset settings.
Enable scheduled refresh, and configure the frequency as needed (e.g., daily or weekly).
Power BI will now automatically refresh the dataset by pulling the latest data from your Google Sheets file, ensuring that your reports stay up to date.
