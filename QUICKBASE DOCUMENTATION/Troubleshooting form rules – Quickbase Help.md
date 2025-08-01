## Troubleshooting form rules

Form rule issues and warnings alert you to poor-performing form rules that could prevent you from saving your form or cause your form to behave incorrectly.

In this article

-   [Review form rules with issues and warnings](https://helpv2.quickbase.com/hc/en-us/articles/16148473308692-Troubleshooting-form-rules#h_01HDM9WBBK21DRGQSM7Q7JQJ95)
-   [Performance issues and warnings](https://helpv2.quickbase.com/hc/en-us/articles/16148473308692-Troubleshooting-form-rules#h_01H1W0GDE9PZVY5HVFWX6PZA15)
-   [Optimizing performance](https://helpv2.quickbase.com/hc/en-us/articles/16148473308692-Troubleshooting-form-rules#h_01HDM9WBBMVKEQRSF99N9ZP43H)
-   [Conflicting rules and warnings](https://helpv2.quickbase.com/hc/en-us/articles/16148473308692-Troubleshooting-form-rules#h_01HDMA49Q5GZJ1X9B1X61BN9Y1)
-   [Missing values and warnings](https://helpv2.quickbase.com/hc/en-us/articles/16148473308692-Troubleshooting-form-rules#h_01HDMAKCD8BJRQK1HGE4R08JKZ)

## Review form rules with issues and warnings

Review your form rules for issues and warnings different ways including: 

-   Review the **Form rules** toggle in the page bar. If you have unsaved rules, rules with issues, or rules with warnings an icon displays. Select the **Form rules** toggle to open your form rule list where you can resolve the issue. 
-   Navigate to your form rules list to see if your rules have any issue or warning indicators in the **Status column.![Screenshot_2023-06-01_at_12.16.08_PM.png](https://helpv2.quickbase.com/hc/article_attachments/16146639539476)**

## Performance issues and warnings

To ensure the protection of all apps on our platform, Quickbase checks if your form rules may adversely impact performance. If we detect that rules may run inefficiently, you'll see an error message:

-   We found form rules that are causing you to reach 80% or more of your performance limit. Resolve the performance issues or turn off rules with performance issues and warnings.

You can't save your form until you have edited your rules to improve the efficiency or deactivated rules with performance issues and warnings.

We continue to check for performance when users interact with the form. In cases where rules exceed Quickbase algorithms, we will display a message:

-   Resolve performance issues or turn off rules with issues to save

## Optimizing performance

Optimizing your app's performance essential to giving you and your users the best experience. Here are some helpful tips:

-   Reduce the records in the first condition as much as possible to improve query speed, as conditions are processed sequentially.
-   Avoid using derived fields unless necessary. Derived fields require additional queries, permission checks, and calculations before evaluation.
-   Use exact matches whenever possible as "is equal to" matching operator will be quicker than using "contains."

Learn more about how you can optimize your app performance in our [Performance optimizer](https://helpv2.quickbase.com/hc/en-us/articles/4570391172884) help article.

## Conflicting rules and warnings

We check form rules for conflicts between their actions that could introduce unexpected behavior when the form rules are executed.

A conflict in form rules can happen when there are two opposite actions that are applied to the same form object. For example, there could be form rule A that shows the **Project Name** field and form rule B that hides the **Project Name** field. In this case, Quickbase flags the conflict.

Action conflicts involve actions like:

-   Show and Hide
-   Require and Unrequire
-   Make editable and Make Read-only 

Usually conflicts happen when:

-   Two or more form rules apply opposite actions on the same object.  
    When this happens, we display warning messages that tell you which form rules these are. These form rules also have a _Conflicting actions_ status. You can still save form changes with this warning.
-   Two or more actions within the same form rule apply opposite actions on the same object.  
    When this happens, we display an error message that tells you which form rule is affected. The form rules also have a _Conflicting actions_ status. You can't save form changes until you resolve this conflict.

## Missing values and warnings

We check form rules for missing elements that could cause unexpected behavior when the form rule is executed.

We show messages for issues including:

-   Missing form objects - we display a warning a message that explains which form rules are affected. These rules have a _Missing objects_ status. In the builder panel, you can find information about what part of an action needs more information. You can't save form changes until you add the missing information.
-   Missing fields in the condition tree - we display an error message that explains which form rules are affected. These rules have a _Missing field_ status. In the builder panel, you can find information about what part of the condition needs more information. You can't save form changes until you add the missing information.