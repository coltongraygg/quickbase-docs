Quickbase may seem to be a static collection of tables and fields. In reality, Quickbase is a dynamic task master, dispatching tasks and passing issues from person to person—nudging users to finish their assignments or reminding them to start. For example, maybe your marketing copy needs to go through an approval process that involves four different people. Or perhaps you have a developer who fixes software bugs and a quality assurance tester who confirms the fix. The solution you'll read about in this topic helps you handle any scenario in which multiple people are responsible for completing different parts of the same task.

Imagine that you run a doll repair shop. A damaged doll goes through several different processes (and departments) on the road to restoration. First, the doll goes to a body work expert who repairs physical damage (a lost head, missing eyes and so on). Then, the doll moves on to a painter for cosmetic improvements. Finally, it needs to be examined by the Quality Control department.

Quickbase can keep the doll moving along the repair assembly-line. For instance, how does the painter know what doll to work on? Simple. They open Quickbase and there's the doll on their daily "to do" list. How did it get there? Read on to find out.

## Step 1: Create User fields

Since you want to assign jobs to individuals, those people must exist in your Quickbase application. You can use your application's list of users to populate a field for this purpose. Not surprisingly, these fields are called [User fields](https://helpv2.quickbase.com/hc/en-us/articles/4570360058132-Manage-Users-in-an-Application-) or [List-User fields](https://helpv2.quickbase.com/hc/en-us/articles/4570332253972-About-List-User-fields-) and Quickbase automatically fills them with the list of users on your application (though you can [decide exactly who should appear in the list](https://helpv2.quickbase.com/hc/en-us/articles/4570277291284-About-User-Fields-#defaultset)). So, the first step is to make sure that you've [shared your application](https://helpv2.quickbase.com/hc/en-us/articles/4570349592852-Sharing-apps-with-other-users-) with the staff and also that they appear in user lists.

Since a repair job moves through three departments and therefore three different people handle each process, the doll repair shop added three User type fields. For example, say that a damaged doll comes in for repair. The shop owner assigns it to a body work expert by selecting a staff member from the **Body work assigned to** user field dropdown. The owner also clicks the **Painter** user field dropdown and assigns a painter. Finally, they select a third staff member from the **Quality Control Checker** list.

Figure out what parts comprise your process and [add each field](https://helpv2.quickbase.com/hc/en-us/articles/4570374838292-Adding-new-fields-) you need, selecting User as the field type.

## Step 2: Create a status field

User fields can't do it on their own. Staff at the Doll Hospital also need to know where a particular repair job is in the repair process. For this purpose, they've added a field called **Status** to track the doll's progress. Choices in this field are: **Body Repair**, **Painting**, **Quality Check** and **Completed**.

Create your own status field: [add a field](https://helpv2.quickbase.com/hc/en-us/articles/4570374838292-Adding-new-fields-), selecting Text - Multiple choice as the field type. Populate this field with the status choices that fit your process.

## Step 3: Add the fields to forms

If you didn't do so when you created the User fields and status field, add these fields to the table's forms. ([Read how](https://helpv2.quickbase.com/hc/en-us/articles/4570300784788-Design-a-Form-).)

## Step 4: Create a report that shows each user their open tasks

Once your user and status fields are set up, you can use them to move tasks down an assembly-line. To do so, you'll make jobs move from one person's "to do" list onto the next person's list. The "to do" list is really a [Quickbase report](https://helpv2.quickbase.com/hc/en-us/articles/4570317429908-About-reports-and-charts-) that sets specific matching criteria on values in the user fields and the Status field.

[Create a report](https://helpv2.quickbase.com/hc/en-us/articles/4570327815572-Create-a-new-report-) and name it something like _My open assignments_. Everyone will access this one report, but what each person sees in that report will be different.

First, decide who should see what. For example, in the doll repair assignments list, a record should display in this report if it meets the following conditions:

-   status is **Body Repair** and current user is listed in **Body work Assigned To** field.
    
-   status is **Painting** and current user is listed in the **Painter** field.
    
-   status is **Quality Check** and the current user is listed in the **Quality Control Checker** field.
    

If you were dealing with only one of these conditions, you could simply enter it within the Filtering section of the report builder. However, because there are many different possible combinations, you need to [create a custom column and use a Quickbase formula](https://helpv2.quickbase.com/hc/en-us/articles/4570272620052-Using-a-report-formula-) to tell the program what to do in each situation.

To create a calculated (formula) column and use a Quickbase formula:

1.  Within the **Columns** section, click the **Custom columns** radio button.
    
2.  Turn on the **Define a calculated column** checkbox
    
3.  Type in a Column label.  
    This label will appear as the column heading.
    
4.  Click the Type dropdown and select **Checkbox**. All these field types are Formula fields, even though they don't explicitly say so. (After all, you're creating a formula column.)
    
5.  Write the formula in the Formula box. Model your formula on the example below.    
    The formula that keeps dolls moving along is the following:  
    If(((\[Body Work Assigned To\] = User()) and (\[Status\] = "Body Repair")) or  
    ((\[Painter\] = User()) and (\[Status\] = "Painting")) or  
    ((\[Quality Control Checker\] = User()) and (\[Status\] = "Quality Check")), true, false)  
    This formula says that if any of the three conditions are met, then turn on the custom column's checkbox field. [Read more about Quickbase Formulas](https://helpv2.quickbase.com/hc/en-us/articles/4570376002580-Using-Formulas-in-Quickbase-).
    
6.  Once you've created the custom column, you need to put it to work in the report. To do so, go to the **Filters** section of the report Builder. Click Filter records. From the Select a field dropdown select **<Custom Column>**. In the second dropdown select **is**, and in the third select **True**. Here you're telling Quickbase to display the job only if the checkbox is turned on—in other words a condition in the formula is met. That's how you get a repair job to appear on a user's list only if they're listed in the user field that matches the appropriate status.
    
7.  Don't forget to save your changes.
    

But what happens when a doll doesn't pass quality control? For instance, say a doll needs to return to the painter for some touch-ups. To handle this scenario, you'd create two additional status choices: **Re-opened for Body Repair** and **Re-opened for Painting**. When you fold them into the calculated column formula, the formula would look like this:

If(((\[Body Work Assigned To\] = User()) and (\[Status\] = "Body Repair" or \[Status\] = "Re-opened for Body Repair")) or  
((\[Painter\] =User()) and (\[Status\] = "Painting" or \[Status\] = "Re-opened for Painting")) or  
((\[Quality Control Checker\] = User()) and (\[Status\] = "Quality Check")), true, false)

Tip: Take this report even further. [Create an email subscription](https://helpv2.quickbase.com/hc/en-us/articles/4570283676052-Create-a-Report-Subscription-) that automatically emails the report to your staff members on a weekly or daily schedule. They won't even need to log into Quickbase to see a list of open assignments.

### Related topics:

-   [Share an application with others](https://helpv2.quickbase.com/hc/en-us/articles/4570349592852-Sharing-apps-with-other-users-)
    
-   [Managing Users in an Application](https://helpv2.quickbase.com/hc/en-us/articles/4570360058132-Manage-Users-in-an-Application-)
    
-   [What is a report?](https://helpv2.quickbase.com/hc/en-us/articles/4570317429908-About-reports-and-charts-)
    
-   [Using Formulas in Quickbase](https://helpv2.quickbase.com/hc/en-us/articles/4570376002580-Using-Formulas-in-Quickbase-)