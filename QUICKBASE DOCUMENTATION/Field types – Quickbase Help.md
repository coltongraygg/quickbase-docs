When you create a [field](https://helpv2.quickbase.com/hc/en-us/articles/4570396310548-What-Is-a-Field-), you also set what type of field it is. Quickbase offers many types of fields—each designed for a specific purpose. You should use the most specific field type possible when defining your fields. This helps Quickbase set up your app.

Some field types (List-User, Multi-select Text, and File Attachment, for example) may not be changed. The **Change Type** link will not be present if this is the case.

Note: Several field types behave differently in the Quickbase mobile app, or in a web browser on a mobile device, when viewing and editing records. [Read more](https://helpv2.quickbase.com/hc/en-us/articles/4570399432980-Field-type-behavior-in-the-Quickbase-mobile-app-).

-   [Basic field information](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-Field-types#Basic)
    -   [Table-to-table relationship fields](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-Field-types#Table-to)
    -   [Detailed field information](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-Field-types#Detailed)
-   [Handling complex ID numbers and ZIP codes](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-Field-types#Handling)
-   [Do not use Quickbase to collect and store credit card numbers](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-Field-types#credit_cards)
-   [Field properties](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-Field-types#Field)
-   [Comments](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-Field-types#Comments)

Quickbase provides the following field types. The table below describes each, and indicates if the field’s [**Searchable** property is set by default](https://helpv2.quickbase.com/hc/en-us/articles/4570284211860-Excluding-fields-from-searches-#searchable).

## Basic field information

| 
Field Type

 | 

Description

 | 

Searchable by default

 |
| --- | --- | --- |
| 

[Text](https://helpv2.quickbase.com/hc/en-us/articles/4570366390804-Text-field-properties-)

 | 

Use this field to hold plain text or data that doesn't fit well into any other type of field. Text fields are the most versatile field type, in which you can enter any kind of character. You can also [limit the length of entries](https://helpv2.quickbase.com/hc/en-us/articles/4570385516692-Set-Maximum-Length-for-Entries-in-a-Text-Field-).

 | Yes |
| 

[Text - multi-line](https://helpv2.quickbase.com/hc/en-us/articles/4570410083348-Text-multi-line-field-properties-)

 | 

Text - multi-line is a text field that automatically displays as a box with 6 lines when it appears on the form. Like a regular text field, this type of field can accept any characters. You might use this when users are going to be entering longer amounts of text, like comments or notes. To use a Text - multi-line type field to store conversations or comments from multiple users, [turn on the field's log edits (append option)](https://helpv2.quickbase.com/hc/en-us/articles/4570433511316-Logging-text-field-edits-).

 | No |
| 

[Text - multiple-choice](https://helpv2.quickbase.com/hc/en-us/articles/4570328005396-Text-multiple-choice-field-properties-)

 | 

Use this field type when you want users to select **only one** item from a list of choices. The field appears on forms as a drop down.

 | Yes |
| 

[Rich text](https://helpv2.quickbase.com/hc/en-us/articles/4570392946068-Rich-text-field-properties-)

 | 

Field includes an editor for content formatting. Use this field type when you want users to be able to format content, add links, insert images, create content tables, and use other rich text features. Advanced builders can view and edit the source and work with HTML if needed.

 | Yes |
| 

[Multi-select - text](https://helpv2.quickbase.com/hc/en-us/articles/4570283477140-Multi-select-text-field-properties)

 | 

Use this field type to allow users to select **multiple** items from a list of choices. The field appears on forms as a drop down with check boxes next to each choice.

 | Yes |
| 

[Numeric](https://helpv2.quickbase.com/hc/en-us/articles/4570417467028-Numeric-field-properties-)

 | 

A field that contains numbers only. Other types of characters are ignored. [Read about configuring numeric fields](https://helpv2.quickbase.com/hc/en-us/articles/4570367709716-Configure-Numeric-Fields-).

 | No |
| 

[Numeric - currency](https://helpv2.quickbase.com/hc/en-us/articles/4570375178644-Numeric-currency-field-properties-)

 | 

Numeric field that automatically is set to display as US currency. With any numeric field, you can define a currency symbol and whether it displays before or after the amount. For example, $25.00 or ¥100 or 86€. [Read about configuring numeric fields](https://helpv2.quickbase.com/hc/en-us/articles/4570367709716-Configure-Numeric-Fields-).

 | No |
| 

[Numeric - percent](https://helpv2.quickbase.com/hc/en-us/articles/4570306901780-Numeric-percent-field-properties-)

 | 

Numeric field that automatically is set to display as a percentage. [Read about configuring numeric fields](https://helpv2.quickbase.com/hc/en-us/articles/4570367709716-Configure-Numeric-Fields-).

 | No |
| 

[Numeric - rating](https://helpv2.quickbase.com/hc/en-us/articles/4570274914196-Numeric-rating-field-properties-) (0-5)

 | 

Numeric field that automatically is set to display values from 0 to 5 as a star rating scale on records and reports. Use this type of field to rate items on a scale of 0 to 5. The rating displays as stars from zero (no stars selected) to 5 (all stars selected). [Read about configuring numeric fields](https://helpv2.quickbase.com/hc/en-us/articles/4570367709716-Configure-Numeric-Fields-).

 | No |
| 

[Date](https://helpv2.quickbase.com/hc/en-us/articles/4570302460820-Date-field-properties-)

 | 

This is a field that contains a date only. When a date field appears on a form, it features a calendar button that lets users select a date. You can configure the date to display in several ways. [Read about configuring date fields](https://helpv2.quickbase.com/hc/en-us/articles/4570137636884-Configure-Date-Fields-).

 | Yes |
| 

[Date / time](https://helpv2.quickbase.com/hc/en-us/articles/4570136718612-Date-time-field-properties-)

 | 

This field is an extended date field that can also contain the time in hours and minutes. On forms, you can use the calendar picker to choose the date, then enter the time manually. Use this type of field in combination with [dynamic form rules](https://helpv2.quickbase.com/hc/en-us/articles/4570277337876-Create-Dynamic-Form-Rules-) to [time stamp](https://helpv2.quickbase.com/hc/en-us/articles/4570321013524-Create-a-Timestamp-with-Dynamic-Form-Rules-) data-driven events like status changes.

 | No |
| 

[Time of day](https://helpv2.quickbase.com/hc/en-us/articles/4570379080212-Time-of-day-field-properties-)

 | 

A field that can store a time of day in hours and minutes. Can be configured to include seconds or display in 24-hour format.

 | No |
| 

[Duration](https://helpv2.quickbase.com/hc/en-us/articles/4570434041876-Duration-field-properties-)

 | 

Use this type of field to contain a period of time, measuring time in different formats. [Read how to configure duration fields.](https://helpv2.quickbase.com/hc/en-us/articles/4570366339220-Configure-Duration-Fields-)

 | No |
| 

[Checkbox](https://helpv2.quickbase.com/hc/en-us/articles/4570319459348-Checkbox-field-properties-)

 | 

Adds a single-choice check box to the form. Users can turn on a check box by selecting (checking) it or turn it off by leaving it blank or deselecting it.

 | Yes |
| 

[Address](https://helpv2.quickbase.com/hc/en-us/articles/4570330891156-Address-field-properties-)

 | 

This single field type automatically adds field entries for:

-   Address search
    
-   Street address (Street 1) - also accepts longitude coordinates
    
-   Street address (Street 2) - also accepts latitude coordinates
    
-   City
    
-   State/region
    
-   Postal code
    

This field creates active address links connected to maps, shows maps on records and pins in maps reports, and performs auto-lookup validation of addresses.

 | Yes |
| 

[Phone number](https://helpv2.quickbase.com/hc/en-us/articles/4570340490900-Phone-number-field-properties-)

 | 

Formats numeric entries in phone number format. Can include extensions. Non-numeric characters are ignored. If your phone numbers or extensions require non-numeric characters, use a text field instead.

**Note on importing phone number data:** Phone numbers to be imported may be formatted in many ways. They may use periods, dashes, spaces, or no spaces as separators. Extensions can be prefixed by _ext_, _ext._, or _x_, but not _X_. The import will apply the standard phone number format shown above.

 | No |
| 

[Email address](https://helpv2.quickbase.com/hc/en-us/articles/4570337565076-Email-address-field-properties-)

 | 

Appears as a **mailto** link on records and in reports. Including email fields in your table also adds to your choice of email recipients in notifications. You can configure how the email link appears. There is also an **email all** option to display an icon in the totals row or reports, where you can start an email to everyone included.

 | Yes |
| 

[User](https://helpv2.quickbase.com/hc/en-us/articles/4570394624660-User-field-properties-)

 | 

A field to choose and store one Quickbase user. On forms, the field appears as a drop-down list where you can select an existing user.

For example, if you're using an app to manage projects, you'd probably want to a way to assign tasks to the actual people who use your app. Use this type of field to:

-   Create reports that show a user only records that pertain to them. For example, when a user opens your app a list of their open issues could display.
    
-   Define record change notification recipients or define the conditions under which a notification is sent. To learn how, see [Creating a Record Change Notification](https://helpv2.quickbase.com/hc/en-us/articles/4570387295892-Create-a-Record-Change-Notification-).
    
-   Control access to an app. To learn how, see [Creating a Custom Rule](https://helpv2.quickbase.com/hc/en-us/articles/4570415966228-Create-a-Custom-Access-Rule-).
    

[Read more about configuring user fields](https://helpv2.quickbase.com/hc/en-us/articles/4570360058132-Manage-Users-in-an-Application-).

 | Yes |
| 

[List - user](https://helpv2.quickbase.com/hc/en-us/articles/4570359290900-List-user-field-properties)

 | 

A field to choose and store one or more Quickbase users. You can choose up to 20 users at once. On forms, the field appears as a drop-down list where you can select existing users.

You can use this field in apps that allow a single task to be assigned to more than one user. For example, in an app used to manage document review and approval, you might want to assign a single document to several different reviewers. [Read more about List - user fields](https://helpv2.quickbase.com/hc/en-us/articles/4570332253972-About-List-User-fields-).

 | Yes |
| 

[File Attachment](https://helpv2.quickbase.com/hc/en-us/articles/4570338184340-File-attachment-field-properties-)

 | 

Attach a file to records. You can [save multiple versions](https://helpv2.quickbase.com/hc/en-us/articles/4570363435668-About-Document-Management-) of the same document.

Maximum size of file attachments is 100 MB.

 | No |
| 

[URL](https://helpv2.quickbase.com/hc/en-us/articles/4570366324244-URL-field-properties-)

 | 

Adds http:// and displays as a link on records and in reports. Users can enter a URL address as they complete a record, or the app manager can design a URL field that Quickbase composes automatically, based on information from other fields in a record. [Read more about URL and URL Formula type fields](https://helpv2.quickbase.com/hc/en-us/articles/4570366896532-Configure-URL-Fields-).

 | No |
| 

[Report link](https://helpv2.quickbase.com/hc/en-us/articles/4570340160788-Report-link-field-properties-)

 | 

Use this field when you want to match records between tables. You configure a report link field to include matching criteria and show either a link to a report or an embedded report on records. Read more about [creating links between tables.](https://helpv2.quickbase.com/hc/en-us/articles/4570342656148-Create-Links-between-Tables-)

When you create table-to-table relationships, the process automatically adds report link fields to show child records on parent records. But you can also use report link fields outside of table-to-table relationships to match information.

 | No |
| 

[vCard](https://helpv2.quickbase.com/hc/en-us/articles/4570138487700-vCard-field-properties-)

 | 

Use the **vCard** standard for exchanging calendar information. When you add this field type to a table, you match the vCard field properties to existing fields in your table for name, email, job title, company, business phone, cell phone, fax, street, city, state, zip, note. [Setting up a vCard field](https://helpv2.quickbase.com/hc/en-us/articles/4570136812820-Set-Up-a-vCard-Field-).

  
**Note**: **vCard** fields have reached [End of Support](https://helpv2.quickbase.com/hc/en-us/articles/4570319163156).

 |   |
| 

[iCalendar](https://helpv2.quickbase.com/hc/en-us/articles/4570345410708-iCalendar-field-properties)

 | 

Use the **iCalendar** standard for exchanging calendar information. When you add this field type to a table, you match the iCalendar field properties to existing fields in your table for subject, description, location, starting time, and ending time. [Setting up iCalendar fields.](https://helpv2.quickbase.com/hc/en-us/articles/4570324787988-Set-Up-an-iCalendar-Field-)

**Note**: **iCalendar** fields have reached [End of Support](https://helpv2.quickbase.com/hc/en-us/articles/4570319163156).

 | No |
| 

[Predecessor](https://helpv2.quickbase.com/hc/en-us/articles/4570377296148-Predecessor-field-properties-)

 | 

Use this field to set up and add dependencies in a project management app. This field stores the list of tasks that must finish before a particular task can begin.

To learn more, see [About Predecessors](https://helpv2.quickbase.com/hc/en-us/articles/4570386630932-About-Predecessors-).

**Note:** You can only have one predecessor field per table.

 | No |
| 

Work date

 | 

Used with predecessor fields. A special type of date field created to accommodate durations that include partial days.

Note: This field type may not appear in your list of available field types until a predecessor field has been created.

Work date fields can handle fractional day computations. (Regular date fields do not.) This is an important feature when you're working with predecessors. For example, if a predecessor task will take 2.5 days to complete, a work date field calculates to that the task ends in the middle of the day. If that task has a successor task, the successor would start on that same day. Regular date fields measure time in whole days. So, if you were to use a regular date field with predecessors, successor tasks would often start a day late.

Read more about using work date fields in the topic [Creating dependencies by adding predecessor fields](https://helpv2.quickbase.com/hc/en-us/articles/4570317165076-Add-Dependencies-to-an-Existing-Project-Management-Application-).

 | No |
| 

Formula

 | 

Computes a value based on a formula that you enter. For information about how to use formulas, see [Using Formulas in Quickbase](https://helpv2.quickbase.com/hc/en-us/articles/4570376002580-Using-Formulas-in-Quickbase-). For detailed information about functions, refer to the [Quickbase Formula Functions](http://www.quickbase.com/db/6ewwzuuj?a=q&qid=6) app.

Formulas can be created for each of the following field types:

| Type | Searchable by default |
| --- | --- |
| [Formula - text](https://helpv2.quickbase.com/hc/en-us/articles/4570378001428-Formula-text-field-properties-) | Yes |
| [Formula - rich text](https://helpv2.quickbase.com/hc/en-us/articles/4570381153044-Formula-rich-text-field-properties-) | Yes |
| [Formula - numeric](https://helpv2.quickbase.com/hc/en-us/articles/4570293327380-Formula-numeric-field-properties-) | No |
| [Formula - date](https://helpv2.quickbase.com/hc/en-us/articles/4570315579412-Formula-date-field-properties-) | Yes |
| [Formula - time of day](https://helpv2.quickbase.com/hc/en-us/articles/4570280129940-Formula-time-of-day-field-properties-) | No |
| [Formula - duration](https://helpv2.quickbase.com/hc/en-us/articles/4570357279252-Formula-duration-field-properties-) | No |
| [Formula - checkbox](https://helpv2.quickbase.com/hc/en-us/articles/4570417038868-Formula-checkbox-field-properties-) | Yes |
| [Formula - phone number](https://helpv2.quickbase.com/hc/en-us/articles/4570344864916-Formula-phone-number-field-properties-) | No |
| [Formula - email address](https://helpv2.quickbase.com/hc/en-us/articles/4570365655188-Formula-email-address-field-properties-) | Yes |
| [Formula - URL](https://helpv2.quickbase.com/hc/en-us/articles/4570366252820-Formula-URL-field-properties-) | No |
| [Formula - User](https://helpv2.quickbase.com/hc/en-us/articles/4570321938324-Formula-user-field-properties) | Yes |
| [Formula - multi-select text](https://helpv2.quickbase.com/hc/en-us/articles/4570367207316-Formula-multi-select-text-field-properties-) | Yes |
| [Formula - list user](https://helpv2.quickbase.com/hc/en-us/articles/4570316574484-Formula-list-user-) | Yes |
| Formula - work date | No |
| [Formula - date/ time](https://helpv2.quickbase.com/hc/en-us/articles/4570329184916-Formula-date-time-field-properties-) | No |

 | Varies – see **Description** column |

### Table-to-table relationship fields

Here are field and attributes involved with table-to-table relationships:

<table><tbody><tr><td><p>Reference</p></td><td><p>When you create a relationship between tables, you'll designate one field as a reference field. "Reference" is not a field type, but an attribute of a field. When you <a href="https://helpv2.quickbase.com/hc/en-us/articles/4570269732756-Creating-table-to-table-relationships-">create a relationship</a> between two tables, you choose a field with which to link them. That field is the reference field. Any type of field can serve as a reference field.</p><p>Relationships include other special field types as well. To learn more, read <a href="https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-">about Relationships</a>.</p></td></tr><tr><td><p>Lookup</p></td><td><p>Lookup fields are part of a relationship. These fields bring in additional information into the details table about records in the parent table.</p><p><a href="https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-#fieldtypes">Read more about relationships</a>.<br><a href="https://helpv2.quickbase.com/hc/en-us/articles/4570275339156-Creating-lookup-fields-">Learn how to create a lookup field</a>.</p></td></tr><tr><td><p>Summary</p></td><td><p>Summary fields are also part of a relationship. Create a Summary field in a parent table to summarize information about the related records in the details table. For example, a summary field could total the total revenue for each of your salespeople.</p><p><a href="https://helpv2.quickbase.com/hc/en-us/articles/4570287263636-About-table-to-table-relationships-#fieldtypes">Read more about relationships</a>.<br><a href="https://helpv2.quickbase.com/hc/en-us/articles/4570321780372-Creating-a-summary-field-">Learn how to create a summary field</a>.</p></td></tr></tbody></table>

Note: Connected fields are fields within a [connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-) that are connected to an app, service, or folder containing CSV files. Connected fields display a ![](https://helpv2.quickbase.com/hc/article_attachments/20329944150292) icon on the Field Settings page.

Since the data in connected fields comes from an external service, you can’t edit the data. You can [rename connected fields](https://helpv2.quickbase.com/hc/en-us/articles/4570271371796-Changing-the-names-of-fields-) and [change the field types](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-). See [About connected fields](https://helpv2.quickbase.com/hc/en-us/articles/4570265917332-About-connected-fields-).

Connected tables are not available to accounts on the Quickbase Essential plan.

### Detailed field information

The table below contains the data space consumed and the base type for each field type. You can find even more details for each field in a table by running a Quickbase API call, API\_GetSchema, on that table. Read more [about using API\_GetSchema](https://www.quickbase.com/api-guide/index.html#getschema.html) in the Quickbase HTTP  API Guide. Quickbase recommends that you use [app tokens](https://helpv2.quickbase.com/hc/en-us/articles/4570313549972-Application-Tokens-) when working with API calls.

**Note**: Derived fields do not consume data space.

| 
Field Type

 | 

Data Space Consumed

 | 

Base Type

 |
| --- | --- | --- |
| 

Text

 | 

8 bytes + 1 byte per character

 | 

text

 |
| 

Text - multi-line

 | 

8 bytes + 1 byte per character

 | 

text

 |
| 

Text - multiple choice

 | 

8 bytes + 1 byte per character

 | 

text

 |
| Multi-select text | 8 bytes + 1 byte per character | text |
| 

Numeric

 | 

8 bytes

 | 

float

 |
| 

Numeric - currency

 | 

8 bytes

 | 

float

 |
| 

Numeric - percent

 | 

8 bytes

 | 

float

 |
| 

Numeric - rating (0-5)

 | 

8 bytes

 | 

float

 |
| 

Date

 | 

8 bytes

 | 

int64

 |
| 

Date / time

 | 

8 bytes

 | 

int64

 |
| 

Time of day

 | 

8 bytes

 | 

int64

 |
| 

Duration

 | 

8 bytes

 | 

int64

 |
| 

Checkbox

 | 

4 bytes

 | 

bool

 |
| 

Address

 | 

24 bytes (4 bytes per subfield)

 | 

text

 |
| 

Phone number

 | 

4 bytes + 1 byte per character

 | 

text

 |
| 

Email address

 | 

4 bytes + 1 byte per character

 | 

text

 |
| 

User

 | 

4 bytes

 | 

text

 |
| 

List-user

 | 

8 bytes

 | 

text

 |
| 

File attachment

 | 

4 bytes

 | 

text

 |
| 

URL

 | 

4 bytes + 1 byte per character

 | 

text

 |
| 

Report link

 | 

0 bytes

 | 

text

 |
| 

vCard

 | 

0 bytes

 | 

text

 |
| 

iCalendar

 | 

0 bytes

 | 

text

 |
| 

Predecessor

 | 

4 bytes + 1 byte per character

 | 

text

 |
| 

Work date

 | 

8 bytes

 | 

int64

 |
| 

Formula - text

Formula - numeric

Formula - date

Formula - time of day

Formula - duration

Formula - checkbox

Formula - phone number

Formula - email address

Formula - URL

Formula - list user

Formula - work date

Formula - date/ time

 | 

4 bytes + their base field type

 | 

Same as the field type associated with the formula.

For example, the base type of Formula - Text is text.

 |
| 

Reference

(Used in apps with multiple tables)

 | 

Space equal to the field being referenced

 | 

Same as the field specified for the reference.

 |
| 

Lookup

(Used in apps with multiple tables)

 | 

4 bytes + their base field type

 | 

Same as the field specified for the lookup.

 |
| 

Summary

(Used in apps with multiple tables)

 | 

4 bytes + their base field type

 | 

float

 |

## Handling complex ID numbers and ZIP codes

You may need consider using a **Text** field for complex numbers and ZIP codes. ID numbers and ZIP codes can start with a zero. If the field is a **Numeric** field, Quickbase automatically removes the preceding zero. This holds true for any long numeric chain that identifies things like account numbers or inventory codes. If a chain of numbers is very long, Quickbase attempts to round the number off. Use a text field to avoid this problem. This is also true if you store postal codes somewhere other than an Address field.

## Do not use Quickbase to collect and store credit card numbers

No one can access your Quickbase data without your authorization, however, Quickbase is not designed to process credit card numbers. **Never store credit card numbers in Quickbase.** If you are a merchant handling credit cards, you must follow PCI compliance guidelines, which specify security practices for card number handling. If you enter and store credit card numbers in Quickbase, you are violating PCI compliance guidelines and could be fined. Use Quickbase for data entry, storage and collaboration, not credit card processing. [More about PCI Compliance from Wikipedia](http://en.wikipedia.org/wiki/PCI_DSS).

## Field properties

Every field type has properties that are unique to it, which you can change at any time. For example, you can specify the format in which you want a date field to display or you can change a text field from a type-in field to a multiple-choice field. To learn how, see the topic on [Changing the Properties of a Field](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-).

To see help on the properties for a single field type, click the linked name in the first table in this topic.

Comments

Use the Comments tab to enter free-form notes about how you are using the field, or anything else you want to document. There is a limit of 500 characters for your comments.

On the Fields page, an icon appears next to fields where you have added comments. If you want to have the icon appear in its own column on the Fields page, choose Advanced Options and select to show the Comments column.

### Related topics:

-   [What is a field?](https://helpv2.quickbase.com/hc/en-us/articles/4570396310548-What-Is-a-Field-)
    
-   [Add a field](https://helpv2.quickbase.com/hc/en-us/articles/4570374838292-Adding-new-fields-)
    
-   [Delete a field](https://helpv2.quickbase.com/hc/en-us/articles/4570367639316-Deleting-a-field-)
    
-   [Duplicate a field](https://helpv2.quickbase.com/hc/en-us/articles/4570321855636-Copy-a-Field-)
    
-   [Changing a field's properties](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-)
    
-   [Change the name of a field](https://helpv2.quickbase.com/hc/en-us/articles/4570271371796-Changing-the-names-of-fields-)
    
-   [Change the field type of an existing field](https://helpv2.quickbase.com/hc/en-us/articles/4570362798868-Changing-the-field-type-of-existing-fields-)
    
-   [Field type behavior in the Quickbase mobile app](https://helpv2.quickbase.com/hc/en-us/articles/4570399432980-Field-type-behavior-in-the-Quickbase-mobile-app-)
    
-   [About localizing currency symbols](https://helpv2.quickbase.com/hc/en-us/articles/4570305824660-About-Localizing-Currency-Symbols-)
    
-   [About localizing dates](https://helpv2.quickbase.com/hc/en-us/articles/4570317130516-About-Localizing-Dates-)
    
-   [About localizing number formats and separators](https://helpv2.quickbase.com/hc/en-us/articles/4570266437780-About-Localizing-Number-Formats-and-Separators-)