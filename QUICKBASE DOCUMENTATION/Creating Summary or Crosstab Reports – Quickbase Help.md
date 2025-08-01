## Creating Summary or Crosstab Reports

Summary reports help you group and total records so you can see patterns and get answers to questions. [Read more](https://helpv2.quickbase.com/hc/en-us/articles/4570366660372-About-Summary-and-Crosstab-Reports-).

To create a summary report:

1.  Choose a table from the sidebar.
    
2.  Select **Reports** to open the reports panel, then click **\+ New Report**.
    
3.  In the dialog, select Summary and click **Create**.
    
4.  Select the values you want to show in your summary report.
    
    Within the **Summarize Data** section, select the fields whose values will make up your report. These fields will appear as columns in your summary report. For each field you choose to show, set summary and display options.
    
    ![Screenshot 2024-09-30 at 9.52.11 AM.png](https://helpv2.quickbase.com/hc/article_attachments/30864993885972)
    
    Note: Summary reports are limited to 25 or fewer columns.
    
5.  For each field you selected within Summarize Data, tell Quickbase what kind of calculation you want the program to perform on these values:
    
    From the **Summarize by** dropdown select one of the following:
    
    -   **Totals.** Sums the values that comprise the set.
        
    -   **Averages.** Returns the value that marks the middle of the set—the mathematical mean. ([Read more at Wikipedia](http://en.wikipedia.org/wiki/Mean).)
        
    -   **Maximums.** Returns the highest value within each set.
        
    -   **Minimums.** Returns the lowest value within each set.
        
    -   **Std. Deviation.** Tells you how spread out values in the set are from the average or mean. ([Read more at Wikipedia](http://en.wikipedia.org/wiki/Standard_deviation).)
        
    -   **Distinct count.** Provides a count of all the unique values in a field. For example, you could show how many different products were ordered in a given month. The distinct count summary field supports all field types except the following: File Attachment, Predecessor, iCalendar, vCard, Report Link, List User, and Multi-select Text.
        
    
    Note: Each value that displays within a summary report is a calculated value. In other words, it represents multiple records grouped by row (unless there's just one in a set for some reason).
    
6.  If you want, have your data summarize figures in a different way.
    
    You may care more about comparing data than totaling values. For example, when deciding on bonuses you don't necessarily want to know how many deals a sales rep closed. Instead you'd like to see what percentage of your business that person brings in. To get numbers like this, you can have Quickbase show percentage values rather than regular numbers.
    
    For each field you chose in Step 3, click the **Display As** dropdown and select one of the following values:
    
    -   **Normal Value.** This setting is no different from the report you'd get if you make no selection in this dropdown.
        
    -   **Percent of column total.** This option shows each value as a percentage of the column. In other words, Quickbase totals values by column and calculates the percent each value contributes the whole at the bottom of the column.
        
    -   **Percent of crosstab column.** Choose this if you want to know what percentage of each **_row_** the value represents. In other words, Quickbase totals figures by row and calculates the percentage each value contributes to the whole, which is totaled on the right. _(You can only select this option after you turn on crosstabs. See Step 8.)_
        
    -   **Running total down column.** Running totals option tallies values as they pile up down the column, so that each value is a compilation of all values so far.
        
    -   **Running total across crosstab.** This "running totals" option works the same way as the running totals by column works, but this setting does its cumulative addition _**across each row**_ instead of down columns. _(You can only select this option after you turn on crosstabs. See Step 8.)_
        
    
    Tip: If you want to define advanced matching criteria options that aren't possible using the basic settings in the Report Builder's **Filters** section (like setting OR matching criteria across fields), you can set up a custom formula column to return only the records you want to summarize. To do so, turn on the **Define a calculated column** checkbox in the Summarize Data section, then create the custom column. [Read how](https://helpv2.quickbase.com/hc/en-us/articles/4570272620052-Using-a-report-formula-).
    
7.  Select your row groupings.
    
    How do you want to break down your numbers? In a summary report, each row is really a group of records. Choose the field you want to group by from the **Grouping and crosstabs** section. When you do, each value in that field displays as a row in your report.
    
8.  Organize your row groupings.
    
    In the dropdown to the right of each selection you made in the preceding step, tell Quickbase how to organize your row groups, by making a selection in the corresponding **Group by** dropdown. Selections here depend upon what field you chose to group by. For instance, if you chose a date field, Quickbase lets you group records by day, week, month, year, quarter or decade. Fields that contain text content, like names, can be grouped alphabetically or by **Equal Values**, meaning that Quickbase will create a single row for each unique entry.
    
9.  If you want, group columns by a specific field (in other words, add cross tabulation, or **_crosstabs_**).
    
    If you want to include information from additional fields, enhance your view with crosstabs. Crosstabs are just groups of columns gathered under a field value. To do so, go to the **Grouping and crosstabs** section and select the **Group columns** radio button. Click the **Group by** dropdown and select the field you want to group columns by. Then tell Quickbase how to break down values in this field, by making a selection in the **Combine** dropdown. Again, selections here depend upon what field you chose to group by. For instance, if you chose a date field, Quickbase lets you group records by day, week, month, year, quarter or decade.
    
    As discussed in Step 6, if you try to group rows by a secondary field, you lose calculations on your highest level group. You can fix this with crosstabs. Instead of using that secondary field to group rows, use it to group columns by creating crosstabs. Not only will you gain calculations grouped by that field, you'll also retain calculations on your original row groupings.
    
    Tip: Each cell in a crosstab report represents records that meet a combination of two variables. For example, **$214,000** is the total deal size of all opportunities that meet both the following criteria: _Sales Rep_ is _Chris Baker_ and _Opportunity Status_ is _Active Opportunity_. That number is a cross tabulation.
    
10.  If you're not using crosstabs, you can set a custom sort order.
    
    The report is automatically sorted according to the selections you made in Step 5. If you want change the field the report sorts on, you can. However, your additional choices are limited to selections you made in the **Summarize Data** section. To change the sort order from within the **Sorting** section, click **Custom order**. Then use the dropdowns to choose a field to sort by, and tell Quickbase how to sort it.
    
11.  Tell Quickbase what records you want to see.
    
    You don't always want to see all the records in the table. You can tell Quickbase to only show you certain ones by setting specific criteria within the **Filters** section. [Read how](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records-).
    
12.  Decide whether to show or hide the totals row on the report.
    
    If you decide to hide the totals row, turn on the **Hide totals row** checkbox.
    
13.  Set advanced report options with formulas. Select **Add a report formula** In the **Report formulas** section. ([Learn more](https://helpv2.quickbase.com/hc/en-us/articles/4570376002580-Using-Formulas-in-Quickbase-) about using formulas.)
    
14.  You can select **Display** to get a preview of your report.
    
    After displaying the report, if you want to make more changes, click the **More customization options** icon at the top of the page to return to the report builder.
    
    ![More customization options icon](https://helpv2.quickbase.com/hc/article_attachments/28605503581204)
    
15.  Once you’re finished customizing, you can save the report. Depending on your role in the app, you can specify who else can see and use the report.
    
    **About saving reports**
    
    You can save reports for others to see in the **Reports & Charts** area for a table if the manager of the app has granted you permission to do so.
    
    When you save this type of shared or common report, so that others can see it, you have several choices:
    
    -   **Everyone**. Everybody can see the report in the panel.
        
    -   **Users in my role**. Users who have my role can see the report in the panel.
        
    -   **Users in specific roles**. Users in any of the chosen roles can see the report in the panel.
        
    -   **No one; hide it.** The report doesn't appear in the panel until you say otherwise. To see the report, create a bookmark in your browser.
        
    
    If your report is personal, choose **Only me**. Only you can see the report in the panel. You can't ever list it for other users. You can still let others open it by sending them links
    
    An app manager can also specify which reports a particular role can see at any time. To learn how, see ![](https://helpv2.quickbase.com/hc/article_attachments/28605512368148 "This functionality  is not available to accounts on the Quickbase Essential plan.")[Specifying which reports a user can see](https://helpv2.quickbase.com/hc/en-us/articles/4570384081556-Specifying-which-reports-a-user-can-see-).
    

## Specifying a drilldown report

When you click a link in a summary report, Quickbase uses the default report to show those details by default. You can also specify which report to display when you click a link.

To specify a drilldown report:

1.  [Edit the report](https://helpv2.quickbase.com/hc/en-us/articles/4570281029396-Edit-a-Report-#vb).
    
2.  Scroll to the **Drilldown Report** section near the bottom of the page.
    
3.  Choose an option from the **Drilldown behavior** dropdown:
    
    -   **Default report** – Use the default report to show details. This option is chosen by default for all new summary and chart reports.
        
    -   **None** – This option will disable clicking through to show details.
        
    -   a report name – Use the specified report to show details. On drilldown, this report is further filtered to show only records included in the summary group you clicked.
        
4.  Save your changes by clicking **Save** in the page bar.
    

### Specifying a drilldown report for a summary field

When you create a summary field, you can specify the report to be displayed when a user clicks the summary field. To do this, open the Summary field properties page and, under **Summary field options**, choose the drilldown behavior.

### Related topics:

-   [Organizing reports](https://helpv2.quickbase.com/hc/en-us/articles/4570407864980-Organizing-reports-)