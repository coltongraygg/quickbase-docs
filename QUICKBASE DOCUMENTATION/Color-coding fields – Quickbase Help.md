## Color-coding fields

In Quickbase, you can [add color-coding](https://helpv2.quickbase.com/hc/en-us/articles/4570255561108-Color-coding-fields#h_01FYPPEBRZ2ZBKBKA5WQHSVQP4) to a table report, Kanban report, or calendar. You can also color code individual fields, which can affect reports as well as forms. You can use formulas to do this, so the color in a field updates based on other values, like priority or completion. This can help you prioritize your work or communicate important information to your end users.![](https://helpv2.quickbase.com/hc/article_attachments/4572816809620)

_Color-coded fields in a report. The Current Priority field is a Formula-Rich-Text field. Its conditional formula says: If Priority is Urgent, make the background red._

  
![](https://helpv2.quickbase.com/hc/article_attachments/4572816829588)

_Color-coded field on a form._

## To color code a field

You can use a formula rich text field to add color to a field. You can also add color to the text in a field instead of the background.

1.  Create or select a formula rich text field.
    
2.  [Access the field's properties page](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-).
    
3.  In the Formula box, enter the formula to color code using a `<div>` tag. See examples in the table below.
    
4.  Click **Save**.
    
5.  Add the new formula rich-text field to reports and forms.
    

## Sample Text Formulas with HTML to color-code field backgrounds

Note

As shown in the examples, all formulas must use the spelling _color_ and not _colour._ 

| 
You want to...

 | 

Formula

 | 

Notes

 |
| --- | --- | --- |
| 

Show value from the **Priority** field with the background always in **pink**.

 | 

<div style=\\"background-color:pink;\\">"& \[Priority\]&"</div>

 | 

This code will display the value from the Priority field on a pink background.

Wherever HTML calls for a quotation mark, you must precede it with a backslash (\\), so Quickbase does not mistake it for the start or end of a literal in the Quickbase formula language. ([Read more about literals and the backslash](https://helpv2.quickbase.com/hc/en-us/articles/4839910743444).)

 |
| 

Show the value from the **Priority** field. Make the background red only if Priority is **_Urgent_**.

 | 

If(\[Priority\]="Urgent", "<div style=\\"background-color:red;\\"> Urgent</div>", \[Priority\] )

or, if you prefer to use a hex value:

If(\[Priority\]="Urgent", "<div style=\\"background-color:#FF0000;\\"> Urgent</div>", \[Priority\] )

Black text is hard to see on red. Make text white:

If(\[Priority\]="Urgent", "<div style=\\"color:white; background-color:#FF0000;\\"> Urgent</div>", \[Priority\] )

 | 

This formula says: If Priority is urgent, enclose the word "urgent" within a div with a red background. Otherwise, just show the value from the Priority field.

Again, wherever HTML calls for a quotation mark, you must precede it with a backslash (\\), so that Quickbase does not mistake it for the start or end of a literal in the Quickbase formula language. ([Read more about literals and the backslash](https://helpv2.quickbase.com/hc/en-us/articles/4839910743444).)

 |
| 

Color code each value from the **Priority** field with various shades of red.

 | 

Case(\[Priority\], "Urgent", "<div style=\\"color:white; background-color:#FF0000;\\"> Urgent</div>",  
"High","<div style=\\"background-color:#FF6666;\\"> High</div>",  
"Medium", "<div style=\\"background-color:#FF9999;\\"> Medium</div>",  
"Low","<div style=\\"background-color:#FFCCCC;\\"> Low</div>", "")

 | 

Use a [Case() function](https://helpv2.quickbase.com/hc/en-us/articles/4893082972180) when you're dealing with values in the same field.

White text is appropriate for red but not for the other colors.

 |

### Related topics:

-   [Color-coding](https://helpv2.quickbase.com/hc/en-us/articles/4570391002260-Color-coding-in-reports-)
-   [Using Formulas in Quickbase](https://helpv2.quickbase.com/hc/en-us/articles/4839910743444)
    
-   [Troubleshooting Formula Errors](https://helpv2.quickbase.com/hc/en-us/articles/4570267666836-Troubleshoot-Formulas-)
    
-   [Formula Functions Reference](https://www.quickbase.com/db/6ewwzuuj?a=q&qid=6)