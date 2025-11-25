# Ex.No:4(E) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:

Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

## AIM:
To implement the Memento Pattern where every change to an article's content is stored as a version, and the user can restore any previous version.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Read the number of versions and save each content change as a memento.

4. Store each saved memento in an ArticleHistory list.

5. Read the version index to restore.

6. Retrieve the memento from history using the index.

7. Restore the article content and print it, or show an error if invalid.




## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: NIXAN DASS A
RegisterNumber:  212222040109
*/
```

## SOURCE CODE:
```
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

<img width="839" height="647" alt="image" src="https://github.com/user-attachments/assets/f607076d-65f4-484b-a6c0-0f52f051b8e4" />



## RESULT:
The program correctly saves article versions and restores the selected version using the Memento Pattern.

