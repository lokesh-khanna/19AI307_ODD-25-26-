# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely wants to enter a secure tech conference. The security system checks certain conditions to grant access. These conditions are:

She must be registered (true/false).

She must have a valid ID (true/false).

She must NOT be blacklisted (true/false).

The system uses logical operators to evaluate her access eligibility:

If she is registered AND has a valid ID, and NOT blacklisted, she is granted access.

Otherwise, access is denied.

Your task is to evaluate these conditions using logical operators and print whether access is granted or denied.

Input Format:
Three boolean values entered by the user (true or false):

<isRegistered>
<hasValidID>
<isBlacklisted>
Output Format:
Access Granted: true/false

For example:

<img width="730" height="238" alt="image" src="https://github.com/user-attachments/assets/46cb804d-b149-4f8d-8317-c842796db671" />



## AIM:
To write a Java program that reads three boolean values and evaluates access permission using logical operators.


## ALGORITHM :

1.	Start the program.
2. Create a Scanner object to read input.
3. Read three boolean values- isRegistered, hasValidId, isBlacklisted.
4. Compute access eligibility using:
accessGranted = isRegistered && hasValidID && !isBlacklisted;
5. Display the result: "Access Granted: " + access.
6. Stop the program.



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: LOKESH KHANNA R
RegisterNumber:  212222040088
*/
```

## Sourcecode.java:

```
import java.util.Scanner;

public class AccessCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        boolean isRegistered = sc.nextBoolean();
        boolean hasValidID = sc.nextBoolean();
        boolean isBlacklisted = sc.nextBoolean();

        boolean accessGranted = isRegistered && hasValidID && !isBlacklisted;

        System.out.println("Access Granted: " + accessGranted);
    }
}


```





## OUTPUT:
<img width="991" height="537" alt="image" src="https://github.com/user-attachments/assets/f6c1da53-d1fe-4152-8774-9af6b7d1ca0f" />




## RESULT:
Thus, the program successfully evaluates access permission using logical operators and produces the correct output.




