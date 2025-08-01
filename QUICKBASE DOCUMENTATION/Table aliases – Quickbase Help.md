## Table aliases

Each table in an app has an alias that serves as a unique identifier. Use table aliases in formulas or API calls and other URLs to reference tables.

## Finding table aliases

1.  Open the table settings, then select **Advanced settings**.
    
2.  Select **Advanced Table Settings** to expand the section.
    
    The table alias appears in all capital letters at the bottom of the section.
    
    Note: You can't change the name of a table alias.
    

![simplified representation of the options in advanced table settings highlighting the table alias _DBID_CLIENT at the end](https://helpv2.quickbase.com/hc/article_attachments/29944788670100)

## Referencing table aliases

### Formulas

Surround the alias in brackets, for example `[_DBID_PROJECTS]`, to reference it in a formula. 

### APIs and URLs

Surround the alias with parentheses, for example `(_DBID_PROJECTS)`, to reference it in URLs, like API calls or navigation URLs.

#### URLs for navigating

Because of updates to Quickbase URL pattern, there are two ways to construct navigation URLs that use table aliases:

-   Legacy: `example.quickbase.com/db/{appDBID}/({tableAlias})?a={action}`
-   Updated: `example.quickbase.com/nav/app/{appDBID}/table/({tableAlias})?a={action}`

While the legacy pattern will continue to be supported, it is highly suggested to use the updated pattern. The updated pattern follows best practices for modern websites and provides a content hierarchy for easy learning. Learn more about [Quickbase's URL updates](https://helpv2.quickbase.com/hc/en-us/articles/26352739460756).