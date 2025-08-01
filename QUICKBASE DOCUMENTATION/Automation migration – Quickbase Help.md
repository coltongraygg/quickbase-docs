## Migrating your automations

Use the migration tool to copy your automation to Pipelines. On the Automations page, automations appear in different states of migration:

-   **Start Migration** means that nothing has started yet for this automation
-   **Analyzed** means that this automation has been analyzed, but not yet migrated
-   **Migrated** means that this automation has already been migrated.

To start this process:

1.  Select Automations on the App Settings or Table Settings page
2.  Click **Start migration** on the automation you want to migrate. The migration window displays and an analysis of your migration begins. This analysis checks to see if there is anything that would make this less than successful, for example, if we didn’t have access to pipelines, or there was something unusual in the structure of our automation. Once the analysis completes, you can start the migration. If there are any issues, resolve them and try again. Otherwise, click **Start migration**.

When it is complete, your migrated automation is copied to pipelines. Your existing automation is retained, so don’t forget to deactivate it when you are working with your pipeline. The migration process doesn’t delete or deactivate your automation. Each migration has a unique ID, so you can refer to it, if you ever need to talk to a Quickbase representative in case you encounter an error. When your pipeline is created it is not turned on.

Each migration will typically take less than five minutes. Once the migration phase has started you cannot cancel the migration. If you navigate away from the migration, you will be able to resume the process.

You can start migrating multiple automations at the same time. There aren't any limits on how many migration you can start at the same time. They may not start at the same time and will be queued. You cannot start multiple migrations for the same automation.

If you complete the analysis phase and don't migrate, you can always start the migration process later unless you have edited the automation. In that case you will need to compete the analysis phase again. Do not edit the automation after you have started the process.

If you migrate the same automation more than once, a different unique pipeline is created. Just click **Migrate again**, for example:

![](https://helpv2.quickbase.com/hc/article_attachments/4572834320532/migrate.again.png)

## What does the automation look like when converted?

The following table shows automation components and their Pipeline equivalents.

| 
Automations

 | 

Pipelines

 |
| --- | --- |
| 

Simple Triggers

![](https://helpv2.quickbase.com/hc/article_attachments/4572812944404/conversion.1_600x288.png)

 | 

On Trigger

![](https://helpv2.quickbase.com/hc/article_attachments/4572812975124/conversion.2_600x614.png)

 |
| 

Combination Triggers

![](https://helpv2.quickbase.com/hc/article_attachments/4572806186260/conversion.5_600x272.png)

 | 

On Event

![](https://helpv2.quickbase.com/hc/article_attachments/4572813003284/conversion.6_600x737.png)

 |
| 

Add Record

![](https://helpv2.quickbase.com/hc/article_attachments/4572813039508/conversion.3_600x151.png)

 | 

Add Record Action

![](https://helpv2.quickbase.com/hc/article_attachments/4572828364180/conversion.4_600x545.png)

 |
| 

Modify Record(s)

![](https://helpv2.quickbase.com/hc/article_attachments/4572841060628/conversion.7_600x202.png)

 | 

Bulk Upsert

![](https://helpv2.quickbase.com/hc/article_attachments/4572806309012/conversion.8_600x761.png)

 |
| 

Define Schedule

![](https://helpv2.quickbase.com/hc/article_attachments/4572813124884/automation.sched.png)

 | 

Schedule Pipeline

![](https://helpv2.quickbase.com/hc/article_attachments/4572828486036/sched.pipe.png)

 |
| 

Automation calendar widget keywords

![](https://helpv2.quickbase.com/hc/article_attachments/4572828547348/automations.widget.png)

 | 

Pipeline's jinja

![](https://helpv2.quickbase.com/hc/article_attachments/4572828573588/pipeline.jinja.1.png)![](https://helpv2.quickbase.com/hc/article_attachments/4572828607252/pipeline.jinja.2.png)

 |
| 

Automations Old Value

![](https://helpv2.quickbase.com/hc/article_attachments/4572828621076/old.value.png)

 | 

Pipelines Old Value

![](https://helpv2.quickbase.com/hc/article_attachments/4572828630420/old.val.pipe.png)

 |
| 

Automations Delete

![](https://helpv2.quickbase.com/hc/article_attachments/4572828654100/automations.delete.record.png)

 | 

Pipelines Remove

![](https://helpv2.quickbase.com/hc/article_attachments/4572828690452/pipeline.remove.record.png)

 |

### Copy records and import table to table

The migration supports automations with copy records and import table to table. The Copy record automation action step migrates as a loop with **Bulk upsert** but does not complete values for the merge field, which means that it is always insert/create new record.

Table to table actions migrate to a Quickbase channel step using the **Make Request** and we will call the import action as an request.**Make Request** is a similar to Webhooks channel **Make Request** step except we do not specify the credentials in clear text values (the usertoken).

## How many automations can I migrate?

You can migrate one automation at a time or you can migrate as many as you want. For example, you can start more than one migration, navigate away, and come back later while the migrations continue in the backgrouond.

During the process you can close the migration window and return later.

## How are Quickbase credentials created

The migration process creates a new Usertoken in Quickbase and Quickbase Credentials in Pipelines. Do not delete these credentials in Pipelines.

## Finding converted Pipelines

Each converted automation is tagged as 'Migrated from Automations' with the original automation name and a unique ID. For example, this migrated automation:

![](https://helpv2.quickbase.com/hc/article_attachments/4572828698644/pipeline.details.2_400x246.png)

Is tagged, Migrated from Automations:

![](https://helpv2.quickbase.com/hc/article_attachments/4572841530260/pipeline.details.1_400x787.png)

## Who can perform migrations

You must have access to the app as the admin to be able to perform a migration . Only automation owners can perform a migration and you also must have access to Pipelines - the migration will not grant you access to Pipelines. Please contact your admin to update your permissions.

## Why does migrating an automation to a pipeline does not deactivate or delete the pipeline?

-   **Multiple Automations** - There could be scenarios when you may want to migrate more than a single automation in order for your workflow to be complete. We anticipate a customer to go through migrate a couple automations, see how the Pipelines behaves together, and manage a cluster.
-   **Flow/Testing** - We've seen customers navigate away to the newly migrated pipeline’s editor, then test out with small data and then determine the switching off themselves later.

## After the migration

When the migration is complete, the existing automation will not be disabled or deleted.

## Migration Limits

In rare situations there are some restrictions on what cannot be migrated. We are working to remove these restrictions. These issues will display during the analysis phase of the migration. Currently, we do not support:

-   Since Pipelines currently limits to 26 steps, the migration stops if your automation has more than 26 steps.

-   If you have a Quickbase formula directly included in your automation, it cannot be migrated, since Pipelines uses the jinja language instead of formulas. Jinja supports similar use cases as formulas and adds more powerful features such as loops.