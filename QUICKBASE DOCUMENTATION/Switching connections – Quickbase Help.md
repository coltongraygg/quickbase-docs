## Switching connections

Connections provide access to data in a [cloud app, service](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-), or [folder containing CSV files](https://helpv2.quickbase.com/hc/en-us/articles/4570365490964-Connecting-to-a-folder-containing-CSV-files-). They enable you to bring data into a [connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-) in your Quickbase app and keep the data in sync.

_App admins can change a connected table to use one of their own connections._

## Why switch to a different connection?

You might want a connected table to use a different connection if the connection owner changes roles, leaves the company, or is not available to [change the connection filter](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table-Help-) or [add](https://helpv2.quickbase.com/hc/en-us/articles/4570325865236-Adding-more-connected-fields-) or [remove](https://helpv2.quickbase.com/hc/en-us/articles/4570367639316-Deleting-a-field-) connected fields from the table. You may also want to switch connections if another connection, with different access privileges, provides the data you need in the connected table.

Don't immediately switch connections if your current connection isn't working. In most cases, you can easily fix your connection. Start by [testing](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-) and re-authorizing the connection.

Remember that you can switch the table from the current connection (yours or someone else's) to one of _your connections_. You can't switch a table to use someone else's connection. Only the connection owner can do that. For example, if you switch a table from using Pat's connection to your connection, then you can't switch the table back to using Pat's connection. Only Pat can switch to their connection, since she owns it.

## Do I need to do anything before switching?

Connections provide access to data in a service. Make sure the connection you're planning to switch to has access to the data that is currently connected in Quickbase.

1.  In Quickbase, check which fields are connected to the service. To do this, open the connected table, click **Settings** and select the connection. In the Connected fields area on the Connection settings Details tab, click **View fields**.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572799393684/view_connected_fields.png)
    
    The Fields page displays. If the Info column is not visible on the Fields page, click **Advanced Options** and select to display the **Info** column.
    
    This column contains the name of the field in the service that the Quickbase field is connected to. Note which fields in the service are connected, so you can make sure that connection you're planing to switch to also has access to them.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572779346068/advanced_options.png)
    
2.  Log in to the service using the credentials associated with the connection you want to switch to.
    
3.  In the service, make sure you have access to the fields that are currently connected in Quickbase. If you don't, there are a few ways you can resolve this. See [Troubleshooting table refresh errors](https://helpv2.quickbase.com/hc/en-us/articles/4570327338132-Troubleshooting-connected-table-refresh-errors-).
    
4.  If you are switching to an existing connection, [test the connection](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-). To do this, click **My preferences** in the global bar. In the **My Connections** area, select the connection you want to test, and click **Test Connection**.

### How do I use a different connection?

1.  Open the connected table and click **Settings**.
    
2.  Select the connection.
    
3.  Click **Use different connection**.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572779371668/switch_connection_link.png)
    
4.  The connection currently in use is highlighted. Select the connection you want to use and then click **Use this connection**.
    
5.  Click **Yes** if you want to switch to the selected connection. To refresh data in the table using the new connection, click **Yes**.
    

Tip: You can also create and switch to a new connection. After you click **Use different connection**, select **Create a new connection**. Create the new connection, and click **Yes** when prompted to switch connections.

### Related topics:

-   [About connections](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-)
    
-   [About connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-)
    
-   [Deleting a connection](https://helpv2.quickbase.com/hc/en-us/articles/4570322374036-Deleting-a-connection-)
    
-   [FAQs about connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570374698388-FAQs-about-connected-tables-)
    
-   [Testing a connection](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-)
    
-   [Refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)