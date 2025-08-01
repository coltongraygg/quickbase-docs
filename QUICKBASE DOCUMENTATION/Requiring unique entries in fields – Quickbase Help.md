## Requiring unique entries in fields

There are certain fields that you never want to contain duplicate values. This might be a field containing the Employee ID or Invoice Number. You can easily prevent a field from having duplicate values by making it unique. In other words, for each record, the value in the field must be different.

A field can be marked as unique when it:

-   Doesn't contain a reference to the record ID#
-   Doesn't contain a reference to a dynamic function
-   Is not a list-user, list-text, phone, or address field
-   Follows the criteria listed in the [Limits in Quickbase article](https://help.quickbase.com/hc/en-us/articles/4570306993940-Limits-in-Quickbase#:~:text=Summary%20fields%20that%20use%20a%20formula%20field%20as%20the%20reference%20field%20are%20only%20supported%20if%20they%20meet%20the%20following%20criteria%3A)

## To require unique values in fields

You can require unique values using either field settings or [Visual Builder](https://helpv2.quickbase.com/hc/en-us/articles/4570376993300-Quickbase-Visual-Builder-).

### Using field settings to require unique values

1.  [Open the field's properties page](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-).
    
2.  In the **Basics** section, select the **Must be unique** check box. You can also check for existing duplicate, non-unique values by selecting **Check existing entries for duplicate values**:
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572878699668)
    
3.  Click **Save**.
    
4.  If you selected to check existing entries, a message appears if there are any duplicates and **Must be unique** is de-selected. You can:
    
    -   Edit existing records to make corrections as necessary, return to the field properties page, then try steps 1-3 again.
        
    -   Select only **Must be unique** if you decide it doesn't matter that existing data in this field is unique, or if you want only new entries in this field to be unique.
        

### Using Visual Builder to require unique values

1.  Open a table, click **Settings**, then click **Structure**. Visual Builder opens with the table expanded.
    
2.  Select the field you want to appear in bold, then use the field properties on the right to select the **Must be unique** checkbox:
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572864212500)
    
3.  All changes are saved automatically.