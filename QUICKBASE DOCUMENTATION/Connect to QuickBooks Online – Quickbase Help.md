## Connect to QuickBooks Online

Connect to QuickBooks Online to bring data from QuickBooks into a [connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-) in your Quickbase app and keep it in sync automatically.

Note: QuickBooks Online requires that you are a QuickBooks Online Administrator to connect. QuickBooks Online allows only **one** active [connection](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-) to a company, regardless of the connection owner. You may need to coordinate among app admins when creating QuickBooks connections.

**Important**: Deleting a connection for Gmail, Google Drive, or QuickBooks will invalidate other QuickBase Sync connections that were created with the same Gmail, Google Drive, or QuickBooks log in credentials. This happens because when a connection is deleted, we send a request to the connected service to revoke the OAuth token that was used by that connection. When Google or QuickBooks receives the request, they invalidate all the OAuth tokens for Quickbase Sync for that user. The connections in Quickbase will fail until the connection owner reauthorizes the connection to get a new valid OAuth token.

To connect to QuickBooks Online:

1.  From the sidebar, select **New Table** and then select **Using connected data**.  
    ![tables_connected_data.png](https://helpv2.quickbase.com/hc/article_attachments/30864993709844)
    
2.  Name your table, select **Next**, and then select **QuickBooks**.
    
3.  **Sign in to QuickBooks Online** to authorize QuickBooks to connect to Quickbase.  
    QuickBooks uses Open Authentication (OAuth), an industry standard that securely grants access to data, while protecting personal information, such as your user name and password.
    
4.  Create your connected table. See [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-) or click the **Help** icon in the top right, while creating your table, and we'll guide you along.
    

## View, test, or delete your connections

To view **details about your connection** and [test](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-), [change](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), or [delete](https://helpv2.quickbase.com/hc/en-us/articles/4570322374036-Deleting-a-connection-) connections, click the user dropdown on the global bar, then click **Profile**. Your connections display in the **My Connections** area.

## View connected table details and history

To view **Details about your connected table**, including the connected service, connection owner, connected fields, filter, and schedule for the connected table, access the connection in **Table Settings**. You can also view a **History** of recent refreshes, and [edit the connection filter](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table-Help-), [refresh schedule](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-), or [switch to use a different connection](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), if necessary.

### Related topics:

-   [About connections](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-)
    
-   [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-)
    
-   [Deleting a connection](https://helpv2.quickbase.com/hc/en-us/articles/4570322374036-Deleting-a-connection-)
    
-   [FAQs about connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570374698388-FAQs-about-connected-tables-)
    
-   [Testing a connection](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-)
    
-   [Refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)