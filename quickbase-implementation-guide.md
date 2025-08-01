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
   - Click **"Settings"** > **"Table"** > **"Fields"**

2. **Add Relationship Field**
   - Click **"+ Add field"**
   - **Field type:** Select **"Relationship"**
   - **Field name:** "Project"
   - **Table to connect to:** Select "Projects"
   - **Relationship type:** Select "Reference" (Many Milestones to One Project)
   - **Display field:** Select "Project Title" from dropdown
   - Click **"Save"**

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

1. **Navigate to Tasks Table**
   - From App Home, click on **"Tasks"** table
   - Click **"Settings"** > **"Table"** > **"Fields"**

2. **Add Project Status Lookup**
   - Click **"+ Add field"**
   - **Field type:** Select **"Lookup"**
   - **Field name:** "Project Status"
   - **Look up from:** Select "Project" (the relationship field)
   - **Field to look up:** Select "Status"
   - Click **"Save"**

3. **Add Assigned Member Email Lookup**
   - Click **"+ Add field"**
   - **Field type:** Select **"Lookup"**
   - **Field name:** "Assigned Member Email"
   - **Look up from:** Select "Assigned To" (the relationship field)
   - **Field to look up:** Select "Email"
   - Click **"Save"**

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
   - **Summary type:** Select **"Total"**
   - **Field to summarize:** Select **"Record ID#"**
   - **Matching Criteria:** Leave empty (to count all tasks)
   - **Field name:** "Total Tasks"
   - Click **"Create"**

4. **Add Completed Tasks Summary Field**
   - Still in the same relationship, click **"Add Summary Field"** again
   - **Summary type:** Select **"Total"**
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
   - **Summary type:** Select **"Total"**
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
   - **Summary type:** Select **"Total"**
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
   - **Summary type:** Select **"Total"**
   - **Field to summarize:** Select **"Record ID#"**
   - **Matching Criteria:** Add criteria:
     - **Field:** Status
     - **Operator:** does not equal
     - **Value:** Complete
   - **Field name:** "Active Tasks"
   - Click **"Create"**

3. **Add Completed Tasks Summary Field**
   - Still in the same relationship, click **"Add Summary Field"** again
   - **Summary type:** Select **"Total"**
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
     - Employee ID
     - Department
     - Job Title
     - Hire Date
     - Status

4. **Set Form Properties**
   - Click **"Form properties"**
   - **Save button text:** "Add Team Member"
   - Click **"Save"**


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

4. **Set Grouping**
   - Click **"Group & summarize"**
   - **Group by:** Select "Status"
   - Click **"Done"**

5. **Set Sorting**
   - Click **"Sort"**
   - **Primary sort:** Project Health (A to Z - this will show Critical first)
   - **Secondary sort:** Days Until Due (smallest to largest)
   - Click **"Done"**

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
     - Project
     - Assigned To
     - Status
     - Priority
     - Due Date
     - Estimated Hours
     - Actual Hours
   - **Group by:** Status
   - **Sort by:** Priority (A to Z), then Due Date (oldest first)
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
   - **Sort by:** Target Date (oldest first)
   - Click **"Save"**

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

1. **Create New Dashboard**
   - From App Home, click **"+ Add page"**
   - Select **"Dashboard"**
   - **Page name:** "Executive Dashboard"

2. **Add Charts and Reports**
   - **Chart 1: Project Status Overview**
     - Click **"+ Add element"** > **"Chart"**
     - **Table:** Projects
     - **Chart type:** Pie chart
     - **Grouping:** Status
     - **Title:** "Project Status Overview"
   
   - **Chart 2: Team Workload**
     - Click **"+ Add element"** > **"Chart"**
     - **Table:** Team Members
     - **Chart type:** Bar chart
     - **X-axis:** Member Name
     - **Y-axis:** Active Tasks
     - **Title:** "Team Workload Distribution"
   
   - **Report: Critical Projects**
     - Click **"+ Add element"** > **"Report"**
     - **Table:** Projects
     - **Filter:** Project Health = "Critical"
     - **Title:** "Critical Projects Requiring Attention"

### Team Manager Dashboard

1. **Create Dashboard**
   - Click **"+ Add page"** > **"Dashboard"**
   - **Page name:** "Team Manager Dashboard"

2. **Add Elements**
   - **My Team Tasks Report**
   - **Team Project Status Chart**
   - **Upcoming Deadlines Report**

### Individual Dashboard

1. **Create Dashboard**
   - Click **"+ Add page"** > **"Dashboard"**
   - **Page name:** "My Dashboard"

2. **Add Personal Elements**
   - **My Tasks Report** (filtered by Current User)
   - **My Projects Report**
   - **My Completion Metrics**

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