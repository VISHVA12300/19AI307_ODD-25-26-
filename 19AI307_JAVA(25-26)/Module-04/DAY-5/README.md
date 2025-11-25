# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an **Article** class where any changes to the article content are saved as **mementos**.  
The user should be able to view and **restore any saved version**.

### Requirements:
- When the content changes, save the version using the **Memento Pattern**.  
- Users should be able to select a previous version and restore it.  
- If an invalid version index is selected, print `"Invalid version"`.

### Input Format:
1. Integer `n` → number of versions  
2. Next `n` lines → article content for each version  
3. Integer index → version number to restore  

### Output Format:
Restored content OR `"Invalid version"`

---

## AIM:
To implement the **Memento Design Pattern** in Java so that article content can be saved, tracked, and restored to any previous version.

---

## ALGORITHM :
1. Start the program.  
2. Create:
   - **Article** → Originator  
   - **ArticleMemento** → Memento  
   - **ArticleHistory** → Caretaker  
3. When content updates, save each version as a memento.  
4. Store all versions in a list.  
5. Ask user for the version index to restore.  
6. If the index is valid, restore content and print it.  
7. Otherwise print `"Invalid version"`.  
8. End the program.

---

## PROGRAM:
```
/*
Program implementing Memento Pattern for Article version control
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.*;

class Article {
    private String content;

    public void setContent(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }

    public ArticleMemento save() {
        return new ArticleMemento(content);
    }

    public void restore(ArticleMemento memento) {
        this.content = memento.getContent();
    }
}

class ArticleMemento {
    private final String content;

    public ArticleMemento(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }
}

class ArticleHistory {
    private List<ArticleMemento> versions = new ArrayList<>();

    public void saveVersion(Article article) {
        versions.add(article.save());
    }

    public ArticleMemento getVersion(int index) {
        if (index >= 0 && index < versions.size()) {
            return versions.get(index);
        }
        return null;
    }
}

public class ArticleManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Article article = new Article();
        ArticleHistory history = new ArticleHistory();

        int n = Integer.parseInt(sc.nextLine());
        for (int i = 0; i < n; i++) {
            String content = sc.nextLine();
            article.setContent(content);
            history.saveVersion(article);
        }

        int restoreIndex = Integer.parseInt(sc.nextLine());
        ArticleMemento m = history.getVersion(restoreIndex);

        if (m != null) {
            article.restore(m);
            System.out.println(article.getContent());
        } else {
            System.out.println("Invalid version");
        }

        sc.close();
    }
}
```

---

## OUTPUT:
<img width="735" height="534" alt="image" src="https://github.com/user-attachments/assets/ed13e005-929b-4725-9c57-617ea437de9a" />


---

## RESULT:
Thus, the program successfully implements the **Memento Design Pattern**, enabling version saving and restoration of article content.
