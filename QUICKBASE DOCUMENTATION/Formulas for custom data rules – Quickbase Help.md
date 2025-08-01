## Formulas for custom data rules

With [custom data rules](https://helpv2.quickbase.com/hc/en-us/articles/4570135620884), you can write a formula at the table level to make sure invalid data isn’t allowed. The formula consists of conditions where the data is not valid and should not be saved. You use the If()function, listing each invalid condition and a matching error message to display for each.

For example, in your opportunities table, you may have business rules that a) you don’t offer discounts above 15%, and b) all deals worth more than $100k must have a signed contract. You could use this formula to enforce those rules:

```
If([Discount %] > 0.15,"Enter a discount of 15% or less.",[Opportunity $ Size] > 100000 and Length([Contract PDF]) = 0,"Deals worth more than $100k require a contract. Please upload the contract to save this deal.")
```

## Conditions

A condition is a scenario where the data your user is trying to save is not valid. Conditions can be as complex as your business needs, using “and”, “or”, as well as parentheses to describe multi-faceted conditions.

| Business need: To Prevent Users from | Formula condition |
| --- | --- |
| Entering an end date before the start date | `[End Date] < [Start Date]` |
| Entering a discount greater than 15% | `[Discount %] > 0.15` |
| Marking a project complete if it has open tasks | `[Status] = “Completed” and [# of Open Tasks] > 0` |
| Submitting a Mac issue to your PC support team | `[Issue Type] = “PC” and Contains([Description], “Mac”)` |
| Closing a deal worth more than $100,000 without uploading an attached contract | `[Opportunity $ Size] > 100000 and Length([Contract PDF]) = 0` |
| Updating an employee’s status to active if they have not signed their I9 form (marked with a checkbox field) | `[Employee Status] = “Active” and [Signed I9 Form?] = false` |

## Error messages

For each condition, you’ll need to write a custom error message to show to the user. For your data validation to be successful, your end users entering the data need to easily understand what the problem is and how they can fix it. See the examples below to avoid using error messages that are too vague.

**Note:** Since custom data rules use Quickbase formulas, you can use record data in your error message, as shown in the project example below.

| To prevent users from | Error message |
| --- | --- |
| Entering an end date before the start date | `“End date can’t be before start date.”` |
| Entering a discount greater than 15% | `"Enter a discount of 15% or less."` |
| Marking a project complete if it has open tasks | `"Project cannot be marked complete because " & [# of Open Tasks] & " are still open."` |
| Submitting a Mac issue to your PC support team | `"Can’t submit Mac questions to our Windows team. Please update Issue Type to Mac and re-submit."` |
| Closing a deal worth more than $100,000 without uploading an attached contract | `"Deals worth more than $100k require a contract. Please upload the contract to save this deal."` |
| Update an employee’s status to active if they have not signed their I9 form (marked with a checkbox field) | `"Employee cannot start working until they have signed their I9 form."` |

## Displaying all errors at once

If a record is invalid because it falls into several of your invalid conditions, the first error message in your list will be displayed. You can string error messages together to display all corresponding error messages for each invalid record.

```
var Text checkBackground = If([Employee Status] = "Active" and [Background Check Completed?] = false, "You must complete a background check before activating an employee");
```

Each text variable checks for one condition, and then the List()function strings all the error messages together into one longer error message.