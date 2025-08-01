## Text-multiple choice field properties

The properties for this field type are:

## Label

Enter a name for this field. This name displays on data-entry forms and as column headings in reports.

## Type

Click Change Type to change the field type.

Some field types (List-User, Multi-select Text, and File Attachment, for example) may not be changed. The **Change Type** link will not be present if this is the case.

**Related Topic:**

-   [About Field Types](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-About-field-types-)

## Required

Select Must be filled in to require users to enter a value in this field. A red asterisk (\*) beside a field in Add and Edit forms indicates that this value has been set for the field.

## Unique

| 
Select this option...

 | 

If you want to...

 |
| --- | --- |
| 

Must be unique

 | 

Ensure that every entry in this field is different.

This is useful for fields that contain information such as product serial numbers or ID numbers.

 |
| 

Check existing entries for duplicate values

 | 

Change a field in an existing application to require unique values and want to require that all previously entered data is unique.

To display this option, select **Must be unique**.

If Quickbase finds existing values in this field that aren't unique, an error message appears and Quickbase clears the **Must be unique** checkbox. If this occurs, you can do one of two things:

-   Sort the field to find duplicate values, make corrections as necessary, return to the Properties page, then select both **Unique** checkboxes again.
    
-   Select **Must be unique** if it doesn't matter whether existing data in this field is unique or if you want only new entries in this field to be unique.
    

 |

## Default value

Enter the value that you want for the initial entry or default for this field. For example, you can set the Status field to **Open** for the default, and users can change it, if they want.

For multiple-choice fields, you must enter a value that is in your list of choices. If you don't want any option to appear automatically, leave this field blank.

For Multi-select Text fields, you can specify a list of default values delimited by semi-colons (;).

## Input type

| 
Select this option...

 | 

If you WANT TO...

 |
| --- | --- |
| 

User input

 | 

Let users type information into this field.

Multi-select Text fields do not show this option.

 |
| 

From list

 | 

Let users select an item from a list.  

1.  Type the items to be shown in the list, each item on a separate line.
    
2.  If you don't want users to add choices to the list, unselect Allow users to create new choices.
    
3.  Click Display choices in the order shown here to determine the order of the list, or click Display choices in alphabetical order.
    

 |
| 

From another field

 | 

Use values from another field in a list that appears in this field.

1.  Click Select shared field, select an app, then click **OK**.
    
2.  Select the field type you want, then click **OK**.
    
3.  Click Display choices in the order shown here to determine the order of the list, or click Display choices in alphabetical order.
    

 |

### Limits

There is no hard limit on how many entries this field type can hold. However, we recommend not exceeding several hundred. If there are entries beyond this, you are more likely to see issues.

Related Topic:

-   [Use Shared Value Fields](https://helpv2.quickbase.com/hc/en-us/articles/4570317315604-Using-shared-value-fields-)
    

## Log entries

Select **Log the edits to this field and show them on forms** to log the entries to this field. Useful for revision tracking, comments, or notes.

## Display

To set the properties for displaying this field, enter the following:

-   Number of lines
-   Max characters
-   Width of input box.

### Value Display

These properties apply when the field appears in table and timeline reports.

| 
Select one or more options...

 | 

To...

 |
| --- | --- |
| 

Display in bold

 | 

Display the data in bold.

 |
| 

Display without wrapping

 | 

Prevent the data from being broken into multiple lines.

 |

## Permissions

### To set the permissions:

1.  Click **Restrict access by role** to limit access to the data in this field.
    
    When selected, the Role and Permission list appears.
    
2.  Select either None, View, or Modify for each role.
    

Note: This property is not available to accounts on the Quickbase Essential plan.

Related Topic:

-   [About Roles](https://helpv2.quickbase.com/hc/en-us/articles/4570323434516-About-Roles-)

## Auto-fill

Select **Copy this value...** to copy the value(s) in this field when the record is copied.

The command to copy a record is visible in the **More** menu when you're viewing the record.

Not all fields are good candidates for this option. For example, if you also select **Unique**, the value of this field is not automatically copied.

## Searchable

Select to allow the field to be included when searching or filtering the table.

## Reportable

### To use this field in reports:

1.  Select Add this field to all new reports to display this field as a column when users create but don't customize reports.
    
    When selected, automatically selects **The field may be used in reports** option.
    
2.  Select The field may be used in reports to use this field in reports.
    
    If you want the field to be a default column, you must select this option.
    

**Related Topics:**

-   [How Quickbase Uses Default Report Settings](https://helpv2.quickbase.com/hc/en-us/articles/4570348881300-Setting-reporting-defaults-)
-   [Specify which fields are reportable](https://helpv2.quickbase.com/hc/en-us/articles/4570402784276-Specify-Which-Fields-are-Reportable-)

## Shared values

### To make entries in this field available as choices in another field:

1.  Select Values from this field may be a source for dropdown lists in other apps, then click **Add App**.
    
2.  Select an application, then click **OK**.
    

Related Topic:

-   [Use Shared Value Fields](https://helpv2.quickbase.com/hc/en-us/articles/4570317315604-Using-shared-value-fields-)

## Snapshot

### To capture a value from a specific lookup field:

1.  Select Get this field's value from a lookup field and don't allow the value to change.
    
    When you capture the value of the lookup field in a snapshot, the value in the snapshot field in the details table doesn't change when you change the master record.
    
2.  From the Lookup field list, select the lookup field for which you want to capture the value.
    
3.  Select **Initialize field for existing records** to update all the existing records with a snapshot of the current value when you set up a snapshot field for an application.
    
    Caution: If you select this option and this field contains existing values, the existing values are overwritten with the current value in the master record.
    

**Related Topics:**

-   [Create a Lookup Field](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-)
-   [Setting Up a Snapshot Field](https://helpv2.quickbase.com/hc/en-us/articles/4570403519508-Setting-up-snapshots-of-lookup-fields-)

## Field help text

If you want to provide help text in association with this field, enter it in the text box. This text will display via the information (![](https://helpv2.quickbase.com/hc/article_attachments/4572801516692/information_icon.png)) icon next to the field.