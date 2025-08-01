## Deleting a connection

You can’t delete a connection that is in use, which means that you can’t delete a connection if it’s been used as the connection for a connected table that still exists. In order to delete a connection, you must first delete all the connected tables that use that connection.

In the steps below, when you visit the My Preferences page, the My Connections section Usage column indicates how many connected tables, if any, use the connection. If 0 tables use it, when you click on the connection and open it, it will say “This connection is not in use” in the Usage section and the Delete Connection button will be enabled.

**Important**: Deleting a connection for Gmail, Google Drive, or QuickBooks will invalidate other QuickBase Sync connections that were created with the same Gmail, Google Drive, or QuickBooks log in credentials. This happens because when a connection is deleted, we send a request to the connected service to revoke the OAuth token that was used by that connection. When Google or QuickBooks receives the request, they invalidate all the OAuth tokens for Quickbase Sync for that user. The connections in Quickbase will fail until the connection owner reauthorizes the connection to get a new valid OAuth token.

To delete a connection:

1.  Click the user dropdown on the Global bar, then click **My preferences**.
    
2.  The **My Connections** section lists all your connections with a Usage column. Only those with Usage set to zero can be deleted. In order to delete a connection, you must first delete all the connected tables that use that connection.
    
3.  Select the connection you want to delete. If the connection isn’t being used, the Usage section displays **This connection is not in use** and the **Delete Connection** button is enabled.
    

### Related topics:

-   [About connections](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-)
    
-   [About connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-)
    
-   [Filtering connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table-Help-)
    
-   [Refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)