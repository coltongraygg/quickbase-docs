## Convert fields (or columns) into tables

Quickbase makes it easy to turn a field into a new [table](https://helpv2.quickbase.com/hc/en-us/articles/4570326161428-What-Is-a-Table-) in your app. Display a table report that includes the column in question and then click to convert the field into its own table, including related fields.

Warning

Once you convert a field into a new table, **you cannot undo this action**. Your field will no longer exist in the original table. If you're not certain that you need a new table, [copy the app](https://helpv2.quickbase.com/hc/en-us/articles/4570366892692) and test this procedure on the copy before you proceed.

If you need to split a table into three or more tables, read the [Splitting a single table into multiple tables](https://helpv2.quickbase.com/hc/en-us/articles/4570316396180-Convert-fields-or-columns-into-tables#h_01H297WTZC2FW3KT11KN19RQJS) section before you begin.

## Default table report: Move field into new related table

In the default table report, you can move a single field into a new related table. (Moving multiple fields at a time is only available in the legacy table report.)

1.  [Open](https://helpv2.quickbase.com/hc/en-us/articles/4570317119252-Displaying-a-report-) a [table report](https://helpv2.quickbase.com/hc/en-us/articles/4570394832916-About-Table-reports-) that contains the field you want to convert into a table.
    
2.  Click on a column heading more menu ![](https://helpv2.quickbase.com/hc/article_attachments/16295295926804).
    
3.  Select **Move field to new related table**.
    
4.  You will see a dialog box. Fill out the information and then click **Next**.
    -   Choose a name for your new table
    -   Choose an icon for your new table
    -   Choose what to call individual records
    -   (Optional) add a description
5.  You will see a preview of the records that will be created in the new table. Review the preview and then click **Move field**. You will be redirected to the new table.

The new table is related to the existing table as the _parent_ table. 

-   [Learn more about relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-)
    
-   [Learn how to create a relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-)
    

Note

If the field used to create a new table was a formula field, the current calculated value in the field is saved to the new table. The original formula will not carry over.

## Legacy table report: New table based on this field

1.  [Display](https://helpv2.quickbase.com/hc/en-us/articles/4570317119252-Displaying-a-report-) a [table report](https://helpv2.quickbase.com/hc/en-us/articles/4570394832916-About-Table-reports-) that contains the field you want to convert into a table.
    
2.  Click on a column heading menu ![](https://helpv2.quickbase.com/hc/article_attachments/16296361095060).
    
3.  Select **New table based on this field**.
    
4.  A dialog box appears, which shows you the unique values that Quickbase found in the field. Each value listed will be a record in the new table.
    
5.  If you want to add more fields to the table, click the **Additional Fields** button in the dialog box. See [Adding additional fields to the new table](https://helpv2.quickbase.com/hc/en-us/articles/4570316396180-Convert-fields-or-columns-into-tables#h_01H2BHR072AKCDKEAKBBQQGY2R).
    
6.  Click **Next**.
    
7.  Click **Continue** to dismiss the warning dialog.
    
8.  In the dialog box that displays, type in a name for the new table.
    
9.  Type in a term for items in the new table and click **Continue**.
    
    Quickbase displays a message telling you that it has created the new table. The table itself now appears at the end of the table list on the sidebar. (Want it in a different spot? [Reorder your tables](https://helpv2.quickbase.com/hc/en-us/articles/4570355475092-Reorder-Tables-in-an-Application-).)
    

The new table is related to the existing table as the _parent_ table.

-   [Learn more about relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-)
    
-   [Learn how to create a relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-)
    

### Adding additional fields to the new table

When you create a new table from an existing field, you can also choose to bring other additional fields. 

1.  In the dialog box that shows you the unique values in the field, click the **Additional Fields** button.
2.  To select a field that you want to add to a table, select the checkbox next to the field name.
    
3.  When you've made all your selections, click **OK** to dismiss the dialog
    

Moving more than one field into a new table can require some extra clean up. For example, say you're converting your Companies column into its own table. One company, Acme Corporation, has offices in New York, Dallas, and Portland. So, when you add the City column to the conversion, Quickbase finds three different locations for Acme. A single value in the column you're converting can only match one value in any additional field. You need to clean up the extra cities before you can create the new table. 

-   If you want to create three separate Acme records (Acme-New York, Acme-Dallas, and Acme-Portland) click the **Conform** link at the top of the column. Quickbase will create unique entries for each combination.
-   If the dissimilar entries are mistakes (say Acme only has one office in New York and the other locations are data-entry errors) go back into your table and correct the inconsistencies—in this case, changing all locations to New York. Then try the conversion again.

## Splitting a single table into multiple tables

You can convert columns into more than one table, but we suggest planning carefully before you being moving fields.

-   Determine how all your tables should relate to each other. Remember, converting a column into a table always creates a [parent table.](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-)
-   Create the first parent, then the parent of that table, then the parent of that table, and so on

**Example:**

Your original table tracks sales. You want to convert this table into three tables:

-   Customers
-   Invoices
-   Products

One customer can have many invoices. Each invoice can have multiple products on it. So, in terms of table relationships, that means:

-   Customers will be a parent table to Invoices
-   Invoices will be a parent table to Products

To create this setup, break out the tables in steps. Your original table which now holds everything will eventually be the Products table—the child table at the end of the line.

1.  Create the parent to the Products table, which is the Invoices table.
    -   Convert the Invoice Number column into its own table. Include all the columns that don't belong in the Products table, too. That means, you'll include not only those columns that belong to the Invoices table but also those that will belong to its parent, the Customers table.
2.  Once you've created the Invoices table, convert the Customer column into its own table. Include all fields that contain customer details.

### Related topics:

-   [Creating a new report](https://helpv2.quickbase.com/hc/en-us/articles/4570327815572-Create-a-new-report-)
    
-   [Displaying a report](https://helpv2.quickbase.com/hc/en-us/articles/4570317119252-Displaying-a-report-)
    
-   [What's a table?](https://helpv2.quickbase.com/hc/en-us/articles/4570326161428-What-Is-a-Table-)
    
-   [About table reports](https://helpv2.quickbase.com/hc/en-us/articles/4570394832916-About-Table-reports-)
    
-   [About table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-)