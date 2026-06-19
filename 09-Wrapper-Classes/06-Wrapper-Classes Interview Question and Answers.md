06-Wrapper-Classes Interview Question and Answers

1. What are wrapper classes in Java?
Answer:
Wrapper classes are classes in Java that provide an object representation of primitive data types.
Each primitive type has a corresponding wrapper class.
Example:
- int -> Integer
- char -> Character
- boolean -> Boolean

2. Why are wrapper classes needed in Java?
Answer:
Wrapper classes are needed because:
- Java collections store objects, not primitives.
- Some APIs require objects.
- Wrapper classes provide useful methods for conversion and comparison.
- They help in object-oriented programming.

3. What is the difference between primitive and wrapper class?
Answer:
A primitive stores only a value, while a wrapper class stores a value as an object.
Primitive example: int x = 10;
Wrapper example: Integer x = 10;
Primitive types are faster, while wrappers provide methods.

4. What are the wrapper classes for all primitive types?
Answer:
- byte -> Byte
- short -> Short
- int -> Integer
- long -> Long
- float -> Float
- double -> Double
- char -> Character
- boolean -> Boolean

5. What is auto-boxing?
Answer:
Auto-boxing is the automatic conversion of a primitive into its corresponding wrapper object.
Example:
Integer obj = 10;

6. What is un-boxing?
Answer:
Un-boxing is the automatic conversion of a wrapper object back into its corresponding primitive type.
Example:
int num = obj;

7. Why is auto-boxing useful?
Answer:
Auto-boxing is useful because it reduces manual conversion code and makes Java code easier to read.
It is especially helpful when working with collections and generics.

8. Why is un-boxing useful?
Answer:
Un-boxing is useful because it allows wrapper objects to be used in arithmetic, conditions, and comparisons as normal primitive values.

9. Can wrapper classes be null?
Answer:
Yes. Wrapper class objects can be null, because they are objects.
Primitive types cannot be null.

10. Are wrapper classes immutable?
Answer:
Yes. Wrapper classes are immutable, which means once their value is assigned, it cannot be changed.

11. What is the difference between parseInt() and valueOf()?
Answer:
parseInt() converts a String into a primitive int.
valueOf() converts a value into a wrapper object.
Example:
- Integer.parseInt("10") returns int
- Integer.valueOf("10") returns Integer

12. What does Integer.parseInt("100") do?
Answer:
It converts the string "100" into the integer value 100.

13. What is the use of toString() in wrapper classes?
Answer:
toString() converts a wrapper object into a String.
Example:
Integer x = 50;
String s = x.toString();

14. Can we store primitive values in ArrayList?
Answer:
No. ArrayList can store objects, not primitives.
So Java uses wrapper classes such as Integer, Double, and Boolean.

15. What is the role of wrapper classes in generics?
Answer:
Generics work with objects, so wrapper classes are required when using primitive values in generic collections.

16. What is the difference between Integer.valueOf(10) and new Integer(10)?
Answer:
Integer.valueOf(10) uses caching and returns a wrapper object efficiently.
new Integer(10) creates a new object explicitly.
Using new Integer(10) is not recommended.

17. What is the importance of wrapper classes in Java collections?
Answer:
Wrapper classes allow primitive values to be stored in collections such as ArrayList, HashSet, and HashMap.

18. Can wrapper classes be used in switch statements?
Answer:
No, switch statements usually use primitive types or strings, not wrapper objects directly.

19. What happens if parseInt() receives an invalid string?
Answer:
It throws NumberFormatException.

20. What is the wrapper class for char?
Answer:
The wrapper class for char is Character.

21. What is the wrapper class for boolean?
Answer:
The wrapper class for boolean is Boolean.

22. Why are wrapper classes called wrapper classes?
Answer:
They are called wrapper classes because they wrap primitive values inside objects.

23. What is the use of equals() with wrapper classes?
Answer:
equals() compares the values of two wrapper objects.
Example:
Integer a = 10;
Integer b = 10;
System.out.println(a.equals(b));

24. What is the output of a.equals(b) if both values are same?
Answer:
It prints true.

25. What is the difference between == and equals() for wrapper classes?
Answer:
== compares references, while equals() compares actual values.
So equals() is better for checking value equality.

26. Give one example where auto-boxing occurs automatically.
Answer:
ArrayList<Integer> list = new ArrayList<>();
list.add(5);
Here, the int value 5 is automatically boxed into Integer.

27. Give one example where un-boxing occurs automatically.
Answer:
int n = new Integer(7);
Here, the Integer object is automatically un-boxed into int.

28. Why do wrapper classes provide methods like parseInt() and valueOf()?
Answer:
Because wrapper classes are objects and they provide useful utility methods to convert values and perform operations.

29. What is a wrapper class object in Java?
Answer:
A wrapper class object is an object that contains a primitive value inside it.

30. What is the main benefit of wrapper classes in Java?
Answer:
The main benefit is that they allow primitives to be used in object-oriented scenarios such as collections, generics, and APIs.

31. What is the difference between Integer and int?
Answer:
int is a primitive type, while Integer is a wrapper class object.
int stores a raw value; Integer stores a value as an object.

32. Can wrapper classes be used with generics?
Answer:
Yes. Wrapper classes are commonly used with generics because generics work with objects.

33. What is the role of wrapper classes in synchronization?
Answer:
Wrapper classes are objects, so they can be used in object-based contexts, but the main use is still conversion and collection support.

34. What is the output of this code?
Example:
Integer a = 10;
Integer b = 20;
System.out.println(a + b);
Answer:
30

35. What is the output of this code?
Example:
Integer a = Integer.valueOf("10");
System.out.println(a);
Answer:
10

36. What is the output of this code?
Example:
String s = "50";
int n = Integer.parseInt(s);
System.out.println(n + 5);
Answer:
55

37. Why is wrapper class conversion important for user input?
Answer:
Because user input is usually received as a string, and wrapper methods help convert it into numeric values.

38. What is the most common wrapper class used in Java collections?
Answer:
Integer is one of the most commonly used wrapper classes in collections.

39. Why do wrapper classes support methods like equals() and compareTo()?
Answer:
Because wrapper objects are objects and need methods for comparison and comparison-based logic.

40. Can wrapper classes be used with arrays?
Answer:
Yes. Arrays can store wrapper objects just like they store other objects.

41. What is the difference between valueOf() and new Integer()?
Answer:
valueOf() is preferred because it may use caching and is more efficient.
new Integer() creates a new object each time.

42. How do wrapper classes help in API design?
Answer:
They allow methods to accept objects, making APIs more consistent with Java’s object model.

43. What is the significance of wrapper classes in Java 8 and later?
Answer:
Wrapper classes became even easier to use because of auto-boxing and un-boxing support.

44. What is the output of this code?
Example:
Boolean b = Boolean.valueOf("TRUE");
System.out.println(b);
Answer:
true

45. Why should we avoid using new Integer()?
Answer:
Because it creates unnecessary objects and is less efficient than valueOf().

46. What is the role of wrapper classes in method overloading?
Answer:
They help because methods can accept objects instead of primitives in certain situations.

47. What is the purpose of the Character wrapper class?
Answer:
It wraps char values and provides methods to test or manipulate characters.

48. What is the purpose of the Boolean wrapper class?
Answer:
It wraps boolean values and provides methods for boolean handling.

49. What is the difference between wrapper classes and strings?
Answer:
Wrapper classes store primitive values as objects, while String stores character sequences.

50. Final summary of wrapper classes.
Answer:
Wrapper classes are essential in Java because they allow primitive values to be used as objects.
They are useful in collections, generics, APIs, and conversion operations.
Auto-boxing and un-boxing make them easy to use.
