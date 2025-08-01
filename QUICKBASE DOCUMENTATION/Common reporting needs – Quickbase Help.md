Quickbase allows you to create custom reports in a variety of formats for your application. Common reporting needs include:

-   [Creating reports that contain data from more than one table](https://helpv2.quickbase.com/hc/en-us/articles/4570331765012-Common-reporting-needs#report_across_tables)
    
-   [Summarizing data](https://helpv2.quickbase.com/hc/en-us/articles/4570331765012-Common-reporting-needs#summary_reports)
    
-   [Reporting on project status and resources](https://helpv2.quickbase.com/hc/en-us/articles/4570331765012-Common-reporting-needs#report_projects)
    
-   [Creating reports that shows a user their own tasks](https://helpv2.quickbase.com/hc/en-us/articles/4570331765012-Common-reporting-needs#individual_reports)
    
-   [Creating user-defined reports](https://helpv2.quickbase.com/hc/en-us/articles/4570331765012-Common-reporting-needs#user_defined_reports)
    

## Creating reports that contain data from more than one table

You can create reports that contain data from more than one table by using either:

-   [Relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570331765012-Common-reporting-needs#relationships) (the most precise method)
    
-   [Report link fields](https://helpv2.quickbase.com/hc/en-us/articles/4570331765012-Common-reporting-needs#report_links) (a more informal method for linking loosely associated records)
    

### Reporting on data from multiple tables using relationships

The best and most precise way to access data from more than one table in your application is to [create a relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-). A relationship is a link between two [tables](https://helpv2.quickbase.com/hc/en-us/articles/4570326161428-What-Is-a-Table-) (similar to a join command in SQL). You usually link tables in a one-to-many relationship, where a single record in a **parent** table links to multiple records in a **child** table. For example, you have a Project Management application with three tables: Projects, Tasks, and Issues. You create a relationship in which Projects is the parent table and Tasks is the child table, because each project has multiple tasks. You create another relationship in which Tasks is the parent table and Issues is the child table, because each task has multiple issues. When you create a relationship between tables, you designate a field with which to link them. This field is called a **reference** field. "Reference" is not a field type, but an attribute of a field. A reference field in the child Tasks table lets you select which parent Project record to associate with a Task.

Data always flows down from the parent table to the child table in a relational database, like Quickbase. In the Project Management application, the data flow is Projects > Tasks > Issues. You include [lookup fields](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-) in the child table to pull information down from related parent table records. Lookup fields can pass all types of data, including text. You could include lookup fields in the Tasks table to pull in the related "Project Name" and "Project Manager" from the Projects table. To create a report that contains text data values from both tables, you must create that report on the child table.

You also can include [summary fields](https://helpv2.quickbase.com/hc/en-us/articles/4570321780372-Creating-a-summary-field-) in the parent table to pull certain information up from the child table; however, summary field do not pull specific text values up from the child table. Summary fields perform functions such as giving you a count of the number of child records tied to a specific parent record, or giving you the maximum value in a numeric or date field across all your child records. Summary fields can be exported and used in formulas. Once you create a summary field in the parent table, you can pass the value of the field down to the child table using a lookup field.

It may be useful to map out your tables' relationships so you can see how the flow occurs and then create your reports accordingly.

Note that at the form level, you actually can view specific information from the child table on an individual parent record.  It's called an [embedded report](https://helpv2.quickbase.com/hc/en-us/articles/4570378411412-Embedding-a-report-in-a-form-). However, you need to create reports to view information for multiple parent records, and you should create those reports on the lowest level child table.

### Reporting on data from multiple tables using report link fields

Creating a relationship is usually the best way to link records from multiple tables. However, there are some cases in which you might not need the precision of a relationship and simply can [create a report link field](https://helpv2.quickbase.com/hc/en-us/articles/4570342656148-Create-Links-between-Tables-) instead. A report link field is great for matching records with a loose connection—where one record may or may not contain a value from a field in another table. Instead of you and your users connecting records in separate tables (by selecting the related item from a dropdown list), Quickbase make those connections on its own automatically. For example, say you have a customer feedback table where you store comments submitted to your web site's suggestion box. In the midst of the "comments" field they may mention one or several of your products. A report link field enables Quickbase to search the comments field for mentions of each product name and have a link in your product record open all relevant feedback records.

## Summarizing data

Summary reports help you make sense of data from a large number of records in a table. You can [sort and group](https://helpv2.quickbase.com/hc/en-us/articles/4570409135252-Sorting-Grouping-) summary reports to specify which records should appear first, how all records should be ordered, and whether like records should be grouped together.

If you have multi-dimensional data to display, you can group by more than one field using a summary report with **crosstabs** (short for cross tabulation). [Summary Crosstab reports](https://helpv2.quickbase.com/hc/en-us/articles/4570366660372-About-Summary-and-Crosstab-Reports-) are much more flexible in terms of table design because they let you group records in rows or columns. This approach gives you added power—literally another dimension in which to display information. [Read more about summary reports](https://helpv2.quickbase.com/hc/en-us/articles/4570366660372-About-Summary-and-Crosstab-Reports-) for a good example of when to use summary and summary crosstab reports, and how to create them.

Note that while summary and table reports calculate totals and averages for you, these values do not actually exist in fields within Quickbase. If you export the report data, the total/average data is not exported. You also cannot use this report-calculated summary data in formulas. Data must exist in a field to be exported and used in formulas. You can create [summary fields](https://helpv2.quickbase.com/hc/en-us/articles/4570321780372-Creating-a-summary-field-) in the parent table to store total, average, and other summary data from related child records. You can include the summary fields when you run reports on a parent table, and if you export the report the summary field data is exported. You also can pass the value of the summary fields down to the child table using a [lookup field](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-) if you want to use the data in child table formulas, include it in child table reports, or export it from the child table.

### Summarizing data by day, week, month, or quarter

Are you managing a project and want to see all tasks that will complete each day, week, month, or quarter? Or perhaps you are managing sales and want to see what payments are due per month. Quickbase allows you to group summary reports by different increments of time (days, weeks, months, quarters, fiscal quarters, years, fiscal years, and even decades).

Specify this type of grouping when you create a summary report by selecting the appropriate field (such as Calculated Finish Date or Payment Due Date) in the Group by dropdown and selecting the appropriate time period in the Combine dropdown, shown below:

![](https://helpv2.quickbase.com/hc/article_attachments/4572828839060)

## Reporting on project status and resources

Common project management reporting needs include:

-   [Task assignments](https://helpv2.quickbase.com/hc/en-us/articles/4570331765012-Common-reporting-needs#task_assignment)
    
-   [Task status](https://helpv2.quickbase.com/hc/en-us/articles/4570331765012-Common-reporting-needs#task_status)
    
-   [Workflow management](https://helpv2.quickbase.com/hc/en-us/articles/4570331765012-Common-reporting-needs#workflow)
    

### Reporting on task assignments

You can run reports to show you the tasks assigned to each person on your project team. You can accomplish this in a variety of ways. For example, your Project application contains a parent Tasks table and a related child Resources table. Each Task record contains an "Assigned to" field that specifies which Resource is assigned to the task. You could create the following kinds of reports on the Tasks table:

-   A [summary report](https://helpv2.quickbase.com/hc/en-us/articles/4570366660372-About-Summary-and-Crosstab-Reports-) in which you set the Summarize dropdown to "# of Tasks" and Group by to "Assigned to". The resulting report contains the number of tasks assigned to each resource, and you can click the resource's name to see a list of thier tasks.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572820548244)
    
-   A [table report](https://helpv2.quickbase.com/hc/en-us/articles/4570394832916-About-Table-reports-) which you sort by the "Assigned to" field. The resulting report contains a list of tasks sorted alphabetically by resource name.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572813564948)
    
-   A [timeline report](https://helpv2.quickbase.com/hc/en-us/articles/4570365345172-About-Timeline-reports-) in which you set Sort & group to sort or group on the "Assigned to" column. The resulting report contains a timeline of project tasks grouped by resource name.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572834994708)
    
-   A line or bar [chart report](https://helpv2.quickbase.com/hc/en-us/articles/4570319468308-About-Chart-reports-) in which you view "Assigned to" resources on the **x-axis** and "# of Tasks" on the y-axis. You can then click any point or bar to view a list of tasks assigned to that resource.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572820598036)
    
-   A pie [chart report](https://helpv2.quickbase.com/hc/en-us/articles/4570319468308-About-Chart-reports-) in which you set the Series to "Assigned to" and the Data Values to "#of Tasks". You can then click any section of the pie to view a list of tasks assigned to that resource.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572841789076)
    

### Reporting on task status

You can easily create a report to view the status of your project's tasks. For example, your Project application contains a Tasks table that has a multiple-choice text field for status (Not Started, In Process, Complete, and Blocked). If you run a [table report](https://helpv2.quickbase.com/hc/en-us/articles/4570394832916-About-Table-reports-) on the Tasks table in which you specify to sort data by the "Status" field, you will see a list of all tasks sorted alphabetically by status.   

You can also create reports that show you only tasks of a particular status, such as a report of only Blocked tasks. [Read more about filtering records that display in reports](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records-).

Quickbase also enables to color code tasks by status, priority, due date, etc. to get the big picture at a glance. In the example below, the project manager has created report of overdue tasks (tasks whose Status is not Complete and whose Calculated Finish Data is earlier than today). The project manager has enabled row colorization to show high priority overdue tasks in red, medium priority overdue tasks in yellow, and low priority overdue tasks in green. Report users can quickly see where to focus attention and apply additional resources.

![](https://helpv2.quickbase.com/hc/article_attachments/4572848835220)

[Read more about using row highlighting (colorization)](https://helpv2.quickbase.com/hc/en-us/articles/4570391002260-Color-coding-in-reports-).

### Using reports to manage workflow

Are multiple people in your project responsible for completing different parts of the same task? If so, Quickbase reports can help you manage your project's workflow. After you implement this workflow solution, tasks flow automatically from one person's "to do" report to the next person's report when the first person completes their part of the task.

For example, maybe your marketing copy needs to go through an approval process that involves four different people. When the first person approves the marketing copy, it automatically appears on the next person's "to do" report. Or perhaps you have a developer who fixes software bugs and a quality assurance tester who confirms the fix. When the developer fixes a bug, it automatically appears on the quality assurance tester's "to do" report.

Read [how to manage workflow with user fields and reports](https://helpv2.quickbase.com/hc/en-us/articles/4570317178132-Manage-Workflow-with-User-Fields-and-reports-).

## Creating reports that users their own tasks

If you have created an application to manage projects and/or tasks, your users often want to see those tasks to which they are assigned. For this reason, Quickbase makes is easy for you to create one custom report that shows each staff member only those records that pertain to them.

How does it work? Since Quickbase knows who's logged in, you can ask the program to show or hide records based on whether or not the current user's identity matches the value in a user or list-user field. ([What's a user field?](https://helpv2.quickbase.com/hc/en-us/articles/4570360058132-Manage-Users-in-an-Application-)  [What's a list-user field?](https://helpv2.quickbase.com/hc/en-us/articles/4570332253972-About-List-User-fields-))

Read [how to create reports that show users their own records](https://helpv2.quickbase.com/hc/en-us/articles/4570327941524-Reports-that-show-users-their-own-records-).

## Creating user-defined reports

Are you are creating many slightly different reports based on individual user's needs? If so, you may want to create a single report that prompts users for selection criteria for one or more fields.

For instance, you have three project task reports: one for open tasks, another for in progress tasks, and a third for closed tasks. Instead, you could create a single report that prompts a user to select the task status.

Or, you have an application that manages contact information for companies and find yourself creating reports to display contact information for individual companies. Instead, you could create a single report that prompts a user to select the company whose contact information they want to view, as shown below.

![](https://helpv2.quickbase.com/hc/article_attachments/4572848859540)

[Read how to create a report that prompts users for selection criteria](https://helpv2.quickbase.com/hc/en-us/articles/4570432732948-Create-a-Report-that-Prompts-Users-for-Selection-Criteria-).

### Related topics:

-   [Plan your application's structure](https://helpv2.quickbase.com/hc/en-us/articles/4570261820180-Planning-your-app-s-structure-)
    
-   [Creating a new report](https://helpv2.quickbase.com/hc/en-us/articles/4570299978772)
    
-   [Displaying a report](https://helpv2.quickbase.com/hc/en-us/articles/4570317119252-Displaying-a-report-)
    
-   [About table reports](https://helpv2.quickbase.com/hc/en-us/articles/4570394832916-About-Table-reports-)
    
-   [About summary and crosstab reports](https://helpv2.quickbase.com/hc/en-us/articles/4570366660372-About-Summary-and-Crosstab-Reports-)
    
-   [About calendar reports](https://helpv2.quickbase.com/hc/en-us/articles/4570298652052-About-Calendar-Reports-)
    
-   [About chart reports](https://helpv2.quickbase.com/hc/en-us/articles/4570319468308-About-Chart-reports-)
    
-   [About timeline reports](https://helpv2.quickbase.com/hc/en-us/articles/4570365345172-About-Timeline-reports-)
    
-   [Specifying which reports a user can see](https://helpv2.quickbase.com/hc/en-us/articles/4570384081556-Specifying-which-reports-a-user-can-see-)
    
-   [Reports that show current user thier own records](https://helpv2.quickbase.com/hc/en-us/articles/4570327941524-Reports-that-show-users-their-own-records-)
    
-   [About row colorization](https://helpv2.quickbase.com/hc/en-us/articles/4570391002260-Color-coding-in-reports-)