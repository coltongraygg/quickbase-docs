A connected table displays and automatically refreshes data from:

-   [a connected service](https://helpv2.quickbase.com/hc/en-us/sections/4572558818708-Connecting-to-other-services), like Salesforce.com, QuickBooks Online, Gmail, Exchange, and others.
    
-   [a connected folder containing CSV files](https://helpv2.quickbase.com/hc/en-us/articles/4570365490964-Connecting-to-a-folder-containing-CSV-files-) stored in Box, Dropbox, Google Drive, or your SFTP server.
    
-   [another Quickbase app](https://helpv2.quickbase.com/hc/en-us/articles/4570395540628-Connecting-to-another-Quickbase-app-)
    
-   The [Quickbase Admin Console](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connecting-to-Quickbase-Admin-Console-)
    

Create a new connected table, drag and drop to select the fields you want to connect, filter the data you bring into Quickbase, and set a schedule to automatically refresh the data in connected fields. You can also refresh data on-demand, any time you want.

This article explains:

-   [What makes connected data different](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-Creating-connected-tables#What)
    
-   [What connected data can do](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-Creating-connected-tables#connected_data_use_cases)
    
-   [How to create a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-Creating-connected-tables#How)
    
-   [What’s in a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-Creating-connected-tables#What%E2%80%99s)
    
-   [Refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-Creating-connected-tables#Refreshi)
    

## What makes connected data different

Data from a connected table flows into Quickbase. Since the data comes from another app, service, or folder containing CSV data, you can’t edit the data in connected fields. This helps keep your data in sync and eliminates confusion about what system is most up-to-date. To add or remove records from your connected table, [refresh the table](https://help.quickbase.com/user-assistance/refreshing_your_connected_table.html) to display the latest connected data.

You can have multiple connected tables within a Quickbase app. Each connected table uses one [connection](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-) to access data. You can re-use your connections across Quickbase apps.

## What connected data can do

You can use connected data to build reports across all your data from within Quickbase. [Add fields](https://helpv2.quickbase.com/hc/en-us/articles/4570374838292-Adding-new-fields-), [create relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-), lookups, and summary fields, [configure permissions](https://helpv2.quickbase.com/hc/en-us/articles/4570355458836-Configure-Permissions-for-a-Role-) and use your connected data in workflows, reports, and home pages.

For example, you might use connected tables to:

<table><tbody><tr><td><strong>Calculate project ROI</strong></td><td>Connect <a href="https://helpv2.quickbase.com/hc/en-us/articles/4570391084180-Connecting-to-QuickBooks-Online-">QuickBooks Online</a> Invoices &amp; Expenses and then relate to projects managed in Quickbase.</td></tr><tr><td><strong>Pay the right people at the right time</strong></td><td>Connect <a href="https://helpv2.quickbase.com/hc/en-us/articles/4570391084180-Connecting-to-QuickBooks-Online-">QuickBooks Online</a> Invoices &amp; Payments and then relate to jobs managed in Quickbase.</td></tr><tr><td><strong>Track programs &amp; campaigns more efficiently</strong></td><td>Connect <a href="https://helpv2.quickbase.com/hc/en-us/articles/4570366929812-Connecting-to-Salesforce-com-">Salesforce.com</a> Accounts and then relate to partner programs managed in Quickbase. Connect Salesforce Contacts and then relate to marketing programs managed in Quickbase.</td></tr><tr><td><strong>Gain visibility into project pipelines</strong></td><td>Connect <a href="https://helpv2.quickbase.com/hc/en-us/articles/4570366929812-Connecting-to-Salesforce-com-">Salesforce.com</a> Opportunities and then start onboarding projects in Quickbase.</td></tr><tr><td><strong>Track detailed customer interactions</strong></td><td>Connect <a href="https://helpv2.quickbase.com/hc/en-us/articles/4570339647380-Connecting-to-Zendesk-">Zendesk</a> Tickets and then relate to customer projects managed in Quickbase.</td></tr><tr><td><strong>Gain a holistic customer view</strong></td><td>Connect <a href="https://helpv2.quickbase.com/hc/en-us/articles/4570391084180-Connecting-to-QuickBooks-Online-">QuickBooks Online</a> Invoices &amp; Payments and then relate to customers or projects managed in Quickbase. Connect <a href="https://helpv2.quickbase.com/hc/en-us/articles/4570366929812-Connecting-to-Salesforce-com-">Salesforce.com</a> Accounts &amp; Cases and then relate to technical sales campaigns managed in Quickbase.</td></tr><tr><td><strong>Prioritize tickets based on customer lifetime value</strong></td><td><a href="https://helpv2.quickbase.com/hc/en-us/articles/4570365490964-Connecting-to-a-folder-containing-CSV-files-">Connect to CSV data</a> from a financial system behind the firewall and relate to the ticketing system managed in Quickbase.</td></tr><tr><td><strong>Track customer emails to sales reps</strong></td><td><a href="https://helpv2.quickbase.com/hc/en-us/articles/4570365490964-Connecting-to-a-folder-containing-CSV-files-">Connect to </a>a central email account, like <a href="https://helpv2.quickbase.com/hc/en-us/articles/4570349790996-Connecting-to-Gmail-">Gmail</a> or <a href="https://helpv2.quickbase.com/hc/en-us/articles/4570319548820-Connecting-to-Exchange-server-">Exchange</a> to bring email messages into Quickbase.</td></tr></tbody></table>

## How to create a connected table

Click **New Table** in the sidebar and then click **Using connected data**. See [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-) for details.

Connected tables display in the sidebar with the ![](https://helpv2.quickbase.com/hc/article_attachments/28605211591956) icon.

## What’s in a connected table

Connected tables display connected records, based on the fields you selected to connect and the filter and refresh options you set. Connected tables and [connected fields](https://helpv2.quickbase.com/hc/en-us/articles/4570265917332-About-connected-fields-) display with a ![](https://helpv2.quickbase.com/hc/article_attachments/28605211591956).

Like all Quickbase tables, connected tables include the five built-in Quickbase fields: Date Created, Date Modified, Record ID#, Record Owner, and Last Modified By.

Connected tables also include a [Refresh Key](https://helpv2.quickbase.com/hc/en-us/articles/4570260038804-About-the-Refresh-Key-field-) field that tells Quickbase what data makes each record that you are connecting unique. Quickbase uses the refresh key, along with the [refresh options](https://helpv2.quickbase.com/hc/en-us/articles/4570314286100-About-refresh-options-) you select, to refresh your data.

Whoever owns the connection can [change the filter](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table-Help-) to display a different set of records and [add new connected fields](https://helpv2.quickbase.com/hc/en-us/articles/4570325865236-Adding-more-connected-fields-) or [remove connected fields](https://helpv2.quickbase.com/hc/en-us/articles/4570367639316-Deleting-a-field-) from the connected table at any time. You can also add Quickbase fields to connected tables.

Note: You can only add connected fields to a connected table.

## Refreshing in a connected table

To add or update a record with the most current data available in the connected data source, [refresh your connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-).

When you refresh a connected table, Quickbase Sync compares the data in the connected table with the data in the external app, service, or most recent CSV file in your connected folder.

Based on the refresh options you selected, Quickbase Sync refreshes your connected table. Depending upon the purpose of your connected table, you can set refresh options to make the table match the data currently in the connected app, service, or CSV or to keep all the data in your connected table, even if the data is not currently in the connected app, service, or CSV file.  
Keeping your data in a CSV can be a good choice if your table serves as an archive of all records. For more info, see [About refresh options](https://helpv2.quickbase.com/hc/en-us/articles/4570314286100-About-refresh-options-).

### Related topics:

-   [About connections](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-)
    
-   [About connected fields](https://helpv2.quickbase.com/hc/en-us/articles/4570265917332-About-connected-fields-)
    
-   [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-)
    
-   [Connecting to a folder containing CSV files](https://helpv2.quickbase.com/hc/en-us/articles/4570365490964-Connecting-to-a-folder-containing-CSV-files-)
    
-   [FAQs about connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570374698388-FAQs-about-connected-tables-)
    
-   [Refreshing the data in your connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)