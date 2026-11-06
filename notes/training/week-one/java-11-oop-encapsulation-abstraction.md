### Encapsulation
#### hiding implementation detail at the execution level
- details that might impact the rest of the system
#### mechanism for hiding detail
- access modifiers
- packages
- modules
- also inheritance

#### Encapsulating Product Type Variation
```java
public enum ProductType {
    DIGITAL, PHYSICAL;
}

public class Product{
    private ProductType type;
}
```

### Abstraction
- hiding detail for a higher-level view
- or defining things by their essential characteristics
- in software, can define abstract objects

### Encapsulation 
- providing ways of packaging information about a component
- hiding unnecessary detail
- an implementation of abstraction


### The Single Responsibility Principle (SRP)
#### a class should have only one reason to change
