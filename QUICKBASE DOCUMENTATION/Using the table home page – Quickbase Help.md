## Using the table home page

You can use the table home page to view the table (the [default report](https://helpv2.quickbase.com/hc/en-us/articles/4570405363348-Customizing-a-Table-Home-Page-#mod_table_home), a specific report, or the advanced search form).

From this page, you can:

-   **Use dynamic filters to show fewer records.** If your table is large enough that you'd like to show a subset of your data, or you're looking for something specific, the table home page offers two ways to show a smaller set of records: the list of [dynamic filters](https://helpv2.quickbase.com/hc/en-us/articles/4570309574420-Using-the-table-home-page#Filters) on the left side of the page, and the **Search** box above the report.
    
    Note: The filters are shown when the table Home page is set to display a report or the default report. If you do not see filters, there may be no filterable fields for that table, or your role may prevent you from seeing the fields used as filters.
    
-   **Create a new report.** If you've filtered the table, you can click the **Save** button that appears on the Page bar to save your changes as a report.
    
-   **Email the list.** Click **Email** on the Page bar to email the list of records shown on the table Home page. Note that this action will only email up to 1000 records.
    
-   **Print the list.** Click **More > Print** on the Page bar to print the list of records shown on the table Home page.
    
-   **Update your data.**[Add](https://helpv2.quickbase.com/hc/en-us/articles/4570336827668-Add-or-Edit-a-Record-) a record, or [modify](https://helpv2.quickbase.com/hc/en-us/articles/4570336827668-Add-or-Edit-a-Record-#edit) an existing record.
    
-   **Refresh connected data**. Click ![](https://helpv2.quickbase.com/hc/article_attachments/20942043748244) to refresh [connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-) with the most recent data from the connected data source.
    
-   **Show a list of reports.** To access a list of reports for the table, click **Reports & charts** to open the [reports panel](https://helpv2.quickbase.com/hc/en-us/articles/4570387181588-About-the-Reports-Charts-panel-).
    
-   **Import or export data.** The **More** menu has several options to import or export data from your table. Use **More > Save as a spreadsheet** to save just the records shown on the table Home page, or for more power and flexibility, try **More > Import/Export**. ([Read more about importing from Excel](https://helpv2.quickbase.com/hc/en-us/articles/4570323207188-Importing-Microsoft-Excel-data-).)
    
-   **Hide or add columns.** You can hide or add columns to customize the data you see on the default report. Click the column and choose to hide it, or click the column next to where you'd like to see an additional column, **Note:** These columns changes are temporary; the report appears with its defined columns next time you load the page.
    

If you have permission to alter table settings, you will see other commands that you can use to:

-   **Go to table settings.** Click the **Settings** link under the table name to access the table settings page.
    
-   **Customize the page.** Click **Customize this Page** to choose what to display on the table Home page (the default report, a specific report, or the advanced search form), and define different views for each role in your app. ([Read more about customizing the home page](https://helpv2.quickbase.com/hc/en-us/articles/4570405363348-Customizing-a-Table-Home-Page-).)
    

## Filtering data

If the report that appears on the table Home page is set to display dynamic filters, you now have a great way to quickly find the data you need. These filters appear on the left side of the table Home page. The filterable values for a field appear indented beneath the field name. If a field has many values and you're not interested in filtering on it, you can collapse it by clicking the arrow to the left of the field name. You can also resize or close the filter list. [Read more about dynamic filters](https://helpv2.quickbase.com/hc/en-us/articles/4570135862420-About-Dynamic-Filters-).

To use dynamic filters:

-   Click a field value to limit the list shown to records containing that value. You can tell when a filter is in effect, because the value is highlighted in the list of filters, and the filtered value is shown at the top of the list, next to the **Search** box.
    
-   Click multiple values for a single field to show _all_ records with _any_ of those values.
    
-   Click a value in each of two fields to show _only_ records with _both_ values.
    
-   Click a highlighted field value to remove that filter. You can also remove it by clicking the **x** icon next to the filter shown beside the **Search these _records_** box.
    

Note: Your role affects the field values shown in the filter list (for example, if you aren't allowed access to a filterable field, it won't display in the list).

If you'd rather type your search term, the **Search these _records_** box will search fields on the report that are marked searchable, but not all the fields. To learn more, see [configured to be Searchable](https://helpv2.quickbase.com/hc/en-us/articles/4570284211860-Excluding-fields-from-searches-).

### Technical notes on filtering:

-   If a field has a value longer than 512 characters, dynamic filters for that field will be disabled.
    
-   If a field has over 200 values, it will display with a message that there are too many values to use for filtering. If all the filterable fields have too many values to display, you are directed to a search page so you can search for and display a subset of your data.
    
-   If a field has 60-200 values, some values will display, and the last item in the list will be an **All Choices** link, which opens a dialog with all the choices available for that field.
    
-   To refresh the filter list, click the table name in the sidebar. The filters and values in the filter list are not updated as you modify your data, for example, if you add a new choice to a multiple-choice field. Reloading the page using the browser controls will also not update the filter list.
    

### Related topics:

-   [Customizing a table Home page](https://helpv2.quickbase.com/hc/en-us/articles/4570405363348-Customizing-a-Table-Home-Page-)
    
-   [Setting reporting defaults](https://helpv2.quickbase.com/hc/en-us/articles/4570348881300-Setting-reporting-defaults-)
    
-   [About dynamic filters](https://helpv2.quickbase.com/hc/en-us/articles/4570135862420-About-Dynamic-Filters-)