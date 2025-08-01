## Hide Formula Components but Show the Result

Formula fields, summary fields, and lookup fields derive their values from the values of other fields. For instance, a formula field, **C**, might be the sum of the values in field **A** and field **B**. These source fields (**A** and **B**) are _**sub-fields**_ of the calculated field **C**. A _**sub-field**_ is any field that contributes its value to a calculated field.

It's not just the value of the calculated field that depends upon its sub-fields. Viewer access to the calculated result field also depends upon sub-field access permission settings. Again, say you've got a formula field **C** that sums values in field **A** and field **B**. The formula result field, **C**, inherits the most restrictive field permissions of all its sub-fields. This means that if a viewer can't see sub-field **B**, they can't see the result, **C**. So, whether or not any information shows in the calculated result field at all, depends upon the permission settings on its sub-fields too.

Often, you do want viewers to see the result, but not the contributing sub-fields. To accomplish this, remove sub-field permissions from the mix, by overriding them.

To override sub-field permissions:

1.  [Open the formula result field's properties page](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-).
    
2.  Within the **Advanced** section, click **Restrict access by role** to see the access permissions for this field. Make changes to the permissions based on your situation.
    
3.  Turn on the checkbox shown in red in the image below to use the permissions you set, even if they are less restrictive than those of the fields that were used to calculate the value of this field.
    
4.  Click **Save**.
    

![](https://helpv2.quickbase.com/hc/article_attachments/4572841646612/override_subfield_perm.png)

_Overriding sub-field access settings is, to some extent, a weakening of permissions. So when you enable this option, it displays in red._

Note: This feature WON'T override restrictions if:

-    You've restricted access to records and want the calculated field to show a summary or result of values in those records. This feature overrides _field-level_ restrictions only, not _record-level_ restrictions.
    
-    Sub-fields live in another application (and are part of a cross-application relationship).
    

### Related topics:

-   [Changing the properties of a field](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-)
    
-   [Formula foundations](https://helpv2.quickbase.com/hc/en-us/articles/4839910743444)
    
-   [Copy apps with cross-app relationships](https://helpv2.quickbase.com/hc/en-us/articles/4570378662548-Copying-apps-with-cross-app-relationships-)