# Ex.No:3(E) INNER CLASS

## QUESTION:
 Write a Java program where the inner class is declared private and accessed through a method in the outer class. 
 
 <img width="630" height="167" alt="image" src="https://github.com/user-attachments/assets/f79cccc4-4994-4e93-b982-baa097c89a0a" />


## AIM:
To demonstrate the use of a private inner class and access it through a method in the outer class.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Create an outer class OuterClass with a method accessInner(int value).
4.	Declare a private inner class InnerClass with a variable data and methods setData() and displayData().
5.	In accessInner(), create an object of InnerClass, set the data, and display it.
6.	In the main method, read input from the user.
7.	Create an object of OuterClass and call accessInner() with the input value.
8.	Stop the program.





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: LOKESH KHANNA R
RegisterNumber:  212222040088
*/
```

## SOURCE CODE:

```

import java.util.Scanner;

public class OuterClass {
    public void accessInner(int value) {
        InnerClass inner = new InnerClass();
        inner.setData(value);
        inner.displayData();
    }

    private class InnerClass {
        private int data;

        void setData(int data) {
            this.data = data;
        }

        void displayData() {
            System.out.println("Data set inside private inner class: " + data);
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int input = scanner.nextInt();
        OuterClass outer = new OuterClass();
        outer.accessInner(input);
        scanner.close();
    }
}


```

## OUTPUT:

<img width="1082" height="289" alt="image" src="https://github.com/user-attachments/assets/9416226f-2971-467c-8818-d3b26aeb315d" />


## RESULT:
The program successfully sets and displays data using a private inner class.

