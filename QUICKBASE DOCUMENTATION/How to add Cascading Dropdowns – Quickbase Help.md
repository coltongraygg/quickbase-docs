## How to add Cascading Dropdowns

You've learned how to create a simple conditional dropdown...but what if you wanted to take it one step further? What if you wanted to develop the form below?

![](https://helpv2.quickbase.com/hc/article_attachments/4572884152084)

The good news is that, if you know how to set up a single conditional dropdown, you know how to set up cascading dropdowns.

## How to create Cascading Dropdowns 

To add a conditional Departments field to your Employee form, follow the [tutorial for setting up a conditional dropdown](https://helpv2.quickbase.com/hc/en-us/articles/4570365398036) and add these steps:

1.  Add a Departments table.
    
2.  Set up these relationships:  
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572862107028)  
    **Note**: These relationships will establish a conditional Department dropdown on the Employee form. You can also set up conditional behavior on the Departments form so that users can first choose a country to see a filtered list of cities. If you'd like to do that, simply follow the steps for creating a single conditional dropdown.
    
3.  Set the Conditional values property for the Employees: Related Department field as follows:  
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572862136980)
    
4.  Quickbase now filters the department list on the employee form, so that you see only those departments located in the selected city.
    

### Related topics:

-   [Conditional Dropdowns](https://helpv2.quickbase.com/hc/en-us/articles/4570365398036-Conditional-Dropdowns-)
    
-   [Conditional Dropdowns: Basic Setup](https://helpv2.quickbase.com/hc/en-us/articles/4570293628436-Conditional-Dropdowns-Basic-Setup-)
    
-   [Another Option for Creating Conditional Dropdowns](https://helpv2.quickbase.com/hc/en-us/articles/4570400857620-Another-Option-for-Creating-Conditional-Dropdowns-)
    
-   [About table-to-table relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-)
    
-   [Designating reference proxy fields](https://helpv2.quickbase.com/hc/en-us/articles/4570306784404-Designating-reference-proxy-fields-)