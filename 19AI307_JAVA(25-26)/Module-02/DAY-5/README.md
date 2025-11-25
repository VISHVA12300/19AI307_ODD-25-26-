# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Define a class **Game** with a **static variable** `maxScore = 500`.  
Print the max score using **three different object references**.  
Then change the value of `maxScore` to **800** through one object, and again print the value using the three references to show that static variables are shared among all objects.

---

## AIM:
To demonstrate the concept of static variables in Java and show that they belong to the class, not individual objects.

---

## ALGORITHM :
1. Start the program.  
2. Create a class **Game** with a static integer variable `maxScore = 500`.  
3. Create three objects of the Game class.  
4. Print `maxScore` using each of the three object references.  
5. Modify `maxScore` to 800 using one object.  
6. Print `maxScore` again using all three objects to show the updated value.  
7. End the program.

---

## PROGRAM:
```
/*
Program to demonstrate static variable behavior
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.*;

class Game {
    static int maxScore = 500;
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Game g1 = new Game();
        Game g2 = new Game();
        Game g3 = new Game();

        System.out.println(g1.maxScore);
        System.out.println(g2.maxScore);
        System.out.println(g3.maxScore);

        g2.maxScore = 800;

        System.out.println(g1.maxScore);
        System.out.println(g2.maxScore);
        System.out.println(g3.maxScore);
    }
}
```

---

## OUTPUT:
<img width="294" height="284" alt="image" src="https://github.com/user-attachments/assets/6b62334a-b741-498f-ab94-9b1dddc41f8a" />


---

## RESULT:
Thus, the program successfully demonstrates that static variables are shared among all objects, and modifying the value through one object updates it for all.
