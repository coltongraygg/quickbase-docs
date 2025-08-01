## What are table-to-table relationships?

Table-to-table relationships in Quickbase help you organize the data in your app. If you have data that is common across what you need to track, a relationship lets you enter the data once and make references to it later, rather than entering it repeatedly.

A relationship is a connection between two [tables](https://helpv2.quickbase.com/hc/en-us/articles/4570326161428-What-Is-a-Table-). When you relate two tables, you don't need to enter the same info in separate tables. This could be helpful in many settings. For instance, a projects might have multiple tasks or a company might have multiple locations. Relationships help you save time and effort by connecting a single record in a **parent** table to records in a **child** table.

Learn about: 

-   [When to use a relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-What-are-table-to-table-relationships#When)
    
-   [One-to-many relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-What-are-table-to-table-relationships#One-to-m)
    
-   [What makes relationships work](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-What-are-table-to-table-relationships#h_01FYCKWEF0EX7BZ430D2NHEGG3)
    
-   [The power of table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-What-are-table-to-table-relationships#The)
    

## When to use a relationship

When you enter a new company, it would be nice to enter all the contacts who work there, or to pick the company a new contact is with while you're entering it. You can use a relationship to do this. Instead of creating new fields for company info on the contacts form, you can connect info from a Companies table right into the Contacts form and summarize all the info from Contacts to display in Companies.

### Almost every Quickbase app has several relationships.

When you relate two tables you:

-   Save time because you don’t need to enter the same data repeatedly in separate tables.
    
-   Reduce the risk of data-entry errors.
    
-   Can summarize data from a related table.
    

You can [create a relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-) between any two tables. Generally, these tables are in the same app, but you can create a relationship with a table in a separate app too.

## One-to-many relationships

When you create a relationship, you’re telling Quickbase to connect a single record in one table to many records in the other table. This is called a **one-to-many** relationship.

In a Quickbase relationship, the table on the "one" side is the parent table and the table on the "many" side is the child table.

It’s easy to think of real-world examples of one-to-many relationships:

-   A business has many locations.
    
-   A project has many tasks.
    
-   One manager has several employees.
    

### Using the companies and contacts example from above:

If you created a one-to-many relationship between a Companies table and a Contacts table, when you enter a new contact, you can relate the new contact info to an existing customer, and the company name and related info come directly from the Companies table. You never need to re-enter company info for new contacts. If the company info changes, it automatically updates in all the related contact records.

## What makes relationships work

When you create a relationship between two tables, Quickbase transforms each table in useful ways. For example, if you related a Contacts table to a Companies table, you can see a list of contacts for that company and enter new contacts directly from the Company form.

You can also use relationships to summarize information from the child records on the parent record, like the number of contacts for each customer.

## Fields used with relationships

Every Quickbase relationship includes a **reference field** in the child table that identifies the related parent record. To keep everything organized, Quickbase uses the parent table's [key field](https://helpv2.quickbase.com/hc/en-us/articles/4570321550612-Setting-key-fields-for-tables-) to populate the child table's reference field. The key field always contains a unique value.

Because the reference field contains the parent record's key field, it usually displays as a number. For instance, instead of "Project Name" users would see the Project ID#. If this happens in your app, you can [designate a reference proxy field](https://helpv2.quickbase.com/hc/en-us/articles/4570306784404-Designating-reference-proxy-fields-) and use that field in reports and on forms.

When you create a relationship between two tables, additional fields include:

-   **Lookup** fields. These appear in the child table and provide more information about a linked record in the parent table. For example, you might want to include additional information on an project within the tasks table like project manager name or start and end dates. [Learn how to create a lookup field](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-).
    
-   **Report link** fields appear in the parent table and display as links. When you choose a report link, you see the related records from the child table. Report links help you get more information between tables quickly. For example, if you were to choose an project's **tasks** link, you'd see a list of all the tasks for that project.
    
-   **URL (formula)** fields appear in the parent table, and are displayed as **buttons** on forms and reports. These buttons let you add a new record to the child table from within the parent table. The new record is automatically related to the parent record. For example, if you choose an **Add Task** button in a project record, the new task record appears with the project already selected.
    
-   **Summary** fields appear in the parent table and display data from the child table. Most often, summary fields calculate totals. For example, a Projects parent table could include a summary named **Number of Tasks**. This field calculates the number of tasks in the Tasks child table that are linked with each project. Summary fields can also include other information, such as showing the record with earliest start date. [Learn how to create a summary field](https://helpv2.quickbase.com/hc/en-us/articles/4570321780372-Creating-a-summary-field-).
    

## The power of table-to-table relationships

As you learn more about table-to-table relationships, you’ll start to see the power of this concept and how it helps create apps that can facilitate complex work flows and business logic.

Here are some more benefits related tables can provide:

-   Though you create a relationship between two tables, it’s actually the records in the tables that form the relationship. For example, each Company record can have many Contact records.
    
-   A parent table can have more than one child table. A company can have many contacts, but also many activities, and many documents.
    
-   A table can be on both sides of a relationship. For example, a country can be the parent to many states, and a state can be the parent to many cities. In this case, a States table is both a parent table and a child table.
    

### Related topics:

-   [Creating table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-)
    
-   [Designating reference proxy fields](https://helpv2.quickbase.com/hc/en-us/articles/4570306784404-Designating-reference-proxy-fields-)
    
-   [Adding fields to table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570416568468-Adding-fields-to-table-to-table-relationships-)
    
-   [Deleting fields from table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570319687956-Deleting-fields-from-table-to-table-relationships-)
    
-   [Creating summary fields](https://helpv2.quickbase.com/hc/en-us/articles/4570321780372-Creating-a-summary-field-)
    
-   [Creating lookup fields](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-)
    
-   [Deleting table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570433178260-Deleting-table-to-table-relationships-)
    
-   [Creating many-to-many relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570285625236-Creating-many-to-many-relationships-)
    
-   [Adding parent records from within child records](https://helpv2.quickbase.com/hc/en-us/articles/4570314757652-Adding-parent-records-from-within-child-records-)
    
-   [Viewing all tables and relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570426975892-Viewing-all-tables-and-relationships-)