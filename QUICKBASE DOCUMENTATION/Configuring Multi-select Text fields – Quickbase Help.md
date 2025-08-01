## Configuring Multi-select Text fields

A multi-select text field type allows users to choose multiple text values within a single field. Multi-select text fields can contain whatever text values you like, for example, locations for a project, areas of a product to demo, or events someone might attend at a conference.

If you've been using multiple checkboxes or other fields to record values that should appear in one field, you can use multi-select Text fields to simplify your app. Likewise, if your requirements for tracking data have led you to create tables in a [many-to-many relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570285625236-Creating-many-to-many-relationships-), you may be able to simplify your app with multi-select Text fields.

![2024-09-23_12-30-16 (1).gif](https://helpv2.quickbase.com/hc/article_attachments/30864998182036)

To create a multi-select text field:

1.  Open field settings for a table in the sidebar by hovering over a table name, opening the menu, and selecting **Fields**.
2.  Select **New Fields** to add new fields.
3.  In the **Field Label** box, enter a name for the field.
    
4.  From the **Type** list, select _Multi-select Text_, and then select **Add fields**.  
    This adds the field to the table.
    
5.  On the new page, add the list of choices for your new field.
    
    Each choice must be on a separate line. Enter up to 100 items in the list. Each item can have up to 60 characters. You can also [specify a shared value field](https://helpv2.quickbase.com/hc/en-us/articles/4570317315604-Using-shared-value-fields-#config_values_shared) on the new field's Properties page.
    
6.  Select how values in the field will be sorted (alphabetically, or in the order they appear in the list).  
    To allow users to add new choices to the list in the field, select the **Allow users to create new choices** checkbox.
    

Every field type has properties that are unique to it, which you can change at any time. Learn more about how to [Change the properties of a field](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-).

To convert a series of checkbox fields to one multi-select text field:

Many people used a series of checkbox fields to record values before the multi-select text field was added to Quickbase. In this section, learn how to consolidate all those fields into one multi-select text field.

1.  Create a Formula - Text field.
    
2.  Enter the formula shown below, substituting your checkbox field names for _Field 1_, _Field 2_, and so on.
    
    ```
    List(";",
    ```
    
    ```
    If([Field 1]=true," Field 1", ""),
    ```
    
    ```
    If([Field 2]=true, " Field 2", ""),
    ```
    
    ```
    If([Field 3]=true, " Field 3", ""),
    ```
    
    ```
    If([Field 4]=true, " Field 4", ""),
    ```
    
    ```
    If([Field 5]=true, " Field 5", "")
    ```
    
    ```
    )
    ```
    
3.  Save your changes.
    
4.  Copy the field.
    
5.  Convert the copied field to multi-select text.
    
6.  Create a table report containing all the checkbox fields, the formula - text field, and the new multi-select text field. Use the report to verify that your data was correctly transformed.
    

Substitute the new multi-select text field for the checkbox fields on forms and reports. When you are sure that the checkbox fields and the formula - text field that you created are no longer needed, you can delete those fields.

## When _can_ you use multi-select text fields?

For the most part, you can use multi-select text fields in the same way you use other fields. You can filter reports, email notifications, and email reminders using these fields. You can sort and group reports by multi-select text fields.

You can also use multi-select text fields as lookup fields when you create a relationship or cross-application relationship between tables.

## When _can't_ you use multi-select text fields?

In some areas, Quickbase does not currently allow the use of multi-select text fields. This field type may not be used:

-   in conditional dropdowns
    
-   for summary fields
    
-   to supply values for [shared value fields](https://helpv2.quickbase.com/hc/en-us/articles/4570317315604-Using-shared-value-fields-)
    
-   as key fields
    

### Related topics:

-   [Entering and editing data in Multi-select Text fields](https://helpv2.quickbase.com/hc/en-us/articles/4570343376660-About-Multi-select-Text-fields-)
    
-   [Label](https://helpv2.quickbase.com/hc/en-us/articles/4570283477140-Multi-select-text-field-properties)
    
-   [Includes and Does not include](https://helpv2.quickbase.com/hc/en-us/articles/4570261800084-Filtering-records-using-fields-with-multiple-values-)
    
-   [Basic field information](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-About-field-types-)