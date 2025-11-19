# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to calculate the factorial of a number using a **for loop**.  
The factorial of a number **n** is the product of all positive integers from **1 to n**.

Example:  
5! = 1 × 2 × 3 × 4 × 5 = 120

---

## AIM:
To write a Java program using a for loop to compute the factorial of a given number.

---

## ALGORITHM :
1. Start the program.  
2. Read an integer **n** from the user using the Scanner class.  
3. Initialize a variable `fact` to 1.  
4. Use a **for loop** from 1 to n and multiply each value with `fact`.  
5. After the loop ends, print the factorial value.  
6. End the program.

---

## PROGRAM:
```
/*
Program to calculate factorial of a number using for loop
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.*;
public class main {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int fact = 1;

        for(int i = 1; i <= n; i++){
            fact *= i;
        }

        System.out.print("Factorial of " + n + " is: " + fact);
    }
}
```

---

## OUTPUT:
<img width="753" height="255" alt="image" src="https://github.com/user-attachments/assets/771ee4d2-64e9-462a-8cfe-69b67ef09f30" />


---

## RESULT:
Thus, the Java program to compute the factorial of a number using a for loop was successfully executed.
