## Connecting to NetSuite

You can bring data from NetSuite into a [connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-) in your Quickbase app and keep it in sync automatically.

To connect to NetSuite:

1.  From the sidebar, click **New Table** and then select **Using connected data**.  
    ![tables_connected_data.png](https://helpv2.quickbase.com/hc/article_attachments/30864998350484)
    
2.  Name your table, click **Next** > **NetSuite**.
    
3.  Choose an **Authorization type**. Note that to use Token Based Authentication (TBA), TBA must be enabled in your NetSuite instance. Note that after you create a NetSuite connection, the authorization type cannot be changed.
    
4.  If you are using the **Username** and **Password** authorization type, enter your NetSuite **user name** and **password**.
    
5.  Enter your NetSuite organization, and role.
    
    -   **Organization**: Enter the NetSuite Internal Account ID. To find this, access NetSuite and click **Setup** > **Integration** > **SOAP Web Services Preferences**. Copy the **Account ID**..
        
    -   **Role**: Enter the numeric NetSuite Role ID. To find the role ID for a role, access NetSuite and click **Setup** > **Users/Roles** > **Manage Roles**. The role ID displays in the Internal ID column. Roles grant various permissions. If you are using the **Token Based Authentication** (TBA) authorization type, use a role with TBA permissions.
        
6.  Create your connected table. See [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-) or click the **Help** icon in the top right, while creating your table, and we'll guide you along.
    

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
    
-   [Refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)