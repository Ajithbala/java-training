# java-training

## What is JVM?

JVM (Java Virtual Machine) is an abstract machine that enables your computer to run a Java program.

When you run the Java program, Java compiler first compiles your Java code to bytecode. Then, the JVM translates bytecode into native machine code (set of instructions that a computer's CPU executes directly).

Java is a platform-independent language. It's because when you write Java code, it's ultimately written for JVM but not your physical machine (computer). Since JVM ​executes the Java bytecode which is platform-independent, Java is platform-independent.


## What is JRE?

JRE (Java Runtime Environment) is a software package that provides Java class libraries, Java Virtual Machine (JVM), and other components that are required to run Java applications.

## What is JDK?

JDK (Java Development Kit) is a software development kit required to develop applications in Java. When you download JDK, JRE is also downloaded with it.

In addition to JRE, JDK also contains a number of development tools (compilers, JavaDoc, Java Debugger, etc).


## Java Variables and Literals

In this tutorial, we will learn about Java variables and literals with the help of examples.
Java Variables

A variable is a location in memory (storage area) to hold data.

To indicate the storage area, each variable should be given a unique name (identifier). Learn more about Java identifiers.
Create Variables in Java

Here's how we create a variable in Java,

int speedLimit = 80;

Here, speedLimit is a variable of int data type and we have assigned value 80 to it.

The int data type suggests that the variable can only hold integers. To learn more, visit Java data types.

In the example, we have assigned value to the variable during declaration. However, it's not mandatory.

You can declare variables and assign variables separately. For example,

int speedLimit;
speedLimit = 80;

## Note: Java is a statically-typed language. It means that all variables must be declared before they can be used.
Change values of variables

The value of a variable can be changed in the program, hence the name variable. For example,

int speedLimit = 80;
... .. ...
speedLimit = 90; 

Here, initially, the value of speedLimit is 80. Later, we changed it to 90.

However, we cannot change the data type of a variable in Java within the same scope.

## What is the variable scope?

Don't worry about it for now. Just remember that we can't do something like this:

int speedLimit = 80;
... .. ...
float speedLimit;

To learn more, visit: Can I change declaration type for a variable in Java?
Rules for Naming Variables in Java

Java programming language has its own set of rules and conventions for naming variables. Here's what you need to know:

    Java is case sensitive. Hence, age and AGE are two different variables. For example,
     

    int age = 24;
    int AGE = 25;

    System.out.println(age);  // prints 24
    System.out.println(AGE);  // prints 25

    Variables must start with either a letter or an underscore, _ or a dollar, $ sign. For example,
     

    int age;  // valid name and good practice
    int _age;  // valid but bad practice
    int $age;  // valid but bad practice

    Variable names cannot start with numbers. For example,
     

    int 1age;  // invalid variables

    Variable names can't use whitespace. For example,
     

    int my age;  // invalid variables



    Here, is we need to use variable names having more than one word, use all lowercase letters for the first word and capitalize the first letter of each subsequent word. For example, myAge.
    When creating variables, choose a name that makes sense. For example, score, number, level makes more sense than variable names such as s, n, and l.
    If you choose one-word variable names, use all lowercase letters. For example, it's better to use speed rather than SPEED, or sPEED.

## There are 4 types of variables in Java programming language:

    Instance Variables (Non-Static Fields)
    Class Variables (Static Fields)
    Local Variables
    Parameters


 ##   Java literals

Literals are data used for representing fixed values. They can be used directly in the code. For example,

int a = 1;
float b = 2.5;
char c = 'F';

Here, 1, 2.5, and 'F' are literals.

Here are different types of literals in Java.
## 1. Boolean Literals

In Java, boolean literals are used to initialize boolean data types. They can store two values: true and false. For example,

boolean flag1 = false;
boolean flag2 = true;

Here, false and true are two boolean literals.
## 2. Integer Literals

An integer literal is a numeric value(associated with numbers) without any fractional or exponential part. There are 4 types of integer literals in Java:

    binary (base 2)
    decimal (base 10)
    octal (base 8)
    hexadecimal (base 16)

For example:

// binary
int binaryNumber = 0b10010;
// octal 
int octalNumber = 027;

// decimal
int decNumber = 34;

// hexadecimal 
int hexNumber = 0x2F; // 0x represents hexadecimal
// binary
int binNumber = 0b10010; // 0b represents binary

In Java, binary starts with 0b, octal starts with 0, and hexadecimal starts with 0x.

Note: Integer literals are used to initialize variables of integer types like byte, short, int, and long.
## 3. Floating-point Literals

A floating-point literal is a numeric literal that has either a fractional form or an exponential form. For example,

class Main {
  public static void main(String[] args) {
    	
    double myDouble = 3.4;
    float myFloat = 3.4F;
 
    // 3.445*10^2
    double myDoubleScientific = 3.445e2;

    System.out.println(myDouble);  // prints 3.4
    System.out.println(myFloat);    // prints 3.4
    System.out.println(myDoubleScientific);   // prints 344.5
  }
}

Run Code

Note: The floating-point literals are used to initialize float and double type variables.
## 4. Character Literals

Character literals are unicode character enclosed inside single quotes. For example,

char letter = 'a';

Here, a is the character literal.

We can also use escape sequences as character literals. For example, \b (backspace), \t (tab), \n (new line), etc.
## 5. String literals

A string literal is a sequence of characters enclosed inside double-quotes. For example,

String str1 = "Java Programming";
String str2 = "Programiz";

### Java Data Types (Primitive)

In this tutorial, we will learn about all 8 primitive data types in Java with the help of examples.
Java Data Types

As the name suggests, data types specify the type of data that can be stored inside variables in Java.

Java is a statically-typed language. This means that all variables must be declared before they can be used.

int speed;

Here, speed is a variable, and the data type of the variable is int.

The int data type determines that the speed variable can only contain integers.

There are 8 data types predefined in Java, known as primitive data types.

Note: In addition to primitive data types, there are also referenced types (object type).
8 Primitive Data Types
### 1. boolean type

    The boolean data type has two possible values, either true or false.
    Default value: false.
    They are usually used for true/false conditions.

Example 1: Java boolean data type
```java
 class Main {
  public static void main(String[] args) {
    	
    boolean flag = true;
    System.out.println(flag);    // prints true
  }
}
 ```
Run Code
### 2. byte type

    The byte data type can have values from -128 to 127 (8-bit signed two's complement integer).
    If it's certain that the value of a variable will be within -128 to 127, then it is used instead of int to save memory.
    Default value: 0

Example 2: Java byte data type
```java 
class Main {
  public static void main(String[] args) {

    byte range;
    range = 124;
    System.out.println(range);    // prints 124
  }
}
 ```
Run Code
### 3. short type

    The short data type in Java can have values from -32768 to 32767 (16-bit signed two's complement integer).
    If it's certain that the value of a variable will be within -32768 and 32767, then it is used instead of other integer data types (int, long).
    Default value: 0

Example 3: Java short data type
``` java
class Main {
  public static void main(String[] args) {
    	
    short temperature;
    temperature = -200;
    System.out.println(temperature);  // prints -200
  }
}
```
Run Code
### 4. int type

    The int data type can have values from -231 to 231-1 (32-bit signed two's complement integer).
    If you are using Java 8 or later, you can use an unsigned 32-bit integer. This will have a minimum value of 0 and a maximum value of 232-1. To learn more, visit How to use the unsigned integer in java 8?
    Default value: 0

Example 4: Java int data type
```java
class Main {
  public static void main(String[] args) {
    	
    int range = -4250000;
    System.out.println(range);  // print -4250000
  }
}
```
Run Code
### 5. long type

    The long data type can have values from -263 to 263-1 (64-bit signed two's complement integer).
    If you are using Java 8 or later, you can use an unsigned 64-bit integer with a minimum value of 0 and a maximum value of 264-1.
    Default value: 0

Example 5: Java long data type
``` java
class LongExample {
  public static void main(String[] args) {
    	
    long range = -42332200000L;
    System.out.println(range);    // prints -42332200000
  }
}
```
Run Code

Notice, the use of L at the end of -42332200000. This represents that it's an integer of the long type.
### 6. double type

    The double data type is a double-precision 64-bit floating-point.
    It should never be used for precise values such as currency.
    Default value: 0.0 (0.0d)

Example 6: Java double data type
```java
class Main {
  public static void main(String[] args) {
    	
    double number = -42.3;
    System.out.println(number);  // prints -42.3
  }
}
```
Run Code
### 7. float type

    The float data type is a single-precision 32-bit floating-point. Learn more about single-precision and double-precision floating-point if you are interested.
    It should never be used for precise values such as currency.
    Default value: 0.0 (0.0f)

Example 7: Java float data type
```java
class Main {
  public static void main(String[] args) {
    	
    float number = -42.3f;
    System.out.println(number);  // prints -42.3
  }
}
```
Run Code

Notice that we have used -42.3f instead of -42.3in the above program. It's because -42.3 is a double literal.

To tell the compiler to treat -42.3 as float rather than double, you need to use f or F.

If you want to know about single-precision and double-precision, visit Java single-precision and double-precision floating-point.
### 8. char type

    It's a 16-bit Unicode character.
    The minimum value of the char data type is '\u0000' (0) and the maximum value of the is '\uffff'.
    Default value: '\u0000'

Example 8: Java char data type
``` java
class Main {
  public static void main(String[] args) {
    	
    char letter = '\u0051';
    System.out.println(letter);  // prints Q
  }
}
```
Run Code

Here, the Unicode value of Q is \u0051. Hence, we get Q as the output.

Here is another example:
``` java
class Main {
  public static void main(String[] args) {
    	
    char letter1 = '9';
    System.out.println(letter1);  // prints 9
    	
    char letter2 = 65;
    System.out.println(letter2);  // prints A

  }
}
```
Run Code

Here, we have assigned 9 as a character (specified by single quotes) to the letter1 variable. However, the letter2 variable is assigned 65 as an integer number (no single quotes).

Hence, A is printed to the output. It is because Java treats characters as an integer and the ASCII value of A is 65. To learn more about ASCII, visit What is ASCII Code?.
String type

Java also provides support for character strings via java.lang.String class. Strings in Java are not primitive types. Instead, they are objects. For example,

String myString = "Java Programming";

## Java Operators

In this tutorial, you'll learn about different types of operators in Java, their syntax and how to use them with the help of examples.

Operators are symbols that perform operations on variables and values. For example, + is an operator used for addition, while * is also an operator used for multiplication.

Operators in Java can be classified into 5 types:

###    Arithmetic Operators
###    Assignment Operators
###    Relational Operators
###    Logical Operators
###    Unary Operators
###    Bitwise Operators

### 1. Java Arithmetic Operators

Arithmetic operators are used to perform arithmetic operations on variables and data. For example,

a + b;

Here, the + operator is used to add two variables a and b. Similarly, there are various other arithmetic operators in Java.
Operator
					Operation
			
+
					Addition
			
-
					Subtraction
			
*
					Multiplication
			
/
					Division
			
%
					Modulo Operation (Remainder after division)
			
Example 1: Arithmetic Operators
``` java
class Main {
  public static void main(String[] args) {
    
    // declare variables
    int a = 12, b = 5;

    // addition operator
    System.out.println("a + b = " + (a + b));

    // subtraction operator
    System.out.println("a - b = " + (a - b));

    // multiplication operator
    System.out.println("a * b = " + (a * b));

    // division operator
    System.out.println("a / b = " + (a / b));

    // modulo operator
    System.out.println("a % b = " + (a % b));
  }
}
``` 
Run Code

Output

a + b = 17
a - b = 7 
a * b = 60
a / b = 2 
a % b = 2 

In the above example, we have used +, -, and * operators to compute addition, subtraction, and multiplication operations.

## / Division Operator

Note the operation, a / b in our program. The / operator is the division operator.

If we use the division operator with two integers, then the resulting quotient will also be an integer. And, if one of the operands is a floating-point number, we will get the result will also be in floating-point.

In Java,

(9 / 2) is 4
(9.0 / 2) is 4.5
(9 / 2.0) is 4.5
(9.0 / 2.0) is 4.5

% Modulo Operator

The modulo operator % computes the remainder. When a = 7 is divided by b = 4, the remainder is 3.

Note: The % operator is mainly used with integers.
2. Java Assignment Operators

Assignment operators are used in Java to assign values to variables. For example,

int age;
age = 5;

Here, = is the assignment operator. It assigns the value on its right to the variable on its left. That is, 5 is assigned to the variable age.

Let's see some more assignment operators available in Java.
Operator
					Example
					Equivalent to
			
=
					a = b;
					a = b;
			
+=
					a += b;
					a = a + b;
			
-=
					a -= b;
					a = a - b;
			
*=
					a *= b;
					a = a * b;
			
/=
					a /= b;
					a = a / b;
			
%=
					a %= b;
					a = a % b;
			
Example 2: Assignment Operators
``` java
class Main {
  public static void main(String[] args) {
    
    // create variables
    int a = 4;
    int var;

    // assign value using =
    var = a;
    System.out.println("var using =: " + var);

    // assign value using =+
    var += a;
    System.out.println("var using +=: " + var);

    // assign value using =*
    var *= a;
    System.out.println("var using *=: " + var);
  }
}
```
Run Code

Output

var using =: 4
var using +=: 8 
var using *=: 32

### 3. Java Relational Operators

Relational operators are used to check the relationship between two operands. For example,

// check if a is less than b
a < b;

Here, < operator is the relational operator. It checks if a is less than b or not.

It returns either true or false.
Operator
					Description
					Example
			
==
					Is Equal To
					3 == 5 returns false
			
!=
					Not Equal To
					3 != 5 returns true
			
>
					Greater Than
					3 > 5 returns false
			
<
					Less Than
					3 < 5 returns true
			
>=
					Greater Than or Equal To
					3 >= 5 returns false
			
<=
					Less Than or Equal To
					3 <= 5 returns true
			
Example 3: Relational Operators
``` java
class Main {
  public static void main(String[] args) {
    
    // create variables
    int a = 7, b = 11;

    // value of a and b
    System.out.println("a is " + a + " and b is " + b);

    // == operator
    System.out.println(a == b);  // false

    // != operator
    System.out.println(a != b);  // true

    // > operator
    System.out.println(a > b);  // false

    // < operator
    System.out.println(a < b);  // true

    // >= operator
    System.out.println(a >= b);  // false

    // <= operator
    System.out.println(a <= b);  // true
  }
}
```
Run Code

Note: Relational operators are used in decision making and loops.
## 4. Java Logical Operators

Logical operators are used to check whether an expression is true or false. They are used in decision making.
Operator
					Example
					Meaning
			
&& (Logical AND)
					expression1 && expression2
					true only if both expression1 and expression2 are true
			
|| (Logical OR)
					expression1 || expression2
					true if either expression1 or expression2 is true
			
! (Logical NOT)
					!expression
					true if expression is false and vice versa
			
Example 4: Logical Operators

class Main {
  public static void main(String[] args) {

    // && operator
    System.out.println((5 > 3) && (8 > 5));  // true
    System.out.println((5 > 3) && (8 < 5));  // false

    // || operator
    System.out.println((5 < 3) || (8 > 5));  // true
    System.out.println((5 > 3) || (8 < 5));  // true
    System.out.println((5 < 3) || (8 < 5));  // false

    // ! operator
    System.out.println(!(5 == 3));  // true
    System.out.println(!(5 > 3));  // false
  }
}

Run Code

Working of Program

    (5 > 3) && (8 > 5) returns true because both (5 > 3) and (8 > 5) are true.
    (5 > 3) && (8 < 5) returns false because the expression (8 < 5) is false.
    (5 < 3) || (8 > 5) returns true because the expression (8 > 5) is true.
    (5 > 3) || (8 < 5) returns true because the expression (5 > 3) is true.
    (5 < 3) || (8 < 5) returns false because both (5 < 3) and (8 < 5) are false.
    !(5 == 3) returns true because 5 == 3 is false.
    !(5 > 3) returns false because 5 > 3 is true.

## 5. Java Unary Operators

Unary operators are used with only one operand. For example, ++ is a unary operator that increases the value of a variable by 1. That is, ++5 will return 6.

Different types of unary operators are:
Operator
					Meaning
			
+
					Unary plus: not necessary to use since numbers are positive without using it
			
-
					Unary minus: inverts the sign of an expression
			
++
					Increment operator: increments value by 1
			
--
					Decrement operator: decrements value by 1
			
!
					Logical complement operator: inverts the value of a boolean
			
## Increment and Decrement Operators

Java also provides increment and decrement operators: ++ and -- respectively. ++ increases the value of the operand by 1, while -- decrease it by 1. For example,

int num = 5;

// increase num by 1
++num;

Here, the value of num gets increased to 6 from its initial value of 5.
Example 5: Increment and Decrement Operators
``` java
class Main {
  public static void main(String[] args) {
    
    // declare variables
    int a = 12, b = 12;
    int result1, result2;

    // original value
    System.out.println("Value of a: " + a);

    // increment operator
    result1 = ++a;
    System.out.println("After increment: " + result1);

    System.out.println("Value of b: " + b);

    // decrement operator
    result2 = --b;
    System.out.println("After decrement: " + result2);
  }
}
```
Run Code

Output

Value of a: 12
After increment: 13
Value of b: 12     
After decrement: 11

In the above program, we have used the ++ and -- operator as prefixes (++a, --b). We can also use these operators as postfix (a++, b++).

There is a slight difference when these operators are used as prefix versus when they are used as a postfix.

To learn more about these operators, visit increment and decrement operators.
6. Java Bitwise Operators

Bitwise operators in Java are used to perform operations on individual bits. For example,

Bitwise complement Operation of 35

35 = 00100011 (In Binary)

~ 00100011 
  ________
   11011100  = 220 (In decimal)

Here, ~ is a bitwise operator. It inverts the value of each bit (0 to 1 and 1 to 0).

The various bitwise operators present in Java are:
Operator
					Description
			
~
					Bitwise Complement
			
<<
					Left Shift
			
>>
					Right Shift
			
>>>
					Unsigned Right Shift
			
&
					Bitwise AND
			
^
					Bitwise exclusive OR
			

These operators are not generally used in Java. To learn more, visit Java Bitwise and Bit Shift Operators.
Other operators

Besides these operators, there are other additional operators in Java.
Java instanceof Operator

The instanceof operator checks whether an object is an instanceof a particular class. For example,

class Main {
  public static void main(String[] args) {

    String str = "Programiz";
    boolean result;

    // checks if str is an instance of
    // the String class
    result = str instanceof String;
    System.out.println("Is str an object of String? " + result);
  }
}

Run Code

Output

Is str an object of String? true

Here, str is an instance of the String class. Hence, the instanceof operator returns true. To learn more, visit Java instanceof.
## Java Ternary Operator

The ternary operator (conditional operator) is shorthand for the if-then-else statement. For example,

variable = Expression ? expression1 : expression2

Here's how it works.

    If the Expression is true, expression1 is assigned to the variable.
    If the Expression is false, expression2 is assigned to the variable.

Let's see an example of a ternary operator.
``` java
class Java {
  public static void main(String[] args) {

    int februaryDays = 29;
    String result;

    // ternary operator
    result = (februaryDays == 28) ? "Not a leap year" : "Leap year";
    System.out.println(result);
  }
}
```
Run Code

Output

Leap year

In the above example, we have used the ternary operator to check if the year is a leap year or not. To learn more, visit the Java ternary operator.


