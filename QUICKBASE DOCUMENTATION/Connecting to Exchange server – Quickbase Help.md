## Connecting to Exchange server

You can automatically connect to a folder on your Exchange server and bring email messages into a Quickbase [connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-). For example, you might want to create a connected table that brings in customer email, so your team can see all correspondence from a specific customer.

You can refresh your connected table automatically, based on a schedule that you set.

Note

A connection can only be made to an Exchange server where IMAP is enabled.

## To connect to Exchange server:

1.  From the sidebar, click **New Table** and then select **Using connected data**.  
    ![tables_connected_data.png](https://helpv2.quickbase.com/hc/article_attachments/30864993617172) 
    
2.  Name your table, click **Next**, and then select **Exchange**.
    
3.  Enter the **Server** name. This is often _outlook.office365.com_. The Exchange server must be running on port 993.
    
4.  Choose an Authorization type.  
    OAuth 2.0 is recommended and is the required authorization type for Office 365 users. If you choose this type, enter the same username you will use to sign in to Exchange when the connection is created. Username and Password authorization can be used for internal Exchange servers. Enter your user username and password for the Exchange server. A username can be either an email address or a domain-qualified account name (domain\\account), depending on the configuration of the Exchange server.
    
    Note
    
    After an Exchange connection has been created, the authorization type cannot be changed.
    
5.  Create your connected table. See [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-) or click the **Help** icon in the top right, while creating your table, and we'll guide you along.
    

## View, test, or delete your connections

To view **details about your connection** and [test](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-), [change](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), or [delete](https://helpv2.quickbase.com/hc/en-us/articles/4570322374036-Deleting-a-connection-) connections, click the user dropdown on the Global bar, then click **My preferences**. Your connections display in the **My Connections** area.

## View connected table details and history

To view **Details about your connected table**, including the connected service, connection owner, connected fields, filter, and schedule for the connected table, access the connection in **Table Settings**. You can also view a **History** of recent refreshes, and [edit the connection filter](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table-Help-), [refresh schedule](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-), or [switch to use a different connection](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), if necessary.

### Related topics:

-   [About connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-)
    
-   [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-)
    
-   [Deleting a connection](https://helpv2.quickbase.com/hc/en-us/articles/4570322374036-Deleting-a-connection-)
    
-   [FAQs about connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570374698388-FAQs-about-connected-tables-)
    
-   [Testing a connection](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-)
    
-   [Refreshing a connected table  
    ](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)