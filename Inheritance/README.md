# Inheritance

## Definition
Inheritance is a concept in object-oriented programming where one class (**Sub/Child class**) can use the properties and methods of another class (**Super/Parent class**).

---

# Use of Inheritance

✅ It helps to reuse code (**no need to write same code again**)  

✅ It makes programs easier to manage and understand  

✅ It allows adding new features without changing old code  

✅ It supports real-life relationships like **parent–child**  

---

# Types of Inheritance 

Java supports the following types of inheritance:

| Inheritance Type | Description |
|---|---|
| **Single Inheritance** | One child class inherits from one parent class |
| **Multilevel Inheritance** | A class inherits from another child class |
| **Hierarchical Inheritance** | Multiple child classes inherit from one parent class |
| **Multiple Inheritance** | One child class inherits from multiple parent classes |
| **Hybrid Inheritance** | Combination of two or more inheritance types |

---

## List of Inheritance Types

### 1️⃣ Single Inheritance
One child class inherits from one parent class.

### 2️⃣ Multilevel Inheritance
A child class becomes the parent of another class.

### 3️⃣ Hierarchical Inheritance
Multiple child classes inherit from the same parent class.

### 4️⃣ Multiple Inheritance
One class inherits from multiple classes.

### 5️⃣ Hybrid Inheritance
Combination of different inheritance types.

---

# Single Inheritance

A child class inherits from one parent class only is called Single Inheritance.

---

## Flow

```text
Class A → Class B
```

(Here B gets features from A)

---

## Code Example:

```java
// Parent class
class A {
    void showA() {
        System.out.println("This is class A");
    }
}

// Child class
class B extends A {
    void showB() {
        System.out.println("This is class B");
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        B obj = new B();

        obj.showA(); // inherited from A
        obj.showB(); // own method of B
    }
}
```

---

# Multilevel Inheritance

A child class inherits from a parent class, and that child class is also inherited by another child class, this type of inheritance is called Multilevel Inheritance.

---

## Flow

```text
Class A → Class B → Class C
```

(C gets features from B, and B gets from A)

---

## Code Example

```java
class A {
    void showA() {
        System.out.println("Class A");
    }
}

class B extends A {
    void showB() {
        System.out.println("Class B");
    }
}

class C extends B {
    void showC() {
        System.out.println("Class C");
    }
}

public class Main {
    public static void main(String[] args) {
        C obj = new C();

        obj.showA();
        obj.showB();
        obj.showC();
    }
}
```

---

# Hierarchical Inheritance

One parent class is inherited by multiple child classes, this type of inheritance is called Hierarchical Inheritance.

---

## Flow

```text
Class A → Class B
Class A → Class C
```

(B and C both get features from A)

---

## Code Example

```java
class A {
    void showA() {
        System.out.println("Class A");
    }
}

class B extends A {
    void showB() {
        System.out.println("Class B");
    }
}

class C extends A {
    void showC() {
        System.out.println("Class C");
    }
}

public class Main {
    public static void main(String[] args) {
        B obj1 = new B();
        C obj2 = new C();

        obj1.showA();
        obj1.showB();

        obj2.showA();
        obj2.showC();
    }
}
```

---

# Multiple Inheritance 
A class tries to inherit from more than one parent class, this type of inheritance is called Multiple Inheritance.(Not directly supported in Java for classes)


---

## Flow (conceptual)

```text
Class A + Class B → Class C
```

(C gets features from both A and B)

---

## Note

Java does not allow this with classes, but it is possible using interfaces.

---

## Code Example

```java
interface A {
    void showA();
}

interface B {
    void showB();
}

class C implements A, B {
    public void showA() {
        System.out.println("Interface A");
    }

    public void showB() {
        System.out.println("Interface B");
    }
}

public class Main {
    public static void main(String[] args) {
        C obj = new C();

        obj.showA();
        obj.showB();
    }
}
```

---

# Hybrid Inheritance 

A mix of two or more inheritance types, this type of inheritance is called Hybrid Inheritance.(Combination of multiple types)

---

## Flow example

```text
Class A → Class B → Class D
Class A → Class C → Class D
```

(D gets features through multiple paths)

---

## Code Example (using interface + class)

```java
class A {
    void showA() {
        System.out.println("Class A");
    }
}

class B extends A {
    void showB() {
        System.out.println("Class B");
    }
}

interface C {
    void showC();
}

class D extends B implements C {
    public void showC() {
        System.out.println("Interface C");
    }
}

public class Main {
    public static void main(String[] args) {
        D obj = new D();

        obj.showA();
        obj.showB();
        obj.showC();
    }
}
```

---

# Why Multiple Inheritance is NOT allowed in Java (for classes)?

Java does not support multiple inheritance using classes because it creates ambiguity problems and makes code confusing and unsafe.

---

# Ambiguity problem

If a class inherits from two parent classes and both parents have the same method, then Java cannot decide which method to use.

---

# Diamond Problem in Inheritance

## Structure (problem shape)

```text
      A
     / \
    B   C
     \ /
      D
```

---

## What happens

- Class A has a method `show()`

- Class B and C both inherit A and override `show()`

- Class D inherits both B and C

---

## Now if D calls `show()`, Java is confused

- Should it call B’s version?

- Or C’s version?

This confusion is called the **Diamond Problem**.

---

# Why Java avoids it

Java avoids multiple inheritance with classes, to:

- Prevent ambiguity

- Avoid unpredictable behavior

- Keep the language simple and safe

---

# Solution of Diamond Problem in Java

## 1. Using Interfaces (Main Solution)

Java allows multiple inheritance through interfaces because interfaces do not have implementation conflict (mostly).

---

## Flow

```text
Interface A
Interface B
Class C implements A, B
```

---

## Idea

- Interfaces only define methods (no confusion of implementation)

- Class must define the method itself

---

