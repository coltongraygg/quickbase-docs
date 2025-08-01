## SumValues() formula query function

SumValues() is a [formula query function](https://helpv2.quickbase.com/hc/en-us/articles/4570286674196) you can use to calculate the sum of values in a field for records that match the query.

## SumValues() examples

|   | To query the same table | To query a different table | Result |
| --- | --- | --- | --- |
| Function layout | 
`SumValues(GetRecords("{query}"), Field ID)`

 | 

`SumValues(GetRecords("{query}", Table Alias), Field ID))`

 | 

Numeric value

 |
| Example using hard-coded value | 

`SumValues(GetRecords("{6.EX.'In Progress'}"), 4)`

Calculates the sum of the values in field id 4 where field ID 6 is equal to “In Progress”

 | 

`SumValues(GetRecords("{6.EX.'In Progress'}", [_DBID_PROJECTS]), 4)`

Calculates the sum of the values in field ID 4 where field ID 6 is equal to “In Progress”

In this case, field 4, field 6 and the records are all from the table with table alias `DBID_PROJECTS`.

 | 

![Example field titled: Total hours spent on all In-Progress projects. Example value returned: 5](https://helpv2.quickbase.com/hc/article_attachments/17494926318228)

Sum value: 5

 |
| Example using field reference | 

`SumValues(GetRecords("{6.EX.'"&[Manager name]&"'}"), 4)`

Calculates the sum of the values in field ID 4 where field id 6 is equal to the value that populates the `Manager name` field in the record this formula is being calculated on

 | 

`SumValues(GetRecords("{6.EX.'"&[Manager name]&"'}", [_DBID_PROJECTS]), 4)`

Calculates the sum of the values in field ID 4 where field id 6 is equal to the value that populates the `Manager name` field in the record this formula is being calculated on

In this case, field 4, field 6 and the records are all from the table with alias `DBID_PROJECTS`

 | 

![Example field titled: Total manager hours spent. Example value returned: 7](https://helpv2.quickbase.com/hc/article_attachments/17494940490772)

Sum value: 7

 |