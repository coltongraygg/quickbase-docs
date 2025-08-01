## Using forms with field value validation

Quickbase forms are designed to increase productivity by making it easier for users to enter data with field value validation. Field value validation alerts users immediately after they have entered an unaccepted value in a field. 

Field validation occurs automatically when the app builder has added it to the field being edited, so it will be a good idea to review the [field value validation table](https://helpv2.quickbase.com/hc/en-us/articles/14966311161876-Using-forms-with-field-value-validation#h_01H28Z5W51PQGJPG0Q7K6KR5QE) before adding [help text](https://helpv2.quickbase.com/hc/en-us/articles/14942938504724) to a form element to avoid repeating information. Field value validation messages are displayed beneath the field and when a validation message is triggered the corresponding field is highlighted with a red border.

## Field value validation

Field value validation is unique to the field type. Take a look at the table to learn more about accepted values for each field and view the validation that will occur.

<table><tbody><tr><td>Field</td><td>Validation</td></tr><tr><td>Email</td><td>Display message: Use this format&nbsp;<a href="mailto:example@example.com" target="_blank" rel="noopener noreferrer" data-stringify-link="mailto:example@example.com" data-sk="tooltip_parent" aria-haspopup="menu" aria-expanded="false" aria-describedby="sk-tooltip-7032">example@example.com</a></td></tr><tr><td>Phone number</td><td>Display message: Enter a valid phone number</td></tr></tbody></table>

## Add value validation to your form

Select the element to open the element settings panel. In the **Behavior** section, select the **Validate for correct format** option to turn on field value validation.

 ![Screenshot](https://helpv2.quickbase.com/hc/article_attachments/16461055465620)