# Quickbase Platform Structure & Reference Guide

## Table of Contents
1. [Quickbase Core Concepts Overview](#quickbase-core-concepts-overview)
2. [Field Types Reference](#field-types-reference)
3. [Formula Functions Library](#formula-functions-library)
4. [Table Relationships Guide](#table-relationships-guide)
5. [Reports & Charts Reference](#reports--charts-reference)
6. [Forms & Rules Documentation](#forms--rules-documentation)
7. [Connected Tables & Integrations](#connected-tables--integrations)
8. [Best Practices Summary](#best-practices-summary)
9. [Common Patterns & Solutions](#common-patterns--solutions)

---

## Quickbase Core Concepts Overview

### Platform Architecture
Quickbase is a cloud-based database platform that organizes data in **tables** (similar to spreadsheets but more powerful) within **applications**. Each table contains **records** (rows) with **fields** (columns) that define the data structure.

### Key Components
- **Apps**: Containers for related tables, forms, reports, and business logic
- **Tables**: Data storage structures with fields and records
- **Fields**: Define data types, validation rules, and display properties
- **Forms**: User interfaces for data entry and editing
- **Reports**: Data visualization and analysis tools
- **Relationships**: Connections between tables for data normalization
- **Formulas**: Calculations and business logic expressions
- **Roles**: Security model defining user permissions

### Data Flow
1. **Data Entry**: Through forms or imports
2. **Data Storage**: In tables with field validation
3. **Data Processing**: Via formulas and relationships
4. **Data Output**: Through reports, charts, and exports

---

## Field Types Reference

### Basic Field Types

#### Text Fields
- **Text**: Standard text input (configurable max length)
- **Text - Multiple Choice**: Dropdown selection from predefined values
- **Multi-select Text**: Multiple selections from dropdown (stored as semicolon-delimited)
- **Email Address**: Email validation with mailto functionality
- **Phone Number**: Phone number formatting
- **URL**: Web address with link functionality

#### Numeric Fields
- **Numeric**: Standard numbers with decimal precision control
- **Numeric - Currency**: Monetary values with currency symbols
- **Numeric - Rating**: 0-5 star rating display
- **Numeric - Percent**: Percentage display format

#### Date/Time Fields
- **Date**: Date values with multiple display formats
- **Date/Time**: Date and time combinations
- **Time of Day**: Time-only values
- **Duration**: Time span calculations
- **Work Date**: Business date calculations with predecessor support

#### Special Fields
- **Checkbox**: Boolean true/false values
- **User**: Single user selection from user list
- **List-User**: Multiple user selections
- **File Attachment**: Document and file storage
- **Report Link**: Links between related tables

### Formula Field Types
Formula fields calculate values based on other fields and functions:

- **Formula - Text**: Text concatenation and manipulation
- **Formula - Numeric**: Mathematical calculations
- **Formula - Date**: Date arithmetic and formatting
- **Formula - URL**: Dynamic URL generation for workflows
- **Formula - Rich Text**: HTML formatting with CSS styling
- **Formula - Checkbox**: Conditional boolean logic

### Field Properties
All fields support common properties:
- **Label**: Display name
- **Required**: Mandatory field validation
- **Unique**: Ensure no duplicate values
- **Default Value**: Pre-populated values
- **Help Text**: User guidance
- **Permissions**: Role-based access control (View/Modify/None)

---

## Formula Functions Library

### Mathematical Functions
```
Sum([Field1], [Field2])           // Addition
[Field1] - [Field2]               // Subtraction
[Field1] * [Field2]               // Multiplication
[Field1] / [Field2]               // Division
Round([Number], [Decimal Places]) // Rounding
Abs([Number])                     // Absolute value
```

### Text Functions
```
[First Name] & " " & [Last Name]  // Concatenation
SearchAndReplace([Text], "old", "new")  // Find and replace
Length([Text Field])              // Character count
Left([Text], [Number])            // Left substring
Right([Text], [Number])           // Right substring
Upper([Text])                     // Uppercase conversion
Lower([Text])                     // Lowercase conversion
```

### Date Functions
```
Today()                           // Current date
Now()                             // Current date/time
[End Date] - [Start Date]         // Date arithmetic
Year([Date])                      // Extract year
Month([Date])                     // Extract month
Weekday([Date])                   // Day of week
Days([Number])                    // Duration in days
Hours([Number])                   // Duration in hours
```

### Conditional Functions
```
If([Condition], "True Value", "False Value")
Case([Field], 
     "Value1", "Result1",
     "Value2", "Result2",
     "Default Result")
```

### Query Functions (Advanced)
```
GetRecords("{field.operator.'value'}")
GetFieldValues(GetRecords("{criteria}"), [Field ID])
SumValues(GetRecords("{criteria}"), [Field ID])
Size(GetRecords("{criteria}"))
GetRecordByUniqueField([Field], [Value])
```

#### Query Operators
- **EX**: Equals (exact match)
- **TV**: True Value (for user fields - searches user ID and email)
- **GT**: Greater than
- **LT**: Less than
- **CT**: Contains
- **SW**: Starts with

#### Query Examples
```
// Find records where Status = "Active"
GetRecords("{'5'.EX.'Active'}")

// Complex query with field reference
GetRecords("{'5'.EX.'"&[Manager Name]&"'}")

// User field query
GetRecords("{'6'.TV." & UserToID([User]) & "}")

// Multiple conditions
GetRecords("{8.EX.'Open'}AND{12.GT.'100'}")
```

### User Functions
```
User()                            // Current user
UserToEmail([User Field])         // Extract email
UserToName([User Field])          // Extract name
```

---

## Table Relationships Guide

### Relationship Types

#### One-to-Many (Parent-Child)
Most common relationship where one parent record relates to multiple child records.

**Components:**
- **Parent Table**: Contains master records
- **Child Table**: Contains detail records
- **Reference Field**: Links child to parent (dropdown showing parent records)
- **Key Field**: Unique identifier in parent table (usually Record ID#)

**Example:** Projects (parent) → Tasks (child)

#### Many-to-Many
Requires a junction table to connect two tables where each can relate to multiple records in the other.

**Structure:**
- Table A ← Junction Table → Table B
- Junction table contains reference fields to both primary tables

**Example:** Students ←→ Courses (via Enrollments junction table)

#### Cross-App Relationships
Relationships spanning multiple Quickbase applications.

**Limitations:**
- Always child-to-parent only
- Role-based security considerations
- Parent app must allow access

### Relationship Fields

#### Lookup Fields
Display data from parent records in child records.
```
// Automatically populated when child record selects parent
[Parent - Project Name]  // Shows project name in task record
```

#### Summary Fields
Aggregate data from child records in parent records.

**Types:**
- **Count**: Number of related child records
- **Total**: Sum of numeric values
- **Average**: Average of numeric values
- **Maximum/Minimum**: Highest/lowest values
- **Combined Text**: Concatenated unique text values
- **Combined User**: List of unique users
- **Distinct Count**: Count of unique values

**Example:**
```
// In Projects table, count of related tasks
Total Tasks: Count of related Task records
```

#### Summary Field Caching
Available on Enterprise plans for performance optimization. Allows summary fields to evaluate only when data changes rather than on every request, improving performance for complex calculations involving millions of cells.

### Best Practices
1. Use Record ID# as key field unless specific business need
2. Set up lookup fields as reference proxies for user-friendly displays
3. Consider summary field caching for complex calculations
4. Plan relationship structure before implementation

---

## Reports & Charts Reference

### Report Types

#### Table Reports
Tabular data display with columns and rows.

**Features:**
- Custom column selection and ordering
- Up to 3 report formulas per report
- Filtering and sorting
- Grouping capabilities
- Export formats (CSV, XML, etc.)
- Color-coding based on formulas

#### Summary Reports
Grouped data with calculations and subtotals.

**Structure:**
- Group by one or more fields
- Summarize numeric data (totals, averages, counts)
- Hierarchical display

#### Chart Reports
Visual data representation.

**Chart Types:**
- **Pie Charts**: Part-to-whole relationships
- **Bar Charts**: Comparisons across categories
- **Line Charts**: Trends over time
- **Area Charts**: Cumulative values
- **Gauge Charts**: Single value against target

**Features:**
- Data labels (Value, Percent, Name combinations)
- Drilldown reports
- Color customization

#### Calendar Reports
Date-based event visualization.

**Configuration:**
- Start date field (required)
- End date field (optional)
- Event display fields
- Color-coding formulas
- Initial month display options

#### Map Reports
Geographic data visualization.

**Requirements:**
- Address field in table
- Pin detail customization
- Map types (roads, satellite, hybrid, terrain)
- 100-pin display limit

#### Kanban Reports
Visual workflow management.

**Requirements:**
- Single-select multiple choice field OR user field
- Card customization (3 fields displayed)
- Drag-and-drop between columns
- Up to 15 groups (columns)
- 100 cards per group
- Manual ordering support (when enabled by app admin)

#### Timeline Reports
Project timeline visualization with fiscal year support.

### Report Components

#### Filters
- **Initial Filters**: Pre-set data restrictions
- **Dynamic Filters**: User-controllable filters
- **Field Types**: Support for all field types with appropriate operators

#### Sorting & Grouping
- Multiple sort levels
- Ascending/descending options
- Group by field values
- Manual ordering (where supported)

#### Color-Coding
Formula-based row/element coloring:
```
If([Priority]="High", "red", 
   [Priority]="Medium", "yellow", 
   "green")
```

---

## Forms & Rules Documentation

### Form Components

#### Form Elements
- **Table Fields**: Data entry fields
- **Components**: Labels, sections, rich text
- **Sections**: Visual containers
- **Columns**: Layout organization
- **Pages**: Multi-page forms with navigation

#### Form Layout
- **Drag-and-drop** element positioning
- **Grouping**: Elements display horizontally when space allows
- **Responsive design**: Adapts to screen size

### Form Rules
Conditional logic controlling form behavior.

#### Rule Structure
**When** (condition) **Then** (action)

#### Condition Types
- Field value comparisons
- User-based conditions
- Record state conditions
- Formula-based logic

#### Action Types

**Presentation Actions:**
- Show/hide fields or sections
- Enable/disable fields
- Change field properties
- Display messages

**Data Actions:**
- Set field values
- Run calculations
- Trigger workflows

#### Rule Examples
```
// Hide field based on selection
When: [Order Type] = "Digital"
Then: Hide [Shipping Address]

// Set calculated value
When: [Discount Type] = "Percentage"
Then: Set [Discount Amount] = [Order Total] * [Discount Percent]

// Conditional validation
When: [Priority] = "High" AND [Due Date] is blank
Then: Show error "High priority items require due date"
```

### Advanced Form Features

#### Subforms
Display related records within parent record forms.

#### Form Suggestions (Beta)
AI-generated field suggestions based on table name and purpose.

#### Mobile Optimization
- Responsive design principles
- Touch-friendly interfaces
- Simplified navigation

---

## Connected Tables & Integrations

### Overview
Connected tables synchronize data from external systems into Quickbase applications.

### Supported Integrations

#### Business Systems
- **Salesforce.com**: CRM data (requires API access enabled and API Enabled permission)
- **QuickBooks Online**: Financial data (requires Administrator access, only one connection per company)
- **NetSuite**: ERP data (Username/Password or Token-based auth, requires TBA enabled for tokens)
- **Intacct**: Accounting data (Company ID, sender ID/password, Web Services authorization required)
- **Bill.com**: AP/AR data

#### Cloud Storage
- **Google Drive**: File and folder data
- **Box**: Document management
- **Dropbox**: File synchronization
- **SFTP Servers**: Secure file transfer

#### Communication
- **Gmail**: Email data
- **Exchange Server**: Email and calendar data
- **Zendesk**: Support ticket data

#### Internal
- **Another Quickbase App**: Cross-app data sharing
- **Admin Console**: User and usage data
- **CSV Files**: From cloud storage folders

### Connection Management

#### Authentication Methods
- **OAuth 2.0**: Secure token-based (Salesforce, QuickBooks, Gmail)
- **Username/Password**: Direct credentials
- **Token-Based Authentication (TBA)**: Service-specific tokens
- **API Keys**: Application-specific authentication

#### Connection Features
- **Testing**: Verify connection validity
- **Reauthorization**: Refresh expired tokens
- **Multiple Connections**: Per service/account
- **Service Accounts**: Enterprise collaboration

### Data Synchronization

#### Refresh Options
- **Manual**: On-demand refresh
- **Automatic**: Scheduled refreshes
  - Hourly
  - Daily  
  - Weekly
  - Monthly

#### Refresh Key
Unique identifier field ensuring proper data synchronization:
- Single field (typical)
- Composite key (up to 3 fields for CSV)
- Must contain unique, non-null values

#### Filtering
Limit synchronized data with field-based filters:
- Field selection
- Operator choice (equals, contains, greater than, etc.)
- Value specification
- Multiple criteria with AND/OR logic

### Error Handling
Common connection issues and resolutions:
- **Invalid Credentials**: Reauthorize connection
- **Column Does Not Exist**: Update field mapping
- **Access Denied**: Check service permissions
- **Quota Exceeded**: Review usage limits

---

## Best Practices Summary

### Application Design
1. **Plan Relationships First**: Design table structure before building
2. **Normalize Data**: Use relationships to avoid duplication
3. **Choose Appropriate Field Types**: Match field type to data purpose
4. **Set Key Fields Wisely**: Use Record ID# unless business logic requires otherwise

### Performance Optimization
1. **Use Summary Field Caching**: For complex calculations (Enterprise plans)
2. **Limit Formula Queries**: Prefer relationships when possible
3. **Index Key Fields**: Ensure unique key fields for fast lookups
4. **Filter Connected Tables**: Limit synchronized data to necessary records

### Security Best Practices
1. **Role-Based Access**: Define roles before user assignment
2. **Field-Level Permissions**: Restrict sensitive data access
3. **Connection Ownership**: Use service accounts for shared integrations
4. **Regular Access Reviews**: Audit user permissions periodically
5. **PCI Compliance**: Never store credit card numbers in Quickbase
6. **Cross-App Security**: Carefully configure role permissions for cross-app relationships

### Formula Best Practices
1. **Use Appropriate Field Types**: Match formula output to field type
2. **Handle Null Values**: Account for empty fields in calculations
3. **Optimize Query Performance**: Use specific criteria in formula queries
4. **Document Complex Formulas**: Add field help text for maintenance

### Form Design
1. **User-Centric Design**: Organize forms by user workflow
2. **Progressive Disclosure**: Use form rules to show relevant fields
3. **Mobile Consideration**: Test forms on mobile devices
4. **Validation Rules**: Implement client-side validation where possible

---

## Common Patterns & Solutions

### Data Validation
```javascript
// Custom data rule for business logic validation
If([Discount %] > 0.15, "Enter a discount of 15% or less.",
   [Opportunity $ Size] > 100000 and Length([Contract PDF]) = 0, 
   "Deals worth more than $100k require a contract.")
```

### Workflow Automation
```javascript
// URL formula for workflow redirection
URLRoot() & "db/" & [_DBID_TASKS] & "?a=API_EditRecord&rid=" & [Record ID#] 
& "&_fid_7=Approved" & "&rdr=" & URLEncode(URLRoot() & "db/" & Dbid() 
& "?a=doredirect&z=" & Rurl())
```

### Dynamic Dropdowns (Cascading)
```javascript
// Parent field determines child field options
If([Category] = "Electronics", 
   ["Phone", "Laptop", "Tablet"],
   [Category] = "Clothing",
   ["Shirt", "Pants", "Shoes"],
   [])
```

### Conditional Formatting
```javascript
// Rich text formula for color-coding
"<div style=\"color:" & 
If([Status] = "Complete", "green",
   [Status] = "In Progress", "blue", 
   "red") & 
"\">" & [Status] & "</div>"
```

### Report Calculations
```javascript
// Running totals in reports
var Number PreviousTotal = 
  SumValues(GetRecords("{3.LT." & [Record ID#] & "}"), 15);
PreviousTotal + [Current Amount]
```

### Cross-Table Lookups
```javascript
// Find related data without formal relationships
GetFieldValues(
  GetRecords("{8.EX.'" & [Customer ID] & "'}"), 
  12  // Field ID to retrieve
)
```

### Date Calculations
```javascript
// Business days calculation
var Date StartDate = [Start Date];
var Date EndDate = [End Date];
var Number TotalDays = EndDate - StartDate;
var Number Weekends = 
  Floor(TotalDays / 7) * 2 + 
  If(Weekday(StartDate) + (TotalDays % 7) > 7, 2, 
     If(Weekday(StartDate) + (TotalDays % 7) > 6, 1, 0));
TotalDays - Weekends
```

### User Assignment Workflows
```javascript
// Assign based on workload
var User LeastBusyUser = 
  ToUser(GetFieldValues(
    GetRecords("{15.EX.'Active'}"), // Active users
    6, // User field ID
    "ASC", // Sort ascending
    1 // Get first record
  ));
LeastBusyUser
```

---

## Conclusion

This comprehensive guide provides the foundational knowledge needed to design, build, and maintain Quickbase applications effectively. The platform's flexibility allows for diverse solutions, from simple data tracking to complex business process automation.

### Key Takeaways
1. **Relationships are Core**: Proper table relationships enable data normalization and powerful reporting
2. **Formulas Add Intelligence**: Use formulas for calculations, validation, and workflow automation
3. **Connected Tables Enable Integration**: Seamlessly incorporate external data sources
4. **Security is Fundamental**: Implement role-based access control from the start
5. **Performance Matters**: Design with scalability and performance in mind

### Next Steps
1. Review specific use cases against these patterns
2. Plan application architecture using relationship diagrams
3. Prototype key workflows and formulas
4. Implement security model early in development
5. Test thoroughly across different user roles and scenarios

For additional support and advanced topics, consult the official Quickbase documentation and community resources.