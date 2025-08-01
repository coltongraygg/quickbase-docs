## Setting up iCalendar fields

**Note**: **iCalendar** fields have reached [End of Support](https://helpv2.quickbase.com/hc/en-us/articles/4570319163156).

Quickbase offers integration with **iCalendar**, a popular standard for exchanging scheduling information. It's a nifty way to make appointment details portable. ([Read more about iCalendar](http://en.wikipedia.org/wiki/ICalendar).)

When you add an iCalendar field to a table, your users can click an icon on Quickbase forms or reports to download a set of basic appointment information. It all travels as a package: subject, time, location—whatever fields you want to make portable. Users can save this information to disk as an .ics file ([read more about this format](http://filext.com/file-extension/ICS)) or they can use a program like Outlook to open and save it in their own calendar. When you email a record that contains an iCalendar field or that record is included in an email notification, Quickbase sends the .ics file as an attachment the recipient can save to their calendar.

### FAQ - Why is the time in my app's record different than the time that shows up in my Microsoft Outlook calendar?

Quickbase and Outlook communicate on time zones, which may result in this kind of discrepancy. For example, if your company headquarters are in California but you're in New York, your [Quickbase billing account's time zone](https://helpv2.quickbase.com/hc/en-us/articles/4570272928660-Set-the-Time-Zone-for-Both-the-Application-and-the-Account-) is probably set to Pacific Time. Quickbase passes this information onto Outlook and Outlook automatically adjusts the time to Eastern Standard Time for you. That means if the appointment begins at 10am in Quickbase, that time translates to 1pm in your Outlook calendar.

###### To add an iCalendar field:

To get this working, you'll follow the steps below to add an iCalendar field to your Tasks or Appointments table (wherever you store scheduling information) and configure it to draw details from fields in that table. Once you do so, the field lets you send that information on the road. You can export it into your Outlook calendar or email it to a colleague.

1.  Open the application which should feature the iCalendar field.
    
2.  From the table containing the field you want to change, click **Settings** in the Page bar.
    
3.  Click **Fields**, then click the ![](https://helpv2.quickbase.com/hc/article_attachments/20330189889684) button to create the iCalendar field.
    
4.  Name the field and set the field type.
    
    In the **Field Label** box, type a name for the field (_iCalendar_ is a good name) and then from the type dropdown, select **iCalendar**. Click **Add**. When Quickbase prompts you to add the field to forms you'll probably want to do so. That way, users can access this new feature. (You can add it to reports later.)
    

Now you must configure the field to collect the information you want.

To configure the iCalendar field:

1.  [Open the iCalendar field's properties page](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-).
    
2.  Associate iCalendar fields with corresponding fields from your table.
    
    The iCalendar feature contains fields, just like your application table does. You must match up your scheduling information fields with iCalendar's fields. That way, the iCalendar knows what fields to extract and group into its portable format and also what to call them.
    
    In the **iCalendar field options** section, click each dropdown and select a field from your table that contains the corresponding information. You'll notice that not all fields are available. That's because each iCalendar field can only handle certain data types:
    
    -   In iCalendar's **Subject** dropdown, select a Text field from your Quickbase table.
        
    -   iCalendar **Location** and **Description** fields can take values from any Text field.
        
    -   Match iCalendar's **Starting time** and **End time** fields with Date/Time fields in your table. For example you may have a field called **Start** and/or **Calculated Finish Date**. You can also select Date and Work Date fields from these dropdowns as well as Formula - Date, Formula - Work Date, and Formula - Date/Time fields. When you use Date or Work Date fields and send the .ics file to Microsoft Outlook or another scheduling program, the outside program treats these fields as all day events.
        
    
    Note: Even though these iCalendar fields have the word _time_ in the label, you can't link them to a Quickbase Time of Day field type. Time of Day fields are missing vital information that iCalendar needs to know when something is happening—namely, the DATE. That's why these fields require Date/Time values. Or, simple Date values will suffice as well.
    
    If you don't want to include a field from your table, don't select it. iCalendar won't know it exists. But, you MUST make a selection in any field with a red asterisk (\*).
    
3.  After you've matched up all the fields, click **Save**.
    

### FAQ - Can I draw my iCalendar field into another table by making it a lookup field?

The iCalendar field will work as a lookup field. Say you want to add the iCalendar field to appear next to your Task table's **Related Project** field, so users can easily send or copy the project schedule. To get it there, [create a lookup field](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-) that displays in Tasks. The iCalendar field functions the same way when it's a lookup field. Users just need to click the icon to open or download scheduling information.

**When you're done, don't forget to add the new iCalendar field to your forms and reports.**

### Related topics:

-   [What is iCalendar?](http://en.wikipedia.org/wiki/ICalendar)
    
-   [Setting up a vCard field in Quickbase](https://helpv2.quickbase.com/hc/en-us/articles/4570136812820-Set-Up-a-vCard-Field-)
    
-   [Creating lookup fields](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-)
    
-   [Edit a report](https://helpv2.quickbase.com/hc/en-us/articles/4570281029396-Edit-a-Report-)