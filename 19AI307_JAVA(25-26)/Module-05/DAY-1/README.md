# Ex.No:5(A) INPUTSTREAMREADER

## QUESTION:
Write a Java program to **write text into a file** using `FileOutputStream`.

The program should:
1. Read a filename from the user  
2. Read the text content to write  
3. Write the content into the file using `FileOutputStream`  
4. Print a success message  

---

## AIM:
To write a Java program that demonstrates handling files using **FileOutputStream** to insert text data into a file.

---

## ALGORITHM :
1. Start the program.  
2. Read the filename from user input.  
3. Read the content to be written into the file.  
4. Create a `FileOutputStream` object using the filename.  
5. Convert the string content into bytes.  
6. Write the bytes into the file using `fos.write()`.  
7. Close the file stream.  
8. Print a success message.  
9. Handle exceptions if file writing fails.  
10. End the program.

---

## PROGRAM:
```
/*
Program to write text into a file using FileOutputStream
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.io.FileOutputStream;
import java.io.IOException;
import java.util.Scanner;

public class WriteFileUsingFOS {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        try {
            String filename = sc.nextLine();
            String content = sc.nextLine();

            FileOutputStream fos = new FileOutputStream(filename);

            fos.write(content.getBytes());
            fos.close();

            System.out.println("File written successfully.");
        } catch (IOException e) {
            System.out.println("An error occurred.");
        }
    }
}
```

---

## OUTPUT:
<img width="765" height="304" alt="image" src="https://github.com/user-attachments/assets/bae36b7f-1f9c-421a-8677-a9aef770240d" />


---

## RESULT:
Thus, the Java program successfully writes text into a file using **FileOutputStream**.
