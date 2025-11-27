# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You are writing a Java program where you read a string input. If the input is "init", you create an object and call its method. If it's "null", no object is created.
Your program crashes with a NullPointerException when "null" is entered.
What caused the crash and how can you handle it to prevent the error?

## AIM:
To understand why a NullPointerException occurs when no object is created and how to prevent it safely.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Read input from user.

4. Declare object reference as null.

5. If input is "init", create the object.

6. Before calling method, check if object is null.

7. If null, print a safe message instead of calling method.




## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: LOKESH KHANNA R
RegisterNumber:  212222040088
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class MyObject {
    void display() {
        System.out.println("Object exists");
    }
}

public class NullPointerObjectExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        String input = sc.next();
        MyObject obj = null;

        if (input.equalsIgnoreCase("init")) {
            obj = new MyObject();
        }

        try {
            obj.display();
        } catch (NullPointerException e) {
            System.out.println("Object is null");
        }

        sc.close();
    }
}
```





## OUTPUT:
<img width="893" height="273" alt="image" src="https://github.com/user-attachments/assets/931a81a0-92bc-423c-a2ca-b06782699c0d" />



## RESULT:
The crash happens because obj is null, and you must check obj != null before calling display().

