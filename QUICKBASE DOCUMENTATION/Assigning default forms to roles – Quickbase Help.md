## Assigning default forms to roles

You can control how your users:

-   edit
-   view
-   add

records in your app by assigning forms to roles. Assigning roles makes it easy to manage the flow of information while working with your team. For example, you might have a role for:

-   managers
-   individual contributors
-   senior management 

For a team that manages construction inventory, _managers_ may have a form that includes purchase order fields, _individual contributors_ may have a form that allows them to enter basic quantity and description fields, and _senior management_ may have a form that includes pricing information.

**Note:** You can also hide and show specific form elements using [form rules](https://helpv2.quickbase.com/hc/en-us/articles/15157249413396).

## Assign a form to a role

Open your table settings and select **Forms**. Find the **Set how different roles use these forms** options and select to expand the controls. Find the name of the role you’d like to change. You may need to [create a new role](https://helpv2.quickbase.com/hc/en-us/articles/4570282908052) and then come back to these controls to set forms for the role.

You can designate a form for the following actions:

<table><tbody><tr><td>View form (Full site)</td><td>Displays the form selected to users in this role anytime they view a record from this table across the app. If you do not make a choice in this column, the user in this role will see a Quickbase auto-generated form which contains all fields.</td></tr><tr><td>Edit form (Full site)</td><td>Displays the form selected to users in this role anytime they edit a record from this table across the app. If you do not make a choice in this column, the user in this role will see a Quickbase auto-generated form which contains all fields.</td></tr><tr><td>Add form (Full site)</td><td>Displays the form selected to users in this role anytime they add a new record from this table across the app. If you do not make a choice in this column, the user in this role will see a Quickbase auto-generated form which contains all fields.</td></tr><tr><td>Grid edit (Full site<strong>)</strong></td><td>Displays the form selected to users in this role anytime they edit a record in grid edit across the app. If you do not make a choice in this column, the user in this role will see a Quickbase auto-generated form which contains all fields.</td></tr><tr><td><p>View/Edit/Add form (Mobile)</p></td><td>Displays the form selected to users in this role anytime they view, edit, or add a record using a mobile device. If you do not make a choice in this column, the user see the default full site form.</td></tr></tbody></table>

**Note:** A user can have multiple roles with multiple assigned forms within an app. When that happens, Quickbase will choose a role, so the system can determine which form appears when the user edits, views, or adds records. To do this, Quickbase checks each role's priority and displays the form associated with the highest priority role.