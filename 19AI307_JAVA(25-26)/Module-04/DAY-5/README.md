# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

## AIM:
To implement the Memento Design Pattern in Java by creating an Article class that saves and restores different versions of its content.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Article with content and methods to save and restore state.
4.	Create a Memento class to store the content state.
5.	Create a Caretaker class to store multiple saved versions (mementos).
6.	Save article content whenever it changes and allow restoring any previous version.
7.	Display saved versions and restore selected version, then stop the program.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109 
*/
```

## SOURCE CODE:

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




## OUTPUT:
<img width="745" height="542" alt="image" src="https://github.com/user-attachments/assets/25d525bc-400e-450b-95b4-913967f3e896" />



## RESULT:
The program successfully demonstrates the Memento Pattern, allowing multiple versions of the article content to be saved and restored without losing previous states.
