## Formula components

Formulas are made up of several components, as shown in the following example.

### Example formula

```
If([Order Complete]=TRUE, [SUBTOTAL] + [TAX], null)
```

-   **Formula function**: `If()`
-   **Argument**: `[Order Complete]=TRUE, [SUBTOTAL] + [TAX], null`
-   **Field references**: `[Order Complete], [SUBTOTAL], and [TAX]`
-   **Literals**: `2`
-   **Operators**: `+`

## Formula function

A formula function is a pre-defined term that performs an action on values and generates a new value. See the [Formula Functions Reference app](https://www.quickbase.com/db/6ewwzuuj?a=td "https://www.quickbase.com/db/6ewwzuuj?a=td") for a list of formula functions.

You don't need to use formula functions in basic formulas; however, most formulas contain at least one function. Complex formulas may contain many functions. See [examples of formula functions.](https://helpv2.quickbase.com/hc/en-us/articles/4893082972180)

## Argument 

An argument is information in a formula function that tells the function which values to act on or produce.

-   Arguments appear inside parentheses that follow a function
    
-   Separate arguments with commas
    
-   Arguments can be exact [literals](https://helpv2.quickbase.com/hc/en-us/articles/18313319756692-Formula-components#Literal), [field references](https://helpv2.quickbase.com/hc/en-us/articles/18313319756692-Formula-components#h_01HJKSB1G0QCWGSTP4CCVVWHWY), or other [functions](https://helpv2.quickbase.com/hc/en-us/articles/18313319756692-Formula-components#Formula-function) 
    
-   Arguments follow an [order of operation](https://helpv2.quickbase.com/hc/en-us/articles/4570399302548), so the order you list them is important 
    

## Field reference

A field reference retrieves values from a specific field in the record to display or use in a calculation.

-   Enclose field references in square brackets, e.g., `[Manager]`
    
-   A field reference uses a field value in the formula, e.g., `[First Name] &” “& [Last Name]` joins the values in the **First Name** and **Last Name** fields (i.e., “John Smith”)
    
-   Use a field reference to call an application variable; see [Creating and using application variables](https://helpv2.quickbase.com/hc/en-us/articles/4570400496020 "https://help.quickbase.com/user-assistance/variables.html")
    

## Literal

A literal is a value that's used exactly as displayed in the formula. Literals can be numbers or text.

-   Enclose textual literals in double quotes; e.g., `If([Discount %] > 0.15,"Enter a discount of 15% or less."`
    
-   Textual literals can contain quotation marks. If a character is part of the literal put a \\ before the character; e.g., `"The \" character is part of this literal.”` 
    
-   Use a backslash to include an open or close square bracket \[\]; e.g., `“The \[ character is part of this literal.”`
    
-   To use a backslash in your literal, use a \\ before the backslash; e.g., `“The \” and the \\ are both special characters.”`
    

## Operators

Operators are special symbols like `**+**` and `*****` that act on one or two values to return a new value.

### Unary operators

Act on a single value. See list of [unary operators](https://www.quickbase.com/db/6ewwzuuj?a=q&qid=10 "https://www.quickbase.com/db/6ewwzuuj?a=q&qid=10").

In a formula, unary operators might look like:

-   \-5
    
-   +4
    
-   not true
    

### Binary operators

Act on two values. See list of [binary operators](https://www.quickbase.com/db/6ewwzuuj?a=q&qid=11 "https://www.quickbase.com/db/6ewwzuuj?a=q&qid=11")

In a formula, binary operators might look like:

-   3 - 4
    
-   \[Start date\] + Days(7)
    

## Up next

-   [Adding formula fields to tables](https://helpv2.quickbase.com/hc/en-us/articles/22286930497300)
-   [Writing formulas](https://helpv2.quickbase.com/hc/en-us/articles/4889032261012)