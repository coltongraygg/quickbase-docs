## Formula queries: field types, type conversions, and variables

[Formula query functions](https://helpv2.quickbase.com/hc/en-us/articles/4570286674196) only work in certain formula field types.

However, you can use variables or type conversion functions to use formula query functions in most formula field types. Conversion functions convert a value from one datatype to another within your function.

For example, the `ToFormattedText` function takes a date field and converts it to the formatted text version. 

For a list of all type conversion functions, see the [Formula Functions Reference app](https://www.quickbase.com/db/6ewwzuuj?a=td).

## Field types you can use on their own

You can use these field types on their own without variables or conversion functions.

<table><tbody><tr><td><strong>Formula query function</strong></td><td><strong>Compatible formula field type</strong></td></tr><tr><td><p>GetFieldValues</p></td><td><p>Formula - Multi-select text</p></td></tr><tr><td><p>SumValues</p></td><td><p>Formula - Numeric</p></td></tr><tr><td><p>Size</p></td><td><p>Formula - Numeric</p></td></tr></tbody></table>

## Formula query using a type conversion

This example shows a formula query that has been added to a formula - text field. 

`ToText(GetFieldValues(GetRecords("{9.EX.'"&[Last Name]&" '}AND{8.EX.'"&[Email]&"'}"), 11))`

This example returns the field value of field 11 in records where:

-   Field ID 9 is equal to the last name on which the formula calculates _and_
-   Field ID 8 is equal to the email of the record on which the field ID calculates

The `ToText` function converts the values of field 11 to text to allow the result to appear in the formula - text field.

For example, if the query returns the value of field 11 from two records, the values appears as text separated by a semi-colon:

![field with text values a;b](https://helpv2.quickbase.com/hc/article_attachments/17526189077524)

## Using formula variables in complex formulas

Formula variables can help shorten complex formulas and save time when you're writing formulas that rely on formula queries. See [Formula variables](https://helpv2.quickbase.com/hc/en-us/articles/4570254813332) for more information.

### Using recordlist in a formula query

In addition to other variable types, you can use `var recordlist` when building formula queries.

**Examples of  `var recordlist`**

-   `var RecordList singleRecord = GetRecord(8);`
-   `var RecordList records = GetRecords("{6.EX.'&[Manager name]&'}");`

These examples use the `GetRecords()` function and `recordlist` to return a list of records.

**Note:** `recordlist`, like the `GetRecords()` function, cannot be used on its own. It needs to be used with another function to return results. Most commonly, it's used in `GetFieldValues()`, `Size()`, or `SumValues()` functions. You can also convert it to text:

```
ToText(GetRecords("{6.EX.'&[Manager name]&'}")
```

### Formula query in a Formula - Check box field type

This is an example of a formula query in a formula - check box field.

`var TextList vals = GetFieldValues(GetRecords("{6.EX.'"&[Status]&"'}", [_DBID_PROJECTS]), 8);`

`If(Contains($vals, "High"), true, false)`

-   This example defines the variable `vals` using the `GetFieldValues` function.
    
    -   `GetFieldsFunction` fetches the value that populates field ID 8 of any records from the table with alias `DBID_PROJECTS` where field ID 6 is equal to the same status as the record this formula is being calculated on.
        
-   The example uses an `If` function. If any field values gathered in `GetFieldValues` contain the text “High,” the result is true. If not, the result is false.
    
-   If the result is true, the check box is checked.
    

### Formula query in a formula - date field type

This is an example of a formula in a formula-date field.

`var number holidays= Size(GetRecords("{7.OAF.'"&[Start Date]&"'}AND{7.OBF.'"&([Start Date]+Days([# of Days (numeric)]))&"'}", [_DBID_HOLIDAYS]));`

`[Start Date]+Days([# of Days (numeric)])+Days(Size(GetRecords("{7.OAF.'"&[Start Date]&"'}AND{7.OBF.'"&([Start Date]+Days([# of Days (numeric)]+Days($Holidays))&"'}", "[_DBID_HOLIDAYS]"))`

-   The `Size()` function counts the number of holiday records that fall within a time period to automatically calculate the end date of a specific task.
    
-   The formula begins with a variable to identify the number of holidays within the duration.
    
    -   This adjusts the final result to account for situations where the original duration may end on a holiday, but the following day is also a holiday (for example, Thanksgiving in the United States).
        
    -   The query is searching the `[_DBID_HOLIDAYS]` (holiday table) for any holiday dates (field ID 7) that fall on or after `[Start Date]` and on or before `[Start Date]` plus the task duration (calculated End Date). The size function counts the number of records returned.
        
-   The final result of the formula, the task end date, is calculated by adding `[Start Date]` to the total task duration (duration defined at the task level, and the number of holidays).
    
    -   The query in this part of the formula is identical to the one defined in the variable, except it is adding the number of holidays from the variable to account for the original duration (`[Start Date]+[# of Days (numeric)]`) ending on a holiday.