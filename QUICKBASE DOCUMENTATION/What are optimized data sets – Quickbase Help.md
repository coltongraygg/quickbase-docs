## What are optimized data sets?

When you create a [connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-), you can choose to create the table using a data set that has been optimized for Quickbase or you can select from advanced data, as displayed directly from the data source’s API. In most cases, **optimized data sets are the best choice** for your connected table.

[What are optimized for Quickbase data sets?](https://helpv2.quickbase.com/hc/en-us/articles/4570311621396-What-are-optimized-data-sets#what_are_optimized_datat_sets)

[What tables does data come from in the optimized data sets?](https://helpv2.quickbase.com/hc/en-us/articles/4570311621396-What-are-optimized-data-sets#defintions)

## What are optimized for Quickbase data sets?

Optimized for Quickbase data sets are a ready-to-use collection of the most commonly requested data sets from popular cloud apps, like QuickBooks Online and Salesforce.com. They are created and maintained by Quickbase and designed to provide quick access to the data you need.

For example, you might choose the Accounts data set if you want to connect account names, numbers, balances, and other important fields in Salesforce.com.

This optimized data set contains all the columns you’ll likely need when connecting Salesforce accounts:

![](https://helpv2.quickbase.com/hc/article_attachments/4572821453844/optimized_data_set.png)

## What tables does data come from in the optimized data sets?

Data may come from one or multiple joined tables:

**Salesforce.com**

| This Salesforce.com optimized data set... | references these tables... |
| --- | --- |
| Accounts | Account, User |
| Campaigns | Campaign, User |
| Case with History | Case, CaseHistory, Contact, Account, Asset, User |
| Contacts | Contact, Account, User |
| Contracts | Contract, Account, Contact, User |
| Leads | Lead, User |
| Opportunities | Opportunity, Account, Campaign, User |

**QuickBooks Online**

| This QuickBooks Online optimized data set... | references these tables... |
| --- | --- |
| Accounts | Account |
| Customers or Clients | Customer |
| Bills - Line Items | Bill |
| Invoices | Invoice |
| Invoice - Line Items | Invoice |
| Invoices Payments - Line Items | Invoice, Payment |
| JournalEntries - Line Items | JournalEntry |
| Payments - Line Items | Payment |
| Products and Services | Item |
| Purchase Orders - Line Items | PurchaseOrder table |
| Purchases - Line Items | Purchase |
| Time Activities | TimeActivity |

**Sample Data**

| This Sample Data optimized data set... | references these tables... |
| --- | --- |
| Call Log | calls, customers, employees |
| Order Log | orders, items, employees, products |
| Order Log by Country | orders, items, products, countries |
| Products by Country | orders, items, products, countries |
| Sales by Employee | orders, customers, items, employees, products |
| Sales by Region | orders, items, customers, countries |

### Related topics:

-   [About connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-)
    
-   [Adding connected fields](https://helpv2.quickbase.com/hc/en-us/articles/4570325865236-Adding-more-connected-fields-)
    
-   [FAQs about connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570374698388-FAQs-about-connected-tables-)
    
-   [Filtering connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table-Help-)
    
-   [Refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)