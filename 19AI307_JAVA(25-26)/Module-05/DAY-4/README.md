# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a Java program to **set the priority and name of the current threads**.  
Consider two threads `t1` and `t2`.

### Requirements:
- Read thread names from the user  
- Set priority of:
  - `t1` → **4**
  - `t2` → **2**
- Display thread information

---

## AIM:
To write a Java program that demonstrates how to set and display **thread names** and **thread priorities**.

---

## ALGORITHM :
1. Start the program.  
2. Read two thread names from the user.  
3. Create two Thread objects: `t1` and `t2`.  
4. Assign user-provided names to both threads using `setName()`.  
5. Set priorities:
   - `t1.setPriority(4)`  
   - `t2.setPriority(2)`  
6. Print thread information using `System.out.println(thread)`.  
7. End the program.

---

## PROGRAM:
```
/*
Program to set thread name and priority for two threads
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.Scanner;

public class ThreadPriorityNameExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name1 = sc.nextLine();
        String name2 = sc.nextLine();

        // Create thread t1
        Thread t1 = new Thread();
        t1.setName(name1);
        t1.setPriority(4);

        // Create thread t2
        Thread t2 = new Thread();
        t2.setName(name2);
        t2.setPriority(2);

        System.out.println(t1);
        System.out.println(t2);

        sc.close();
    }
}
```

---

## OUTPUT:
<img width="879" height="244" alt="image" src="https://github.com/user-attachments/assets/4ad5487e-4c81-42a5-aa89-5e25e4eb5c4c" />


---

## RESULT:
Thus, the program successfully sets and displays the **name** and **priority** of two threads.
