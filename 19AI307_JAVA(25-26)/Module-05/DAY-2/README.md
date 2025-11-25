# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION

## QUESTION:
Write a Java program to **serialize a collection of objects** (such as `ArrayList<Student>`) into a file.

- Use `ObjectOutputStream` to serialize a list of Student objects.  
- Use `ObjectInputStream` to read the list back.  
- Class `Student` must implement `Serializable`.  
- Finally, display the deserialized list.

---

## AIM:
To write a Java program that demonstrates **serialization** and **deserialization** of a collection of objects using Java’s object streams.

---

## ALGORITHM :
1. Start the program.  
2. Create a `Student` class that implements `Serializable`.  
3. Read `n` student entries from the user and store them in an `ArrayList<Student>`.  
4. Define a method `serializeStudents()` to serialize the list into a file.  
5. Define a method `deserializeStudents()` to read list data back from file.  
6. Serialize the list to `"students.dat"`.  
7. Deserialize the file and store the resulting list.  
8. Print all deserialized student objects.  
9. End the program.

---

## PROGRAM:
```
/*
Program to serialize and deserialize a collection of Student objects
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    // Serialize list of students
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    // Deserialize list of students
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); // consume newline

        for (int i = 0; i < n; i++) {
            int id = scanner.nextInt();
            scanner.nextLine(); // consume newline
            String name = scanner.nextLine();
            double marks = scanner.nextDouble();
            scanner.nextLine(); // consume newline

            students.add(new Student(id, name, marks));
        }

        String fileName = "students.dat";

        // Serialize
        serializeStudents(students, fileName);

        // Deserialize
        List<Student> deserializedStudents = deserializeStudents(fileName);

        // Display deserialized data
        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}
```

---

## OUTPUT:
<img width="1170" height="807" alt="image" src="https://github.com/user-attachments/assets/00bb0ba3-e885-4263-9891-c082a6dc3bdc" />


---

## RESULT:
Thus, the program successfully serializes and deserializes a collection (`ArrayList<Student>`) using Java object streams.
