## Conditional dropdowns

A conditional dropdown is a list whose items depend on a selection in another field. These items change depending on what a user selects in another list. For example, a conditional dropdown for employees could list only certain cities because in another field, a particular country was selected.

A conditional dropdown is always a reference field created when you create relationships among tables. In the example above, there are really three tables and three relationships involved:

-   Employees table
    
-   Countries table
    
-   Cities table
    

When you establish relationships among your tables, Quickbase creates a number of reference and proxy fields in each of your tables. You'll see, in the tutorial that follows, that a reference field for City will be created in your Employees table after you have established the right relationships. This is the field you'll use to select a city for each employee. You'll tell Quickbase to make this field conditional, based on the selection of the employee's country.

### Turning on conditional behavior

You make a field "conditional" using the Conditional Behavior field property. Because conditional fields must be reference fields, you'll see this property only when you're editing reference field properties.

![](https://helpv2.quickbase.com/hc/article_attachments/4572812229652/conditionalbehavior.png)

Once you've turned on the The values in this field depend on a selection in another field property, Quickbase asks you to complete the statement which will specify the conditions for filtering the values in the dropdown. The first dropdown determines the choices displayed for the conditional field (set to Employees: Country in the image). The second dropdown is the field Quickbase uses to filter the values for the conditional field (Cities: Country in the image). Quickbase compares the values in this field with the user's selection in the first field. When you select the employee's Country, Quickbase returns only cities from that country.

Note that, in the example above, we've chosen proxy fields in the conditional dropdowns. When you're making selections in these dropdowns, you should be sure to choose the proxy field rather than reference fields. Reference fields may display a number, like a record ID. Proxy fields display values that are more useful to your users.

Note: List-user fields cannot be used in conditional dropdowns.

### Related topics:

-   [Conditional Dropdowns Basic Setup](https://helpv2.quickbase.com/hc/en-us/articles/4570293628436-Conditional-Dropdowns-Basic-Setup-)
    
-   [Another Option for Creating Conditional Dropdowns](https://helpv2.quickbase.com/hc/en-us/articles/4570400857620-Another-Option-for-Creating-Conditional-Dropdowns-)
    
-   [How To Add Cascading Dropdowns](https://helpv2.quickbase.com/hc/en-us/articles/4570407379604-How-To-Add-Cascading-Dropdowns-)
    
-   [About table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-)
    
-   [Designating reference proxy fields](https://helpv2.quickbase.com/hc/en-us/articles/4570306784404-Designating-reference-proxy-fields-)