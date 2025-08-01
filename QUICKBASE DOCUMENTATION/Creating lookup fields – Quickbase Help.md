## Creating lookup fields

You may need to create a report that includes information from two different tables. First you [create a table-to-table relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-) between the tables, then to draw many values from the different tables together, you can need to enhance the relationship with **_lookup fields_**.

You can create lookup fields:

-   [By editing table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields#lookup_fieldstab)
    
-   [From within reports](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields#lookup_inview)
    
-   [From the Report Builder](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields#lookup_view)
    

## Creating lookup fields by editing table-to-table relationships

You must have an existing [relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-), or [create a relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-) between two tables.

1.  Open the app that contains the relationship you want to enhance with lookup fields.
    
    If you created a relationship between tables in two different apps (a cross-app relationship), open the application that contains the child table.
    
2.  Open the table.
    
3.  Select **Settings**, then click **Table-to-table relationships**.
    
4.  Select the relationship that you want to edit. The relationship properties appear:
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572802120084/editrelationship.png)
    
5.  Select **Add Lookup Fields** at the bottom of the **Child Table**. A **New Lookup Fields** page appears.
    
6.  On the New Lookup Fields page, select up to three lookup fields from the parent table that you want to display in the child table.
    
7.  Select Create to save your changes.
    
    To add more lookup fields, repeat the previous two steps.
    

Note: When you add a lookup field from within the Relationships list, it doesn't automatically appear on reports or forms. You'll need to add it yourself by [editing reports](https://helpv2.quickbase.com/hc/en-us/articles/4570281029396-Edit-a-Report-) or [customizing forms](https://helpv2.quickbase.com/hc/en-us/articles/4570300784788-Design-a-Form-).

## Creating a lookup field from within a report

**Note**: This feature only exists in the legacy version of table reports.

Often you've displayed a report and you want to add a column of information to it.

To create a lookup field from within a report (and add it to the report):

1.  Select the ![](https://helpv2.quickbase.com/hc/article_attachments/4572816750740/rptmenu.png) button in the heading of the reference field that connects the child table to the parent table.
    
2.  Within the menu that displays select **Add a column**.
    
3.  Select a table related to Tablename and then choose the table from the drop-down. Quickbase displays a list of fields from the table you selected.  
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572802185876/addrelated.png)
    
4.  Select one or more fields and click **OK**. When you do so, Quickbase creates the lookup fields and adds them to the report.
    
5.  To save the report, click **Save** at the top of the screen. If you click **Revert** instead, the report changes are not saved, but the lookup fields have still been created behind the scenes.
    

Note: When you add a lookup field to a report, it doesn't automatically appear on forms. You'll need to add it yourself by [customizing forms](https://helpv2.quickbase.com/hc/en-us/articles/4570300784788-Design-a-Form-).

## Creating a lookup field from the Report Builder

There may be times when you're in the middle of [creating a report](https://helpv2.quickbase.com/hc/en-us/articles/4570299978772-Creating-new-reports-from-scratch-) and you realize that you want to incorporate a field from a related parent table.

To create a lookup field from the report builder:

1.  Within the Report Builder, under the **Columns** section, select **Custom columns**.
    
2.  Within the **Available** list that appears on the left, select **<Columns from a related table>**.
    
    Quickbase displays a dialog box listing related tables and fields.
    
3.  Select the table and field(s) you want to display in your report and click **OK**. Quickbase creates a lookup field and includes it in the report you're building.
    
    Note: If the field you choose is part of multiple relationships, Quickbase first prompts you for more information. For example, say you're creating a report for the **Tasks** table and you choose the field **Company** from the **Resources** table. Quickbase displays a message telling you that the **Task Creator**, **Assigned To** and **Project Lead** fields all reference the **Company** field. The question you need to answer is: Whose company do you want to see -- the Task Creator's? the individual to whom the task is assigned? or the Project Lead? Make a choice and click **OK**.
    

Note: When you add a lookup field to a report, it doesn't automatically appear on custom forms. You'll need to add it yourself by [customizing forms](https://helpv2.quickbase.com/hc/en-us/articles/4570300784788-Design-a-Form-).

### Related topics:

-   [Creating table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-)
    
-   [Adding field s to table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570416568468-Adding-fields-to-table-to-table-relationships-)
    
-   [Deleting fields from table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570319687956-Deleting-fields-from-table-to-table-relationships-)
    
-   [Deleting table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570433178260-Deleting-table-to-table-relationships-)