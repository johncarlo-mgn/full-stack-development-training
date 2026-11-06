### Aggregation (Weak Relationship)


- In an aggregation relationship
  - the child object can exist independently of the parent. 
  - If you delete the parent object, the child object remains fully intact.

```text
Rule:

The child belongs to the parent, 
but it can also belong to other parents 
or exist on its own.
```

<br>

#### Java Code Example:

*Person.java*

```java
public class Person {
    public String name;

    public Person(String name) {
        this.name = name;
    }
}

```

*House.java*

```java
public class House {
    public Person resident; // The House holds a Person

    public void moveIn(Person person) {
        this.resident = person;
    }
}

```

*Main.java* - Driver object created independently

```java
public class Main {
    public static void main(String[] args) {
        Person alex = new Person("Alex"); // 1. Alex exists

        {
            House condo = new House();
            condo.moveIn(alex);
            // 2. The condo is destroyed when this block ends
        }

        // 3. Alex still exists independently!
        System.out.println(alex.name + " still exists.");
    }
}
```

<br><br>
