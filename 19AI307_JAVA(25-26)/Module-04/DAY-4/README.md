# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create a program that loads an **Operating System Shell** using the **Factory Pattern**.

Based on user input, return the corresponding shell object:
- `"windows"` → WindowsShell  
- `"linux"` → LinuxShell  
- `"mac"` → MacShell  

If the user enters `"exit"`, stop the program.

If an invalid OS name is entered, print:
```
Invalid OS: <os>
```

---

## AIM:
To implement the **Factory Design Pattern** in Java to dynamically create shell objects based on operating system input.

---

## ALGORITHM :
1. Start the program.  
2. Define a `Shell` interface with a `launch()` method.  
3. Create shell classes (`WindowsShell`, `LinuxShell`, `MacShell`) that implement the interface.  
4. Create a `ShellFactory` class with a `getShell()` method that returns the correct shell object based on input.  
5. In the main method, repeatedly read OS names from user input.  
6. On each OS name:  
   - If `"exit"`, terminate.  
   - If OS has changed, request shell object from factory.  
   - Launch the shell if valid; otherwise show error.  
7. End the program.

---

## PROGRAM:
```
/*
Program to load OS shells using Factory Pattern
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.Scanner;

interface Shell {
    void launch();
}

class WindowsShell implements Shell {
    public void launch() {
        System.out.println("Launching Windows Shell...");
    }
}

class LinuxShell implements Shell {
    public void launch() {
        System.out.println("Launching Linux Shell...");
    }
}

class MacShell implements Shell {
    public void launch() {
        System.out.println("Launching Mac Shell...");
    }
}

class ShellFactory {
    public static Shell getShell(String os) {
        if (os.equalsIgnoreCase("windows"))
            return new WindowsShell();
        else if (os.equalsIgnoreCase("linux"))
            return new LinuxShell();
        else if (os.equalsIgnoreCase("mac"))
            return new MacShell();
        else
            return null;
    }
}

public class Main {
    private static String last = "";

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        while (sc.hasNextLine()) {
            String os = sc.nextLine().trim();

            if (os.equalsIgnoreCase("exit")) break;

            if (!os.equals(last)) {
                Shell s = ShellFactory.getShell(os);
                if (s == null) {
                    System.out.println("Invalid OS: " + os);
                } else {
                    s.launch();
                }
                last = os;
            }
        }

        sc.close();
    }
}
```

---

## OUTPUT:
<img width="610" height="308" alt="image" src="https://github.com/user-attachments/assets/24c55cae-aafb-4e2c-a86d-ecbbf1c3cd06" />


---

## RESULT:
Thus, the Java program successfully implements the **Factory Pattern** to dynamically load OS shell objects based on user input.
