# Introduction to Java OOP (Object-Oriented Programming)

Java OOP means writing programs using **“objects”** instead of just step-by-step instructions.

In real life, we see everything as objects. For example, a car, a student, or a mobile phone. Each object has:

- **Properties (data)** → like color, size, name  
- **Actions (behavior)** → like start, stop, study, call  

Java OOP works the same way.


### What is OOP in Java?

OOP (Object-Oriented Programming) in Java is a way of programming where we organize code using **classes and objects**.

- A **Class** is like a blueprint (design)  
- An **Object** is a real thing made from that blueprint  


### Example

- Class: Car design  
- Object: Your actual car (Toyota, BMW, etc.)

---

# Main Features of Java OOP


### 1. Class and Object

- **Class = design**
- **Object = real example**

👉 A class is a blueprint, and an object is created from it.



### 2. Encapsulation

It means **hiding data and protecting it**.

Only allowed methods can access the data.

#### Example:
ATM card PIN is hidden.



### 3. Inheritance

One class can use properties of another class.

#### Example:

- Parent class: Animal  
- Child class: Dog (Dog gets features of Animal)


### 4. Polymorphism

One thing can behave in different ways.

#### Example:

A person can be a student, a player, or a teacher.



### 5. Abstraction

Showing only important things and hiding details.

#### Example:

You drive a car without knowing how engine works.

---

## Why Java OOP is useful?

Java OOP is useful because it makes programming easier, cleaner, and more powerful for real-world applications.



### Key Reasons

- Makes code easy to manage  
- Reusable code (write once, use many times)  
- Easy to understand and maintain  
- Helps in building real software systems  


#### Simple Summary

Java OOP helps developers write **organized, reusable, and real-world friendly code**.

----

# Working of Class and Objects in Java 
In Java, **Class and Object** work together to build programs in an organized way.


## 1. What is a Class?

A Class is like a **blueprint or design**.

It does not occupy memory by itself. It only defines:

- what data (variables) will be stored  
- what actions (methods) can be done  

#### Example idea:

A car design paper is a class. It tells how a car should be, but it is not a real car.



## 2. What is an Object?

An Object is a **real instance of a class**.

When we create an object:

- Memory is allocated  
- We can use data and methods  

#### Example idea:

A real Toyota car built from the car design is an object.

---

#  How Class and Object Work Together

#### Step-by-step working:

- We define a class (blueprint)  
- We create objects from that class  
- Objects use variables and methods defined in the class  

---

## Simple Java Example

```java
class Student {
    String name;
    int age;

    void showInfo() {
        System.out.println(name + " " + age);
    }
}

public class Main {
    public static void main(String[] args) {

        Student s1 = new Student();  // object creation

        s1.name = "Rahim";
        s1.age = 20;

        s1.showInfo();
    }
}
```

#### Explanation of Example

- `Student` = Class (blueprint)  
- `s1` = Object  
- `new Student()` = creates memory for object  
- `s1.name` = accessing variable  
- `s1.showInfo()` = calling method  

---

# TRICKY EXAM QUESTIONS (Class & Object)


#### 1. What happens if we don’t create any object of a class?

**Answer:**  
No memory is allocated for variables and methods (except static members).



#### 2. Can a class exist without an object?

**Answer:**  
Yes  

But it has no active memory usage unless an object is created.



#### 3. How many objects are created here?

```java
Student s1 = new Student();
Student s2 = new Student();
Student s3 = new Student();
```

**Answer:** 3 objects



#### 4. Do all objects share same memory?

**Answer:**  
No  

Each object has its own separate memory.



#### 5. Output prediction

```java
class Test {
    int x = 10;

    void show() {
        System.out.println(x);
    }

    public static void main(String[] args) {
        Test t1 = new Test();
        Test t2 = new Test();

        t1.x = 20;

        t1.show();
        t2.show();
    }
}
```

**Answer:**
```text
20
10
```

**Explanation:**
- `t1` and `t2` are separate objects  
- Changing `t1.x` does NOT affect `t2.x`  



#### 6. Trick: What is output?

```java
class A {
    int a = 5;

    public static void main(String[] args) {
        A obj = new A();
        System.out.println(obj.a);
    }
}
```

**Answer:**
```text
5
```


#### 7. Can we create object without class?

**Answer:** No  

Class is required to create an object.



### 8. What is stored inside an object?

**Answer:**
- Instance variables  
- Not methods (methods are shared in memory)


#### 9. Trick Question

If 5 objects are created, how many copies of method exist?

**Answer:** 1 copy (shared)


#### 10. What is wrong here?

```java
Student.s1 = new Student();
```

**Answer:** Syntax error  

**Correct form:**
```java
Student s1 = new Student();
```



#### 11. Can two objects have same data?

**Answer:** Yes  

But they still have different memory locations.



#### 12. What happens when object is created?

**Answer:**

- Memory is allocated  
- Constructor runs automatically  
- Object becomes active  

---