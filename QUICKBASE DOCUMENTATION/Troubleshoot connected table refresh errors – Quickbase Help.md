-   [Find information about connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570327338132-Troubleshoot-connected-table-refresh-errors#Finding)
-   [Connect to cloud services](https://helpv2.quickbase.com/hc/en-us/articles/4570327338132-Troubleshoot-connected-table-refresh-errors#Connecti)
-   [Create a connection to Salesforce.com](https://helpv2.quickbase.com/hc/en-us/articles/4570327338132-Troubleshoot-connected-table-refresh-errors#Creating)
-   [Connect to a table in another Quickbase app](https://helpv2.quickbase.com/hc/en-us/articles/4570327338132-Troubleshoot-connected-table-refresh-errors#Troubleshooting_QuickBase_connections)
-   [Connect to the Admin Console](https://helpv2.quickbase.com/hc/en-us/articles/4570327338132-Troubleshoot-connected-table-refresh-errors#Connecti2)
-   [Connect to a folder containing CSV files](https://helpv2.quickbase.com/hc/en-us/articles/4570327338132-Troubleshoot-connected-table-refresh-errors#Troubleshooting_CSV)

Sometimes, we may not be able to refresh your connected data. The connection owner can usually resolve this using the information below. If you’re still having trouble, please reach out to our [Quickbase Technical Support team](https://helpv2.quickbase.com/hc/en-us/articles/4570259530644-Getting-help-from-Quickbase-Customer-Care-).

## Find information about connected tables

### View connected table details and history

To view **Details about your connected table**, including the connected service, connection owner, connected fields, filter, and schedule for the connected table, access the connection in table settings You can also view a **History** of recent refreshes, and [edit the connection filter](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table-Help-), [refresh schedule](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-), or [switch to use a different connection](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), if necessary.

### View, test, or delete your connections

To view **details about your connection** and [test](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-), [change](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), or [delete](https://helpv2.quickbase.com/hc/en-us/articles/4570322374036-Deleting-a-connection-) connections, click the user dropdown on the global bar, then click **Profile**. Your connections display in the **My Connections** area.

## Connect to cloud services

If you're having trouble connecting or refreshing data from cloud services, you may see one of the following:

| error includes: | Explanation | How to Fix the issue |
| --- | --- | --- |
| 
Column does not exist

 | 

The connected table is looking for a column in the service that no longer exists or is not accessible, based on permissions granted by the connection.

 | 

If you don't need this field, [remove the field](https://helpv2.quickbase.com/hc/en-us/articles/4570278916372-Adding-and-removing-connected-fields-#Remove_connected_fields) from the connected table and [edit the connection filter](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table-Help-#Edit_filter), if it includes any unavailable fields.

 |
| Invalid field | The column in the service may have been deleted. | If you need access to this data, sign in to the service with the same credentials and find out if the data is accessible. |
| Does not recognize queried object | Access privileges in the service may have been changed or the current connection may not have access to the table or fields. | You may need to make adjustments to your account, or if the data is not accessible using the credentials you signed in with, you'll need to use a connection with different credentials. See [switch connections](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-). |
| 

Query requires additional inputs

Requires credentials

Login verification failed

Invalid credentials

 | 

The login to the data source isn’t working.

 | 

Verifying your credentials and/or access to the data source and then [test and update your connection](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-).

 |
| 

Table source not found

 | 

We’re having trouble accessing a table in the data source.

 | 

Try again later.

 |

## Create a connection to Salesforce.com

If you're having trouble creating your Salesforce connection, check with your administrator to make sure Salesforce.com API access and permissions are enabled. Salesforce.com requires that your Salesforce.com account have **API access** enabled. Your user account must also have the **API Enabled** permission selected.

See [Salesforce User Permissions](https://help.salesforce.com/apex/HTViewHelpDoc?id=admin_userperms.htm&language=en) for more information.

## Connect to a table in another Quickbase app

If you're having trouble connecting to or refreshing from a table in another Quickbase app, you may see one of the following:

| Error includes: | Explanation | How to Fix the issue |
| --- | --- | --- |
| 
No such operation

SSL connection required

Unknown hostname

Reading the QuickBase API\_Authenticate response from ...  
QBI\_GetDBInfo failed

Reading the QuickBase QBIGetDBInfo response from ...  
API\_Authenticate failed

We couldn't save your connection

We couldn't connect to Quickbase

 | 

The Quickbase URL is incorrect.

 | 

Locate the Quickbase URL in the browser. For example, _https://myco.quickbase.com_.

Copy and paste the correct URL into the Quickbase URL field.

Don’t include the /db/ portion and what comes after it when copying and pasting into the Quickbase URL field.

Be sure to use https instead of http in the Quickbase URL field.

 |
| 

No such database or login operation requires a database name

 | 

The database ID is missing or incorrect.

 | 

Open the home page of the app.

In the URL that displays, copy the alpha-numeric text that displays after db/. For example, _bi4zjv7mq_.

 |
| 

Invalid application token

 | 

The application token is missing or incorrect.

 | 

Copy or create an app token for the app you want to connect to.

On the app home page, click **Settings**, then click **Manage Application Token**. Copy and paste the app token into the App Token field.

 |
| 

There was a problem refreshing the table

The error was: Invalid input - QB error code: 2

 | 

Possible causes include:

1.  The field type of a connected field was changed to a lookup field.
2.  The refresh attempted to pull a value into a connected field that exceeds the limit for that field.
3.  The refresh attempted to pull unsupported javascript into a field.
4.  The field type of a connected field changed from text to multi-select text, which has a limit of 100 choices. The refresh attempted to add data that exceeded that limit.

 | 

1.  Change the lookup field to a regular field type (for example, from Lookup - Text to Text, or Lookup - Numeric to Numeric), remove the connected field marked as lookup from the connected table, or mark the lookup field in the source table as unique.
2.  Review the source table to identify the field that caused the issue.
3.  Remove the unsupported javascript.
4.  Reduce the number of choices in the multi-select text field.

 |

## Connect to the Admin Console

If you are a realm admin and you do not see the Admin Console channel as an option listed in the sources when setting up a new connected table, check to make sure you have not exceeded the limit of three Admin Console connected tables per realm.

## Connect to a folder containing CSV files

If you're having trouble connecting to a folder containing CSV files, you may see one of the following:

| error includes: | Explanation | How to Fix the issue |
| --- | --- | --- |
| 
Table replication requires non-null key values

 | 

Null key values refers to empty cells in the column used as the [Refresh Key](https://helpv2.quickbase.com/hc/en-us/articles/4570260038804-About-the-Refresh-Key-field-) field.

 | 

Update the CSV file to include a value for this field in each record or change the Refresh Key.

 |
| 

We couldn't open the fields list

 | 

-   The CSV file has empty fields in the header row or duplicate fields in the header row. Each field in the header row must have a unique name.
-   There are duplicate values in the Refresh Key field or a missing value in the Refresh Key field.
-   The file name ends in .csv, but the file is not UTF8-encoded

 | 

Update the CSV file so that each field in the header row has a unique name.

Save the file as a UTF8-encoded .csv.

Make sure the value in the Refresh Key field is unique for each record (no duplicate entries or missing entries).

 |
| 

The resource '\[\[connection\_3226\]\]."Complete data export":ServiceDefinitionTable' does not exist.

 | 

The connected folder could not be found within the Quickbase Sync folder in the file storage service (Box, Dropbox, Google Drive).

 | 

Make sure the folder displays in the file storage service, inside the Quickbase Sync folder, and that it contains a valid .csv file.

 |
| 

The source data includes non-unique key values, the column value(s) from the source query that correspond to the destination key column(s) must be unique.

 | 

Multiple rows in the CSV file have the same value in the Refresh Key field.

 | 

Review the structure of your CSV file and the intended use of the data to determine how best to resolve duplicates and understand which column, containing unique values, makes the best Refresh Key for your data.

 |
| 

Unknown column: IndexName

 | 

An expected column name was not found in the CSV file.

 | 

Review your CSV file to determine if a column name changed.

 |
| 

Error parsing .csv. A cell contains an invalid quoted string.

 | 

The CSV file does not conform to the standard, such as a value containing an un-escaped double quote.

 | 

Review your CSV file and ensure that is it a UTF-8 encoded .csv files in which:

-   values are separated by commas
-   the same number of values are in each row
-   values containing special characters (commas, double quotes, and line breaks) must be enclosed in double quotes
-   if double quotes are used, then a double quote within a field must be escaped by preceding it with another double quote, for example "aaa", "b""bb","ccc"
-   leading and trailing blanks are not ignored
-   the first row contains the column names (no blanks or duplicates)

 |
| 

The file was example.csv. The error was: Invalid character in row 00001, field 1, position 1.

 | 

The CSV file contains a character that is not a valid UTF-8 character.

 | 

Locate and remove the invalid character. The error message identifies the first invalid character that is encountered in the file. The file’s header row is considered row 1. The field (column) number is based on the order the connected fields were added to the connected table. The position is where in the field the invalid character is located.

 |

Note: If your automatic refresh schedule was set to manual because of a number of unsuccessful refresh attempts, review the most recent error message in the table history and resolve the problem. After you resolve the problem, you can reset the refresh schedule to automatic.

If you’re having trouble, [please open a support case](https://www.quickbase.com/qb/support/redirecttorealm?subject=%22Issue+with+connected+table%22).

### Related topics:

-   [About connections](https://helpv2.quickbase.com/hc/en-us/articles/4570366771476-About-connections-)
    
-   [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-)
    
-   [FAQs about connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570374698388-FAQs-about-connected-tables-)
    
-   [Refreshing a connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)