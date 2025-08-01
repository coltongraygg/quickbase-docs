So you've snapped and posted photographs of all your Hummel collectibles and you'd like to share them with the world. Of course, you've inventoried your entire collection in a Quickbase. Now, you want to connect each record with its corresponding image, but the images all live on your "Hot Hummels" Web site. Sure, you could create a [file attachment field](https://helpv2.quickbase.com/hc/en-us/articles/4570363435668-About-Document-Management-) to store and show images within each Quickbase record, but you'd rather not store them in two places.

URL fields to the rescue! Quickbase **URL** and **Formula - URL** fields let you store and compose links that deliver whatever page you wish to the viewer's browser. The URL field type you choose, depends upon what you'd like to do:

-   When you want users to type in an entire URL for a record they're entering, create a **_plain URL field_**. For example, say users are entering company information into your Quickbase. A URL field lets them enter the company's Web site address. Once they save, Quickbase displays the field as a link that delivers the Web site to any viewer.
    
-   When you want users to enter part of a URL (like the image file name of a Hummel figure on your Web site) use a **_Formula-URL field_**. You can compose the formula field to always include the start of your Web site's URL. When you create another field (something like _Image Name_) then you or a viewer can use it to enter only the file name that completes the URL. Format your URL formula field to concatenate (string together) the start of the URL and whatever file name lives in the Image Name field to get a custom URL for each record.
    

**FAQ - What if I want all records to show the same URL?**  
If you want each record to contain a link to one particular Web site, create a plain URL field. Open the field's properties page and set the **Default value** to be whatever URL you want. Save changes. Add the field to forms or reports and make it a "Read-only" type field. That way, the one address you entered appears to each viewer, but no one can edit it.

To create a plain URL field:

1.  Create the URL field.
    
    [Add a new field](https://helpv2.quickbase.com/hc/en-us/articles/4570374838292-Adding-new-fields-). Name it something like "Company Web site" or whatever describes the type of URL that users will enter. Select **URL** as the field type. When prompted, add the field to forms where you want it to appear.
    
2.  [Open the field's properties page](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-).
    
3.  Set URL display preferences.
    
    Your URL field doesn't necessarily need to show a huge URL that's hard for average readers to parse out. Instead, the link it displays can contain a more informative label like "Company Web site" or "View product image" or whatever you want. To show more descriptive text, enter the term you want in the Display section's Link text  field.
    
    You can also tweak format with the following options:
    
    -   **Don't show 'http://' when showing the URL.** Turn on this checkbox to shorten the URL to a more digestible length by removing extras from the beginning. So, instead of **https://myaccount.quickbase.com**, viewers would see only **myaccount.quickbase.com**. Or, if your URL ends with a file name, Quickbase displays only the file name.
        
    -   **Display as a button.** If you really want to emphasis to users that they can "click here" to see a picture or related Web page, then turn on this checkbox to display the URL field as a button instead of a blue underlined link.
        
    -   **Open target in new window.** If you don't want viewers to stray away from your Quickbase application, turn on this checkbox. When you do, the URL field's link opens a new instance of the browser in which to display the link's destination. The Quickbase screen from which viewers launched the link still displays underneath the new window.
        
4.  When you're done setting preferences, click **Save**.
    

When editing a record, app users will be able to enter Web addresses in the new URL field. When viewing a record, the URL field appears as a link or button.

To create a Formula - URL field:

1.  Create a field to contain the portion of the URL that users enter.
    
    Create a Text field ([read how to add a field](https://helpv2.quickbase.com/hc/en-us/articles/4570374838292-Adding-new-fields-)) in which users can enter a portion of your URL. For example, this may be an image file that lives on the Web or an HTML page that contains information relevant to the record. Add this field to forms on which it should appear.
    
2.  Add a Formula - URL field to the same table.
    
3.  [Open the field's properties page](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-).
    
4.  Compose the formula.
    
    Within the Formula box, type the formula that generates the link that this field will display. This formula should begin with the start of your URL in quotes, followed by an ampersand and then a field reference to the field whose value completes the address. For example:
    
    "http://www.example.com/images/" & \[Image Name\]
    
5.  Set display preferences.
    
    Formula-URL fields offer the same display settings as plain URL fields. To learn about all your options, please read Step 3 in the preceding section.
    
6.  Click **Save**.
    
    Now whenever a user enters a file name in the field you created in Step 1, Quickbase automatically generates a working URL that opens that file in a viewer's browser.
    

Note: If your Formula-URL field includes an API call and your application requires [application tokens](https://helpv2.quickbase.com/hc/en-us/articles/4570313549972-Application-Tokens-), you'll need to insert the appropriate token in the API call. (API calls and app tokens are not available to accounts on the Quickbase Essential plan.)

## Formulas and workflow

Many users find the formula URL fields to be extremely valuable because they make it easy to design complex workflows, for example, when you are using formulas such as URL field buttons like, **Add Task**, **Add Document**, or **Add Project**. It doesn't matter if records are child or parent records you are creating, only that you are leaving one location to manually add or edit a record and you wish to return back to the location from which you started.

### Workflows that require user input

When creating a relationship, Quickbase automatically generates an "Add Record" Formula - URL field. In the field itself,`"&z="&Rurl()`is added to the field when the relationship is created. This provides a quick way for users to create a child record.

There are three valid use cases for `"&z="&Rurl()`. One is when you use `API_GenAddRecordForm` and the second is when you use the `a=er` function to edit a record, and the third is using `DoRedirect` within an API button to return to the page you started on. In both cases, you would manually modify a record, save the record, and return back to the URL from which you started. Here's an example using `API_GenAddRecordForm`:

```
URLRoot() & "db/" & [_DBID_TASKS] & "?act=API_GenAddRecordForm&_fid_48=" & [Record ID#] & "&_fid_8=" & [Est Start Date] & "&z=" & Rurl()
```

And here's an example using `a=er:`

```
>URLRoot() & "db/" & Dbid() & "?a=er&rid=" & URLEncode([Record ID#]) & "&dfid=12" & "&z=" & Rurl()
```

The thing to remember about the above two examples is that you are starting from one spot, either adding or editing a record, manually saving the record and returning to your starting spot. The `"&z="&Rurl()`only works in this situation.

### Workflows that do not require user input

If you are using another API call such as `API_AddRecord` or `API_EditRecord`, the format for redirecting to another page is different. In this case, you can redirect the final API call in your formula to an `a=doredirect` URL. This takes the z=rurl() concept and makes it more valuable, since it allows you to make one or more API calls, and then reload the current page. For example:

```
URLRoot() & "db/" & [_DBID_TASKS] & "?a=API_EditRecord&rid=" & [Record ID#] & "&_fid_7=Approved" & "&rdr="&URLEncode(URLRoot() & "db/" & Dbid() & "?a=doredirect&z=" & Rurl())
```

You can also use `rdr` to redirect the user to a specific page. For example, after a new record is created, perhaps you want to display a "thank you" rich text page you've created. This thank you page should appear as the next step in the workflow, if the user was on the app dashboard before they created the record, or if they came from the table home page. For example:

```
URLRoot() & "db/" & [_DBID_TASKS] & "?a=API_EditRecord&rid=42&_fid_7=Approved"&"&rdr="&URLEncode(URLRoot() & "db/" & Dbid() & "?a=dbpage&pageID=30")
```

## Features when working with formula-url text fields

The features and capabilities include:

-   When you open a formula url as a pop-up, you can set a website to open in a popup window or a new tab.
    
-   You can embed a secure, external website as an iframe on a form. You can use this feature to embed YouTube videos or other file services (Box, Drive, etc.) as a file preview. For security purposes, the only .quickbase.com URLs are allowed for code pages. All other .quickbase.com URLs do not function when embedded on a Quickbase form.
    
    **Note**: The limits and restrictions of iframes are due to third party limitations, not because of Quickbase.
    
-   You can refresh the source page when a popup is closed using the `data-refresh` parameter.
-   You can customize the size of a popup using the `data-width` and `data-height` parameters
    
    Here’s an example that uses these two features in combination with the OpenAsPopup class:  
    `"<a class='Vibrant Success OpenAsPopup' data-height=200 data-width=200 data-refresh=true href='" & [url] & "'>Click here</a>"   `
    
    -   Use record ID# as a parameter when you click a custom hyperlink from an add record form. This lets you leverage _newly_ created record IDs and expands custom code page workflow options. Use record ID# in formulas with `data-replacerid=true` and `%%rid%%` where you would like the RID.
    -   **Note**: You can only use this parameter when the hyperlink navigates to the same tab, not when it is set to open in a new tab or popup.

The properties for this field type are:

## Label

Enter a name for this field. This name displays on data-entry forms and as column headings in reports.

## Type

Click Change Type to change the field type.

Some field types (List-User, Multi-select Text, and File Attachment, for example) may not be changed. The **Change Type** link will not be present if this is the case.

**Related Topic:**

-   [About Field Types](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-About-field-types-)

## Unique

| 
Select this option...

 | 

If you want to...

 |
| --- | --- |
| 

Must be unique

 | 

Ensure that every entry in this field is different.

This is useful for fields that contain information such as product serial numbers or ID numbers.

 |
| 

Check existing entries for duplicate values

 | 

Change a field in an existing application to require unique values and want to require that all previously entered data is unique.

To display this option, select **Must be unique**.

If Quickbase finds existing values in this field that aren't unique, an error message appears and Quickbase clears the **Must be unique** checkbox. If this occurs, you can do one of two things:

-   Sort the field to find duplicate values, make corrections as necessary, return to the Properties page, then select both **Unique** checkboxes again.
    
-   Select **Must be unique** if it doesn't matter whether existing data in this field is unique or if you want only new entries in this field to be unique.
    

 |

## Formula

Enter the formula to generate the value this field shows. When you click the Formula text field, a **Fields & Functions** list appears.

1.  Click **Select a Function** to open the Quickbase Formula Functions dialog box.
    
2.  Select or search for the type of function you want from the list.
    
3.  Click the formula that you want, then click **Insert**.
    

**Related Topics:**

-   [Using Formulas in Quickbase](https://helpv2.quickbase.com/hc/en-us/articles/4570376002580-Using-Formulas-in-Quickbase-)
-   [Quickbase Formula Functions Reference](http://www.quickbase.com/db/6ewwzuuj?a=q&qid=6)

## Features when working with formula-rich text fields

The features and capabilities include:

-   When you open a formula url as a pop-up, you can set a website to open in a popup window or a new tab. You can use this same functionality with formula-rich text by applying the CSS class (`OpenAsPopup`).
-   Use the CSS class (`SaveBeforeNavigating`) inside of a formula-rich text field and Quickbase will save the record before navigating.  
    **Note**: Only one of these workflow classes is supported per formula-rich text.
-   Here’s an example of a formula-rich text field that uses this feature:
    
    `"<a class='Vibrant Success SaveBeforeNavigating' data-replacerid=true href='/db/abc?a=dr&rid=%%rid%%'>Click here</a>"`
    

### Related topics:

-   [About field types](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-About-field-types-)