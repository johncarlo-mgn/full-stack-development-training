### Working with String 

#### String class
- stores a sequence of Unicode characters
- literals are enclosed in double quotes
- values can be concatenated using + and +=

<br>

#### Strings are Immutable
- string variables do not directly hold the string value
- hold a reference to the instance of a string
- changes in the value create a new instance of the string

<br>

#### String Equality
- comparing with `==` equality operator
  - checks if both reference the same string instance
- comparing with `.equals()` method
  - character by character comparison
- the equals method is the best choice in most cases

<br>

#### Interning a String
- provides a canonicalized value
- when you enter a string, a string of any given value, will always return back a reference to the same string instance
- enables reliable `==` operator comparison
- improves performance of frequently compared strings

```java
String s1 = "I love java";
String s3 = s1.intern();
String s4 = s1.intern();
if(s3 == s4){};
```

<br>

#### String Class Methods
- length 
  - `lenght();`
- create new strings from existing
  - `concat();`
  - `replace();`
  - `toLowerCase();`
  - `toUpperCase();`
  - `trim();`
  - `split();`
- extract substring
  - `chartAt();`
  - `sunstring();`
- test substring
  - `conatains();`
  - `endWith();`
  - `startsWith();`
  - `indexOf();`
  - `lastIndexOf();`
- comparison
  - `equals()`
  - `equalsIgnoreCase()`
  - `isEmpty()`
  - `compareTo()`
  - `compareToIgnoreCase()`
- formatting
  - `format();`
- String for non-string
  - `valueOf();`
``

<br>

#### Converting non-string Types to String
- virtually all data types can be converted into a string

```java
int i = 100;
String iString = String.valueOf(i); // "100"
```

#### String Builder
- provides mutable string buffer
  - efficiently constructs string values
  - add a new content to end with `append`
  - add a new content within with `insert`
- extract content to a string
  - using `toString();`

```java
String location = "Mars";
String city = " red city";
StringBuilder fullAddress = new StringBuilder();
fullAddress.append("I am ");
fullAddress.append(location);
fullAddress.append(city);
String myAddress = fullAddress.toString();

String in = "in ";
int position = fullAddress.indexOf("Mars");
fullAddress.insert(position, in);
myAddress = fullAddress.toString();
```














