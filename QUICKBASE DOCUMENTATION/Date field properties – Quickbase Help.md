## Date field properties

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

## Default Value

Select **Today** to make today's date automatically appear in this field each time users create a new record. Users can change this value, if they want.

## Default sort order

| 
Select this option...

 | 

To...

 |
| --- | --- |
| 

Ascending

 | 

Sort numeric values in ascending order.

 |
| 

Descending

 | 

Sort numeric values  in descending order.

 |

## Format

By default, the date displays in the following format: 07-08-2008. To format the date differently, select one or more of the following options:

| 
Select any of the following options...

 | 

To display...

 |
| --- | --- |
| 

Show the month as a name

 | 

The first three letters of the name of the month. For example, JUL-08-2012.

 |
| 

Show the day of the week

 | 

The day of the week and the date. For example, Sunday, 07-08-2012.

 |
| 

Don't show the year for dates in the current year

 | 

The date using commas, for example, 07, 08, 2012.

If the date falls within the current year, Quickbase does not display the year. For example, if you enter 07-08-2012, and the current day falls within 2012, the date that appears is 07 08.

Tip: Select Show the month as a name to display the date as Jul 08, 2012.



 |

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

To set the permissions:

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

To use this field in reports:

1.  Select Add this field to all new reports to display this field as a column when users create but don't customize reports.
    
    When selected, automatically selects **The field may be used in reports** option.
    
2.  Select The field may be used in reports to use this field in reports.
    
    If you want the field to be a default column, you must select this option.
    

**Related Topics:**

-   [How Quickbase Uses Default Report Settings](https://helpv2.quickbase.com/hc/en-us/articles/4570348881300-Setting-reporting-defaults-)
-   [Specify which fields are reportable](https://helpv2.quickbase.com/hc/en-us/articles/4570402784276-Specify-Which-Fields-are-Reportable-)

## Shared values

To make entries in this field available as choices in another field:

1.  Select Values from this field may be a source for dropdown lists in other apps, then click **Add App**.
    
2.  Select an application, then click **OK**.
    

Related Topic:

-   [Use Shared Value Fields](https://helpv2.quickbase.com/hc/en-us/articles/4570317315604-Using-shared-value-fields-)

## Snapshot

To capture a value from a specific lookup field:

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