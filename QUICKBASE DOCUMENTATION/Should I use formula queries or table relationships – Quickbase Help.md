## Should I use formula queries or table relationships?

Before deciding whether to use a formula query instead of a table relationship, ask yourself:

-   Can I accomplish the task easily by using a table relationship?   
    If yes, then don't use a formula query, use a table relationship instead
-   Is the information I need already part of a parent-to-child relationship?
    
-   Is the information I need already part of a many-to-many relationship?
    
-   Can I accomplish this by using a direct lookup or summary field?
    

See [About table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636) to learn more.

## When to use formula queries

Formula queries make it much easier to build calculations based on data from other records and data from other tables. For example, if you wanted to find the total estimated cost of all approved budgets and use that calculation on another table, you could use this formula:

```
SumValues(GetRecords("{41.EX.'Approved'} "), 15)
```

Here are some more ideas:

| Scenario | Example |
| --- | --- |
| 
Display data between two tables that share similar data points but are not directly or indirectly connected via a relationship

 | 

The tables _Tasks_ and _Out of Offices_ may share certain data points, but the workflow does not require a table relationship.

Customers may want to check a task owner’s office status when assigning the task.

 |
| 

Reference data from records within the same table

 | 

You may want to create a running total of data or count the number of records that share a common data point.

 |
| 

Avoid complex app structure

 | 

Some workflows, like checking the number of holidays that occur during a certain period, might call for a relationship or create additional tables in an app to summarize data for calculation. You can avoid these additions with formula queries.

 |

## When to use table relationships

Here are some benefits related tables can provide:

-   When you relate two tables, you don't need to enter the same information into separate tables. This could be helpful in many settings. For instance, imagine needing to re-type a project name, project start date, and name of the project manager every time you need to add a new task.
-   Though you create a relationship between two tables, it’s actually the records in the tables that form the relationship. For example, each Company record can have many Contact records.
    
-   A parent table can have more than one child table. A company can have many contacts, but also many activities, and many documents.
    
-   A table can be on both sides of a relationship. For example, a country can be the parent to many states, and a state can be the parent to many cities. In this case, a States table is both a parent table and a child table.
    

## Related

-   [What are formula queries?](https://helpv2.quickbase.com/hc/en-us/articles/4570286674196)
-   [Building queries for your formulas](https://helpv2.quickbase.com/hc/en-us/articles/17510454481044)