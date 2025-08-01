## Reports that show users their own records

Often, your users don't need to see the big picture. All they want to know is what they have to do today. For this reason, Quickbase makes is easy for you to create one custom report that shows each staff member only those records that pertain to them.

How does it work? Since Quickbase knows who's logged in, you can ask the program to show or hide records based on whether or not the current user's identity matches the value in a user or list-user field. ([What's a user field?](https://helpv2.quickbase.com/hc/en-us/articles/4570360058132-Manage-Users-in-an-Application-)[What's a list-user field?](https://helpv2.quickbase.com/hc/en-us/articles/4570332253972-About-List-User-fields-)) For example, say you assign tasks by selecting a user from a field called Assigned To. Each staff member only wants to see their own tasks. So, you'll ask Quickbase to show only those records where the current user is the person listed in the Assigned To field.

To create report that shows only records that relate to the current user:

1.  [Create a new report](https://helpv2.quickbase.com/hc/en-us/articles/4570327815572-Create-a-new-report-).
    
2.  Set filtering options.
    
    In the Filters section of the report builder, select Filter records. In the dropdown field that appears, select the User field in question. Then in the next dropdown field, select **is the current user**.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572843618196/curusuer.png)
    
3.  Set other options in the report builder as desired. ([Read more about building a report](https://helpv2.quickbase.com/hc/en-us/articles/4570299978772-Creating-new-reports-from-scratch-).)
    
4.  Save the report.
    
    Click **Save** to save and display the report. This type of report is often named something like "My Open Issues" or "My Overdue Tasks" since each user who selects this report sees only their own records.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572850523412/myissues.png)
    

When you display the report, you'll see records where your name is the value in the User field that you used to set the matching criteria. When your colleague opens the same report, she'll see only those records where her name appears in that field.

Use this "current user" trick to craft reports that focus attention where it needs to be. Or, if sensitive data's at stake, create a role that uses "is current user" settings to limit access to data. [Read how](https://helpv2.quickbase.com/hc/en-us/articles/4570415966228-Create-a-Custom-Access-Rule-).

**FAQ - How do I show records where the value in a user field is NOT equivalent to the current user?**  
That report involves a small trick. When you select _**is not equal to**_ as the operator, Quickbase doesn't offer "the current user" as an additional option. However, if you click the fourth dropdown field and select **<other>**. A text box displays to the dropdown's right. Type **\_curuser\_** in this box (see illustration). If you want to match records where a value is the current user OR another user, you can also select **<other>** to type in your OR statement. [Read more about entering OR matching criteria](https://helpv2.quickbase.com/hc/en-us/articles/4570401617940-Search-for-Records-that-Match-Either-A-or-B-).

![](https://helpv2.quickbase.com/hc/article_attachments/4572850549012/not_curuser.png)