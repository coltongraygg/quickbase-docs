Create rules to control how your form looks and behaves. Form rules have one or more conditions that trigger one or more actions of your choice. For example, a form that tracks food inventory for a restaurant might include a rule to ensure the team avoids running out of items. You can build a form rule that requires users to enter purchase order information when the value in the quantity field is less than 50 units. 

In this article

-   [Create a form rule](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM4VNFHWF7JK65GA9NZ)
-   [Describe and organize your rule](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM4AN5V39EZ2C97G783)
    -   [Name your rule](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM4S4M3C877V19Q4RD9)
    -   [Add a description](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM4NYRR01D9F21KK5YR)
    -   [Add or create tags](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM4A54RAQSK868WPXP4)
-   [Choosing a form rule building method](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM49ZF30VZ4DTXACS8G)
-   [Define form rule conditions - When](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01H153HD134AG9TBVFQ176RA4Y)
    -   [Form rule condition elements](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM4X7B3B5KQVMM17JH1)
    -   [Create a form rule condition with the formula builder](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM47B54E6QMDYN7TK20)
    -   [Create a form rule condition with the expression tree builder](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM4ARKQBRV1PP7NGDTF)
    -   [Parent and subset conditions](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01H26MM8XTA3TDJ73MWHZ3A5ZX)
-   [Select actions to trigger when your rule conditions are true – Then](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM4MT7X77X0GN1JCJNQ)
    -   [Actions](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM5798JXA0C3RM7A6TV)
-   [When form rule conditions are evaluated as false – Otherwise](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM52ACT18BV9M2HC7FK)
-   [Form rule run options](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM5FJP8Q718S5HE08V6)
    -   [Run change actions when a condition changes from false to true](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM5XXRTPNC9BD1JRPMS)
-   [Set rules as active or inactive before saving](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM50TNKSXC9TKF0ESTJ)
    -   [Active rules](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM5DS3XDFPHG8K42KY5)
    -   [Inactive rules](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM592AYX00RBEEAZAYM)
-   [Saving your form rules](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01HC0SVEM5MK7JHFXTM3T1V8N2)

## Create a form rule

You can create a form rule by selecting an on the design page, or opening the form rule builder.

1.  Use the **Create rule** or **Create a form rule** button to start building rules for your form.
2.  Select the **Description and tags** tab in the form builder panel.
3.  Add a name and description to document the purpose of the rule

Delete form rules on the form rules page using the Delete rule action.  
![](https://helpv2.quickbase.com/hc/article_attachments/33355858444820)

## Describe and organize your rule

### Name your rule

Use the edit button to change the name of your rule on the **Expression tree** tab.

Each of your rules are automatically named **Untitled rule** with a number that indicates the order in which it was created, for example your first rule is titled **Untitled rule** and your next rule is titled **Untitled rule 2.**    

### Add a description

Add a description to your rule to document the purpose or function of the rule. Type the description you would like to add to your rule in the description field. Your description will be displayed beneath the form rule name in the form rules list. You can view the full description by returning to the **Description & tags** tab.

 ![an example of a rule name and description. The rule description displays directly below the rule name The rule name is Rule 1 and the description is This rule requires PO information when the item quantity is less than 50.](https://helpv2.quickbase.com/hc/article_attachments/20004030428436)

### Add or create tags

Tags can help you organize and manage multiple rules in complex forms. To create new tags:

-   Typing the label for the tag in the tag field
-   Select the add option

Your tags are stored, so when you create more rules for the form, you can search and select previously used tags in the tag field. 

View the tags added to your rules in the **Tags** column of the form rules list

## Choosing a form rule building method

Build your form rule by writing a formula with the form rule formula builder or by describing your conditions and actions in the expression builder. You can switch from the formula builder to the expression builder and back by selecting **Expression tree builder** or **Formula builder** in the form rule panel.  
**Note**: Your data will not be converted or saved between form building methods.

## Define form rule conditions - When

Form rule conditions are logical expressions that must evaluate to true before the rule can run and trigger the action. For example, _when a user is in the manager role._ You can create simple conditions or create [parent conditions with subset conditions](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01H26MM8XTA3TDJ73MWHZ3A5ZX).

### Form rule condition elements

<table><tbody><tr><td><p>When a user is or is not in a role</p></td><td><p>This condition is based on user roles you have designated in your app. You could create a rule with a condition that only triggers an action when the user is in a manager role to show confidential information not shared with individual contributors. You can learn more about how to create roles in your app in our <a href="https://helpv2.quickbase.com/hc/en-us/articles/4570282908052" target="_self">Create a new role</a> article.</p><p>For example, <em>when a user is in the manager role...</em></p></td></tr><tr><td>When a field value</td><td><p>Field value conditions trigger the rule when the field value equals, contains, starts with, or includes a designated value. This can be a value entered into the field that triggers the rule or a value&nbsp;entered into a different field. For example, you can create a condition that turns a column red when a user enters an end date that is more than 14 days from the value entered into the start date field.</p><p>For example,&nbsp;<em>when the cost field is greater than $500...</em></p></td></tr></tbody></table>

### Create a form rule condition with the formula builder

You can use the formula builder to create a formula for the condition you’d like to use to trigger an action.

-   Select **Use the formula builder** button on the **Expression tree** tab of the rule panel to switch to the formula builder

![](https://helpv2.quickbase.com/hc/article_attachments/15348517592340)

In the formula builder, conditions are defined in the formula editor. You can select the field and function you’d like to add to the formula editor or start writing your condition formula from scratch in the formula editor. You can learn more about using formulas in Quickbase in our [Writing formulas](https://helpv2.quickbase.com/hc/en-us/articles/4889032261012) article. Keep in mind that formula conditions must output a boolean result:

-   Boolean formulas always produce one of two values — true or false.
    
-   Boolean values result from comparison operations, like `4<5`. For example, if you want your formula condition to compare two values when "the **Cost** field greater than the **Projected cost** field", the formula could look like this: `[Projected cost] > [Cost]`. The condition will either be true or false.

### Create a form rule condition with the expression tree builder

Use the expression tree builder to define your condition by selecting from a menu of options. ![2023-06-07_Image](https://helpv2.quickbase.com/hc/article_attachments/16263890717076)

Your menus adjust to only show the available options for your condition as you make your choices.

-   Make a choice between any and all to tell your rule how you would like your conditions to be evaluated. When **All** is selected, each of the conditions in the rule will need to be evaluated as true to trigger the action. When **Any** is selected, any of the conditions in the rule will need to be evaluated as true to trigger the action
-   Choose an [element](https://helpv2.quickbase.com/hc/en-us/articles/15342169525396-Create-a-form-rule#h_01H153HD134AG9TBVFQ176RA4Y), would you like your condition to be based on the user’s role or a field value?
-   Select your operator and matching criteria. For example, you might select _the user_ as the element, then _in this role_ as the operator, and _viewer_ for the matching criteria. ![Screenshot](https://helpv2.quickbase.com/hc/article_attachments/16263890719892)

You can decide to deploy the rule actions if any or all of the conditions you define are true. If you have a form section you’d like to display to users in a manager role or an assistant manager role you could create a condition for when the user is in a manager role and a condition for when the user is in the assistant manager role and select _any of these conditions are true_ and the rule will display the section when the user is either a manager or an assistant manager. ![Screen](https://helpv2.quickbase.com/hc/article_attachments/16263874324244)

Add additional conditions to your rule by using the **Add condition** option. Your conditions will be evaluated in order from top to bottom as they appear in the expression builder. You can reorder and delete each condition by using the condition action menu.

### Parent and subset conditions

Create a hierarchy with the conditions your form rule validates by nesting conditions as subsets under parent conditions. When the parent condition is true, the subset condition is validated. To nest form rule conditions:

## Select actions to trigger when your rule conditions are true – Then

After you have described your conditions, it’s time to select the actions the rule triggers when any or all the conditions are true. Actions can make changes to what the form looks like, how users can enter and view data, and makes changes to the data in the fields. You can add one or more actions to each rule.

### Actions

<table><tbody><tr><td>Show</td><td>You can choose to show a field, label, column, section, or page based on the conditions you describe.</td></tr><tr><td>Hide</td><td>You can choose to hide a field, label, column, section, or page based on the conditions you describe.</td></tr><tr><td>Require</td><td>Based on the conditions you select you can make certain fields, columns, sections, or pages a requirement users need to complete before saving a record. <span>W<span>hen a page, section, or column is required, all fields within must be filled with an accepted value.</span></span></td></tr><tr><td>Unrequired</td><td>You can make required fields un-required using this action. For example, if a user enters an amount in an estimate field you can create a rule that would make the purchase price un-required because the user may not have the exact purchase price amount at this point.</td></tr><tr><td>Make read-only</td><td>Make fields, columns, sections, or pages read-only based on the conditions you select.</td></tr><tr><td>Make editable</td><td>You can make read only fields, columns, sections, or pages available for edit by adding this action to a rule.</td></tr><tr><td>Change label</td><td>Using this action you can change the label on fields, columns, sections, or pages to a label of your choice based on the rule conditions.</td></tr><tr><td><p>Set color</p></td><td>You can create a rule that will change the color of a column to the color of your choice when the rule is triggered.</td></tr><tr><td>Display message</td><td>This action displays a custom message you create when the form rule conditions you set are true. You can learn more about the types of display messages you can choose from in our <a href="https://helpv2.quickbase.com/hc/en-us/articles/16264688328596" target="_self">Form rule display message action</a> article.</td></tr><tr><td>Prevent save</td><td>You may want to stop users from saving a record based on your set of conditions. For example if you want to create a form with a required sales amount field and prevent the user from saving the form if the amount they enter is over $10,000 you can do this by making the field required and creating a rule that triggers the prevent save action when the value in the sales amount field is greater than 10,000.</td></tr><tr><td>Change value</td><td>With the change value action, you can change the value in a field of your choice to the value of your choice based on the form rule conditions you set. You can also change the target field to the value in another field.</td></tr></tbody></table>

Form rule action availability is based on the conditions you define. You can add additional actions to your form rule by using the **Add action** option. Form rule actions run from first to last when the conditions you select are evaluated as true. 

## When form rule conditions are evaluated as false – Otherwise

You can see how form rules will behave when the form rule conditions you set are false by reviewing the otherwise section of the expression builder. The form rule builder automatically reverses the actions selected for the rule to build an otherwise scenario. For example, if you build a rule with a condition that says when a user is in a manager role and is viewing a record, the rule should trigger an action to show material cost fields, the otherwise section for the form rule would read _when the condition is equal to false hide material cost field_.

The otherwise section is generated automatically and cannot be changed or deleted.

## Form rule run options

Form rules can be set to run when you decide. Your form rule run options are based on the conditions you define and action you select.

<table><tbody><tr><td>Form rule run option</td><td>Description</td><td>Related actions</td></tr><tr><td>Changes a field value</td><td>Triggers the rule to run when a value is changed in a record's fields</td><td>All actions</td></tr><tr><td>Saves a record</td><td>Triggers the rule immediately after the user selects&nbsp;<strong>Save.</strong></td><td>Change value, prevent save</td></tr><tr><td>Saves a record after validating</td><td>Triggers the rule immediately after the user selects&nbsp;<strong>Save </strong>and Quickbase validates the values entered in required fields.</td><td>Change value, prevent save</td></tr><tr><td>Opens a record to edit or adds a record</td><td>Triggers the rule immediately when the record is opened or when a new record is added</td><td><p>Display a message</p></td></tr></tbody></table>

### Run change actions when a condition changes from false to true

When you select **change value** as your form rule action you can specify when the value is changed using the **Run change actions when a condition changes from false to true** option. When the **run change actions when a condition changes from false to true** option is applied, the change value action is only taken when the condition changes from false to true instead of being applied to existing records in the table.  

For example, if you’re creating a rule for your inventory form to display a purchase order section when the quantity of an item falls below 50 units, you wouldn’t want the purchase order section to display when a user is adding a new record for an inventory item that only has 40 units. You would only want to apply the rule to inventory units that change from a number greater than 50 to a number less than 50. In this case, you would use the run change actions when a condition changes from false to true option to only apply the rule to inventory records that have a number that is greater than 50 units and changes to a number that is less than 50 units. 

## Set rules as active or inactive before saving

You can choose to turn your rules on or off by using the **Active/Inactive** toggle in your form rule list or on the **Description and tags** tab of the form rule panel.

### Active rules

When rules are set to active they begin running as soon as the form is saved. It’s important to remember that toggling a rule to active does not save the rule and your progress will be lost if you navigate away from the form rule builder without saving. If two or more rules have actions that apply to the same object (i.e. two rules that have a show or hide action on the same field), the top-most rule is run first. 

### Inactive rules

When rules are set to inactive they do not run or trigger actions in your form. When you save inactive form rules they are added to your form rule list, but they do not run. You can run an inactive rule by toggling to **Active** in the form rule list or on the **Description and tags** tab of the form rule panel.

## Saving your form rules

When you’re done building your rules, select the **Done** option in the form rule panel to close the panel. If the **Done** option is inactive you may have to solve issues with the form rule formula or performance before you can close the panel. Learn more about form rule issues and how to solve them in our [Troubleshooting form rules](https://helpv2.quickbase.com/hc/en-us/articles/16148473308692) article.

You need to save your form to save your changes to the form rules. You can select **Save** or **Save & keep working** to save your form rules and run your active rules.