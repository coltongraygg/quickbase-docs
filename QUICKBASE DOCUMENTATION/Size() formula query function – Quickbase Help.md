## Size() formula query function

Size() is a [formula query function](https://helpv2.quickbase.com/hc/en-us/articles/4570286674196) you can use to count the number of records in a text, user , or record list. Size() can use `GetRecords` as a parameter, or it can use a user list or multi-select text field.

## Size() examples

|   | To query the same table | To query a different table | Result |
| --- | --- | --- | --- |
| Function layout | 
`Size(GetRecords("{query}"))`

`Size([Mulit-Select Field Name])`

 | 

`Size(GetRecords("{query}", Table Alias))`

`Size([Mulit-Select Field Name], Table Alias)`

 | 

Numeric value

 |
| Example using a hard-coded value | 

`Size(GetRecords("{6.EX.'In Progress'}"))`

Counts the number of records where field ID 6 is equal to “In Progress”

 | 

`Size(GetRecords("{6.EX.'In Progress'}", [_DBID_PROJECTS]))`

Counts the number of records in the table assigned alias `DBID_PROJECTS` where field ID 6 is equal to “In Progress”

 | 

![Example field titled: Total # of projects In-Progress. Example value returned: 3](https://helpv2.quickbase.com/hc/article_attachments/17495194114964)

Total count: 3

 |
| Example using a field reference | 

`Size([Assignees])`

Counts the number of assignees (list-user field)

 | 

`Size([Assignees], [_DBID_PROJECTS])`

Counts the number of assignees (list-user field) in the table assigned alias `DBID_PROJECTS`

 | 

![Example field titled: Total # of employees assigned to project. Example field value: 4](https://helpv2.quickbase.com/hc/article_attachments/17495231274388)

Total count: 4

 |
|  | 

`Size(GetRecords("{6.EX.'"&[Status]&"'}"))`

Counts the number of records where field ID 6 is equal to the value found in the `Status` field of the record this formula is being calculated on

 | 

`Size(GetRecords("{6.EX.'"&[Status]&"'}", [_DBID_PROJECTS]))`

Counts the number of records on the table assigned alias `DBID_PROJECTS` where field ID 6 is equal to the value found in the `Status` field of the record this formula is being calculated on

 | 

![Example field titled: Total manager hours spent. Example field value: 7](https://helpv2.quickbase.com/hc/article_attachments/17495214975636)

Total count: 2

 |