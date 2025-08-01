## Changing the field type of a field in the refresh key

Note: This functionality is available only to Quickbase Sync CSV early access customers who have the option, if necessary, to combine up to three additional fields to create a unique Refresh Key.

**Caution:** If you change the field type of a field that is included in a composite Refresh Key, we'll permanently delete all data in the connected table. The connected table will remain empty until you refresh it.

You can't change the type of the Refresh Key field itself, but you can change the types of the individual fields that make up the composite [Refresh Key](https://helpv2.quickbase.com/hc/en-us/articles/4570260038804-About-the-Refresh-Key-field-), as long as none of those fields are designated as the [key](https://helpv2.quickbase.com/hc/en-us/articles/4570321550612-Setting-key-fields-for-tables-) of the table. For example, you can change the type of a text field to email address.

If you change the type of a field included in a composite Refresh Key, all the rows in the table will be deleted and remain empty until you refresh your table.

To change a field type of a field included in the Refresh Key:

1.  [Access the field's properties page](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-).
    
2.  Click **Change Type**. If this link doesn't appear on the field's properties page, you can't change the field type.
    
    The Change Field Type page displays.
    
3.  From the **Select a field type** dropdown, choose the new field type, and then click **Change Type**. To ensure accurate data refreshes, we recommend only changing Text fields to the following field types:
    

-   Numeric
-   Numeric – Currency
-   Numeric – Rating (0-5)
-   Date
-   Email Address

## Restrictions to field type changes

In general, the dropdown on the Change Field Type page will contain the allowable list of new field types. Some field types have been called out below:

-   **List - User fields**. You can't change the field type of a List-User field. In addition, you cannot change another field to a List-User field.
    
-   **File attachment fields**. You can't change the field type of a File Attachment field.
    
-   **Multi-select Text fields**. You can't change the field type of a Multi-select Text field. You can change Text and Text - Multiple Choice fields to Multi-select Text fields.
    

### Related topics:

-   [About field types](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-About-field-types-)
    
-   [About the Refresh Key field](https://helpv2.quickbase.com/hc/en-us/articles/4570260038804-About-the-Refresh-Key-field-)
    
-   [About refresh options](https://helpv2.quickbase.com/hc/en-us/articles/4570314286100-About-refresh-options-)