## How to use a different connection

This table uses a [connection](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-) to access external data. The connection may belong to you or another app admin. If you're an app admin, you can switch to use another one of your connections or create and use a new connection, if necessary. You can switch a table _from_ using someone else's connection, but you can't switch _to_ using someone else's connection.

## Why use a different connection?

Switching connections is usually necessary _only when the connection owner is no longer available_.

Only the connection owner can add and remove connected fields from the table and change the connection filters.  
If you need to make changes like these, and the connection owner is not available to make the changes, you'll need to switch to use one of your connections.

For example, if the connection owner has left the company, switch to one of your connections. You may also want to switch connections if another connection, with different access privileges, provides the data you need in this connected table.

Don't immediately switch connections if your current connection isn't working. In most cases, you can easily fix your connection. Start by [testing](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-) and re-authorizing the connection.

Remember that you can switch the table _from_ the current connection (yours or someone else's) _to_ one of _your connections_. You can't switch a table to use someone else's connection. Only the connection owner can do that. For example, if you switch a table from using Pam's connection to your connection, then you can't switch the table back to using Pam's connection. (Only Pam could do that.)

## Do I need to do anything before switching?

Connections provide access to data in a service. Make sure the connection you're planning to switch to has access to the data that is currently connected in Quickbase.

1.  In Quickbase, check which fields are connected to the service. To do this, open the connected table, click **Settings** and select the connection. In the Connected fields area on the Connection settings Details tab, click **View fields**.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572799393684/view_connected_fields.png)
    
    The Fields page displays. If the Info column is not visible on the Fields page, click **Advanced Options** and select to display the **Info** column.
    
    The Info column contains the name of the field in the service that the Quickbase field is connected to. Note which fields in the service are connected, so you can make sure that connection you're planing to switch to also has access to these fields.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572779346068/advanced_options.png)
    
2.  Log in to the service using the credentials associated with the connection you want to switch to.
    
3.  In the service, make sure you have access to the fields that are currently connected in Quickbase. If you don't, there are a few ways you can resolve this. See [Troubleshooting table refresh errors](https://helpv2.quickbase.com/hc/en-us/articles/4570327338132-Troubleshooting-connected-table-refresh-errors-).
    
4.  If you are switching to an existing connection, [test the connection](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-). To do this, click **My preferences**. In the **My Connections** area, select the connection you want to test, and click **Test Connection**.

## How do I switch to a different connection?

1.  Open the connected table and click **Settings**.
    
2.  Select the connection.
    
3.  Click **Use different connection**.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572779371668/switch_connection_link.png)
    
4.  The connection currently in use is highlighted. Select the connection you want to use and then click **Use this connection**.
    
5.  Click **Yes** if you want to switch to the selected connection. To refresh data in the table using the new connection, click **Yes**.
    

Tip: You can also create and switch to a new connection. After you click **Use different connection**, select **Create a new connection**. Create the new connection, and click **Yes** when prompted to switch connections.

Learn more [about connections](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-).