## Making fields required

When you require a field, users can’t save a record until the value is entered. You can make a field required across your entire app or only when it appears on a special form.

## To require entries in a field across your entire app

You can require fields names using either field settings or [Visual Builder](https://helpv2.quickbase.com/hc/en-us/articles/4570376993300-Quickbase-Visual-Builder-).

### Using field settings to require fields

1.  [Open the field's properties page](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-).
    
2.  In the **Basics** section, select the **Must be filled in** checkbox:
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572829385620/require-fields.png)
    
3.  Click **Save**. Required fields are shown with a red asterisk next to the field's name on the fields page. For users, a red asterisk appears next to fields on forms to indicate that values are required.
    

### Using Visual Builder to require fields

1.  Open a table, click **Settings**, then click **Structure**. Visual Builder opens with the table expanded.
    
2.  Select the field you want to require, then use the field properties on the right to select the **Must be filled in** checkbox:
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572829406868/vb-require-fields.png)
    
3.  All changes are saved automatically.
    

## How to require entries in a field only when it appears on a particular form

1.  [Create](https://helpv2.quickbase.com/hc/en-us/articles/4570289798804-Create-a-Custom-Form-) or [edit](https://helpv2.quickbase.com/hc/en-us/articles/4570270668180-Edit-a-Custom-Form-) the form on which you want to make the field required.
    
2.  Select the field you want to require, then select the **Required** checkbox.
    
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572835565844/require_form_elem.png)
    
3.  Click **Save**.
    

## How to make a field required, but only when it is shown

You can use dynamic form rules to make a field required, but only when it is shown:

![Screenshot_2023-04-17_at_12-23-28_TS_-_Case_Audit_App_-_Audits_-_Main_Form.png](https://helpv2.quickbase.com/hc/article_attachments/14934594392724)