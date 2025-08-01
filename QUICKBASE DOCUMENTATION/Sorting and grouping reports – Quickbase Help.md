## Sorting and grouping reports

Table and Summary reports display a list of records. But which record should come first? Which ones go together?

Using the Report Builder, you specify custom sorting and grouping for your reports. Custom sorting lets you specify which records should appear first, and how all records should be ordered. Grouping lets you group "like" records together; you tell Quickbase how to group records in your report.

Note: If you don't choose custom sorting, Quickbase automatically sorts records using the default sort order specified in the [default report settings](https://helpv2.quickbase.com/hc/en-us/articles/4570348881300-Setting-reporting-defaults-). The field chosen is decorated with a green double-arrow icon (![](https://helpv2.quickbase.com/hc/article_attachments/4572849605652/defsorticon.png)) in the Fields list.

In this topic:

-   [Choosing a custom sort order](https://helpv2.quickbase.com/hc/en-us/articles/4570409135252-Sorting-and-grouping-reports#Choosing_a_custom_sort_order)
    
-   [Choosing custom sorting and grouping](https://helpv2.quickbase.com/hc/en-us/articles/4570409135252-Sorting-and-grouping-reports#Choosing_custom_sorting_and_grouping)
    
-   [Setting up sub-sorting](https://helpv2.quickbase.com/hc/en-us/articles/4570409135252-Sorting-and-grouping-reports#Setting_up_sub-sorting)
    
-   [Sorting and grouping example](https://helpv2.quickbase.com/hc/en-us/articles/4570409135252-Sorting-and-grouping-reports#Sorting_and_grouping_example)
    

## Choosing a custom sort order

When sorting, you can choose either of these options:

-   **Sort from low to high by** – Quickbase puts the lowest values from the field you're about to choose at the top of your list. For dates, Quickbase orders from earliest to latest. Text fields are sorted in alphabetical order.
    
-   **Sort from high to low by** – Quickbase puts the highest values from the field you're about to choose at the top of your list. For dates, Quickbase orders from latest to earliest. Text fields are sorted in reverse alphabetical order.
    

To specify sorting:

1.  In the Sorting & Grouping section of the Report Builder screen, choose Sort or group on other columns.
    
2.  Start typing the field name or field type to see a filtered list of fields. For example, if you want to sort by "Start Date," typing in "Date" will show you all field names or types with the word "Date." Select a sort order from the dropdown. If you want to group as well, see the next section for sorting and grouping options.
    
3.  Choose a field to sort by.
    
4.  Click **Save** on the Page bar to save your changes.
    

## Choosing custom sorting and grouping

If you choose both sorting and grouping, you specify a field that will be used to sort AND group records.

When you specify a field, Quickbase displays another dropdown letting you indicate the increment by which you want to group. The choices you see here depend upon the field type of your grouping field.

For all field types, you can choose Equal Values. Grouping by Equal Values creates a separate line for each unique entry.

The most common grouping methods appear below:

| field types | grouping options |
| --- | --- |
| 
Text

 | 

-   First Word
    
-   First Letter
    
-   Equal Values
    

 |
| 

Numeric

 | 

-   Numeric increments, from .001 to 1,000,000
    
-   Equal Values
    

 |
| 

Date

 | 

-   Day
    
-   Week
    
-   Month
    
-   Quarter
    
-   Fiscal Quarter
    
-   Year
    
-   Fiscal Year
    
-   Decade
    
-   Equal Values
    

 |
| 

User

 | 

-   First Letter
    
-   Equal Values
    

 |
| 

Duration

 | 

-   Second
    
-   Minute
    
-   Hour
    
-   Day
    
-   Week
    
-   Equal Values
    

 |

To specify sorting and grouping:

1.  In the Sorting & Grouping section of the Report Builder screen, choose Sort or group on other columns.
    
2.  In the type-ahead dropdown list, enter the field name or field type and select one of the sort and group fields from the dropdown.
    
3.  Choose a field to sort and group on.
    
4.  Choose how you'd like to group the field's values.
    
5.  Click **Save** on the Page bar to save your changes.
    

## Setting up sub-sorting

You may want to specify another level of sorting as well. For example, say you're sorting a list of contacts by last name, but you have 42 Joneses on it. You'll probably want to sort by first name as well. It's easy to do.

Click the ![](https://helpv2.quickbase.com/hc/article_attachments/4572793303316/plusicon.png) icon that appears when you hover your mouse over the field you've already selected in the Sorting & Grouping section to set the secondary order. If you want, keep going. Quickbase lets you set up to six sort orders. Each sort is nested within the sort above it.

## Sorting and grouping example

If you want to further sort your records within each group, you can add additional rows using the icons that appear when you hover your mouse over the current line. Use the ![](https://helpv2.quickbase.com/hc/article_attachments/4572793303316/plusicon.png) icon to add a row after the current line.

For example, say that within each week you want to further sort records by who's in the Assigned To field. The resulting report categorizes your data by week, and then sorts the data by staff member.

Your settings should look similar to the following:

![](https://helpv2.quickbase.com/hc/article_attachments/4572871471380/sort_grp_set2.png)

The resulting report should look similar to the following:

![](https://helpv2.quickbase.com/hc/article_attachments/4572899294612/groupex2.png)

### Related topics:

-   [To specify sorting for a chart report:](https://helpv2.quickbase.com/hc/en-us/articles/4570315165972-Sorting-Chart-Data-)
    
-   [Filter Records](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records-)
    
-   [Understanding Relative Date Ranges](https://helpv2.quickbase.com/hc/en-us/articles/4570263936660-Understanding-Relative-Date-Ranges-)
    
-   [Columns to Display](https://helpv2.quickbase.com/hc/en-us/articles/4570310548628-Columns-to-Display-)
    
-   [About Row Colorization](https://helpv2.quickbase.com/hc/en-us/articles/4570391002260-Color-coding-in-reports-)