## Create a Timeline

You can create a [timeline report](https://helpv2.quickbase.com/hc/en-us/articles/4570365345172-About-Timeline-reports-) for tables that contain scheduled items, like tasks, projects or similar events. Timelines allow you to graphically represent your project schedules. You can create a timeline report for any records that have a start date and end date (typically tasks or projects).

In this topic:

-   [Understand timeline parameters](https://helpv2.quickbase.com/hc/en-us/articles/4570361669268-Create-a-Timeline#timeline_parameters)
    
-   [Group timeline reports](https://helpv2.quickbase.com/hc/en-us/articles/4570361669268-Create-a-Timeline#group)
    
-   [To create a timeline report](https://helpv2.quickbase.com/hc/en-us/articles/4570361669268-Create-a-Timeline#To_create_a_timeline_report:)
    

## Understand timeline parameters

To create a timeline report, Quickbase needs to gather information about what you want to see. In the Timeline section of the Report Builder, specify:

-   Period of time to examine
    
-   Timeline resolution—the time increments to use in the report
    
-   Milestones to highlight (optional)
    
-   Start and end dates for the event you want to track
    

### Define the start and end dates

Tell Quickbase which period of time you want to examine. Set a **Starting Date** and **Ending Date** for your timeline report.

If you make no selections here, Quickbase automatically sets the report time span for you based on the start of the earliest event included in the report and the end date of the latest event.

### Specify timeline resolution

Tell Quickbase how to break down your timeline. Timelines always measure time in two increments. You can view events by any of the following combinations:

-   week/day
-   month/week
-   quarter/month
-   fiscal quarter/month
-   year/month
-   year/quarter
-   fiscal year/quarter

The example image below shows a timeline set up as (1)year/(2)month.

![](https://helpv2.quickbase.com/hc/article_attachments/30864993822484)

When you select a resolution, Quickbase always expands the duration your timeline shows to include a full instance of the highest level time increment. For example, if you've chosen July 23 as a starting date, but selected Month/week as your resolution, the timeline will start on July 1, the beginning of the first month. Timelines must show the entirety of the highest resolution increments.

### Define your fiscal year

When you create timelines using fiscal quarter or fiscal year increments, Quickbase gives you some flexibility in how you define your fiscal year. You can:

-   Use the application's default setting – Application managers can define the fiscal year for each app by specifying the first month of the fiscal year. Once set, this default becomes the default setting for the application. If the application manager chooses not to change this setting, the first month of the fiscal year defaults to January. In either case, you have the option of using the application's setting for any timeline report you create.
    
-   Define a separate fiscal year for this report only – You can also choose to define the fiscal year for this report only. You may choose to use this setting if, for instance, the application manager did not set the fiscal year for the application. This option gives you a quick way to generate a fiscal year timeline on the fly.
    
-   You can also define whether the first or last month determines the year of the fiscal year. For example, a company's fiscal year runs from August 2023 through July 2024. If the fiscal year is based on the first month, then the fiscal year is 2023. If the fiscal year is based on the last month, then the fiscal year is 2024. You can change this setting in the application's Date/Time options. Read [set calendar options for the application](https://helpv2.quickbase.com/hc/en-us/articles/4570349355924-Application-Calendar-Options-).
    

### Choose whether you want to see milestones

If you want some tasks to display as milestones, select the **Milestone** dropdown box and select the checkbox field you use to denote a milestone. (Don't have such a field? [Read how to set up milestones](https://helpv2.quickbase.com/hc/en-us/articles/4570306502548-Setting-Up-Milestones-for-a-Timeline-Report-).)

### Select start and end fields for the task or event you want to track

Within the **Starting Field** and **Ending Field** dropdowns beneath the timeline diagram, select the fields containing dates that represent the beginning and finish of each record event you want to track. For instance, if you want your report to show the timespan between each project's start date and its end date, choose Actual Start Date for the Starting Field and Actual End Date as the Ending Field.

![](https://helpv2.quickbase.com/hc/article_attachments/30864993826452)

### Set fields to display

As you are building your timeline report, you can choose up to three fields to display in the report’s bars. Seeing these fields on the top level of your report can help provide additional context to users. To add new display fields to existing reports, simply open a timeline report’s settings and select up to three fields.

![](https://helpv2.quickbase.com/hc/article_attachments/4572846295956)

## Group timeline reports

You can group your timeline by a specific field like Company, Project or Status. [Read more](https://helpv2.quickbase.com/hc/en-us/articles/4570409135252-Sorting-Grouping-). You can even create subgroups and nest them within your highest level group.

### Create a nested timeline

Use sorting/grouping settings to create a nested timeline. For example, say you'd like to show your client how their projects fit on your staff schedule. A nested timeline can show your customer the projects and tasks you're executing for him as well as who's responsible and when it's all happening. To create a timeline like this, set three levels of grouping.

-   First, sort and group from high to low by Customer Name
-   Then sort and group from high to low by Project Name
-   Then sort and group from high to low by Assigned To

To show records in chronological order (within the final group), sort by Start Date. To show all groups in chronological order, follow the instructions to sort groups by the starting field, below.

### Sort by the Starting field

If you've created groups and want to sort them chronologically, turn on the **Sort groups by starting field** checkbox in the Sorting & Grouping section. For example, if you've created a timeline of tasks and grouped it by project, the project headings appear in alphabetical order. Turn on this checkbox, and Quickbase reorders how your projects appear in the report. The project containing the task with the earliest start date moves to the top of the list. This creates a cascade effect, as illustrated in the image below. The checkbox appears only if you've grouped records.

## ![](https://helpv2.quickbase.com/hc/article_attachments/4572839588756)  
Create a timeline report

To create a timeline report:

1.  Choose a table from the sidebar.
    
2.  Click **Reports** to open the reports panel, then click **\+ New report**.
    
3.  In the dialog, select Timeline and click Create.
    
4.  In the Filters section, [specify filter criteria](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records-).
    
5.  Specify [timeline parameters](https://helpv2.quickbase.com/hc/en-us/articles/4570361669268-Create-a-Timeline#timeline_parameters).
    
6.  Specify [sorting or grouping](https://helpv2.quickbase.com/hc/en-us/articles/4570361669268-Create-a-Timeline#group).
    
7.  Choose the columns you want to display in your report.
    
8.  Choose whether you want to include a [define a calculated column](https://helpv2.quickbase.com/hc/en-us/articles/4570272620052-Using-a-report-formula-) for your report.
    
9.  When you're done, click **Display** on the page bar to view the results of your modifications. If you don't like the results, click the **Customize** button at the top of the page to return to the report builder.
    
10.  Save the report. To do so, you will need to supply a name for the report, and whether you're saving the report as Personal (only you can view it) or Shared (others can view it). Optionally, you can also [assign the report to a group](https://helpv2.quickbase.com/hc/en-us/articles/4570407864980-Organizing-reports-).
    
    -   If you've displayed the report, you can save without returning to the report builder. To do so, go to the prompt by the report title and click **Save as**.  
        
    -   To display and save at the same time from within the report builder, click **Save**.
        
    
    **About saving Shared reports:**  
    You can only save a shared report if the manager of the application has granted you permission to do so. When you save a shared report, you don't need to allow absolutely everyone access to it. Quickbase prompts you to select the roles that should see it. To share with all application users, select **All Roles**. (An Application Manager can change which reports a particular role can access at any time. To learn how, see [Specifying Which reports a User Can Access](https://helpv2.quickbase.com/hc/en-us/articles/4570384081556-Specifying-which-reports-a-user-can-see-).) To help others understand what your report shows, type in a description. If you want the description to display above the report, turn on the **Show description on report page** checkbox.
    

### Related topics:

-   [About timeline reports](https://helpv2.quickbase.com/hc/en-us/articles/4570365345172-About-Timeline-reports-)
    
-   [Setting timeline report defaults](https://helpv2.quickbase.com/hc/en-us/articles/4570358398228-Set-Timeline-Defaults-)
    
-   [What is a report?](https://helpv2.quickbase.com/hc/en-us/articles/4570317429908-About-reports-and-charts-)
    
-   [Adding milestones](https://helpv2.quickbase.com/hc/en-us/articles/4570306502548-Setting-Up-Milestones-for-a-Timeline-Report-)
    
-   [Organizing reports](https://helpv2.quickbase.com/hc/en-us/articles/4570407864980-Organizing-reports-)