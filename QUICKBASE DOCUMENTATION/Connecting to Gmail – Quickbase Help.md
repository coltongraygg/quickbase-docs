You can automatically import emails into Quickbase to save time and reduce the errors that can arise from manually copying and pasting messages into Quickbase. After you import the Gmail to a [connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-) in your Quickbase app, it can automatically refresh in Quickbase, based on a schedule that you set.

**Important**: Deleting a connection for Gmail, Google Drive, or QuickBooks will invalidate other QuickBase Sync connections that were created with the same Gmail, Google Drive, or QuickBooks log in credentials. This happens because when a connection is deleted, we send a request to the connected service to revoke the OAuth token that was used by that connection. When Google or QuickBooks receives the request, they invalidate all the OAuth tokens for Quickbase Sync for that user. The connections in Quickbase will fail until the connection owner reauthorizes the connection to get a new valid OAuth token.

To connect to Gmail:

1.  From the sidebar, click **New Table** and then select **Using connected data**.  
    ![tables_connected_data.png](https://helpv2.quickbase.com/hc/article_attachments/30864993692308) 
    
2.  Name your table, click **Next**, and then select **Gmail**.
    
3.  Enter your Gmail user name and password.
    
4.  Create your connected table. See [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-) or click the **Help** icon in the top right, while creating your table, and we'll guide you along.
    

## View, test, or delete your connections

To view **details about your connection** and [test](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-), [change](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), or [delete](https://helpv2.quickbase.com/hc/en-us/articles/4570322374036-Deleting-a-connection-) connections, click the user dropdown on the Global bar, then click **My preferences**. Your connections display in the **My Connections** area.

## View connected table details and history

To view **Details about your connected table**, including the connected service, connection owner, connected fields, filter, and schedule for the connected table, access the connection in **Table Settings**. You can also view a **History** of recent refreshes, and [edit the connection filter](https://helpv2.quickbase.com/hc/en-us/articles/4570365360148-Filtering-data-to-connect-in-a-connected-table-Help-), [refresh schedule](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-), or [switch to use a different connection](https://helpv2.quickbase.com/hc/en-us/articles/4570136372244-Switching-connections-), if necessary.

### Queries optimized for Quickbase

When you connect a table to a Gmail account, you can use two queries optimized for Quickbase. These are:

-   Inbox Summary by Conversation
    
-   Inbox with Forwards
    

Let's take a look at each of these.

![](https://helpv2.quickbase.com/hc/article_attachments/4572836165268)

### Inbox Summary by Conversation

Gmail has a handy feature that allows you to group responses together in a "conversation." With this feature enabled in Gmail, you can see all emails relating to one conversation inside a single email. You don't have to open several emails or search for a specific message to follow the conversation.

When you use this query, you won't have to bring in individual messages, and you can create just one record to contain a series of related messages. This reduces the number of records in your table and makes it easier to manage related customer communications.

The **Inbox Summary by Conversation** query has four fields that let you optimize the benefits of a Gmail conversation in your Quickbase table:

-   **# Thread Count** is a summary field that shows the number of messages in the conversation.
    
-   **Starting Date** is the date of the original email in the conversation
    
-   **Original To** is the email address of the first recipient of the message.
    
-   **Original From** is the email address of the first sender of the message.
    

When you import a Gmail conversation into Quickbase, each conversation will appear in a single block in your table, with the latest message at the top.

### Inbox with Forwards

Many businesses use Gmail for their company's communications. Here's a common scenario that illustrates how connecting a table to a Gmail account will enable you to track customer emails by importing them to Quickbase.

Let's say your sales reps send and receive emails to customers. To track them in a central location, sales reps forward these emails to a central Gmail account. To get these emails into Quickbase, set up a connection to this Gmail account.

The email address most useful to you is the customer's email address, but this address is buried in the body of the forwarded message. So, Quickbase provides four fields to let you bring the email addresses you care most about into your Quickbase table: 

-   **OriginalFrom** The email address of the customer.
    
-   **OriginalTo**. The email address of the sales rep who received the message.
    
-   **Forwarded From** The email address of the sales rep who forwarded the customer email to the central Gmail account.
    
-   **Forwarded To** The email address of the central Gmail account.
    

When you connect to the Gmail account, you select these fields and Quickbase will extract the customer's email address from the body of the email and import them to your Quickbase table.

### Related topics:

-   [About connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-)
    
-   [Adding a connected table to your app](https://helpv2.quickbase.com/hc/en-us/articles/4570271750292-Adding-a-connected-table-)
    
-   [Deleting a connection](https://helpv2.quickbase.com/hc/en-us/articles/4570322374036-Deleting-a-connection-)
    
-   [FAQs about connected tables](https://helpv2.quickbase.com/hc/en-us/articles/4570374698388-FAQs-about-connected-tables-)
    
-   [Testing a connection](https://helpv2.quickbase.com/hc/en-us/articles/4570323329812-Testing-a-connection-)
    
-   [Refreshing a connected table  
    ](https://helpv2.quickbase.com/hc/en-us/articles/4570263852436-Refreshing-a-connected-table-)