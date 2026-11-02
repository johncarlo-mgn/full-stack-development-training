### Conditionals

#### Relational Operators
- `>` - greater than
- `>=` - greater than or euqal
- `<` - less than
- `<=` - less than or equal
- `==` - equal to
- `!=` - not equal to

#### Conditional Assignment (ternary operator)
   
    result = (condition) ? true-value : false-value;

<br>

### If-else statement
- conditionally executes a statement
- else clause executes a statement when condition is false, it is optional


    if (condition){
        true-statement;
    } else {
        false-statement;
    }

#### Chaining if-else

    if (condition){
        true-statement;
    } else if  {
        true-statement;
    } else {
        false-statement;
    }

<br>

### Logical Operators
- produce a single true/false value result from two true/false values
- `&` - And
- `|` - Or
- `^` - exclusive or XOR
- `!` - negation
- `&&` - conditional And
- `||` - conditional Or

<br>

### Switch Statement
- test value against multiple matches
  

    switch(value-to-test){

        case matching-value;
            statements;
            break;
        case matching-value;
            statements;
            break;
        default:
            statements;

    }
