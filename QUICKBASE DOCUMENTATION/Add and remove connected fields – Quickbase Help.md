## Add and remove connected fields

If you are the connection owner and an app admin, you can add and delete connected fields from a connected table at any time. You add and delete connected fields just like Quickbase fields.

If you are an app admin, but not the connection owner, you can add and remove Quickbase fields (but not connected fields).

To add connected fields to a connected table:

1.  Open the connected table from the sidebar. Select **Settings** under the table name in the page bar, then click ![](https://helpv2.quickbase.com/hc/article_attachments/4572818917780) next to **Fields**.
    
2.  Select **Using connected data**. A list of fields in the data source that are not currently connected displays.
    
3.  Select the fields on the left that you want to connect and drag them to the right to add them to your connected table.
    
4.  Click **Done**. If you want to see the fields you added, click **Exit Settings** and then click ![](https://helpv2.quickbase.com/hc/article_attachments/4572811842196)**Refresh data** to refresh your connected table.
    

To remove connected fields from a connected table:

1.  Open the connected table from the sidebar. Select **Settings** under the table name in the page bar, then click **Fields**. Or hover over the three dot menu by the table name in the sidebar, and select **Fields**. 
    
2.  Select **Using connected data**. A list of fields in the data source that are not currently connected displays.
    
3.  Locate the field you want to delete, and optionally, check the usage of this field: Hover the mouse over the field name, then click **Where is this field used?** in the popup that appears. The Usage page displays a list of the places where your application references this field.
    
4.  Complete one of the following tasks:
    
    -   To delete more than one field, select the checkbox next to the name of each field that you want to delete, then click **![](https://helpv2.quickbase.com/hc/article_attachments/28601968701204) Delete** at the top of the table.
        
    -   To delete a single field, click the delete icon (![](https://helpv2.quickbase.com/hc/article_attachments/28601968701204)), to the right of the field that you want to delete.
        
5.  Click **Delete** to confirm that you want to disconnect and delete the connected field.
    

You can also [add Quickbase fields](https://helpv2.quickbase.com/hc/en-us/articles/4570374838292-Adding-new-fields-) to your connected table. These Quickbase fields are associated with the connected record.

Just like with any Quickbase table, you can create relationships among your connected table and other tables.

Note: You can add more connected fields to a connected table at any time, but you can’t add connected fields to existing Quickbase tables. Instead, create a new connected table that contains the data you want to access in Quickbase and then relate it to your existing Quickbase table.

### Related topics:

-   [About connections](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-)
    
-   [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-)
    
-   [FAQs about connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570374698388-FAQs-about-connected-tables-)