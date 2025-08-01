> Access to this feature can change based on your Quickbase plan. Learn more about feature availability and plans in [Quickbase capabilities](https://helpv2.quickbase.com/hc/en-us/articles/21309804922004).

Create a [connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-) to access data about your realm's apps, audit logs, connected tables, pipelines, users and user tokens from the [Quickbase Admin Console](https://helpv2.quickbase.com/hc/en-us/articles/4570325441044-Admin-Console-Overview-). You can also add access information to [create a relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-) between the users and app data sources, which allows you to create reports on which apps users can access.

Note

Connections can only be set up by realm admins, with a limit of one Admin Console connected table for each type.

In this article

-   [Connect to the Quickbase Admin Console](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#h_01JXFZS2HSCTK4PMZ21P3886JW)
-   [View, test, or delete your connections](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#01GSZXFTMXBS0E6SFXZZGMH52S)
-   [View connected table details and history](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#01GSZXFTMX443NE49AXM1ZVY1G)
-   [Calculations used in displays](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#01H8HN9FS0YN02ZTMZE5RCNWZE)
-   [Limits](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#01GSZXFTMXH9FMSW4MWG695QJT)
-   [Integrate with Governance Core apps](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#h_01JATZR6JBV99H1SMEDV688N44)
-   [Fields available in the Admin console connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#h_01HH2AHQ6XC5950YC76W3E308F)
    -   [Access table](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#h_01JATJSCZVX2A2EXHTPMQEQ10W)
    -   [Apps table](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#h_01JATJV69RFHXATW9KE568S1BQ)
    -   [Audit logs table](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#h_01JH5XWF41XSJ6PRVNQG7WP0W4)
    -   [Connected tables table](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#h_01JATJV95TZREG2QNTTV3PTBWG)
    -   [Pipelines table](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#h_01JATJVC4PCG1CK0K32TPVGXVM)
    -   [Realm users table](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#h_01JATJVF73RWZG92KH67Z1VKP5)
    -   [Users table](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#h_01JATJVF73RWZG92KH67Z1VKP5)
    -   [User tokens table](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#h_01JATJVJ2VP9PCXR50QPS5PEVT)

Note

Date/Time connected fields, such as App Create Date for Apps and Last Access for Users, use UTC (Coordinated Universal Time).

Bring the data you want into your app and refresh it based on a schedule you set, or any time, on-demand.

You need:

-   **User Token**—This layer of security is required. This user token must be created by a realm admin in the target URL (see below). Realm admins can create a user token in your Profile.  
    Note: To set up the **Audit Logs** table, you must assign the user token used for the Admin Console connection to the app where the connected table resides.
    
-   **Quickbase URL**—Locate the Quickbase URL in the browser. For example, _https://yourcompanyname.quickbase.com_.
    

## Connect to the Quickbase Admin Console

1.  [Add a new connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table) and select Admin Console as the data source.
    
    -   If you're creating a new Admin Console connection, enter a connection name, the Quickbase URL, and the User Token.
    -   If you already have an Admin Console connection, select it from the options shown.
2.   Select one of the following sets of records:
    
    -   **Access**
    -   **Apps**
    -   **Audit logs**
    -   **Connected tables**
    -   **Pipelines**
    -   **Realm users** (only available for realms with multiple accounts)
    -   **Users** (only available for realms with a single account)
    -   **User tokens**
    
    Note
    
    If a connected table for a set of records has already been created, it states the app where that table resides and the connection owner.
    

## View, test, or delete your connections

To view **details about your connection** and [test](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-), [change](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), or [delete](https://helpv2.quickbase.com/hc/en-us/articles/4570322374036-Deleting-a-connection-) connections, click the user dropdown on the global bar, then click **Profile**. Your connections display in the **My Connections** area.

## View connected table details and history

To view **Details about your connected table**, including the connected service, connection owner, connected fields, filter, and schedule for the connected table, access the data connection settings in **Table Settings**. You can also view a **History** of recent refreshes and [edit the connected table filter](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table-Help-), [refresh schedule](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-), or [switch to use a different connection](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-).

## Calculations used in displays

Any conversions of the bytes in a connected field need to use base 2 (binary, 1024) and not base 10 (decimal, 1000).

## Limits

-   One Admin Console connected table for each type.
-   Connected tables using the Access source cannot be synced hourly.
-   Deactivated users aren't included in the results of the Admin Console Users and Access sources. Denied users aren't included in the results of the Access source. However, connected tables where the connection owner is denied or deactivated are included in the results of the Connected Tables source.
-   If a connected table was created in an account that is now inactive, it isn’t included in the Connected Tables results.
-   The _source_ fields only apply to connected tables when another Quickbase table is the source. For example, the source fields are empty if the source is Salesforce, QuickBooks, or Gmail.

## Integrate with Governance Core apps

Admin Console-connected tables can be used to power Quickbase's Governance Core apps. These apps streamline governance by creating a centralized location for all Admin Console-connected tables. [Learn more about optimizing connected tables](https://community.quickbase.com/discussions/quickbase-discussions/optimizing-quickbase-admin-console-connected-sync-tables-for-effective-governanc/86326)

Install the GCA Instructions app from the Exchange to view instructions on creating the Admin Console Sync Hub, which warehouse your connected tables.

To install the GCA instructions app:

1.  Go to the **Exchange** from the global navigation menu
2.  Search for GCA Instructions, and then select **Install**
3.  Name your app and select **Install**
4.  Follow the instructions to construct the Governance Core Apps

## Fields available in the Admin console connected tables

### Access table

This table allows you to bring in both users and apps information so you can report on which apps users have access to.

<table><tbody><tr><td><strong>Field</strong></td><td><strong>Description</strong></td></tr><tr><td>Key</td><td>Unique identifier for the access record</td></tr><tr><td>User ID</td><td>Identifier for the user associated with the record</td></tr><tr><td>App ID</td><td>Identifier for the application that the user accessed or managed</td></tr><tr><td>Last Accessed</td><td>The most recent date and time the user accessed the application</td></tr><tr><td>App-Level Permission</td><td>Permission level assigned to the user within the application</td></tr><tr><td>Account ID</td><td>Identifier for the Quickbase account the user belongs to</td></tr></tbody></table>

### Apps table

This table includes all applications in the realm.

<table><tbody><tr><td><strong>Field</strong></td><td><strong>Description</strong></td></tr><tr><td>ID</td><td>Unique identifier for each application or user</td></tr><tr><td>Application Name</td><td>The name of the application</td></tr><tr><td>Open To Internet</td><td>Indicates whether the application is accessible over the internet</td></tr><tr><td>Tables</td><td>The number of tables within the application</td></tr><tr><td>App Create Date</td><td>The date the application was created</td></tr><tr><td>Application Size (Bytes)</td><td>The total storage size occupied by the application, measured in bytes</td></tr><tr><td>API Count</td><td>The number of API requests made to the application</td></tr><tr><td>Attachment Size (Bytes)</td><td>The total size of file attachments within the application, measured in bytes</td></tr><tr><td>Manager UID</td><td>The user ID of the manager responsible for the application</td></tr><tr><td>Groups</td><td>The number of groups associated with the application</td></tr><tr><td>Last Modified</td><td>The date and time when the application was last modified</td></tr><tr><td>Manager Status</td><td>Indicates the status of the application manager</td></tr><tr><td># of users with any access</td><td>The total number of users with any level of access to the application</td></tr><tr><td># of users with direct access</td><td>The number of users with direct access permissions to the application</td></tr><tr><td>Last Access</td><td>The date and time when the application was last accessed by a user</td></tr><tr><td>Mobile offline enabled</td><td>Indicates whether the application supports offline access on mobile devices</td></tr><tr><td>Data change logs enabled</td><td>Indicates if logging of data changes is enabled</td></tr><tr><td>Sandbox required</td><td>Indicates whether a sandbox environment is required for the application</td></tr><tr><td>Sandbox enabled</td><td>Indicates if the sandbox environment is currently enabled for the application</td></tr><tr><td>Account ID</td><td>Identifier for the Quickbase account the user belongs to</td></tr></tbody></table>

### Audit logs table

This table contains audit logs for the realm. Audit log data is only available for full days in the past, and does not include data for the current day. Audit logs related to login events, API events, user events and activity, and record events are excluded from this table. Refer to the [Audit Log Library](https://resources.quickbase.com/nav/app/budurkasx/action/showpage/2b2941e4-f34d-4d41-9b0e-db790d20e9ab?pageIdV2=quickbase.com-DashboardGroup-15760d74-2243-4ce9-9495-7cc8790f12e7) to find out which specific actions are included.

At the time of set up, audit logs are available for up to 3 days in the past. To refresh the Audit Logs table without error, you must assign the user token used for the Admin Console connection to the app where the connected table resides. Data can be refreshed daily or manually. If a manual refresh hasn’t been performed within the past 3 days, only data for the last 3 days is returned.

Important

Once 95% of the table size limit (500MB) is reached, data is automatically purged from the oldest 3 days of audit log events.

<table><tbody><tr><td><strong>Field</strong></td><td><strong>Description</strong></td></tr><tr><td>Log ID</td><td>Unique identifier of the audit log</td></tr><tr><td>First name</td><td>User’s first name</td></tr><tr><td>Last name</td><td>User’s last name</td></tr><tr><td>Email address</td><td>User’s email address</td></tr><tr><td>Action</td><td>What action was taken, such as log in, create app, report access, or table search</td></tr><tr><td>Time</td><td>The exact time the action was taken, including date, and time with hour, minutes and seconds. Time zone is displayed in UTC in connected tables.</td></tr><tr><td>IP</td><td>The IP address the action was taken from</td></tr><tr><td>User agent</td><td>The browser and OS the action was taken from</td></tr><tr><td>Session info</td><td>The Session ID associated with a user’s browsing session on a particular device (which resets when the session expires), or a short snippet of the User Token, which is used for compatible API calls</td></tr><tr><td>Description</td><td><p>A description of the action that occurred.</p><p>View examples of descriptions in the <a href="https://resources.quickbase.com/nav/app/budurkasx/action/showpage/2b2941e4-f34d-4d41-9b0e-db790d20e9ab?pageIdV2=quickbase.com-DashboardGroup-15760d74-2243-4ce9-9495-7cc8790f12e7">Audit Log Library.</a></p></td></tr><tr><td>Resource URL</td><td>A link to the resource that was accessed or changed</td></tr><tr><td>Application</td><td>UI for user interface or API for an API call</td></tr><tr><td>User ID</td><td>Unique identifier for the user associated with the record</td></tr><tr><td>Payload changes</td><td>Details the record changes, if there are any</td></tr></tbody></table>

### Connected Tables table

This table includes all connected tables that exist in the realm.

<table><tbody><tr><td><strong>Field</strong></td><td><strong>Description</strong></td></tr><tr><td>Source Table Name</td><td>The name of the table in the source application</td></tr><tr><td>Source Table ID</td><td>The unique identifier for the source table</td></tr><tr><td>Source App Name</td><td>The name of the source application containing the table</td></tr><tr><td>Source App ID</td><td>The unique identifier for the source application</td></tr><tr><td>Source App Manager ID</td><td>The user ID of the manager responsible for the source application</td></tr><tr><td>Source Realm ID</td><td>The unique identifier for the realm containing the source application</td></tr><tr><td>Source Account ID</td><td>The account ID associated with the source application</td></tr><tr><td>Destination Table Name</td><td>The name of the table in the destination application</td></tr><tr><td>Destination Table ID</td><td>The unique identifier for the destination table</td></tr><tr><td>Destination App Name</td><td>The name of the destination application containing the table</td></tr><tr><td>Destination App ID</td><td>The unique identifier for the destination application</td></tr><tr><td>Destination App Manager ID</td><td>The user ID of the manager responsible for the destination application</td></tr><tr><td>Destination Realm ID</td><td>The unique identifier for the realm containing the destination application</td></tr><tr><td>Destination Account ID</td><td>The account ID associated with the destination application</td></tr><tr><td>Connection Name</td><td>The name of the connection between the source and destination tables</td></tr><tr><td>Connection Owner ID</td><td>The user ID of the person who owns the connection</td></tr><tr><td>Last Refreshed</td><td>The most recent date and time the connection was refreshed</td></tr><tr><td>Data Source</td><td>Indicates the origin or type of data source used in the connection</td></tr></tbody></table>

### Pipelines table

This table includes all Pipelines within the realm.

<table><tbody><tr><td><strong>Field</strong></td><td><strong>Description</strong></td></tr><tr><td>User ID</td><td>Identifier for the user associated with the record</td></tr><tr><td>Pipeline ID</td><td>The unique identifier for the pipeline</td></tr><tr><td>Description</td><td>A description of the pipeline's function or purpose</td></tr><tr><td>Pipeline Trigger Type</td><td>Specifies the type of trigger that activates the pipeline (e.g., schedule-based, event-based)</td></tr><tr><td>State</td><td>The current state or status of the pipeline (e.g., active, paused)</td></tr><tr><td>Last Triggered</td><td>The date and time when the pipeline was last triggered</td></tr><tr><td>Pipeline Name</td><td>The name of the pipeline</td></tr><tr><td>App IDs</td><td>The identifier of the apps used in the pipeline</td></tr><tr><td>Tables and fields</td><td>Tables and fields used in the pipeline</td></tr><tr><td>Channels</td><td>Channels used in the pipeline</td></tr><tr><td>Last Modified</td><td>Date the pipeline was last updated</td></tr><tr><td>Successful runs (last 24 hours)</td><td>Successful pipeline runs from the last 24 hours</td></tr><tr><td>Unsuccessful runs (last 24 hours)</td><td>Unsuccessful pipeline runs from the last 24 hours</td></tr><tr><td>Tags</td><td>Tags used in the pipeline</td></tr><tr><td>Quickbase Authentication (User Token, Simple Auth or Mixed)</td><td>The authentication method used for the pipeline</td></tr></tbody></table>

### Realm users table

This table includes all users in the realm, excluding deactivated users. It is only available for realms that have multiple accounts. Realms with a single account can connect to the [Users](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#01JXG049G2PCHYE5F9Q9A8EWK4) table instead. 

<table><tbody><tr><td><strong>Field</strong></td><td><strong>Description</strong></td></tr><tr><td>Account User ID</td><td>The combined Account ID and ID used as a unique identifier</td></tr><tr><td>Account ID</td><td>Identifier for the Quickbase account the user belongs to</td></tr><tr><td>ID</td><td>Unique identifier of the user</td></tr><tr><td>First Name</td><td>The user's first name</td></tr><tr><td>Last Name</td><td>The user's last name</td></tr><tr><td>Email</td><td>The user's email address</td></tr><tr><td>Username</td><td>The username associated with the user's account</td></tr><tr><td>Last Access</td><td>The date and time when the application was last accessed by a user</td></tr><tr><td>Access Status</td><td>Indicates the current access status of the user (e.g., active, suspended)</td></tr><tr><td>Can Create Apps</td><td>Indicates whether the user has permission to create applications</td></tr><tr><td>In Realm Company</td><td>Specifies if the user is part of a company within the realm</td></tr><tr><td>Realm Approved</td><td>Indicates whether the user is approved in the realm</td></tr><tr><td>Number of Groups</td><td>The number of groups the user belongs to</td></tr><tr><td>Number of Groups Managed</td><td>The number of groups the user manages</td></tr><tr><td>Realm Admin</td><td>Indicates if the user has realm-level administrative privileges</td></tr><tr><td>Realm Registration Status</td><td>Specifies the user's registration status in the realm</td></tr><tr><td>External Auth ID</td><td>The external authentication ID associated with the user</td></tr><tr><td>Account Admin</td><td>Indicates if the user has account-level administrative privileges</td></tr><tr><td>Super User</td><td>Indicates if the user has elevated privileges beyond normal users</td></tr><tr><td>Receive security question reset requests</td><td>Specifies if the user receives requests to reset security questions</td></tr><tr><td># of apps managed</td><td>The number of applications managed by the user</td></tr><tr><td>Pipelines create permission</td><td>Indicates if the user has permission to create pipelines</td></tr><tr><td>App Admin</td><td>Indicates if the user has administrative privileges within applications</td></tr><tr><td>Can Create Tokens</td><td>Indicates if the user can create authentication tokens</td></tr><tr><td>Access to Solutions</td><td>Specifies the user's level of access to pre-configured solutions</td></tr><tr><td>Authentication</td><td>Indicates the authentication method used for the user</td></tr><tr><td>Service Account</td><td>The name of the service account</td></tr><tr><td>Service Account Assigned Users</td><td>The users assigned to the service account</td></tr></tbody></table>

### Users table

This table includes all users in the realm, excluding deactivated users. It is only available for realms that have a single account. Realms with multiple accounts can connect to the [Realm users](https://helpv2.quickbase.com/hc/en-us/articles/4570424924052-Connect-to-the-Quickbase-admin-console#h_01JATJVF73RWZG92KH67Z1VKP5) table instead. 

<table><tbody><tr><td><strong>Field</strong></td><td><strong>Description</strong></td></tr><tr><td>ID</td><td>Unique identifier of the user</td></tr><tr><td>First Name</td><td>The user's first name</td></tr><tr><td>Last Name</td><td>The user's last name</td></tr><tr><td>Email</td><td>The user's email address</td></tr><tr><td>Username</td><td>The username associated with the user's account</td></tr><tr><td>Last Access</td><td>The date and time when the application was last accessed by a user</td></tr><tr><td>Access Status</td><td>Indicates the current access status of the user (e.g., active, suspended)</td></tr><tr><td>Can Create Apps</td><td>Indicates whether the user has permission to create applications</td></tr><tr><td>In Realm Company</td><td>Specifies if the user is part of a company within the realm</td></tr><tr><td>Realm Approved</td><td>Indicates whether the user is approved in the realm</td></tr><tr><td>Number of Groups</td><td>The number of groups the user belongs to</td></tr><tr><td>Number of Groups Managed</td><td>The number of groups the user manages</td></tr><tr><td>Realm Admin</td><td>Indicates if the user has realm-level administrative privileges</td></tr><tr><td>Realm Registration Status</td><td>Specifies the user's registration status in the realm</td></tr><tr><td>External Auth ID</td><td>The external authentication ID associated with the user</td></tr><tr><td>Account Admin</td><td>Indicates if the user has account-level administrative privileges</td></tr><tr><td>Super User</td><td>Indicates if the user has elevated privileges beyond normal users</td></tr><tr><td>Receive security question reset requests</td><td>Specifies if the user receives requests to reset security questions</td></tr><tr><td># of apps managed</td><td>The number of applications managed by the user</td></tr><tr><td>Pipelines create permission</td><td>Indicates if the user has permission to create pipelines</td></tr><tr><td>App Admin</td><td>Indicates if the user has administrative privileges within applications</td></tr><tr><td>Can Create Tokens</td><td>Indicates if the user can create authentication tokens</td></tr><tr><td>Access to Solutions</td><td>Specifies the user's level of access to pre-configured solutions</td></tr><tr><td>Authentication</td><td>Indicates the authentication method used for the user</td></tr><tr><td>Service Account</td><td>The name of the service account</td></tr><tr><td>Service Account Assigned Users</td><td>The users assigned to the service account</td></tr></tbody></table>

### User tokens table

This table contains all user tokens created within the realm.

<table><tbody><tr><td><strong>Field</strong></td><td><strong>Description</strong></td></tr><tr><td>Token ID</td><td>The unique identifier for each token</td></tr><tr><td>Token Name</td><td>The name of the token</td></tr><tr><td>Description</td><td>A description of the pipeline's function or purpose</td></tr><tr><td>Owner First Name</td><td>The first name of the token's owner</td></tr><tr><td>Owner Last Name</td><td>The last name of the token's owner</td></tr><tr><td>Owner Email</td><td>The email address of the token's owner</td></tr><tr><td>Token Date Created</td><td>The date the token was created</td></tr><tr><td>Last Used</td><td>The most recent date and time the token was used</td></tr><tr><td>Active</td><td>Indicates whether the token is active</td></tr><tr><td>App Names</td><td>The names of the applications associated with the token</td></tr><tr><td>App IDs</td><td>The unique identifiers of the applications associated with the token</td></tr><tr><td># of Apps</td><td>The number of applications associated with the token</td></tr><tr><td>Owner User ID</td><td>The user ID of the token's owner</td></tr></tbody></table>

### Related topics:

-   [About connections](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-)
    
-   [About data connection details](https://helpv2.quickbase.com/hc/en-us/articles/4570281951252-Viewing-connected-table-details-)
    
-   [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-)
    
-   [Refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)
    
-   [Testing a connection](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-)
    
-   [About connected fields](https://helpv2.quickbase.com/hc/en-us/articles/4570265917332-About-connected-fields-)