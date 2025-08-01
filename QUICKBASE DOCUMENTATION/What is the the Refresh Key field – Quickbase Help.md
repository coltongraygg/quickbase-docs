## What is the the Refresh Key field?

The Refresh Key is the field in the external app, service, or CSV file that makes each record that you are connecting unique. Quickbase uses the Refresh Key, along with the [refresh options](https://helpv2.quickbase.com/hc/en-us/articles/4570314286100-About-refresh-options-) you select, to refresh data in your connected table.

Every connected table has a Refresh Key field. Ordinary tables do not have one.

## What are multiple-field refresh keys?

If you are syncing to a CSV file, you typically select a single field as the Refresh Key, but if necessary, you can combine up to three additional fields to create a unique Refresh Key.

## How is the Refresh Key set?

Either the connection owner selects the Refresh Key or we select it automatically when the table is created. The Refresh Key must be a connected field with unique values and no blanks.

If we know a specific field ensures that each record is unique, for example, the Salesforce ID, we'll automatically select that field as the Refresh Key.

For some data sources, such as CSV, the connection owner needs to select a field with unique values and no blanks as the Refresh Key.

## Is the Refresh Key the same thing as a Key?

No, these settings have separate purposes. All Quickbase tables have a [key field](https://helpv2.quickbase.com/hc/en-us/articles/4570321550612-Setting-key-fields-for-tables-), which lets Quickbase tell one record from another. The key must be a field with unique values and no blanks.

In contrast, only [connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-) have a _Refresh Key_ field, which lets Quickbase tell one record from another _specifically when refreshing data from a connected source_. The Refresh Key must be a connected field with unique values and no blanks.

###### Is the same field used as both the Refresh Key and key?

Usually. When you create a connected table, we set both of these to the same field. We recommend leaving them alone, unless you have a specific reason to change them. Data refresh and table-to-table relationships can get complicated if they're not assigned to the same field.

You can [change the key field](https://helpv2.quickbase.com/hc/en-us/articles/4570321550612-Setting-key-fields-for-tables-) in the usual way, if needed; for example, your connected table might be the "parent" in a relationship that requires text instead of numbers as the key. Make sure the table still has a _unique Refresh Key_; we'll need it to refresh your data.

You can change the Refresh Key field in the [Connection Details](https://helpv2.quickbase.com/hc/en-us/articles/4570281951252-Viewing-connected-table-details-) page in table settings, in some cases, if necessary; for example if the current Refresh Key is no longer unique. The Refresh Key is editable only if:

-   the Refresh Key was not set automatically
-   the table is connected using one of your own connections

Change the Refresh Key _only if absolutely necessary_; a different Refresh Key may result in different data displaying in the table.

Learn more about [refresh options](https://helpv2.quickbase.com/hc/en-us/articles/4570314286100-About-refresh-options-) and [refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-).