Connections provide access to data in a [cloud app, service](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-), or [folder containing CSV files](https://helpv2.quickbase.com/hc/en-us/articles/4570365490964-Connecting-to-a-folder-containing-CSV-files-). They enable you to bring data into a [connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-) in your Quickbase app and keep the data in sync.

A connection belongs to you and contains references to the service that it connects to, for example, Salesforce.com or QuickBooks Online. You can reuse your connection to create multiple connected tables in multiple Quickbase apps and create new connections as needed.

This article covers general information about connections, including requirements and how to reauthorize, view, test, and delete connections. 

Learn more about connecting to a specific data source:

-   [Folders containing CSV files in Box, Dropbox, Google Drive, or an SFTP server](https://helpv2.quickbase.com/hc/en-us/articles/4570365490964-Connecting-to-a-folder-containing-CSV-files-)
    
-   [Another Quickbase app](https://helpv2.quickbase.com/hc/en-us/articles/4570395540628-Connecting-to-another-Quickbase-app-)
    
-   [Quickbase Admin Console](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connecting-to-Quickbase-Admin-Console-)
    
-   [Bill.com](https://helpv2.quickbase.com/hc/en-us/articles/4570367115412-Connecting-to-Bill-com-)
    
-   [Exchange server](https://helpv2.quickbase.com/hc/en-us/articles/4570319548820-Connecting-to-Exchange-server-)
    
-   [Gmail](https://helpv2.quickbase.com/hc/en-us/articles/4570349790996-Connecting-to-Gmail-)
    
-   [Intacct](https://helpv2.quickbase.com/hc/en-us/articles/4570137783316-Connecting-to-Intacct-)
    
-   [NetSuite](https://helpv2.quickbase.com/hc/en-us/articles/4570276321300-Connecting-to-NetSuite-)
    
-   [QuickBooks Online](https://helpv2.quickbase.com/hc/en-us/articles/4570391084180-Connecting-to-QuickBooks-Online-)
    
-   [Salesforce.com](https://helpv2.quickbase.com/hc/en-us/articles/4570366929812-Connecting-to-Salesforce-com-)
    
-   [Zendesk](https://helpv2.quickbase.com/hc/en-us/articles/4570339647380-Connecting-to-Zendesk-)
    

## Multiple connections to a service

We recommend that you create a second connection to a service, such as QuickBooks Online, only if you need to access a new account or company. While some data sources, such as Salesforce.com, allow multiple connections to the same company information, others, such as QuickBooks Online, do not.In fact, QuickBooks Online allows only one connection to a company, regardless of the connection owner. You may need to coordinate among app admins when creating QuickBooks connections.

For example, if you sign in differently to access different companies in QuickBooks Online, then you would have two different QuickBooks connections: one to Company A and one to Company B. Each of these connections provides access to the QuickBooks data associated with the company, user name, and password that you supplied.

Since connections are unique to you, you can give each connection a name. For example, _Pam’s QBO Company A_ connection.

## What do I need to create a connection?

Each data source has different requirements for providing Quickbase with access to your data. Many data sources, such as Salesforce.com and QuickBooks Online, use Open Authentication (OAuth), an industry standard that securely grants access to data, while protecting personal information, such as your user name and password.

In addition to credentials, some data sources also have other requirements:

-   **Salesforce.com**: requires that your Salesforce.com account have **API access** enabled. Your user account must also have the **API Enabled** permission selected.
    
-   **QuickBooks Online**: requires that you are a QuickBooks Online **Administrator**. QuickBooks Online allows _only one active connection to a company_. If you create a new QuickBooks Online connection to the same company, the prior connection is invalid.
    

Tip: For help while creating a new connected table, click the **Help** icon in the top right and we'll guide you along.

## To reauthorize a connection

The Reauthorize button is available only for connections that use OAuth authentication. Use it to reconnect a connection token that has expired or become invalid.

1.  Select the user dropdown on the global bar, then choose **Profile**.
2.  In the My Connections section, select the connection you want to reauthorize.
3.  Click **Reauthorize** and sign in to the account.

## View, test, or delete your connections

To view **details about your connection** and [test](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-), [change](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), or [delete](https://helpv2.quickbase.com/hc/en-us/articles/4570322374036-Deleting-a-connection-) connections, click the user dropdown on the global bar, then click **Profile**. Your connections display in the **My Connections** area.

## View connected table details and history

To view **Details about your connected table**, including the connected service, connection owner, connected fields, filter, and schedule for the connected table, access the connection in table settings. You can also view a **History** of recent refreshes, and [edit the connection filter](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table-Help-), [refresh schedule](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-), or [switch to use a different connection](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), if necessary.

### Related topics:

-   [About connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-)
    
-   [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-)
    
-   [Deleting a connection](https://helpv2.quickbase.com/hc/en-us/articles/4570322374036-Deleting-a-connection-)
    
-   [FAQs about connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570374698388-FAQs-about-connected-tables-)
    
-   [Refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)
    
-   [Testing a connection](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-)
    
-   [Using a different connection](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-)