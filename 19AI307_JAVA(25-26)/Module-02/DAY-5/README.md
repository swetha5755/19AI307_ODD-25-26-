# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Employee with method display(). Inside display(), return the current object using this. Create another method that calls display().printName()

## AIM:
To create an Employee class where the display() method returns the current object using this, and demonstrate calling display().printName() from another method.

## ALGORITHM :
Create a class Employee with a variable name.

Write a method setName() to assign value to name.

Write a method display() that returns the current object using return this;.

Write a method printName() to print the employee name.

Add another method show() that internally calls display().printName().

In the main() method, read the employee name from the user.

7.Create an Employee object and set the name.

Call both display().printName() and show() to demonstrate method chaining.	

## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Swetha S
RegisterNumber:  212224040344
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Employee {
    String name;

    void setName(String name) {
        this.name = name;  
    }

    Employee display() {
        return this;  
    }

    void printName() {
        System.out.println("Employee Name: " + name);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String inputName = scanner.nextLine();

        Employee emp = new Employee();
        emp.setName(inputName);
        emp.display().printName();  
    }
}
```

## OUTPUT:

<img width="635" height="313" alt="image" src="https://github.com/user-attachments/assets/dfb44496-3751-4c2c-8805-37fef2030b9a" />



## RESULT:
Therefore the program has been executed successfully.

