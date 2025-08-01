## Designating reference proxy fields

Once you've created a [table-to-table relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-), you may find that the [reference field](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-#fieldtypes) doesn't show the information you want. For example, when you display a record or report, the field may show the Record ID#. You may want to show more meaningful information, such as project name or company.

Numbers may be shown in reference fields because Quickbase typically uses the parent table's key field (such as Record ID#) to link the tables together. But, you don't need to use the reference field in reports and on forms. Instead, Quickbase lets you designate a _**reference proxy field**_. Use this feature to specify that another field, containing more user-friendly information, should look and act like the reference field when you create or edit a child record.

For example, instead of **Record ID#**, use the **Company Name** field. You then use this reference proxy field in reports and forms instead of the reference field. You can still use the field to select values from a parent table or to access the parent record.

If you add at least one [lookup](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-) field to your table-to-table relationship, then that field is designated as the reference proxy automatically. But you may need to add or change the reference proxy field settings for a table-to-table relationship in your app.

You designate reference proxy fields within the properties of the relationship's reference field, in the child table.

Before you start, the child table needs to include at least one **lookup** field, which includes data from the parent table, or at least one **formula** field, which could also include data from the lookup fields, as these field types are included as choices for the reference field proxy.

Tip: You can [create a formula field](https://helpv2.quickbase.com/hc/en-us/articles/4570376002580-Using-Formulas-in-Quickbase-) that combines values from lookup fields, then you can select that formula field as your proxy field. For example, you may want to combine a project manager first name field and a project manager last name field into a single entry.

To designate a reference proxy:

1.  [Access the field properties](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-) of the relationship's reference field, either by [editing the relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570416568468-Adding-fields-to-table-to-table-relationships-) or opening table settings.
    
2.  In the **Reference field options** section, click the **Proxy field** drop-down and select the field you want.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572827917716/refproxy.png)
    
3.  Click **Save** in the upper right to save the field properties.
    
4.  Add the reference proxy field to any additional reports and forms.
    
5.  You may also want to review the [record picker settings](https://helpv2.quickbase.com/hc/en-us/articles/4570419445524-Setting-record-picker-display-fields-) for your tables, to customize the values that appear in your reference proxy field.
    

### Related topics:

-   [About table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-)
    
-   [Creating table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-)
    
-   [Adding fields to table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570416568468-Adding-fields-to-table-to-table-relationships-)
    
-   [Deleting fields from table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570319687956-Deleting-fields-from-table-to-table-relationships-)
    
-   [Creating summary fields](https://helpv2.quickbase.com/hc/en-us/articles/4570321780372-Creating-a-summary-field-)
    
-   [Creating lookup fields](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-)
    
-   [Deleting table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570433178260-Deleting-table-to-table-relationships-)
    
-   [Creating many-to-many relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570285625236-Creating-many-to-many-relationships-)