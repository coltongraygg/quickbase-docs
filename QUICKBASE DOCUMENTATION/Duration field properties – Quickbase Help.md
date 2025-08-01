## Duration field properties

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

## Default value

Enter the value that you want for the initial entry or default for this field. For example, you can set the Status field to **Open** for the default, and users can change it, if they want.

For multiple-choice fields, you must enter a value that is in your list of choices. If you don't want any option to appear automatically, leave this field blank.

For Multi-select Text fields, you can specify a list of default values delimited by semi-colons (;).

## Blank

Do one of the following tasks:

-   Select **Treat blank values as "0" in calculations** to treat blank entries in this field and in calculations as a zero. This is the default.
    
-   Clear this option if you don't want Quickbase to treat blank entries as a zero and in calculations as a zero, for example, when calculating averages.
    

## Totals and averages

| 
Select this option...

 | 

To...

 |
| --- | --- |
| 

Display a total of this field in reports

 | 

Have Quickbase compute the sum of all the values in this field and display the result at the bottom of the view (totals row).

 |
| 

Display an average of this field in reports

 | 

Have Quickbase compute the average of all the values in this field and display the result at the bottom of the view (average row).

 |

## Decimal places

Enter the number of digits you want to appear after the decimal point. For example, you might enter 2 if the field is a price field. If a user enters more digits after the decimal point than you enter here, Quickbase rounds the number and extends it only to the number of decimal places you specify. Here are some examples:

-   .5 rounds the number away from 0.
    
-   3.5 rounds to 4
    
-   \-3.5 rounds to -4.
    

Use the Round formula instead of the decimal places option to round up .5, meaning that -3.5 would round to -3.

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

| 
Select one of these options...

 | 

To display the duration in...

 |
| --- | --- |
| 

HH:MM

 | 

Hours and minutes. For example, **03:45**.

 |
| 

HH:MM:SS

 | 

Hours, minutes, and seconds. For example, **03:45:22**.

 |
| 

:MM

 | 

Minutes only. For example, if you enter "45 min," it displays as **:45**.

 |
| 

:MM:SS

 | 

Minutes and seconds. For example, if you enter ":45.25 min," it displays as **:45:15**.

 |
| 

Smart Units

 | 

The most appropriate format for the value you enter. For example, "120 min" displays as **2 hours**. "84 hrs" displays as **3.5 days**. How smart is that?

 |
| 

Weeks

 | 

Number of weeks. For example, if you enter "84 hrs," it displays as **.5**.

 |
| 

Days

 | 

Number of days. For example, if you enter "84 hrs," it displays as **3.5**.

 |
| 

Hours

 | 

Number of hours. For example, if you enter "3.5 days," it displays as **84**.

 |
| 

Minutes

 | 

Number of minutes. For example, if you enter "3.5 days," it displays as **5040**.

 |
| 

Seconds

 | 

Number of seconds. For example, if you enter "3.5 days," it displays as **302400**.

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