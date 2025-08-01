## Grid edit behavior and formula query fields

If you are using [grid edit](https://helpv2.quickbase.com/hc/en-us/articles/4570328849812) on tables that have formula queries in formula fields, there are some different behaviors:

-   You cannot directly edit formula fields while using grid edit
-   However, you can edit fields that are referenced in formula queries
-   Some formula fields will update immediately when a field they reference is updated. Others will not.

## How formulas that reference other records calculate

When you edit a field that is referenced in a formula query, you'll see the formula field update only for that record.

For example: in this table, 

-   Field **A** is not a formula field
-   Field **C** is a formula field
-   Field **C** references field **A** when it calculates

<table><tbody><tr><td><strong>Record</strong></td><td><p><strong>Field<br></strong><span>(not a formula field)</span></p></td><td><p><strong>Formula field<br></strong><span>(contains a formula query)</span></p></td><td><strong>Changes to formula field</strong></td></tr><tr><td><strong>1</strong></td><td>A<br><span>(updated during grid edit)</span></td><td><p>C&nbsp;<br><span>(references field A)</span></p></td><td>Occurs instantly</td></tr><tr><td><strong>&nbsp;2</strong></td><td>A</td><td><p>C&nbsp;<br><span>(references field A)</span></p></td><td>Click Save to see changes</td></tr></tbody></table>

-   When you edit **field A** in **record** **1** during a grid edit:
    -   Record 1: the value of field C will change instantly since it is on the same record as the edited field
    -   Record 2: the value of field C will change on Save

## How formulas that rely on other records with formulas calculate

During a grid edit if you

-   Edit fields that impact formula query results AND
-   Other fields rely on the calculated results for their value

Then

-   The original value is used in the additional formula calculation until after you save

**This means formulas could use outdated data in their calculations until you Save.**

For example: in this table, 

|   | **Field  
**(not a formula field) | **Formula field  
**(contains a formula query) | 
**Formula field  
**(contains a formula query)

 | 

**Changes to formula field**

 |
| --- | --- | --- | --- | --- |
| Record 1 | A  
(updated during grid edit) | B | C  
(references field A) | Occur instantly |
| Record 2 | A | B | C  
(references field A in **record 1**) | Click Save to see changes |
| Record 3 | A | B  
(references C in **record 2**) | C | Click Save to see correct calculation. Pre-save, will calculate based on the previous value of field C in record 2 |

-   Field C in records 1 and 2 references reference field A in its calculation
    
-   Field B in record 3 references field C in record 2 in its calculation
    
-   If you edit field A in record 1, only field C in record 1 will update before saving the grid edit
    
    -   Field C in record 2 will not update
        
-   Before saving the grid edit, field C in record 3 is calculated using the original value of field C in record 2
    
-   After saving the grid edits, all field values are updated