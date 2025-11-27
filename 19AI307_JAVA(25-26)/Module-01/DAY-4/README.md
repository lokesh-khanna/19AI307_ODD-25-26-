# Ex.No:1(D) ARRAYS

## QUESTION:

Write a Java Program to Find the Average of Array Elements.

For example:

<img width="602" height="269" alt="image" src="https://github.com/user-attachments/assets/713be153-11a0-4816-96a5-9684ce45cb67" />


## AIM:

To write a Java program that reads an array of integers and calculates the average of its elements.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Read the size of the array from the user.
4.	Create an integer array of the given size.
5.	Read each element and add it to a variable sum.
6.	Compute the average using sum / n.
7.	Display the average value.
8.	Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: LOKESH KHANNA R
RegisterNumber:  212222040088
*/
```

## SOURCE CODE:

```
import java.util.*;

public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int[] arr=new int[n];
        int sum=0;
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
            sum=sum+arr[i];

        }
        double avr=(double) sum/n;
        System.out.printf("The average of elements is %.2f",avr);
    }
}

```





## OUTPUT:


<img width="1001" height="638" alt="image" src="https://github.com/user-attachments/assets/229bdaf1-8c5d-4fde-9b4e-5736030f974f" />


## RESULT:

The program successfully calculates and displays the average of the array elements.

