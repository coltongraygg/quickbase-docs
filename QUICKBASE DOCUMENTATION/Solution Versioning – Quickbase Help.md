## Solution Versioning

> Access to this feature can change based on your Quickbase plan. Learn more about feature availability and plans in [Quickbase capabilities](https://helpv2.quickbase.com/hc/en-us/articles/21309804922004).

In Quickbase Solutions, you can use versioning to store and deploy versions of a solution, creating a layer of security and control over any development effort.

Note that versioning does not support plugins. When you restore, the link to the plugin will be removed from the app. 

This article explains how to create new versions and roll back to stored versions. To learn more about navigating solutions and required permissions, read [Solutions](https://helpv2.quickbase.com/hc/en-us/articles/14153924852756).

In this article

-   [Versioning on the Solutions level](https://helpv2.quickbase.com/hc/en-us/articles/14153734546836-Solution-Versioning#01GWJ10CZA803WQ4CX6W91C0AV)
-   [Rollback to a stored version](https://helpv2.quickbase.com/hc/en-us/articles/14153734546836-Solution-Versioning#01GWJ10CZAX828JCAJKVFE7M6H)
-   [When no common resources exist](https://helpv2.quickbase.com/hc/en-us/articles/14153734546836-Solution-Versioning#01H553JX9SSFFY8X2GR92PDWRR)
-   [Deleting Versions](https://helpv2.quickbase.com/hc/en-us/articles/14153734546836-Solution-Versioning#01GWJ10CZBB4JHWS6M0WVA5TYP)

## Versioning on the Solutions level

The Versioning feature works at the Solutions level over schema only and not your data. A schema is a digital plan that shows how your data is organized within a Quickbase database. This means that when you create a Solution Versioning snapshot, it's a snapshot of the schema of all resources in the solution. As a Solutions Manager or Contributor, enter **[My solutions](https://helpv2.quickbase.com/hc/en-us/articles/14153924852756),** select a single solution and take a snapshot of the Solution by clicking on **New Version:** 

![](https://helpv2.quickbase.com/hc/article_attachments/14327465945492)

This snapshot is stored in **My solutions**. 

![soluutions1.png](https://helpv2.quickbase.com/hc/article_attachments/14326712678036)

-   You can store multiple versions of the same Solution.
    
-   View a list of all versions stored and their metadata.
    
-   Up to 30 versions to be stored per solution.
    

## Rollback to a stored version

You can select a snapshot version and restore it. This will replace the running solutions structure with one from the snapshot. From the version detail page, click **Restore**:

![versions.detail.restore.png](https://helpv2.quickbase.com/hc/article_attachments/14327751433876)

Compare this version to the live solution and click **Next step** to continue the process. We will not restore any deleted apps or pipelines and we won't revert apps or pipelines that were removed from the solution after the back up was made. Apps or pipelines added since the version was created will remain in the solution, but will not be rolled back, since they weren't in the original back up. 

![restore0.png](https://helpv2.quickbase.com/hc/article_attachments/14401646073108)

If the running version contains tables/fields that are not present in the old version, you will receive a warning that the replacement will delete all data from the missing tables/fields. 

If the old version contains fields/tables that are not present in the running version, those will still be created by a roll back. No data will be restored.

![restore.1.png](https://helpv2.quickbase.com/hc/article_attachments/14401682462100)

Click **Restore** to proceed with the restore process. 

**Note**: during the restoration process that takes a few of seconds, the pipelines in the solution will be in edit mode which means they will not be executed during that time, just like if you enter a pipeline to edit it through the pipelines designer.

### Versioning and plugins

Versioning does not support plugins. During restore, any link to a plugin will not display.

## When no common resources exist

You cannot start a version restore when there are no common resources (apps/pipelines) in the schema of the solution. If you try to restore a version with no common resources, an error message displays and you will not be able to proceed with the restore of this version.

![restore.png](https://helpv2.quickbase.com/hc/article_attachments/17330320806676)

## Deleting Versions

You can delete a stored version of the solution. From the version detail page, click **Delete**:

![versions.detail.delete.png](https://helpv2.quickbase.com/hc/article_attachments/14327751440276)

Click **Yes, Delete** to delete the snapshot:

![versions.delete.png](https://helpv2.quickbase.com/hc/article_attachments/14326975898900)

### Listing versions

You can display all the versions that exist for your solution:

![history.versions.v2.png](https://helpv2.quickbase.com/hc/article_attachments/15754909529620)