Method Overriding in Java

Definition
Method overriding is a feature in Java where a child class provides its own implementation of a method that is already defined in the parent class.
The method name, return type, and parameters must match the parent method.

Why this concept is used
- It allows a child class to change inherited behavior.
- It helps in implementing polymorphism.
- It makes code more specific and meaningful for the child class.
- It improves code flexibility and readability.

How this helps Java programming
- Lets subclasses customize inherited behavior.
- Helps in writing cleaner object-oriented programs.
- Supports runtime behavior based on actual object type.
- Makes real-world modeling easier.

Important theory
- The method in the child class must have the same signature as the parent method.
- The return type should be compatible.
- @Override is optional but recommended.
- Overriding is used for runtime polymorphism.

Example idea
- Animal has a method sound().
- Dog overrides sound() with a different behavior.

Program 1: Method Overriding Example

Code:

class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class MethodOverridingDemo {
    public static void main(String[] args) {
        Animal a = new Animal();
        Dog d = new Dog();

        a.sound();
        d.sound();
    }
}

Line-by-line explanation with comments

class Animal {                           // Line 1: Declares parent class Animal
    void sound() {                        // Line 2: Declares sound() method in Animal
        System.out.println("Animal makes a sound"); // Line 3: Prints animal message
    }                                    // Line 4: Ends sound() method
}                                        // Line 5: Ends Animal class

class Dog extends Animal {               // Line 6: Dog inherits Animal
    @Override                            // Line 7: Indicates overriding of parent method
    void sound() {                        // Line 8: Declares sound() in Dog with same signature
        System.out.println("Dog barks"); // Line 9: Prints dog-specific message
    }                                    // Line 10: Ends sound() method
}                                        // Line 11: Ends Dog class

public class MethodOverridingDemo {     // Line 12: Main class declaration
    public static void main(String[] args) { // Line 13: Main method starts execution
        Animal a = new Animal();         // Line 14: Creates Animal object
        Dog d = new Dog();               // Line 15: Creates Dog object

        a.sound();                       // Line 16: Calls Animal's sound()
        d.sound();                       // Line 17: Calls Dog's overridden sound()
    }                                    // Line 18: Ends main method
}                                        // Line 19: Ends class

Why this program is used
This program is used to show how a child class can replace the behavior of a parent method.
It helps students understand overriding clearly.

How this program helps in Java learning
- Shows the difference between parent and child behavior.
- Helps explain runtime polymorphism.
- Makes OOP concepts easier to understand.

Pseudocode
START
    CREATE class Animal
    DEFINE sound()

    CREATE class Dog extends Animal
    OVERRIDE sound()

    CREATE main method
    CREATE Animal object
    CREATE Dog object
    CALL a.sound()
    CALL d.sound()
END

Output
Animal makes a sound
Dog barks

Summary
Method overriding allows a child class to provide a specific implementation of a method already defined in the parent class.
In this example, Dog overrides the sound() method of Animal.

Important note
The overriding method must have the same name and parameters as the parent method.

Diagram explanation

Animal
  |
  | inherits
  v
Dog

Animal has:
- sound()

Dog has:
- sound()   <-- overridden

Visual structure
Animal
  |
  +----> Dog

Simple flow diagram
Start
  |
  v
Create Animal object
  |
  v
Call sound() from Animal
  |
  v
Create Dog object
  |
  v
Call sound() from Dog (overridden)
  |
  v
End

One-line definition
Method overriding is when a subclass provides a new implementation of a method already present in the superclass.
