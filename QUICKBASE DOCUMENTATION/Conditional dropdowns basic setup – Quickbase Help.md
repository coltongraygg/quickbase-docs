## Conditional dropdowns basic setup

Before setting the conditional behavior property, complete these steps:

1.  Create three tables in your app.
    
2.  Create three one-to-many relationships among your tables.
    
3.  Enter some data.
    
4.  Modify field properties to set up your conditional field. The field properties let you define the conditions that determine what appears in the resulting dropdown.
    

Each of these steps is more fully explained in the tutorial below. You can follow the steps in this tutorial to set up the app used in the example above.

Note: While this is the most common and the recommended way to create conditional dropdowns, you can choose another method. [Click to learn how](https://helpv2.quickbase.com/hc/en-us/articles/4570400857620-Another-Option-for-Creating-Conditional-Dropdowns-).

## Tutorial: Creating an Employee HR app with conditional dropdowns

Follow this tutorial to set up an app that allows you to enter employee names, countries, and cities. The Add Employee form should contain a conditional dropdown, allowing you to filter the cities list based on the selection of the employee's country.

## Step 1: Create an app with three tables

While your actual app may include many more than three tables, to achieve the conditional dropdown shown in the example form, you need to create at least the tables and fields shown in the table below:

-   [How to create a table](https://helpv2.quickbase.com/hc/en-us/articles/4570404266004-Adding-new-tables-#table_from_scratch)
    
-   [How to create a field](https://helpv2.quickbase.com/hc/en-us/articles/4570374838292-Adding-new-fields-#add_field)
    

| 
table

 | 

Fields (all of type text)

 | 

Description

 |
| --- | --- | --- |
| 

Employees

 | 

-   Last name
    
-   First name
    

 | 

You'll record all information about each employee in this table.

 |
| 

Countries

 | 

Country

 | 

Use this table to store the names of all countries where your company has at least one office.

 |
| 

Cities

 | 

City

 | 

Use this table to store the names of all cities where your company has at least one office.

 |

## Step 2. Create three one-to-many relationships

Each of your tables needs to know something about at least one other table in your app:

-   Your Employees table needs to have access to the country and cities lists in the Countries and Cities tables, so that you can specify the appropriate country and city when entering an employee record.
    
-   Your Countries and Cities tables need to know about each other, so that you can pair each city with the appropriate country.
    

So, you should set up these three relationships:

![](https://helpv2.quickbase.com/hc/article_attachments/4572812196756/employeeapparelationships.png)

The relationships should be set up this way because:

-   One country has many cities
    
-   One country has many employees
    
-   One city has many employees
    

How reference fields help you with conditional dropdowns:

Once you've [created these relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-), you should see these reference fields:

| 
when you create this relationship...

 | 

this reference field is created in the details table

 | 

How the field helpS you create conditional dropdowns

 |
| --- | --- | --- |
| 

Countries ![](https://helpv2.quickbase.com/hc/article_attachments/4572827275540/relationship_icon.png) Cities

 | 

Related Country

 | 

Having the Related Country field in the Cities table lets you pair each city with a country.

 |
| 

Countries ![](https://helpv2.quickbase.com/hc/article_attachments/4572827275540/relationship_icon.png) Employees

 | 

Related Country

 | 

Having the Related Country field in the Employees table lets you associate each employee record with the right country.

 |
| 

Cities ![](https://helpv2.quickbase.com/hc/article_attachments/4572827275540/relationship_icon.png) Employees

 | 

Related City

 | 

The Related City field in the Employees table is your conditional field. Having this field in the Employees table lets you associate each employee with the right city. It also lets you set up conditional behavior that allows you to specify checking that the selection of the employee's country and then filter the Related City list accordingly.

 |

For now, just make note of the reference fields. You'll use these later in the process.

## Step 3: Enter data in your app

Populate your Countries and Cities tables as follows:

| countries | cities |
| --- | --- |
| 
Canada

 | 

-   Toronto
    
-   Vancouver
    

 |
| 

England

 | 

-   London
    
-   Westminster
    

 |
| 

France

 | 

Paris

 |
| 

United States

 | 

-   Boston
    
-   Chicago
    
-   New York
    
-   San Francisco
    

 |

## Step 4: Set conditional behavior properties for your conditional field

Remember that your goal is to create a form where you can enter employee information and be able to filter the City list based on the employee's country. You can see that your Employee table now contains these reference fields: Related Country and Related City fields. The field you want to define as conditional is the Related City reference field in the Employee table.

To set conditional behavior properties for your conditional field:

1.  Access the field properties of the Related City field in the Employees table.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572812229652/conditionalbehavior.png)
    
2.  Check The values in this field depend on a selection in another field. (Note: You'll see this option only in the field properties for Reference fields; if you don't see it, you may have chosen the wrong field by mistake.)
    
    Select fields to complete this statement: A selection in <field1> shows choices where <field1> = <field2>.
    
3.  Set these conditions:
    

1.  In the first field, select Employees: Country. This checks the value of the Employees: Country field to determine which cities to display.
    
2.  In the second field, select Cities: Country. This displays only those cities that belong to the country the user selected.  
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572819334548/QA_proxyfield.png)
    
3.  Click Save.
    

### Cleaning up your Employee form

Depending on the order in which you created your relationships, your Employee form may contain an extra field (City--Related Country). If this is the case, simply edit your form properties and remove the field from your form.

## Testing your conditional dropdown

Once you've completed these steps, you can test your conditional dropdown by adding a new employee.

To test the conditional dropdown:

1.  From the Employees table, click + New Employee in the page bar.
    
2.  Enter a Last name and First name.
    
3.  In the Country dropdown, select Canada.
    
4.  Click the Cities dropdown. Quickbase displays only the Canadian cities: Toronto and Vancouver.
    
5.  Select Toronto and click Save.
    

### Related topics:

-   [Conditional Dropdowns](https://helpv2.quickbase.com/hc/en-us/articles/4570365398036-Conditional-Dropdowns-)
    
-   [Another Option for Creating Conditional Dropdowns](https://helpv2.quickbase.com/hc/en-us/articles/4570400857620-Another-Option-for-Creating-Conditional-Dropdowns-)
    
-   [How To Add Cascading Dropdowns](https://helpv2.quickbase.com/hc/en-us/articles/4570407379604-How-To-Add-Cascading-Dropdowns-)
    
-   [About table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-)
    
-   [Designating reference proxy fields](https://helpv2.quickbase.com/hc/en-us/articles/4570306784404-Designating-reference-proxy-fields-)