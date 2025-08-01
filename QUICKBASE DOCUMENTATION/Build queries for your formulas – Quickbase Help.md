## Build queries for your formulas

Formula query functions use [Quickbase API query language](https://helpv2.quickbase.com/hc/en-us/articles/4418310913684-API-DoQuery).

Tip

Copying-and-pasting examples from this and other formula query articles helps while you're getting started with formula queries. To avoid errors in Quickbase, always convert these examples to plain text before pasting them in the formula editor.

## Components of a query

A query consists of:

-   At least one query string that contains:
    -   Field ID (fid)
        
    -   Uppercase comparison operator
        
        -   For a full list of available operators, see [Components of a Query](https://helpv2.quickbase.com/hc/en-us/articles/4418287644308-Components-of-a-Query)
            
    -   Value to be compared against
        

## Query string guidelines

-   Separate each [component of a query string](https://helpv2.quickbase.com/hc/en-us/articles/17510454481044-Build-queries-for-your-formulas#h_01H6YBRTX06CW6M0XAVWBRRRMV) with a period
-   Enclose the entire query string in curly braces
-   Use single quotes to enclose the value to be compared against

**Example of the format of a query**

`{'fid'.operator.'matching_value'}`

`{fid.operator.'"&[field reference]&"'}`

## Additional guidelines for queries in formulas

-   Use double quotation marks to enclose a query that's in a formula query function
-   Single quotes around the field ID are optional

**Example of a query in a formula**

`GetFieldValues(GetRecords("{'5'.EX.'In Progress'}"),3)`

-   Returns records where the value of field ID 5 is equal to the value “In Progress”
-   Used within the `GetFieldValues` function, the formula's output is the values of field ID 3 in records returned by the query
-   Ampersand (&) concatenates, or links, elements of the query string 

## To reference a field in a query

-   Enclose the field you want to reference in ampersands
-   Surround the ampersands with double quotation marks
    -   This signals that the ampersands and field reference should not be treated as literals

**Example of referencing a field in a query**

`GetFieldValues(GetRecords("{'5'.EX.'"&[Manager name]&"'}"), 3)`

-   Returns records where the value of field ID 5 is equal to the value in the `Manager name` field of the record
-   Used within the `GetFieldValues` function the formula's output is the values of field ID 3

### To reference a user field in a query

-   Use the comparison operator TV (true value) instead of EX
    -   EX operator searches only against the displayed value.
    -   TV searches all components of the field. For user fields, this includes user display name and user ID.
-   Wrap user field references in `UserToID()` or `UserToEmail()`.
    -   When a user field is referenced in a formula it's converted to a text string that contains both the user ID and email.
        
    -   Quickbase needs either the user ID or the email to recognize the user, not both. Wrap the user field reference in `UserToID()` or `UserToEmail()` to tell Quickbase to only look at the user ID or the email to evaluate the user.
        

**Example of referencing a user field in a query**

`GetFieldValues(GetRecords(“{‘6’.TV.“&UserToID([User])&"}”), 3)`

-   Returns records where the value of field 6 is the same true value as the `[User]` field of the record on which the formula calculates

## To add multiple queries to a formula

To add more queries to a formula, separate query strings with the AND or OR operators.

**Example query using AND**

`GetFieldValues(GetRecords("{8.EX.'"&[Email]&"'}AND{7.EX.'"&[Last Name]&"'}"), 3)`

-   Find values of field id 3 on records where field 8 is the same email on the record on which the formula calculates _and_ field 7 is the same last name as the record on which the formula calculates
-   For example, this formula can help determine if there are duplicate table records that share the same last name and email

## Up next

[Finding field, record IDs, and table aliases](https://helpv2.quickbase.com/hc/en-us/articles/17525208040468)