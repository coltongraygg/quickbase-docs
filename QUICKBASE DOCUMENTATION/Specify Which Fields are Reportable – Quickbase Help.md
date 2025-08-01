You've designed your Quickbase app to store and track lots of information, and so each table in your app may contain many fields. When your users are creating reports, they don't necessarily need to filter or report on every field in every table. In fact, there are some fields and field types they'll never need for these purposes.

The Reportable column on the Fields list lets you specify which fields you want to show in these cases. Put a check in this column to show a field in lists of criteria used for filtering, sorting, and grouping report data in Quickbase. Note that fields listed as default columns on the [Default report settings](https://helpv2.quickbase.com/hc/en-us/articles/4570348881300-Setting-reporting-defaults-) page are automatically reportable.

Note: If this column does not appear in the field list, click the **Advanced Options** link, select **Reportable**, and click **Save** on the Page bar.

When you designate a field as reportable, Quickbase makes that field available in the Report Builder for filtering, sorting, and grouping reports. In addition, you can choose reportable fields as columns that display on a report.

Outside of the Report Builder, reportable fields are available in most places where you can specify filter criteria. That is, you'll be able to select reportable fields when you:

-   Perform an Advanced Search operation from a table Home page
    
-   Specify additional criteria in Email Notifications and Reminders
    

When a field is NOT reportable, it isn't available for filtering, sorting, or grouping in the Report Builder. You can't select it to appear as a column in any report. And, it isn't available for filtering in any of the scenarios listed above.

## Why designate reportable fields?

When you designate only some fields as reportable, you can greatly reduce the number of fields users need to deal with when creating reports. And, limiting the number of fields that are reportable can help speed up how quickly fields load in the Report Builder.

## How does the Reportable option affect the default columns?

On the Default Report Settings page, you can specify fields that you want to be used as the default columns in your reports. Default columns will automatically appear on a report when the report creator doesn't customize it, and in certain other scenarios. (See [How Quickbase Uses Default Report Settings](https://helpv2.quickbase.com/hc/en-us/articles/4570348881300-Setting-reporting-defaults-#defaultreportplaces).)

The Reportable option affects not only whether the field appears in filtering criteria, but also whether the field will be available for display in your reports. Therefore, if you've selected a field for the default columns, that field must also be reportable. Quickbase will actually enforce this relationship, by automatically selecting the Reportable option when you specify that a field should be a default column.

## What about iCalendar, vCard, Report Link, and Formula URLs?

In reality, there are certain field types on which you'll never need to filter, group, or sort: namely iCalendar, vCard, Report Link, and Formula - URL fields. Because of this, these field types will NEVER appear in the field lists used for filtering, sorting, or grouping, even if you set the Reportable option for them.

In these cases, the Reportable option means that the field will be available for users to choose when customizing reports. It also means that you can choose to include it as a default column for your reports. It will not, however, cause the field to appear in filtering, sorting, or grouping dropdowns.  You'll never have to scroll through these field types when searching or building criteria for reports or email notifications or reminders.

## How does changing the reportable option affect existing reports, notifications, and reminders?

If you turn the Reportable property off for a field that's already used in an existing report, notification, or reminder, Quickbase still uses the field correctly. However, when you modify the report, notification, or reminder, you'll see that Quickbase displays the field in red.

In the Report Builder example below, you can see that Venue field appears in red. This means that the option was set on this field at the time the report was created, but it has since been turned off.  If you don't change this field, the report will remain this way and will use the Venue field in filter criteria. However, if you select another field here, and then save the report, the Venue field will no longer appear as an available filter. (The same is true for email reminders and notifications.)

![](https://helpv2.quickbase.com/hc/article_attachments/4572899692564/notreportable_callout.png)

## How to make a single field reportable

To make a single field reportable, go to the field's properties page, and select The field may be used in reports from the Reportable option under Advanced options. Click **Save** on the Page bar to save your changes.

![](https://helpv2.quickbase.com/hc/article_attachments/4572871939348/reportableproperty.png)

## How to make several fields reportable

To make several fields reportable, go to the Fields list page. If the Reportable column does not appear in the field list, click the Advanced Options link, select Reportable, and click Save on the Page bar. Set the checkmark in the Reportable column for any field you want to see in Report Builder.

![](https://helpv2.quickbase.com/hc/article_attachments/4572893154452/reportable_column.png)

Note: If a column has been set to be a default column on the [Default report settings](https://helpv2.quickbase.com/hc/en-us/articles/4570348881300-Setting-reporting-defaults-) page, it is automatically checked on the Fields list and cannot be changed.

### Related topics:

-   [Preventing Quickbase from Searching a Field](https://helpv2.quickbase.com/hc/en-us/articles/4570284211860-Excluding-fields-from-searches-)