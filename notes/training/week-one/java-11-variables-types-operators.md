
### Variables
- Named data storage
- Strongly typed

    ``` 
    int dataValue;
    dataValue = 100;
    int info = 200;
    ```

#### Variable naming conventions
- Use only letters and numbers
- First character cannot be a number
- Use camelCase

#### Final variables
- Use final modifier
- Value cannot be changed once set
- Helps avoid errors caused by inadvertent variable changes

    ``` 
    final int i = 25;
    ```

<br>

### Primitive Data Types
- built into the language
- foundation of all other types
- primitive data types are stored by value
  - each variable's values are unrelated to any other variable's values
  - each variable are allocated an area of memory

      ``` 
      int first = 100;
      int second = first;
  
      first = 50;
      second = 70;
      ```

#### Four Categories

1. **integer**
    
    | Type  | Bits | Min Value                  | Max Value                 |
    |-------|------|----------------------------|---------------------------|
    | byte  | 8    | -128                       | 127                       |
    | short | 16   | -32_768                    | 32_767                    |
    | int   | 32   | -2_147_483_648             | 2_147_483_647             |
    | long  | 64   | -9_223_372_036_854_775_808 | 9_223_372_036_854_775_807 |

    ``` 
    byte b = 10;
    short s = 1000;
    int i = 10000000
    long l = 1000000000000L;
    ```

2. **floating point**
- store values containing a fractional value

   | Type   | Bits | Min Value         | Max Value        |
   |--------|------|-------------------|------------------|
   | float  | 32   | 1.4 x $10^{-45}$  | 3.4 x $10^{38}$  |
   | double | 64   | 4.9 x $10^{-324}$ | 1.7 x $10^{308}$ |

    ``` 
    float f = 42.195f;
    double d = 0.000000001d;
    ```

3. **character**
- stores a single Unicode character
- single quotes
- for Unicode pints, \u followed by 4 digits hex

    ``` 
    char c= 'C';
    char u = '\u00DA';
    ```

4. **boolean**
- stores true/false values

    ``` 
    boolean isGood = true;
    ```

<br>

### Operators

#### Arithmetic Operators
- `+` - add
- `-` - subtract
- `*` - multiply
- `/` - divide
- `%` - modulus

#### Prefix and Postfix Operators
- `++` - increment operator
- `--` - decrement operator

#### Compound Assignment Operators
- apply right side value to the left side, store result on the left side
- `+=`
- `-=`
- `*=`
- `/=`
- `%=`

#### Type Conversion
- Implicit type conversion
    - automatically performed by the compiler  

    ``` 
    int i = 50;
    long x = i;
    ```

- Explicit type operator 
  - performed explicitly in code with cast operator

    ``` 
    long x = 50;
    int i = ()int l;
    ```













