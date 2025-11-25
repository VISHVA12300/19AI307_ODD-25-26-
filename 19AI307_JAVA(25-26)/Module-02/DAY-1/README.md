# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class **Course** with the following attributes:

- `code` → Course code (String)  
- `title` → Course title (String)  
- `credits` → Number of credits (int)

Read details of **two** courses from the user and print them in the format:
```
code | title | credits credits
```

---

## AIM:
To write a Java program that defines a class with attributes and uses objects to store and display course information.

---

## ALGORITHM :
1. Start the program.  
2. Create a class **Course** with attributes: code, title, and credits.  
3. In the main method, create a Scanner object to read input.  
4. Create two Course objects: `c1` and `c2`.  
5. Read course details (code, title, credits) for both objects.  
6. Display both course details in the required format.  
7. End the program.

---

## PROGRAM:
```
/*
Program to create Course class and display course details
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.Scanner;

class Course {
    String code;
    String title;
    int credits;
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Course c1 = new Course();
        c1.code = sc.next();
        c1.title = sc.next();
        c1.credits = sc.nextInt();

        Course c2 = new Course();
        c2.code = sc.next();
        c2.title = sc.next();
        c2.credits = sc.nextInt();

        System.out.println(c1.code + " | " + c1.title + " | " + c1.credits + " credits");
        System.out.println(c2.code + " | " + c2.title + " | " + c2.credits + " credits");

        sc.close();
    }
}
```

---

## OUTPUT:
<img width="848" height="253" alt="image" src="https://github.com/user-attachments/assets/faab137e-5c37-4141-968b-483771e7da06" />


---

## RESULT:
Thus, the Java program using a class to represent course details and displaying them was successfully executed.
