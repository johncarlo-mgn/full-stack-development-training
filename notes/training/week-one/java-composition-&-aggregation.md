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

### Composition (Strong Relationship)

- In a composition relationship, 
  - the child object cannot exist without the parent. 
  - The child object is entirely owned by the parent, and its lifecycle is managed completely by that parent.

```text
Rule:

When the parent object is destroyed, 
all of its composed child parts 
are automatically destroyed along with it.
```

<br>

#### Java Code Example:

*Engine.java*

```java
public class Engine {
    private String type;

    public Engine(String type) {
        this.type = type;
    }
}
```

*Car.java*

```java
public class Car {
    private Engine engine; // Composition: Engine is PART OF the car

    public Car() {
        // The engine is created INSIDE the car's constructor. 
        // It cannot exist without the Car.
        this.engine = new Engine("V8");
    }
}
```

*Main.java*

```java
public class Main {
    public static void main(String[] args) {
        Car luxuryCar = new Car();

        luxuryCar = null;
        // The luxuryCar is marked for deletion. 
        // Because the Engine was created inside it, that Engine is now dead too.
        System.out.println("The car and its engine are both marked for deletion.");
    }
}

```

<br><br>
