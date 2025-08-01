## Create chart reports

The process of getting your data into a chart varies, depending upon how you've structured your Quickbase and what kind of chart you want to make.

To create a chart report:

1.  In the sidebar, choose a table.
    
2.  Click **Reports** to open the reports panel, then click **+ New** **report** in the reports panel.
    
3.  In the dialog, select Chart and click **Create**.
    
4.  Select a chart type.
    
    Within the **Chart Details** section, click the dropdown to select a type of chart. Quickbase offers a variety of chart types, each of which is designed to convey a specific type of information. For help choosing one, [read about chart types](https://helpv2.quickbase.com/hc/en-us/articles/4570361263636-Select-a-Chart-Type-).
    
5.  Tell Quickbase what records to include.
    
    If you want your chart to show only a certain kind of record or only records that meet specific conditions, you can tell Quickbase so in the report Builder's **Filters** section. For example, maybe you only want to show sales figures for a specific period of time, like the last quarter. Or maybe you'd only like to see sales of "widgets" and not your other products. To make choices like this, go to the **Filters** section and select the Filter records radio button. Then make the selections you want. ([Read how](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records-).)
    
6.  Fill the chart with data.
    
    Quickbase needs to know what information you want the chart to show. The program offers different options depending on what chart type you chose. Read how to:
    
    -   [How to get data into a pie chart](https://helpv2.quickbase.com/hc/en-us/articles/4570305029140-Get-Data-into-a-Pie-Chart-).
        
    -   [How to get data into bar, line, and area charts](https://helpv2.quickbase.com/hc/en-us/articles/4570300330644-Get-Data-into-Bar-Line-and-Area-Charts-).
        
7.  Set data labels.
    
    The graphic nature of charts really helps viewers understand your data. But additional text never hurts. Use the Chart Details section to let people know the actual numbers and values that a bar or pie wedge represents. To add helpful text to your chart, turn on the **Data labels always visible** checkbox. Quickbase displays a dropdown you can use to select a labeling mode:
    
    -   **Value.** If you want to show the actual value (reflected in the y-axis) for an item, choose this option. For example, perhaps there were 3 banjos sold in March.
        
    -   **Percent of Series.** Shows what portion each bar or point on a line contributes to the total. If you have a bar chart and it's broken into a series, the percentage shows what portion each bar contributes to the total of like items (all bars that are the same color).
        
    -   **Percent.** Pie and funnel charts let you show what percent of the whole each wedge represents.
        
    -   **Value and Name.** Pie and funnel charts let you show the value (the actual number) along with the name of the item (like **Banjos**, for instance.)
        
    -   **Percent and Name.** Pie and funnel charts let you label each wedge and show what percent of the whole each represents.
        
    
    **Note:** This control does not appear on gauge charts.
    
    Tip: If you're a Quickbase formula maven, you can create a special formula field for the chart report. This formula could use other fields to calculate a special value in your chart, or help you set matching criteria. To add a formula field, go to the **Options** section and select Define a calculated column. ([Read more about using formulas in a report](https://helpv2.quickbase.com/hc/en-us/articles/4570272620052-Using-a-report-formula-).)
    
8.  You can select **Display** to get a preview of your chart report.
    
    After displaying the report, if you want to make more changes, click the **More customization options** icon at the top of the page to return to the report builder.
    
    Note: When the chart displays, no report name is shown. Don't worry about that right now. Later, when you save the report, you'll name it.
    
9.  Once you’re finished customizing, you can save the chart report. Depending on your role in the app, you can specify who else can see and use the chart.
    
    **About saving reports**
    
    You can save reports for others to see in the **Reports & Charts** area for a table if the manager of the app has granted you permission to do so.
    
    When you save this type of shared or common report, so that others can see it, you have several choices:
    
    -   **Everyone**. Everybody can see the report in the panel.
        
    -   **Users in my role**. Users who have my role can see the report in the panel.
        
    -   **Users in specific roles**. Users in any of the chosen roles can see the report in the panel.
        
    -   **No one; hide it.** The report doesn't appear in the panel until you say otherwise. To see the report, create a bookmark in your browser.
        
    
    If your report is personal, choose **Only me**. Only you can see the report in the panel. You can't ever list it for other users. You can still let others open it by sending them links
    
    An app manager can also specify which reports a particular role can see at any time. To learn how, see ![](https://helpv2.quickbase.com/hc/article_attachments/28605212728468 "This functionality  is not available to accounts on the Quickbase Essential plan.")[Specifying which reports a user can see](https://helpv2.quickbase.com/hc/en-us/articles/4570384081556-Specifying-which-reports-a-user-can-see-).
    

## Specifying a drilldown report

When you click a segment of a chart, Quickbase uses the default report to show those details by default. You can also specify which report to display.

To specify a drilldown report:

1.  [Edit the report](https://helpv2.quickbase.com/hc/en-us/articles/4570281029396-Edit-a-Report-#vb).
    
2.  Scroll to the **Drilldown Report** section near the bottom of the page.
    
3.  Choose an option from the **Drilldown behavior** dropdown:
    
    -   **Default report** – Use the default report to show details. This option is chosen by default for all new summary and chart reports.
        
    -   **None** – This option will disable clicking through to show details.
        
    -   a report name – Use the specified report to show details. On drilldown, this report is further filtered to show only records included in the chart segment you clicked.
        
4.  Save your changes by clicking **Save** in the page bar.
    

### Related topics:

-   [Viewing and displaying charts](https://helpv2.quickbase.com/hc/en-us/articles/4570380581524-View-and-Display-Charts-)
    
-   [Selecting a chart type](https://helpv2.quickbase.com/hc/en-us/articles/4570361263636-Select-a-Chart-Type-)
    
-   [Get data into a pie chart](https://helpv2.quickbase.com/hc/en-us/articles/4570305029140-Get-Data-into-a-Pie-Chart-)
    
-   [Get data into all other types of charts](https://helpv2.quickbase.com/hc/en-us/articles/4570300330644-Get-Data-into-Bar-Line-and-Area-Charts-)
    
-   [Using the legend's color chooser](https://helpv2.quickbase.com/hc/en-us/articles/4570385472788-Choosing-colors-for-a-chart-)
    
-   [Data structure and charting](https://helpv2.quickbase.com/hc/en-us/articles/4570382065428-Data-Structure-and-Charting-)
    
-   [What's a logarithmic chart?](https://helpv2.quickbase.com/hc/en-us/articles/4570136865044-Logarithmic-Chart-)
    
-   [Organizing reports](https://helpv2.quickbase.com/hc/en-us/articles/4570407864980-Organizing-reports-)