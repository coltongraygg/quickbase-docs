## Formula queries and performance

The following guidelines will help you avoid errors and performance issues when using formula queries.

## To help performance

-   Do not filter, sort, or group reports based on formula query fields  
    This avoids additional processing time and helps to optimize your apps as they grow.
-   Use formula queries with complex logic in fields on tables, rather than as [report formulas](https://helpv2.quickbase.com/hc/en-us/articles/4570272620052)
-   Do not make formula query fields searchable unless absolutely necessary

## Performance checks

When you create a formula query, or run one in a report or via API, Quickbase checks to see if it will have high performance impact. 

If the performance impact is determined to be too high, an error message will prevent you from saving the formula until you've made adjustments.

### Suggested adjustments

-   Eliminate the most records in the first comparison string to improve query speed
    
-   Use manual input fields rather than derived fields like summary or formula fields
    
-   Use exact matches when possible to build your filter criteria  
    Using “is equal to” as your matching operator will be faster than using  “contains”
    

If these suggestions do not resolve the issue, use the [performance analyzer](https://helpv2.quickbase.com/hc/en-us/articles/4570366376596) and [other performance tools](https://helpv2.quickbase.com/hc/en-us/articles/14598511642772) to find more ways to optimize your app.