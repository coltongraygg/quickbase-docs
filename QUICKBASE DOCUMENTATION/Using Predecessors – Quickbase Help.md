## Using Predecessors

In Quickbase, you can keeps items in a sequenced order by using **predecessor fields**. For example, tasks in a project can occur in a specific order where one task cannot start until another task finishes. A predecessor task must finish before another task can begin. When you specify a predecessor for a task, you set up a dependency between two tasks.

When you link a task to a predecessor, you link their dates together. The projected finish date of a predecessor task automatically becomes the start date of a successor task. If you make changes to a predecessor's start date or duration, Quickbase automatically updates the calculated finish date. That finish day automatically carries over into the Start Date field of the successor task. For example, if a task's start date is changed to be one day later, Quickbase automatically changes the start date of the successor task to reflect the one day delay.

Project management apps built by the Quickbase team come with predecessors built-in. To see this feature in action, create an app using a project management app from the Exchange. 

![](https://helpv2.quickbase.com/hc/article_attachments/33585688589844)  
For example, in the Simple Project Manager app, the Start field of a task has a dot in the field that indicates the predecessor. When you hover over it, it explains that the task cannot start until this date because of its predecessors.

Using predecessor fields with work dates.

Read about how to [add predecessors](https://helpv2.quickbase.com/hc/en-us/articles/4570317165076-Add-Dependencies-to-an-Existing-Project-Management-Application-) to any project management app.

### Related topics:

-   [Creating dependencies by adding predecessor fields](https://helpv2.quickbase.com/hc/en-us/articles/4570317165076-Add-Dependencies-to-an-Existing-Project-Management-Application-)