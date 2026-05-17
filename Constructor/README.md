# Constructor in Java (Easy Explanation)

A constructor is a special type of method in Java that is used to initialize objects.

When you create an object, the constructor runs automatically.

---

# 1. What is Constructor?

A constructor:

- Has the same name as the class  
- Has no return type (not even `void`)  
- Runs automatically when object is created  

---

# 2. Why Constructor is Used?

It is used to:

- Initialize variables  
- Set default values  
- Prepare object for use  

---

# Example

```java
class Student {
    String name;
    int age;

    // Constructor
    Student() {
        name = "Unknown";
        age = 0;
    }

    void show() {
        System.out.println(name + " " + age);
    }
}

public class Main {
    public static void main(String[] args) {

        Student s1 = new Student(); // constructor runs automatically
        s1.show();
    }
}
```

---

# Output

```text
Unknown 0
```

---

# 6. Key Points

- Constructor runs automatically  
- Used for object initialization  
- Same name as class  
- No return type  
- Can be overloaded (multiple constructors)  

---

# 7. Real-Life Example

Think like this:

- **Class** = Mobile design  
- **Constructor** = Initial setup (battery full, settings ready)  
- **Object** = Actual mobile you use  

---

# Constructor vs Method in Java (Easy Differences)

Both constructor and method are used inside a class, but they are not the same.

---

# 1. Basic Meaning

- **Constructor**: Used to initialize an object  
- **Method**: Used to perform actions or tasks  

---

# 2. Key Differences

| Feature | Constructor | Method |
|---|---|---|
| Purpose | Initialize object | Perform operations |
| Name | Same as class name | Any valid name |
| Return type | No return type (not even `void`) | Must have return type |
| Call | Automatically called | Must be called manually |
| Frequency | Called once per object creation | Can be called multiple times |
| Inheritance | Not inherited | Can be inherited |
| Overloading | Can be overloaded | Can be overloaded |

---

# 3. Example

## Constructor Example:

```java
class Student {
    String name;

    Student() {   // constructor
        name = "Unknown";
    }
}
```

👉 Runs automatically when object is created

---

## Method Example:

```java
class Student {
    String name;

    void show() {   // method
        System.out.println(name);
    }
}
```

👉 Must be called like:

```java
s1.show();
```

---

# 4. Simple Understanding

- Constructor = “Object setup system”  
- Method = “Work doing system”  

---

# 5. Real-Life Example

| Real Life | Constructor | Method |
|---|---|---|
| Mobile | Initial setup (language, time) | Calling, messaging |
| Student | Assign initial data | Studying, playing |

---