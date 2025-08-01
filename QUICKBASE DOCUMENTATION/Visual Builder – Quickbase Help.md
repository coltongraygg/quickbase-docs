## Visual Builder

Visual Builder provides an easy way to create and update apps. You can create tables, add fields, and connect relationships, all by dragging and dropping items on a canvas.

![](https://helpv2.quickbase.com/hc/article_attachments/4572853552916/vb.png)

Using Visual Builder, you can test out configurations to determine the best data model for your app.

You can use Visual Builder to create a new app or to update an existing app.

To create a new app using Visual Builder

1.  On My apps, choose **Create new app**.
    
2.  Choose either **Build from a template** or **Start from scratch**. Visual Builder appears.
    
3.  You can use Visual Builder to name your app, choose an icon and color, create tables, fields, and relationships for your app, then choose **Create app** (top right).
    

To update an existing app in Visual Builder

Note that when working with an existing app, changes in Visual Builder are saved immediately. When first trying out Visual Builder with an existing app, you may want to use a copy of your app.

1.  Open your app and select **Settings**.
    
2.  In the Basics section, select **Structure**.
    
3.  When working on a table, you can also open Visual Builder by clicking **Settings** > **Structure**.
    

To create table-to-table relationships

To create table-to-table relationships in Visual Builder, use the relationship icon: ![](https://helpv2.quickbase.com/hc/article_attachments/4572817397396/vb-rel-icon.png)

Click and hold the icon to drag a line between tables you want to connect with a relationship. The **Create a table-to-table relationship** dialog appears. To start a same-table or cross-app relationship, single-click the icon to start the relationship dialog.

Relationships between tables in your app are connected with a solid arrow. Cross-app relationships are shown by a dashed arrow from tables pointing to the top of the page.

## Current limitations

Visual Builder does not currently support the following:

**Connected tables.** You cannot use Visual Builder to add connected tables. Visual Builder shows existing connected tables in your app and you can add normal fields, but you cannot add connected fields, make modifications to connected fields or adjust connection properties.

**Summary fields and lookup fields**. Visual Builder may add some lookup fields for you automatically during relationship creation, but you cannot currently use Visual Builder to add summary fields or lookup fields to a relationship. You can exit Visual Builder to edit the relationship, adding summary fields or adding or editing lookup fields.

**Formula field properties**. You can use Visual Builder to add formula field types to your tables, but currently you cannot create or edit formulas or change other properties within Visual Builder.

**Address and List - user field types**. Because these two types include several subfields, you can’t configure address or list - user field types with Visual Builder.

**Number of tables limited to 80**. Currently, if you try to open an existing app with 80 or more tables, a message appears preventing you from opening the app in Visual Builder. If you are using Visual Builder and add an 80th table to your app, a message appears preventing you from adding that table.

**Test as user/test as role**. While these options may appear in the user menu, the “test as user” and “test as role” features don’t function within Visual Builder, because you are working on the app structure.