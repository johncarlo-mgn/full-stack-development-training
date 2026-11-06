### Fundamentals of Object Oriented Programming in Java

<br>

#### Object Orientation
- based on objects, which consists of
  - state (data, held in fields/variables)
  - behavior (methods, functions)
- the state is hidden from other objects
  - the data is accessed through the object's own methods
- an OO program is a collection of objects working together
- objects are created by a class (template)
- an object created by a class is an instance of that class
- a class can be used to create a number of instances

<br>

#### Why Object Orientation
- almost universal in the software industry
- useful for analysis, design, and coding
- most successful for managing complexity
  - supports decoupling of subsystems
  - encourage reuse of components
- design rationale for much of Java language

<br>

#### Whats wrong with Global Data Structures?
- responsibility for state becomes spread out
- different subsystems are coupled together
- difficulty representing varied data formats
- extremely difficult to parallelize

<br>

#### From Use Cases to Conceptual Classes
- the process of object oriented design begins with building a picture of the requirements that the system should fulfil.
- this process is done by means of ***use cases***

<br>

#### Use Cases 
- scenarios/stories of system operation (written in natural language) that describes a self-contained sequence of events.
- often started by a human user (requesting some behavior from the system)
- list the sequence of interaction steps

```text
Use Case 1. Create Order and Checkout
"A customer creates an order by first adding various products 
(digital or physical) to a shopping cart, 
then checks out, making a payment using a credit card." 
```
```text
Use Cases 
↓ 
Domain Model (consists of real world entities, called conceptial classes)
↓
 Software Classes (Java Classes)
```

<br>

#### Discovering Conceptual Classes
- identify nouns and noun phrases in the use case description, usually takes several iterations 

```text
Use Case 1. Create Order and Checkout

"A customer creates an order by first adding various products 
(digital or physical) to a shopping cart, 
then checks out, making a payment using a credit card." 

// Conceptial Classes
- Customer, Order, Product, Shopping Cart, Payment, Credit Card
```

<br>

#### Class Relations
1. HAS-A 
2. IS-A

<br>

#### Software Classes

- currently CreditCard and Customer classes are immutabable
```java
// Customer has-a Credit Card

// java class for credit card
class CreditCard {
    private final long cardNumber;
    
    CreaditCard(long cardNumber){
        this.cardNumber = cardNumber;
    }
}

// java class for customer
public Class Customer(){
    private final String name;
    private CreditCard creditCard;
    
    public Customer(String name, long ccNumber){
        this.name = name;
        this.creditCard = new CreditCard(ccNumber);
  }
    
}
```

- shopping cart and product software classes
- `::` operator in Java is called a method reference.

```java
// java class for Product

import java.util.ArrayList;

public class Product() {
  private final String name;
  private int price;

  public Product(String name, int price) {
    this.name = name;
    this.price = price;
  }

  public int getPrice() {
    return price;
  }
}

// java class for shopping cart

public class ShoppingCart() {
  private List<Product> products = new ArrayList<>();
  
  public void addProduct(Product product){
      products.add(product);
  }
  
  // stream api
  public int getTotalCost(){
      return products.stream()
              .mapToInt(Product::getPrice)
              .sum();
  }
}

```




