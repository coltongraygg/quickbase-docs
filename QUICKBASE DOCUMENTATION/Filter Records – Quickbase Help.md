When you're creating a [report](https://helpv2.quickbase.com/hc/en-us/articles/4570317429908-About-reports-and-charts-) or doing an [advanced search](https://helpv2.quickbase.com/hc/en-us/articles/4570326980500-Use-Advanced-Search-) operation, often you want to see only records that fall within specific parameters. For instance, you may want to see records that are assigned to a particular user, or only those records with a certain status. To do so, you set initial filter criteria to tell Quickbase what values the data must match to meet your requirements and appear in the set of records returned.

Note: Setting initial filter criteria differs from configuring [dynamic filters](https://helpv2.quickbase.com/hc/en-us/articles/4570135862420-About-Dynamic-Filters-). The initial filter criteria determine what records are shown when the report or search is run. The dynamic filters are shown along with the query results.

This topic describes:

-   [Creating a filter](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records#Creating_a_filter)
    
-   [Comparing a field to a specific value](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records#Comparing_a_field_to_a_specific_value)
    
-   [Comparing the value in one field to the value in another](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records#compare_fields)
    
-   [Filtering on dates relative to today’s date](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records#Filtering_on_dates_relative_to_today_s_date)
    
-   [Adding and removing filter criteria](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records#Adding_and_removing_search_criteria)
    
-   [Re-ordering filter criteria](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records#reordering_filters)
    
-   [Reporting on file attachment fields](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records#Reporting_on_file_attachment_fields)
    
-   [Filtering example](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records#Filtering_Example)
    

If you want to filter on List - User fields, you need to understand how the operators you choose will affect your results. [Click here to learn more.](https://helpv2.quickbase.com/hc/en-us/articles/4570261800084-Filtering-records-using-fields-with-multiple-values-)

Note: If you use the Report Builder, you can create both simple and complex queries. [Learn more](https://helpv2.quickbase.com/hc/en-us/articles/4570253942036-Building-Queries-).

## Creating a filter

When you create a filter, you're telling Quickbase to return only records that have passed some rule or condition you've created. To create a condition, you specify the following:

-   The field you want to filter on. For example, if you’re searching for the field “Start Date,” typing in “Date” will get you a filtered list of all field names that include “Date” along with any Date or Date/Time fields on your table
    
-   An operator. The operator tells Quickbase how to filter the records. Example operators are: is equal to, is greater than, is greater than or equal to, and so forth.
    
-   **A matching value or a value in another field.** Depending on the type of field you're filtering on and what operator you chose, you may have to type in a value or choose one from a list.
    

For instance, if you want to see all tasks that are in progress, you'd choose the following:

| 
Field

 | 

Operator

 | 

Matching value

 |
| --- | --- | --- |
| 

Status

 | 

is equal to

 | 

In progress

 |

## Comparing a field to a specific value

You can create reports that find records where fields match a certain value that you specify. To create a report that finds a specific matching value, you simply enter or select a value in the field that appears when you choose an operator.

![](https://helpv2.quickbase.com/hc/article_attachments/4572816556948/matchingvalue.png)

## Comparing the value in one field to the value in another

You can also write reports that find records where a field value matches the value in another field of the same type.  For instance, in a project management application, you might want to create a report that shows records where the value in the Estimated Hours field exactly matches the value in the Actual Hours field

### Field types that can be used as a query's matching value

Note that you can compare only fields of the same type. In the example below, the two fields being compared are both Date fields. When you choose "the date in the field," Quickbase displays only those fields whose type matches the field type of the field being compared.

![](https://helpv2.quickbase.com/hc/article_attachments/4572816574484/valueinthefield.png)

The following table lists valid matches for all field types:

| 
Field type

 | 

Notes

 |
| --- | --- |
| 

Text

 | 

You can compare any Text field with any other Text field. Text fields are:

-   Text
    
-   Text - Multi-line
    
-   Text Multiple Choice
    
-   Formula - Text
    

Note that you can mix and match the types above--that is, you can compare a simple Text field with a Formula - Text field in your query.

 |
| 

Numeric

 | 

You can compare any Numeric field with any other Numeric field. Numeric fields are:

-   Numeric
    
-   Numeric - Currency
    
-   Numeric - Percent
    
-   Numeric - Rating
    
-   Formula - Numeric
    

Note that you can mix and match the types above – that is, you can compare a simple Numeric field with a Numeric - Percent field in your query.

 |
| 

Date

 | 

You can compare any Date field with any other Date field. Date fields are:

Date

Date/Time

Formula - Date/Time

Note that you can mix and match the types above--that is, you can compare a Date field with a Date/Time field.

 |
| 

Checkbox

 | 

You can compare Checkbox fields with other Checkbox fields or Formula - Checkbox fields.

 |
| 

Duration

 | 

You can compare Duration fields with other Duration fields or Formula - Duration fields.

 |
| 

Email Address

 | 

You can compare Email Address fields with other Email Address fields or Formula - Email Address fields.

 |
| 

List-User

 | 

You can compare List-User fields with other List-User fields and Formula List-User fields.

 |
| Multi-select Text | You can compare Multi-select Text fields with other Multi-select Text fields. |
| 

Phone Number

 | 

You can compare Phone Number fields with other Phone Number fields or Formula - Phone Number fields.

 |
| 

Time of Day

 | 

You can compare Time of Day fields with other Time of Day fields or Formula - Time of Day fields.

 |
| 

URL

 | 

You can compare URL fields with other URL fields and Formula - URL fields.

 |
| 

User

 | 

You can compare User fields with other User fields and Formula - User fields.

 |
| 

Work Date

 | 

The Work Date field type is available only in tables that contain Predecessor fields. Work Dates are different from other Date fields and can be compared only to other Work Date fields.

 |

### Field types that can't  be used as a query's matching value

You cannot use the following field types as the matching value in a query:

-   Predecessor
    
-   iCal
    
-   vCard
    
-   File attachment
    
-   Duration
    
-   Report link
    

## Filtering on dates relative to today’s date

When filtering on dates, you can use the following operators to compare a date field with a specific date you enter:

-   is equal to
    
-   is not equal to
    
-   is before
    
-   is after
    
-   is on or before
    
-   is on or after
    

You can also use two additional operators to find records relative to today’s dates:

-    is during
    
-    is not during
    

These operators let you search for records that contain dates relative to today—that is, you can find records that are due this week, next month, and in the next 3 quarters. [Learn more about reporting with relative dates.](https://helpv2.quickbase.com/hc/en-us/articles/4570263936660-Understanding-Relative-Date-Ranges-)

## Adding and removing filter criteria

If you want to specify criteria for more than one field, Quickbase makes it easy. If, for instance, you want to see all overdue project tasks in a certain project for a certain employee, you'll want to filter on three fields: Assigned to, Project Name, and Days Overdue.

Quickbase makes it easy to add or remove filtering criteria to your report.

Quickbase starts you off with a single field. You can set a single line of criteria, or add more fields if you'd like. Simply hover your mouse over the field dropdown. Plus and minus sign icons appear to the right of the field.

At any point in your list of criteria, you can use the plus sign (![](https://helpv2.quickbase.com/hc/article_attachments/4572793303316/plusicon.png)) icon to add another line of filter criteria. Use the minus sign (![](https://helpv2.quickbase.com/hc/article_attachments/4572793320468/minusicon.png))  icon to delete the current line.

## Re-ordering filter criteria

If you are working with a lot of data, sometimes re-ordering your filter criteria will speed up reporting. Filter criteria are executed in order, so for best performance, put the filter criteria that eliminate the largest number of records first. Instead of searching for _Task Name contains "network"_, then _Task Status is equal to Overdue_, reversing the order of those filters might make the report run much faster.

Simply hover over a row in the list of filter criteria, then click anywhere in the blue highlighted area. The row is selected, and up (![](https://helpv2.quickbase.com/hc/article_attachments/4572801922452/criteria_up.png)) and down (![](https://helpv2.quickbase.com/hc/article_attachments/4572823842196/criteria_down.png)) controls appear on the left side of the row. Use these controls to move the selected row up or down.

Note: The selected row may only be moved up or down in its current indentation level. If you'd like to indent a row to create a filter set, use the new set (![](https://helpv2.quickbase.com/hc/article_attachments/4572781080980/newseticon.png)) icon. [Learn more about filter sets](https://helpv2.quickbase.com/hc/en-us/articles/4570253942036-Building-Queries-).

To de-select the row, click the selection highlight or a row control on the right.

## Reporting on file attachment fields

You can choose to filter on records that contain file attachments that contain certain words or phrases. See [Search for or within a Document](https://helpv2.quickbase.com/hc/en-us/articles/4570137919124-Search-for-or-within-File-Attachments-) for information on how to build search criteria for file attachments.

## Filtering example

Imagine that you have a project management application, and are creating a Table report to display only the tasks assigned to Colleen Garton.

1.  Select Filter tasks.
    
2.  From the list of fields in the dropdown that appears, select the field containing the value you want to filter on. In this example, you'd select **Assigned To**.
    
3.  From the list of operators in the second column, select the operator that qualifies the value you're about to specify. In this case, select **is**.
    
4.  In the third column, specify the resource whose tasks you want to display.
    
    Note: For some types of fields, the third column displays as a dropdown. Select an item from the list, or, if you want to enter text or [set OR criteria](https://helpv2.quickbase.com/hc/en-us/articles/4570401617940-Search-for-Records-that-Match-Either-A-or-B-), select **<other...>** and then enter text in the box that appears.
    
5.  Click Display in the Page bar to show the new report.
    

### Related topics:

-   [Building queries using the Report Builder](https://helpv2.quickbase.com/hc/en-us/articles/4570253942036-Building-Queries-)
    
-   [Includes and Does not include](https://helpv2.quickbase.com/hc/en-us/articles/4570261800084-Filtering-records-using-fields-with-multiple-values-)
    
-   [Understanding relative date ranges](https://helpv2.quickbase.com/hc/en-us/articles/4570263936660-Understanding-Relative-Date-Ranges-)
    
-   [Sorting/Grouping](https://helpv2.quickbase.com/hc/en-us/articles/4570409135252-Sorting-Grouping-)
    
-   [Columns to display](https://helpv2.quickbase.com/hc/en-us/articles/4570310548628-Columns-to-Display-)
    
-   [About Row Colorization (Highlighting)](https://helpv2.quickbase.com/hc/en-us/articles/4570391002260-Color-coding-in-reports-)