## Setting up a vCard field

**Note**: **vCard** fields have reached [End of Support](https://helpv2.quickbase.com/hc/en-us/articles/4570319163156).

Quickbase offers integration with the **vCard** standard for exchanging addresses and contact information.

When you add the vCard feature to your application, users can click an icon on Quickbase forms or reports to download a set of basic contact information. Users can save it as a .vcf file or they can use a program like Outlook to open and save it in their own email contacts list. When you email a record that contains a vCard field (via a notification or by clicking the record's **email** button), Quickbase sends the .vcf file as an attachment the recipient can save.

To configure the vCard field:

1.  Open the vCard field's properties.
    
2.  Associate vCard fields with corresponding fields from your contacts table.
    
    The vCard contains contact fields, just like your contacts table does. You must match up your contact information fields with vCard's fields. That way, the vCard knows what fields to extract and group into its portable format and also what to call them. Within the **vCard field options** section, click each dropdown and select a field from your table that contains the corresponding information. For example, in the **Name** dropdown, select a field like Contact Name (You must select a text type field.) Match up phone number fields and pieces of address information.
    

## Using a vCard field as a lookup field

A vCard field will work as a lookup field. Say you want to add the vCard field next to your Task table's **Assigned To** field so users can easily send or copy contact information. To get it there, [create a lookup field](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-) that displays in Tasks. The vCard field functions the same way when it's a lookup field. Users just need to click the icon to open or download contact information.

### Related topics:

-   [Setting up an iCalendar field in Quickbase](https://helpv2.quickbase.com/hc/en-us/articles/4570324787988-Set-Up-an-iCalendar-Field-)
    
-   [Creating lookup fields](https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-)