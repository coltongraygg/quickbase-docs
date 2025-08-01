## GetFieldValues() formula query function

GetFieldValues() is a [formula query function](https://helpv2.quickbase.com/hc/en-us/articles/4570286674196) that you can use get values from a specific field of the records referenced in the `GetRecord`, `GetRecordByUniqueField()`, or `GetRecords` function. 

## GetFieldValues() examples

|   | To query the same table | To query a different table | Result |
| --- | --- | --- | --- |
| Function layout | 
`GetFieldValues(GetRecords("{query}"), Field ID)`

 | 

`GetFieldValues(GetRecords("{query}", Table Alias), Field ID)`

 | 

List of field values

Values display like multi-select fields in the table

 |
| Example using hard-coded value | 

`GetFieldValues(GetRecords("{6.EX.'In Progress'}"), 3)`

Returns the value of the field with field ID 3 in records where field ID 6 is equal to “In Progress”

(Field id 3 is the `Record ID#` field, so this will return a record id number.)

 | 

`GetFieldValues(GetRecords("{6.EX.'In Progress'}", [_DBID_PROJECTS]), 3)`

Returns the value of field 3 in records where field ID 6 is equal to “In Progress”.

In this case, field 3, field 6 and the records are from the table with table alias `DBID_PROJECTS`

(Field ID 3 is the `Record ID#` field, so this returns a record ID number.)

 | 

![Example field titled: Other tasks In-Progress. Example values returned from formula: 2,3. Values in the field are separated in a small box, just like multi-select fields display. There is no separating punctuation between the values.](https://helpv2.quickbase.com/hc/article_attachments/17476025094292)

Field values: 2, 3

 |
|  | 

`GetFieldValues(GetRecord(101), 5)`

Returns the value of the field with field id 5 in the record with record id 101

 | 

`GetFieldValues(GetRecord(101, [_DBID_PROJECTS]), 5)`

Returns the value of the field with field ID 5 in the record with record ID 101 from the table with alias `DBID_PROJECTS`

 | 

![Example field titled: Prioritization. Example value returned: Med. Value in the field are separated in a small box, just like multi-select fields display.](https://helpv2.quickbase.com/hc/article_attachments/17475996099476)

Field value: Med

 |
|  | 

`GetFieldValues(GetRecordByUniqueField("1001", 6), 13)`

Returns the value of the field with field id 13 in the record where the value of field id 6 is 1001

 | 

`GetFieldValues(GetRecordByUniqueField("1001", 6, [_DBID_SALES]), 13)`

Returns the value of the field with field ID 13 in the record where the value of field ID 6 is 1001. 

In this case, field 6 and field 13 are from the table with table alias `DBID_SALES`

 | 

![mceclip0.png](https://helpv2.quickbase.com/hc/article_attachments/17475985779988)

Field value: Michele Cherise

 |
| Example using field reference | 

`GetFieldValues(GetRecords("{6.EX.'"&[Manager name]&"'}"), 10)`

Returns the value of the field with field ID 10 in records where field ID 6 is equal to the `Manager name` field in the record the formula is being calculated on

 | 

`GetFieldValues(GetRecords("{6.EX.'"&[Manager name]&"'}", [_DBID_PROJECTS]), 10)`

Returns the value of the field with field ID 10 in records where field ID 6 is equal to the `Manager name` field in the record the formula is being calculated on

In this case, field 10, field 6 and the records are all from the table with table alias `DBID_PROJECTS`

 | 

![Example field titled: Also managing these projects. Example values returnes: Annual conference, Market Analysis. Values in the field are separated in a small box, just like multi-select fields display. There is no separating punctuation between the values.](https://helpv2.quickbase.com/hc/article_attachments/17476025104788)

Field values: Annual conference, Market analysis

 |
|   | 

`GetFieldValues(GetRecord([Primary Contact ID#]), 8)`

Returns the value of field ID 8 from the record where the field `Primary Contact ID#` matches with the same value as the record the formula is being calculated on

 | 

`GetFieldValues(GetRecord([Primary Contact ID#], [_DBID_CUSTOMERS]), 8)`

Returns the value of field ID 8 from the record where the field `Primary Contact ID#` matches the same value as the record the formula is being calculated on

In this case, field ID 8 and the records are on the table assigned table alias `DBID_CUSTOMERS`

 | 

![Example field titled: Primary Contact Phone Number. Example value returned: (583)669-2868. Value in the field are separated in a small box, just like multi-select fields display.](https://helpv2.quickbase.com/hc/article_attachments/17475993435284)

Field value: (538)669-2868

 |
|   | 

`GetFieldValues(GetRecordByUniqueField([Order Number], 6), 13)`

Returns the value of the field with field ID 13 where the value in the field `Order Number` matches the value in field ID 6

 | 

`GetFieldValues(GetRecordByUniqueField([Order Number], 6, [_DBID_SALES]), 13)`

Returns the value of the field with field ID 13 where the value in the field `Order Number` matches the value in field ID 6

In this case, field 6 and field 13 are from the table with table alias `DBID_SALES`

 | 

![mceclip0.png](https://helpv2.quickbase.com/hc/article_attachments/17475985779988)

Field value: Michele Cherise

 |