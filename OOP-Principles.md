# Using OOP concepts to write high-performance Java code (2023)

## List of OOP concepts in Java:
- Abstraction
- Encapsulation
- Inheritance
- Polymorphism
- Association
- Aggregation
- Composition

# What are OOP concepts in Java?
 - Object-oriented programming focuses on objects made up of both data (fields) and code (properties or attributes). 
 - Java supports object-oriented programming
    
# Advantages of OOP
- Classes provide easy “building blocks” for faster coding and make code highly maintainable
- Create more stable and consistent code
- Make large and complex code bases more efficient and manageable
- Teams working from the same code base will benefit from existing well-written classes
- Java in particular enforces OOP, which creates good habits (but may be challenging for beginners)

# Definitions of OOP concepts

## 1. Abstraction
- Abstraction aims to hide complexity from users and show them only relevant information. For example, if you’re driving a car, you don’t need to know about its internal workings.

### Abstraction in Java
- Hides the underlying complexity of data
- Helps avoid repetitive code
- Presents only the signature of internal functionality
- Gives flexibility to programmers to change the implementation of abstract behavior
- Partial abstraction (0-100%) can be achieved with abstract classes
- Total abstraction (100%) can be achieved with interfaces
  
### Abstract classes
An abstract class is a superclass (parent class) that cannot be instantiated. To create a new object, you need to instantiate one of its child classes. Abstract classes can have both abstract and concrete methods. Abstract methods contain only the method signature, while concrete methods declare the method body as well. Abstract classes are defined with the abstract keyword.

### Interfaces
An interface is a 100% abstract class. It can only have static, final, and public fields and abstract methods. It’s frequently referred to as a blueprint of a class as well. Java interfaces allow you to implement multiple inheritances in your code, as a class can implement any number of interfaces. Classes can access an interface with the implements keyword.

## 2. Encapsulation
- Encapsulation helps with data security, allowing you to protect the data stored in a class from system-wide access. As the name suggests, it safeguards the internal contents of a class like a capsule.
- You can implement encapsulation in Java by making the fields (class variables) private and accessing them via their public getter and setter methods. JavaBeans are examples of fully encapsulated classes.

### Encapsulation in Java:

- Restricts direct access to data members (fields) of a class
- Fields are set to private
- Each field has a getter and setter method
- Getter methods return the field
- Setter methods let us change the value of the field



  
### Notes: 
- This Article is Quoted from RAYGUN, But i try to summarize it as much as posssible for fellow GitHub Friends.
- You Can Find the Original Article On: [RAYGUN](https://raygun.com/blog/oop-concepts-java/#composition)
