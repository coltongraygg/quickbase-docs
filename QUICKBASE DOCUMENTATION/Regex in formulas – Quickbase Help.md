## Regex in formulas

A regular expression, or regex, is a pattern made up of symbols and characters. Regex is used to match strings with specific patterns, similar to a very powerful text search.

Quickbase offers three regex functions. These functions allow you to parse text so you can extract, replace, or match data in your table.

This article covers the three regex functions available in Quickbase. It does not provide an in-depth explanation of regex.

In this article

-   [Before you start](https://helpv2.quickbase.com/hc/en-us/articles/32800503697044-Regex-in-formulas#Before-you-start)
    -   [Regex functions and formula field types](https://helpv2.quickbase.com/hc/en-us/articles/32800503697044-Regex-in-formulas#Regex-functions-and-formula-field-types) 
    -   [Backslashes in regex functions](https://helpv2.quickbase.com/hc/en-us/articles/32800503697044-Regex-in-formulas#Backslashes-in-regex-functions)
-   [RegexMatch](https://helpv2.quickbase.com/hc/en-us/articles/32800503697044-Regex-in-formulas#RegexMatch)
-   [RegexExtract](https://helpv2.quickbase.com/hc/en-us/articles/32800503697044-Regex-in-formulas#RegexExtract)
-   [RegexReplace](https://helpv2.quickbase.com/hc/en-us/articles/32800503697044-Regex-in-formulas#RegexReplace)
-   [Troubleshoot regex strings](https://helpv2.quickbase.com/hc/en-us/articles/32800503697044-Regex-in-formulas#h_01JEP76G67EZ15B27Q8XCXD5FW)

## Before you start

Quickbase’s implementation of regex is based on the [Google RE2 standard](https://github.com/google/re2/wiki/Syntax "https://github.com/google/re2/wiki/Syntax"). This helps ensure it is performant, stable, and secure. To use the regex functions in Quickbase, you need to be familiar with regex and the [Google RE2 standard](https://github.com/google/re2/wiki/Syntax "https://github.com/google/re2/wiki/Syntax").

Consider using outside resources, like [regex101](https://regex101.com/ "https://regex101.com/"), or the [MDN Regex cheatsheet](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions/Cheatsheet "https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions/Cheatsheet"), to learn more about regex and pattern matching

Note

Regex statements must be written directly in the formula function and can't come from a field or variable.

### Regex functions and formula field types

Regex always operates on text. This means that if the input is a non-text field, like a number or phone number, you need to use the ToText() conversion function. It also means the output is a text value. In most cases, this means you’ll use the formula - text field type for regex formula functions. However, if you want to use a different field type, like formula - numeric, make sure to use conversion functions like ToNumber().

### Backslashes in regex functions

Escape backslashes used in regex formula functions. For example, if your regex contains `\d`, write `\\d`.

## RegexMatch

Use the RegexMatch formula function to match data in your table. This is useful for validating data, like email addresses and phone numbers.

<table><tbody><tr><td><strong>Function</strong></td><td><strong>Formula output</strong></td><td><strong>Example formula</strong></td><td><strong>Input</strong></td><td><strong>Result</strong></td></tr><tr><td rowspan="2">RegexMatch()</td><td rowspan="2">Boolean value</td><td rowspan="2">RegexMatch([Email Address], "^[\\w\\.+-]+@[\\w\\.-]+\\.\\w+$")</td><td>“user@example.com”&nbsp;</td><td>TRUE&nbsp;</td></tr><tr><td>invalid_email&nbsp;</td><td>FALSE&nbsp;</td></tr></tbody></table>

Use the RegexExtract formula function to extract a certain part of a text string that matches the regular expression. If the formula finds no matches, it returns a blank value. This is useful to do things like extract a specific part of a URL.

Only the first match in the text is returned by the formula. 

<table><tbody><tr><td><strong>Function</strong></td><td><strong>Formula output</strong></td><td><strong>Example formula</strong></td><td><strong>Input</strong></td><td><strong>Result</strong></td></tr><tr><td rowspan="4">RegexExtract()</td><td rowspan="4">Alphanumeric characters</td><td rowspan="2">RegexExtract([url], "\\b[\\w-]+$")</td><td><u data-renderer-mark="true">https://example.com/product/12345</u>&nbsp;</td><td>12345&nbsp;</td></tr><tr><td><u data-renderer-mark="true">https://example.com/no-product-here</u>&nbsp;</td><td><em data-renderer-mark="true">Blank</em>&nbsp;</td></tr><tr><td>RegexExtract([email], "@(.*)")&nbsp;</td><td><u data-renderer-mark="true">Joe.smith@aol.com</u></td><td>@aol.com &nbsp;</td></tr><tr><td>RegexExtract("test string is this","t*")</td><td>test string is this</td><td><strong>te</strong><br>Note: te is the first match, and the only one returned.&nbsp;<strong>tr</strong> and&nbsp;<strong>th</strong> are not returned because they come after&nbsp;<strong>te</strong>.&nbsp;</td></tr></tbody></table>

## RegexReplace

Use the RegexReplace formula function to substitute values that match the regular expression with a replacement value. This is useful for things like normalizing phone numbers.

<table><tbody><tr><td><strong>Function</strong></td><td><strong>Formula field type</strong></td><td><strong>Example formula</strong></td><td><strong>Input</strong></td><td><strong>Result</strong></td></tr><tr><td rowspan="2">RegexReplace()</td><td rowspan="2">Formula - text</td><td rowspan="2">RegexReplace(ToText([client_contact]), "[()-. ]", "")</td><td>(555) 123-4567&nbsp;</td><td>5551234567&nbsp;</td></tr><tr><td>555.555.5555</td><td>5555555555</td></tr></tbody></table>

## Troubleshoot regex strings

We suggest testing regular expressions using online resources like [regex101](https://regex101.com/ "https://regex101.com/"). Select **Golang** under Flavor. There may be small differences in syntax.