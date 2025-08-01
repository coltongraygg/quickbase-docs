## Excluding Fields from Searches

You may have an app with fields including information that you don't want to include in search. You can set which fields are included or excluded in searches.

## Understanding Quickbase searches

Quickbase lets you search for data in your app in a number of places, such as:

-   Search (in the global bar)
    
-   When building reports:
    
    -   Filter criteria and Grouping criteria (All report types)
        
    -   Data to summarize and Row grouping (Summary reports)
        
    -   Sorting and Filtering (Calendar reports)
        
    -   Sorting and Grouping (Timeline reports)
        
-   Summary fields
    
-   Email reminders
    
-   Dynamic form rules
    
-   Custom Permissions
    

In each of these areas, you can tell Quickbase you want to find any field with data matching the criteria you specify.

**Note:** Unless absolutely necessary, set all formula query fields as unsearchable in reports.

## The Searchable property

There is a **Searchable** property to include or exclude each field. This property is enabled or disabled by default [depending on the field type](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-About-field-types-), however, you can disable this property for any field so that Quickbase skips over these fields when performing searches that use **<Some field>** as the search criteria.

You can set the Searchable property using either field settings or [Visual Builder](https://helpv2.quickbase.com/hc/en-us/articles/4570376993300-Quickbase-Visual-Builder-).

### Using field settings to set the Searchable property

Set the Searchable property for one field using field properties:

![](https://helpv2.quickbase.com/hc/article_attachments/4572802513428/searchable_property_per_field.png)

Set the Searchable property for several fields at one time by selecting the checkmarks on the field list page.

Note: If you don’t see the **Searchable** column for your app, choose **Advanced Options**, then select to show the Searchable column.

![](https://helpv2.quickbase.com/hc/article_attachments/4572802520724/searchable_column.png)

### Using Visual Builder to set the Searchable property

1.  Open a table, click **Settings**, then click **Structure**. Visual Builder opens with the table expanded.
    
2.  Select the field for which you want to set the Searchable property, then use the field properties on the right. Click **Show more**, then select the **Include this field when searching/filtering this table** checkbox:
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572817161236/vb-searchable.png)
    
3.  All changes are saved automatically.
    

## What happens when I search for a particular field?

Even if you've turned off the Searchable property for a particular field, you can still search that field. Whenever you specify a particular field in a search (instead of using <Some field>), Quickbase searches that field even if you've turned off the property for that field.

To exclude one or more fields from <Some field> searches:

1.  From the table containing the field you want to exclude, click **Settings** in the Page bar, then click **Fields**.
    
2.  If the Searchable column does not appear in the Fields list, click the Advanced Options link, select Searchable, and click Save.
    
3.  Clear the checkmark in the Searchable column for any field you do not want to include in search. 
    

### Related topics:

-   [Preventing Quickbase from searching a table](https://helpv2.quickbase.com/hc/en-us/articles/4570352802964-Prevent-Quickbase-from-Searching-a-Table-)
    
-   [Improving global app search](https://helpv2.quickbase.com/hc/en-us/articles/4570136223764-Improving-Global-App-Search-)