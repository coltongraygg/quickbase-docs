## Setting maximum length for entries in text fields

On occasion, you may wish to limit the number of characters end users can enter or store in a field. You can set a limit on the number of characters Quickbase accepts, but only for text type fields.

To set the maximum length for a text field:

1.  [Access the text field's properties page](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-).
    
2.  Under the **Display** section, within the Max characters field, type the number of characters you want to allow.
    
3.  Click **Save**.
    

Quickbase restricts future entries in this field to the number of characters you specify.

### FAQ: What if my text field already has information stored in it?

If you set a maximum length and there are existing entries in the field that exceed that length, those entries remain until the next time that record is edited. When you edit and try to save the record—even if you make no changes to the limited field—Quickbase displays an error asking you to shorten the offending entry.