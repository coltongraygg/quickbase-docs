## Refresh a connected table

This article explains how to refresh a connected table manually and how to change the frequency of automatic refreshes.

In this article

-   [Refresh a connected table manually](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refresh-a-connected-table#h_01JQ763FKN5H7GZMAATVRADX1Y)
    -   [Permissions](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refresh-a-connected-table#h_01JJMC82X5YJ14YCSAJJ5ZM9P3)
-   [Refresh a connected table automatically](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refresh-a-connected-table#h_01JJMC8EC4PXSAZJ9VC1WF8VV1)

## Refresh a connected table manually

You may need to manually refresh a connected table when setting up a new connected table, testing a connection, and when a refresh is required between automated refreshes. If your table requires frequent refreshes, you should configure the connected table to [refresh automatically](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refresh-a-connected-table#h_01JJMC8EC4PXSAZJ9VC1WF8VV1) instead.

To manually refresh the data, open a connected table and select **Refresh Data** ![](https://helpv2.quickbase.com/hc/article_attachments/4572809642644) on the page bar.

![refresh-data.png](https://helpv2.quickbase.com/hc/article_attachments/34291576431892)

### Permissions

The Refresh Data button only appears for roles that have the correct table permissions, otherwise only the date of the last successful refresh is shown. To grant these permissions, app admins can navigate to **App Settings** > **Roles** and check these Table Access permissions for the user's role: 

-   View All Records
-   Modify All Records
-   Add
-   Delete
-   Refresh Connected Data

Note: Roles with the App Access permission _Edit app structure and permissions_ automatically have the _Refresh Connected Data_ permission enabled for all connected tables in the app.

![](https://helpv2.quickbase.com/hc/article_attachments/37616683890068)

## Refresh a connected table automatically

You can also refresh a connected table automatically, on a **monthly**, **weekly**, **daily**, or **hourly** basis. The scheduled time is based on the app's timezone settings, which are set in app properties.

When you [create a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-), you choose when and how to refresh data in the table on the Refresh options page. App admins and the connection owner can change the [refresh options](https://helpv2.quickbase.com/hc/en-us/articles/4570314286100-About-refresh-options-) any time.

To set or change refresh options:

1.  Open your connected table and select **Settings**.
    
2.  Click the **Connection**, for example, _QuickBooks connection_.
    
3.  On the **Details** tab, locate **Refresh options** and then click **Edit options**.
    
4.  Set or adjust the refresh options and then click **Done**. To stop a connected table from refreshing according to a schedule, select **Manual only**.
    

Tip

Before you change the [refresh options](https://helpv2.quickbase.com/hc/en-us/articles/4570314286100-About-refresh-options-), make sure you understand the purpose of the connected table.

### Related topics:

-   [About connections](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-)
    
-   [About connected fields](https://helpv2.quickbase.com/hc/en-us/articles/4570265917332-About-connected-fields-)
    
-   [About refresh options](https://helpv2.quickbase.com/hc/en-us/articles/4570314286100-About-refresh-options-)
    
-   [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-)
    
-   [FAQs about connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570374698388-FAQs-about-connected-tables-)