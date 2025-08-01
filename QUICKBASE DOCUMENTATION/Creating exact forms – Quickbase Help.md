## Creating exact forms

Unsupported feature

Exact Forms are [no longer supported](https://community.quickbase.com/blog/the-qrew-blog-/exact-forms-is-being-retired/88688). Instead, check out [Document Creation](https://helpv2.quickbase.com/hc/en-us/articles/30225959071508)—our updated feature for easier document design and generation.  

-   Existing Exact Form Microsoft Word templates will continue to work indefinitely 
-   New accounts created after September 15, 2024 may not create Exact Form templates
-   In the second half of 2025, all accounts will lose the ability to create new Exact Form templates

An exact form is a template you use to insert Quickbase content into documents like letters and invoices.

Say you enter all your client contact information in Quickbase and now you want to put it to work. It's time to generate your quarterly sales letters. So how do you get your data out of Quickbase and into your form letter? You can easily generate documents like this by creating an **exact form**.

## How exact forms work

If you have permission to create an application, you can create exact forms. Using a special Microsoft Word template, you can insert Quickbase data directly into whatever document you create (like a letter, invoice or work order) and then print the document from within your Quickbase application.

To create exact forms, you download the exact forms template, open it in Microsoft Word, then enter your text—including field codes that Quickbase uses to insert data from your records. Each field code copies values from the field you choose, directly into your document. (If you ever generated a mail merge in a word-processing program, you've seen field codes in action.) When you finish, save the exact form in your Quickbase account and use it to print documents from there.

**Note:** Exact Forms is not compatible with realms that use SSO or have Two-Step Authentication enabled.

### Requirements

-   Microsoft Word for Windows to create exact forms. Word 2010 and later are supported.  
    Note: The template will not work if you try to use it with Microsoft Word for Mac.
    
-   Permission to create an application in Quickbase.
    
    **Note**: Although exact forms use the Quickbase API, they do not require [application tokens](https://helpv2.quickbase.com/hc/en-us/articles/4570313549972-Application-Tokens-). In fact, exact forms don't work with any app that requires tokens. If an app requires tokens, you see a blank page. If an app that you'd like to create exact forms for requires tokens, [disable tokens](https://helpv2.quickbase.com/hc/en-us/articles/4570338870420-Disable-Application-Tokens-) for that app.
    

### To create an exact form

1.  Download the [Quickbase Exact Forms template](https://www.quickbase.com/tools/QuickBase%20Exact%20Forms%202007.dotm) for Microsoft Word.  
    **Note**: If you need a 64-bit version of the template, please open a [new case with Customer Care.](https://helpv2.quickbase.com/hc/en-us/articles/4570259530644)
    
2.  Right-click the template you want and select **Save Target As** or **Save Link As** (varies by browser) from the shortcut menu.
    
3.  If your browser asks whether you want to open or save the file, click **Save**.
    
4.  Select a location for the **Quickbase Exact Forms** template. You can save it on your desktop or in any folder you want.
    
    Once you've selected a destination folder, click **Save**.
    
5.  Double-click the **Quickbase Exact Forms** template. Microsoft Word opens.
    
    If you have Word 2010, the yellow Message Bar appears with a shield icon. Click **Enable Content**.
    
    Note: You must select **trust all**, or at the very least, **enable this content** for the template to work.
    
6.  The document that appears contains some explanatory text which includes links to sample documents. Click one of the links to view a sample. To use it as a template, replace the field names with those from your table, then add the text that you want.
    
    Or, just work in the first document that opens, replace all the explanatory text with your own.
    
    Note: You must start with one of these templates because these files have built-in features that communicate with Quickbase and let you save the file there.
    
7.  Design and format the form. You can enter whatever text you want. Include field codes and formulas to draw in specific information from Quickbase. (These fields should all exist in the table to which you link the exact form in Step 8.)
    
8.  When you finish [customizing the exact form](https://helpv2.quickbase.com/hc/en-us/articles/4570263029140-Customize-an-Exact-Form-), click **Add-Ins > Save to Quickbase As**.
    
9.  A sign-in dialog box appears. Enter your Quickbase **User Name** and **Password**.
    
10.  If your app uses a custom URL, such as _mycompany.quickbase.com_, you must replace the text that Quickbase inserts in the **Quickbase Domain** field with your own custom domain.
    
11.  When you complete all fields, click **Sign In**.
    
12.  Select the table that contains the data that you want the form to use.
    
    From the **Quickbase Tables** list, select the name of the app and table that you want. If that table already has an exact form connected with it, the filename displays in the **Quickbase Exact Forms** box below the table list.
    
    Note:  You can save multiple forms in a table as long as you give each one a unique name.
    
13.  Enter a name for your form, for example, "Letter", then click **Save**.
    
    When you save your form, Quickbase generates multiple HTML pages—one for each record in your table. To store each file, the program automatically creates a Formula - URL field in the table you chose. This field is named **Print _Exact Form name_** (where _Exact Form name_ is the name of your form).
    
14.  Add the new Formula - URL field to any reports or forms where you want it to appear.
    
    Note: Quickbase automatically creates the Formula - URL field that hosts your exact form, but you must add this column/field to any custom forms or reports in which you want it to appear.
    
    In a table report, click the ![](https://helpv2.quickbase.com/hc/article_attachments/30463876977684) button in the column heading and select **Add a Column** from the menu. The new field contains a link that opens the finished product: a document containing information from your app.
    
15.  To open one of these exact form documents, display a report of your table or a specific record in the table and click this link.
    

### To print an exact form from Quickbase:

1.  Open a report or form that features this field, then click **Print Exact Form Name**.
    
    The page displays in a new browser window.
    
2.  Select **File > Print**.
    
    Quickbase Exact Forms print one record per document.
    

### To edit an existing exact form:

1.  Open the Quickbase Exact Form template file, then click **Add-Ins > Open from Quickbase**.
    
2.  Select the table that contains the exact form that you want.
    
3.  Select the form name, when it appears, then click **Open**.
    
4.  Complete one of the following tasks;
    
    To save the form in the **same** table, click **Add-Ins > Save to Quickbase**.
    
    To save the form to a **different** table, click **Add-ins> Save to Quickbase As**.:
    

### To view the exact forms in an app:

1.  Open an app, then click **Home**, then click **Settings**.
    
2.  Click **Pages**.
    

**Note:** If you display an exact form in an app that requires application tokens, only a blank page appears. If an app that you'd like to create exact forms for requires tokens, [disable tokens](https://helpv2.quickbase.com/hc/en-us/articles/4570338870420-Disable-Application-Tokens-) for that app.

### Related topics:

-   [Customizing an exact form](https://helpv2.quickbase.com/hc/en-us/articles/4570263029140-Customize-an-Exact-Form-)
    
-   [Editing a report](https://helpv2.quickbase.com/hc/en-us/articles/4570281029396-Edit-a-Report-)
    
-   [Editing an exact form](https://helpv2.quickbase.com/hc/en-us/articles/4570328955668-Edit-an-Exact-Form-)
    
-   [Deleting an exact form](https://helpv2.quickbase.com/hc/en-us/articles/4570282769172-Delete-an-Exact-Form-)