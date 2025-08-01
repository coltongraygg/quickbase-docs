## Setting Up Snapshots of Lookup Fields

Generally, in a parent-child relationship, the lookup field in a child record effectively imports the current value of a field in the parent record. If the value of the field in the parent record changes, then the value in the lookup field changes as well. There are times; however, when it would be useful to preserve the value of a lookup field. You can accomplish this using a separate, companion snapshot field.

The concept is:

-   You have a lookup field that may change depending on the data in the parent record.
    
-   You can add a separate snapshot field to store and preserve values from a lookup field. When adding a snapshot field, you pick the lookup field from which it gets data.
    

For example, in an order entry app with a products table and an order details table, there might be a lookup field in the order details table that looks up the price of an item in the products table. When someone places an order, they order the product at its current price and that's what they expect to pay. The price should never change in the order details table if the price changes at a later date in the products table.

Using a separate, companion snapshot field, you can capture the value in a lookup field used in a parent-child relationship and preserve it. Once you have captured the value of a specific lookup field, the value in the snapshot field (in the child table) will not change when changes are made to the contents of the parent record. The only time the value of a snapshot field set to be a snapshot can change is if the child record is changed so that it refers to another parent record. Then the snapshot field would take on the value of the lookup field in the new parent record, and afterwards it will be preserved as described above.

When setting up snapshot fields, the following rules apply:

-   You can set the snapshot field property for these field types: Text, Numeric, Date, Date/Time, Time of Day, Duration, Checkbox, Phone Number, Email Address, User, List - User, and URL.
    
-   You can only take a snapshot of a [lookup field](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-).
    
-   Snapshot fields cannot have a required value.
    
-   Snapshot fields cannot be set to have unique values.
    

To set up a snapshot field:

These steps assume your app has at least one table-to-table relationship.

1.  [Add a field](https://helpv2.quickbase.com/hc/en-us/articles/4570374838292-Adding-new-fields-) in the child table to be your new snapshot field. (This is a regular field, not a lookup field.)
    
2.  For the field properties in the **Advanced** section, select the **Snapshot** checkbox, then choose the lookup field you want to preserve:  
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572886345364/snapshot-field.png)
    
3.  Once you select a lookup field, an **Initialize field for existing records** checkbox appears. To update all the existing records in your app with a snapshot of the current value, select this checkbox, click **Save**, and then click **OK** to confirm that you want to overwrite the existing values in this field with the current values in the parent record.
    
    Note: This initialize option is only available at the time you create the snapshot field.