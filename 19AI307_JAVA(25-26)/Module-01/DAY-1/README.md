# Ex.No:1(B) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is entering a battle arena tournament, but only heroes who meet specific power and skill criteria are allowed inside.

To enter the arena, she must satisfy **any one** of the following conditions:

- Her power level is above 80 **and** her rank is above 5  
  → `(power > 80 && rank > 5)`

**OR**

- She has a magic orb **and** her experience is at least 3 years  
  → `(hasMagicOrb == true && experience >= 3)`

If either of the above conditions is true, Lovely is allowed to enter the arena.

**Input Format:**
1. int power  
2. int rank  
3. boolean hasMagicOrb  
4. int experience  

**Output Format:**  
`Can Enter Arena: true/false`

---

## AIM:
To write a Java program that uses logical operators to determine whether a hero (Lovely) is eligible to enter the arena based on given conditions.

---

## ALGORITHM :
1. Start the program.  
2. Read the input values: power, rank, hasMagicOrb, and experience.  
3. Check Condition 1: power > 80 AND rank > 5.  
4. Check Condition 2: hasMagicOrb is true AND experience ≥ 3.  
5. Combine both conditions using the logical OR operator.  
6. Print whether Lovely can enter the arena.  
7. End the program.

---

## PROGRAM:
```
/*
Program to check arena eligibility using logical operators
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
        int pow=sc.nextInt();
        int rank=sc.nextInt();
        boolean hm=sc.nextBoolean();
        int ex=sc.nextInt();
        if(pow>80 && rank>5)
        System.out.println("Can Enter Arena: true");
        else if(hm==true && ex>=3)
        System.out.println("Can Enter Arena: true");
        else
        System.out.println("Can Enter Arena: false");
    }
}
```

---

## OUTPUT:
<img width="1192" height="580" alt="image" src="https://github.com/user-attachments/assets/ffb1a20d-b6eb-474f-9d5b-d728396221fe" />


---

## RESULT:
Thus, the Java program using logical operators to determine Lovely’s arena eligibility was successfully executed.
