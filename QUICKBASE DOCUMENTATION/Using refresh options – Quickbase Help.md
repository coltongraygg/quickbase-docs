Refresh options determine how and when data in this [connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-) refreshes. We use the [Refresh Key field](https://helpv2.quickbase.com/hc/en-us/articles/4570314286100-Using-refresh-options#Refresh_ID_field), [Table updates](https://helpv2.quickbase.com/hc/en-us/articles/4570314286100-Using-refresh-options#Table_updates), and [schedule](https://helpv2.quickbase.com/hc/en-us/articles/4570314286100-Using-refresh-options#schedule) to refresh your data.

Note: Before you change the refresh options, make sure you understand the purpose of this connected table. For example, if this connected table serves as an archive of all orders, you may not want to change the [Table updates](https://helpv2.quickbase.com/hc/en-us/articles/4570314286100-Using-refresh-options#Table_updates) settings because that might result in records being removed from the table.

## Refresh Key field

The [Refresh Key](https://helpv2.quickbase.com/hc/en-us/articles/4570260038804-About-the-Refresh-Key-field-) is the field in the external app, service, or CSV file that makes each record you are connecting unique. It must be a **connected field with unique values for each record and can't be blank**. Quickbase uses the Refresh Key to tell one record from another when refreshing data from a connected source.

Every connected table has a Refresh Key field. Ordinary tables do not have one.

Either the connection owner selects the Refresh Key or we select it automatically when the table is created. When you create a connected table, we set the [key field](https://helpv2.quickbase.com/hc/en-us/articles/4570321550612-Setting-key-fields-for-tables-) as the [Refresh Key](https://helpv2.quickbase.com/hc/en-us/articles/4570260038804-About-the-Refresh-Key-field-).

_We recommend that you do not move the key from the Refresh Key field, unless you have a specific reason_. Data refresh and table-to-table relationships can get complicated if the Refresh Key and key are not assigned to the same field.

The Refresh Key is editable only if:

-   the Refresh Key was not set automatically
-   the table is connected using one of _your_ own connections

Rarely, the connection owner might need to change Refresh Key; for example if the current Refresh Key is no longer unique. Change the Refresh Key _only if absolutely necessary_; a different Refresh Key may result in different data displaying in the table. When you change a refresh key,

If you are syncing to a CSV file, you typically select a single field as the Refresh Key, but if necessary, you can combine up to three additional fields to create a unique Refresh Key.

## Table updates

Table updates tell us what to do with records that are in your Quickbase table now, but have been deleted from the connected app, service, or CSV file.

Choose an option:

-   **Make my table match \[data source\]**. We'll remove any records from your table that are not in the data source any more, so that the connected table matches the source exactly.
    
-   **Keep everything in my table and add new records**. We'll keep all the records in your table, even if they aren't in the data source any more. You can delete records from the table when you no longer need them. This is good choice if your table serves as an archive of all records.
    

If you are using a CSV data source, the following also applies:

-   If Make my table match is selected, only the newest CSV file in the folder is used when the table refreshes. The file is not moved when the refresh finishes.
-   If Keep everything is selected, the table refresh will process multiple CSV files in the folder, starting from oldest to newest. After a file is processed, it is moved to a Done subfolder within the folder.

Before you change a connected table's historic data settings, make sure you understand the purpose and use of the table.

For example, if a connected table with a CSV data source is set to **Keep everything** and the table serves as an archive of all records, if you change to **Make my table match the latest CSV file**, when the tables refreshes, records will be removed and replaced with only the records currently in the connected service.

## Automatic refresh schedule

You can automatically refresh your connected table on a monthly, weekly, daily, or hourly basis. The scheduled time is based on the **app's timezone settings**, which are set in App properties.

If there's a problem refreshing your connected table, the app manager and the connection owner will receive an **email**. You can opt out of this email notification by clearing the **Email me if there’s a problem refreshing my table** checkbox.

To stop a connected table from refreshing according to a schedule, select **Manual only**. To refresh your connected table at any time, open the connected table and click **Refresh data**![](https://helpv2.quickbase.com/hc/article_attachments/17374674564116).

Note: In all cases, regardless of whether you receive email notifications of unsuccessful scheduled refreshes, if refresh attempts continue unsuccessfully, we’ll send an email alert and change the refresh schedule for that table to manual. You can view the table [History](https://helpv2.quickbase.com/hc/en-us/articles/4570281951252-Viewing-connected-table-details-#History) for details and access troubleshooting tips that may help you resolve the problem. After you resolve the problem, you can reset the refresh schedule to automatic.