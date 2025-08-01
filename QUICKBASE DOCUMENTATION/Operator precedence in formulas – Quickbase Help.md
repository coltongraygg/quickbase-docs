## Operator precedence in formulas

Operators are special symbols like `**+**` and `*****` that act on one or two values to return a new value. Quickbase evaluates operators in a specific order, called operator precedence. 

## Operator precedence

Quickbase evaluates certain operators before it acts on others.

For example,

-   \* has higher precedence than +.
-   The expression **3+4\*2** evaluates as:
    1.  4\*2 = 8
    2.  8+3 = 11

### Types of operators

**Unary operators**

-   Act on a single value. See list of [unary operators](https://www.quickbase.com/db/6ewwzuuj?a=q&qid=10 "https://www.quickbase.com/db/6ewwzuuj?a=q&qid=10").
-   Evaluate right to left when there are multiple of the same precedence next to each other

**Binary operators**

-   Act on two values. See list of [binary operators](https://www.quickbase.com/db/6ewwzuuj?a=q&qid=11 "https://www.quickbase.com/db/6ewwzuuj?a=q&qid=11")
-   Evaluate left to right when there are multiple of the same precedence next to each other

### Operator precedence table

The following table lists operators from highest precedence to lowest precedence:

| Precedence Level | Operator | Evaluation Order in Expressions |
| --- | --- | --- |
| 1 (highest) | unary +, unary -, not | Right to left |
| 2 | ^ | Left to right |
| 3 | \*, / | Left to right |
| 4 | binary +, binary -, & | Left to right |
| 5 | <, >, <=, >= | Left to right |
| 6 | \=, <>, != | Left to right |
| 7 | and | Left to right |
| 8 (lowest) | or | Left to right |

### Manually control operator precedence

Enclose portions of your formula in parentheses to manually control operator precedence.

-   Quickbase evaluates operators within parentheses first
-   Then uses the resulting calculation when it moves on to the rest of the formula

## Related

-   [Formula components](https://helpv2.quickbase.com/hc/en-us/articles/18313319756692)
    
-   [Writing formulas](https://helpv2.quickbase.com/hc/en-us/articles/4889032261012)
-   [Troubleshooting formulas](https://helpv2.quickbase.com/hc/en-us/articles/4570267666836)
    
-   [Formula Functions Reference](https://www.quickbase.com/db/6ewwzuuj?a=q&qid=6)