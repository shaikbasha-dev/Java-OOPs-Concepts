Rules of Method Overriding in Java

1. Definition
Method overriding occurs when a subclass provides a specific implementation of a method that is already defined in its superclass.

2. Main rules of method overriding

Rule 1: Same method name
The overriding method in the child class must have the same name as the method in the parent class.

Rule 2: Same parameters
The number, type, and order of parameters must be the same in both methods.

Rule 3: Same return type (or compatible return type)
The return type of the overriding method should be the same as the parent method, or a subtype (covariant return type).

Rule 4: Access modifier should not be more restrictive
A child class method cannot make the access level more restricted than the parent method.
Example:
- If parent method is public, child method cannot be private.

Rule 5: The overriding method cannot throw broader checked exceptions
The child method can throw fewer or narrower exceptions, but not broader checked exceptions.

Rule 6: The method must be inherited
The method being overridden must be inherited from the parent class.
If the method does not exist in the parent class, overriding is not possible.

Rule 7: Use of @Override annotation
The @Override annotation is recommended because it tells Java that the method is intended to override a parent method.
It helps catch mistakes during compilation.

Rule 8: Static methods cannot be overridden
Static methods belong to the class, not the object, so they cannot be overridden in the usual way.

Rule 9: Final methods cannot be overridden
If a method is declared final in the parent class, it cannot be overridden.

Rule 10: Private methods cannot be overridden
Private methods are not visible to subclasses, so they cannot be overridden.

3. Why these rules are important
These rules are important because they ensure that method overriding works correctly and that Java can properly perform runtime polymorphism.

4. Example program demonstrating rules

class Animal {
    public void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    public void sound() {
        System.out.println("Dog barks");
    }
}

public class RulesOfMethodOverridingDemo {
    public static void main(String[] args) {
        Animal a = new Animal();
        Dog d = new Dog();

        a.sound();
        d.sound();
    }
}

5. Line-by-line explanation with comments

class Animal {                          // Line 1: Declares the parent class
    public void sound() {                // Line 2: Declares a public method named sound()
        System.out.println("Animal makes a sound"); // Line 3: Prints base behavior
    }                                    // Line 4: Ends the sound() method
}                                        // Line 5: Ends the Animal class

class Dog extends Animal {               // Line 6: Dog inherits Animal
    @Override                            // Line 7: Indicates method overriding
    public void sound() {                // Line 8: Same method name and same parameters
        System.out.println("Dog barks"); // Line 9: Prints overridden behavior
    }                                    // Line 10: Ends the sound() method
}                                        // Line 11: Ends the Dog class

public class RulesOfMethodOverridingDemo { // Line 12: Main class declaration
    public static void main(String[] args) { // Line 13: Main method starts here
        Animal a = new Animal();         // Line 14: Creates Animal object
        Dog d = new Dog();               // Line 15: Creates Dog object

        a.sound();                       // Line 16: Calls parent version
        d.sound();                       // Line 17: Calls overridden child version
    }                                    // Line 18: Ends main method
}                                        // Line 19: Ends class

6. Output
Animal makes a sound
Dog barks

7. Pseudocode
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

8. Summary
Method overriding is allowed only when the child class method matches the parent method name, parameters, and access level rules.
Using @Override makes the code clearer and safer.

9. Important note
If the method name or parameters are changed, then it is not overriding; it becomes method overloading or a new method.
