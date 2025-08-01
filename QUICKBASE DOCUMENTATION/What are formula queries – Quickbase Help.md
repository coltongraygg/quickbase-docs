## What are formula queries?

Formula queries allow you to build flexible, complex workflows and data flows without using code.  Most formulas reference information in a single record. 

![](https://helpv2.quickbase.com/hc/article_attachments/4572796726420)

Formulas can use queries to query information across multiple records and unrelated tables in the same app.

![Formula with queries:Formula uses a query to reference data on related and unrelated tables. Example formula referenced records from a related field and an unrelated table.](https://helpv2.quickbase.com/hc/article_attachments/4572832167956)

## What can I do with formula queries?

Formula queries let you do things like:

-   Find duplicate records in a table 
    
-   Keep track of running totals
    
-   Auto number records (learn more in our [example in Community](https://community.quickbase.com/discussions/quickbase-discussions/creating-sequential-numbering-unique-to-your-business-powered-by-formula-queries/83933)) 
    
-   Create advanced calculations and report filters
    
-   Create fields with outputs similar to lookup summary fields (without creating additional table relationships)
    

## How do I add a formula query to my app?

You can add a formula query to:

-   [Formula fields](https://helpv2.quickbase.com/hc/en-us/articles/4886964472724) in apps 
-   [Report formulas](https://helpv2.quickbase.com/hc/en-us/articles/4570272620052) 
-   [Custom data rules](https://helpv2.quickbase.com/hc/en-us/articles/4570135620884) 

### To make sure users can see formula results

Enable permissions to all fields when building or editing an app that leverages formula queries.

-   Users without permission to view the fields that a formula query uses cannot see the formula results
-   This is true even if you check the **Override sub-field access** setting in the formula field properties 

## Formula query functions 

-   [GetRecord()](https://helpv2.quickbase.com/hc/en-us/articles/17359016669972)
-   [GetRecordByUniqueField()](https://helpv2.quickbase.com/hc/en-us/articles/17399240931092)
-   [GetRecords()](https://helpv2.quickbase.com/hc/en-us/articles/17407057985684)
-   [GetFieldValues()](https://helpv2.quickbase.com/hc/en-us/articles/17476009195796)
-   [SumValues()](https://helpv2.quickbase.com/hc/en-us/articles/17494910680212)
-   [Size()](https://helpv2.quickbase.com/hc/en-us/articles/17495208491796)

## Related

-   [Should I use formula queries or table relationships?](https://helpv2.quickbase.com/hc/en-us/articles/17568408977684)
-   [Building queries for your formulas](https://helpv2.quickbase.com/hc/en-us/articles/17510454481044)