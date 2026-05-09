# Abstract Class 

## Definition

An abstract class is a class that cannot be used to create objects directly. It is used as a base class for other classes.

It is declared using the `abstract` keyword.

---

## Key Features

- Cannot create object of abstract class

- Can have abstract methods (no body)

- Can also have normal methods (with body)

- Used for inheritance and code reuse

- Child class must implement abstract methods

---

## Why we use it

- To provide a common structure for all child classes

- To force child classes to follow a rule (method implementation)

- To achieve partial abstraction

---

## Simple Example Idea (Flow)

```text
Abstract Class A
        ↓
     Class B (implements methods)
```

---

## Important Points for Exam

- Declared using `abstract` keyword

- Can contain both abstract and non-abstract methods

- Cannot be instantiated

- Supports inheritance

---

## Code Example of Abstract Class:

```java

// Abstract Class
abstract class Exam {
    abstract void startExam();
    abstract void evaluate();
    abstract void showResult();
}

// Programming Exam
class ProgrammingExam extends Exam {
    int marks;

    void startExam() {
        System.out.println("Programming Exam Started");
    }

    void evaluate() {
        marks = 85;
        System.out.println("Evaluating based on code output and test cases");
    }

    void showResult() {
        System.out.println("Programming Exam Marks: " + marks);
    }
}

// Theory Exam
class TheoryExam extends Exam {
    int marks;

    void startExam() {
        System.out.println("Theory Exam Started");
    }

    void evaluate() {
        marks = 78;
        System.out.println("Evaluating written answers");
    }

    void showResult() {
        System.out.println("Theory Exam Marks: " + marks);
    }
}

// Viva Exam
class VivaExam extends Exam {
    int marks;

    void startExam() {
        System.out.println("Viva Exam Started");
    }

    void evaluate() {
        marks = 90;
        System.out.println("Evaluating oral performance");
    }

    void showResult() {
        System.out.println("Viva Exam Marks: " + marks);
    }
}

// Main Class
public class UniversityExamSystem {
    public static void main(String[] args) {

        Exam prog = new ProgrammingExam();
        Exam theory = new TheoryExam();
        Exam viva = new VivaExam();

        System.out.println("---- Programming Exam ----");
        prog.startExam();
        prog.evaluate();
        prog.showResult();

        System.out.println("\n---- Theory Exam ----");
        theory.startExam();
        theory.evaluate();
        theory.showResult();

        System.out.println("\n---- Viva Exam ----");
        viva.startExam();
        viva.evaluate();
        viva.showResult();
    }
}

```

---

# Interface 

## Definition

An interface in Java is a blueprint of a class that contains only method declarations (before Java 8). It is used to achieve 100% abstraction and multiple inheritance (through interfaces).

It is declared using the `interface` keyword.

---

## Key Features

- Cannot create objects of an interface

- Contains abstract methods (by default)

- Variables are `public`, `static`, and `final` (constant)

- A class uses `implements` keyword to use an interface

- Supports multiple inheritance in Java

- All methods must be implemented by the class

---

## Why we use it

- To achieve full abstraction

- To support multiple inheritance

- To define a common behavior for different classes

- To make code more flexible and reusable

---

## Simple Flow Example

```text
Interface A, Interface B
          ↓
       Class C implements A, B
```

---

## Important Points for Exam

- Declared using `interface` keyword

- Cannot be instantiated

- Methods are abstract by default (before Java 8)

- Supports multiple inheritance

- Used with `implements` keyword

---

## Code Example:

```java

# Interface in Java (Complete Notes with Code)

## Definition:
An interface in Java is a **blueprint of a class** that defines a set of rules (methods) that must be implemented by classes. It is used to achieve **100% abstraction** and **multiple inheritance in Java**.

---

## Idea:
Interface defines **what to do**, and the implementing class defines **how to do it**.

---

## Code Example:

```java
interface Animal {
    void sound();   // abstract method (no body)
}

class Dog implements Animal {

    public void sound() {
        System.out.println("Dog barks");
    }
}

class Cat implements Animal {

    public void sound() {
        System.out.println("Cat meows");
    }
}

public class Main {
    public static void main(String[] args) {

        Animal a1 = new Dog();
        Animal a2 = new Cat();

        a1.sound();
        a2.sound();
    }
}

```

### Simple Explanation:

- `interface Animal` defines a rule: every animal must have `sound()`
- `Dog` and `Cat` implement the rule in their own way
- Same method name, different behavior
- This shows runtime polymorphism using interface
- One interface can be used by many classes

---

### Key Understanding:

- Interface is a **contract (rule set)** for classes  
- It does not provide full implementation (only method declarations)  
- Classes must implement all interface methods  
- Helps achieve **loose coupling (flexible design)**  
- One interface → many implementations  

---

### Important Points:

- Cannot create objects of an interface  
- Methods are abstract by default (before Java 8)  
- Variables are `public static final` (constants)  
- A class uses `implements` keyword  
- Supports multiple inheritance  
- All interface methods must be overridden in implementing class  
- Improves code flexibility and scalability  

---

### Real-Life Example Idea:

- Interface: Vehicle → rule: `start()`, `stop()`  
- Classes: Car, Bike, Bus → different implementations  

---

### Simple Summary:

- Interface = only rules (no full logic)  
- Class = actual implementation  
- Used for **100% abstraction**  
- Supports multiple inheritance and runtime polymorphism  

---