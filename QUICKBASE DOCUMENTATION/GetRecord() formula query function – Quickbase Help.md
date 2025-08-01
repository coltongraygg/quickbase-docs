## GetRecord() formula query function

GetRecord() is a [formula query function](https://helpv2.quickbase.com/hc/en-us/articles/4570286674196) you can use to fetch a specific record for reference. 

-   You can't use this function on its own
-   Use within `[GetFieldValues](https://helpv2.quickbase.com/hc/en-us/articles/17476009195796)`, `[SumValues](https://helpv2.quickbase.com/hc/en-us/articles/17494910680212)`, or `[Size](https://helpv2.quickbase.com/hc/en-us/articles/17495208491796)` functions, which use a list of records as a parameter
-   Only generated record IDs (not custom key fields) can be used to fetch records using `GetRecord()`

## GetRecord() examples

|   | To query the same table | To query a different table | Result |
| --- | --- | --- | --- |
| Function layout | 
`GetRecord(Numeric field)`

 | 

`GetRecord(Numeric field, Table Alias)`

 | 

Returns the record with the specified record ID

 |
| Example using hard-coded value | 

`GetRecord(101)`

Returns the record with record ID 101

 | 

`GetRecord(101, [_DBID_PROJECTS])`

Returns the record with record ID 101 on the table assigned alias `DBID_PROJECTS`

 | 

N/A

Results depend on the other function where it's used

 |
| Example using field reference | 

`GetRecord([Primary Contact ID#])`

Returns the record with the record ID that matches the value in `Primary Contact ID#` in the record where it's used

 | 

`GetRecord([Primary Contact ID#], [_DBID_CUSTOMERS])`

Returns the record with the record ID that matches the value in `Primary Contact ID#` in the record where it's used. In this case, the record is on the table with alias `DBID_CUSTOMERS`

 | 

N/A

Results depend on the other function where it's used

 |