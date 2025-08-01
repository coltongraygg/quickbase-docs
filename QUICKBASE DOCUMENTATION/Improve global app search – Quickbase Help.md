## Improve global app search

Global app search is accessible from the **Search** button on the global bar. If you are on an app's home page, clicking **Search** will display a dropdown that lets you enter a search term. Searching from this location will search the entire app.

## Which fields are searched by global app search?

Global app search will search fields marked **Searchable** that your role has access to. Field types are set to searchable by default [depending on the field type](https://helpv2.quickbase.com/hc/en-us/articles/4570297480980-About-field-types-). The built-in fields **Date Created**, **Date Modified**, and **Record ID#** are also set to not be searched by default. Read more about the [Searchable property.](https://helpv2.quickbase.com/hc/en-us/articles/4570284211860-Excluding-fields-from-searches-#searchable)

## Why don't I see my search term in the results?

The search results are displayed using the default report for each table. Sometimes the default report doesn't include the field that contains your search term.

## Why is global app search sometimes slow?

Global app search is equivalent to searching for _<Some field> contains My\_search\_term_ in every table in the app. By default, the search must look at the contents of every field in every record in every table to return results.

Instead, you can set the default behavior for global search within an app to **Match the search term exactly**, rather than match any terms that contain the typed value. In the app settings area, go to **App properties**, then look for **Performance options** in the **Advanced settings** area of the page, and select the **Match the search term exactly** checkbox.

If you do set the default to Global searches in this app default to **Match search term exactly**, users will still have a option to clear the **Match search term exactly** checkbox and search instead for a value containing the value that they type.

A _<Some field> contains My\_search\_term_ global search may be slower if your tables have some combination of these three factors:

-   Many records (tens of thousands)
-   Hundreds or thousands of fields in each table (especially if many of those fields are text fields)
-   Lots of data stored in text or formula fields

## Optimizing global app search for your users

Try some of these techniques to improve the search experience for your users:

-   Try table search
-   Try exact search
-   Create targeted reports
-   Create custom search widgets
-   Archive some data
-   Hide fields and tables from some roles

Each of these techniques is described below.

### Try table search

First of all, recommend that your app users try the table search functionality (2) before running global app searches (1).

![](https://helpv2.quickbase.com/hc/article_attachments/31642580835604)

### Try exact search

Recommend that your app users select **Match search term exactly** on the search dropdown, for app search and table search. When this checkbox is selected, the search changes to _<Some field> **is equal to** My\_search\_term_. This type of search is generally faster than a _contains_ search.

### Create targeted reports

Next, investigate what your app users most commonly search for, and create "[ask the user](https://helpv2.quickbase.com/hc/en-us/articles/4570432732948-Create-a-Report-that-Prompts-Users-for-Selection-Criteria-)" filters or targeted reports that will handle those searches. You can use all the usual techniques of creating reports to narrow the amount of data that will be searched.

![](https://helpv2.quickbase.com/hc/article_attachments/31642565556116)

### Create custom search widgets

Hide the **Search** button on the global bar for most roles. Create custom search widgets on the app home page so that your app users can perform targeted searches.

![](https://helpv2.quickbase.com/hc/article_attachments/31642565557012)

Search widgets will perform a _contains_ search by default, but they can be [configured](https://helpv2.quickbase.com/hc/en-us/articles/4570312276756-About-Search-Widgets-) to look for the exact search term entered instead. Using **Match search term exactly** causes your searches to be faster because it is not a a _contains_ search.

### Archive data

If your tables are very large or contain historical data, try archiving some of that unused data – that way there's less to search.

### Hide fields and tables

If your users still choose to use the global app search, here are some techniques for improving the experience:

-   Unset the **Searchable** property on fields/tables that you don't want to search. [Learn more](https://helpv2.quickbase.com/hc/en-us/articles/4570284211860-Excluding-fields-from-searches-).
    
    Fields that tend to cause performance issues include Text fields (especially Text - Multi-line with log entries turned on, and formula fields).
    
-   Use role settings to hide very large tables from roles that tend to do a lot of searching.
    

### Related topics:

-   [To search your app](https://helpv2.quickbase.com/hc/en-us/articles/4570425947796-How-Can-I-Quickly-Find-Information-in-My-Application-)
    
-   [Understanding Quickbase searches](https://helpv2.quickbase.com/hc/en-us/articles/4570284211860-Excluding-fields-from-searches-)
    
-   [To prevent Quickbase from searching a specific table:](https://helpv2.quickbase.com/hc/en-us/articles/4570352802964-Prevent-Quickbase-from-Searching-a-Table-)
    
-   [Creating a Search widget](https://helpv2.quickbase.com/hc/en-us/articles/4570312276756-About-Search-Widgets-)
    
-   [Hide one or more UI options](https://helpv2.quickbase.com/hc/en-us/articles/4570326445204-Customizing-the-user-interface-by-roles-#Hide_one_or_more_menus_from_users_in_this_role._)