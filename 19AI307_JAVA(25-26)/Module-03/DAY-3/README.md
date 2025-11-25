# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create an abstract class **GameScore** with an abstract method `finalScore()`.

Two subclasses must extend it:

### **ArcadeGame**
```
score = baseScore + (level × 100)
```

### **PuzzleGame**
```
if attempts ≤ 3:
    score = 1000 - (attempts × 100)
else:
    score = 500
```

### **Input Format**
- First line: game type (1 → Arcade, 2 → Puzzle)  
- Second line:  
  - For ArcadeGame → `baseScore level`  
  - For PuzzleGame → `attempts`

### **Output Format**
Print the **final score (int)**.

---

## AIM:
To write a Java program demonstrating **abstract classes**, **method overriding**, and **runtime polymorphism** to compute final game scores for two different game types.

---

## ALGORITHM :
1. Start the program.  
2. Define an abstract class **GameScore** with abstract method `finalScore()`.  
3. Create subclass **ArcadeGame** that overrides `finalScore()` using formula:  
   `baseScore + level × 100`.  
4. Create subclass **PuzzleGame** that overrides `finalScore()` using attempt-based logic.  
5. In `main()`, read game type from the user.  
6. If type is 1, read `baseScore` and `level`.  
7. If type is 2, read `attempts`.  
8. Create the appropriate subclass object and assign it to a `GameScore` reference.  
9. Call `finalScore()` polymorphically and print the result.  
10. End the program.

---

## PROGRAM:
```
/*
Program to calculate game scores using abstract class and method overriding
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.Scanner;

// Abstract class
abstract class GameScore {
    abstract int finalScore();
}

// ArcadeGame subclass
class ArcadeGame extends GameScore {
    int baseScore;
    int level;

    @Override
    int finalScore() {
        return baseScore + (level * 100);
    }
}

// PuzzleGame subclass
class PuzzleGame extends GameScore {
    int attempts;

    @Override
    int finalScore() {
        if (attempts <= 3)
            return 1000 - (attempts * 100);
        else
            return 500;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();

        GameScore game;

        if (type == 1) {
            ArcadeGame ag = new ArcadeGame();
            ag.baseScore = sc.nextInt();
            ag.level = sc.nextInt();
            game = ag;
        } else if (type == 2) {
            PuzzleGame pg = new PuzzleGame();
            pg.attempts = sc.nextInt();
            game = pg;
        } else {
            System.out.println("Invalid game type");
            sc.close();
            return;
        }

        System.out.println(game.finalScore());
        sc.close();
    }
}
```

---

## OUTPUT:
<img width="415" height="213" alt="image" src="https://github.com/user-attachments/assets/61204a80-e741-462e-9450-2676673de093" />


---

## RESULT:
Thus, the program successfully implements **abstract classes**, **method overriding**, and **polymorphism** to compute scores for two different game types.
