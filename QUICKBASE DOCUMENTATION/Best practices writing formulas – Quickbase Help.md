## Best practices: writing formulas

## Get familiar with operator precedence

Quickbase acts on certain operators before it acts on others. This is called operator precedence. Operator precedence impacts the outcome of your formula.

-   Quickbase reads operators in a predetermined order, not left to right
-   You can change the order of operator evaluation by using parentheses
-   Quickbase always starts reading a formula within the deepest set of parentheses
-   Review [operator precedence](https://helpv2.quickbase.com/hc/en-us/articles/4570399302548)

## Add comments to formulas

Comments help you and others understand parts of your formula. Use double slashes (//) to include comments in your formula. Everything you type from the double slashes to the end of the line is a comment, not part of the formula.

Example of a formula with comments

```
If ( Abs([x]) < 5,        //test the value
```

## Create formula variables

Formula variables can help you simplify complicated formulas. See [Formula variables](https://helpv2.quickbase.com/hc/en-us/articles/4570254813332).

## Working with null values

Most fields can have a special value called the _null value_. Null means that a field's value is undefined, or that no data is entered in the field.

Things you should know:

-   Checkbox and text fields are never null. A Boolean value is either true or false. For example, a checkbox field is either checked or unchecked.
    
-   Empty text fields ("") are considered text strings with zero characters, not null values
    
-   Not all functions can handle null values. For example, in the formula `[Field name]=null` the equals operator requires a value so this example doesn't work. The equals operator can handle a zero, but not a null value.
    

### Null is useful in formulas

For instance, if you want to get an invoice total only if the **Delivered on** field is filled out, create a formula in the **total** field that says: "If there's data in the **Delivered on** Date field, then add **subtotal** and **tax**.

Example of a formula with a null value  

```
If(not IsNull([Delivered on]),[subtotal] + [tax],null)
```

This means that if the **Delivered on** date field contains a value, then take the value in the **subtotal** field and add it to the value in the **tax** field. Otherwise, leave the field empty (null).

### Few functions accept null as an argument

-   `IsNull()` function returns True if the field is null and False if it's not
-   `Nz()` function returns zero if the field is null; otherwise it returns the value of the field  
    This is useful for calculations (see [Null formula examples](https://helpv2.quickbase.com/hc/en-us/articles/16909898126612-Best-practices-writing-formulas#h_01H4196TQ2MDEM2V1GTVKK94WY))  
    **Tip:** If you don't use the `Nz()` function, you can treat a null in a numeric field as a zero to use it in calculations. To set this up, [open the field's properties page](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348 "https://help.quickbase.com/user-assistance/changing_field_properties.html")  and turn on **Treat blank as zero in calculations** checkbox. For numeric fields, Quickbase turns this setting on automatically.

## Null formula examples

<table data-number-column="false"><colgroup><col> <col> <col></colgroup><tbody><tr><th colspan="1" rowspan="1" data-colwidth="226.67" aria-sort="none"><div tabindex="0" aria-disabled="false"><p data-renderer-start-pos="6436">YOU WANT TO</p></div></th><th colspan="1" rowspan="1" data-colwidth="226.67" aria-sort="none"><div tabindex="0" aria-disabled="false"><p data-renderer-start-pos="6454">FORMULA</p></div></th><th colspan="1" rowspan="1" data-colwidth="226.67" aria-sort="none"><div tabindex="0" aria-disabled="false"><p data-renderer-start-pos="6465">FORMULA EXPLANATION</p></div></th></tr><tr><td colspan="1" rowspan="1" data-colwidth="226.67"><p data-renderer-start-pos="6490">Get and display the value from the Temperature field. If the field is empty (null) use 98.6 instead</p></td><td colspan="1" rowspan="1" data-colwidth="226.67"><p data-renderer-start-pos="6602"><code data-renderer-mark="true">If (IsNull([Temperature]), 98.6, [Temperature])</code></p></td><td colspan="1" rowspan="1" data-colwidth="226.67"><p data-renderer-start-pos="6653">If the&nbsp;<strong data-renderer-mark="true">Temperature</strong>&nbsp;field is null, then display the result&nbsp;<strong data-renderer-mark="true">98.6</strong>. Otherwise, display the value from the&nbsp;<strong data-renderer-mark="true">Temperature</strong>&nbsp;field.</p></td></tr><tr><td colspan="1" rowspan="1" data-colwidth="226.67"><p data-renderer-start-pos="6779">Add the number of hours worked in a week</p></td><td colspan="1" rowspan="1" data-colwidth="226.67"><p data-renderer-start-pos="6827"><code data-renderer-mark="true">Nz([Mon]) + Nz([Tues] + Nz([Wed]) + Nz([Thurs]) + Nz([Fri])</code></p></td><td colspan="1" rowspan="1" data-colwidth="226.67"><ul><li data-renderer-start-pos="6890">Return the value in the&nbsp;<strong data-renderer-mark="true">Mon</strong>&nbsp;field.</li><li data-renderer-start-pos="6890">If the&nbsp;<strong data-renderer-mark="true">Mon</strong> field is null then return zero. Add that to the value in the <strong data-renderer-mark="true">Tues</strong>&nbsp;field.</li><li data-renderer-start-pos="6890">If the&nbsp;<strong data-renderer-mark="true">Tues</strong> field is null then return zero. Add that to the value in the <strong data-renderer-mark="true">Wed</strong>&nbsp;field, and so on.</li></ul><p data-renderer-start-pos="7121"><strong data-renderer-mark="true">Note:</strong>&nbsp;You'd use Nz() here instead of IsNull(). To add these values together, Quickbase needs the result to be a number. Nz() generates a zero for a null, which the program can use in the calculation.</p></td></tr><tr><td colspan="1" rowspan="1" data-colwidth="226.67"><p data-renderer-start-pos="7326">Calculate the <strong data-renderer-mark="true">Revenue</strong> field if a date is entered in the <strong data-renderer-mark="true">Submitted for Billing</strong> field</p><p data-renderer-start-pos="7430"><strong data-renderer-mark="true">Tip:</strong> To return a result where a value is not null, add NOT in front of the IsNull() function</p></td><td colspan="1" rowspan="1" data-colwidth="226.67"><p data-renderer-start-pos="7532"><code data-renderer-mark="true">If(not IsNull([Submitted for Billing]),[Revenue Forecast])</code></p></td><td colspan="1" rowspan="1" data-colwidth="226.67"><p data-renderer-start-pos="7594">If there's a value in the <strong data-renderer-mark="true">Submitted for Billing</strong> field, then display the value from the <strong data-renderer-mark="true">Revenue Forecast</strong> field</p></td></tr></tbody></table>

**Note:** If a formula that includes a null function isn't working, access the field's properties page and turn off the **Treat blank as zero in calculations** checkbox.

## Requiring unique values in formula fields

-   **Require unique values** in the formula field property page  
    Unique values could be used to:
    -   Create autonumbering
    -   Concatenate multiple fields in a formula - text field to avoid duplicate records
-   Formula fields that reference the following field types cannot be unique:  
    -   Lookup
    -   Date/Time
    -   Address
    -   Record ID

## Up next

-   [Commonly used formula functions and formula examples](https://helpv2.quickbase.com/hc/en-us/articles/4893082972180)
-   [Troubleshooting formulas](https://helpv2.quickbase.com/hc/en-us/articles/4570267666836)