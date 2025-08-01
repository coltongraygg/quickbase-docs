## Using Report Link Fields to Create Links between Tables

Usually, you link tables together by creating a [relationship](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-) between them. This is the precise way to specify that certain records are related to each other.

Report link fields behave a bit differently depending on whether you're using them on a report or a form.

-   On a report, the field type provides a link to another report.
-   On a form, it can do that as well, but it is more frequently used to directly display an embedded report. We generate a report link field for the builder automatically when you relate two tables. This is the most common setup.

It's possible to create a report link field from scratch. You can do things like, link to a report child records on a report that's automatically filtered to a subset of the child records, or display info about all other records on the same table. The use case for report link fields on forms is to provide broader context and perspective about a piece of work being done. For instance, a project form could have embedded reports listing budgets, tasks, and documents for that project.

When you create table-to-table relationships, the process automatically adds report link fields to show child records on parent records. But you can also use report link fields outside of table-to-table relationships to match information. You can create and configure a report link field to include matching criteria and show either a link to a report or an embedded report on records.

To configure a report link field:

1.  In properties, in the **Field relationship** section, use the **Match the values in this field from this table** drop-down.
    
    Note: Text from this field serves as the text of your link. Or you can enter different text in the Link text property in the **Display** section.
    
2.  In the values in this field column, choose **Select Target**, then step through the dialogs to select the app and field on which you want to report.
    
3.  To narrow the matching in the report, you can select the **Value matching** choice to only include values if they match exactly in both fields.
    

## Report link field example

The [Formula Functions Reference](http://www.quickbase.com/db/6ewwzuuj?a=q&qid=6) contains a field called **More examples**. This field connects each Formula Function record with records in the Sample Formulas table. If any content in the Sample Formulas' **Solution** field contains text from the Formula Functions Reference's **Function** field, a link is made.