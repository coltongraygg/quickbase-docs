## Configure Numeric Fields

When you add a numeric type field to Quickbase, you probably have a very specific job in mind for that field. For example, maybe it holds a price or contains a rating. To help the field be most effective, Quickbase lets you control its display and behavior.

Note: Numeric fields take only numbers. Try to enter a letter or other character, and Quickbase won't stand for it. You'll get a message telling you where you went wrong and the numeric field will be blank - waiting for you to do right and type a number in it.

## Types of numeric fields

When you add a new field, Quickbase offers a few different types of numeric fields as options:

-   **Simple Number.** A plain-vanilla numeric field holds basic numbers or decimals, and offers different options for totals and calculations that you'll read about in a minute.
    
-   **Star Rating.** Using Quickbase to assess product ideas or review movies? If so, check out the Numeric - Rating field type, which lets users give an item one to five stars. The values for this field display as stars (unless you tell Quickbase otherwise).
    
-   **Percent.** If you need to measure portions (for example, what amount of a salesperson's monthly goal did they actually meet?) you'll want to use a Numeric-Percent field.
    
    **FAQ - I'm using a percentage field in my formula, and it's not working. Why not?**
    
    While values in this type of field display as percentages, the _**real**_ value is the exact mathematical representation of percent, which is always a portion of the whole number, one. For example, 20% is really **.2** and 3% is really the number **.03**. This is an important concept to understand if you plan to use a Numeric - Percent field in a Quickbase formula. Say you created a formula to color-code records where the percent complete is less than 100% you'd need to use the number **1** instead of the number 100. This formula should look like this: If(\[percent complete\]< 1, "pink", ""). (Read more about [formulas](https://helpv2.quickbase.com/hc/en-us/articles/4570376002580-Using-Formulas-in-Quickbase-) and [row colorization](https://helpv2.quickbase.com/hc/en-us/articles/4570391002260-Color-coding-in-reports-).)
    
-   **Currency.** Inputting prices? Any time you want to record a monetary amount, you'll use a Numeric - Currency field. ([Read how to format currency symbols](https://helpv2.quickbase.com/hc/en-us/articles/4570367709716-Configure-Numeric-Fields#curr).)
    

## Changing a numeric field type to another numeric field type

Each type of Numeric field has its own particular talent, but they're not as different as they first appear. **In the list of field types Quickbase offers, these are listed as separate field types. In reality, these types are all one single type - Numeric.** You can change the properties of any Numeric field to show values in one of the formats listed above. In other words, Currency is not its own field type, but rather an attribute of a Numeric field that tells the field how to display and behave. What does this mean? Well, it means that you could change ratings into actual numeric values in a snap. You do it all on the field's Properties page.

To display a numeric field in a different kind of numeric format:

1.  Open the field's Properties page.
    
    Access the field's Properties page in one of the following ways:If you're in a form, right-click the field or field label and select Edit the field properties for this fieldIf you're in a report, click on a column heading menu (), then select Field properties.From the table containing the field you want to change, click Settings on the Page bar. Click Fields, then click the field name to access its Properties page. From the fields list, click the field name to access its Properties page.
2.  Change the attributes of the field. Under Display, go to the **Display as** option and select the numeric format from the dropdown.
    
3.  Click **Save**.
    

## Total or average numbers

Tell Quickbase how to wrap up the numbers when the numeric field appears in a table. The program either totals or averages all the numbers. The result appears at the bottom of the column. Usually, you'll want to total regular numbers and monetary amounts. Most application managers choose to average percentages and ratings. To set this, open the field's properties page (see Step 1 above) and turn on the correct checkbox in **Totals and averages** under Numeric field options.

## Offer options in a multiple-choice format

You may wish to offer specific choices to your users in a dropdown, instead of letting them enter anything they want. This might be a nice feature of a rating field, for instance. To do so, locate the Input type option on the field's Properties screen and click the **From list** radio button. In the box that displays, type in the options, one to a line.

## Decimals

If you want, you can add decimals into the mix. Just go to the field's Properties screen and enter the number of digits you want to display after the decimal point in the **Decimal places** option. Leave it blank for a floating point. If a user enters more digits after the decimal point than you've entered here, Quickbase rounds the number and extends it only to the number of decimal places you specified. The fraction .5 rounds the number away from 0.  For example, 3.5 rounds to 4, and -3.5 rounds to -4.  If you would rather .5 always round up, meaning that -3.5 would round to -3, use the Round formula instead of the decimal places option for rounding.

## Handling complex ID numbers and zip codes

Zip codes contain numbers. So, you might think that you should use a Numeric field to contain these values, but you're better off using a **Text** field. Why? Often zip codes start with a zero. If the field is a Numeric field, Quickbase automatically removes any zeroes preceding the number. This holds true for any long numeric chain that identifies things like account numbers or inventory codes. If a chain of numbers is very long, Quickbase attempts to round the number off. Use a Text field to avoid this problem.

## Formatting currency symbols

If your numeric field is not already in currency format, go to Display as on the [field properties page](https://helpv2.quickbase.com/hc/en-us/articles/4570253123348-Change-the-Properties-of-a-Field-) and select **Currency** from the dropdown. If you want, you can enter a different currency symbol of up to 10 UTF-8 characters, and set its placement relative to the number.

The default [currency symbol](https://helpv2.quickbase.com/hc/en-us/articles/4570305824660-About-Localizing-Currency-Symbols-) is the dollar sign ($). To change it, type the currency symbol into the **Symbol** field, either as an HTML character entity or as a Unicode character code. [View a list of character entities on the W3C web site](http://www.w3schools.com/tags/ref_entities.asp).

To specify the placement of the currency symbol:

Select one of the following options from the Position dropdown:

-   **Between "-" and the number** displays the currency symbol between the minus sign and the numerical value. For example: -$34.95
    
-   **Before number** displays the currency symbol on the left side of the value. For example: $-34.95
    
-   **After number** displays the currency symbol on the right side of the value. For example: 34.95$
    

### Related topics:

-   [About localizing number formats and separators](https://helpv2.quickbase.com/hc/en-us/articles/4570266437780-About-Localizing-Number-Formats-and-Separators-)
    
-   [About localizing currency symbols](https://helpv2.quickbase.com/hc/en-us/articles/4570305824660-About-Localizing-Currency-Symbols-)