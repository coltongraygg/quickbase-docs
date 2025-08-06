# Project Management App - Quickbase Implementation Guide

## Implementation Overview

This guide provides detailed UI navigation steps for building a comprehensive project management application in Quickbase. Each step includes specific clicks, menu locations, and field configurations.

## Step 1: Create the Application

1. **Navigate to Application Creation**
   - Log into your Quickbase account
   - From the My Apps page, click the **"Create a new app"** button (blue button, top right)
   - Select **"Start from scratch"**

2. **Configure Application Settings**
   - **App name:** Enter "Project Management System"
   - **Description:** Enter "Internal business project management for tracking projects, teams, and tasks"
   - Click **"Create app"** button

3. **Initial Setup**
   - Quickbase will create your app with a default table
   - You'll be taken to the App Home page
   - Note your app URL for future reference

## Step 2: Create Core Tables (In Order)

### Table 1: Team Members Table
**This must be created first as other tables will reference it**

1. **Create the Table**
   - From App Home, click **"Add table"** (+ icon in left sidebar)
   - Select **"Create a blank table"**
   - **Table name:** "Team Members"
   - **Single record name:** "Team Member"
   - **Plural record name:** "Team Members"
   - Click **"Create table"**

2. **Configure Table Fields**
   Navigate to **Settings > Table > Fields** or click **"Fields"** tab

   **Field 1: Member Name**
   - Click **"+ Add field"**
   - **Field type:** Text
   - **Field name:** "Member Name"
   - **Size:** 255 characters
   - Check **"Required field"**
   - Click **"Save"**

   **Field 2: Email**
   - Click **"+ Add field"**
   - **Field type:** Email Address
   - **Field name:** "Email"
   - Check **"Required field"**
   - Click **"Save"**

   **Field 3: Employee ID**
   - Click **"+ Add field"**
   - **Field type:** Text
   - **Field name:** "Employee ID"
   - **Size:** 50 characters
   - Check **"Unique field"** (under Advanced Options)
   - Click **"Save"**

   **Field 4: Department**
   - Click **"+ Add field"**
   - **Field type:** Text
   - **Field name:** "Department"
   - **Size:** 100 characters
   - Click **"Save"**

   **Field 5: Job Title**
   - Click **"+ Add field"**
   - **Field type:** Text
   - **Field name:** "Job Title"
   - **Size:** 100 characters
   - Click **"Save"**

   **Field 6: Hire Date**
   - Click **"+ Add field"**
   - **Field type:** Date
   - **Field name:** "Hire Date"
   - Click **"Save"**

   **Field 7: Status**
   - Click **"+ Add field"**
   - **Field type:** Multiple choice - Text
   - **Field name:** "Status"
   - **Choices:** Enter each on a new line:
     ```
     Active
     Inactive
     On Leave
     ```
   - **Default value:** Select "Active"
   - Click **"Save"**

### Table 2: Teams Table

1. **Create the Table**
   - From App Home, click **"Add table"** (+ icon in left sidebar)
   - Select **"Create a blank table"**
   - **Table name:** "Teams"
   - **Single record name:** "Team"
   - **Plural record name:** "Teams"
   - Click **"Create table"**

2. **Configure Table Fields**

   **Field 1: Team Name**
   - Click **"+ Add field"**
   - **Field type:** Text
   - **Field name:** "Team Name"
   - **Size:** 255 characters
   - Check **"Required field"**
   - Click **"Save"**

   **Field 2: Team Manager**
   - Click **"+ Add field"**
   - **Field type:** User
   - **Field name:** "Team Manager"
   - Check **"Required field"**
   - Click **"Save"**

   **Field 3: Department**
   - Click **"+ Add field"**
   - **Field type:** Text
   - **Field name:** "Department"
   - **Size:** 100 characters
   - Click **"Save"**

   **Field 4: Team Description**
   - Click **"+ Add field"**
   - **Field type:** Rich text
   - **Field name:** "Team Description"
   - Click **"Save"**

   **Field 5: Created Date**
   - Click **"+ Add field"**
   - **Field type:** Date
   - **Field name:** "Created Date"
   - **Default value:** Select "Today"
   - Click **"Save"**

   **Field 6: Status**
   - Click **"+ Add field"**
   - **Field type:** Multiple choice - Text
   - **Field name:** "Status"
   - **Choices:**
     ```
     Active
     Inactive
     Restructuring
     ```
   - **Default value:** Select "Active"
   - Click **"Save"**

### Table 3: Projects Table

1. **Create the Table**
   - From App Home, click **"Add table"**
   - Select **"Create a blank table"**
   - **Table name:** "Projects"
   - **Single record name:** "Project"
   - **Plural record name:** "Projects"
   - Click **"Create table"**

2. **Configure Table Fields**

   **Field 1: Project Title**
   - Click **"+ Add field"**
   - **Field type:** Text
   - **Field name:** "Project Title"
   - **Size:** 255 characters
   - Check **"Required field"**
   - Click **"Save"**

   **Field 2: Description**
   - Click **"+ Add field"**
   - **Field type:** Rich text
   - **Field name:** "Description"
   - Click **"Save"**

   **Field 3: Requirements**
   - Click **"+ Add field"**
   - **Field type:** Rich text
   - **Field name:** "Requirements"
   - Click **"Save"**

   **Field 4: Edge Cases**
   - Click **"+ Add field"**
   - **Field type:** Rich text
   - **Field name:** "Edge Cases"
   - Click **"Save"**

   **Field 5: Estimated Completion Date**
   - Click **"+ Add field"**
   - **Field type:** Date
   - **Field name:** "Estimated Completion Date"
   - Click **"Save"**

   **Field 6: Actual Completion Date**
   - Click **"+ Add field"**
   - **Field type:** Date
   - **Field name:** "Actual Completion Date"
   - Click **"Save"**

   **Field 7: Status**
   - Click **"+ Add field"**
   - **Field type:** Multiple choice - Text
   - **Field name:** "Status"
   - **Choices:**
     ```
     Not Started
     In Progress
     Complete
     Awaiting Approval
     ```
   - **Default value:** Select "Not Started"
   - Click **"Save"**

   **Field 8: Priority**
   - Click **"+ Add field"**
   - **Field type:** Multiple choice - Text
   - **Field name:** "Priority"
   - **Choices:**
     ```
     Low
     Medium
     High
     Critical
     ```
   - **Default value:** Select "Medium"
   - Click **"Save"**

   **Field 9: Budget**
   - Click **"+ Add field"**
   - **Field type:** Currency
   - **Field name:** "Budget"
   - Click **"Save"**

   **Field 10: Created Date**
   - Click **"+ Add field"**
   - **Field type:** Date
   - **Field name:** "Created Date"
   - **Default value:** Select "Today"
   - Click **"Save"**

   **Field 11: Created By**
   - Click **"+ Add field"**
   - **Field type:** User
   - **Field name:** "Created By"
   - **Default value:** Select "Current User"
   - Click **"Save"**

### Table 4: Key Milestones Table

1. **Create the Table**
   - From App Home, click **"Add table"**
   - Select **"Create a blank table"**
   - **Table name:** "Key Milestones"
   - **Single record name:** "Milestone"
   - **Plural record name:** "Key Milestones"
   - Click **"Create table"**

2. **Configure Table Fields**

   **Field 1: Milestone Name**
   - Click **"+ Add field"**
   - **Field type:** Text
   - **Field name:** "Milestone Name"
   - **Size:** 255 characters
   - Check **"Required field"**
   - Click **"Save"**

   **Field 2: Description**
   - Click **"+ Add field"**
   - **Field type:** Rich text
   - **Field name:** "Description"
   - Click **"Save"**

   **Field 3: Target Date**
   - Click **"+ Add field"**
   - **Field type:** Date
   - **Field name:** "Target Date"
   - Check **"Required field"**
   - Click **"Save"**

   **Field 4: Actual Date**
   - Click **"+ Add field"**
   - **Field type:** Date
   - **Field name:** "Actual Date"
   - Click **"Save"**

   **Field 5: Status**
   - Click **"+ Add field"**
   - **Field type:** Multiple choice - Text
   - **Field name:** "Status"
   - **Choices:**
     ```
     Not Started
     In Progress
     Complete
     Overdue
     ```
   - **Default value:** Select "Not Started"
   - Click **"Save"**

   **Field 6: Priority**
   - Click **"+ Add field"**
   - **Field type:** Multiple choice - Text
   - **Field name:** "Priority"
   - **Choices:**
     ```
     Low
     Medium
     High
     Critical
     ```
   - **Default value:** Select "Medium"
   - Click **"Save"**

### Table 5: Tasks Table

1. **Create the Table**
   - From App Home, click **"Add table"**
   - Select **"Create a blank table"**
   - **Table name:** "Tasks"
   - **Single record name:** "Task"
   - **Plural record name:** "Tasks"
   - Click **"Create table"**

2. **Configure Table Fields**

   **Field 1: Task Name**
   - Click **"+ Add field"**
   - **Field type:** Text
   - **Field name:** "Task Name"
   - **Size:** 255 characters
   - Check **"Required field"**
   - Click **"Save"**

   **Field 2: Description**
   - Click **"+ Add field"**
   - **Field type:** Rich text
   - **Field name:** "Description"
   - Click **"Save"**

   **Field 3: Due Date**
   - Click **"+ Add field"**
   - **Field type:** Date
   - **Field name:** "Due Date"
   - Click **"Save"**

   **Field 4: Estimated Hours**
   - Click **"+ Add field"**
   - **Field type:** Numeric
   - **Field name:** "Estimated Hours"
   - **Format:** Decimal places: 2
   - Click **"Save"**

   **Field 5: Actual Hours**
   - Click **"+ Add field"**
   - **Field type:** Numeric
   - **Field name:** "Actual Hours"
   - **Format:** Decimal places: 2
   - Click **"Save"**

   **Field 6: Status**
   - Click **"+ Add field"**
   - **Field type:** Multiple choice - Text
   - **Field name:** "Status"
   - **Choices:**
     ```
     Not Started
     In Progress
     Complete
     Awaiting Approval
     Blocked
     ```
   - **Default value:** Select "Not Started"
   - Click **"Save"**

   **Field 7: Priority**
   - Click **"+ Add field"**
   - **Field type:** Multiple choice - Text
   - **Field name:** "Priority"
   - **Choices:**
     ```
     Low
     Medium
     High
     Critical
     ```
   - **Default value:** Select "Medium"
   - Click **"Save"**

   **Field 8: Created Date**
   - Click **"+ Add field"**
   - **Field type:** Date
   - **Field name:** "Created Date"
   - **Default value:** Select "Today"
   - Click **"Save"**

   **Field 9: Created By**
   - Click **"+ Add field"**
   - **Field type:** User
   - **Field name:** "Created By"
   - **Default value:** Select "Current User"
   - Click **"Save"**

## Step 3: Create Junction Tables for Many-to-Many Relationships

### Junction Table 1: Team Assignments

1. **Create the Table**
   - From App Home, click **"Add table"**
   - Select **"Create a blank table"**
   - **Table name:** "Team Assignments"
   - **Single record name:** "Team Assignment"
   - **Plural record name:** "Team Assignments"
   - Click **"Create table"**

2. **Configure Fields**

   **Field 1: Assignment Date**
   - Click **"+ Add field"**
   - **Field type:** Date
   - **Field name:** "Assignment Date"
   - **Default value:** Select "Today"
   - Click **"Save"**

   **Field 2: Role**
   - Click **"+ Add field"**
   - **Field type:** Text
   - **Field name:** "Role"
   - **Size:** 100 characters
   - Click **"Save"**

   **Field 3: Status**
   - Click **"+ Add field"**
   - **Field type:** Multiple choice - Text
   - **Field name:** "Status"
   - **Choices:**
     ```
     Active
     Inactive
     ```
   - **Default value:** Select "Active"
   - Click **"Save"**

### Junction Table 2: Project Team Assignments

1. **Create the Table**
   - From App Home, click **"Add table"**
   - Select **"Create a blank table"**
   - **Table name:** "Project Team Assignments"
   - **Single record name:** "Project Team Assignment"
   - **Plural record name:** "Project Team Assignments"
   - Click **"Create table"**

2. **Configure Fields**

   **Field 1: Assignment Date**
   - Click **"+ Add field"**
   - **Field type:** Date
   - **Field name:** "Assignment Date"
   - **Default value:** Select "Today"
   - Click **"Save"**

   **Field 2: Role on Project**
   - Click **"+ Add field"**
   - **Field type:** Text
   - **Field name:** "Role on Project"
   - **Size:** 100 characters
   - Click **"Save"**

   **Field 3: Status**
   - Click **"+ Add field"**
   - **Field type:** Multiple choice - Text
   - **Field name:** "Status"
   - **Choices:**
     ```
     Active
     Inactive
     ```
   - **Default value:** Select "Active"
   - Click **"Save"**

## Step 4: Create Table Relationships

**IMPORTANT:** Create relationships in this exact order to avoid dependency issues.

### Relationship 1: Team Assignments → Team Members

1. **Navigate to Team Assignments Table**
   - From App Home, click on **"Team Assignments"** table
   - Click **"Settings"** > **"Table"** > **"Fields"**

2. **Add Relationship Field**
   - Click **"+ Add field"**
   - **Field type:** Select **"Relationship"**
   - **Field name:** "Team Member"
   - **Table to connect to:** Select "Team Members"
   - **Relationship type:** Select "Reference" (Many Team Assignments to One Team Member)
   - **Display field:** Select "Member Name" from dropdown
   - Click **"Save"**

### Relationship 2: Team Assignments → Teams

1. **Still in Team Assignments Table**
   - Click **"+ Add field"**
   - **Field type:** Select **"Relationship"**
   - **Field name:** "Team"
   - **Table to connect to:** Select "Teams"
   - **Relationship type:** Select "Reference" (Many Team Assignments to One Team)
   - **Display field:** Select "Team Name" from dropdown
   - Click **"Save"**

### Relationship 3: Project Team Assignments → Team Members

1. **Navigate to Project Team Assignments Table**
   - From App Home, click on **"Project Team Assignments"** table
   - Click **"Settings"** > **"Table"** > **"Fields"**

2. **Add Relationship Field**
   - Click **"+ Add field"**
   - **Field type:** Select **"Relationship"**
   - **Field name:** "Team Member"
   - **Table to connect to:** Select "Team Members"
   - **Relationship type:** Select "Reference" (Many Project Team Assignments to One Team Member)
   - **Display field:** Select "Member Name" from dropdown
   - Click **"Save"**

### Relationship 4: Project Team Assignments → Projects

1. **Still in Project Team Assignments Table**
   - Click **"+ Add field"**
   - **Field type:** Select **"Relationship"**
   - **Field name:** "Project"
   - **Table to connect to:** Select "Projects"
   - **Relationship type:** Select "Reference" (Many Project Team Assignments to One Project)
   - **Display field:** Select "Project Title" from dropdown
   - Click **"Save"**

### Relationship 5: Projects → Teams (Primary Team Assignment)

1. **Navigate to Projects Table**
   - From App Home, click on **"Projects"** table
   - Click **"Settings"** > **"Table"** > **"Fields"**

2. **Add Relationship Field**
   - Click **"+ Add field"**
   - **Field type:** Select **"Relationship"**
   - **Field name:** "Assigned Team"
   - **Table to connect to:** Select "Teams"
   - **Relationship type:** Select "Reference" (Many Projects to One Team)
   - **Display field:** Select "Team Name" from dropdown
   - Click **"Save"**

### Relationship 6: Key Milestones → Projects

1. **Navigate to Key Milestones Table**
   - From App Home, click on **"Key Milestones"** table
   - Click **"Settings"** > **"Table-to-table relationships"**

2. **Create Relationship**
   - Click **"+ New relationship"**
   - **Select table to connect to:** Choose "Projects"
   - **Relationship type:** Many Key Milestones belong to One Project
   - **Reference field name:** "Related Project"
   - Click **"Next"**
   - **Add lookup fields** (optional):
     - Project Title
   - Click **"Save"**

### Relationship 6.5: Key Milestones → Tasks (Optional - for Task-Linked Milestones)

**Note:** If this relationship already exists from the initial table setup, skip to step 2.

1. **Create the relationship (if not already existing)**
   - In Key Milestones Table, go to **"Settings"** > **"Table-to-table relationships"**
   - Click **"+ New relationship"**
   - **Select table to connect to:** Choose "Tasks"
   - **Relationship type:** Many Key Milestones belong to One Task
   - Click **"Create"**
   - The system will create a reference field (may be named "Task" or "Related Task")
   
2. **Add or verify lookup fields**:
   - If relationship already exists, click on it to edit
   - Click **"Add lookup fields"** (or verify these are already added):
     - **Task Name**
     - **Status** (not "Project - Status" - you want the task's status directly)
     - **Due Date** (for automatic target date calculation)
   - Click **"Done"**

3. **Configure the Related Task field filtering**:
   - Go to **"Settings"** > **"Fields"**
   - Find the **"Related Task"** field (or whatever your reference field is named)
   - Click to edit it
   - In the field properties, set up the filter:
     - **Show choices where:** 'Key Milestones: Related Project' = Tasks Table: Related Project
   - This ensures users only see tasks from the selected project when creating milestones
   - Click **"Save"**
   - Note: This field is optional - leave blank for general milestones not tied to specific tasks

4. **Add Formula Field for Automatic Status**
   - In **"Settings"** > **"Fields"**
   - Click **"+ Add field"**
   - **Field type:** Select **"Formula"**
   - **Field name:** "Auto Status"
   - **Formula return type:** Select "Text"
   - **Formula:** Enter:
     ```
     If([Task - Status]="Complete", "Complete", [Status])
     ```
   - Click **"Save"**
   - This formula checks if the related task is complete and updates the milestone status accordingly
   - Note: The lookup field name might be "Task - Status" or "Related Task - Status" depending on how you named the reference field

5. **Add Formula Field for Calculated Target Date**
   - Click **"+ Add field"**
   - **Field type:** Select **"Formula"**
   - **Field name:** "Calculated Target Date"
   - **Formula return type:** Select "Date"
   - **Formula:** Enter:
     ```
     If(IsNull([Related Task]), [Target Date], [Task - Due Date])
     ```
   - Click **"Save"**
   - This formula uses the task's due date if a task is linked, otherwise uses the manually entered target date

6. **Update Milestone Reports and Forms**
   - When creating forms, include the "Related Task" field as optional
   - In reports:
     - Show "Auto Status" instead of "Status" to reflect task-driven updates
     - Show "Calculated Target Date" instead of "Target Date" for consistent dates
   - The manual Status and Target Date fields remain available for milestones not linked to tasks

**Future Enhancement with Pipelines:**
When you have access to Pipelines, you can create automation that:
- When a Task status changes to "Complete"
- Find all milestones where Related Task equals that task
- Update the milestone Status field to "Complete"
This would eliminate the need for the formula field approach.

### Relationship 7: Tasks → Projects

1. **Navigate to Tasks Table**
   - From App Home, click on **"Tasks"** table
   - Click **"Settings"** > **"Table"** > **"Fields"**

2. **Add Relationship Field**
   - Click **"+ Add field"**
   - **Field type:** Select **"Relationship"**
   - **Field name:** "Project"
   - **Table to connect to:** Select "Projects"
   - **Relationship type:** Select "Reference" (Many Tasks to One Project)
   - **Display field:** Select "Project Title" from dropdown
   - Click **"Save"**

### Relationship 8: Tasks → Team Members (Assigned To)

1. **Still in Tasks Table**
   - Click **"+ Add field"**
   - **Field type:** Select **"Relationship"**
   - **Field name:** "Assigned To"
   - **Table to connect to:** Select "Team Members"
   - **Relationship type:** Select "Reference" (Many Tasks to One Team Member)
   - **Display field:** Select "Member Name" from dropdown
   - Click **"Save"**

2. **Add Lookup Fields Through This Relationship**
   - Navigate to **Settings** > **"Table-to-table relationships"**
   - Click on the **Tasks → Team Members** relationship you just created
   - Click **"Add Lookup Field"**
   - **Field to lookup:** Email
   - **Field label:** "Assigned Member Email"
   - Click **"Create"**
   
   - Click **"Add Lookup Field"** again
   - **Field to lookup:** Navigate to find Team Manager field (may need to go through Team Assignments → Team → Team Manager)
   - **Field label:** "Assigned To Team Manager"
   - Click **"Create"**
   - Click **"Done"** to close the relationship configuration

### Relationship 9: Tasks → Tasks (Dependencies)

1. **Still in Tasks Table**
   - Click **"+ Add field"**
   - **Field type:** Select **"Relationship"**
   - **Field name:** "Depends On"
   - **Table to connect to:** Select "Tasks"
   - **Relationship type:** Select "Reference" (Many Tasks to One Task)
   - **Display field:** Select "Task Name" from dropdown
   - **Field label:** "Depends On"
   - Click **"Save"**

## Step 5: Create Lookup Fields

### In Projects Table - Add Team Manager Lookup

1. **Navigate to Projects Table**
   - From App Home, click on **"Projects"** table
   - Click **"Settings"** > **"Table"** > **"Fields"**

2. **Add Team Manager Lookup**
   - Click **"+ Add field"**
   - **Field type:** Select **"Lookup"**
   - **Field name:** "Team Manager"
   - **Look up from:** Select "Assigned Team" (the relationship field we created)
   - **Field to look up:** Select "Team Manager"
   - Click **"Save"**

### In Tasks Table - Add Project Status Lookup

1. **Navigate to Tasks Table Relationships**
   - From App Home, click on **"Tasks"** table
   - Click **"Settings"** > **"Table-to-table relationships"**

2. **Add Project Status Lookup**
   - Click on the **Tasks → Projects** relationship
   - Click **"Add Lookup Field"**
   - **Field to lookup:** Status
   - **Field label:** "Project Status"
   - Click **"Create"**
   - Click **"Done"**

### In Project Team Assignments Table - Add Team Name Lookup

1. **Navigate to Project Team Assignments Table Relationships**
   - From App Home, click on **"Project Team Assignments"** table
   - Click **"Settings"** > **"Table-to-table relationships"**

2. **Add Team Name from Project**
   - Click on the **Project Team Assignments → Projects** relationship
   - Click **"Add Lookup Field"**
   - Navigate to **"Related Team"** > **"Team Name"**
   - **Field label:** "Project Team Name"
   - Click **"Create"**
   - Click **"Done"**
   - This displays which team the project is assigned to in your Project Team Assignments table

## Step 6: Create Summary/Formula Fields

### In Projects Table - Create Summary Fields Through Relationships

**IMPORTANT:** Summary fields must be created through the table-to-table relationship interface, not directly in the table fields.

1. **Navigate to Projects Table Relationships**
   - From App Home, click on **"Projects"** table
   - Click **"Settings"** > **"Table-to-table relationships"**

2. **Select the Projects-Tasks Relationship**
   - Click on the relationship between Projects and Tasks
   - The relationship properties page opens

3. **Add Total Tasks Summary Field**
   - Under **Parent Table** (Projects) section, click **"Add Summary Field"**
   - **Summary type:** Select **"Count"**
   - **Field to summarize:** Select **"Record ID#"**
   - **Matching Criteria:** Leave empty (to count all tasks)
   - **Field name:** "Total Tasks"
   - Click **"Create"**

4. **Add Completed Tasks Summary Field**
   - Still in the same relationship, click **"Add Summary Field"** again
   - **Summary type:** Select **"Count"**
   - **Field to summarize:** Select **"Record ID#"**
   - **Matching Criteria:** Click to add criteria:
     - **Field:** Status
     - **Operator:** equals
     - **Value:** Complete
   - **Field name:** "Completed Tasks"
   - Click **"Create"**

### In Projects Table - Create Formula Fields

5. **Navigate to Projects Table Fields**
   - From App Home, click on **"Projects"** table
   - Click **"Settings"** > **"Table"** > **"Fields"**

6. **Add Completion Percentage Formula Field**
   - Click **"+ Add field"**
   - **Field type:** Select **"Numeric"** (from Formula section)
   - **Field name:** "Completion Percentage"
   - **Formula:** Enter:
     ```
     If([Total Tasks] > 0, [Completed Tasks] / [Total Tasks] * 100, 0)
     ```
   - Click **"Save"**

7. **Add Days Until Due Formula Field**
   - Click **"+ Add field"**
   - **Field type:** Select **"Numeric"** (from Formula section)
   - **Field name:** "Days Until Due"
   - **Formula:** Enter:
     ```
     If(IsNull([Estimated Completion Date]), null, [Estimated Completion Date] - Today())
     ```
   - Click **"Save"**

8. **Add Project Health Formula Field**
   - Click **"+ Add field"**
   - **Field type:** Select **"Text"** (from Formula section)
   - **Field name:** "Project Health"
   - **Formula:** Enter:
     ```
     If([Completion Percentage] >= 90, "On Track",
        If([Completion Percentage] >= 70, "At Risk",
           If([Completion Percentage] >= 50, "Behind",
              "Critical")))
     ```
   - Click **"Save"**

### In Teams Table - Create Summary Fields Through Relationships

1. **Navigate to Teams Table Relationships**
   - From App Home, click on **"Teams"** table
   - Click **"Settings"** > **"Table-to-table relationships"**

2. **Add Total Members Summary Field (Teams → Team Assignments)**
   - Click on the relationship between Teams and Team Assignments
   - Under **Parent Table** (Teams) section, click **"Add Summary Field"**
   - **Summary type:** Select **"Count"**
   - **Field to summarize:** Select **"Record ID#"**
   - **Matching Criteria:** Add criteria:
     - **Field:** Status
     - **Operator:** equals
     - **Value:** Active
   - **Field name:** "Total Members"
   - Click **"Create"**

3. **Add Active Projects Summary Field (Teams → Projects)**
   - Click on the relationship between Teams and Projects
   - Under **Parent Table** (Teams) section, click **"Add Summary Field"**
   - **Summary type:** Select **"Count"**
   - **Field to summarize:** Select **"Record ID#"**
   - **Matching Criteria:** Add criteria:
     - **Field:** Status
     - **Operator:** does not equal
     - **Value:** Complete
   - **Field name:** "Active Projects"
   - Click **"Create"**

### In Team Members Table - Create Summary Fields Through Relationships

1. **Navigate to Team Members Table Relationships**
   - From App Home, click on **"Team Members"** table
   - Click **"Settings"** > **"Table-to-table relationships"**

2. **Add Active Tasks Summary Field (Team Members → Tasks)**
   - Click on the relationship between Team Members and Tasks
   - Under **Parent Table** (Team Members) section, click **"Add Summary Field"**
   - **Summary type:** Select **"Count"**
   - **Field to summarize:** Select **"Record ID#"**
   - **Matching Criteria:** Add criteria:
     - **Field:** Status
     - **Operator:** does not equal
     - **Value:** Complete
   - **Field name:** "Active Tasks"
   - Click **"Create"**

3. **Add Completed Tasks Summary Field**
   - Still in the same relationship, click **"Add Summary Field"** again
   - **Summary type:** Select **"Count"**
   - **Field to summarize:** Select **"Record ID#"**
   - **Matching Criteria:** Add criteria:
     - **Field:** Status
     - **Operator:** equals
     - **Value:** Complete
   - **Field name:** "Completed Tasks"
   - Click **"Create"**

### In Team Members Table - Create Formula Fields

4. **Navigate to Team Members Table Fields**
   - From App Home, click on **"Team Members"** table
   - Click **"Settings"** > **"Table"** > **"Fields"**

5. **Add Task Completion Rate Formula Field**
   - Click **"+ Add field"**
   - **Field type:** Select **"Numeric"** (from Formula section)
   - **Field name:** "Task Completion Rate"
   - **Formula:** Enter:
     ```
     If(([Active Tasks] + [Completed Tasks]) > 0, 
        [Completed Tasks] / ([Active Tasks] + [Completed Tasks]) * 100, 0)
     ```
   - Click **"Save"**

## Step 7: Create Forms

### Project Entry Form

1. **Navigate to Projects Table**
   - From App Home, click on **"Projects"** table
   - Click **"Forms"** tab at the top

2. **Create New Form**
   - Click **"+ New form"**
   - **Form name:** "Project Entry Form"
   - **Form type:** Select "Add"
   - Click **"Create form"**

3. **Configure Form Layout**
   - **Drag and arrange fields** in this order:
     - Project Title
     - Description
     - Requirements
     - Edge Cases
     - Estimated Completion Date
     - Status
     - Priority
     - Budget
     - Assigned Team
   - **Remove fields** not needed for initial entry:
     - Actual Completion Date
     - Created Date (auto-populated)
     - Created By (auto-populated)
     - Calculated fields (Total Tasks, etc.)

4. **Set Form Properties**
   - Click **"Form properties"** (gear icon)
   - **Redirect after save:** Select "Display the record that was just added"
   - **Save button text:** "Create Project"
   - Click **"Save"**

### Task Entry Form

1. **Navigate to Tasks Table**
   - From App Home, click on **"Tasks"** table
   - Click **"Forms"** tab

2. **Create New Form**
   - Click **"+ New form"**
   - **Form name:** "Task Entry Form"
   - **Form type:** Select "Add"
   - Click **"Create form"**

3. **Configure Form Layout**
   - **Arrange fields:**
     - Task Name
     - Description
     - Project
     - Assigned To
     - Due Date
     - Estimated Hours
     - Priority
     - Status
     - Depends On
   - **Remove auto-populated fields:**
     - Created Date
     - Created By
     - Actual Hours (to be filled later)

4. **Set Form Properties**
   - Click **"Form properties"**
   - **Save button text:** "Create Task"
   - Click **"Save"**

### Team Member Form

1. **Navigate to Team Members Table**
   - From App Home, click on **"Team Members"** table
   - Click **"Forms"** tab

2. **Create New Form**
   - Click **"+ New form"**
   - **Form name:** "Team Member Form"
   - **Form type:** Select "Add"
   - Click **"Create form"**

3. **Configure Form Layout**
   - **Include all fields:**
     - Member Name
     - Email
     - User Account
     - Employee ID
     - Department
     - Job Title
     - Hire Date
     - Status

4. **Set Form Properties**
   - Click **"Form properties"**
   - **Save button text:** "Add Team Member"
   - Click **"Save"**

### Team Assignments Form

1. **Navigate to Team Assignments Table**
   - From App Home, click on **"Team Assignments"** table
   - Click **"Forms"** tab

2. **Create New Form**
   - Click **"+ New form"**
   - **Form name:** "Team Assignment Form"
   - **Form type:** Select "Add"
   - Click **"Create form"**

3. **Configure Form Layout**
   - **Include only these fields:**
     - Related Team Member
     - Related Team
     - Status
   - **Remove/hide these fields:**
     - Assignment Date
     - Role
     - Team Member - Member Name (lookup field)
     - Team Name (lookup field)
     - Team Manager (lookup field)

4. **Set Form Properties**
   - Click **"Form properties"**
   - **Save button text:** "Assign Team Member"
   - Click **"Save"**

### Project Team Assignments Form

1. **First, Clean Up Unnecessary Fields**
   - Navigate to **Project Team Assignments** table
   - Click **"Settings"** > **"Fields"**
   - Consider deleting these fields if not needed:
     - Assignment Date
     - Role on Project
     - Status

2. **Create Simplified Form**
   - Click **"Forms"** tab
   - Click **"+ New form"**
   - **Form name:** "Assign to Project Form"
   - **Form type:** Select "Add"
   - Click **"Create form"**

3. **Configure Form Layout**
   - **Include only these fields:**
     - Related Project
     - Related Team Member
   - **Remove/hide these lookup fields:**
     - Project Title (lookup)
     - Team Member - Member Name (lookup)

4. **Set as Default Form**
   - Go to Settings > Forms
   - Set "Assign to Project Form" as the default form for adding records


### THIS IS WHERE I STOPPED 8/1/25 
---------------------------------------------------
## Step 8: Create Reports

### Report 1: Project Dashboard

1. **Navigate to Projects Table**
   - From App Home, click on **"Projects"** table
   - Click **"Reports"** tab

2. **Create New Report**
   - Click **"+ New report"**
   - **Report type:** Select "Table"
   - **Report name:** "Project Dashboard"

3. **Configure Report Columns**
   - Click **"Columns"** button
   - **Add these fields** (drag from Available Fields to Selected Fields):
     - Project Title
     - Status
     - Completion Percentage
     - Days Until Due
     - Project Health
     - Team Manager
     - Total Tasks
     - Completed Tasks
   - **Remove** any fields not listed above
   - Click **"Done"**

4. **Set Sorting and Grouping**
   - In the **Sorting & Grouping** section, select **"Sort and group from high to low by"**
   - In the dropdown that appears, select **"Status"**
   - For **"Grouping by"**, select **"Equal values"**
   - Leave the checkboxes unchecked:
     - [ ] Show summary table based on the grouped columns
     - [ ] Hide main table and show only summary table
   - Note: This will group projects by their status while still showing all project details

6. **Save Report**
   - Click **"Save"**

### Report 2: Team Workload Report

1. **Navigate to Team Members Table**
   - From App Home, click on **"Team Members"** table
   - Click **"Reports"** tab

2. **Create New Report**
   - Click **"+ New report"**
   - **Report type:** Select "Table"
   - **Report name:** "Team Workload Report"

3. **Configure Report**
   - **Columns to include:**
     - Member Name
     - Department
     - Active Tasks
     - Completed Tasks
     - Task Completion Rate
   - **Sort by:** Active Tasks (largest to smallest)
   - Click **"Save"**

### Report 3: Task Status Report

1. **Navigate to Tasks Table**
   - From App Home, click on **"Tasks"** table
   - Click **"Reports"** tab

2. **Create New Report**
   - Click **"+ New report"**
   - **Report type:** Select "Table"
   - **Report name:** "Task Status Report"

3. **Configure Report**
   - **Columns:**
     - Task Name
     - Related Project
     - Assigned To
     - Status
     - Priority
     - Due Date
     - Estimated Hours
     - Actual Hours
   - **Sorting & Grouping:**
     - Select **"Sort and group from low to high by"**
     - In the dropdown, select **"Status"**
     - For **"Grouping by"**, select **"Equal values"**
   - **Then sort by:**
     - Click **"Then"**
     - Select **"sort from low to high by"**
     - In the dropdown, select **"Priority"**
     - Click **"Then"** again
     - Select **"sort from low to high by"**
     - In the dropdown, select **"Due Date"**
   - Click **"Save"**

### Report 4: Milestone Tracking Report

1. **Navigate to Key Milestones Table**
   - From App Home, click on **"Key Milestones"** table
   - Click **"Reports"** tab

2. **Create New Report**
   - Click **"+ New report"**
   - **Report type:** Select "Table"
   - **Report name:** "Milestone Tracking Report"

3. **Add Calculated Field for Days Until Due**
   - First, go to **Settings > Table > Fields**
   - Click **"+ Add field"**
   - **Field type:** Select **"Formula"**
   - **Field name:** "Days Until Due"
   - **Formula return type:** Select "Numeric"
   - **Formula:** Enter:
     ```
     If(IsNull([Target Date]), null, [Target Date] - Today())
     ```
   - Click **"Save"**

4. **Configure Report**
   - **Columns:**
     - Milestone Name
     - Project
     - Target Date
     - Status
     - Priority
     - Days Until Due
   - **Sorting:**
     - Select **"Sort from low to high by"**
     - In the dropdown, select **"Target Date"**
   - Click **"Save"**



--- SKIPPING FOR NOW -----
## Step 9: Set Up Notifications

### Notification 1: Task Assignment

1. **Navigate to Tasks Table**
   - From App Home, click on **"Tasks"** table
   - Click **"Settings"** > **"Table"** > **"Notifications"**

2. **Create New Notification**
   - Click **"+ Add notification"**
   - **Notification name:** "Task Assignment Notification"
   - **When:** Select "a record is added OR a field value changes"
   - **Field that triggers:** Select "Assigned To"

3. **Configure Email Settings**
   - **Recipients:** Click **"+ Add recipient"**
     - **Type:** Field value
     - **Field:** Assigned To
   - **Subject:** Enter "New Task Assigned: [Task Name]"
   - **Message:** Enter:
     ```
     Hello [Assigned To],
     
     You have been assigned a new task:
     
     Task: [Task Name]
     Project: [Project]
     Due Date: [Due Date]
     Priority: [Priority]
     
     Description: [Description]
     
     Please log into the Project Management System to view details.
     ```
   - Click **"Save"**

### Notification 2: Project Status Change

1. **Navigate to Projects Table**
   - From App Home, click on **"Projects"** table
   - Click **"Settings"** > **"Table"** > **"Notifications"**

2. **Create New Notification**
   - Click **"+ Add notification"**
   - **Notification name:** "Project Status Change"
   - **When:** Select "a field value changes"
   - **Field that triggers:** Select "Status"

3. **Configure Recipients**
   - **Recipients:** Click **"+ Add recipient"**
     - **Type:** Field value
     - **Field:** Team Manager
   - **Subject:** "Project Status Update: [Project Title]"
   - **Message:**
     ```
     Project Status Update
     
     Project: [Project Title]
     New Status: [Status]
     Completion: [Completion Percentage]%
     
     View project details in the Project Management System.
     ```
   - Click **"Save"**


---- -SKIPPING FOR NOW -----
### Notification 3: Overdue Task Alert

1. **Navigate to Tasks Table**
   - From App Home, click on **"Tasks"** table
   - Click **"Settings"** > **"Table"** > **"Reminders"**

2. **Create New Reminder**
   - Click **"+ Add reminder"**
   - **Reminder name:** "Overdue Task Alert"
   - **When to send:** Select "Daily"
   - **Time:** Select preferred time (e.g., 9:00 AM)

3. **Set Conditions**
   - **Send when:** Click **"Add condition"**
     - **Condition 1:** Due Date is less than Today()
     - **Condition 2:** Status does not equal "Complete"
   - **Combine conditions:** Select "AND"

4. **Configure Recipients**
   - **Recipients:** Field value - "Assigned To"
   - **Subject:** "Overdue Task Alert: [Task Name]"
   - **Message:**
     ```
     Overdue Task Alert
     
     Task: [Task Name]
     Project: [Project]
     Due Date: [Due Date]
     Current Status: [Status]
     
     This task is overdue. Please update the status or due date.
     ```
   - Click **"Save"**


----- SKIPPING FOR NOW AUG 3 -----
## Step 10: Configure User Permissions

### Setting Up Roles

1. **Navigate to App Settings**
   - From App Home, click **"Settings"** > **"App"** > **"Roles"**

2. **Create Project Manager Role**
   - Click **"+ Add role"**
   - **Role name:** "Project Manager"
   - **Description:** "Full access to projects, tasks, and milestones"

3. **Set Project Manager Permissions**
   - **Projects table:** Full permissions (View, Add, Modify, Delete)
   - **Tasks table:** Full permissions
   - **Key Milestones table:** Full permissions
   - **Team Members table:** View only
   - **Teams table:** View only
   - **Team Assignments table:** View and Modify
   - **Project Team Assignments table:** Full permissions

4. **Create Team Member Role**
   - Click **"+ Add role"**
   - **Role name:** "Team Member"
   - **Description:** "Limited access focused on assigned tasks"

5. **Set Team Member Permissions**
   - **Projects table:** View only
   - **Tasks table:** 
     - View: All records
     - Modify: Only records where "Assigned To" = Current User
   - **Key Milestones table:** View only
   - **Team Members table:** View only
   - **Other tables:** View only

6. **Create Team Manager Role**
   - Click **"+ Add role"**
   - **Role name:** "Team Manager"
   - **Description:** "Manage team and team projects"

7. **Set Team Manager Permissions**
   - **Teams table:** Modify only teams where "Team Manager" = Current User
   - **Team Members table:** View all, modify team assignments
   - **Projects table:** View and modify projects assigned to their teams
   - **Tasks table:** View and modify tasks for their team members
   - **Other tables:** View only

### Assigning Users to Roles

1. **Navigate to Users**
   - From App Settings, click **"Users"**

2. **Add Users and Assign Roles**
   - Click **"+ Add user"**
   - Enter email address
   - Select appropriate role from dropdown
   - Click **"Send invitation"**

## Step 11: Create Dashboards

### Executive Dashboard

1. **First, Create the Chart Reports**

   **Chart 1: Project Status Overview**
   - Navigate to **Projects** table
   - Click **"Reports"** tab
   - Click **"+ New report"**
   - Select **"Chart"** as report type
   - **Report name:** "Project Status Overview"
   - **Chart type:** Pie chart
   - **Series:** Status
   - **Series grouping:** Equal values
   - **Data values:** # of Projects
   - **Sorting:**
     - Sort by: Values - # of Projects
     - Direction: High to low (shows largest slices first)
   - Click **"Save"**

   **Chart 2: Team Workload Distribution**
   - Navigate to **Team Members** table
   - Click **"Reports"** tab
   - Click **"+ New report"**
   - Select **"Chart"** as report type
   - **Report name:** "Team Workload Distribution"
   - **Chart type:** Bar chart
   - **X-axis:** Member Name (Equal values)
   - **Y-axis:** Active Tasks (summed)
   - **Sorting:**
     - Sort by: Values - Active Tasks (summed)
     - Direction: High to low (shows busiest team members first)
   - Click **"Save"**

   **Report 3: Critical Projects**
   - Navigate to **Projects** table
   - Click **"Reports"** tab
   - Click **"+ New report"**
   - Select **"Table"** as report type
   - **Report name:** "Critical Projects Requiring Attention"
   - **Columns to include:**
     - Project Title
     - Status
     - Completion Percentage
     - Days Until Due
     - Team Manager
     - Budget
     - Total Tasks
     - Completed Tasks
   - **Filter:**
     - Click **"Filters"**
     - Add filter: Project Health equals "Critical"
     - Note: Type "Critical" in the text field
   - Click **"Save"**

2. **Create the Dashboard**
   - From App Home, click **"+ Add page"**
   - Select **"Dashboard"**
   - **Page name:** "Executive Dashboard"

3. **Add Charts and Reports to Dashboard**
   - Click **"Add Widget"** > **"Report"**
   - Select **"Projects"** > **"Project Status Overview"**
   - Position on dashboard
   
   - Click **"Add Widget"** > **"Report"**
   - Select **"Team Members"** > **"Team Workload Distribution"**
   - Position on dashboard
   
   - Click **"Add Widget"** > **"Report"**
   - Select **"Projects"** > **"Critical Projects Requiring Attention"**
   - Position on dashboard

### Team Manager Dashboard

1. **First, Create the Reports**

   **Report 1: My Team Members Workload**
   - First, add lookup fields to Team Assignments table:
     - Navigate to **Team Assignments** table
     - Click **"Settings"** > **"Table-to-table relationships"**
     
     - Click on **Team Assignments → Team Members** relationship
     - Add lookup fields:
       - Active Tasks
       - Completed Tasks
       - Task Completion Rate
     - Click **"Done"**
     
     - Click on **Team Assignments → Teams** relationship
     - Add lookup field:
       - Team Manager
     - Click **"Done"**
   
   - Create the report:
     - Navigate to **Team Assignments** table
     - Click **"Reports"** tab
     - Click **"+ New report"**
     - Select **"Table"** as report type
     - **Report name:** "My Team Members Workload"
     - **Columns to include:**
       - Related Team Member (or Team Member name)
       - Related Team
       - Role
       - Active Tasks
       - Completed Tasks
       - Task Completion Rate
     - **Filter:**
       - Click **"Filters"** > **"Add a filter"**
       - First filter:
         - Field: **"Team - Team Manager"** (the lookup field we created)
         - Operator: **"equals"**
         - Value: **"the current user"**
         - Note: If "the current user" option doesn't appear, the Team Manager field in the Teams table needs to be a User type field, not Text
       - Add second filter:
         - Field: **"Status"**
         - Operator: **"equals"**
         - Value: **"Active"**
     - **Grouping and Sorting:**
       - Click **"Sort & group"** dropdown
       - Select **"Sort and group from low to high by"** > **"Related Team"**
       - For **"Grouping by"**, select **"Equal values"**
       - Click **"then"**
       - Select **"sort from high to low by"** > **"Team Member - Active Tasks"**
       - This groups team members by their team alphabetically and shows busiest members first within each group
     - Click **"Save"**

## Step 13: Task Dependencies (Relies Upon Functionality)

### Overview
This feature allows tasks to depend on other tasks, creating a workflow where some tasks cannot start until prerequisite tasks are complete.

### Setup Task Dependencies

**Note:** This assumes you already have a self-referencing Tasks → Tasks relationship.

1. **Add Lookup Fields to Existing Relationship**
   - Go to **Tasks** table > **Settings** > **Table-to-table relationships**
   - Find the **Tasks → Tasks** relationship (self-referencing)
   - Click to edit it
   - Click **"Add lookup fields"**
   - Select these fields:
     - **Status** (creates "Relies Upon - Status")
     - **Due Date** (creates "Relies Upon - Due Date")
     - **Related Project** (creates "Relies Upon - Related Project")
   - The existing lookup should already include "Task Name"

2. **Add Conditional Filtering to Relies Upon Field**
   - Go to **Settings** > **Fields**
   - Edit the **"Relies Upon"** field (the numeric reference field)
   - Check **"The values in this field depend on a selection in another field"**
   - **Parent field:** Related Project
   - **Show choices where:** Tasks Table: Related Project = Tasks Table: Related Project
   - This ensures users only see tasks from the same project

3. **Add Formula Fields**
   
   **Can Start Status:**
   - Field type: **Formula**
   - Name: **"Can Start"**
   - Return type: **Text**
   - Formula: `If([Status]="Complete", "Complete", If([Relies Upon]=0, "Yes", If([Relies Upon - Status]="Complete", "Ready", "Blocked")))`
   - Note: Quickbase stores 0 (not null) in empty reference fields
   
   **Is Blocking Others Indicator:**
   - Field type: **Formula**
   - Name: **"Is Blocking Others"**
   - Return type: **Text**
   - **Option 1 - Using Summary Field:**
     - First create a summary field on the parent side of the Tasks → Tasks relationship to count dependent tasks
     - Formula: `If([Status]="Complete", "No", If([# of Tasks] > 0, "Yes - " & [# of Tasks] & " tasks waiting", "No"))`
   - **Option 2 - Using Formula Query (if summary field won't cooperate):**
     - Field type: **Formula - Numeric**
     - Name: **"Tasks Depending on This"**
     - Formula: `Size(GetRecords("{17.EX." & [Record ID#] & "}", "your_tasks_table_dbid"))`
     - Note: Replace 17 with your Relies Upon field ID and your_tasks_table_dbid with your actual table ID from the URL
     - Then create Is Blocking Others as: `If([Status]="Complete", "No", If([Tasks Depending on This] > 0, "Yes - " & [Tasks Depending on This] & " tasks waiting", "No"))`
   - Note: Completed tasks show "No" regardless of dependencies since they're no longer blocking

4. **Create Task Status Report**
   - Navigate to **Tasks** table
   - Click **"Reports"** tab
   - Click **"+ New report"**
   - Select **"Table"** as report type
   - **Report name:** "Task Status Report"
   - **Columns to include:**
     - Task Name
     - Related Project (or Project Title)
     - Assigned To (or Member Name)
     - Due Date
     - Priority
     - Status
     - Relies Upon - Task Name
     - Can Start
     - Is Blocking Others
   - **Sorting:**
     - Sort from high to low by Priority
     - Then sort from low to high by Due Date
   - Click **"Save"**

5. **Update Task Forms**
   - Add **"Relies Upon"** field to task creation/edit forms
   - Add **"Can Start"** field to show blocking status
   - The conditional filtering will automatically show only tasks from the same project

### Benefits
- Visual indication of task dependencies
- Users can see which tasks are blocked vs ready to start
- Identify critical path tasks that are blocking others
- Better project workflow management

### ============ THIS IS WHERE I STOPPED - AUGUST 4, 2025 ============

   **Chart 1: Team Project Status**
   - Navigate to **Projects** table
   - Click **"Reports"** tab
   - Click **"+ New report"**
   - Select **"Chart"** as report type
   - **Report name:** "Team Project Status"
   - **Chart type:** Bar chart (stacked)
   - **X-axis:** Related Team (Equal values)
   - **Y-axis:** # of Projects
   - **Series:** Status
   - **Filter:**
     - Add filter: Team Manager equals Current User
   - Click **"Save"**

   **Report 2: Upcoming Deadlines**
   - Navigate to **Tasks** table
   - Click **"Reports"** tab
   - Click **"+ New report"**
   - Select **"Table"** as report type
   - **Report name:** "Upcoming Deadlines"
   - **Columns:**
     - Task Name
     - Related Project
     - Assigned To
     - Due Date
     - Priority
     - Status
   - **Filter:**
     - Due Date is during the next 7 days
     - AND Status does not equal "Complete"
   - **Sorting:**
     - Sort by Due Date (low to high)
   - Click **"Save"**

2. **Create the Dashboard**
   - From App Home, click **"+ Add page"**
   - Select **"Dashboard"**
   - **Page name:** "Team Manager Dashboard"

3. **Add Reports to Dashboard**
   - Click **"Add Widget"** > **"Report"**
   - Select **"Team Assignments"** > **"My Team Members Workload"**
   - Position on dashboard
   
   - Click **"Add Widget"** > **"Report"**
   - Select **"Projects"** > **"Team Project Status"**
   - Position on dashboard
   
   - Click **"Add Widget"** > **"Report"**
   - Select **"Tasks"** > **"Upcoming Deadlines"**
   - Position on dashboard

### Individual Dashboard

1. **First, Set Up User Account Fields**

   **Add User Account field to Team Members table:**
   - Navigate to **Team Members** table
   - Click **"Settings"** (gear icon)
   - Click **"Fields"**
   - Click **"+ New field"**
   - **Field label:** "User Account"
   - **Field type:** Select **"User"**
   - Click **"Add"**
   - Note: You'll need to populate this field with the corresponding Quickbase user for each team member

   **Add lookup field to Tasks table:**
   - Navigate to **Tasks** table
   - Click **"Settings"** > **"Table-to-table relationships"**
   - Find the **Tasks → Team Members** relationship (using Assigned To field)
   - Click on the relationship
   - In the **"Add lookup fields"** section:
     - Find and select **"User Account"**
     - Click **"Add Lookup Field"**
   - Click **"Done"**
   - This creates a field called "Assigned To - User Account" in the Tasks table

2. **Create the Personal Reports**

   **Report 1: My Tasks**
   - Navigate to **Tasks** table
   - Click **"Reports"** tab
   - Click **"+ New report"**
   - Select **"Table"** as report type
   - **Report name:** "My Tasks"
   - **Columns to include:**
     - Task Name
     - Related Project
     - Due Date
     - Priority
     - Status
   - **Filter:**
     - Click **"Filters"** > **"Add a filter"**
     - Field: **"Assigned To - User Account"** (the lookup field we created)
     - Operator: **"equals"**
     - Value: **"the current user"**
   - **Sorting:**
     - Click **"Sort & group"** dropdown
     - Select **"Sort from low to high by"** > **"Due Date"**
   - Click **"Save"**

   **Report 2: My Completion Metrics**
   - First, create a formula field in Tasks table:
     - Navigate to **Tasks** table
     - Click **"Settings"** > **"Fields"**
     - Click **"+ New field"**
     - **Field label:** "Is Complete"
     - **Field type:** Select **"Formula - Numeric"**
     - **Formula:** `If([Status]="Complete",1,0)`
     - Click **"Add"**
   
   - Now create the report:
     - Navigate to **Tasks** table
     - Click **"Reports"** tab
     - Click **"+ New report"**
     - Select **"Summary"** as report type
     - **Report name:** "My Completion Metrics"
     - **Summarize Data section:**
       - In **"Summarize"** dropdown, select **"# of Tasks"**
       - For **"Display as"**, select **"Normal value"**
       - Rename this column to **"Total Tasks"**
       - Click **"+ Add"** to add another summary
       - In **"Summarize"** dropdown, select **"Is Complete"** (the formula field)
       - For **"Summarize by"**, select **"Totals"**
       - For **"Display as"**, select **"Normal value"**
       - Rename this column to **"Completed Tasks"**
     - **Grouping and crosstabs section:**
       - In **"Rows"**, click **"Group by"** and select **"Assigned To"**
       - For **"Combine"**, select **"Equal values"**
       - Leave **"Crosstabs"** as **"Don't group columns"**
     - **Sorting section:**
       - Leave as **"Default order"**
   - **Filter:**
     - Click **"Filters"** > **"Add a filter"**
     - Field: **"Assigned To - User Account"** (the lookup field we created)
     - Operator: **"equals"**
     - Value: **"the current user"**
   - Click **"Save"**

2. **Create Dashboard**
   - Click **"+ Add page"** > **"Dashboard"**
   - **Page name:** "My Dashboard"

3. **Add Personal Reports to Dashboard**
   - Click **"Add Widget"** > **"Report"**
   - Select **"Tasks"** > **"My Tasks"**
   - Position on dashboard
   
   - Click **"Add Widget"** > **"Report"**
   - Select **"Tasks"** > **"My Completion Metrics"**
   - Position on dashboard

## Step 11: Managing Team and Project Assignments

### Team Assignments (Manual Process)

Currently, team assignments are managed manually. When you need to assign a team member to a team:

1. Navigate to **Team Assignments** table
2. Click **"New Team Assignment"**
3. Select the **Team Member** and **Team**
4. Set **Status** to "Active"
5. Click **"Save"**

**Future Enhancement with Pipelines:**
This process could be automated when new team members are added. A pipeline could automatically create team assignments based on department or other criteria.

### Project Team Assignments (Manual Process)

When a project is assigned to a team, you need to manually create Project Team Assignments to track which team members are working on that project:

1. Create or edit a **Project** and assign it to a **Team**
2. Navigate to **Project Team Assignments** table
3. For each active team member on that team:
   - Click **"New Project Team Assignment"**
   - Select the **Project**
   - Select the **Team Member**
   - Click **"Save"**

**Automation with Pipelines:**

When you have access to Pipelines, you can automate this process. Here's how to implement it:

### Pipeline: Auto-assign Team Members to Projects

#### Step 1: Create New Pipeline

1. **Navigate to Pipelines**
   - From App Home, click **"Settings"** > **"Pipelines"**
   - Click **"+ New Pipeline"**
   - **Name:** "Auto-assign Team Members to Projects"
   - **Description:** "When a project is assigned to a team, automatically add all team members"
   - Click **"Create"**

#### Step 2: Configure Trigger

1. **Set up Trigger**
   - In Step A, click **"Select a trigger"**
   - Choose **"Quickbase"** > **"New Event"**
   - **Table:** Select **"Projects"**
   - **Fields:** Select **"Related Team"** (or "Assigned Team")
   - **Trigger on any field:** No
   - **Trigger on Any of These Specific Fields:** Select **"Related Team"**
   - **On add record:** Yes
   - **On modify record:** Yes
   - **On delete record:** No

#### Step 3: Add Search for Team Members

1. **Add Step B - Search Records**
   - Click **"+"** to add new step
   - Choose **"Quickbase"** > **"Search Records"**
   - **Table:** Select **"Team Assignments"**
   - **Add Filters:**
     - Filter 1: **"Related Team"** equals {{a.related_team}}
     - Filter 2: **"Status"** equals "Active"

#### Step 4: Add Loop to Create Assignments

1. **Add Step C - For Each Loop**
   - Click **"+"** to add new step
   - Choose **"Loops"** > **"For Each"**
   - **Loop through:** Team Assignments (automatically selected)

2. **Add Step D - Create Records (inside loop)**
   - Click **"+"** inside the loop
   - Choose **"Quickbase"** > **"Create Record"**
   - **Table:** Select **"Project Team Assignments"**
   - **Field mappings:**
     - **Related Project:** Select from trigger (On New Event > Record ID)
     - **Related Team Member:** Select from loop (Search Records > Team Member > Record ID#)
     - **Assignment Date:** Type "Today"
     - **Status:** Type "Active"

#### Step 5: Activate and Test

1. **Save and Activate**
   - Save the pipeline
   - Toggle to **"Active"**

2. **Test the Pipeline**
   - Create a test project with a team assigned
   - Check Project Team Assignments table for automatic records
   - Review pipeline activity log for any errors

This automation ensures that whenever a project is assigned to a team, all active members of that team are automatically linked to the project.

## Step 12: Testing and Validation

### Creating Test Data

1. **Add Sample Team Members**
   - Navigate to Team Members table
   - Click **"+ New Team Member"**
   - Create 5-10 sample team members with different departments

2. **Create Test Teams**
   - Navigate to Teams table
   - Create 2-3 sample teams
   - Assign managers from the team members you created

3. **Add Team Assignments**
   - Navigate to Team Assignments table
   - Assign team members to teams

4. **Create Sample Projects**
   - Navigate to Projects table
   - Create 3-5 test projects with different statuses
   - Assign to different teams

5. **Add Tasks and Milestones**
   - Create various tasks assigned to different team members
   - Add milestones for each project

### Testing Workflows

1. **Test Task Assignment**
   - Create a new task and assign it to a team member
   - Verify the notification email is sent
   - Check that the team member can see the task

2. **Test Project Status Changes**
   - Change a project status
   - Verify notifications are sent to team managers
   - Check that completion percentages update correctly

3. **Verify Calculations**
   - Add tasks to projects and mark some as complete
   - Check that completion percentages calculate correctly
   - Verify summary fields update properly

## Step 13: Go-Live Preparation

### Final Checklist

- [ ] All tables created with proper fields
- [ ] All relationships established and working
- [ ] Summary and formula fields calculating correctly
- [ ] Forms created and tested
- [ ] Reports showing accurate data
- [ ] Notifications working properly
- [ ] User roles and permissions configured
- [ ] Dashboards created and populated
- [ ] Test data validates all functionality

### User Training Materials

1. **Create User Guides**
   - Document how to add new projects
   - Explain task assignment process
   - Show how to update task status
   - Demonstrate report usage

2. **Schedule Training Sessions**
   - Plan training for each user role
   - Create hands-on exercises
   - Prepare FAQ documentation

This comprehensive guide provides detailed UI navigation steps for implementing a complete project management system in Quickbase. Each step includes specific clicks and field configurations to ensure successful implementation.