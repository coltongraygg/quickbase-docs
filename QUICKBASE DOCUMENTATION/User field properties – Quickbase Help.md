## User field properties

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

## Choices

You can use the default user set or create your own custom user set for field options.

To determine who is in your default set:

Click **Users** on the sidebar to show the Manage Users page. The users who have a green check mark in this column are members of the default user set.

To choose the set of users that will appear in the field:

Select one of the following options:

-   Click Default user set to use the default user set for this application.
    
-   Click **Custom user set** to create a custom list of users, then add or remove users from the list.  
    Enter each item on its own line.  
    

To allow users to create new choices:

Select the **Allow users to create new choices** checkbox if you want the app's users to add choices to the list.

Tip: Leave the **Default Value** option in the Basics section blank to initially show nothing in the list.

To set the invitation behavior when new users are added:

Select one of the following options:

-   Click ask whether to send them invitations to display a dialog when you save the record after adding a new user. The dialog allows you to choose whether to send an invitation to each new user, and what role (if any) to put that user into.
    
-   Click don't invite them or give them a role to automatically add the new user to the None role without sending an invitation.
    

Related Topic:

-   [Manage Users in an Application](https://helpv2.quickbase.com/hc/en-us/articles/4570360058132-Manage-Users-in-an-Application-)

## Value Display

These two properties apply when the field appears in table and timeline reports.

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
Select one of the following options...

 | 

To...

 |
| --- | --- |
| 

Full Name

 | 

Display the first name and last name of the user.

Note: If a user doesn't enter a full name during registration, Quickbase displays the email address.



 |
| 

Last Name, First Name

 | 

Display the full name of the user, but with the last name displaying first. This format lets you create reports that correctly sort by last name.

Note: If a user doesn't enter a full name during registration, Quickbase displays the email address.



 |
| 

User Name

 | 

Display the Quickbase user name of the user.

Note: If a user doesn't have a user name, Quickbase displays the email address.



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

If you want to provide help text in association with this field, enter it in the text box. This text will display via the information (![](https://helpv2.quickbase.com/hc/article_attachments/26812985040532)) icon next to the field.