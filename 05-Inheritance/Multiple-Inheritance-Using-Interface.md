Multiple Inheritance Using Interface in Java

Definition
Multiple inheritance using interface means a class can inherit behavior from more than one interface.
Java does not allow a class to inherit from multiple classes, but it allows a class to implement multiple interfaces.

Why this concept is used
- It avoids the problems caused by multiple class inheritance.
- It allows one class to use features from more than one source.
- It helps in designing flexible and reusable code.
- It supports abstraction and contract-based programming.

How this helps Java programming
- Provides a way to achieve multiple inheritance safely.
- Keeps code modular and organized.
- Promotes loose coupling between classes.
- Makes programs easier to extend.

Important theory
- Interface: a blueprint that defines what methods a class must implement.
- implements keyword: used by a class to inherit from an interface.
- A class can implement multiple interfaces.
- Interfaces do not contain method bodies (unless default methods are used).

Example idea
- Swim is one interface.
- Fly is another interface.
- Duck implements both interfaces.

Program 1: Multiple Inheritance Using Interface

Code:

interface Swim {
    void swim();
}

interface Fly {
    void fly();
}

class Duck implements Swim, Fly {
    public void swim() {
        System.out.println("Duck swims");
    }

    public void fly() {
        System.out.println("Duck flies");
    }
}

public class MultipleInheritanceUsingInterfaceDemo {
    public static void main(String[] args) {
        Duck d = new Duck();
        d.swim();
        d.fly();
    }
}

Line-by-line explanation with comments

interface Swim {                       // Line 1: Declares interface Swim
    void swim();                        // Line 2: Declares abstract method swim()
}                                       // Line 3: Ends interface Swim

interface Fly {                        // Line 4: Declares interface Fly
    void fly();                         // Line 5: Declares abstract method fly()
}                                       // Line 6: Ends interface Fly

class Duck implements Swim, Fly {       // Line 7: Duck implements both interfaces
    public void swim() {                // Line 8: Defines swim() method
        System.out.println("Duck swims"); // Line 9: Prints swim message
    }                                   // Line 10: Ends swim() method

    public void fly() {                 // Line 11: Defines fly() method
        System.out.println("Duck flies"); // Line 12: Prints fly message
    }                                   // Line 13: Ends fly() method
}                                       // Line 14: Ends Duck class

public class MultipleInheritanceUsingInterfaceDemo { // Line 15: Main class declaration
    public static void main(String[] args) { // Line 16: Main method starts execution
        Duck d = new Duck();            // Line 17: Creates Duck object
        d.swim();                       // Line 18: Calls swim() method
        d.fly();                        // Line 19: Calls fly() method
    }                                   // Line 20: Ends main method
}                                       // Line 21: Ends class

Why this program is used
This program is used to show that a class can inherit features from more than one interface.
It helps in understanding how Java solves the problem of multiple inheritance.

How this program helps in Java learning
- Shows how multiple inheritance is achieved using interfaces.
- Explains the difference between class inheritance and interface inheritance.
- Helps students understand abstraction and polymorphism better.

Pseudocode
START
    CREATE interface Swim
    DECLARE swim()

    CREATE interface Fly
    DECLARE fly()

    CREATE class Duck implements Swim, Fly
    DEFINE swim()
    DEFINE fly()

    CREATE main method
    CREATE object of Duck
    CALL swim()
    CALL fly()
END

Output
Duck swims
Duck flies

Summary
Java does not allow multiple inheritance using classes directly, but it allows a class to implement multiple interfaces.
This example shows how Duck inherits behavior from both Swim and Fly interfaces.

Important note
A class can implement many interfaces, but it can extend only one class.

Diagram explanation

+---------+
|  Swim    |
| swim()   |
+---------+
      |
      |
+---------+
|   Fly    |
| fly()    |
+---------+
      |
      |
     Duck
   implements both

Visual structure
Swim  +  Fly
   \    /
    \  /
      Duck

Simple flow diagram
Start
  |
  v
Create Duck object
  |
  v
Call swim() from Swim interface
  |
  v
Call fly() from Fly interface
  |
  v
End

One-line definition
Multiple inheritance using interface means a class implements more than one interface to reuse behaviors from multiple sources.
