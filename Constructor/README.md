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