# Ex.No:5(C) FILE HANDLING USING JAVA

## QUESTION:
Ask the user for **name**, **age**, and **email address**.  
Write the collected data into a file named **userdata.txt** in a clean structured format, then read the file and display its contents.

---

## AIM:
To write a Java program that collects user information, writes it into a file using `FileWriter`, and then reads and prints the stored data using `BufferedReader`.

---

## ALGORITHM :
1. Start the program.  
2. Read **name**, **age**, and **email** from the user.  
3. Create a file named `userdata.txt`.  
4. Write structured user data into the file using `FileWriter`.  
5. Close the writer to save data.  
6. Open the file with `BufferedReader` and read its contents line by line.  
7. Print the contents to the console.  
8. Handle I/O exceptions appropriately.  
9. End the program.

---

## PROGRAM:
```
/*
Program to collect user data and write it to a file
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.io.*;
import java.util.*;

public class UserDataCollector {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String fileName = "userdata.txt";

        try {
            String name = scanner.nextLine();
            int age = scanner.nextInt();
            scanner.nextLine(); // consume newline
            String email = scanner.nextLine();

            // Step 2: Write to file
            FileWriter writer = new FileWriter(fileName);
            writer.write("User Information\n");
            writer.write("================\n");
            writer.write("Name  : " + name + "\n");
            writer.write("Age   : " + age + "\n");
            writer.write("Email : " + email + "\n");
            writer.close();

            BufferedReader reader = new BufferedReader(new FileReader(fileName));
            String line;
            while ((line = reader.readLine()) != null) {
                System.out.println(line);
            }
            reader.close();

        } catch (IOException e) {
            System.out.println("File error: " + e.getMessage());
        }

        scanner.close();
    }
}
```

---

## OUTPUT:
<img width="706" height="252" alt="image" src="https://github.com/user-attachments/assets/5686d5dd-0bd7-4579-a34f-282a40071c1e" />


---

## RESULT:
Thus, the program successfully collects user data, writes it to a file, and displays the stored data by reading it back using file-handling techniques.
