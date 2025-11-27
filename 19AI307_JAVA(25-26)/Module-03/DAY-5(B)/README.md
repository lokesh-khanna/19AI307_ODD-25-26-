# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to reverse a number using the Integer wrapper class and compare it with the original number.

<img width="597" height="250" alt="image" src="https://github.com/user-attachments/assets/2e85df78-b7e4-4561-9331-bddbbc7de830" />


## AIM:
To write a Java program that reverses a number using the Integer wrapper class and checks if it is a palindrome.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read an integer input from the user.
4.	Convert the primitive int to Integer using Integer.valueOf().
5.	Reverse the number using a method that extracts digits (% 10) and builds the reversed number.
6.	Compare the original number with the reversed number.
7.	If equal, print that it is a palindrome; otherwise, print it is not and show the reversed number.
8.	Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: LOKESH KHANNA R
RegisterNumber:  212222040088
*/
```

## SOURCE CODE:


```
import java.util.Scanner;

public class ReverseNumberCheck {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int originalNumber = scanner.nextInt();

        Integer number = Integer.valueOf(originalNumber);

        int reversedNumber = reverseInteger(number);


        if (originalNumber == reversedNumber) {
            System.out.println(originalNumber + " is a palindrome number.");
        } else {
            System.out.println(originalNumber + " is not a palindrome number.");
            System.out.println("Reversed Number: "+reversedNumber);
        }

        scanner.close();
    }

    public static int reverseInteger(Integer num) {
        int reversed = 0;
        while (num != 0) {
            int digit = num % 10;
            reversed = reversed * 10 + digit;
            num /= 10;
        }
        return reversed;
    }
}

```


## OUTPUT:

<img width="958" height="326" alt="image" src="https://github.com/user-attachments/assets/64a8bd73-8315-4563-bd6b-b71d24de41bb" />


## RESULT:

The program successfully reverses a number, compares it with the original, and correctly identifies palindrome numbers using the Integer wrapper class.

