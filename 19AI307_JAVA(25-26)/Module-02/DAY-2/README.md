# Ex.No:2(B) METHODS

## QUESTION:
Write a method `void modifyValue(int num)` that attempts to modify the passed value by adding 10 and prints:

```
Inside method: <value>
```

Then, in `main()`, show that the **original value does NOT change**, proving Java uses **pass-by-value** for primitive types.

After calling the method, print:

```
Outside method: <value>
```

---

## AIM:
To demonstrate Java's pass-by-value behavior by showing that modifying a parameter inside a method does not affect the original variable.

---

## ALGORITHM :
1. Start the program.  
2. Read an integer `num` from the user.  
3. Call the method `modifyValue(num)`.  
4. Inside the method, add 10 to `num` and print the modified value.  
5. After returning to `main()`, print the original `num` to show it remains unchanged.  
6. End the program.

---

## PROGRAM:
```
/*
Program to demonstrate pass-by-value in Java
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.*;
public class main {

    public static void modifyValue(int num){
        num = num + 10;
        System.out.println("Inside method: " + num);
    }

    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);

        int num = sc.nextInt();

        modifyValue(num);

        System.out.println("Outside method: " + num);
    }
}
```

---

## OUTPUT:
<img width="582" height="184" alt="image" src="https://github.com/user-attachments/assets/f0bf5511-f023-4e2a-ba35-4423235f19be" />


---

## RESULT:
Thus, the program successfully demonstrates that primitive data types in Java are passed by value, and modifying them inside a method does not affect the original value.
