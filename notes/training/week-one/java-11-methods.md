### Methods
- organizing code
- reusable code
- can receive data
- can return data

<br>

#### Declaring and Calling Method
- name
  - same rules as variables
- typed parameter list 
  - allow data values to be passed in
  - can be empty parameter list
- body 
  - consists of 0 or more statements
  - enclosed in brackets
- return type 
  - indicates the type of data returned
  - use void when no value returned

```
// syntax
modifier return-type name (typed-parameter-list){
    statements
}
```

```
// call method
doSomething();

// declare method
static void doSomething(){
    sout("Hello!");
}
```

<br>

#### Method Data
- variables - scope limited to method where declared
- parameters - enable passing data to methods

<br>

#### Using Parameters

```
// calling
show("Hello!");

// declaration
static void show(String s){
    sout(s);
}
```

<br>

#### Method Exits
1. end of method - no more code in method
2. `return` statement - explicitly exit method
3. error occurs - method exits when error occurs, throws an exception

```
// calling
show(0);

// declaration
static void show(int i){

    if(i < 0) 
        return;

    sout("many codes here!");
}
```
<br>

#### Returning a Value

```
// calliing
int result = sum(1, 2);
sout(result);

// declaration
static int sum(int i, int j){
    return i + j;
}
```
<br>

#### Returning an Array

```
// calliing
int[] result = returnArray(1, 2);
sout(result);

// declaration
static int[] returnArray(int i, int j){
    int[] arr = {i, j};
    return arr;
}
```

<br>