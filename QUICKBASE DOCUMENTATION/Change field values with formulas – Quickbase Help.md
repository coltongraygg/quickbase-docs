## Change field values with formulas

This article explains how to use a formula in a Change value action in a form rule. 

Use the Change value action to change the value of a field. You can use a formula to update values in a form rule action. Using a formula gives you more control, and you can update values dynamically. That is, create a form rule that uses a single action for multiple factors with a formula, instead of creating an action for each scenario.

For example, in a Tasks app you have a field for the status change log. That is, a field that tracks who changes a status, to what, and when. 

Instead of creating multiple Change value actions, you can use a formula in a single action.

![the rule builder that shows then logic to change the value of the Status Change Log field to the value in the formula UserToName(User()) & has changed the status to &status](https://helpv2.quickbase.com/hc/article_attachments/20712234690836)

Use this formula

`UserToName(User()) & " has changed the status to " & [Status]`

This formula:

-   identifies the user
-   sets the field value
-   uses in the value of the status field
-   calculates a value for the Status Change Log field

Tip

Use the controls under the formula builder to add relevant fields and the browse functions you can add to a formula.

Learn more about [using the formula builder](https://help.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM47B54E6QMDYN7TK20).