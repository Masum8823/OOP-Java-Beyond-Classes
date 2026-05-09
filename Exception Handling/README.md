# Exception Handling

## Definition

Exception handling in Java is a way to handle runtime errors so that the program does not stop suddenly. It allows the program to continue execution even if an error occurs.

---

## Basic Idea

```text
If an error happens → Java handles it → program continues
```

---

## Main Keywords

- `try` → code that may cause error

- `catch` → handles the error

- `finally` → always runs (optional)

- `throw` → manually create exception

- `throws` → declares exception

---

## Simple Example

```java
public class Main {
    public static void main(String[] args) {

        try {
            int a = 10;
            int b = 0;

            int result = a / b; // error (divide by zero)
            System.out.println(result);
        }

        catch (ArithmeticException e) {
            System.out.println("Cannot divide by zero");
        }

        finally {
            System.out.println("Program finished");
        }
    }
}
```

---

### Simple Explanation

- `try` → risky code (division by zero)

- `catch` → handles error and shows message

- `finally` → always executes

---

## Why Exception Handling is used

- Prevents program crash

- Improves program stability

- Gives user-friendly error messages

- Helps in real-world applications

---

## Summary

- Exception = runtime error

- Handling = catching error and controlling program flow

- Java uses `try-catch` system

---