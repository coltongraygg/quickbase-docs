You can connect to folders containing CSV files stored in Dropbox, Box, Google Drive, or an SFTP server and sync data into a [connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-) in your Quickbase app.

Any data that you can save in CSV format, from any system, on premise or in the cloud, can automatically refresh in Quickbase, based on a schedule that you set.

As with all connected tables, the data that you bring in is read-only and can’t be edited in Quickbase. This helps keep your data in sync and eliminates potential confusion about which system contains the most up-to-date information.

You can update _records_ in your connected table by [refreshing the table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-) to display data from the most recent CSV file(s) in your connected folder. We only look at CSV files in your connected folder.

You decide how refresh the data in your connected table. You can choose:

-   **Keep everything in my table and add new records** to keep all the data in your connected table, even if it is not in the most-recent CSV file. Existing records will updated and new records added. You can also use this option when your source folder contains [multiple files](https://helpv2.quickbase.com/hc/en-us/articles/4570365490964-Connecting-to-a-folder-containing-CSV-files#multiple_files).
    
    Tip: This is a good choice if your table serves as an archive of all records.
    
-   **Make my table match the latest CSV file** to overwrite your table so it matches the latest CSV file exactly. Each time you refresh your connected table, we'll use the most recent CSV file in the folder, regardless of the file name.

## Before you connect to a folder containing CSV files

Make sure your CSV file:

-   Ends with .csv
-   Has a header row - and no heading is the same  
    We'll use the information in the first row of your .csv file as the column names in your connected table. If the first row is not a header, data in the first row will become the column names in your connected table.
-   Has no blank columns
-   Has a field that makes each record unique. You'll need to set this field as the [Refresh Key](https://helpv2.quickbase.com/hc/en-us/articles/4570260038804-About-the-Refresh-Key-field-).
-   Is a UTF-encoded .csv file

## Connecting to a folder containing CSV data

The first time you connect to Box, Dropbox, Google Drive, or an SFTP server, we'll guide you through connecting, creating a folder, and adding your CSV file:

1.  Open your Quickbase app, click **New Table** in the sidebar, and select **Using connected data**. ![tables_connected_data.png](https://helpv2.quickbase.com/hc/article_attachments/27113833469076)
    
2.  Name your table, click **Next**, and select your file storage location: **Box**, **Dropbox**, **Google Drive** or **SFTP**.
    
3.  Give your connection a name and then **Sign in**.
    
4.  The first time you create a connection, we'll create a **QuickBase Sync folder** in your account. Then, we'll ask you to:
    

1.  **Go to the service**, for example, Dropbox.
    
2.  Create a **new folder within the QuickBase Sync folder**.
    
3.  Put a **CSV file inside the folder** you created. Each time you refresh, we'll use the most recent .csv file in the folder, regardless of the file name.
    

6.  Return to Quickbase and click **Yes, I did** to continue. The folder you added inside the QuickBase Sync folder displays.
    
7.  Select the folder and then choose the fields you want to connect. These fields become text fields in the connected table. Later, you can [change field types](https://helpv2.quickbase.com/hc/en-us/articles/4570362798868-Changing-the-field-type-of-existing-fields-). The first row of the CSV file becomes the column names in your connected table.
    
8.  Optionally, [define a filter](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table-Help-) to limit the records that you connect.
    
9.  Select [refresh options](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-) to define when and how to refresh the connected table. We'll always use the **most recent CSV file in your connected folder** when refreshing your table.
    

1.  [Refresh Key](https://helpv2.quickbase.com/hc/en-us/articles/4570260038804-About-the-Refresh-Key-field-) - Select a field that makes each record unique. It must be a connected field with unique values (no blanks).
    
2.  Table updates - Choose **Keep everything in my table and add new records** to keep all the data in your connected table, even if it is not in the most-recent CSV file. Existing records will be updated and new records added.
    
    Tip: This is a good choice if your table serves as an archive of all records.
    
    For new CSV-connected tables, you can also use this option when your source folder contains [multiple files](https://helpv2.quickbase.com/hc/en-us/articles/4570365490964-Connecting-to-a-folder-containing-CSV-files#multiple_files).
    
    Choose **Make my table match the latest CSV file** to overwrite your table so it matches the latest CSV file exactly.
    
3.  Schedule - optionally, set a schedule to automatically refresh using the most recent CSV file in your connected folder. You can refresh your table any time by clicking **Refresh Data**![](https://helpv2.quickbase.com/hc/article_attachments/27112915430548).
    

Later, you can update the CSV file or put a new CSV file in your connected folder, and then refresh your table to keep in sync with your latest changes.

If connected records don't display in your new table, click the yellow warning icon beside Refresh Data ![](https://helpv2.quickbase.com/hc/article_attachments/4572839037972) for details and then check out [Troubleshooting connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570327338132-Troubleshooting-connected-table-refresh-errors-#Troubleshooting_CSV) for tips.

## Connect to a folder with multiple files

For CSV-connected tables, you can sync data from files dropped into your CSV folder from multiple sources, like invoice data from different vendors. Or, suppose your order management system outputs multiple CSV files every hour. You can ensure each of the files will be synced to your connected table.

Here's how it works:

-   If you choose **Make my table match the latest CSV file**, Quickbase only connects to the file that was uploaded last (according to the file's time stamp). Any other files in the folder are ignored.
    
-   If you choose **Keep everything in my table and add new records**, Quickbase connects to the files one at a time, starting with the oldest file and proceeding to the latest (according to the time stamp of the file).
    
    Quickbase will process a maximum of 10 files in a single refresh. After each file is read, Quickbase moves it to the _Done_ folder. (Files in the Done folder have a timestamp appended to the filename). New records are added to your connected Quickbase table, and records with matching refresh keys are updated. No existing records are removed from the Quickbase table even if they are not in the connected files.
    

Warning:  As a best practice, do not create more than one "keep everything" connected table that points to the same CSV folder, since files that are processed and moved to the **Done** folder when you refresh one connected table won’t be available for refreshing another connected table.

## Connecting more folders

After you've created a connected folder in your Box, Dropbox, Google Drive, or SFTP server, you can add another connected folder by going to the service, creating a new folder inside the QuickBase Sync folder, and putting a CSV file inside it. When you create a new connected table, your new folder will display in the list of folders you can connect.

## View connected table details and history

To view **Details about your connected table**, including the connected service, connection owner, connected fields, filter, and schedule for the connected table, access the connection in **Table Settings**. You can also view a **History** of recent refreshes, and [edit the connection filter](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table-Help-), [refresh schedule](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-), or [switch to use a different connection](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), if necessary.

## View, test, or delete your connections

To view **details about your connection** and [test](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-), [change](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), or [delete](https://helpv2.quickbase.com/hc/en-us/articles/4570322374036-Deleting-a-connection-) connections, click the user dropdown on the Global bar, then click **My preferences**. Your connections display in the **My Connections** area.

### Related topics:

-   [About connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-)
    
-   [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-)
    
-   [Checklist for connecting to an SFTP server](https://helpv2.quickbase.com/hc/en-us/articles/4570237628052-Checklist-for-connecting-to-an-SFTP-server-)
    
-   [FAQs about connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570374698388-FAQs-about-connected-tables-)
    
-   [Testing a connection](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-)
    
-   [Refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)