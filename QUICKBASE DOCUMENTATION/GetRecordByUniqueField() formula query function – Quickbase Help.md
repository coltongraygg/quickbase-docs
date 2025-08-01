## GetRecordByUniqueField() formula query function

GetRecordByUniqueField() is a [formula query function](https://helpv2.quickbase.com/hc/en-us/articles/4570286674196) you can use to fetch a specific record for reference. 

-   `GetRecordByUniqueField()` can fetch records based on any unique field with the inputs of field ID and a value parameter
-   Use `GetRecordByUniqueField()` to fetch records with custom key fields
-   You can't use this function on its own. Results depend on the other function where it's used
-   Use within `[GetFieldValues](https://helpv2.quickbase.com/hc/en-us/articles/17476009195796)`, `[SumValues](https://helpv2.quickbase.com/hc/en-us/articles/17494910680212)`, or `[Size](https://helpv2.quickbase.com/hc/en-us/articles/17495208491796)` functions, which use a list of records as a parameter

## GetRecordByUniqueField() examples

|   | To query the same table | To query a different table | Result |
| --- | --- | --- | --- |
| Function layout | 
`GetRecordByUniqueField("Unique value", Field ID)`

 | 

`GetRecordByUniqueField("Unique Value", Field ID, Table Alias)`

 | 

Returns the record with the specified record ID

 |
| Example using hard-coded value | 

`GetRecordByUniqueField("1001", 12)`

Returns the record where the value of field ID 12 is 1001

 | 

`GetRecordByUniqueField("Customer Service System Update", 8, [_DBID_PROJECTS])`

Returns the record where the value of field ID 8 is "Customer Service System Update." In this case, the record is on the table with alias `DBID_PROJECTS`.

 | 

Results depend on the other function where it's used

 |
| Example using field reference | 

`GetRecordByUniqueField([Order Number], 6)`

Returns the record where the value in the Order Number field matches the value in field ID 6 

 | 

`GetRecordByUniqueField(([Order Number], 6), [_DBID_ORDERS])`

Returns the record where the value in the Order Number field matches the value in field id 6. In this case, the record is on the table with alias `DBID_ORDERS`.

 | 

Results depend on the other function where it's used

 |

## Tips for using GetRecordByUniqueField()

-   GetRecordByUniqueField() is ideal for custom key fields but you can use it with any fields that are both **unique** and **required**
    -   Fields that are not unique: the query returns the first found record if there are duplicates
    -   Blank fields: the query doesn't return a value for the record. Other records aren't affected.
-   If a field was previously unique and required, but it is no longer unique and required, the query returns a blank value  
    
-    If GetRecordByUniqueField() references a user field, enter one of the following:
    
    -   Field reference (ex: the user field \[Assigned to\])
        
    -   User's email address
        
        -   Entering a username like "abelrose" or the user's actual name like "Abdul Belrose" won't work
            
    -   Complete user ID (ex: 58651643.bzb4)
        
        Incomplete user ID won't work (for example, one missing the .bzb4 suffix)