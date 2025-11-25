# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a **Library** contains multiple **Book** objects.  
Each `Book` must be created **inside** the `Library`, meaning:

### → Books cannot exist without the Library (Composition)

- The Library manages the creation of Book objects.
- Users input multiple books, and the Library stores them.
- Finally, the Library should display all books.

---

## AIM:
To demonstrate **composition** in Java by creating a Library class that *owns* Book objects, ensuring that Books cannot exist independently.

---

## ALGORITHM :
1. Start the program.  
2. Create a `Book` class with private attributes `title` and `author`.  
3. Create a `Library` class that contains a list of `Book` objects.  
4. Add a method in Library to create and store Book objects internally (composition).  
5. In `main()`:  
   - Create a Library object  
   - Read the number of books  
   - Read each book’s title and author  
   - Add each book to the library using the composition method  
6. Display all stored books using `showBooks()`.  
7. End the program.

---

## PROGRAM:
```
/*
Program to demonstrate Composition using Library and Book classes
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {
    private List<Book> books = new ArrayList<>();

    public void addBook(String title, String author) {
        books.add(new Book(title, author)); 
    }

    public void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books) {
            System.out.println("- " + b.getDetails());
        }
    }
}
```

---

## OUTPUT:
<img width="909" height="549" alt="image" src="https://github.com/user-attachments/assets/a1aae3d3-15b7-4db3-87c9-a5d5fbbd30ef" />



---

## RESULT:
Thus, the program successfully demonstrates **composition**, where Book objects are created and managed only by the Library, and cannot exist independently.
