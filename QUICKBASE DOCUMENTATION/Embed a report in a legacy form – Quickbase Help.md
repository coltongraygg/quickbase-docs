## Embed a report in a legacy form

You can embed a report within a form to automatically display a list of child records related to a parent record. For example, as a project manager, you could display a list of related tasks as you're viewing the project record.

**Note:** By default, embedded reports do not load until they are visible to you on the page; whether by scrolling down or by switching form tabs.

To easily create an informative display form (similar to the following image), you can embed a report within the display form.  
![](https://helpv2.quickbase.com/hc/article_attachments/31637354450452)

To embed a report:

1.  Display the form you want to embed the report on.
    
    This form must belong to a parent table. You cannot embed a report within a child record. To access a form, display a report of the table's records and click the view button (![](https://helpv2.quickbase.com/hc/article_attachments/16298393618964)) next to any record.
    
2.  Click **Customize this Form** on the page bar.
    
    The Form Builder's **Elements** tab appears.
    
3.  Add the [report link field](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-#fieldtypes) (that links to the details table) to the form.
    
    Don't know how to add form elements and work with the report builder? [Read how](https://helpv2.quickbase.com/hc/en-us/articles/4570300784788-Design-a-Form-). The report link field is easy to spot as it's usually named after the details table you want to display. Also, when you select the field, its type displays in the Form Builder's right pane.![](https://helpv2.quickbase.com/hc/article_attachments/31637354462356)
    
    _When you select the **Tasks** field on the left, Quickbase displays info and controls to the right of the form  
    __elements list, and shows the field type at the top._
    
4.  In the right-hand pane, select **Display the related records directly on the form**.
    
    This lets Quickbase know you want to show the report. If you select the other option, **Display just a link to the related records**, Quickbase would insert a link instead of a list. The link opens the report you're about to specify.
    
5.  Click the **Base the display on the report** drop-down and select the report you want to show within the parent record.
    
    You can see and edit report settings directly from this screen, if you want. To do so, select a report from the drop-down, then click the blue report link. The report opens in the report builder. DO NOT select a report set with matching criteria (filtering). Doing so means that you may not show some records that users expect to see in a list of related records.
    
6.  If you want the embedded report to display in [Grid Edit mode](https://helpv2.quickbase.com/hc/en-us/articles/4570328849812-Grid-edit-), turn on the Editable checkbox.
    
    When you make the report editable, viewers can edit child records the report contains directly on the parent form. They can also add new records without navigating to a new screen (even if the parent record has not yet been saved).  [Read more about enabling spreadsheet-style editing of an embedded report](https://helpv2.quickbase.com/hc/en-us/articles/4570269916692-Edit-records-across-multiple-tables-from-a-single-form-).![](https://helpv2.quickbase.com/hc/article_attachments/31637396063508)
    
    _An Embedded Grid Edit Report lets users edit and add records spreadsheet-style. Editable reports don't display in Grid Edit  
    mode when you merely **display** the parent record form. Like any other data-entry field on the form, embedded Grid Edit  
    reports are only editable when you're **editing** or **adding** a parent record._
    
    Note: Embedded Grid Edit reports speed data entry. But there are certain situations in which you won't want to turn this feature on. [What are they?](https://helpv2.quickbase.com/hc/en-us/articles/4570269916692-Edit-records-across-multiple-tables-from-a-single-form-)
    
7.  Set the dimensions of the embedded report.
    
    Form real estate can be valuable. If your report takes up too much room, you can limit its size in one of two ways:
    
    -   **Limit the size of the list in pixels.** Tell Quickbase how many pixels tall to make the list. When you do, the program creates a box within the form that contains the report. It features scroll bars on the bottom and right sides, which let users scroll down the list. It's almost like a window that lets viewers see and scroll through the list of records. Don't underestimate this number or you'll confuse your users who'll get a peak of a report heading with no records. A minimum of 200 pixels is usually best. But see for yourself: Enter a number and click **Preview** on the page bar to see how it looks.
        
    -   **Limit the list to a certain number of rows.** When you do so, Quickbase displays only the number of records you specify. The program adds navigation controls so users can click through all related records without leaving the form. For example, if you set the number of rows to three, Quickbase divides the list into pages of three records each. Users click page links and Quickbase show the list three records at a time.
        
8.  Tell Quickbase when the report should appear on the form.
    
    When do you want the list of child records to display? Only when the form is in display mode? Edit mode? Or both? Specify your preference by selecting one of these options within the **Display when this form is used for:** drop-down.
    

**Note:** To ensure you see the records you expect, make sure the report you insert has no [matching criteria](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records-) set. You can view or edit the report by selecting the report, then selecting the **report** link.

### Embedded reports properties

Form Properties include settings for **When there are embedded reports in the form**. The options are explained here:

-   (default) Use the app's embedded report loading behavior. This setting works in conjunction with the App Properties global setting.
    

-   Display the form, then load embedded reports afterward
    

-   Load the form, then load embedded reports, and display together
    

The Form Properties setting overrides the App Properties setting when you change the default setting of how to load embedded reports.

In App Properties, there is a global setting **Load all embedded reports on a form when the form loads** that defaults to unchecked meaning all forms in the app will load their embedded reports separately from the form (asynchronously). The App Properties setting defines the default embedded report loading behavior. We recommend leaving this setting unselected so that forms with embedded reports are optimized when loading.

The following table shows the results of the possible setting interactions between App Properties and Form Properties:

| App properties | Form properties | Result |
| --- | --- | --- |
| Unchecked | (default) Use the app's embedded report loading behavior | Reports load separately from the form |
| Unchecked | Display the form, then load embedded reports afterward | Reports load separately from the form |
| Unchecked | Load the form, then load embedded reports, and display together | Reports load with the form |
| Checked | (default) Use the app's embedded report loading behavior | Reports load with the form |
| Checked | Display the form, then load embedded reports afterward | Reports load separately from the form |
| Checked | Load the form, then load embedded reports, and display together | Reports load with the form |

### Related topics:

-   [Adding child records from within parent records](https://helpv2.quickbase.com/hc/en-us/articles/4570344338964-Adding-child-records-from-within-parent-records-)
    
-   [Adding records to multiple tables from within a single form](https://helpv2.quickbase.com/hc/en-us/articles/4570344338964-Adding-child-records-from-within-parent-records-)
    
-   [About custom forms](https://helpv2.quickbase.com/hc/en-us/articles/4570411373332-About-Custom-Forms-)
    
-   ![](https://helpv2.quickbase.com/hc/article_attachments/16298393620884 "This functionality  is not available to accounts on the Quickbase Essential plan.")[Creating custom forms](https://helpv2.quickbase.com/hc/en-us/articles/4570289798804-Create-a-Custom-Form-)
    
-   ![](https://helpv2.quickbase.com/hc/article_attachments/16298393620884 "This functionality  is not available to accounts on the Quickbase Essential plan.")[Creating dynamic form rules](https://helpv2.quickbase.com/hc/en-us/articles/4570277337876-Create-Dynamic-Form-Rules-)
    
-   ![](https://helpv2.quickbase.com/hc/article_attachments/16298393620884 "This functionality  is not available to accounts on the Quickbase Essential plan.")[Associating a custom form with reports and roles](https://helpv2.quickbase.com/hc/en-us/articles/4570330404628-Associate-a-Custom-Form-with-Roles-)
    
-   ![](https://helpv2.quickbase.com/hc/article_attachments/16298393620884 "This functionality  is not available to accounts on the Quickbase Essential plan.")[Editing a custom form](https://helpv2.quickbase.com/hc/en-us/articles/4570270668180-Edit-a-Custom-Form-)
    
-   ![](https://helpv2.quickbase.com/hc/article_attachments/16298393620884 "This functionality  is not available to accounts on the Quickbase Essential plan.")[Copying a custom form](https://helpv2.quickbase.com/hc/en-us/articles/4570376950292-Copy-a-Custom-Form-)
    
-   ![](https://helpv2.quickbase.com/hc/article_attachments/16298393620884 "This functionality  is not available to accounts on the Quickbase Essential plan.")[Deleting a custom form](https://helpv2.quickbase.com/hc/en-us/articles/4570310456084-Delete-a-Custom-Form-)