## Share data across apps

## Methods for sharing data

Quickbase apps manage data for processes. When you need to replicate, share, or transform this data, you have different options including:

-   [Connected tables](https://helpv2.quickbase.com/hc/en-us/articles/19713658161428#h_01HBV1976AFQ1ZBMX5GGNFWMAG)
-   [Pipelines](https://helpv2.quickbase.com/hc/en-us/articles/19713658161428#h_01HBV1HHJJNG59ZH8HTEW8AV2K)
-   [Cross-app relationships](https://helpv2.quickbase.com/hc/en-us/articles/19713658161428#h_01HBTXYD2RPYQK18DPQ3N4M6J2)
-   [Table-to-table imports](https://helpv2.quickbase.com/hc/en-us/articles/19713658161428#h_01HBTYD5M0WVT3EXAAVP2TZP7J)

Consider your particular data needs and the pros and cons of each option to select the one that best suits your app. Key factors to consider are your needs for immediacy, consistency, and control.

For a detailed discussion, see [Sharing Data Across Quickbase Apps](https://helpv2.quickbase.com/hc/en-us/articles/19713658161428)

## Limits

We prevent app builders from using cross-app relationships, table-to-table imports, or shared multiple-choice fields if it will result in a group of apps dependent on each other that take up more than 50gb of estimated memory (learn more about how memory is calculated in the [Quickbase Memory Calculations community post](https://community.quickbase.com/blogs/evan-martinez1/2019/08/30/quick-base-memory-calculations)).

Apps that exceeded this limit before we put it in place may experience instability or may not perform as expected with all features such as app copies or backup/restore.

### Finding memory estimations for your app

1.  From the app home page, click the Settings icon![](https://helpv2.quickbase.com/hc/article_attachments/14598715320084).
2.  Click **App Management** in the **Advanced Features** column.   
    ![](https://helpv2.quickbase.com/hc/article_attachments/14598748711572)
3.  Click **Show app statistics** in the **Show App Info** section.  
    ![](https://helpv2.quickbase.com/hc/article_attachments/14598817013012)
4.  Find **Est. memory incl. dependent apps** on the list.  
    ![](https://helpv2.quickbase.com/hc/article_attachments/14598870665364)

### What to do if you encounter this limit

-   Choose a different method to share data besides a cross-app relationship, table-to-table import, or shared multiple-choice field.
    
-   Try to optimize your app by deleting unused fields and migrating tables to a separate app. Customers on Enterprise-level plans can access the [Performance Optimizer](https://helpv2.quickbase.com/hc/en-us/articles/4570391172884) and [Performance Insights](https://helpv2.quickbase.com/hc/en-us/articles/9302765409044) for more help optimizing their apps.
-   Contact our Technical Support team or your account team for help scaling your apps.