## Commonly used formula functions and formula examples

## Formula examples

<table data-number-column="false"><colgroup><col> <col> <col> <col></colgroup><tbody><tr><th data-colwidth="170" aria-sort="none"><p data-renderer-start-pos="49">You want to</p></th><th data-colwidth="170" aria-sort="none"><p data-renderer-start-pos="67">Use field type</p></th><th data-colwidth="170" aria-sort="none"><p data-renderer-start-pos="86">Formula</p></th><th data-colwidth="170" aria-sort="none"><p data-renderer-start-pos="97">Explanation</p></th></tr><tr><td data-colwidth="170"><p data-renderer-start-pos="115">Multiply 32 and 2.5.</p></td><td data-colwidth="170"><p data-renderer-start-pos="139">Formula - Numeric</p></td><td data-colwidth="170"><p data-renderer-start-pos="160"><code data-renderer-mark="true">32 * 2.5</code></p></td><td data-colwidth="170"><p data-renderer-start-pos="172">32 times 2.5</p></td></tr><tr><td data-colwidth="170"><p data-renderer-start-pos="190">Determine net worth by subtracting liabilities from assets.</p></td><td data-colwidth="170"><p data-renderer-start-pos="253">Formula - Numeric</p></td><td data-colwidth="170"><p data-renderer-start-pos="274"><code data-renderer-mark="true">[Assets] – [Liabilities]</code></p></td><td data-colwidth="170"><p data-renderer-start-pos="302">Take the value in the&nbsp;<strong data-renderer-mark="true">Assets</strong>&nbsp;field and subtract from it the value in the&nbsp;<strong data-renderer-mark="true">Liabilities</strong>&nbsp;field.</p></td></tr><tr><td data-colwidth="170"><p data-renderer-start-pos="399">Determine net worth after receiving a standard tax refund.</p></td><td data-colwidth="170"><p data-renderer-start-pos="461">Formula - Numeric</p></td><td data-colwidth="170"><p data-renderer-start-pos="482"><code data-renderer-mark="true">([Assets] + 3000) - [Liabilities]</code></p></td><td data-colwidth="170"><p data-renderer-start-pos="519">Take the value in the&nbsp;<strong data-renderer-mark="true">Assets</strong>&nbsp;field and add 3000. Then take the result and subtract from it the value in the&nbsp;<strong data-renderer-mark="true">Liabilities</strong>&nbsp;field.</p></td></tr><tr><td data-colwidth="170"><p data-renderer-start-pos="651">Calculate the area of a circle whose radius is in the field named Radius.</p></td><td data-colwidth="170"><p data-renderer-start-pos="728">Formula - Numeric</p></td><td data-colwidth="170"><p data-renderer-start-pos="749"><code data-renderer-mark="true">[Radius] * [Radius] * 3.14159</code></p></td><td data-colwidth="170"><p data-renderer-start-pos="782">Take the value in the&nbsp;<strong data-renderer-mark="true">Radius</strong>&nbsp;field and multiply it by the value in the&nbsp;<strong data-renderer-mark="true">Radius</strong>&nbsp;field. Then multiply by&nbsp;<strong data-renderer-mark="true">3.14159</strong>.</p></td></tr><tr><td data-colwidth="170"><p data-renderer-start-pos="898">Calculate the minimum payment.</p></td><td data-colwidth="170"><p data-renderer-start-pos="932">Formula - Numeric</p></td><td data-colwidth="170"><p data-renderer-start-pos="953"><code data-renderer-mark="true">Min([Balance Due], 25.00)</code></p></td><td data-colwidth="170"><p data-renderer-start-pos="982">Display whichever amount is less: the value in the&nbsp;<strong data-renderer-mark="true">Balance Due</strong>&nbsp;field or 25.00.</p></td></tr><tr><td data-colwidth="170"><p data-renderer-start-pos="1066">Display a contact's full name.</p></td><td data-colwidth="170"><p data-renderer-start-pos="1100">Formula - Text</p></td><td data-colwidth="170"><p data-renderer-start-pos="1118"><code data-renderer-mark="true">[First Name] &amp; " " &amp; [Last Name]</code></p></td><td data-colwidth="170"><p data-renderer-start-pos="1154">Display the value in the&nbsp;<strong data-renderer-mark="true">First Name</strong>&nbsp;field. Display a space. Display the value in the&nbsp;<strong data-renderer-mark="true">Last Name</strong>&nbsp;field.</p><p data-renderer-start-pos="1257"><strong data-renderer-mark="true">Note:</strong>&nbsp;To create a space between the names, this formula inserts a text literal. Quickbase displays whatever characters appear between a set of double quotes.</p></td></tr><tr><td data-colwidth="170"><p data-renderer-start-pos="1420">Calculate the date one week from today.</p></td><td data-colwidth="170"><p data-renderer-start-pos="1463">Formula - Date</p></td><td data-colwidth="170"><p data-renderer-start-pos="1481"><code data-renderer-mark="true">Today() + Days(7)</code></p></td><td data-colwidth="170"><p data-renderer-start-pos="1502">Display the date that is today plus 7 days.</p></td></tr><tr><td data-colwidth="170"><p data-renderer-start-pos="1551">Discover if net worth of over $1 million.</p></td><td data-colwidth="170"><p data-renderer-start-pos="1596">Formula - Checkbox</p></td><td data-colwidth="170"><p data-renderer-start-pos="1618"><code data-renderer-mark="true">[Net Worth] &gt; 1000000</code></p></td><td data-colwidth="170"><p data-renderer-start-pos="1643">Display a<strong data-renderer-mark="true">&nbsp;true</strong>&nbsp;result if the value in the&nbsp;<strong data-renderer-mark="true">Net Worth</strong>&nbsp;field is greater than 1,000,000.</p><p data-renderer-start-pos="1729"><strong data-renderer-mark="true">Note:</strong>&nbsp;This is a&nbsp;<em data-renderer-mark="true">Boolean</em>&nbsp;statement, which only returns a true or false. This result only applies to a checkbox field which is either ON (true) or OFF (false).</p></td></tr><tr><td><p data-renderer-start-pos="1551">Find the lesser of two values</p></td><td><p data-renderer-start-pos="1596">Formula - Numeric</p></td><td><p data-renderer-start-pos="1618"><code data-renderer-mark="true">Min(41,23)</code></p></td><td><p data-renderer-start-pos="1643">Display whichever amount is less: 41 or 23. The result is 23.</p></td></tr><tr><td><p data-renderer-start-pos="1551">Find the lesser of two values, where one of those values comes from a field in your Quickbase application</p></td><td><p data-renderer-start-pos="1596">Formula - Numeric</p></td><td><p data-renderer-start-pos="1618"><code data-renderer-mark="true">Min(41,23,[tax])</code></p></td><td><p data-renderer-start-pos="1643">Display whichever amount is less: 41, 23, or the value in the&nbsp;<strong data-renderer-mark="true">tax</strong>&nbsp;field.</p></td></tr><tr><td><p data-renderer-start-pos="1551">Total some specific values</p></td><td><p data-renderer-start-pos="1596">Formula - Numeric</p></td><td><p data-renderer-start-pos="1618"><code data-renderer-mark="true">Sum(12.5, 0.5, 3)</code></p></td><td><p data-renderer-start-pos="1643">Add 12.5 to .5 to 3 and display the result, which is 16.</p></td></tr><tr><td><p data-renderer-start-pos="1551">Find the average of a few values</p></td><td><p data-renderer-start-pos="1596">Formula - Numeric</p></td><td><p data-renderer-start-pos="1618"><code data-renderer-mark="true">Average(12, 6, 9)</code></p></td><td><p data-renderer-start-pos="1643">Display the average of 12, 6 and 9. The result is 9.</p></td></tr><tr><td><p data-renderer-start-pos="1551">Find the median of numbers or a duration</p></td><td><p data-renderer-start-pos="1596">Formula - Numeric</p><p>Formula - Duration</p></td><td><p data-renderer-start-pos="1618"><code data-renderer-mark="true">Median(1, 3, 2)</code></p></td><td><p data-renderer-start-pos="1643">Display the median of 1, 3, 2. The result is 2.</p></td></tr><tr><td><p data-renderer-start-pos="1551">Get today's date</p></td><td><p data-renderer-start-pos="1596">Formula - Date</p></td><td><p data-renderer-start-pos="1618"><code data-renderer-mark="true">Today()</code></p></td><td><p data-renderer-start-pos="1643">Display today's date. This function doesn't require any arguments, but you still need to supply the parentheses.</p></td></tr></tbody></table>

## Type conversion formulas

Use type conversion functions to transfer data from one data type to another. 

<table data-number-column="false"><colgroup><col> <col> <col> <col></colgroup><tbody><tr><th data-colwidth="170" aria-sort="none"><p data-renderer-start-pos="49">You want to</p></th><th data-colwidth="170" aria-sort="none"><p data-renderer-start-pos="67">Use field type</p></th><th data-colwidth="170" aria-sort="none"><p data-renderer-start-pos="86">Formula</p></th><th data-colwidth="170" aria-sort="none"><p data-renderer-start-pos="97">Explanation</p></th></tr><tr><td data-colwidth="170"><p data-renderer-start-pos="115">Convert a text string to a date</p></td><td data-colwidth="170"><p data-renderer-start-pos="139">Formula - Date</p></td><td data-colwidth="170"><p data-renderer-start-pos="160"><code data-renderer-mark="true">ToDate("Jan 30, 2021")</code></p></td><td data-colwidth="170"><p data-renderer-start-pos="172">Converts "Jan 30, 2021," which is a text literal to a date value</p></td></tr><tr><td data-colwidth="170">Convert text to a boolean value</td><td data-colwidth="170">Formula - Checkbox</td><td data-colwidth="170"><code data-renderer-mark="true">ToBoolean("Yes")</code></td><td data-colwidth="170">Converts "Yes," which is a text literal to the Boolean value true</td></tr><tr><td data-colwidth="170">Convert date to text value</td><td data-colwidth="170"><p>Formula - Date&nbsp;</p><p>Formula Date / Time</p></td><td data-colwidth="170"><code data-renderer-mark="true">ToFormattedText(Date(2021,01,30),"MMDDYYY")</code></td><td data-colwidth="170">Converts a date value to formatted text, in this case 01-30-2021</td></tr><tr><td data-colwidth="170">Convert text to a number</td><td data-colwidth="170">Formula - Numeric</td><td data-colwidth="170"><code data-renderer-mark="true">ToNumber("-12.3")</code></td><td data-colwidth="170">Converts the text value -12.3 to a numerical value.</td></tr><tr><td data-colwidth="170">Convert a date field to a work date field</td><td data-colwidth="170">Formula - Work Date</td><td data-colwidth="170"><code data-renderer-mark="true">ToWorkDate([Completion Date])</code></td><td data-colwidth="170">Converts the values in the <strong data-renderer-mark="true">Completion Date</strong> field to work dates</td></tr><tr><td><p data-renderer-start-pos="1551">Format a date to ISO8601</p></td><td><p data-renderer-start-pos="1596">Formula - Text</p></td><td><p data-renderer-start-pos="1618"><code>ToFormattedText(01-01-1970,ISO8601) = 1970-01-01T00:00:00-05:00</code></p></td><td><p data-renderer-start-pos="1643">Format 01-01-1970 to ISO8601. ISO8601 is an international standard used in many systems, including our RESTful APIs.&nbsp;</p></td></tr><tr><td><p data-renderer-start-pos="1551">Format a date to unix time</p></td><td><p data-renderer-start-pos="1596">Formula - Date / time,</p><p data-renderer-start-pos="1596">Formula - Date</p></td><td><p data-renderer-start-pos="1618"><code>ToUnixTime(01-01-1970) = 18000</code></p></td><td><p data-renderer-start-pos="1643">Output the numeric unix time of 01-01-1970. Result will include milliseconds.</p></td></tr></tbody></table>

## Setting conditions with the If() function

You can set conditions for your formulas.

For example, you may want

-   Total to appear on an invoice only if the order is complete.
-   **Status** field to say "Completed" only if the **Date Completed** field has been filled out.

To do this, use an If() function.

When using an If() function:

-   Describe a condition for Quickbase to evaluate
-   Specify what to do if the condition is met
-   Specify what to do if the condition is not met
-   Separate the condition and arguments from each other with commas

This is the basic syntax of an If() function:

```
If(condition, value if condition is true, value if condition is false)
```

### If() function example - Boolean statement

You want your Quickbase app to show companies with a net worth greater than 1 million dollars.

Create a Formula - Checkbox field called **Million**, and enter the following formula:

```
If([net worth] > 1000000, TRUE, FALSE)
```

Formula explanation:

-   If the value in the **net worth** field is greater than 1,000,000
-   then turn ON (true) the **Million** checkbox
-   Otherwise, turn it OFF (false)

This is a _Boolean_ statement, which only returns True or False.

### If() function example - text field

Create a Formula - Text field.

Enter the following formula:

`If([Net Worth]>1000000, [Telephone Number], "not top sales priority")`

Formula explanation:

-   If the **Net Worth** field is greater than 1,000,000
-   then display the value from the **Telephone Number** field
-   If not, then display the text _not top sales priority_.

### More If() examples

<table data-number-column="false"><colgroup><col> <col> <col> <col></colgroup><tbody><tr><th colspan="1" rowspan="1" data-colwidth="170" aria-sort="none"><p data-renderer-start-pos="5569">You want to</p></th><th colspan="1" rowspan="1" data-colwidth="170" aria-sort="none"><p data-renderer-start-pos="5587">Use field type</p></th><th colspan="1" rowspan="1" data-colwidth="170" aria-sort="none"><p data-renderer-start-pos="5606">Formula</p></th><th colspan="1" rowspan="1" data-colwidth="170" aria-sort="none"><p data-renderer-start-pos="5617">Explanation</p></th></tr><tr><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="5634">Calculate speed.</p></td><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="5654">Formula - Numeric</p></td><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="5675"><code data-renderer-mark="true">If ([Time] &gt; 0, [Distance]/[Time], null)</code></p></td><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="5719">If the value in the time field is greater than zero, then display the value in the distance field divided by the value in the time field. Otherwise, leave the field empty. (An empty field is called a&nbsp;null <span>[Link to best practices article]</span>.)</p><p data-renderer-start-pos="5927"><strong data-renderer-mark="true">Tip:</strong>&nbsp;You don't need to add the null at the end, as Quickbase defaults to a null argument automatically.</p></td></tr><tr><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="6036">Automatically complete the&nbsp;<strong data-renderer-mark="true">Territory</strong>&nbsp;field, based on who the salesperson is.</p></td><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="6116">Formula - Text</p></td><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="6134"><code data-renderer-mark="true">If([Salesperson]=ToUser("baker@example.com"), "Western", "Eastern")</code></p></td><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="6205">Take the email address&nbsp;<a title="mailto:baker@example.com" href="mailto:baker@example.com" data-renderer-mark="true"><em data-renderer-mark="true">baker@example.com</em></a>&nbsp;and convert it to the user value connected with that email account (you can use a user name instead of an email address). If the value in the&nbsp;<strong data-renderer-mark="true">Salesperson</strong>&nbsp;field is that user, then display the word&nbsp;<em data-renderer-mark="true">Western</em>, otherwise, display the word&nbsp;<em data-renderer-mark="true">Eastern</em>.</p><p data-renderer-start-pos="6489">Tip:&nbsp;&nbsp;Form rules can also automatically populate fields based on other values.</p><p data-renderer-start-pos="6572">To set this up for multiple salespeople and territories, use the Case() function instead. Read how in the next section.</p></td></tr><tr><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="6697">Display an invoice total only if the order is complete.</p></td><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="6756">Formula - Numeric</p></td><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="6777"><code data-renderer-mark="true">If([Order Complete]=TRUE, [SUBTOTAL] + [TAX], null)</code></p></td><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="6832">If the&nbsp;<strong data-renderer-mark="true">Order Complete</strong>&nbsp;checkbox is on, then add the value in the&nbsp;<strong data-renderer-mark="true">subtotal</strong>&nbsp;field to the value in the&nbsp;<strong data-renderer-mark="true">tax</strong>&nbsp;field and display it. If not, then leave the field empty (or&nbsp;<a title="https://help.quickbase.com/user-assistance/using_formulas_in_QuickBase.html#null" href="https://help.quickbase.com/user-assistance/using_formulas_in_QuickBase.html#null" data-renderer-mark="true">null</a>).</p></td></tr><tr><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="7008">Automatically set the&nbsp;<strong data-renderer-mark="true">Status</strong>&nbsp;field to "Complete," when a staff member enters a date in the&nbsp;<strong data-renderer-mark="true">Completion Date</strong>&nbsp;field.</p></td><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="7125">Formula - Text</p></td><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="7143"><code data-renderer-mark="true">If(isnull([Completion Date]), "Pending", "Complete")</code></p></td><td colspan="1" rowspan="1" data-colwidth="170"><p data-renderer-start-pos="7199">If no one's entered a value in the&nbsp;<strong data-renderer-mark="true">Completion Date</strong>&nbsp;field (in other words, that field is&nbsp;<a title="https://help.quickbase.com/user-assistance/using_formulas_in_QuickBase.html#null" href="https://help.quickbase.com/user-assistance/using_formulas_in_QuickBase.html#null" data-renderer-mark="true">null</a>) then display the word&nbsp;<em data-renderer-mark="true">Pending</em>. If not, display the word&nbsp;<em data-renderer-mark="true">Complete</em>.</p></td></tr></tbody></table>

## Setting multiple conditions with the Case() function

Use the Case() function to evaluate multiple conditions against a single field.

### Case() example - turn numeric rating to text

-   A movie review application contains a field called **Rating.** Viewers pick a number from one to four.
-   You want to translate this score into a one-word review.
-   Create a Formula-Text field and use the Case() function to enter multiple conditions:

```
Case([rating],1,"poor"
```

Formula explanation

-   If the value in the **rating** field is 1, display the word _poor_
-   If the value in the rating field is 2, display the word _fair_, and so on.

**Tip:** Use double slashes (//) to add comments about what each part of your formula does

```
If ( Abs([x]) < 5,        //test the value
```

## Using the SearchAndReplace function

With the`SearchAndReplace` function, you can:

-   Replace words with other words
-   Remove words

### Example - empty quotes to remove a word or phrase

To filter out noise in your data, like removing HTML tags from email messages that have been synced to a Quickbase app:

```
SearchAndReplace([Email Body],"<p>","")
```

This formula removes all appearances of `<p>` from the body of the email.

### Example - SearchAndReplace several times in a row

Replace several words or phrases in the same piece of text.

For example,

Create a formula to search the Notes field of an app and replace acronyms with the phrases they represent:

`SearchAndReplace(SearchAndReplace(SearchAndReplace([Notes],"GTM","Go-to Market"),"KPI","Key Performance Indicator"),"YoY Growth","Year-over-Year Growth")`

### Example - SearchAndReplace with other functions

Use `SearchAndReplace`with other functions like `Left` and `Right` to exclude text in a field.

For example,

Exclude all text in a field up to the first appearance of the word “Approved.” This will help you examine an approval log and see if there are multiple approvals.

-   The `Left/Right/NotLeft/NotRight` functions only operate on a single character at a time
-   So, replace a word with a single character
-   Then use a function such as `NotLeft`
-   Select a character which does not appear in your source field
    -   For example, "#" doesn’t appear anywhere in the source data
-   Use this `If()`formula to determine if the word "Approved" appears more than once:

`If(Contains(NotLeft(SearchAndReplace([Approval Log],"Approved","#"),"#"),"#") = false,true,false)`

## Related

-   [Writing formulas](https://helpv2.quickbase.com/hc/en-us/articles/4889032261012)
-   [Best practices: writing formulas](https://helpv2.quickbase.com/hc/en-us/articles/16909898126612)
-   [Troubleshooting formulas](https://helpv2.quickbase.com/hc/en-us/articles/4570267666836)