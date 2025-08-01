## Changing the field type of existing fields

**Caution:** Changing a field's type modifies all the data in the field so that it conforms to the new field type. **If the data cannot be converted, it is lost.** To prevent the loss of data, [duplicate the field](https://helpv2.quickbase.com/hc/en-us/articles/4570321855636-Copy-a-Field-) that you want to change, and then make changes to the duplicate.

## To change a field type

You can change [field types](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-About-field-types-) using either field settings or [Visual Builder](https://helpv2.quickbase.com/hc/en-us/articles/4570376993300-Quickbase-Visual-Builder-).

### Using field settings to change field types

1.  [Access the field's properties page](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-).
    
2.  Click **Change Type**. (If this link does not appear on the field's properties page, then the field type cannot be changed.) The **Change Field Type** page displays.
    
3.  From the **Select a field type** dropdown, choose the new field type, and then click **Change Type**. **Important**: This change is saved as soon as you click **Change Type**.
    

### Using Visual Builder to change field types

1.  Open a table, click **Settings**, then click **Structure**. Visual Builder opens with the table expanded.
    
2.  Hover on the field, then click the edit icon:
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572832085012/vb-change-field-card_400x367.png)
    
3.  Using the menu in the second column to change the field type, and then click outside of the field. All changes are saved automatically.
    

## Restrictions to field type changes

In general, the field type menus in field settings and in Visual Builder contain the allowable list of new field types. Some field types have been called out below:

-   **List - user fields**. You can't change the field type of a List - user field. In addition, you cannot change another field to a List - user field.
    
-   **Multi-select text fields**. You can't change the field type of a Multi-select text field.
    

### Related topics:

-   [About field types](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-About-field-types-)