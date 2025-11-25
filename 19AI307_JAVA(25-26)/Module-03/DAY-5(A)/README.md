# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an **inner class** and access it from the **outer class**.  
The inner class should contain a method that prints a greeting message using a name given as input.

---

## AIM:
To write a Java program that demonstrates the concept of **inner classes** and shows how to create and access an inner class object from the outer class.

---

## ALGORITHM :
1. Start the program.  
2. Define an outer class `Main`.  
3. Inside the outer class, define a non-static inner class `Inner` with a method `greet()`.  
4. In the `main()` method:  
   - Read the user’s name  
   - Create an instance of the outer class  
   - Use it to create an instance of the inner class  
5. Call the `greet()` method of the inner class.  
6. End the program.

---

## PROGRAM:
```
/*
Program to demonstrate inner class access in Java
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.*;

public class Main {

    class Inner {
        void greet(String name) {
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();

        Main outer = new Main();        
        Main.Inner inner = outer.new Inner();

        inner.greet(name);
    }
}
```

---

## OUTPUT:
<img width="1146" height="246" alt="image" src="https://github.com/user-attachments/assets/b1c3702e-319d-4b40-af41-61ca77a4e628" />


---

## RESULT:
Thus, the Java program successfully demonstrates the creation and usage of an **inner class** from the **outer class**.
