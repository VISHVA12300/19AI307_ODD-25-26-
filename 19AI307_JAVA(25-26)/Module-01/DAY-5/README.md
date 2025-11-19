# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to convert a given **camelCase** string into **snake_case**.

Example:  
`helloWorld` → `hello_world`  
`mySampleText` → `my_sample_text`

---

## AIM:
To write a Java program that converts camelCase formatted text into snake_case using regular expressions.

---

## ALGORITHM :
1. Start the program.  
2. Read a camelCase string from the user.  
3. Identify places where a lowercase letter is followed by an uppercase letter.  
4. Insert an underscore `_` between them using `replaceAll()`.  
5. Convert the entire string to lowercase.  
6. Print the final snake_case string.  
7. End the program.

---

## PROGRAM:
```
/*
Program to convert camelCase to snake_case
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.*;
public class main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String s = sc.nextLine();

        String sn = s.replaceAll("([a-z])([A-Z])", "$1_$2").toLowerCase();

        System.out.print("snake_case: " + "_" + sn);
    }
}
```

---

## OUTPUT:
<img width="728" height="241" alt="image" src="https://github.com/user-attachments/assets/f32c4617-3235-4768-b33b-abb7a3e5ae01" />


---

## RESULT:
Thus, the Java program successfully converts a camelCase string into snake_case using regular expressions.
