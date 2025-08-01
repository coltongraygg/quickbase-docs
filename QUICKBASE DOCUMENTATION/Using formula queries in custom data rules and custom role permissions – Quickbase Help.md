## Using formula queries in custom data rules and custom role permissions

This article contains examples and guidelines for using formula queries in custom data rules and custom role permissions

## Custom data rules

[Custom data rules](https://helpv2.quickbase.com/hc/en-us/articles/4570135620884) allow you to validate data. Using formula queries, you can do things like:

-   Prevent duplicates in a table
-   Stop users from adding new records, based on fields in other tables

We'll cover each of these examples in more depth.

### Example: Prevent duplicates

You could use a custom data rule to prevent potential duplicates on a table.

`If(Size(GetRecords("{6.EX.'"&[Customer Name]&"'}AND{7.EX.'"&[Region]&"'}")) > 1, "This customer already has an account entry for this region. Please choose a different region for this customer or enter a new customer name.")`

-   This formula uses the `Size` function to count how many records have the same Customer Name and Region as the current record.
-   If that number is greater than 1, that means a record already exists with the same customer name and region
-   The record will not be saved and the user will see the message: "This customer already has an account entry for this region. Please choose a different region for this customer or enter a new customer name."

### Example: Stop users from adding records if criteria in other tables are not met

Assume you have two unrelated tables, Projects and Invoices. You don’t want to allow a new project to be started while there are outstanding invoices.

You could add a custom data rule on the Projects table, similar to this one:

`If(Size(GetRecords("{7.XEX.'Complete'}", [_DBID_INVOICES])) > 0, "You must complete all invoices before starting a new project")`

-   This formula uses the `Size` function to count how many records do not have the value “Complete” populating field ID 7.
-   If that number is greater than 0, that means there is a record not marked “Complete”
-   The user will see the message: “You must complete all invoices before starting a new project.”

## Custom role permissions

-   If adding formula queries to custom role permission formulas, it is best if they reference a different table than the one they calculate on
-   Using a formula query that references its own table may cause unexpected behavior 
-   This is because a change on one record could invalidate a related record