## Deleting table-to-table relationships

Before you delete a relationship, understand that you'll lose any data you've entered in fields belonging to that relationship.

## **To delete a table-to-table relationship:**

1.  Open the app that contains the relationship you want to delete.
    
    If you created a relationship between tables in two different apps (a cross-app relationship), open the application that contains the child table. (**Note:** You have the option to disable and re-enable cross-app relationships, rather than deleting them.)
    
2.  Open the table.
    
3.  In the list of table-to-table relationships,locate the relationship that you want to delete, and either:
    

-   Select its Permanently delete this relationship icon (![](https://helpv2.quickbase.com/hc/article_attachments/4572816625044/deleteicon_12x12.png)) in the right column.
    
    or
    
-   Select the relationship to open its properties page, and then select Delete relationship button in the top right.
    

5.  After step 3, a **Delete Relationship?** confirmation page appears. Select the Delete button in the top right. A **Delete Fields?** dialog appears.
    
6.  Select the **Delete** button. A message letting you know how many fields were deleted, along with a message asking if you want to delete the reference field.
    
    **Note:** Quickbase deletes all the fields that are part of the relationship except the reference field itself, which is _not_ deleted. This field reverts to a regular field. To avoid confusion you may want to delete this field too.
    
7.  If you decide to delete the reference field, the field properties page appears. On the **Usage** tab, select **Delete Field**.
    
8.  Select **Delete** to confirm the action and return to the Relationships tab.