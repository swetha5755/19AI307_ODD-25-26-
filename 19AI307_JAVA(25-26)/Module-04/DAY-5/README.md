# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create a program that sends different types of notifications: "email", "sms", and "push". Use the Factory Pattern to generate the appropriate notification sender and call its notifyUser() method.

## AIM:
To write a Java program that demonstrates a Behavioral Pattern using the Factory Method, allowing different notification types to send messages through a common interface.

## ALGORITHM :
Start the program.
Import the necessary package 'java.util'
Create an interface Notification with method notifyUser().
Implement concrete classes: EmailNotification, SMSNotification, and PushNotification.
Create a NotificationFactory that returns the appropriate object based on user input.
In main(), get the notification type from the user.
Call the notifyUser() method of the returned object.
If no valid type is provided, display an error.
Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Swetha S
RegisterNumber: 212224040344 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Notification {
    void notifyUser();
}

// ===== Concrete Notifications =====
class EmailNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Email Notification");
    }
}

class SMSNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending SMS Notification");
    }
}

class PushNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Push Notification");
    }
}

// ===== Factory =====
class NotificationFactory {
    public Notification createNotification(String type) {
        if (type == null) return null;
        switch (type.toLowerCase()) {
            case "email":
                return new EmailNotification();
            case "sms":
                return new SMSNotification();
            case "push":
                return new PushNotification();
            default:
                return null;
        }
    }
}

// ===== Main =====
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        NotificationFactory factory = new NotificationFactory();

        while (true) {
            String input = sc.nextLine().trim();
            if (input.equalsIgnoreCase("exit")) break;

            Notification n = factory.createNotification(input);
            if (n != null) {
                n.notifyUser();
            } else {
                System.out.println("Invalid notification type: " + input);
            }
        }

        sc.close();
    }
}
```

## OUTPUT:

<img width="822" height="352" alt="image" src="https://github.com/user-attachments/assets/e8f5587e-f6b3-4220-9e4b-e18423de18c5" />



## RESULT:
Therefore the program has been executed successfully.
