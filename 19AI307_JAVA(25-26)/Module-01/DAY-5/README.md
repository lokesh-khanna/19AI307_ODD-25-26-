# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

Write a Java program to reverse a given string.

<img width="455" height="160" alt="image" src="https://github.com/user-attachments/assets/a4325fc6-f20c-47d0-be19-fa3194f4d905" />

## AIM:

To write a Java program that reads a string and prints its reverse.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Read the input string from the user.
4.	Use StringBuilder to reverse the string.
5.	Convert it back to a string and display the reversed output.
6.	Stop the program.



## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: LOKESH KHANNA R
RegisterNumber:  212222040088
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class ReverseString {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        String input = scanner.nextLine();

        // Reverse the string using StringBuilder
        StringBuilder sb = new StringBuilder(input).reverse();
        String reversed = sb.toString();

        System.out.println("Reversed string: " + reversed);
    }
}

```



## OUTPUT:

<img width="828" height="397" alt="image" src="https://github.com/user-attachments/assets/326b9817-11f8-4e33-b1a3-e26d0e332280" />



## RESULT:

The program successfully reverses the given string and displays the result.

