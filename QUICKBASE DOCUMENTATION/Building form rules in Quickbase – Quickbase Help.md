Form rules control how your form behaves based on custom scenarios you create. For example:

-   To display required parent or guardian information fields on a patient information form when the patient birthdate is less than 18 years in the past, you can create a form rule to display the fields automatically when a user edits the patient date of birth field with an affected birthdate.
-   You could create a rule that takes a user to the purchase order page when an inventory item is entered with a quantity less than five or create a rule that takes users to the closing costs section of a property management form when they select the sold checkbox. You can create rules using the form rules designer in the form builder.

## About form rules

Form rules are created by describing conditions (when) that trigger the rule and the actions (then) that should occur when the rule is triggered. Form rules are built in the form rules designer in the form builder. 

 ![2023-06-07_Image](https://helpv2.quickbase.com/hc/article_attachments/16266312267924)

## Build a form rule

You can build your form rule by:

-   Writing a formula with the form rule formula builder
-   Describing your conditions and actions in the expression tree builder.

You can switch from the formula builder to the expression builder and back, however your data will not be converted or saved between form building methods. 

### Expression tree builder 

The expression tree builder allows you to select the element, operator, and matching criteria for your form rule conditions from available options. You can build many conditions using the expression builder and create parent and subset conditions by nesting conditions beneath another. You can select the actions you’d like your condition(s) to trigger using the expression builder as well.

### Formula builder

You can use the formula builder to create a formula for the form rule condition. You can insert fields and functions into the formula editor to build your formula and select the actions you would like your condition(s) to trigger.

### Building conditions – When 

Form rule conditions are logical expressions that must evaluate to true before the rule can run and trigger the action. Basically, when you build your form rule, you’re telling your Quickbase form that when this _condition_ happens then take this _action_. Conditions can be simple, or complex based on the available condition options:

#### When a user is or is not in a role

This condition is based on [user roles](https://helpv2.quickbase.com/hc/en-us/articles/15372235950228) you have designated in your app. You could create a rule with a condition that only triggers an action when the user is in a manager role to show confidential information not shared with individual contributors. You can learn more about how to create roles in your app in our [Create a new role](https://helpv2.quickbase.com/hc/en-us/articles/4570282908052) article.

#### When a field value

Field value conditions trigger the rule when the [field value](https://helpv2.quickbase.com/hc/en-us/articles/15369423074324) equals, contains, starts with, is greater than, is less than, includes a designated value, etc. This can be a value entered into the field that triggers the rule or a value entered into a different field. For example, you can create a condition that turns a column red when a user enters an end date that is more than 14 days from the value entered into the start date field.

You can create rules with singular or complex conditions. You can add additional conditions to any form rule by using the **Add condition** option. Form rules can be designed to run when any or all the conditions you select are true.       

### Choosing actions – Then 

When any or all the conditions you describe in your rule are true, the rule will trigger an action. Actions fall into two categories, presentation actions and data actions. Presentation actions make changes to what the form looks like or how users can interact with it and data actions makes changes to the data in the fields. You can add more than one action to each rule. You can choose from

#### Presentation actions

<table><tbody><tr><td>Action</td><td>Description</td></tr><tr><td>Show</td><td>You can choose to show a field, column, section, or page based on the conditions you describe.</td></tr><tr><td>Hide</td><td>You can choose to hide a field, column, section, or page based on the conditions you describe.</td></tr><tr><td>Require</td><td>Based on the conditions you select you can make certain fields, columns, sections, or pages a requirement users need to complete before saving a record.</td></tr><tr><td>Unrequired</td><td>You can make required fields un-required using this action. For example, if a user enters an amount in an estimate field you can create a rule that would make the purchase price un-required because the user may not have the exact purchase price amount at this point.</td></tr><tr><td>Make read-only</td><td>Make fields, columns, sections, or pages read-only based on the conditions you select.</td></tr><tr><td>Make editable</td><td>You can make read only fields, columns, sections, or pages available for edit by adding this action to a rule.</td></tr><tr><td>Display message</td><td>This action displays a custom message you create when the form rule conditions you set are true.</td></tr><tr><td>Prevent save</td><td>You may want to stop users from saving a record based on your set of conditions. For example, if you want to create a form with a required sales amount field and prevent the user from saving the form if the amount they enter is over $10k you can do this by making the field required and creating a rule that triggers&nbsp;the prevent save action when the value in the sales amount field is greater than 10k.</td></tr></tbody></table>

#### Change actions

<table><tbody><tr><td>Action</td><td>Description</td></tr><tr><td>Change label</td><td>Using this action you can change the label on fields, columns, sections, or pages to a label of your choice based on the rule conditions.</td></tr><tr><td>Set color</td><td>You can create a rule that will change the color of a column to the color of your choice when the rule is triggered.</td></tr><tr><td>Change value</td><td>With the change value action, you can change the value in a field of your choice to the value of your choice based on the form rule conditions you set.</td></tr></tbody></table>

You can create rules with one or many actions. You can add additional actions to any form rule by using the **Add action** option. Form rule actions run from first to last when any or all the conditions you select are true.

### When form rule conditions are false – Otherwise

You can see how form rules will behave when the form rule conditions you set are false by reviewing the otherwise section of the form rule panel. The form rule builder automatically reverses the actions selected for the rule to build an otherwise scenario. For example, if you build a rule with a condition that says when a user is in a manager role and is viewing a record, the rule should trigger an action to show material cost fields, the otherwise section for the form rule would read _when the condition is equal to false hide material cost field_.

The otherwise section is generated automatically and cannot be changed or deleted.

## Active and inactive rules

You can save both rules you are ready to deploy and rules you’re still editing by turning your rules on or off using the **Active/Inactive** toggle on the **Description and tags** tab of the form rule panel.

### Active rules

When rules are set to active they begin running as soon as the form is saved. It’s important to remember that toggling a rule to active does not save the rule and your progress will be lost if you navigate away from the form rule builder without saving. Active form rules run in order from top to bottom based on the order in the form rules list. If two or more rules have actions that apply to the same object (i.e. two rules that have a show or hide action on the same field), the top-most rule is run first. 

### Inactive rules

When rules are set to inactive they do not run or trigger actions in your form. When you save inactive form rules they are added to your form rule list, but are not run.