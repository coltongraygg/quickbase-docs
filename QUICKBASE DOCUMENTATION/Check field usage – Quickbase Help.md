## Check field usage

Understanding how fields are used and referenced can help you maintain and improve your apps. App admins can access field usage information from the fields settings page in table settings. This article covers how to access field usage information and the types of information available. 

In this article

-   [Check field usage](https://helpv2.quickbase.com/hc/en-us/articles/4570268070036-Check-field-usage#h_01JERVMPBSZGMV0ZSCTEGW3NEZ)
-   [Types of field usage information](https://helpv2.quickbase.com/hc/en-us/articles/4570268070036-Check-field-usage#h_01HHHJ16HJ062V02NKEJYM6Y07)
    -   [Forms and reports](https://helpv2.quickbase.com/hc/en-us/articles/4570268070036-Check-field-usage#h_01HHHJ16HJ0ZQS1Z8R6WYEJKCG)
    -   [Derived fields usage](https://helpv2.quickbase.com/hc/en-us/articles/4570268070036-Check-field-usage#h_01HHHJ16HJHDQFVYM75W0X6M97)
    -   [Pipelines](https://helpv2.quickbase.com/hc/en-us/articles/4570268070036-Check-field-usage#h_01JERVWWM63MH6F9HDYKMN0DBY)
    -   [Other](https://helpv2.quickbase.com/hc/en-us/articles/4570268070036-Check-field-usage#h_01HHHJ16HJWH381EK3F1TTAGTR)
    -   [Address fields](https://helpv2.quickbase.com/hc/en-us/articles/4570268070036-Check-field-usage#h_01HHHJ16HJB4QZFR4ZV2DNHHXK)
-   [Dependency diagrams](https://helpv2.quickbase.com/hc/en-us/articles/4570268070036-Check-field-usage#h_01HHHJ16HJ0XMAR62GM3CKEFDY)
    -   [View a dependency diagram](https://helpv2.quickbase.com/hc/en-us/articles/4570268070036-Check-field-usage#h_01JERW16JPJSYCC3HC96TWSGCR)
    -   [Interact with the dependency diagram](https://helpv2.quickbase.com/hc/en-us/articles/4570268070036-Check-field-usage#h_01JERW5D41FQPRW6E1NWS63ZT3)
    -   [Information included on the dependency diagram](https://helpv2.quickbase.com/hc/en-us/articles/4570268070036-Check-field-usage#h_01JERW80YCG5KZEWSWCX49V4PE)

## Check field usage

1.  Select the table that contains the field.
    
2.  Select **Settings**, then choose **Fields**.  
    Or hover over the table name in the sidebar and select the three dot more menu. Select **Fields** to get to the fields setting page.
    
3.  Hover over the field name, then select **Where is this field used?** in the dialog box that appears. The Usage page displays a list of the places where the field is used in your app.
    

Alternatively, if you are editing a field's properties, select the **Usage** tab.

## Types of field usage information

The table on the form usage tab displays: 

-   Where the field is used—dashboards, emails, reports, etc.
-   Name of the place it is used—the name of specific dashboard, forms, reports, etc.
-   Owner, if the information is available—for example, emails have an owner that is listed on this page
-   Reason—additional details about how the field is used

The following sections cover places where fields may be used.

### Forms and reports

-   Forms
-   Access permissions
-   A form rule, with information on which form rule
-   Document templates or an advanced dashboard
-   A report link
-   Report formulas
-   Row color-coding for reports
-   Initial filters for reports
-   Default report settings
-   All reports that use the default report settings are italicized with a note that they use the default fields. This way, if you need to delete or change a field, you can easily see if the field is part of the default settings and only change the report settings once.

### Derived fields

-   Lookup fields
-   Summary fields
-   Formula fields
-   A snapshot or shared values field

### Pipelines

When fields are used in pipelines, the following information is included:

-   Pipeline name—a clickable URL that opens the associated pipeline where the field is used
-   Owner
-   Reason—the indexes of the steps within the pipeline where the field is used

Field usage and count don't show for pipelines if:

-   A field is used in steps through Jinja expressions
-   A sub-field is exclusively used in the advanced query field
-   A sub-field is used in the following steps: Import with CSV, Remove Record(s), Copy Records, and Export Records to CSV

### Other

-   Used in an email reminder or notification
-   Used in a webhook
-   Part of a table-to-table relationship
-   Used in a custom data rule
-   The number of records that have a value in this field with a link to a table report of those records
-   Estimated space (memory or data) consumed  
    Due to variations in how Quickbase and data are used, we provide an estimated size for each field to provide a sense of relative field usage. This value may also change as an application is used.
    -   For scalar (data entry) fields, this represents the total size of the field as stored on disk. For derived fields (summary, lookup, formula), this represents memory since these values are not stored.

### Address fields

For address fields, also known as composite fields, field usage info reflects both the primary field and all of its sub-fields. For example, if users enter Street 1, City, State/Region, and Postal Code separately, the record will be counted in the total number of Address field records. Also the memory used by all these sub-fields will be counted in the memory usage total for the Address field. The exception is when the Country field has the default value “United States,” then the Country value is not counted.

In pipelines, there are specific limitations for displaying sub-field usage. Field usage information isn't shown and counts aren't changed in the following cases:

-   When the sub-field is exclusively used in the advanced query field
-   When the sub-field is used in the following steps: Import with CSV, Remove Record(s), Copy Records, and Export Records to CSV

## Dependency diagrams

Dependency diagrams help you better manage and track your apps by tracing the source of your fields. They show the flow of information between fields in your app.

Field types that have a dependency diagram include:

-   Address
-   Lookup
-   Summary
-   Formula
-   Composite fields used in Quickbase Sync
-   Fields referenced in the filter criteria of a Summary field

### View a dependency diagram

1.  Go to the **Fields** setting page in table settings.
2.  Select a field from the list.  
    
    Note
    
    The field must be one of the field types listed above. Otherwise it will not include a dependency diagram.
    
3.  Select the **Dependency Diagram** tab.

### Interact with the dependency diagram

All fields are shown when you open the diagram; there is no need to expand any information. Field information is shown in cards on the diagram canvas.

-   Drag the canvas to recenter the diagram or see additional cards
-   Use browser controls to zoom in and out
-   Drag individual cards to rearrange the diagram

### Information included on the dependency diagram

Each card gives information on the fields, including:

-   Field name—each field name is a link that opens in a new tab
-   Field ID
-   Field type
-   Table where field is located. Fields that are on the same table are outlined in the same color.

Each field is only shown once. If it is referenced multiple times, there are multiple branching lines that show which fields are referencing it. 

Some branching lines may be red and have the label **recursion**. Recursion happens when fields directly or indirectly reference themselves. Recursion can lead to unreliable calculations.