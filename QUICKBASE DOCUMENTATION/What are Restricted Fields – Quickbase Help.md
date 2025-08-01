## What are Restricted Fields?

There may be times when you want to share your application with many users, but limit access to certain fields. For example, say you want all your employees to access most of the information in your human resources application, but not the Salary field. In addition, maybe you'd like to grant the HR department the ability to see this field, but only grant the HR Manager the power to edit it.

It's easy to exclude special fields from view and/or modification. As with any access restrictions, you'll use [roles](https://helpv2.quickbase.com/hc/en-us/articles/4570323434516-About-Roles-) to [restrict access](https://helpv2.quickbase.com/hc/en-us/articles/4570355458836-Configure-Permissions-for-a-Role-#field_restrict) to a field. To do so, you specify what level of access users in a particular role should have to the field. Quickbase lets you choose from three access settings: **None**, **View** or **Modify**.

## "None" Access

When you grant None to a particular role, users in that role face the following limitations:

-   The field won't appear in any reports.
    
-   The field won't appear in record change notifications  
    The exception to this rule is if the field is included in an "open" notification. See [About Record Change Notifications](https://helpv2.quickbase.com/hc/en-us/articles/4570363594260-About-Record-Change-Notifications-) to learn more about notifications and their permissions.
    
-   The field won't display on forms.
    
-   Quickbase excludes the field when a user in that role exports data.
    

### How restricted fields affect reports

When users in a role are restricted from accessing a particular field, those users can usually view reports that contain the restricted field; they’ll be able to view all data except the field that is restricted.

However, reports that  filter,group, or sort data using a restricted field will NOT be available to users who are not allowed access to the field.

In the example mentioned above, the Salary field in the Employees table is a restricted field;  users in the role Employee are not allowed to access this field.

If you have created a report that either filters, groups, or sorts employee records by Salary, users in the role Employee will not be able to access the report.  Unless you’ve turned off the report for that role in the [Roles and Reports Matrix](https://helpv2.quickbase.com/hc/en-us/articles/4570384081556-Specifying-which-reports-a-user-can-see-), the report will be listed in the reports listing for the table; however, when a user tries to access the report, Quickbase denies access to the report.

## "View" Access

Granting View access always grants the ability to see the data, but not to edit it. Quickbase allows exporting the field's contents when a user in that role exports data.

## "Modify" Access

Anything goes when a user has this level of access. A user can see, edit and delete values in the field. Modify access is the automatic setting for a field, unless you tell Quickbase otherwise.

## Things to know

When setting up restricted fields, the following rules apply:

-   Application managers don't automatically have access to restricted fields. If you need access to a restricted field, you must make sure that you grant field access to the role you're in.
    
-   Restricted field access permissions cannot override record level permissions.
    
    For example, if you've granted **View All Records** access to a user's role, and you give that same role **View/Modify** access to a particular field, then the user has only View access to the restricted field and won't be able to modify its content.
    
-   Users whose access you've blocked may still see the names of restricted fields displayed in dropdown lists and other areas. However, they cannot view the data in these fields.
    

For instructions on how to set up restricted fields, see [Setting Up Restricted Fields](https://helpv2.quickbase.com/hc/en-us/articles/4570278329620-Set-Up-Restricted-Fields-).

### Related topics:

-   [Setting Up Restricted Fields](https://helpv2.quickbase.com/hc/en-us/articles/4570278329620-Set-Up-Restricted-Fields-)
    
-   [View a list of users who have access to restricted fields](https://helpv2.quickbase.com/hc/en-us/articles/4570361366548-View-Users-With-Access-to-Restricted-Fields-)