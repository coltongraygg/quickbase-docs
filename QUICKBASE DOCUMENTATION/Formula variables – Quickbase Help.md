Formula variables are short proxies or stand-ins for a specific part of a formula. They allow you to easily reuse a section or snippet of your formula multiple times. Formula variables make it easier to read complex formulas and can also help you save time while you write your formula.

## Defining a formula variable

To use a variable in your formula, you first need to define it. Use the following format:

`var (type of variable) (variable name)=(formula snippet);`

Note: The parenthesis are included in the format to show the elements that make up a formula variable. The type of variable and variable names are not surrounded by parenthesis when you define a variable.

Variable examples:

-   `var number total=[Price]*[Quantity];`
    
-   `var text fullname=[First name]&" "&[Last name];`
    

Note: Variables only work within a single formula. You must define a variable in every formula field where you would like to use it.

### Types of variables

The type of variable you use should match the type of data that will result from the formula snippet. For example, if the part of the formula you define in your variable will result in a numeric result, you should use the number variable type.

You can create the following types of variables:

-   var bool
    
-   var number
    
-   var text
    
-   var textlist
    
-   var date
    
-   var datetime
    
-   var duration
    
-   var timeofday
    
-   var workdate
    
-   var user
    
-   var recordlist\*
    

\*Note: `var recordlist` is used specifically with formula queries. To learn more, [read the Formula Queries help article](https://helpv2.quickbase.com/hc/en-us/articles/4570286674196).

### Naming a formula variable

When you define a formula variable, you also assign it a name. This allows you to refer to the variable in the formula. Names must only contain letters. They cannot contain numbers, spaces, or special characters (like a parenthesis, bracket, or dash).

## Using a variable in a formula

After you have defined a variable, you can then reference it within the formula. You indicate the use of a variable with a dollar sign ($).

For example, the following formula calculates how names should be displayed in the formula field.

`var text fullname=[first name]&" "&[last name];`

`Case([title],"Dr.",[title]&" "&$fullname,`

`"Mr.",[title]&" "&$fullname,`

`"Ms.",[title]&" "&$fullname,`

`"Hon.",[title]&" "&$fullname, $fullname)`

The variable is defined at the top. It's a text type variable, called **fullname**, which consists of the string: \[first name\] & " " & \[last name\]

This formula says: If the title field is populated with the value "Dr.", then display the title, a space, and the fullname (which is the string: \[first name\] & " " & \[last name\]). If the title is" Mr.", display the title, a space, and the fullname. If the title is "Ms.", display the title, a space, and the fullname. If the title is "Hon.", display the title, a space, and the fullname. If the title field does not contain any of these values, display only the fullname.

### Setting Boolean conditions example

Formula variables are especially useful if you need to set lots of conditions and they appear multiple times within your formula.

For example, the following formula uses two variables to set conditions about contract approval.

`var bool contractApproved=(([Contract Approval]="Approved")or([Contract Approval])="PreApproved"));`

`var bool printApproved=(([PRINT Approval]="Approved")or([PRINT Approval])="Changed"));`

Each variable is of data type Boolean (bool), which means the result will be yes or no. If the conditions that follow are met, the result is yes (true), if not, the result is no (false). So, the `contractApproved` variable will be true if the value in the Contract Approval field is "Approved" or "PreApproved." The `printApproved` variable will be true if the value in the PRINT Approval field is "Approved" or "Changed."

The rest of the formula references the variable whenever it needs to use these conditions. For example if formula is in a field called Contract Status, and it might look like this:

`If ($contractApproved and $printApproved and not([Needs VP/Finance Approval]), "In Production", "Pending")`

This formula says that if the `contractApproved` variable is true and the `printApproved` variable is true and Needs VP/Finance Approval checkbox field is not turned on, then status is "In Production", otherwise it's "Pending."

### Related topics:

-   [Formula foundations](https://helpv2.quickbase.com/hc/en-us/articles/4839910743444)
    
-   [Troubleshooting formulas](https://helpv2.quickbase.com/hc/en-us/articles/4570267666836-Troubleshoot-Formulas-)
    
-   [Formula queries](https://helpv2.quickbase.com/hc/en-us/articles/4570286674196)