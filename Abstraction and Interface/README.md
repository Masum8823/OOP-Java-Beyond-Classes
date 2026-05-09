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
