# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You are asked to simulate a simple Shape Drawing Tool using the Factory Design Pattern in Java.

You will implement a Shape interface with concrete classes for different shapes (Circle, Square, Rectangle). Using a ShapeFactory, your program will take shape names from user input and draw them accordingly. If the shape is unknown, print an error message.

Requirements:
Create a Shape interface with a draw() method.

Implement Circle, Square, and Rectangle classes that implement Shape and override the draw() method to print a specific message.

Implement a ShapeFactory class that returns the correct shape instance based on input.

In your main method, continuously read shape names from the user (using Scanner) until they type "exit" (case-insensitive).

For each valid shape name, create the shape and call draw().

For invalid shapes, print: Invalid shape: <name>

## AIM:
To implement a Shape Drawing Tool using the Factory Pattern, where user-entered shape names create corresponding objects dynamically and call their draw() methods.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Define a Shape interface with a draw() method.

4. Implement Circle, Square, and Rectangle classes overriding draw().

5. Create ShapeFactory to return shape objects based on input.

6. Continuously read user input until "exit".

7. For each input, create and draw the shape or print an invalid message.




## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: LOKESH KHANNA R
RegisterNumber: 212222040088
*/
```

## SOURCE CODE:
```
import java.util.Scanner;


interface Shape {
    void draw();
}

class Circle implements Shape {
    public void draw() {
        System.out.println("Drawing Circle");
    }
}

class Square implements Shape {
    public void draw() {
        System.out.println("Drawing Square");
    }
}

class Rectangle implements Shape {
    public void draw() {
        System.out.println("Drawing Rectangle");
    }
}

class ShapeFactory {
    public Shape getShape(String shapeType) {
        if (shapeType == null) return null;
        switch (shapeType.toLowerCase()) {
            case "circle":
                return new Circle();
            case "square":
                return new Square();
            case "rectangle":
                return new Rectangle();
            default:
                return null;
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ShapeFactory factory = new ShapeFactory();
        
        while (true) {
            String input = sc.nextLine();
            if (input.equalsIgnoreCase("exit")) break;
            
            Shape shape = factory.getShape(input);
            if (shape != null)
                shape.draw();
            else
                System.out.println("Invalid shape: " + input);
        }
    }
}
```





## OUTPUT:

<img width="829" height="474" alt="image" src="https://github.com/user-attachments/assets/e6a9eb6a-511e-4704-9b24-e019cbdfdeeb" />


## RESULT:

The program correctly creates and draws shapes using the Factory Pattern, handling invalid inputs gracefully.

