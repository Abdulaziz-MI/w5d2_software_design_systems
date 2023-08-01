# Answers for the Software Design Methodologies Task

- Structured design
- Function oriented design
- Object oriented design

## Question 1 - What do we mean by **coupling** and **cohesion** when discussing structured design?

### Structured Design
Firstly, structured design is a software development methodology that aims to enhance the understandability, maintainability, and efficiency of the software. This is done by breaking down a complex system into smaller and more manageable components.

### Cohesion:
Cohesion is a measure of how closely elements within a module are related to each other. So, for Java it would be about how fields and methods are related within a class. 

Similarly to the Single Responsibility Principle, which states that a class should only have one responsibility. The module following this principle is likely to have high cohesion.

![Alt text](<Screenshot 2023-07-31 at 13.19.36.png>)
![Alt text](<Screenshot 2023-07-31 at 13.30.26.png>)
 As seen in the picture the low cohesion example has unrelated methods such as sendEmail(). Ideally, that method should belong in a different class related to emails.

Essentially, a highly cohesive module is clearly defined with a  focused purpose on a specific functionality without being burdened with unrelated tasks.




### Coupling:

Coupling is a measure of how dependent one module/class is on another to perform its functionality. It represents the level of interaction/communication between modules.

<img src="Screenshot 2023-07-31 at 13.17.47.png" alt="Coupling" style="width: 300px; display: block; margin: 10px auto;">
This show different levels of coupling 

<img src="Screenshot 2023-07-31 at 15.38.27.png" alt="Tight Coupling" style="width: 300px;  display: block; margin: 10px auto;">
This is tight coupling because the two classes are very reliant upon one another, and it is overcomplicated. the order class does not need a customer object, and id or index would serve the purpose smoothly.

<img src="Screenshot 2023-07-31 at 15.38.46.png" alt="Loose coupling" style="width: 300px;  display: block; margin: 10px auto;" >
This is loose coupling as instead of a Customer object in the Order class a customerId is used instead.
<br> <br>
Loose coupling is advantageous as, it indicates that modules are loosely connected and can be modified/replaced independently without affecting other modules.






## Question 2 - What is the difference between **top-down** and **bottom-up** design? Which best describes a function oriented design?


### Top-Down vs. Bottom-Up Design

| Aspect | Top-Down Design | Bottom-Up Design |
|---|---|---|
| Starting Point | High-level overview of the system, starting with the main module representing the entire system, then dividing it | Individual components or modules are developed first |
| Approach | Starts with a broad view and progressively breaks down the system into smaller and manageable components | Starts with specific modules and builds up the system by combining them |
| Complexity Handling | Suitable for large and complex systems | Suitable for smaller and simpler systems |
| Focus | Emphasizes understanding the overall system structure and interaction between modules | Focuses on developing individual components and their functionalities |
| Advantages | Easier to understand and maintain due to clear structure hierarchy | Allows for focusing on solving specific problems first |
| Disadvantages | May be time-consuming to identify all lower-level modules in the beginning | Integration challenges may arise when combining modules |
| Examples | Software architectural designs like the Waterfall model | Developing modular libraries or APIs |


###  Which best describes a function oriented design? 

Bottom-Up design 

In a function-oriented design, the focus is on developing individual components or functions first and then combining them to build the overall system. this is much better suited with the Bottom-Up approach.



## Question 3 - In which design methodology would a **class diagram** be most useful?

A class diagram is most useful in the Object-Oriented Design (OOD) methodology. 

### Object-Oriented Design methodology

Object-Oriented Design (OOD) methodology is an approach to software design based on the principles of Object-Oriented Programming (OOP). It serves as a model software system through a collection of interacting objects.
<img src="Screenshot 2023-07-31 at 16.42.27.png" alt="Loose coupling" style="width: 300px;  display: block; margin: 10px auto;" >


Class diagrams are a fundamental tool in Object-Oriented Design, which focuses on representing the structure and relationships between classes and objects in a software system.


## Question 4 - What are the **four pillars of object oriented programming**? Give a single-sentence description of each.

1. ### Encapsulation:
    - Encapsulation is the process of **hiding the internal implementation details of a class** and **providing access to the class through public methods** - getters and setters.
    - It helps in maintaining the **integrity and security of data**.

2. ### Inheritance:
    - Inheritance allows classes to **inherit properties and methods from a parent class**, forming a **hierarchical relationship**.
    - It promotes **code reuse** and enables the creation of more specialised classes based on existing ones.

3. ### Polymorphism:
    - Polymorphism allows different classes to be treated as instances of a common superclass, enabling dynamic method **overriding** and providing a unified interface for objects of different types.

4.  ### Abstraction:
    - Abstraction is the process of representing the **essential features of an object and hiding the unnecessary details**.
    - Abstract classes **cannot be instantiated**, meaning you cannot create objects directly from it. **It serves as a blueprint for its subclasses**, providing common attributes and methods that can be inherited. Abstract classes can have both abstract and non-abstract methods. Abstract methods are declared without an implementation and must be overridden in the subclasses.
    

## Question 5 - What is the **strategy pattern**? How would its implementation differ between a functional and object oriented system? 

### Strategy Pattern
The Strategy Pattern is a behavioral design pattern that defines a family of algorithms, encapsulates each one, and makes them interchangeable at runtime.This enables the object to be more flexible and reusable, as different strategies can be easily added or modified without changing the object's core code. 

### OOD
In an OOD system, the Strategy Pattern is typically implemented using interfaces and abstract classes.The main components are:

- Strategy Interface: This interface **declares methods that represent the different strategies**, each strategy is represented by a method within this interface.

- Concrete Strategies: Concrete classes **implement the strategy interface** by providing specific implementations for the methods. Essentially, overriding them.

- Context (Contextual Class): The context class holds a reference to the **strategy interface and provides methods that allow clients to set or switch strategies**. The context class uses the strategy interface to perform its operations.

### Functional Design 

In a functional system, the Strategy Pattern can be implemented using higher-order functions. Instead of creating classes for each strategy, different functions are defined to represent the strategies. The context function takes one of these strategy functions as an argument and invokes it to perform the desired operation.


## Question 6 - Imagine your is creating a new online payment system. In order to gain maximum market share it can't be tied to a particular sector - it needs to work just as well when ordering a takeaway as when buying a new coat. Which design methodology would you suggest following? Give some justification for your decision.

I would choose the OOD system. 

### Reason for OOD

In OOD, we can create modular and flexible systems by breaking down the functionality into objects that represent real-world entities. Each object encapsulates its behavior and data, making it easy to reuse and extend functionality without affecting other parts of the system (loose coupling). For example, a Cafe, Bike shop, and grocery store can all use the same payment system given that they implement the strategy from an interface effectively.



