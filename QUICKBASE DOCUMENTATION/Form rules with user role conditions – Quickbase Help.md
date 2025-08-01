## Form rules with user role conditions

You can create rules with conditions that trigger actions based on the user roles you created in your app. For example, You could create a rule that would only allow users in a manager role to see and edit fields in the purchase order section of your form. You would need to create a user role condition that triggers an action to show the purchase order section when the user is in a manager role. You could also add an action that makes the fields in the purchase order section editable. 

## User role condition operators

Each user role condition is paired with an operator that tells the rule how to evaluate the user role. For example your condition might read, if the user `is in the role` manager. Operators for user role conditions are as follows:

<table><tbody><tr><td>User role condition operator</td><td>Description</td></tr><tr><td>Is in the role</td><td>The user’s role must match the role specified to be true.&nbsp;&nbsp;</td></tr><tr><td>Is not equal to</td><td>The user’s role must be any other role except the role specified to be true</td></tr></tbody></table>

## Building user role conditions

Example: If you wanted to display salary information to managers in your employee record app, you could use the user role condition and an `is in the role` operator to show the fields to the correct users. 

You would select:

When

a user is in the manager role

Then

show salary fields

![Screenshot_2023-05-23_at_12.38.43_PM.png](https://helpv2.quickbase.com/hc/article_attachments/15893611070868)