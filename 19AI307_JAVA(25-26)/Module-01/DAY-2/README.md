# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
A pirate ship has a code lock that only opens if:

The input code is even, and

If it is less than 100, say "Weak Code".

If it is between 100 and 999, say "Strong Code".

If the code is odd, deny access -"Access Denied".

For example:

<img width="536" height="139" alt="image" src="https://github.com/user-attachments/assets/59f560a3-e0fb-4a7a-8a40-75ac033edb26" />



## AIM:

To write a Java program that checks whether the entered pirate code is valid and prints the correct message based on its value.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the integer input code from the user.
4.	Check if the number is even.
5.	If even and less than 100, display “Weak Code”.
6.	If even and between 100 and 999, display “Strong Code”.
7.	Otherwise, display “Access Denied”.
8.	If the number is odd, display “Access Denied”.
9.	Stop the program.





## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: NIXAN DASS A
RegisterNumber:  212222040109
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int code = scanner.nextInt();

        if (code % 2 == 0) { // Check if code is even
            if (code < 100) {
                System.out.println("Weak Code");
            } else if (code >= 100 && code <= 999) {
                System.out.println("Strong Code");
            } else {
                System.out.println("Access Denied"); 
            }
        } else {
            System.out.println("Access Denied");
        }

        scanner.close();
    }
}


```


## OUTPUT:
<img width="1110" height="447" alt="image" src="https://github.com/user-attachments/assets/b33c5f6c-524f-453b-96a2-7bfe2b684b44" />




## RESULT:

Thus, the program successfully evaluates the pirate code using conditional statements and displays the correct message based on the given rules.
