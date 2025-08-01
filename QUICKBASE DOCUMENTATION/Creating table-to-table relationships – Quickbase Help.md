## Creating table-to-table relationships

> Access to this feature can change based on your Quickbase plan. Learn more about feature availability and plans in [Quickbase capabilities](https://helpv2.quickbase.com/hc/en-us/articles/21309804922004).

You can create a [relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-) between two tables within an app, or between two tables in separate apps. To create a relationship between tables in an app

You can create table-to-table relationships using table settings or [Visual Builder](https://helpv2.quickbase.com/hc/en-us/articles/4570376993300-Quickbase-Visual-Builder-).

### Using table settings to create relationships

1.  Open the app.
    
2.  Open one of the tables you want to relate.
    
3.  Select **Settings**, then select **Table-to-table relationships**.
    
4.  Select the **+ New Relationship** button. The **Create a table-to-table relationship** dialog appears:
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572802920852)
    
5.  The dialog steps you through all the elements of creating a relationship, and provides guidance for each step.
    
    -   **Tables**: Select the tables to connect, and choose which table is the **parent** and which table is the **child**.
        
    -   **How to relate child records to a parent**: This step involves choosing a **reference field** for the relationship. This step may not appear depending on how the **key field** in the parent table is set.
        
        **Key field**: The key field ensures that records have a unique identifier. Quickbase creates Record ID# as the key field, but you can specify a different key field in table settings.
        
        **Reference field**: When adding a child record, the reference field provides a list of parent records. For most relationships, using the default reference field is sufficient. You might select a different reference field if you have data that matches between parent and child, such as project number or customer ID, and want the relationship to automatically link existing records. If you use the default reference field, you can add a lookup field as a reference proxy, which acts as the reference field, but contains user-friendly information.
        
    -   **Add lookup fields:** Choose fields from the parent table to appear as [lookup](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-) fields in child records. When you create a new child record and choose a parent, lookup fields populate automatically with info from the parent record. If you don’t need lookup fields right now, choose Create Relationship to finish. You can add more fields later by editing this table-to-table relationship.
        
        **Lookup field as reference proxy**: Quickbase automatically sets your first [lookup](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-) field as a [reference proxy](https://helpv2.quickbase.com/hc/en-us/articles/4570306784404-Designating-reference-proxy-fields-), which acts as the reference field, but contains user-friendly information that lets you relate child records to a parent. You can change the reference proxy at any time using table settings.
        
6.  After you create the relationship, it appears on the **Table-to-table relationships** page. You can [edit the relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570416568468-Adding-fields-to-table-to-table-relationships-) from here if necessary, to view settings, change properties for the fields, or add fields.
    

### Using Visual Builder to create relationships

Visual Builder provides an easy way to see your tables in a data model. Relationships appear as lines between parent and child tables, for example:

![Relationship in Visual Builder](https://helpv2.quickbase.com/hc/article_attachments/4572824845076)

1.  To create a relationship in Visual Builder, open an app, click **Settings**, then click **Structure**. Visual Builder opens.
    
2.  On a table, use the relationship icon: ![](https://helpv2.quickbase.com/hc/article_attachments/4572817397396)
    
    Click and hold the icon to drag a line between tables you want to connect with a relationship. The **Create a table-to-table relationship dialog** appears. Or, to start a same-table or cross-app relationship, single-click the icon to start the relationship dialog.
    

Relationships between tables in your app are connected with a solid arrow. Cross-app relationships are shown by a dashed arrow from tables pointing to the top of the page.

**Summary fields and lookup fields limitation**. Visual Builder may add some lookup fields for you automatically during relationship creation, but you cannot currently use Visual Builder to add summary fields or lookup fields to a relationship. You can exit Visual Builder to edit the relationship, adding summary fields or adding or editing lookup fields.

## Creating a cross-app relationship

You can create a child-to-parent relationship between tables in two different apps.

Note: This feature is not available to accounts on the Quickbase Essential plan.

The process for creating a cross-app relationship is similar to creating a relationship within one app, however, there are some key differences to consider.

By choosing a table in another app, you are limited to creating a child-to-parent relationship. The app containing the relationship details is always the child table. The app containing the parent table does not list the relationship in settings.

With roles and permissions, it is important to ensure you are securing data correctly. The parent table must be set to allow access to the child table and include a role for the all users in the child table. If a user has access to both apps, the role in the parent table will take precedence over the user's role in the child table.

A cross-app relationship is useful in these cases:

-   Connecting simple, small to medium-sized apps.
    
-   Limited edits in the child table.
    
-   Immediate data availability in the child for viewing on forms and reports.
    

**Important**: Before proceeding with a cross-app relationship, read about all the [options for sharing data across apps](https://helpv2.quickbase.com/hc/en-us/articles/4570325773844) and select the case that best fits your app and data.

To create a cross-app relationship:

1.  In the section above, follow the steps to use either table settings or Visual Builder.
    
2.  In the **Create a table-to-table relationship** dialog, when choosing a table, pick **Select a table in another app** at the bottom of the drop-down.
    
3.  You may need to ensure the other app is set to allow access.
    
    -   If you are an administrator of the other app, you'll see a panel prompting you to choose the role for the cross-app relationship.
        
        Important:
        
        -   Select the appropriate role to limit access to records in the parent app.
            
        -   Your choices here depend upon what [roles](https://helpv2.quickbase.com/hc/en-us/articles/4570323434516-About-Roles-) you've set up for the parent app.
            
        -   The role you choose affects what information is available to the child app.
            
        -   Permissions to create records in the parent table must be granted to the individual users, not to a group.
            
        
        For example, a sales department has a Marketing Leads app, and would like to create a cross-app relationship with an Employee Information app to populate fields. You need to restrict access to certain employee information. Create a role in the Employee Information app that only allows access to fields needed for the Marketing Leads app, such as name and telephone extension. Then, grant the Marketing Leads app the ability to create a relationship with the HR app, specifying that it can only access the Employee Information app using the role you created.
        
    -   If you are not an administrator of the other app, you'll see the message **You need permission to create a relationship**. Select the **Request permission** button to send an email to the app owner. Once the app admin allows access for your app, you can resume with creating the relationship.
        
4.  Select the table to connect to, which will become the parent table.
    
    **Note:** Unlike with a regular table-to-table relationship inside one app, child-creation (URL formula) buttons and reports lists are not automatically added to the parent table. These fields can be added to the parent table manually, by editing the relationship (in the child table) and [adding fields](https://helpv2.quickbase.com/hc/en-us/articles/4570416568468-Adding-fields-to-table-to-table-relationships-).
    
5.  After you create the relationship, it appears on the **Table-to-table relationships** page for the child table only. You can [edit the relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570416568468-Adding-fields-to-table-to-table-relationships-) from here if necessary, to view settings, change properties for the fields, or add fields.

### Related topics:

-   [About table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-)
    
-   [Designating reference proxy fields](https://helpv2.quickbase.com/hc/en-us/articles/4570306784404-Designating-reference-proxy-fields-)
    
-   [Creating many-to-many relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570285625236-Creating-many-to-many-relationships-)
    
-   [Creating lookup fields](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-)