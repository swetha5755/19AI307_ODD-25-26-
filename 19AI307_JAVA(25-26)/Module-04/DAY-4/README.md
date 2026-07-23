# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You are asked to simulate a simple Shape Drawing Tool using the Factory Design Pattern in Java.

You will implement a Shape interface with concrete classes for different shapes (Circle, Square, Rectangle). Using a ShapeFactory, your program will take shape names from user input and draw them accordingly. If the shape is unknown, print an error message.

## AIM:
To write a Java program that implements the Factory Design Pattern to create and draw shapes dynamically based on user input.


## ALGORITHM :
Start the program.
Import the necessary package 'java.util'
Create a Shape interface containing a draw() method.
Create concrete classes Circle, Square, and Rectangle implementing Shape.
Create a ShapeFactory class with a method getShape(String shapeType).
In the main() method, accept user input for shape type.
Call factory method to get the appropriate object.
Draw the shape or print error if unknown.
Stop the program.	

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Swetha S
RegisterNumber: 212224040344 
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
        if (shapeType == null) {
            return null;
        }
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
            String input = sc.nextLine().trim();
            if (input.equalsIgnoreCase("exit")) {
                break;
            }
            
            Shape shape = factory.getShape(input);
            if (shape != null) {
                shape.draw();
            } else {
                System.out.println("Invalid shape: " + input);
            }
        }
        sc.close();
    }
}
```
## OUTPUT:

<img width="797" height="547" alt="image" src="https://github.com/user-attachments/assets/e8292803-0829-49d6-ac8b-7d25cb7f81cc" />

## RESULT:
Therefore the program has been executed successfully.
