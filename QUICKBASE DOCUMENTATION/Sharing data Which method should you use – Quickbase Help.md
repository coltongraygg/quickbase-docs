One of the most powerful aspects of Quickbase is that you can create many apps that can be deployed across your enterprise and accessed with a shared user base. The more apps you build and share, the more value you drive in your business. This article discusses the different ways you can share, replicate, and transform data in Quickbase and explores the various tools Quickbase provides for moving data between apps:

-   [Connected tables](https://helpv2.quickbase.com/hc/en-us/articles/19713658161428-Sharing-data-Which-method-should-you-use#h_01HBV1976AFQ1ZBMX5GGNFWMAG)
-   [Pipelines](https://helpv2.quickbase.com/hc/en-us/articles/19713658161428-Sharing-data-Which-method-should-you-use#h_01HBV1HHJJNG59ZH8HTEW8AV2K)
    -   [Pipelines - Copy Records](https://helpv2.quickbase.com/hc/en-us/articles/19713658161428-Sharing-data-Which-method-should-you-use#h_01HF77A8TCWCZBEWQ0B79VVQA6)
-   [Cross-app relationships](https://helpv2.quickbase.com/hc/en-us/articles/19713658161428-Sharing-data-Which-method-should-you-use#h_01HBTXYD2RPYQK18DPQ3N4M6J2)
-   [Table-to-table imports](https://helpv2.quickbase.com/hc/en-us/articles/19713658161428-Sharing-data-Which-method-should-you-use#h_01HBTYD5M0WVT3EXAAVP2TZP7J)

The aim is to make it easier for builders to decide which strategy works best for their needs. 

## Connected tables

Use connected tables (formerly Quickbase Sync) to connect tables to numerous cloud services including Quickbase itself. Connected tables can also connect to .csv files via cloud storage services such as Box, Dropbox, and Google Drive; as well as SFTP servers.  

**_Key Benefit_** \- You can easily configure and schedule data replication.  

Pros: 

-   You can easily connect Quickbase tables using the wizard configurator 
-   You can use light filtering 
-   You can schedule table refreshes can up to every hour 
-   You can run applications independently without sharing resources (CPU) 

Cons: 

-   Data is read-only 
-   No real-time updates 
-   Refreshes require comparing data sets, which can take a few minutes
-   Cannot do nested filtering 

Connected tables works well when: 

1.  You need to schedule table refreshes for times when there is light usage in the source and destination applications. 
2.  You need a hub-and-spoke model where multiple destination tables pull data from the source. 
3.  You need to keep applications decoupled. 
4.  You don't need to edit the data in the destination table. 

### Considerations for connected tables

-   Don't schedule unnecessary updates
-   Consider the frequency of updates being made in the source and how quickly you need the updates in the destination. Your needs will help determine the refresh schedule and eliminate unnecessary updates. 
-   Consider not creating an endless hub and spoke model. Too many connections on one source can begin to cause bottlenecks.
-   Do not do more than one sync an hour against the source. Consider having a master source and additional satellite sources to support multiple syncs in a given hour.

#### Consider alternative Quickbase functionality when real-time updates are needed

Connected table updates are scheduled or manually executed. When real-time updates are needed consider using other tools which trigger updates on changes in the source, such as pipelines.  

#### Use connected tables to decouple application dependencies

Connected tables allow builders to easily connect tables between applications without sharing system resources. As such, this tool can be useful when you need to connect multiple large and complex apps with high usage.

#### Schedule refreshes during low use times when possible

Table refreshes can be expensive and take minutes when the data sets being replicated are large. When using connected tables, a best practice is to schedule refreshes during non-business hours/low usage. 

#### Ensure the connection owner has the appropriate privileges in the destination

The connection to the source table is established and maintained with the credentials and permissions of the person who created the connection. The user creating the connection in the destination app must be in a role that has administrative rights. User access to the destination table is controlled the same way as any other table in the destination application, through roles and permissions. 

Learn more about [creating connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716).  

## Pipelines 

You can use [Pipelines](https://helpv2.quickbase.com/hc/en-us/articles/7009738152212) to perform actions on Quickbase data across applications (and realms) either by a trigger (data added, modified, or deleted) or on a schedule and fully integrate their data across cloud-based software tools, as well as some [on-premise](https://help.quickbase.com/pipelines/On_premises_connectivity.html) systems.

**_Key Benefit -_** _You can_ create a workflow with no code and connect disparate third-party systems without always needing to use an API. 

Pros:  

-   No coding is required 
-   Easy to replicate data across apps
-   Execute in real-time or on a schedule 
-   Built-in resiliency
-   Perform actions against another application without sharing system resources (CPU) 
-   Ability to take action(s) based on responses 
-   Connect third party systems – Quickbase is not required to be part of a pipeline

Cons: (_please keep in mind some of these will be addressed in future_ [_releases_](https://help.quickbase.com/release-notes/all.html)) 

-   Visible only to user who created the pipeline (and realm admins via [Switch User](https://helpv2.quickbase.com/hc/en-us/articles/4481359830676) functionality.) 

Pipelines work well when:  

1.  You need to transform data before upserting to another table/system 
2.  You need to integrate with [third party systems](https://help.quickbase.com/pipelines/about_channels.html) such as Salesforce, Jira, Box, or via an API 
3.  You need to take action(s) on a response from another action (add/delete/update action) 
4.  You want to set your applications up for maximum scale

### _Pipelines considerations_ 

#### Don’t create infinite loops

Actions, webhooks, and triggered pipelines all execute based on a trigger. Ensure triggering one doesn’t trigger the initiator. 

#### Consider the rate at which your pipelines will fire

For any app, a maximum of 50 HTTP messages can be sent per second. If the rate is exceeded, subsequent messages are not sent, and the app manager receives an alert and email notification. The limit of 50 triggers per second becomes increasingly important with scripts involving a high frequency of adds, edits, and deletes that will trigger a pipeline. 

#### Consider how real-time your changes need to be

You’re able to have 90 unique triggers per Quickbase table. Scheduling pipelines or utilizing callable pipelines is a scalable and efficient building pattern. Consider consolidating pipelines if they share a trigger and using logic within the pipeline to drive the workflow. 

#### Schema changes can break pipelines

Pipelines do not have control over changes made to the schema. Therefore, changes to field names could break a pipeline. _Set up a process to audit your pipelines._ Pipelines does not currently have a notification for failures.

Learn more about [building pipelines](https://helpv2.quickbase.com/hc/en-us/articles/4482687641236). 

### Pipelines - Copy Records

The Copy Records step is a key feature in Pipelines when considering options for sharing data across applications. It offers an automated data replication pattern across the Quickbase platform. It is simple, efficient, and powerful, with built-in data replication mapping between tables in separate applications.

Pros:

-   It's easy to configure your field mappings
-   Large datasets get intelligently divided into smaller chunks which maximizes execution speed
-   Supports complex filtering criteria
-   Does not create application dependencies between the source and destination
-   Can be scheduled or triggered in Pipelines

Cons:

-   Data does not move in real-time
-   Does not support data transformation
-   You must have access to both source and destination

Copy Records works well when:

-   You need to replicate large data sets between applications
-   You are implementing a hub and spoke model. (The data hub and spoke model is a data architecture approach that is designed to centralize and streamline the management of data within an organization. In this model, the “hub” serves as a central repository for data, while the “spokes” represent the various systems and applications that interact with the hub to access and exchange data.)
-   You're aggregating data from multiple applications into a consolidated view

#### Copy Records considerations

If your data has inconsistencies like missing required or unique fields, you may have errors when using Copy Records. Depending on the volume of data you're moving, the copy records step may upsert your data in chunks. This means if one chunk has errors that collection of records will fail while all other chunks will continue to be upserted. There is no roll-backs of Copy Records. 

Tips:

-   Check to see that your data types match when you're mapping fields, to prevent unwanted results. The one exception is importing a numeric into a text field, which displays the number in text form.
-   Copy records allows the source and destination application to operate independently
-   Copy records does not create dependencies which allows builders to create solutions (collections of applications and pipelines that work together) that scale. When applications operate independently the platform will load balance them appropriately.

## Cross-app relationships 

You can use cross-app relationships to connect two tables from different applications within a given account. They are quick to set up and follow the same pattern as relating two tables in the same Quickbase app.  

**_Key Benefit_** \- You can create one-to-many relationships between tables in separate apps.  

Pros:  

-   Operates like a single application table-to-table relationships 
-   Real-time updates 
-   No additional authentication needed 
-   Quick setup 

Cons 

-   You can't edit related data in the destination, like lookups and summaries
-   Role setup can be tricky 
-   Relationships are not visible in the Parent table application 
-   Dependency results in shared system resources, limiting applications from scaling out (CPU)

Cross-app relationships work well when: 

1.  You are connecting small to medium-sized applications with light-to-moderate complexity. 
2.  You don't need to edit the data in the destination (child) table 
3.  You do need data to be immediately available on the destination table and ready for viewing on forms and reports  

### Cross-app relationships considerations 

-   Make sure that data visibility is as you expect
-   Roles and permissions can be tricky with cross-app relationships, so it is important to make sure you are securing data in the way you intend.
-   The parent table must grant the child table access and assign a role for all users in the child table. Additionally, if a user has access to both applications the role in the parent table will take precedence 

#### Document the purpose of the cross-app relationship 

-   Document why you are creating each lookup and summary field. 
-   Consider using field comments

#### Use a consistent naming connection for cross-app fields

Understanding the source of data is especially important for builders. By developing a naming convention for lookup and summary fields, a convention that indicates the data is coming from another application, you can help save a lot of time when creating or modifying reports, forms, or relationships. This convention becomes even more important as your applications grow in both size and complexity.  

#### Cross-app relationships create application dependencies

When you create a cross-app relationship, it results in the two apps sharing system resources. This sharing of system resources can become an issue when daisy-chaining apps or creating a hub-and-spoke structure with a large number of applications or a few large and complex apps. We suggest never using x-app relationships with high-complexity apps.

Learn more about creating cross-application relationships in our [table-to-table relationship help guide.](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756)

## Table-to-table imports 

You can use table-to-table imports (TTI) to move data from one table into another, within the same app or across different apps. You accomplish this by defining field mappings from a source table with fields in a destination table.  

**_Key Benefit_** \- You can replicate data from multiple sources into one table.  

Pros: 

-   It's easy to configure field mappings 
-   Large data sets execute quickly 
-   You'll be able to merge data from multiple sources 
-   Supports complex filtering criteria 
-   You set it up once and use when needed 

Cons:  

-   Data is not moved in real-time 
-   No native ability to schedule runs 
-   User creating import must have access to both tables/applications 
-   No warning when the source or destination field is deleted 
-   Application dependency results in shared system resources (CPU) 

Table-to-table imports work well when: 

1.  You need to connect small to medium-sized applications with light-to-moderate complexity. 
2.  You need to centralize data from multiple apps into one app e.g. for rollup reporting purposes. 
3.  You need to create snapshots of data for trend reporting. 
4.  You don't need the import to happen immediately when the source data changes. 

### Table-to-table imports considerations 

-   Use [API\_RunImport](https://helpv2.quickbase.com/hc/en-us/articles/4418310954772) to automate table-to-table imports
-   You configure TTIs once, but you can run them manually at any point. If you would like to set up the TTI to run at some interval, you will need to leverage the Quickbase API (API\_RunImport) using a script or an integration platform such as Workato or Zapier.  

#### Ensure data types are the same when mapping fields

When you configure the TTI, make sure that your field types for source and destination match, to prevent unwanted results. The one exception is importing a numeric into a text field, which displays the number in text form.

#### Ensure you have the correct permission levels set for the destination

Once you import the data into the destination, you view and modify the data following the same roles and permissions as data entered by a user. If your intention is for the data to be read-only/not editable, be sure to configure each role to have view-only permissions. 

#### Leverage table-to-table imports for trend reporting

Table-to-table imports allow you to configure an import to capture data over time (snapshots) for trend reporting by executing the TTI at a desired interval.  

#### Document the purpose of the TTI and the intended field mappings

You should periodically review the TTIs and ensure field mapping and filter criteria still exist and make sense. The documentation and periodic review are especially useful when multiple application managers work with the schema because field type changes and field deletions can affect the TTI. 

#### TTIs create dependencies between applications when executed

When you execute TTIs, it results in the share of system resources. This sharing of system resources can become an issue with leveraging TTIs for roll-up reporting across a large number of applications (10 or more apps, as a rule of thumb) or a few apps that are large and complex. 

**Note**: There may be situations when you need to transfer relatively big amounts of records (over 1000, or maybe as many as tens and hundreds of thousands) across your Quickbase apps and tables. See [Using Copy Records in Bulk Record Sets](https://helpv2.quickbase.com/hc/en-us/articles/18546974843156) for more information.  

Learn how to create [table-to-table imports](https://helpv2.quickbase.com/hc/en-us/articles/4570329650580).