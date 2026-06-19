Hierarchical Inheritance in Java

Definition
Hierarchical inheritance is a type of inheritance in which one parent class is inherited by multiple child classes.
In simple words, one base class has many derived classes.

Why this concept is used
- It helps in reusing the same code for multiple classes.
- It reduces duplication of methods and fields.
- It keeps the program structure organized.
- It helps in modeling real-world relationships where one category has multiple specialized forms.

How this helps Java programming
- Makes the code easier to reuse.
- Reduces unnecessary repetition.
- Improves maintainability.
- Makes it easy to add more child classes later.

Important theory
- Parent class or base class: the common class.
- Child classes or derived classes: classes that inherit from the same parent.
- Keyword used: extends
- In hierarchical inheritance, one superclass can have many subclasses.

Example idea
- Animal is the parent class.
- Dog and Cat are two child classes.
- Both Dog and Cat inherit from Animal.

Program 1: Hierarchical Inheritance Example

Code:

class Animal {
    public void eat() {
        System.out.println("Animal eats food");
    }
}

class Dog extends Animal {
    public void bark() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    public void meow() {
        System.out.println("Cat meows");
    }
}

public class HierarchicalInheritanceDemo {
    public static void main(String[] args) {
        Dog d = new Dog();
        Cat c = new Cat();

        d.eat();
        d.bark();

        c.eat();
        c.meow();
    }
}

Line-by-line explanation with comments

class Animal {                           // Line 1: Creates the base class Animal
    public void eat() {                  // Line 2: Creates eat() method in Animal
        System.out.println("Animal eats food"); // Line 3: Prints message
    }                                    // Line 4: Ends eat() method
}                                        // Line 5: Ends Animal class

class Dog extends Animal {               // Line 6: Dog inherits from Animal
    public void bark() {                 // Line 7: Creates bark() method in Dog
        System.out.println("Dog barks"); // Line 8: Prints bark message
    }                                    // Line 9: Ends bark() method
}                                        // Line 10: Ends Dog class

class Cat extends Animal {               // Line 11: Cat inherits from Animal
    public void meow() {                 // Line 12: Creates meow() method in Cat
        System.out.println("Cat meows"); // Line 13: Prints meow message
    }                                    // Line 14: Ends meow() method
}                                        // Line 15: Ends Cat class

public class HierarchicalInheritanceDemo { // Line 16: Main class declaration
    public static void main(String[] args) { // Line 17: Main method starts execution
        Dog d = new Dog();               // Line 18: Creates Dog object
        Cat c = new Cat();               // Line 19: Creates Cat object

        d.eat();                         // Line 20: Calls eat() from Animal using Dog object
        d.bark();                        // Line 21: Calls bark() from Dog

        c.eat();                         // Line 22: Calls eat() from Animal using Cat object
        c.meow();                        // Line 23: Calls meow() from Cat
    }                                    // Line 24: Ends main method
}                                        // Line 25: Ends class

Why this program is used
This program is used to show that one common parent class can be shared by multiple child classes.
It helps in understanding how hierarchical inheritance works.

How this program helps in Java learning
- Shows how one class can support many subclasses.
- Demonstrates code reuse in a hierarchy.
- Helps in understanding OOP relationships clearly.

Pseudocode
START
    CREATE class Animal
    DEFINE eat()

    CREATE class Dog extends Animal
    DEFINE bark()

    CREATE class Cat extends Animal
    DEFINE meow()

    CREATE main method
    CREATE Dog object
    CREATE Cat object
    CALL d.eat()
    CALL d.bark()
    CALL c.eat()
    CALL c.meow()
END

Output
Animal eats food
Dog barks
Animal eats food
Cat meows

Summary
Hierarchical inheritance allows one parent class to be inherited by multiple child classes.
In this program, both Dog and Cat inherit Animal, so they can use the common eat() method.

Important note
This type of inheritance is useful when many classes share the same base behavior.

Diagram explanation

Animal (Base Class)
    |
    +------> Dog (Child)
    |
    +------> Cat (Child)

Animal has:
- eat()

Dog has:
- bark()
- also inherits eat()

Cat has:
- meow()
- also inherits eat()

Visual structure
Animal
  |
  +----> Dog
  |
  +----> Cat

Simple flow diagram
Start
  |
  v
Create Dog object
  |
  v
Call eat() from Animal
  |
  v
Call bark() from Dog
  |
  v
Create Cat object
  |
  v
Call eat() from Animal
  |
  v
Call meow() from Cat
  |
  v
End

One-line definition
Hierarchical inheritance is when one parent class is inherited by multiple child classes.
