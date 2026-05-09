# Upcasting 

## Definition

Upcasting means converting a child class object into a parent class reference. It is done automatically in Java.

It is used to achieve runtime polymorphism.

---

## Basic Idea

```text
Parent reference → Child object
```

---

## Code Example:

```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }

    void breed() {
        System.out.println("Labrador breed");
    }
}

public class Main {
    public static void main(String[] args) {

        Animal obj = new Dog(); // Upcasting

        obj.sound(); // calls Dog's method (runtime polymorphism)

        // obj.breed(); ❌ Not allowed (parent reference cannot access child-specific methods)
    }
}
```

---

## Quiz Question:

```java
// Quiz_Question from Mahadi_Sir

class Employee {
    String name;
    double baseSalary;

    Employee(String name, double baseSalary) {
        this.name = name;
        this.baseSalary = baseSalary;
    }

    double calculateSalary() {
        return baseSalary;
    }

    void display() {
        System.out.println(name + " salary : " + calculateSalary() + " TK");
    }
}

class Lecturer extends Employee {
    int extraClasses;
    double ratePerClass;

    Lecturer(String name, double baseSalary, int extraClasses, double ratePerClass) {
        super(name, baseSalary);
        this.extraClasses = extraClasses;
        this.ratePerClass = ratePerClass;
    }

    // overriding
    double calculateSalary() {
        return extraClasses * ratePerClass;
    }
}

class LabAssistant extends Employee {
    int overtimeHours;
    double overtimeRate;

    LabAssistant(String name, double baseSalary, int overtimeHours, double overtimeRate) {
        super(name, baseSalary);
        this.overtimeHours = overtimeHours;
        this.overtimeRate = overtimeRate;
    }

    // overriding
    double calculateSalary() {
        return overtimeHours * overtimeRate;
    }
}

class AdminStaff extends Employee {
    double bonus;

    AdminStaff(String name, double baseSalary, double bonus) {
        super(name, baseSalary);
        this.bonus = bonus;
    }

    // overriding
    double calculateSalary() {
        return baseSalary - bonus;
    }
}

public class Quiz_Question_Mahadi_Sir {
    public static void main(String[] args) {

        Employee e1 = new Lecturer("Rahim", 30000, 5, 1000);
        Employee e2 = new LabAssistant("Karim", 20000, 10, 1200);
        Employee e3 = new AdminStaff("Sadia", 25000, 5000);

        Employee[] employees = {e1, e2, e3};

        for (Employee e : employees) {
            e.display();
        }
    }
}

```

## Key Points

- Upcasting = child object → parent reference

- It is automatic (no need to write extra syntax)

- Only parent class methods can be accessed (overridden methods behave dynamically)

- Child-specific methods cannot be accessed directly

---

## Summary

- Upcasting = treat child object as parent

- It helps in flexibility and runtime polymorphism

- Java decides method execution at runtime

---

# Downcasting 

## Definition

Downcasting means converting a parent class reference back into a child class object. It is used when you want to access child class-specific methods that are not available in the parent reference.

It is not automatic in Java, you must do it manually.

---

## Basic Idea

```text
Parent reference → Child object (converted back)
```

---

## When it is used

- After upcasting, when you need child-specific features

- To access methods that exist only in child class

---

## Code Example:

```java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }

    void breed() {
        System.out.println("Labrador");
    }
}

public class Main {
    public static void main(String[] args) {

        Animal obj = new Dog(); // Upcasting

        Dog d = (Dog) obj; // Downcasting

        d.sound();  // Dog version
        d.breed();  // now accessible (child method)
    }
}
```

---

## Important Points

- Downcasting must be done manually using `(ChildClass)`

- It works only if object is originally a child object

- It allows access to child-specific methods

- If done wrongly, it can cause runtime error (`ClassCastException`)

---

## Summary

- Upcasting = safe, automatic (child → parent)

- Downcasting = manual, risky (parent → child)

- Downcasting is used to get back child features after upcasting

---

# Upcasting vs Downcasting in Java

| Feature | Upcasting | Downcasting |
|---|---|---|
| Meaning | Child object is treated as parent object | Parent reference is converted back to child object |
| Direction | Child → Parent | Parent → Child |
| Type conversion | Automatic | Manual (needs casting) |
| Syntax | No extra syntax needed | `(ChildClass)` casting required |
| Safety | Safe | Risky (may cause runtime error) |
| Access | Only parent class methods can be accessed | Child class specific methods can be accessed |
| Polymorphism use | Used in runtime polymorphism | Used to regain child features after upcasting |
| Error chance | No runtime error | Can cause `ClassCastException` |

---

