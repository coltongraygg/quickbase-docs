## How real-time error checking works

As you enter information in your formula, real-time error checking quickly fixes or flags formatting and syntax errors and checks formula argument types.

If Quickbase detects an error, a warning icon will appear. ![](https://helpv2.quickbase.com/hc/article_attachments/22290522675860) Click the icon to view specific error messages.

## Automatic error checking

After you save your formula, the software checks formula syntax, ensures fields and references are valid, and evaluates the formula to make sure no other errors exist.

### Formula syntax check

Quickbase checks the formula syntax, such as parentheses placement.

When the cursor is to the right of an opening or closing parenthesis, a gray frame highlights the matching parenthesis, if there is one. 

![](https://helpv2.quickbase.com/hc/article_attachments/18207555103380)

### Formula validation

Formula validation occurs once the formula's syntax is correct. Quickbase makes sure that

-   Field references refer to fields in the app
-   Formula data types and field references match those required by functions and operators

### Formula evaluation

After a formula is validated, Quickbase processes the formula and produces the result.

Some errors don't show up until evaluation. For example, if a formula refers to a deleted field the result of the evaluation is [null](https://helpv2.quickbase.com/hc/en-us/articles/16909898126612). 

Formulas are evaluated many times to ensure they work. For example, formulas are evaluated when displaying a record that contains formulas or sorting a table on a formula field.

## Related

-   [Troubleshooting formulas](https://helpv2.quickbase.com/hc/en-us/articles/4570267666836)
-   [Best practices: writing formulas](https://helpv2.quickbase.com/hc/en-us/articles/16909898126612)
-   [Formula components](https://helpv2.quickbase.com/hc/en-us/articles/18313319756692)