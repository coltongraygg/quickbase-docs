## Rich text field properties

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

## Log entries

Select **Log the edits to this field and show them on forms** to log the entries to this field. Useful for revision tracking, comments, or notes.

## Mention users

Use the **Mention users** property to set up collaboration tools in your app.

1.  Select **Enable users to mention others by typing @FirstName LastName**.When selected, users can can type the @ symbol in a rich text field. Then they can enter the name of the person they want to mention or select one from the list.
2.  Create a [custom email](https://helpv2.quickbase.com/hc/en-us/articles/26055881235732) and set it up to send to users @mentioned in the rich text field.

When these two steps are completed, users can mention other app users and those app users will receive an email notifying them of the mention.

## Display

To set the properties for displaying this field, enter the following:

-   Number of lines
-   Max characters
-   Width of input box.

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

If you want to provide help text in association with this field, enter it in the text box. This text will display via the information (![](https://helpv2.quickbase.com/hc/article_attachments/26886588507924)) icon next to the field.