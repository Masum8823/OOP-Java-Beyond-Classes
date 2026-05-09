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