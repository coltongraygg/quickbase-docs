 In this article

-   [Creating and managing connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570374698388-FAQs-about-connected-tables#h_01HQKRAWMAX8CW3GYBY14PV636)
-   [Refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570374698388-FAQs-about-connected-tables#h_01HQKS9QKV47V489JTY1SGPR57)
-   [Keeping your data secure](https://helpv2.quickbase.com/hc/en-us/articles/4570374698388-FAQs-about-connected-tables#h_01HQKR5XAVB2ZSV50B3Z9QT8QV)

## Creating and managing connected tables

### Do I need special permissions to create a connected table?

No. If you can create a Quickbase table within an app, then you can create a connected table in that app. See [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-).

### Can other users see my connected table?

Yes, a connected table is just like an ordinary Quickbase table. You can allow and prevent users from viewing connected data using Quickbase roles and permissions.

### Can other users manage the connection?

You must be the connection owner to manage the connection, including:

-   Adding new connected fields to the table
-   Updating the connected table’s filter
-   Changing the refresh key of a the connected table

To allow a group of users to manage the connection, set up the connected table using a service account. This approach ensures continuity if the connection owner leaves the company, or if you need to shift responsibilities.

Learn more about [using a service account to manage connected tables](https://helpv2.quickbase.com/hc/en-us/articles/35223919570836).

### Can I set notifications and subscriptions on a connected table?

Yes, connected tables behave just like Quickbase tables. So, you could set up notifications to automatically let you know when a new closed and won opportunity is added to your Salesforce.com connected table.

### How can I use a connected table?

You can use a connected table to bring data from an external service or application into Quickbase. You can [create relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-) among the connected table and your other Quickbase tables and applications. You can create lookups, summary fields, perform calculations, run reports, and use the data however you choose. You use connected data in your workflows and build reports and [home pages](https://helpv2.quickbase.com/hc/en-us/articles/4570366229396-Create-an-App-Home-Page-) across all your data. Check out [What can I do with connected data?](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-) for some ideas.

### Can I change the fields in my connected table?

If you are the connection owner and an app admin, you can add and delete connected fields from a connected table at any time. You can also modify the filters and the automatic refresh schedule. If you are an app admin, but not the connection owner, you can add and remove Quickbase fields (but not connected fields) and change the automatic refresh schedule.

Note

Like all Quickbase tables, connected tables automatically include the five built-in Quickbase fields: Date Created, Date Modified, Record ID#, Record Owner, and Last Modified By.

### Can I change an existing table into a connected table?

No, you cannot change an existing regular table into a connected table. You must specify a table as a connected table at the time it is created.

### When should I create a connected table that uses another Quickbase app as its source?

If you want to include a number of fields from another Quickbase app in your app and keep the data in sync, you may want to create a connected table. Using connected tables to access data in other Quickbase apps, instead of cross-application relationships, enables you to access all of the data that you want, rather than just specific lookup fields. You can update the data in the connected table automatically, according to the refresh schedule that you set. See [Connecting to other Quickbase apps](https://helpv2.quickbase.com/hc/en-us/articles/4570395540628-Connecting-to-another-Quickbase-app-).

Learn more about when to use connected tables instead of cross-app relationships in [Sharing data: Which method should you use](https://helpv2.quickbase.com/hc/en-us/articles/19713658161428-Sharing-data-Which-method-should-you-use).

Note

Through a connection, Quickbase fields are simplified as needed to fit these types: Text, Number, Date, Time, and Checkbox.

### What if I want to connect to a lot of data?

You can set a filter to limit the data that you connect from an external service, such as QuickBooks Online or Salesforce.com. Setting a filter helps restrict records to the ones you really care about; for example, invoices from this year, rather than all invoices.

If you are bringing a large amount of data into a connected table, it may take some time for your connected data to display the first time. Since table refreshes bring in only new or changed data, subsequent table refreshes will be much faster than the table creation.

Quickbase can sync to a maximum of one billion cells (where a cell = number of records x number of fields). If you exceed this limit during an attempted refresh, the refresh will not happen and you'll get an error message. You can set a filter to limit the data to be synced.

Here are some guidelines if you expect the connected table you are creating will contain 25MB or more of data:

1.  When creating your connected table, filter the table to bring in just one record.
    
2.  Confirm that the connected table brings in the data you expect.
    
3.  In table **Settings**, edit the connected table to change the filter to bring in the entire record set you want.
    
4.  In table **Settings**, schedule the first refresh of the table to occur overnight. After the table is populated for the first time, you can change or remove the scheduled refresh.
    

### Can I copy a connected table?

No, you can’t copy a connected table. However, if you want to make the data in your connected table editable, you can make a copy of your app with data. Doing this creates an editable copy of the table in the copied app.

This copy of the connected table is not connected to the data source and can’t be re-connected.

To make a copy of your app with data:

1.  In App Settings, select **App management**.
    
2.  In the Manage the app area, select **Copy app**.
    
3.  In the Copy Options area, select **Copy this application with data** and then click the **Copy Application** button.
    

### I already have a Quickbase table; can I add connected fields to it?

You can only add connected fields to connected tables.

If you want to bring connected fields into an existing Quickbase table, you can create a new connected table, choose the fields that you want to connect, and then create relationships between that connected table and your existing Quickbase table.

## Refreshing a connected table

### What happens when I refresh my connected table?

When you refresh your connected table, the data in the connected table is compared with the data in the external service. If there are changes or additions to connected data in the external service, your connected table is updated with those changes, based on the refresh options you set.

Since the data in connected fields comes from an external service, you can’t edit the data in connected fields or add a new record to a connected table. This helps to keep your data in sync across multiple services and eliminate potential confusion about which system contains the most up-to-date information.

To add or update a record with the most current data available in the connected data source, refresh your connected table

### How can I stop my connected table from refreshing?

If the connected table is scheduled to refresh according to a schedule, you can edit the schedule to turn off automatic refresh. To do this:

1.  Access table **Settings**
2.  Select the connection
3.  Click the **edit** link next to **Refresh**.
4.  In the Schedule area, select **Manual only** to turn off the scheduled refresh.
5.  You can then refresh the connected table whenever you’re ready by clicking ![](https://helpv2.quickbase.com/hc/article_attachments/24074595679252)**Refresh data** on your connected table.

### Do data refreshes in connected tables count against my Quickbase API requests?

Usage of connected tables does not count as Quickbase API requests.

### What happens to my data if there’s an error?

If an error occurs during data refresh, the refresh fails. If a refresh fails, you’ll notice an error icon at the top of your connected table. Hover over the icon to view a brief description of the problem. To access sync history, details, and troubleshooting information, click the error icon.

It is highly unusual for an error to occur when updating data in Quickbase. (If you were to encounter an error, it may occur earlier in the process, such as when logging into the external service.) Click **Refresh data** at any time to update your connected table.

## Keeping your data secure

### Can somebody else use my connections to create their own tables?

No. Your connection belongs to you and includes references and user permissions from the external service.

Tip

Hover over Refresh data ![](https://helpv2.quickbase.com/hc/article_attachments/24074595679252) to see the last date and time that the table was refreshed successfully.

### Is my data secure?

Yes. Using connected tables to access an external cloud application or another Quickbase app requires credentials for the source application. The data exposed by the source application is governed by the permissions granted to those credentials. Connected tables do not allow access to apps or tables to which a specific user does not already have access.

### Are my credentials safe?

Many data sources, such as Salesforce.com and QuickBooks Online, use Open Authentication (OAuth), an industry standard that securely grants access to data, while protecting personal information, such as your username and password.

Whenever OAuth is available, connected tables use OAuth to securely access your data. For those services that require connected tables to handle user names and passwords, Quickbase adheres to best practices for encryption and storage.

### Related topics:

-   [About connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-)
    
-   [About connections](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-)
    
-   [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-)
    
-   [Refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)