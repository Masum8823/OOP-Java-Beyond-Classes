# super Keyword in Java 

## Definition

`super` keyword is used in Java to refer to the parent class object from a child class. It is mainly used to access parent class variables, methods, and constructor.

---

# Uses of super keyword

1. To access parent class variable

2. To call parent class method

3. To call parent class constructor

---

# Example in Inheritance

```java
class A {
    int x = 10;

    void show() {
        System.out.println("Class A method");
    }
}

class B extends A {
    int x = 20;

    void display() {
        System.out.println("Child class variable x: " + x);
        System.out.println("Parent class variable x: " + super.x);

        show();         // child or inherited method
        super.show();   // calling parent class method
    }
}

public class Main {
    public static void main(String[] args) {
        B obj = new B();
        obj.display();
    }
}
```

---

# Simple Explanation

- `super.x` → accesses parent class variable

- `super.show()` → calls parent class method

- `super()` → calls parent class constructor (used inside constructor)

---

# Calling Parent Class Constructor using super() (with variable access in child class)

## Concept

`super()` is used inside the child class constructor to call the parent class constructor and initialize parent class variables.

---

# Code Example:

```java
class A {
    int x;

    // Parent class constructor
    A(int x) {
        this.x = x;
        System.out.println("Parent constructor called");
    }
}

class B extends A {
    int y;

    // Child class constructor
    B(int x, int y) {
        super(x); // calling parent constructor
        this.y = y;
        System.out.println("Child constructor called");
    }

    void display() {
        System.out.println("Parent variable x: " + x);
        System.out.println("Child variable y: " + y);
    }
}

public class Main {
    public static void main(String[] args) {
        B obj = new B(10, 20);
        obj.display();
    }
}
```

---

# Simple Explanation

- `super(x)` sends value to parent constructor

- Parent constructor sets `x`

- Child class inherits `x` and can use it directly

- Then child class uses both `x` and `y` in `display()`

---

# Output Idea

```text
Parent constructor called
Child constructor called
Parent variable x: 10
Child variable y: 20
```

---

