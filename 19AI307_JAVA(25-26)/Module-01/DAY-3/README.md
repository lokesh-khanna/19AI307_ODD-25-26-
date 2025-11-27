# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Reversing a number means rearranging its digits in the opposite order. For example:

The reverse of 1234 is 4321

The reverse of 9870 is 789 (since leading zeros in the reversed number are not shown)

Write a Java program that takes an integer input from the user and then reverses its digits using a while loop.

The program should repeatedly extract the last digit of the number using the modulus operator (%) and then build the reversed number.

The loop should continue until the number becomes 0.

Finally, display the reversed number as output.

For example:


<img width="487" height="150" alt="image" src="https://github.com/user-attachments/assets/751bb7e1-3ef8-41ed-8b4c-19f65dc46af1" />



## AIM:

To write a Java program that reads an integer and reverses its digits using a while loop.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Read the integer input from the user.
4.	Initialize a variable reversed = 0.
5.	Use a while loop while the number is not 0.
6.	Extract the last digit using % 10 and add it to reversed.
7.	Remove the last digit using / 10.
8.	Display the reversed number and stop the program.



## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: LOKESH KHANNA R
RegisterNumber:  212222040088
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class ReverseNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int number = scanner.nextInt();

        int originalNumber = number;
        int reversed = 0;

        while (number != 0) {
            int digit = number % 10;          
            reversed = reversed * 10 + digit; 
            number = number / 10;             
        }

        System.out.println("Reversed number: " + reversed);

        scanner.close();
    }
}


```


## OUTPUT:

<img width="801" height="414" alt="image" src="https://github.com/user-attachments/assets/46726599-36a6-45f6-8253-d62f012d0687" />




## RESULT:

The program successfully reverses the input number and prints the result.

