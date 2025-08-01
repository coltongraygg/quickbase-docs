## Filtering data to connect in a connected table

This topic describes how to filter the data you want to connect using a connected table. After you create your [connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-), you can set [filters](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records-) on the connected table to view an even more refined subset of your data. Only the connection owner can create or edit a filter on a connected table.

## Filtering the data to connect

You can set a filter to limit the data that you connect from an external service, such as QuickBooks Online or Salesforce.com. Setting a filter helps restrict connected records to the ones you really care about; for example, invoices from this year, rather than all invoices.

The filter criteria that you set determines the values that the data must match in order to appear in the set of records returned; for example, only records with an Active status.

You can filter on any of the fields in your source data - not just the fields that you selected to connect. This helps you refine your connected data, without bringing unnecessary fields into your connected table.

You can set or change a filter on a connected table any time.

To create or edit a filter on a connected table

1.  Open your connected table and select **Settings**.
    
2.  Click the **Connection**, for example, _QuickBooks connection_.
    
3.  On the **Details** tab, click the **edit** link next to **Filter**.
    
4.  [Define the filter](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table#Define_a_filter) and then click **Done**.
    
5.  Click **Yes** to refresh your data. Your changes won’t take effect until the data is refreshed. You can refresh your data any time by clicking ![](https://helpv2.quickbase.com/hc/article_attachments/4572811842196/refresh_data.png)**Refresh data**.
    

## Filtering to view a subset of connected data

## Defining a filter

A filter tells Quickbase to connect only those records that match the criteria you set. To set filter criteria, specify the following:

-   The field you want to filter on. If you want to see all tasks with a particular start date, you'd choose Start as your filtering field.
    
-   An operator. Operators vary according to the field type. The operator tells Quickbase how to filter the records. Example operators are: equals, is greater than, is greater than or equal to, and so forth.
    
-   A matching value or a value in another field**.** Depending on the type of field you're filtering on and what operator you chose, you may have to type in a value or choose one from a list.
    

For instance, if you want to see all tasks that are in progress, you'd choose the following:

<table><tbody><tr><td><p>Field</p></td><td><p>Operator</p></td><td><p>Matching value</p></td></tr><tr><td><p>Status</p></td><td><p>is</p></td><td><p>In progress</p></td></tr></tbody></table>

You can set a single line of criteria, or add more fields if you'd like. Hover your mouse over the field dropdown. Plus and minus sign icons appear to the right of the field.

Click the plus sign (![](https://helpv2.quickbase.com/hc/article_attachments/4572793303316/plusicon.png)) icon to add another line of filter criteria. Use the minus sign (![](https://helpv2.quickbase.com/hc/article_attachments/4572793320468/minusicon.png))  icon to delete the current line.

## Comparing a field to a specific value

To create a filter that finds a specific matching value, enter or select a value in the field that appears when you choose one of the following operators:

<table><tbody><tr><td><p>Field type</p></td><td><p>Operators</p></td></tr><tr><td><p>Text</p></td><td><ul><li>contains<strong>*</strong></li><li>does not contain<strong>*</strong></li><li>is — if this is empty, the field is empty or null</li><li>is not — if this is empty, the field is not empty or not null</li><li>starts with<strong>*</strong></li><li>does not start with<strong>*</strong></li><li>comes before</li><li>comes before or same as</li><li>comes after</li><li>comes after or same as</li></ul><p><strong>* Notes</strong></p><p>contains, does not contain, starts with, and does not start with operators are case-insensitive. All other text operators are case-sensitive.</p><p>When you connect to Exchange or Gmail, some operators only support complete matches, not partial matches. For example, the filter "Subject contains Project" would return messages with "Project" but no variations such as "Projects" or "Projections."</p><p>For Exchange, these operators filter on complete words:</p><ul><li>contains, starts with</li></ul><p>For Gmail, these operators filter on complete words:</p><ul><li>contains, does not contain, starts with, does not start with</li></ul></td></tr><tr><td><p>Numeric</p></td><td><ul><li>equals</li><li>does not equal</li><li>is less than</li><li>is less than or equal to</li><li>is greater than</li><li>is greater than or equal to</li></ul></td></tr><tr><td><p>Date</p></td><td><ul><li>equals</li><li>does not equal</li><li>is before</li><li>is on or before</li><li>is after</li><li>is on or after</li></ul><p>Enter a specific date or choose a relative value (yesterday, today, tomorrow, one week from today, the first day of the previous month, and so forth).</p><ul><li>is during</li><li>is not during</li></ul><p>Choose a relative date range (previous, current, next) for day, month, quarter, or year.</p></td></tr><tr><td><p>Date/Time</p></td><td><ul><li>equals</li><li>does not equal</li><li>is before</li><li>is on or before</li><li>is after</li><li>is on or after</li></ul><p>Enter a specific date and time or choose a relative value (midnight yesterday, midnight today, midnight tomorrow, midnight one week from today, midnight on the first day of the previous month, and so forth). Midnight refers to the beginning of the day.</p><ul><li>is during</li><li>is not during</li></ul><p>Choose a relative date range (previous, current, next) for day, month, quarter, or year.</p></td></tr><tr><td><p>Time of Day</p><p>Duration</p></td><td><ul><li>equals</li><li>does not equal</li><li>is after</li><li>is on or after</li><li>is before</li><li>is on or before</li></ul></td></tr><tr><td><p>Checkbox</p></td><td><ul><li>is checked (or true)</li><li>is not checked (or false)</li></ul></td></tr></tbody></table>

**Notes:**

-   Connected table filters for Date and Date/Time fields are based on the timezone setting for the app where the connected table resides.
-   If you change the timezone setting for a connected table’s app, the new timezone may not be immediately used for existing Date and Date/Time filters during the next manual refresh. One way to ensure that the new timezone will be used is to sign out of Quickbase and sign back in before manually refreshing the connected table.

### Related topics:

-   [About connections](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-)
    
-   [About connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-)
    
-   [Refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)