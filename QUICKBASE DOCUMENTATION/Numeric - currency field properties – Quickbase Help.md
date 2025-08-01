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

Related Topic:

-   [Use Shared Value Fields](https://helpv2.quickbase.com/hc/en-us/articles/4570317315604-Using-shared-value-fields-)
    

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

## Display Format

Choose the format used to display numeric values for this field. Organizations in the United States will typically use one of the first two options; organizations in other countries (or who have offices in multiple countries) may want to use any of these options.

| 
Select one of the following options...

 | 

To...

 |
| --- | --- |
| 

12345678.00

 | 

Display numeric values with:

-   decimal mark of period \[.\]
    
-   no thousands separator
    

 |
| 

12,345,678.00

 | 

Display numeric values with:

-   decimal mark of period \[.\]
    
-   thousands separator of comma \[,\]
    
-   commas separating the number into groups of 3
    

 |
| 

1,23,45,678.00

 | 

Display numeric values with:

-   decimal mark of period \[.\]
    
-   thousands separator of comma \[,\]
    
-   commas separating the number into groups of 2, except for the first group of 3
    

 |
| 

12345678,00

 | 

Display numeric values with:

-   decimal mark of comma \[,\]
    
-   no thousands separator
    

 |
| 

12.345.678,00

 | 

Display numeric values with:

-   decimal mark of comma \[,\]
    
-   thousands separator of period \[.\]
    
-   periods separating the number into groups of 3
    

 |
| 

1.23.45.678,00

 | 

Display numeric values with:

-   decimal mark of comma \[,\]
    
-   thousands separator of period \[.\]
    
-   periods separating the number into groups of 2, except for the first group of 3
    

 |

## Separators

Choose when separators appear in numeric values.

| 
Select one of the following options...

 | 

To...

 |
| --- | --- |
| 

Show separator after 3 places

 | 

Display the thousands separator after the value in the field has more than 3 places (i.e., non-decimal part larger than 999)

 |
| 

Show separator after 4 places

 | 

Display the thousands separator after the value in the field has more than 4 places (i.e., non-decimal part larger than 9999)

 |

## Display as

| 
Select one of the following options...

 | 

To display...

 |
| --- | --- |
| 

Simple number

 | 

The number in this field, along with any decimals, separators, or negative signs that have been configured to display. All other characters are ignored.

 |
| 

Star Rating

 | 

The value in this field as 0-5 stars. For example, you might want to use this option in a movie or book review application.

 |
| 

Percent

 | 

The value in this field as a percentage.

 |
| 

Currency

 | 

A [currency symbol](https://helpv2.quickbase.com/hc/en-us/articles/4570305824660-About-Localizing-Currency-Symbols-) of up to 10 UTF-8 characters, and set its placement relative to the number.

Type the currency symbol into the **Symbol** field, either as an HTML character entity or in Unicode decimal format. For example, to display a pound sign (£), enter one of the following:

-   **&pound;** (HTML character entity)
    
-   **0163** on the number pad while holding down the ALT key (Unicode decimal format)
    

To specify the placement of the currency symbol, select one of the following options from the Position list:

-   Select **Between "-" and the number** to display the currency symbol between the minus sign and the numerical value. For example: -$34.95
    
-   Select **Before number** to display the currency symbol on the left side of the value. For example: $-34.95
    
-   Select **After number** to display the currency symbol on the right side of the value. For example: 34.95$
    

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