# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition)

## AIM:

To write a Java program that demonstrates composition, where a Library contains multiple Book objects.
The program should accept book details from the user, store them inside a Library object, and display all stored books.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Create a Book class with private title and author, a constructor, and a getDetails() method.

4. Create a Library class with a List<Book>, an addBook() method, and a showBooks() method.

5. In main(), create a Scanner and a Library object.

6. Read integer n, then loop n times to read title & author, then add each book to the library.

7. Call showBooks() to display all books and close the scanner.



## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: LOKESH KHANNA R
RegisterNumber:  212222040088
*/
```

## SOURCE CODE:

```
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

    Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    String getDetails() {
        return "- " + title + " by " + author;
    }
}

class Library {
    private List<Book> books;

    Library() {
        books = new ArrayList<>();
    }

    void addBook(String title, String author) {
        books.add(new Book(title, author));
    }

    void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books)
            System.out.println(b.getDetails());
    }
}
```





## OUTPUT:
<img width="1065" height="589" alt="image" src="https://github.com/user-attachments/assets/29303759-e3a5-4b61-b7c6-a4871a8096eb" />



## RESULT:
The program has been executed successfully and the desired output has been obtained.

