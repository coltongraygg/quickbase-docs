## File attachment field properties

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

## Revisions

| 
Select this option...

 | 

To...

 |
| --- | --- |
| 

Keep all revisions

 | 

Store every revision made to a document in Quickbase.

Note: Every version of a document counts toward the total file attachment size limit of the service plan your account is on. Over time, keeping every version of a document could significantly reduce the amount of file attachment space available to other workgroup members.

Maximum number of revisions for a file attached to a table = 100.

 |
| 

Keep the last _n_

 | 

Enter the number of document revisions that you want Quickbase to store in each attachment field.

Note: You can change this number at any time. If you reduce the number, the oldest versions of all documents in this field are deleted. For example, if the current number is 5 and you change the number to 3, Quickbase deletes the two oldest versions of every document with this field type.



 |
| 

Allow users to make older versions the current version

 | 

Let users view previous uploads to this attachment field. Users who can view the revision history can restore a previous version of a document and make it the current version.

 |

## Link Behavior

Select **Use a new browser window for file attachments** to open a file attachment in a new browser window when a user clicks the link to view it.

## Allow Open Access

If you'd like to send a link to a file stored in this field to someone who isn't a Quickbase user, select **Allow access to this file attachment from a Quickbase link without signing in**.

Warning: Any link to a file stored in this field will allow open access to the file for _anyone_ who clicks the link as long as this checkbox is selected. Do not use this option for files that contain sensitive or confidential data.

## Display

You can set the following display options for your file attachments.

### Link Text

You can type in text to display as the link to your file attachment. By default, the file name will display.

### Images

Select **Show .jpg, .png, and .gif files as images in forms** to display a thumbnail image instead of the file name. Users can select the image to view it full size.

![](https://helpv2.quickbase.com/hc/article_attachments/4572857826708/thumbnail_image_forms_200x159.png)

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

## Field help text

If you want to provide help text in association with this field, enter it in the text box. This text will display via the information (![](https://helpv2.quickbase.com/hc/article_attachments/4572801516692/information_icon.png)) icon next to the field.