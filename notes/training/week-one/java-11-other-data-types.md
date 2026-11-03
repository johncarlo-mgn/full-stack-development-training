### Time and Date

#### Parsing a string with DateTimeFormatter

```java
String dateString = "07-04-2026";

DateTimeFormatter dateFormat = DateTimeFormatter.ofPattern("MM-dd-yyy");

LocalDate date = LocalDate.parse(dateString, dateFormat);
```

<br>

### Primitive Wrapper Classes
- primitive types are unable to provide methods
- primitive wrapper class provide methods
- each primitive has a wrapper class
- first letter are capitalized

<br>

### Classes and Interfaces
- Classes
  - contain state
  - contain code to manipulate state
  - allows to create custom data type
- Interfaces
  - model data type behavior
  - create contracts between data types