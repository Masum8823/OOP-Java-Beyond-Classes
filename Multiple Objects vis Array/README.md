# Multiple Object Creation via Array 

## Idea

Instead of creating many objects one by one, we can store multiple objects in an array of objects. This helps to manage many objects easily.

---

## Concept

```text
Class Object Array → stores multiple objects
```

---

## Code Example

```java
import java.util.Scanner;

class Student {
    int id;
    String name;

    Student(int id, String name) {
        this.id = id;
        this.name = name;
    }

    void display() {
        System.out.println(id + " " + name);
    }
}

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // Array of objects
        Student[] s = new Student[3];

        // Creating objects using loop
        for (int i = 0; i < s.length; i++) {
            System.out.print("Enter ID: ");
            int id = sc.nextInt();

            sc.nextLine(); // clear buffer

            System.out.print("Enter Name: ");
            String name = sc.nextLine();

            s[i] = new Student(id, name); // object creation inside loop
        }

        // Display objects
        System.out.println("\nStudent Details:");
        for (int i = 0; i < s.length; i++) {
            s[i].display();
        }

        sc.close();
    }
}
```

---

### Simple Explanation

- Loop runs 3 times

- Each time, input is taken from user

- New object is created inside loop

- Object is stored in array

- Second loop prints all objects

---

### Key Points

- Objects can be created dynamically using loop

- Useful when number of objects is large or unknown

- Reduces manual coding

- Common in real applications (student list, employee system, etc.)

---

### Summary

- Loop → take input → create object → store in array

- Repeat process for multiple objects

- Easy and scalable approach

---

## Another Code Example:

```java
class A {
    private int x;

    A(int x) {
        this.x = x;
    }

    int f() {
        return x + 2;
    }
}

class B extends A {

    B(int x) {
        super(x);
    }

    int f() {
        return super.f() + 3;
    }
}

public class Main {

    public static void main(String[] a) {

        A[] arr = new A[5];

        for (int i = 0; i < arr.length; i++) {
            if (i % 2 == 0)
                arr[i] = new A(i);
            else
                arr[i] = new B(i);
        }

        int sum = 0;

        for (int i = 0; i < arr.length; i++) {
            int v = arr[i].f();
            sum = sum + v;
            System.out.println(v);
        }

        System.out.println(sum);
    }
}

```