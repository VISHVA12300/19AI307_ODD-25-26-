# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores input strings into a String array and prints each string in **uppercase**.  
However, a **NullPointerException** occurs.

**Question:**  
What should you check in your array before calling `.toUpperCase()` on an element?

---

## AIM:
To understand and demonstrate how to safely handle `null` values in a String array before calling methods like `.toUpperCase()`.

---

## ALGORITHM :
1. Start the program.  
2. Read input from the user.  
3. Convert the input to `null` if the user types `"null"`.  
4. Before calling `.toUpperCase()`, check whether the string is `null`.  
5. If it is not null, convert it to uppercase.  
6. If it is null, catch the exception or print a message.  
7. End the program.

---

## PROGRAM:
```
/*
Program to demonstrate NullPointerException handling in String array elements
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.Scanner;

public class NullPointerArrayExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String input = sc.next();
        String str = input.equalsIgnoreCase("null") ? null : input;

        try {
            System.out.println(str.toUpperCase());
        } catch (NullPointerException e) {
            System.out.println("Null element");
        }

        sc.close();
    }
}
```

---

## **ANSWER (Important):**
Before calling `.toUpperCase()` on an array element, you must check:

```
if (array[i] != null)
```

Because calling any method (like `.toUpperCase()`) on a **null reference** causes a **NullPointerException**.

---

## OUTPUT:
<img width="532" height="246" alt="image" src="https://github.com/user-attachments/assets/070e7207-75f8-412a-b9fc-da91b3845b5e" />


---

## RESULT:
Thus, the program demonstrates why you must check for `null` before calling methods on String objects to avoid `NullPointerException`.
