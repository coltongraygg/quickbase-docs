## Creating many-to-many relationships

A [relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-) between tables is usually one-to-many, where one record in the parent table relates to many records in the child table. For example, one project has many tasks. But what if you have a many-to-many scenario, such as students and classes, where you need to assign many students to many classes?

To accomplish this, you can add a third table that acts as a go-between, and handles all the possible combinations involved.

Tips:

-   **Testing the scenario:**: You can test out the steps below to make sure it's what you want. To do so, [make a copy of your application with data](https://helpv2.quickbase.com/hc/en-us/articles/4570366892692), then follow the instructions below to see if this solution is the one you're looking for. If you like the way it works in the copy, make the same changes to your live app.
    
-   Carefully plan projects, resources, and tasks: Lots of project managers ask Quickbase how to create a many-to-many relationship between resources and tasks. But before you set up your project management application to assign multiple users to a task, ensure you consider what a task is and who is actually in charge of completing it. Can the job be broken down into individual tasks that each person completes? Sometimes, a many-to-many relationship may be more complex than you need for your app, and a one-person-to-many-tasks set up may be preferable.
    

To create a many-to-many relationship:

1.  Create a new table to serve as the intermediate table.
    
    [Add a new table](https://helpv2.quickbase.com/hc/en-us/articles/4570404266004-Adding-new-tables-) to your application and give it an appropriate name. For example, if you are connecting students and classes, you may have an _Assignments_ table.
    
2.  [Create a relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-) between the new table and the existing tables.
    
    Create two relationships. The new, intermediate table should be the child table to each previously existing table. In other words, the new table is the "many" in a one-to-many relationship with both existing tables.
    
3.  Add lookup fields to the relationship.
    
    For example, you may want the Assignments table to display the class description and instructor name from the Classes table. The more information you draw into your new table, the more useful it is—not just for creating assignments, but also for creating reports and charts, because all your reporting will be based on the intermediate table from this point forward.
    
4.  Delete unnecessary fields from parent tables.
    
    If there are fields in the existing tables that track information that's now in the new intermediate table, you'll want to [delete those fields](https://helpv2.quickbase.com/hc/en-us/articles/4570367639316-Deleting-a-field-), for example, a Class field in the Students table that you'll no longer use.
    
5.  Create automated email notifications for the new table.
    
    If you have email [notifications](https://helpv2.quickbase.com/hc/en-us/articles/4570363594260-About-Record-Change-Notifications-), [subscriptions](https://helpv2.quickbase.com/hc/en-us/articles/4570276923156-About-Report-Subscriptions-) or [reminders](https://helpv2.quickbase.com/hc/en-us/articles/4570363377300-About-Reminders-) set up, you may need to replicate these on the new table. For example, if your Students table notified a person when you assign them to a class, you need to create that notification for your intermediate table (Assignments) because that's where you now make class assignments. ([Read more about automated emails](https://helpv2.quickbase.com/hc/en-us/articles/4570337442324-About-Automatic-email-).)
    

## Using the many-to-many relationship

Now, whenever you want to add information that links your two original tables, you do so by adding a record to the new table. For example, if you want to sign a student up for a course, you'd add a new record to the Assignments table. Within the new record, select the class and select the student. To assign multiple people to one class, create multiple records in the assignments table—one for each combination of person and class. Quickbase makes this easier by adding an **Add Assignments** button to each parent table. From within a Class record, you can click the **Add Assignments** button to assign a person to that class. You can do the same from within a Student's record. The button adds a new record to the Assignment table that joins a Student and a Class.

You should do most of your reporting from within the new table. For instance, say you want to see a list of everyone in a particular class so you can send them an email. [Create this report](https://helpv2.quickbase.com/hc/en-us/articles/4570327815572-Create-a-new-report-) within the Assignments table.

After you create a new table, you may need to edit access permissions to its contents. [Read about permissions](https://helpv2.quickbase.com/hc/en-us/articles/4570403703316-Set-Up-Access-Permissions-). If you change the structure of your application, you may need to change your approach to permission settings. For example, you may want students to see only their own class assignments, and not all assignments, and so you may want to limit access based on a user's relationship to each record. [Read how to implement this kind of access rule](https://helpv2.quickbase.com/hc/en-us/articles/4570340960276-Manage-User-Access-Based-on-a-User-s-Relationship-to-Application-Content-).

Note: Do you need to hide information from your users or are you just trying to focus their attention on the information that interests them? If it's a question of security, set access permissions. If you just want to make your application easier to use, don't set permissions, create custom [reports](https://helpv2.quickbase.com/hc/en-us/articles/4570317429908-About-reports-and-charts-) instead. Not sure what to do? [Read more](https://helpv2.quickbase.com/hc/en-us/articles/4570277017492-About-Data-Access-and-Security-).

### Related topics:

-   [About table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-)
    
-   [Creating table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-)
    
-   [Adding a Table](https://helpv2.quickbase.com/hc/en-us/articles/4570404266004-Adding-new-tables-)
    
-   [Creating lookup fields](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-)
    
-   [Setting access permissions](https://helpv2.quickbase.com/hc/en-us/articles/4570403703316-Set-Up-Access-Permissions-)
    
-   [Limit access based on a user's relationship to data](https://helpv2.quickbase.com/hc/en-us/articles/4570340960276-Manage-User-Access-Based-on-a-User-s-Relationship-to-Application-Content-)
    
-   [Embedding a report within a form](https://helpv2.quickbase.com/hc/en-us/articles/4570378411412-Embedding-a-report-in-a-form-)