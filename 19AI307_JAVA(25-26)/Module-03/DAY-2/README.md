# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program using **method overloading** to print student details.  
Create a class **Student** (here implemented as class `prog`) with the following overloaded methods:

- `print(String name)`  
- `print(String name, int age)`  
- `print(String name, int age, String dept)`

Use different method calls to print details with increasing information.

---

## AIM:
To write a Java program that demonstrates **method overloading** by defining multiple print methods with different parameter lists to display student details.

---

## ALGORITHM :
1. Start the program.  
2. Create a class with three overloaded `print()` methods:  
   - One that prints just the student name  
   - One that prints name and age  
   - One that prints name, age, and department  
3. In `main()`, read input values for each case separately.  
4. Call the appropriate overloaded method based on the number of arguments.  
5. Display the student details accordingly.  
6. End the program.

---

## PROGRAM:
```
/*
Program to demonstrate method overloading for student details
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.Scanner;

class prog {

    // Overloaded methods
    void print(String name) {
        System.out.println("Name: " + name);
    }

    void print(String name, int age) {
        System.out.println("Name: " + name + ", Age: " + age);
    }

    void print(String name, int age, String dept) {
        System.out.println("Name: " + name + ", Age: " + age + ", Dept: " + dept);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        prog s = new prog();

        // For first call
        String name = sc.nextLine();
        s.print(name);

        // For second call
        String name2 = sc.nextLine();
        int age = sc.nextInt();
        s.print(name2, age);

        sc.nextLine(); // consume leftover newline

        // For third call
        String name3 = sc.nextLine();
        int age3 = sc.nextInt();
        sc.nextLine(); // consume leftover newline
        String dept = sc.nextLine();
        s.print(name3, age3, dept);

        sc.close();
    }
}
```

---

## OUTPUT:
<img width="818" height="602" alt="image" src="https://github.com/user-attachments/assets/943ce835-5f5d-4a97-9a17-566f4d571fc8" />


---

## RESULT:
Thus, the Java program successfully demonstrates **method overloading** by printing student details using multiple versions of the `print()` method.
