## Create reports that prompt users for selection criteria

You may not always know what records your users want to see. You can create a report that prompts users to enter selection criteria for one or more fields. After a user selects the report, Quickbase presents a dialog box like the one shown below.

![](https://helpv2.quickbase.com/hc/article_attachments/31642580021396)

_In this case, Quickbase prompts the user to select a Project Phase. The user can  
select **<other...>** to type in another value or choose **<anything>** to see  
contacts for all companies._

After a user types in a value or makes a selection from a dropdown, Quickbase displays the report you designed, but includes only the records for the user's selection. Any type of report can prompt the user.

To create a report that prompts users to select or enter filtering criteria:

1.  [Create](https://helpv2.quickbase.com/hc/en-us/articles/4570327815572-Create-a-new-report-) or [edit](https://helpv2.quickbase.com/hc/en-us/articles/4570281029396-Edit-a-Report-) the report you want to prompt users.
    
2.  In the **Filters** section, select **Filter \[table noun\] records**.
    
3.  Select the field whose value the user will choose.
    
    From the dropdown list on the left, select the field you want the user to fill in.
    
4.  In the second column, select an operator.
    
    The value you choose here qualifies the value that the user will enter. For example, Date _**is**_ or Date **_is on or before_** are very different qualifiers.
    
    Whatever value you select, the user will see in the prompt, so they know exactly the report will return. ([Read more about operators](https://helpv2.quickbase.com/hc/en-us/articles/4570137000980-Filter-Records-).)
    
5.  In the third column, select **the value**.
    
6.  Tell Quickbase to ask the user by selecting **<ask the user>** from the dropdown list.
    
    Note
    
    Some field types will not show a dropdown list. In that case, you can type **\_ask1\_** into the text box.
    

## Prompting for Multiple Fields

When you have Quickbase ask users for _multiple_ values, you give you colleagues more tools with which to hone results:

A report that prompts the user for information in multiple fields looks like the one show in the following image.

Tip

As with any filtering or search operation, your users can search for records that match **any** of the words they enter. To do so, just separate the entries with the word **OR** (must be capitalized), as shown below:

![](https://helpv2.quickbase.com/hc/article_attachments/31642580026772)

_If you want to search for any of a few values within a dropdown field, select **<other>**.  
In the field that appears, type in each value separated by **OR** (must be capitalized)._