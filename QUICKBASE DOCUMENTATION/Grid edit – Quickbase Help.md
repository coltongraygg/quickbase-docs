## Grid edit

Grid Edit transforms any table report into a spreadsheet-style display that you can edit at will. You can:

-   Copy and Paste between cells
    
-   Fill Down
    
-   Directly modify multiple records at a time
    
-   Add multiple records at a time
    
-   Delete multiple records at a time
    

Tip: Anyone editing or adding lots of records usually switches to Grid Edit mode. But, if you're managing an application, you can actively use Grid Edit to create a smart and efficient data-entry experience for your end users. [Read how](https://helpv2.quickbase.com/hc/en-us/articles/4570328849812-Grid-edit#grideditreports).

To use Grid Edit to edit records:

1.  [Display a table report](https://helpv2.quickbase.com/hc/en-us/articles/4570317119252-Displaying-a-report-), such as List All.
    
2.  Click the **Grid Edit** button on the page bar ![](https://helpv2.quickbase.com/hc/article_attachments/31640522232852).
    
    Quickbase makes the entire table editable, so you can change any value directly from this report. This feature is a handy way to make changes to several records at once or to add or delete several records at a time.
    
    Note: If you don't see a **Grid Edit** button, your application manager has removed this feature from this report.
    

## Editing in Grid Edit

Double-click in any cell to change its value. Depending upon what type of field you choose, you see either a text entry area, a dropdown, or some other user-interface control that is appropriate for changing the value in that cell. Once you change a value in a cell, the background of that cell turns yellow so that you can see your modifications at a glance. Immediately after changing a cell, you can undo the change by typing Ctrl-Z or by right-clicking on the table and selecting **Undo _Action_**.

### FAQ - Why is some data colored gray?

Some columns or cells may be grayed out in Grid Edit. This is data that you cannot edit. You may not have permission to modify a particular record or a field, for example. If you double-click on the cell, Quickbase will explain why you can't edit it.

### FAQ - When I add a record in grid edit mode, the report shows additional columns that aren't included in the report. Why?

When you add records in grid edit mode, the report changes to include columns for any [required fields](https://helpv2.quickbase.com/hc/en-us/articles/4570324988692-Making-fields-required-) that are not included in the report. These columns appear on  the right side of the report.

### Selecting cells

Lots of grid-edit features (like adding multiple records at once or copying a value down all cells in a column) depend upon you selecting a group of cells.

-   Select a single cell by clicking on it.
    
-   Select a range of cells by clicking and dragging.
    
-   Select a row by clicking on the leftmost cell in the row. Drag down to select multiple rows.
    
-   Select a column by clicking its heading. Drag across to select multiple columns.
    

Tip: When you have a single cell selected, move from cell to cell using the arrow keys on your keyboard.

## Grid Edit Actions

Once you've selected the cells in question, right-click to access grid edit's handiest features. You can:

-   **Copy values.** Select a cell or multiple cells. Right-click and select **Copy** from the menu. Select the same number of cells elsewhere in grid edit. Right-click and select **Paste**.
    
-   **Clear values.** Select the cells you want to clear and press the Backspace key.
    
-   **Back out of select changes.** In grid edit, it's not too late to change your mind until you click save. If you've made some edits you regret, just select those cells again. Right-click and select **Reset to Original Values**.
    
-   **Fill Down.** As in your favorite spreadsheet program, you can save time completing or changing fields in the same column, as long as the cells are adjacent. The value in the top cell will be copied into all selected cells beneath it. Select the cells (including the cell with the value you want to copy), right-click and select **Fill Down**. If you love keyboard shortcuts, you can press Ctrl-D instead (in Internet Explorer only).
    
-   **Insert/Add multiple records**. [Read how](https://helpv2.quickbase.com/hc/en-us/articles/4570342429204-Add-Multiple-Records-at-Once-).
    
-   **Add a single record.** Add a single record in one of two ways:
    
    -   Scroll to the bottom of the list and start typing in an empty row. (Grid edit mode always features four blank lines at the bottom for new records.)
        
    -   At the top of the report, select **New**. Quickbase jumps your cursor down to the first blank row at the bottom of the list. Enter the new record in that blank row.
        
    
-   **Delete and undelete records**. [Read how](https://helpv2.quickbase.com/hc/en-us/articles/4570366549524-Delete-Multiple-Records-).
    
-   **Undo your last action.** Right-click anywhere in the grid and select **Undo _Action_** to back out of your last action. Undo doesn't depend on the current selection. It simply undoes the most recent operation.
    

### FAQ - I've made changes using grid edit, but I've changed my mind. How do I cancel the whole operation?

You can back out of individual changes using the undo and reset functions covered in the list above. To discard all your changes, just navigate away from the grid edit page. You can do so by clicking any link on the page. For example, click the application title on the upper left of the screen to return the application Home page. Quickbase will ask if you're sure you want to leave the page and, as a result, cancel your edits.

## Smart places to use Grid Edit in your application

When you're designing a Quickbase application, you can use grid edit mode to help your users enter data more efficiently.

### Create a Grid Edit report

Speed data entry tasks by creating reports that automatically display in Grid Edit mode. These reports let your users enter lots of records at once. For instance, say they need to enter multiple timecards at the end of the week. To create a tool like this, [create a new report](https://helpv2.quickbase.com/hc/en-us/articles/4570327815572-Create-a-new-report-) and make its type **Grid Edit**.

Note: Users with the _Basic Access_ access level may not create Grid Edit reports.

### Embed a Grid Edit report on a form

Often you'll want to add a parent record and related child records all at once. For instance when you create a new project, you'd like to create tasks for the project at the same time. This ability is a great feature to offer your end users. Grant this ability by embedding a report on the parent form and then make that report editable so they can edit and add related records spreadsheet-style. [Read how](https://helpv2.quickbase.com/hc/en-us/articles/4570378411412-Embedding-a-report-in-a-form-).

## Keyboard Shortcuts

If you have fast fingers, you may find these keyboard shortcuts useful in Grid Edit:

**CTRL+S** - Save. (Internet Explorer only) Saves the records that have been changed since the last save.

**ALT+Shift+S** - Save. (Firefox only) Saves the records that have been changed since the last save.

**CTRL+D** - Fill down. (Internet Explorer only) Copies the values in the topmost cell(s) into the selected cells below.

**DEL or Backspace** - Delete. Deletes the contents of the selected cells.

**CTRL+X** - Cut

**CTRL+C** - Copy

**CTRL+V** - Paste

**CTRL+Z** - Undo

### Related topics:

-   ![](https://helpv2.quickbase.com/hc/article_attachments/31640522253588 "This functionality  is not available to accounts on the Quickbase Essential plan.")[Configuring Grid Edit by role](https://helpv2.quickbase.com/hc/en-us/articles/4570365839124-Configure-Grid-Edit-)
    
-   [Enable grid edit for reports embedded within parent records](https://helpv2.quickbase.com/hc/en-us/articles/4570269916692-Edit-records-across-multiple-tables-from-a-single-form-)