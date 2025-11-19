# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to check if an element is present **more than once** in an array.  
If any number appears more than once, print **"Yes"**, otherwise print **"No"**.

---

## AIM:
To write a Java program that detects duplicate elements in an array using a HashSet.

---

## ALGORITHM :
1. Start the program.  
2. Read the size of the array **n** from the user.  
3. Read **n** elements into the array.  
4. Create a `HashSet` to store unique elements.  
5. Traverse the array:  
   - If an element is already in the set → a duplicate exists.  
   - Otherwise, add the element to the set.  
6. Print **"Yes"** if a duplicate is found; otherwise print **"No"**.  
7. End the program.

---

## PROGRAM:
```
/*
Program to check if an array contains duplicate elements
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

        int n = sc.nextInt();
        int[] arr = new int[n];

        for(int i = 0; i < arr.length; i++){
            arr[i] = sc.nextInt();
        }

        HashSet<Integer> set = new HashSet<>();
        boolean dup = false;

        for(int num : arr){
            if(set.contains(num)){
                dup = true;
                break;
            }
            set.add(num);
        }

        if(dup)
            System.out.print("Yes");
        else
            System.out.print("No");
    }
}
```

---

## OUTPUT:
<img width="367" height="664" alt="image" src="https://github.com/user-attachments/assets/2a1b242d-a08a-4be5-9acd-cd3084442a6a" />


---

## RESULT:
Thus, the Java program successfully checks whether an array contains duplicate elements using a HashSet.
