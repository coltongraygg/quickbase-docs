## Logging text field edits

When a user edits a field in your Quickbase application, they overwrite the existing value with a new value, replacing whatever had been there before. But what if you want to keep a record of changes to a particular field? For example, say you have a notes field in which many different staff members enter progress updates and explanations. If you want to keep a record of everybody's entries in a running log, you can do so with a Text - Multi-line field that has been set to keep every edit and add a timestamp and the name of the person who made the change. These fields are sometimes referred to as _append fields_. All the entries display when the field is viewed or edited:

![](https://helpv2.quickbase.com/hc/article_attachments/4572864603540)  
_An append field on an edit form. Whatever you type in the white box would append as a third entry._

To log entries on a Text - Multi-line field:

1.  [Create a new field](https://helpv2.quickbase.com/hc/en-us/articles/4570374838292-Adding-new-fields-) and make its type **Text**.
    
2.  Within the **Fields** list, click the field name to open its properties page.
    
3.  Within the **Text field options** section, select the **Log the edits to the field, and show them on forms** checkbox, and select an option:
    
    -   **Show the name and date on the same line as the entry**. This option records the entry and information about it on the same line. This format is usually best for scenarios in which you'd like to use a formula field to extract or locate specific entries in your append field. Tight Style entries look like this:
        
        \[MAR-14-12 Gladys Glover\] text entry  
        \[MAR-14-12 Gladys Glover\] another entry
        
    -   **Show the name and date on their own line**. This format is less condensed and a bit easier to read. It places the entry and information about it on separate lines separated by a series of dashes, like this:
        
        \-- \[MAR-14-12 Gladys Glover\] --------------  
        text entry  
        \-- \[MAR-14-12 Gladys Glover\] --------------  
        another entry
        
4.  Tell Quickbase where to add the latest entry.
    
    Just below the options mentioned in step 3, you can tell Quickbase where to add the new entries in the field: select the **Show new entries at the bottom of the field** checkbox, or unselect it to add the latest entry to the top of the list).
    
5.  Set how user names are formatted in the append field.
    
    Within an entry, Quickbase can record the user's full name, or user name. To insert a full name, select the **Show full names instead of user names** checkbox. To use a user name instead, turn this checkbox off.
    
6.  If you want, include a timestamp.
    
    To insert a time after the date recorded for each entry, select the **Show the time in addition to the date** checkbox. When you do so, the append field records date and time of each entry.
    
7.  Click **Save**.
    

Tip: If you include an append field in a report, it often takes up a lot of room because it contains so much text. If you want, you can display only the last entry in the append field. To do so, create a formula-text field to hold the value and display that field instead of the text field.

-   If the append field is set to prepend the most recent entry, use this formula to design the formula-text field: `Part([appendfieldname],2,"[")`
    
-   If the field appends entries, try this formula instead: `Right([appendfieldname],"]")`
    

If you find that you want to edit some previously-entered data in your append field you can, by temporarily turning off the append feature. To so do, access the field's properties page (right-click the field label on any form and select **Edit the field properties for this field**). Follow step 3 above (except unselect the checkbox), save your changes, return to the record in question and edit the data. Then return to the field's properties and reselect the checkbox.