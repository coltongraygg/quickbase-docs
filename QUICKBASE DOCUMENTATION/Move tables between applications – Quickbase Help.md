## Move tables between applications

If you're managing many Quickbase applications, you may eventually want to consolidate or reorganize tables between apps. You can also take an existing table from any app and move it into another app.

When you move a table into an app, it no longer belongs to the original app. This means that the table doesn't appear on the source app's sidebar, and any relationships with other tables in that app are broken. The moved table becomes a table in the destination app.

Note: To move a table, you must be the manager of the table you want to move and also the manager of the app that you move the table to.

When you move a table into another app, some attributes of the original app do not carry over to the new application. These attributes are:

-   Roles and their properties
    
-   Users who have access to the table
    
-   Custom pages that feature the table
    
-   Application variables ([what are these?](https://helpv2.quickbase.com/hc/en-us/articles/4570400496020-About-Application-Variables-))
    

Be sure to make a note of any attributes that you want to keep before you move the table. If you move the table to its own application, these attributes reappear in the new application.

Before you begin, note that:

-   The user transferring the table needs app creation rights and must be the app manager of both source and destination apps
    
-   The source and destination apps must be in the same realm
    
-   If all tables are transferred (that is, the app has no table), the app will be deleted
    

Note: You can also [move a table to create a _new_ app](https://helpv2.quickbase.com/hc/en-us/articles/4570403369492-Remove-a-Table-from-an-Application-), or [delete the table](https://helpv2.quickbase.com/hc/en-us/articles/4570320587924-Deleting-tables-) at any time.

To move a table into another application:

1.  Open the app to which you want to move a table.
    
2.  From the app home page, click **Settings**, then click **App management**.
    
3.  Click **Move a table into this app**.
    
4.  Click **Select a Table**. A list of your applications appears.
    
5.  Select the application that contains the table you want to move, then click **OK**.
    
6.  Select the table you want to move and click **OK**. (Quickbase skips this step if the app you chose only has one table.)
    
7.  Choose the access permissions on this table to give other roles.
    
    While you're in the process of moving a table, it's usually best to grant "no access" until you have everything set up exactly as you wish. Later, you can assign permissions properly via the [Customize Roles](https://helpv2.quickbase.com/hc/en-us/articles/4570355458836-Configure-Permissions-for-a-Role-) page. As administrator, you'll have full access to this table, even with "no access" turned on.
    
    Note: This functionality is not available to accounts on the Quickbase Essential plan.
    
8.  Click **OK**.
    

Tip: When adding tables to an application, consider making the term for "record" unique for each table you add so that users aren't confused when they try to add a record. To learn more, see [Changing names for records](https://helpv2.quickbase.com/hc/en-us/articles/4570424416916-Changing-names-for-records-).

### Related topics:

-   [Copying a table](https://helpv2.quickbase.com/hc/en-us/articles/4570245208852-Copy-a-Table-)
    
-   [Add a new table to an app](https://helpv2.quickbase.com/hc/en-us/articles/4570404266004-Adding-new-tables-)
    
-   [Moving a table into a new app](https://helpv2.quickbase.com/hc/en-us/articles/4570403369492-Remove-a-Table-from-an-Application-)