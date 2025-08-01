## Add Dependencies to an Existing Project Management Application

Often one task can't start until another finishes. If this is true of your process, you can let Quickbase track these dependencies for you, with a predecessor field. A predecessor field requires at least two work date fields to determine the start and end time for the task.

You can only have one predecessor field per table.

-   **Start Date.** Must be a **Work date** field.
    
-   **End Date.** This must be either a **Work date** field (if you want users to manually enter an end date) or a **Formula - work date** field if you want to use a separate duration field to calculate the end date.
    

**Note:** The Work date field type doesn't appear in your list of available field types until a predecessor field has been created.

To add dependencies to an app:

1.  Add a **Predecessor** field to your app and ensure it’s included on your form.
    
2.  Create or edit a start date field.
    
    If you don't yet have a start date field, create one and make its type **Work date**, or if you have an existing start date field you want to use, change its type to **Work date**.
    
3.  Create or edit an end date field.
    
    If you want users to manually enter the end date, create or edit an end date field so that its type is **Work date**.
    
    If you want to calculate an end date based on duration:
    
    1.  Add a **Formula - work Date** field.
        
    2.  In the **Formula - work Date field options** section of the properties screen, select **Use the End Date formula builder**.
        
    3.  Within the **Start date field** drop-down, choose your start date field.
        
    4.  Within the **Time span field** drop-down, select the duration field you want to use.
        
    
    Quickbase automatically calculates the end date for a task based on a five-day work week. To include weekends in the calculation, deselect the **Work week is Monday - Friday** check box.
    
4.  Configure your predecessor field.
    
    In the **Predecessor field options** section, select the start date and end date fields. Your choices are limited to Work date and Formula - work date fields.