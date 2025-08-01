## Form rules with field value conditions

You can create rules with conditions that trigger actions the value in a field matches the criteria you select. When you build a rule with a field value condition, you can select the field, the operator by which the rule will evaluate the value, and the value.

For example, if you wanted to create a rule for your client management form that requires users to schedule a new appointment with a client when they are more than 30 days have passed since their last contact, you would need to create a rule with a field value condition that triggers an action that makes the fields in the appointment section required when the value in the days since last contact field is greater than 30 days.

![Screenshot_2023-05-25_at_2.07.09_PM.png](https://helpv2.quickbase.com/hc/article_attachments/15963817419668)

## Field value condition operators

Each field value condition contains an operator that tells the form rule how to evaluate the field value.

<table><tbody><tr><td>Operator</td><td>Description</td></tr><tr><td>Is equal to</td><td><p>The value in the field must be equal to selected value exactly</p><p><strong>Note: </strong>When used with list - user and multi-select text fields, only all of the selected values can appear in the field to be true. &nbsp;</p></td></tr><tr><td>Is not equal to</td><td><p>The value in the field must not be equal to the selected value</p><p><strong>Note: </strong>When used with list - user and multi-select text fields, the values that appear in the field can not equal to the&nbsp;exact set of values&nbsp;specified in the selected values to be true.</p></td></tr><tr><td>includes</td><td>The value in the field can match the selected value exactly, or it can contain the exact selected value along with other values</td></tr><tr><td>Does not include</td><td>The value in the field cannot contain the selected value</td></tr><tr><td>is less than</td><td>The value must be less than the selected value</td></tr><tr><td>is lower than alphabetically</td><td>Quickbase uses alphabetical order to determine whether a value is lower than the selected value</td></tr><tr><td>is greater than</td><td>The value must be greater than the selected value</td></tr><tr><td>is higher than alphabetically&nbsp;</td><td>Quickbase uses alphabetical order to determine whether a value is higher than the selected value</td></tr><tr><td>is less than or equal to</td><td>The value must be less than or equal to the selected value to be true</td></tr><tr><td>is lower than or equal to alphabetically</td><td>Quickbase uses alphabetical order to determine whether a value is lower than or equal to the selected value</td></tr><tr><td>is greater than or equal to</td><td>The value must be greater than or equal to the selected value to be true. For text fields</td></tr><tr><td>is higher than or equal to alphabetically</td><td>Quickbase uses alphabetical order to determine whether a value is higher than or equal to the selected value</td></tr><tr><td>is before</td><td>The date/time in the field must occur chronologically before the selected value</td></tr><tr><td>is after</td><td>The date/time in the field must occur chronologically after the selected value</td></tr><tr><td>is on or before</td><td>The date/time in the field must occur on or chronologically before the selected value</td></tr><tr><td>is on or after</td><td>The date/time in the field must occur on or after the selected value</td></tr><tr><td>is during</td><td>The date/time in the field must occur within the selected value range</td></tr><tr><td>is not during</td><td>The date in the field must not occur within the selected value range</td></tr><tr><td>starts with</td><td><p>The value in the field must start with the selected value</p></td></tr><tr><td>does not start with</td><td><p>The value in the field must not start with the selected value</p></td></tr><tr><td>is the current user</td><td>The user must match the selected user</td></tr><tr><td><p>filename contains</p></td><td><p>The name of the file that appears in the field can match the selected values exactly, or it can contain those values and other values as well</p></td></tr><tr><td>filename does not contain</td><td><p>The name of the file that appears in the field can not match the selected values exactly, and it can not contain those values</p></td></tr><tr><td>filename is equal to</td><td><p>The name of the file that appears in the field must match the selected value exactly</p></td></tr><tr><td>filename is not equal to</td><td><p>The name of the file that appears in the field must must not match the selected value exactly</p></td></tr><tr><td>filename starts with</td><td><p>The name of the file that appears in the field must start with the selected value</p></td></tr><tr><td>filename does not start with</td><td><p>The name of the file that appears in the field must not start with the selected value</p></td></tr><tr><td>contains</td><td><p>The value in the field must contain the exact selected value</p></td></tr><tr><td>does not contain</td><td><p>The value in the field must not contain the exact selected value.</p></td></tr></tbody></table>

## Building field value condition rules with is equal to operators

Example: If you wanted to capture sales details on a sales volume tracking form when users indicate they have completed a sale, you could use the is equal to operator to create a rule to display and require a multi-select field for users to select the products they sold to each client.

To build your rule you would select:

**When**

sale (_checkbox field)_

is equal to

checked

**Then**

show

field

products sold 

_Add action_

require

field

products sold

## Building field value condition rules with is less than operators

Example: If you wanted to display a message to users to reorder items with low inventory, you can use the is less than operator.

To build your rule, you would select

**When**

the user

is in this role

Manager

and

units in stock

is less than

the value

50

**Then**

display message

modal

"Complete reorder form for this item within 72 hours."