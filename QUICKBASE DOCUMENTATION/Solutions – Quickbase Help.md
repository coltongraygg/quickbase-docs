> Access to this feature can change based on your Quickbase plan. Learn more about feature availability and plans in [Quickbase capabilities](https://helpv2.quickbase.com/hc/en-us/articles/21309804922004).

Solutions are a collection of apps and/or pipelines in a realm that app admins use for versioning. By creating a solution, users can take a backup snapshot of all the apps in the solution, which can be restored as needed. 

For example, if you have connected apps and pipelines that work together in a workflow, you can use a solution to manage them so that all components always remain compatible and the workflow is never broken. 

This article explains how to navigate Solutions and the required permissions. To learn more about creating and restoring versions, read [Versioning and Rollbacks](https://helpv2.quickbase.com/hc/en-us/articles/14153734546836).

In this article

-   [Accessing the Solutions tab](https://helpv2.quickbase.com/hc/en-us/articles/14153924852756-Solutions#01GW5AP4RN71D89FNEWGQWZMZT)
-   [Permissions](https://helpv2.quickbase.com/hc/en-us/articles/14153924852756-Solutions#01GW5AP4RN6BHW8FR9J9SEH0Z9)
-   [Navigating Solutions](https://helpv2.quickbase.com/hc/en-us/articles/14153924852756-Solutions#01GW5AP4RP0JYRR2Y3VHR6GXPV)
-   [Delete a solution](https://helpv2.quickbase.com/hc/en-us/articles/14153924852756-Solutions#01GW5AP4RP2KJR58E55FS4BXP5)
-   [Solutions Permission Matrix](https://helpv2.quickbase.com/hc/en-us/articles/14153924852756-Solutions#01H1RY784PADMQJBDKPRTD4048)

## Accessing the Solutions tab

In the global navigation menu, select **Solutions**.

![](https://helpv2.quickbase.com/hc/article_attachments/33171368955668)

**Note:** You may not have direct access to **Solutions**. If it isn't available, ask your account admin.

## Permissions

Access to **Solutions** is granted on the **Permissions** page of the **Admin Console**.

![sol3.png](https://helpv2.quickbase.com/hc/article_attachments/19681950260628)

The default value is OFF, but Realm/Account Admins are granted access automatically. 

**Note**:  if at least one account in a realm is on a Business or Enterprise plan, every account in the realm will be able to build solutions.

## Navigating Solutions

When you open **Solutions**, the grid with all the Solutions that you have access to is shown. Realm/ account admins see all solutions. Other types of users that have access to **Solutions** will see solutions they own or contribute to.

![sol1.png](https://helpv2.quickbase.com/hc/article_attachments/19681907852308)

When you click on a solution, a side panel is loaded with details of the solution and editing options for the solution. 

![sol2.png](https://helpv2.quickbase.com/hc/article_attachments/19681892152724)

The grid is sorted by **Last modified date** by default.

If you delete or remove apps from a solution, this does not affect your actual apps. Only the solution and versions will be deleted.

### Attributes of a Solution

The side panel has these sections that represent the attributes of a solution.

![icon.legends.png](https://helpv2.quickbase.com/hc/article_attachments/14164526616724)

### General

Any user that can see a solution can edit the general details of it.

<table><tbody><tr><td><strong>Label</strong></td><td><strong>Definition</strong></td></tr><tr><td><span>Name</span></td><td><span>Up to 250 characters.</span></td></tr><tr><td><span>Alias</span></td><td><span>Must be unique in the realm and cannot contain spaces. Up to 1000 characters.</span></td></tr><tr><td><span>Description</span></td><td><span>Up to 4000 characters.</span></td></tr><tr><td><span>Owner</span></td><td><span>The user who created the solution.</span></td></tr><tr><td><span>ID</span></td><td><span>An automatically generated ID unique within Quickbase platform.</span></td></tr><tr><td><span>Created Date</span></td><td>The date the solution was initially created.</td></tr><tr><td><span>Last Modified Date</span></td><td>The date the solution was last modified.&nbsp;</td></tr></tbody></table>

### Apps

This section shows the apps currently included in the solution, along with options to add or remove apps. In the app picker, contributors see app they are a manager of and can add them to the solution. Realm admins and super users can add any app in the realm. 

All contributors can remove any app from a solution.

![aps.sol.1.png](https://helpv2.quickbase.com/hc/article_attachments/14165580763668)

![](https://helpv2.quickbase.com/hc/article_attachments/14454492385044)

Important: An app can belong to one solution only.

### Pipelines

This section shows the pipelines currently included in the solution, along with options to add or remove pipelines. In the pipeline picker, contributors see add any pipeline they are the owner of and can add them to the solution. Realm admins and super users can add any pipeline in the realm.

All contributors can remove any pipeline from a solution.

![my.sol.new2.png](https://helpv2.quickbase.com/hc/article_attachments/16116943847828)

### Contributors

This section displays the contributors already in the solution with the option to add or remove them.

If you aren't a realm/account admin, you won't see all solutions, but you can be added as contributors to specific ones, so that you may contribute in them.

Only the solution owner or a realm/account admin can add or remove contributors in a solution.

![](https://helpv2.quickbase.com/hc/article_attachments/14454489846292)

![](https://helpv2.quickbase.com/hc/article_attachments/14454496321044)

## Delete a solution

If you are the owner of the solution or realm/account administrators, you can delete a solution. Click on the delete icon:

![solutionsdel.4.png](https://helpv2.quickbase.com/hc/article_attachments/14326541220500)

Click **Yes, delete** to continue:

![solutions4.png](https://helpv2.quickbase.com/hc/article_attachments/14326653336724)

## Solutions Permission Matrix

Permissions access to Solutions from the Admin console (in Permissions)

| 
**Quickbase Role**

 | 

**Solutions Role**

 | 

**Provisioning**

 |
| --- | --- | --- |
| 

**Realm Admin**

 | 

Solutions Admin

 | 

Automatic

 |
| 

**Account Admin (Full/Support)**

 |
| 

**Super User**

 |
| 

_None of the above_

 | 

Solutions User

 | 

Manual via Permissions page

 |

Actions that can be performed within the Solutions

<table><colgroup><col> <col> <col></colgroup><tbody><tr><td><strong>Solution Action</strong></td><td><strong>Solution Admin</strong></td><td colspan="2"><strong>Solution Owner*</strong></td><td><strong>Solution Contributor*</strong></td></tr><tr><td><strong>Create Solution</strong></td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td colspan="2"><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td>N/A</td></tr><tr><td>Delete Solution</td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td colspan="2"><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809569300" alt="X-mark.png"></td></tr><tr><td><strong>Add App</strong></td><td><p><strong><span>&nbsp; &nbsp; &nbsp;<img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"> </span></strong><strong><span>**</span></strong></p></td><td colspan="2"><p><strong><span>&nbsp; &nbsp; &nbsp;<img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"> </span></strong><strong><span>**</span></strong></p></td><td><p><strong><span>&nbsp; &nbsp; <img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"> </span></strong><strong><span>**</span></strong></p></td></tr><tr><td>Remove App</td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td colspan="2"><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td></tr><tr><td><strong>Add Pipeline</strong></td><td><p><strong><span>&nbsp; &nbsp; &nbsp; &nbsp;<img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"> </span></strong><strong><span>***</span></strong></p></td><td colspan="2"><p><strong><span>&nbsp; &nbsp; &nbsp; &nbsp;<img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"> </span></strong><strong><span>***</span></strong></p></td><td><p><strong><span>&nbsp; &nbsp; &nbsp; &nbsp;<img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"> </span></strong><strong><span>***</span></strong></p></td></tr><tr><td>Remove Pipeline</td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td colspan="2"><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td></tr><tr><td><strong>Add Contributor</strong></td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td colspan="2"><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809569300" alt="X-mark.png"></td></tr><tr><td>Remove Contributor</td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td colspan="2"><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809569300" alt="X-mark.png"></td></tr><tr><td><strong>Create Versions</strong></td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td colspan="2"><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td></tr><tr><td><strong>Execute Rollbacks</strong></td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td colspan="2"><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/16247809554708" alt="check_mark_32.png"></td></tr></tbody></table>

\*Owner/Contributor which are non-Solution Admins

\*\*Apps displayed in the dropdown are only ones where the user is assigned as the Manager, or they are Super User

\*\*\* Pipelines appearing in the dropdown are only ones created by the user, or all if they are realm admin