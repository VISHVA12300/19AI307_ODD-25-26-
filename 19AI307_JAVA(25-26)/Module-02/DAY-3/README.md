# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called **Rectangle** with **private** instance variables `length` and `width`.  
Provide **public getter and setter** methods to access and modify these variables.  
Also include a method to calculate the area of the rectangle.

---

## AIM:
To write a Java program that demonstrates encapsulation by using private variables with public getter and setter methods in a class.

---

## ALGORITHM :
1. Start the program.  
2. Create a class **Rectangle** with private variables `length` and `width`.  
3. Provide public getter and setter methods for both variables.  
4. Create a method `calculateArea()` that returns `length * width`.  
5. In the main method, take input for length and width from the user.  
6. Use setter methods to store values inside the object.  
7. Print the values using getter methods.  
8. End the program.

---

## PROGRAM:
```
/*
Program to demonstrate encapsulation using getters and setters
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.Scanner;

class Rectangle {
    // Private instance variables
    private double length;
    private double width;

    // Getter and Setter for length
    public double getLength() {
        return length;
    }
    public void setLength(double length) {
        this.length = length;
    }

    // Getter and Setter for width
    public double getWidth() {
        return width;
    }
    public void setWidth(double width) {
        this.width = width;
    }

    // Method to calculate area
    public double calculateArea() {
        return length * width;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Rectangle rect = new Rectangle();

        double len = sc.nextDouble();
        rect.setLength(len);

        double wid = sc.nextDouble();
        rect.setWidth(wid);

        System.out.println("Length: " + rect.getLength());
        System.out.println("Width: " + rect.getWidth());
    }
}
```

---

## OUTPUT:
<img width="521" height="374" alt="image" src="https://github.com/user-attachments/assets/6b4291ad-6263-4309-8e66-4dca349280b2" />


---

## RESULT:
Thus, the Java program successfully demonstrates encapsulation by using private instance variables with public getter and setter methods.
