### While Loop
- continue running as long as the condition is true
```
while(condition){
    statement;
}
```

<br>

### Do-while 
- condition is checked at the end of the loop
- continue running as long as the condition is true
- always rund at least once

```
do{
    statement;
} while (condition);
```
<br>

### For Loop
- condition checked at loop start

```
for(initialize; condition; update){
    statement;
}
```

<br>

### Arrays
- provide an ordered collection of elements
- each element is accessed via an index
- index range from 0 - number-of-elements minus 1
- number of elements can be accessed via array's `length` value

```
// declare array

float[} vals = new float[3]; 

// set values
vals[0] = 10.0f;
vals[1] = 20.0f;
vals[2] = 30.0f;

// initialize array

float[] vals = { 10.0f, 20.0f; 30.0f }; 

// looping array

for(int i = 0; i < vals.length; i++){
    sout(vals[i]);
}

```
