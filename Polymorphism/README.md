# Polymorphism 

## Definition:
Polymorphism in Java means **one name, many forms**. It allows a single method, object, or operator to behave in different ways depending on the situation.

---

## Simple Idea:

- Same action can behave differently  
- One method name can do different tasks  
- One object reference can show different behaviors  

---

## Types of Polymorphism:

### 1. Compile-Time Polymorphism (Method Overloading)
- Same method name with different parameters  
- Decision is made at compile time  

**Example idea:**
- add(2, 3)
- add(2, 3, 4)

---

### 2. Runtime Polymorphism (Method Overriding)
- Same method in parent and child class  
- Decision is made at runtime  
- Achieved using inheritance  

**Example idea:**
- Animal → sound()
- Dog → sound() (barks)
- Cat → sound() (meows)

---

## Key Understanding:

- Polymorphism increases flexibility  
- Same interface/method behaves differently  
- Reduces code complexity  
- Supports reusability  

---

## Real-Life Example:

- A person can be:
  - Student in school  
  - Employee in office  
  - Customer in shop  

Same person, different roles → polymorphism

---

##  Summary:

- Polymorphism = one thing, many behaviors  
- Two types: compile-time and runtime  
- Helps make Java code flexible and reusable  

---

# Compile-Time Errors 

Compile-time errors are mistakes that Java detects before running the program.

---

## 1. Syntax error

- Missing semicolon `;`

- Wrong brackets `{ }`

👉 Example:

```java
System.out.println("Hello") ❌
```

(missing `;`)

---

## 2. Undeclared variable

- Using a variable that is not declared

👉 Example:

```java
System.out.println(x); ❌
```

(`x` not defined)

---

## 3. Type mismatch

- Wrong data type assignment

👉 Example:

```java
int x = "Hello"; ❌
```

---

## 4. Missing method or wrong method name

- Calling a method that does not exist

👉 Example:

```java
obj.showw(); ❌
```

(method not defined)

---

## 5. Access violation

- Trying to access private members from outside class

👉 Example:

```java
obj.privateMethod(); ❌
```

---

## 6. Wrong class reference

- Using class that is not imported or not present

👉 Example:

```java
Scanner sc = new Scanner(System.in); ❌
```

(if `Scanner` not imported)

---

### Summary

- ❌ Compile-time error → detected before running (syntax, type, declaration mistakes)

- ❌ Divide by zero → NOT compile-time, it is runtime error

---

# Runtime Errors 

## Definition

Runtime errors are errors that occur during program execution (after compilation). The program compiles successfully but crashes or behaves abnormally when running.

---

## 1. Divide by zero

- Happens when a number is divided by `0`

👉 Example idea:

```java
10 / 0
```

→ `ArithmeticException`

---

## 2. Array index out of bounds

- Accessing array position that does not exist

👉 Example idea:

```java
Array size = 3, but accessing index 5
```

→ `ArrayIndexOutOfBoundsException`

---

## 3. Null pointer exception

- Using an object that has no value (`null`)

👉 Example idea:

```java
String s = null;
s.length();
```

→ `NullPointerException`

---

## 4. Input mismatch

- Giving wrong type of input

👉 Example idea:

```java
Expecting integer but giving text
```

→ `InputMismatchException`

---

## 5. Class cast exception

- Wrong type conversion between objects

👉 Example idea:

```java
Converting parent object into wrong child type
```

→ `ClassCastException`

---

# Overloading vs Overriding 

---

## Feature Comparison Table:

| Feature | Method Overloading | Method Overriding |
|----------|-------------------|-------------------|
| **Meaning** | Same method name with different parameters | Same method name with same parameters in parent and child class |
| **Class relation** | Happens in same class | Happens in inheritance (parent-child) |
| **Parameters** | Must be different | Must be exactly same |
| **Return type** | Can be same or different | Must be same (or compatible) |
| **Polymorphism type** | Compile-time polymorphism | Runtime polymorphism |
| **Decision time** | Decided at compile time | Decided at runtime |
| **Inheritance needed** | Not required | Required |
| **Purpose** | Increase method flexibility | Change behavior of parent method |

---

## Simple Idea:

- **Overloading = same name, different input (same class)**  
- **Overriding = same name, same input (parent-child change behavior)**  