# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a Java program to create a class **Circle** that uses a **constructor** to calculate the area of a circle using the given radius.  
The program should read the radius, compute the area inside the constructor, and display it using a method.

---

## AIM:
To write a Java program that demonstrates constructor usage by calculating and displaying the area of a circle based on the radius provided by the user.

---

## ALGORITHM :
1. Start the program.  
2. Define a class **Circle** with instance variables `radius` and `area`.  
3. Create a **parameterized constructor** that:  
   - Accepts radius  
   - Stores it  
   - Calculates area using the formula: `area = π × r × r`  
4. Create a method `display()` to print the area.  
5. In the main method, read the radius from the user.  
6. Create a Circle object by passing the radius to the constructor.  
7. Call the `display()` method to print the result.  
8. End the program.

---

## PROGRAM:
```
/*
Program to calculate circle area using constructor
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.*;

class Circle {
    double radius;
    double area;

    Circle(double r) {
        radius = r;
        area = Math.PI * r * r;
    }

    void display() {
        System.out.printf("Area of the circle with radius %.2f is %.2f", radius, area);
    }
}

public class main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double r = sc.nextDouble();

        Circle c = new Circle(r);
        c.display();
    }
}
```

---

## OUTPUT:
<img width="1010" height="202" alt="image" src="https://github.com/user-attachments/assets/d7ab94d4-88a0-40d2-831b-9ce764f26f06" />


---

## RESULT:
Thus, the Java program successfully calculates the area of a circle using a constructor and displays the result.
