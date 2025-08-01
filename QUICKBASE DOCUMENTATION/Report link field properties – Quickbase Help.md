## Report link field properties

Report link fields appear in the parent table and display as links. When you choose a report link, you see the related records from the child table. Report links help you get more information between tables quickly. For example, if you were to choose an project’s tasks link, you’d see a list of all the tasks for that project. Unique features of report links:

-   They appear as links on reports / dashboards
-   When a report link is on a form, you have the option to display it as an embedded report

The properties for this field type are:

## Label

Enter a name for this field. This name displays on data-entry forms and as column headings in reports.

## Type

Click Change Type to change the field type.

**Related Topic:**

-   [About Field Types](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-About-field-types-)

## Field relationship

You can match the values in a field from this table to a field in a different table. For example, if you want to match company names, enter the name of the field in the target table that contains company names.

To create a field relationship:

1.  Under Match the values in this field from this table, select the field that you want in this table.
    
2.  Click **Select Target**, select an application that you want, then select the field in the target table that contains the data that you want to match.
    

## Value matching

Select Only include values if they match exactly in both fields to require that the word or phrase (for example, the company name) in the source application table matches the word or phrase in the target application table.

For example, if you are matching company names and select this option if the company name in the source application table is "Bayshore Oil Co." and the company name in the target application table is "Bayshore Oil," then no match occurs. However, if you clear the Only include values if they match exactly in both fields checkbox, a match occurs because Quickbase ignores "Co." and "Corp.".

## Link behavior

Select **Open link in a new browser window** to display the Web page in a new browser when you click the link to view it.

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

###### To set the permissions:

1.  Click **Restrict access by role** to limit access to the data in this field.
    
    When selected, the Role and Permission list appears.
    
2.  Select either None, View, or Modify for each role.
    

Note: This property is not available to accounts on the Quickbase Essential plan.

Related Topic:

-   [About Roles](https://helpv2.quickbase.com/hc/en-us/articles/4570323434516-About-Roles-)

## Searchable

Select to allow the field to be included when searching or filtering the table.

## Reportable

###### To use this field in reports:

1.  Select Add this field to all new reports to display this field as a column when users create but don't customize reports.
    
    When selected, automatically selects **The field may be used in reports** option.
    
2.  Select The field may be used in reports to use this field in reports.
    
    If you want the field to be a default column, you must select this option.
    

**Related Topics:**

-   [How Quickbase Uses Default Report Settings](https://helpv2.quickbase.com/hc/en-us/articles/4570348881300-Setting-reporting-defaults-)
-   [Specify which fields are reportable](https://helpv2.quickbase.com/hc/en-us/articles/4570402784276-Specify-Which-Fields-are-Reportable-)

## Shared values

###### To make entries in this field available as choices in another field:

1.  Select Values from this field may be a source for dropdown lists in other apps, then click **Add App**.
    
2.  Select an application, then click **OK**.
    

Related Topic:

-   [Use Shared Value Fields](https://helpv2.quickbase.com/hc/en-us/articles/4570317315604-Using-shared-value-fields-)

## Field help text

If you want to provide help text in association with this field, enter it in the text box. This text will display via the information (![](https://helpv2.quickbase.com/hc/article_attachments/21170874931476)) icon next to the field.