# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to find the **square root** of a number using the **Double wrapper class**.

---

## AIM:
To write a Java program that demonstrates the use of the **Double wrapper class** along with the `Math.sqrt()` method to compute the square root of a given number.

---

## ALGORITHM :
1. Start the program.  
2. Read a number from the user using `Scanner`.  
3. Store the value in a `Double` wrapper object.  
4. Use `Math.sqrt()` to compute the square root.  
5. Print the original number and its square root.  
6. End the program.

---

## PROGRAM:
```
/*
Program to find square root using Double wrapper class
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        double num = sc.nextDouble();
        Double number = num;
        Double result = Math.sqrt(number);

        System.out.println("Square root of " + number + " is: " + result);
    }
}
```

---

## OUTPUT:
<img width="750" height="253" alt="image" src="https://github.com/user-attachments/assets/091dcce9-a21f-4654-b36a-a4c4185379d7" />


---

## RESULT:
Thus, the Java program successfully computes the square root of a number using the **Double wrapper class**.
