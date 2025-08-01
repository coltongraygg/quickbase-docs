## Connect to another Quickbase app

You can create a [connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-) to access data in another Quickbase app. Bring the data you want into your app and refresh it based on a schedule you set, or any time, on-demand.

Note

You can also access data in other Quickbase apps using a [cross-app relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-). However, creating a connected table lets you access all of the fields within a table, rather than specific lookup fields.

## Create a connected table

1.  Open _the app that you want to connect to_ and make note of the following:
    
    -   **Application ID**: Open the home page of the app. In the URL that displays, copy the alpha-numeric text that displays after _/app/_. For example, _bi4zjv7mq_.
        
    -   **App Token**: This extra layer of security may be required if you are authorizing a connection with user name and password. Authorizing with a [user token](https://helpv2.quickbase.com/hc/en-us/articles/4570374095124-About-User-Tokens-), instead of a user name and password is recommended.  
        To find the app token, from the sidebar select **App settings**, then **App properties**. In the Advanced settings section, find the **Require Application Token** checkbox, then click **Manage Application Token**. Copy the token value. Learn more about [app tokens](https://helpv2.quickbase.com/hc/en-us/articles/4570313549972-App-tokens).
        
    -   **Quickbase URL**: Locate the Quickbase URL in the browser. For example, _https://yourCompanyName.quickbase.com_.
        
2.  Choose an Authorization type. [User token](https://helpv2.quickbase.com/hc/en-us/articles/4570374095124-About-User-Tokens-) is recommended. Enter your user token or create a user token in My Preferences. If you choose to authorize using user name and password, enter your Quickbase **user name** and **password** for the app you are connecting to.
    
3.  Create your connected table. See [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-) or click the **Help** icon in the top right, while creating your table, and we'll guide you along.
    

Note: Through a connection, Quickbase fields are simplified as needed to fit these types: Text, Numeric, Date, Time, Checkbox, and Address. See [About connected fields](https://helpv2.quickbase.com/hc/en-us/articles/4570265917332-About-connected-fields-).

## View, test, or delete your connections

To view **details about your connection** and [test](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-), [change](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), or [delete](https://helpv2.quickbase.com/hc/en-us/articles/4570322374036-Deleting-a-connection-) connections, click the user dropdown on the global bar, then click **Profile**. Your connections display in the **My Connections** area.

## View connected table details and history

To view **Details about your connected table**, including the connected service, connection owner, connected fields, filter, and schedule for the connected table, access the connection in **Table Settings**. You can also view a **History** of recent refreshes, and [edit the connection filter](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table-Help-), [refresh schedule](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-), or [switch to use a different connection](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), if necessary.

### Related topics:

-   [About connections](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-)
    
-   [About data connection details](https://helpv2.quickbase.com/hc/en-us/articles/4570281951252-Viewing-connected-table-details-)
    
-   [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-)
    
-   [Refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)
    
-   [Testing a connection](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-)