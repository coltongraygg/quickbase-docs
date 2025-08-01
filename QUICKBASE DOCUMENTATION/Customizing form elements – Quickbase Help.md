## Customizing form elements

Fields from your table and other components are added to your form as form elements. Think of them as building blocks. You can organize elements in groups, columns, sections, and pages.

-   For example, if you want your service techs to enter date, time, and devices installed during technician appointments into client records in a client information table. You would add a form element for the date, time, and device multi-select fields to your form. You could even group these elements on a separate page on your form with "Service appointments" as the heading.

You can also add component elements to your form including:

-   A block of read-only [rich-text](https://helpv2.quickbase.com/hc/en-us/articles/15121774456980) that instructs sales reps on how to complete a form, or
-   A [report](https://helpv2.quickbase.com/hc/en-us/articles/15118187296660) that displays contact records for clients.

By default, form elements fill the width of the column they’re added to. You can specify the width of some elements.

## Adding form elements

To add a form element:

1.  Select **Click to add here** in any column. The quick add form element menu will appear.
2.   Choose an element from the list of fields, components, and widgets. Or, use the search to find an element.

To add multiple elements, select the checkbox next to each element you want to add.

-   The quick add menu remembers the order of the elements you choose and stack them vertically. The first element you checked is at the top and the last at the bottom.

![FormsAddElementsToFormJan92024.gif](https://helpv2.quickbase.com/hc/article_attachments/22697205970196)Elements that already exist on the form have a jump icon ![Screen_Shot_2023-05-16_at_3.39.12_PM.png](https://helpv2.quickbase.com/hc/article_attachments/15709296024340). Click the icon to go to the existing element on the form builder canvas 

To create a new field for your form:

1.  Click **Create field** in the quick add form element menu.
2.  Add a field label and choose a type for the new field.
3.  Start typing in the new row created to create more fields without leaving the pop-up window.

![Screen_Shot_2023-04-17_at_3.32.29_PM.png](https://helpv2.quickbase.com/hc/article_attachments/14942636549652)

## Customizing form elements

Click anywhere in a form element to open the form element settings.

![Screen_Shot_2023-04-17_at_3.37.04_PM.png](https://helpv2.quickbase.com/hc/article_attachments/14942682950804)

### Form element labels

Use the label options to decide how to label elements for your end users.

-   **Default** uses the field label as the default form element label
-   **Custom** allows you to create a custom label
-   **Hide** hides the label from your end users

You will be able to see label changes immediately on your form canvas.

### Display form elements when form is used for editing, viewing, and adding records

Decide if an element should be visible all for all form activity or for only some form activities.

-   Choose **Edit** to display the element when end users edit the form
-   Choose **View** to display the element when end users view the form
-   Choose **Add** to display the element when end users add new records

You can choose any or all of the three options. Switch to [preview mode](https://helpv2.quickbase.com/hc/en-us/articles/14942005711508) in the page bar to see how the form looks in when users view, edit, and add records. 

### Form element layout

Adjust element width in the **Layout** section of the form element settings.

**Auto width** is the default setting.

-   Auto width will make the element wide enough to fill the column
-   If you resize the column, the form elements in the column will also resize to fill the new width

Some elements allow you to set a **Custom** width.

-   Set width in pixels
-   Set width in percentage of the column's width
-   Your custom form element width may shrink to fit in it's column if the column width is too narrow

### Form element help text

You can add help text to field elements. Help text displays below an element. 

![2023-06-07_Image_of_a_field_with_help_text.png](https://helpv2.quickbase.com/hc/article_attachments/16165872656276)

Use help text to communicate unique information about the data you expect to be added to a field.

-   For example, you could add help text to a field that captures sensitive data that lets users know that their information will be safe

Keep in mind that Quickbase validates values entered into fields automatically. Familiarize yourself with value validation before you write help text. Learn more about value validation and accepted values in our [Using forms with field value validation](https://helpv2.quickbase.com/hc/en-us/articles/14966311161876) article.

### Form element behavior

Control element behavior in the **Behavior** section of form element settings. 

-   Make an element read-only when users are editing or adding records
-   Make an element required when users are editing and adding records 

### Form element rules

View, add, and edit form rules for an element in this panel. 

Expand a rule to see a description and the actions for the rule. Use the **Create a form rule** button to add a new rule for this element.

## Moving and reordering form elements

Drag and drop form elements to reorder them. Or, use the **Move to section** button in form element settings. 

Group elements by dragging and dropping one element on top of another. [Grouped elements](https://helpv2.quickbase.com/hc/en-us/articles/14940102079380) display horizontally on the same row and can be moved together by dragging and dropping the group.

![D1142883-02A5-4082-858F-2C7E94DE5957__1_.gif](https://helpv2.quickbase.com/hc/article_attachments/14942881931156)

## Deleting form elements

Delete form elements by using **Delete element** in the form element settings menu or by clicking the top right corner of the form element to reveal the remove option.

-   Deleting form elements from your form will not delete the field from your table
-   Re-add deleted elements by using **Click to add here** in any column and selecting the element you want from the form element menu or by clicking **Undo**