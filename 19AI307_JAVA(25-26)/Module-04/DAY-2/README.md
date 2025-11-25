# Ex.No:4(B) IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM

## QUESTION:
At an international airport, there is **only one Radar Control Tower** that handles all flight communications.  
Regardless of how many flights are arriving, **every flight must contact the same tower instance**.

If multiple tower objects were created, it could lead to inconsistent instructions — a major aviation safety issue.

Your task is to simulate this using the **Singleton Design Pattern**.

### Key Requirements:
- Only **one instance** of `RadarControlTower` should ever exist.
- All flights must communicate using this single instance.
- Each flight should register its name.
- Log the **order of registration**.

### Input Format:
- First line: integer `n` → number of incoming flights  
- Next `n` lines: each line contains a flight name  

### Output Format:
For each flight:
```
[FlightName] registered with Radar Control Tower. Total Flights: [count]
```

---

## AIM:
To implement the **Singleton Pattern** in Java and simulate a centralized Radar Control Tower where all flights use the same shared instance to register their approach.

---

## ALGORITHM :
1. Start the program.  
2. Create a class `RadarControlTower` with:  
   - a private static instance variable  
   - a private constructor  
   - a public `getInstance()` method returning the same instance  
3. Maintain a counter to track number of registered flights.  
4. In the main method:  
   - Read the number of incoming flights  
   - For each flight, get the singleton instance of the tower  
   - Register the flight and print the total registration count  
5. End the program.

---

## PROGRAM:
```
/*
Program to simulate a Radar Control Tower using the Singleton pattern
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.*;

class RadarControlTower {
    private static RadarControlTower instance;
    private int flightCount = 0;

    private RadarControlTower() {}

    public static RadarControlTower getInstance() {
        if (instance == null) {
            instance = new RadarControlTower();
        }
        return instance;
    }

    public int registerFlight(String flightName) {
        flightCount++;
        return flightCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        sc.nextLine();  // consume leftover newline

        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance();
            int total = tower.registerFlight(flight);

            System.out.println(
                flight + " registered with Radar Control Tower. Total Flights: " + total
            );
        }
    }
}
```

---

## OUTPUT:
<img width="1191" height="242" alt="image" src="https://github.com/user-attachments/assets/7d3fa494-c35f-4c8a-ba98-44cc2f8a1c51" />


---

## RESULT:
Thus, the program successfully implements the **Singleton Pattern** to ensure that all flights communicate with one and only one Radar Control Tower instance.
