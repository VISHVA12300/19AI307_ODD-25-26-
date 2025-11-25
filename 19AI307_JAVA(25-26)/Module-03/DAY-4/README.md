# Ex.No:3(D) INTERFACE

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface **WeatherBot** and return a prediction.

### Bot Types:
- **SunBot**  
  Predicts:  
  - "HOT" if temperature > 30  
  - "MODERATE" otherwise  

- **RainBot**  
  Predicts:  
  - "COLD" if temperature < 20  
  - "WARM" otherwise  

### Input:
1. temperature  
2. botType  
   - 1 → SunBot  
   - 2 → RainBot

### Output:
A prediction string.

---

## AIM:
To write a Java program that demonstrates **interfaces** and **runtime polymorphism** by creating weather prediction bots with different prediction logic.

---

## ALGORITHM :
1. Start the program.  
2. Define an interface **WeatherBot** with method `predict(int temperature)`.  
3. Implement the interface in **SunBot** and **RainBot** classes with their respective prediction rules.  
4. In `main()`, read temperature and bot type from the user.  
5. Use the bot type to create the appropriate bot object.  
6. Call the `predict()` method polymorphically.  
7. Print the prediction.  
8. End the program.

---

## PROGRAM:
```
/*
Program to demonstrate interface-based weather prediction bots
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.*;

interface WeatherBot {
    String predict(int temperature);
}

class SunBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature > 30) return "HOT";
        return "MODERATE";
    }
}

class RainBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature < 20) return "COLD";
        return "WARM";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        WeatherBot bot;

        if (botType == 1)
            bot = new SunBot();
        else
            bot = new RainBot();

        System.out.println(bot.predict(temperature));
    }
}
```

---

## OUTPUT:
<img width="341" height="154" alt="image" src="https://github.com/user-attachments/assets/94e800d1-b49a-4978-9e21-4a271dc997bf" />


---

## RESULT:
Thus, the program successfully demonstrates the use of **interfaces** and **polymorphism** to generate weather predictions using different bot types.
