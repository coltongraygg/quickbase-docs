## Create a summary field

To perform calculations in your table, for example total orders based on specific criteria, use summary fields. Summary fields are part of table-to-table relationships. Stored in the parent table of a relationship, they summarize fields from related records in the child table. 

For example, a Sales Orders table is related to a Sales Team table. In the relationship, Sales Team is the parent table, where one team member can have many orders. To determine how many sales each team member closed, or the total revenue each person earned, add a summary field to the Sales team table. This adds a field to each record that calculates these totals.

## Summary Field Caching

> Access to this feature can change based on your Quickbase plan. Learn more about feature availability and plans in [Quickbase capabilities](https://helpv2.quickbase.com/hc/en-us/articles/21309804922004).

While calculations are very fast in most cases, certain fields like formula queries or nested summary fields can start a calculation of hundreds of millions of cells and can get re-calculated on every request, even if the underlying data hasn't changed.

**Note**: Summary fields are available on all plans. **Summary field caching,** however, is only available on the Enterprise plan.

Customers with the Advanced Performance Pack, on our Enterprise plan, can now set eligible summary fields to only evaluate when data changes in the application, improving performance.

![eval.png](https://helpv2.quickbase.com/hc/article_attachments/14616994346004)

The goal of this feature is to give the you the option to use your business case knowledge to determine which of your apps don't need to recalculate a specific field on every request. This is only appropriate when dynamic content doesn't exist in your chain.

## Types of summary fields

The following types of summary fields are available:

-   **The number of _child\_records_ related to that _parent\_record_** – Counts the number of child records related to each parent record.
    
    For example, if your parent table contains salespeople and your child table contains sales orders, Quickbase totals the number of orders for each salesperson and displays the total number of orders in each salesperson's record. The label for this option depends on what you call the records in a table. For this example, the label will be **The number of Orders related to that Salesperson**.
    
-   **A summary of a specific field** – Summarizes a specific field of your choice.
    

-   **Total**—Adds values from specific fields.
    
    For example, if you want to total each salesperson's sales in dollars, select this option and the "Sale Amount" field.
    
-   **Average**—Averages values from a numeric field.
    
-   **Maximum**—Returns the largest (for numeric fields) or latest (for date fields) value.
    
-   **Minimum**—Returns the smallest (for numeric fields) or earliest (for date fields) value.
    
-   **Standard Deviation**—Returns the standard deviation for a particular field.
    
-   **Combined Text**—Combines text values from child records. Use this option to display lists of values from child records, such as listing all the details of an order item along with the order. This option summarizes unique values from text fields only. Duplicate entries are automatically removed. The aggregated list in this field follows summary field rules such as excluding records that you don’t have access to. The field is stored as multi-select text.
    
-   **Combined User**—Combines values from user fields in child records. Use this option to display lists of unique values from user fields only. Duplicate entries are automatically removed. The field is stored as a list-user field. It is possible to filter the values being combined. For example, you can filter the users set to project manager. 
-   **Distinct count**—Provides a count of all the unique values in a field in the child table. For example, you could show many different products were ordered in a given month. The distinct count summary field supports all field types except the following: File Attachment, Predecessor, iCalendar, vCard, Report Link, List User, and Multi-select Text.
    

Another benefit of summary fields is that the data from these fields can be exported and used in formulas. You also can pass the value of summary fields down to the child table using a [lookup field](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-) if you want to use summaries in child table formulas or reports, or export data from the child table.

To create a summary field, you must have an existing [relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-), or [create a relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-) between two tables.

## To create a summary field:

1.  Open the app that contains the relationship you want to enhance with a summary field.
    
    If you created a relationship between tables in two different apps (a cross-app relationship), open the app that contains the child table.
    
2.  Open the table.
    
3.  Select the relationship that you want to edit. The relationship properties appear:
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/19404404284052)
    
4.  Under the **Parent Table** settings on the left side of the screen, click **Add Summary Field**. A **New Summary Field** page appears.
    
5.  Select the type of summary field you want, then select the field.
    
6.  Under **Matching Criteria**, select and add fields to set matching criteria. You may want to summarize only specific records in your table.
    
    Use the Matching Criteria to select the records that you want the summary field to calculate. For example, you may choose to only summarize the tasks that are overdue or only sales figures above a certain amount.
    
7.  Select **Create** in the upper right of the page. A **Choose name** dialog appears.
    
8.  Type a name for the summary field, then click **OK**.
    

Note: When you add a summary field, it doesn't automatically appear on reports or forms. You need to add it yourself by [editing reports](https://helpv2.quickbase.com/hc/en-us/articles/4570281029396-Edit-a-Report-) or [customizing forms](https://helpv2.quickbase.com/hc/en-us/articles/4570300784788-Design-a-Form-).

### Related topics:

-   [Creating table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-)
    
-   [Adding fields to table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570416568468-Adding-fields-to-table-to-table-relationships-)
    
-   [Deleting fields from table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570319687956-Deleting-fields-from-table-to-table-relationships-)
    
-   [Deleting table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570433178260-Deleting-table-to-table-relationships-)