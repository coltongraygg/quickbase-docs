## Using Multi-select Text fields

Multi-select Text fields allow you to choose multiple text values for a single field, for example, locations for a project, areas of a product to demo, or events someone might attend at a conference.

<table><tbody><tr><td><img src="https://helpv2.quickbase.com/hc/article_attachments/4572822346900/multi_edit_form.png"><p><em>Multi-select Text field when <strong>editing </strong>a record.</em></p></td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/4572822357780/multi_view_form.png"><p><em>Values in a Multi-select Text field when <strong>viewing </strong>a record.</em></p></td></tr></tbody></table>

## Entering and editing data in Multi-select Text fields

Click the arrow on the right side of the field to display the dropdown. Search for a particular value in the dropdown, or scroll to find the value you're looking for. Searching within the field narrows the list of values to ones containing your search term. Select the checkbox next to a value to put it in the field. (Deselect the checkbox next to a value to remove it from the field.)

You can select up to 20 values for a single field.

The dropdown is also available from grid edit mode.

![](https://helpv2.quickbase.com/hc/article_attachments/4572822376596/multi_edit_grid.png)

### Adding a choice

If a Multi-select Text field has been configured to allow new choices, there will be an **<Add New Choice...>** entry at the bottom of the list of choices in the dropdown.

To add a new choice to the field, click **<Add New Choice...>**. Enter the new value in the dialog that appears, and click **OK**. The new value is added to the dropdown and selected for this field.

### Orphaned choices

If a value appears in red on a table report or in the Multi-select Text dropdown, it has been _orphaned_. An orphaned choice was once a valid value in the dropdown, and someone chose that value in a record. Afterward an app admin removed it from the list of choices, so it was no longer a valid value. In the example below, _Walpole_ is an orphaned choice. It only appears in the dropdown when editing records where it was previously selected as a value, and Quickbase makes its orphaned status visually distinct.

<table><tbody><tr><td><img src="https://helpv2.quickbase.com/hc/article_attachments/4572831205780/multi_edit_tablerpt.png"><p><em>Orphaned choice shown in a table report.</em></p></td><td><img src="https://helpv2.quickbase.com/hc/article_attachments/4572850899476/multi_edit_orphan.png"><p><em>Orphaned choice shown on a form.</em></p></td></tr></tbody></table>

## Importing data

To import data into a table containing a Multi-select Text field, first obtain or construct the data to be imported. Check your data values for the Multi-select Text field to make sure that:

-   Values are text only. No HTML or other markup is allowed.
    
-   Values for a single field are separated using semi-colons (;). If your data contains semi-colons, they must be escaped. If you're importing a spreadsheet, values for each field should appear in a single cell.
    
-   Values for each record are on a single line (or in a single row if you're importing a spreadsheet).
    

An example of data that is valid for import appears below:

`Abington; Hanover; Methuen; Walpole`

## Exporting data

If you export data from an app that contains Multi-select Text fields, you'll see that Quickbase exports the list of values separated by semi-colons.

The example below shows you how an export of a record containing a Multi-select Text field called _Active Locations_ might look:

`Company,Contact Name,Project Name,**Active Locations**,Project Manager,Priority,Status,Start Date,# Tasks,# Messages,# Documents`

`Northeast Craft Air,Henry Beland,Deploy Document Management,**North Adams;Pittsfield;Sturbridge**,Gregory Baxter <1004.bfc9>,Medium,In-Progress,09-08-2015,8,1,0`

## Printing reports

When you print a report with records containing a Multi-select Text field, you'll see that the values are separated by semi-colons. See the _Active Locations_ column in the image.

![](https://helpv2.quickbase.com/hc/article_attachments/4572843946900/print_multitext.png)

### Related topics:

-   [Includes and Does not include](https://helpv2.quickbase.com/hc/en-us/articles/4570261800084-Filtering-records-using-fields-with-multiple-values-)
    
-   [Basic field information](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-About-field-types-)