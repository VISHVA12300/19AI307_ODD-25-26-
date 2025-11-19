# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
Aayush studies at Teswan National University. It is exam results time, and he hopes that his scores in 5 subjects could help him secure a scholarship for GRE preparation.

The university follows a **5-point grading system** (2 to 5):

- **2** → Fail (F grade)  
- Student **must not** fail any subject  
- Student **must score at least one 5** (full score)  
- Student must have a **grade point average (GPA) ≥ 4.0**

Given Aayush’s 5 subject scores, determine whether he will receive the scholarship.

**Input:** 5 integers (scores in 5 subjects)  
**Output:** `"yes"` if he receives the scholarship, otherwise `"no"`

---

## AIM:
To write a Java program that determines whether a student is eligible for a scholarship based on grading rules using conditional statements.

---

## ALGORITHM :
1. Start the program and read 5 subject scores from the user.  
2. Check if any score is equal to **2** → if yes, the student fails and is not eligible.  
3. Check if there is **at least one score of 5**.  
4. Compute the **average** of the 5 scores.  
5. Verify that the average is **≥ 4.0**.  
6. If all conditions are satisfied, print `"yes"`; otherwise print `"no"`.  
7. End the program.

---

## PROGRAM:
```
/*
Program to check scholarship eligibility based on grades
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.*;
public class main{
    public static void main(String[]args){
        Scanner sc=new Scanner(System.in);
        int s1=sc.nextInt();
        int s2=sc.nextInt();
        int s3=sc.nextInt();
        int s4=sc.nextInt();
        int s5=sc.nextInt();
        
        if(s1==2||s2==2||s3==2||s4==2||s5==2){
            System.out.print("no");
        }
        else if(s1!=5 && s2!=5 && s3!=5 && s4!=5 && s5!=5){
            System.out.print("no");
        }
        else{
            double avg=(s1+s2+s3+s4+s5)/5.0;
            if(avg<4.0){
                System.out.print("no");
            }
            else{
                System.out.print("yes");
            }
        }
    }
}
```


## OUTPUT:
```
<img width="469" height="212" alt="image" src="https://github.com/user-attachments/assets/cf50c8bb-f940-46f4-812d-5a8334f1413c" />


```

## RESULT:
Thus, the Java program successfully determines whether Aayush is eligible for the scholarship based on university grading rules.
