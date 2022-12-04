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


## Java Basic Input and Output

In this tutorial, you will learn simple ways to display output to users and take input from users in Java.
### Java Output

In Java, you can simply use
```java
System.out.println(); or

System.out.print(); or

System.out.printf();

```
to send output to standard output (screen).

Here,

    System is a class
    out is a public static field: it accepts output data.

Don't worry if you don't understand it. We will discuss class, public, and static in later chapters.

Let's take an example to output a line.
```java
class AssignmentOperator {
    public static void main(String[] args) {
    	
        System.out.println("Java programming is interesting.");   
    }
}
```
Run Code

Output:

Java programming is interesting.

Here, we have used the println() method to display the string.
Difference between println(), print() and printf()

    print() - It prints string inside the quotes.
    println() - It prints string inside the quotes similar like print() method. Then the cursor moves to the beginning of the next line.
    printf() - It provides string formatting (similar to printf in C/C++ programming).

Example: print() and println()

```java
class Output {
    public static void main(String[] args) {
    	
        System.out.println("1. println ");
        System.out.println("2. println ");
    	
        System.out.print("1. print ");
        System.out.print("2. print");
    }
}
```
Run Code

Output:

1. println 
2. println 
1. print 2. print

In the above example, we have shown the working of the print() and println() methods. To learn about the printf() method, visit Java printf().
Example: Printing Variables and Literals

```java
class Variables {
    public static void main(String[] args) {
    	
        Double number = -10.6;
    	
        System.out.println(5);
        System.out.println(number);
    }
}

```
Run Code

When you run the program, the output will be:

5
-10.6

Here, you can see that we have not used the quotation marks. It is because to display integers, variables and so on, we don't use quotation marks.
Example: Print Concatenated Strings

```java
class PrintVariables {
    public static void main(String[] args) {
    	
        Double number = -10.6;
    	
        System.out.println("I am " + "awesome.");
        System.out.println("Number = " + number);
    }
}
```
Run Code

Output:

I am awesome.
Number = -10.6

In the above example, notice the line,

System.out.println("I am " + "awesome.");

Here, we have used the + operator to concatenate (join) the two strings: "I am " and "awesome.".

And also, the line,

System.out.println("Number = " + number);

Here, first the value of variable number is evaluated. Then, the value is concatenated to the string: "Number = ".
### Java Input

Java provides different ways to get input from the user. However, in this tutorial, you will learn to get input from user using the object of Scanner class.

In order to use the object of Scanner, we need to import java.util.Scanner package.


import java.util.Scanner;

To learn more about importing packages in Java, visit Java Import Packages.

Then, we need to create an object of the Scanner class. We can use the object to take input from the user.


// create an object of Scanner
Scanner input = new Scanner(System.in);

// take input from the user
int number = input.nextInt();

Example: Get Integer Input From the User

```java
import java.util.Scanner;

class Input {
    public static void main(String[] args) {
    	
        Scanner input = new Scanner(System.in);
    	
        System.out.print("Enter an integer: ");
        int number = input.nextInt();
        System.out.println("You entered " + number);

        // closing the scanner object
        input.close();
    }
}

```
Run Code

Output:

Enter an integer: 23
You entered 23

In the above example, we have created an object named input of the Scanner class. We then call the nextInt() method of the Scanner class to get an integer input from the user.

Similarly, we can use nextLong(), nextFloat(), nextDouble(), and next() methods to get long, float, double, and string input respectively from the user.

Note: We have used the close() method to close the object. It is recommended to close the scanner object once the input is taken.
Example: Get float, double and String Input

```java
import java.util.Scanner;

class Input {
    public static void main(String[] args) {
    	
        Scanner input = new Scanner(System.in);
    	
        // Getting float input
        System.out.print("Enter float: ");
        float myFloat = input.nextFloat();
        System.out.println("Float entered = " + myFloat);
    	
        // Getting double input
        System.out.print("Enter double: ");
        double myDouble = input.nextDouble();
        System.out.println("Double entered = " + myDouble);
    	
        // Getting String input
        System.out.print("Enter text: ");
        String myString = input.next();
        System.out.println("Text entered = " + myString);
    }
}

```
Run Code

Output:

Enter float: 2.343
Float entered = 2.343
Enter double: -23.4
Double entered = -23.4
Enter text: Hey!
Text entered = Hey!

As mentioned, there are other several ways to get input from the user. To learn more about Scanner, visit Java Scanner.



## Java Comments

In this tutorial, you will learn about Java comments, why we use them, and how to use comments in right way.

In computer programming, comments are a portion of the program that are completely ignored by Java compilers. They are mainly used to help programmers to understand the code. For example,

// declare and initialize two variables
int a =1;
int b = 3;

// print the output
System.out.println("This is output");

Here, we have used the following comments,

    declare and initialize two variables
    print the output

Types of Comments in Java

In Java, there are two types of comments:

### single-line comment
### multi-line comment

### Single-line Comment

A single-line comment starts and ends in the same line. To write a single-line comment, we can use the // symbol. For example,

// "Hello, World!" program example
 ```java
class Main {
    public static void main(String[] args) {    	
        // prints "Hello, World!"
        System.out.println("Hello, World!");
    }
}
```
Run Code

Output:

Hello, World!

Here, we have used two single-line comments:

    "Hello, World!" program example
    prints "Hello World!"

The Java compiler ignores everything from // to the end of line. Hence, it is also known as End of Line comment.
Multi-line Comment

When we want to write comments in multiple lines, we can use the multi-line comment. To write multi-line comments, we can use the /*....*/ symbol. For example,

/* This is an example of  multi-line comment.
 * The program prints "Hello, World!" to the standard output.
 */
``` java
class HelloWorld {
    public static void main(String[] args) {

        System.out.println("Hello, World!");
    }
}
```
Run Code

Output:

Hello, World!

Here, we have used the multi-line comment:

/* This is an example of multi-line comment.
* The program prints "Hello, World!" to the standard output.
*/

This type of comment is also known as Traditional Comment. In this type of comment, the Java compiler ignores everything from /* to */.


### Java if...else Statement

In this tutorial, you will learn about control flow statements using Java if and if...else statements with the help of examples.

In programming, we use the if..else statement to run a block of code among more than one alternatives.

For example, assigning grades (A, B, C) based on the percentage obtained by a student.

    if the percentage is above 90, assign grade A
    if the percentage is above 75, assign grade B
    if the percentage is above 65, assign grade C

## 1. Java if (if-then) Statement

The syntax of an if-then statement is:

if (condition) {
  // statements
}

Here, condition is a boolean expression such as age >= 18.

    if condition evaluates to true, statements are executed
    if condition evaluates to false, statements are skipped

Working of if Statement
if the number is greater than 0, code inside if block is executed, otherwise code inside if block is skipped
Working of Java if statement
Example 1: Java if Statement
``` java
class IfStatement {
  public static void main(String[] args) {

    int number = 10;

    // checks if number is less than 0
    if (number < 0) {
      System.out.println("The number is negative.");
    }

    System.out.println("Statement outside if block");
  }
}
```
Run Code

Output

Statement outside if block

In the program, number < 0 is false. Hence, the code inside the body of the if statement is skipped.

Note: If you want to learn more about about test conditions, visit Java Relational Operators and Java Logical Operators.

We can also use Java Strings as the test condition.
Example 2: Java if with String
``` java
class Main {
  public static void main(String[] args) {
    // create a string variable
    String language = "Java";

    // if statement
    if (language == "Java") {
      System.out.println("Best Programming Language");
    }
  }
}
```
Run Code

Output

Best Programming Language

In the above example, we are comparing two strings in the if block.
### 2. Java if...else (if-then-else) Statement

The if statement executes a certain section of code if the test expression is evaluated to true. However, if the test expression is evaluated to false, it does nothing.

In this case, we can use an optional else block. Statements inside the body of else block are executed if the test expression is evaluated to false. This is known as the if-...else statement in Java.

The syntax of the if...else statement is:

if (condition) {
  // codes in if block
}
else {
  // codes in else block
}

Here, the program will do one task (codes inside if block) if the condition is true and another task (codes inside else block) if the condition is false.
How the if...else statement works?
If the condition is true, the code inside the if block is executed, otherwise, code inside the else block is executed
Working of Java if-else statements
Example 3: Java if...else Statement
``` java
class Main {
  public static void main(String[] args) {
    int number = 10;

    // checks if number is greater than 0
    if (number > 0) {
      System.out.println("The number is positive.");
    }
    
    // execute this block
    // if number is not greater than 0
    else {
      System.out.println("The number is not positive.");
    }

    System.out.println("Statement outside if...else block");
  }
}
```
Run Code

Output

The number is positive.
Statement outside if...else block

In the above example, we have a variable named number. Here, the test expression number > 0 checks if number is greater than 0.

Since the value of the number is 10, the test expression evaluates to true. Hence code inside the body of if is executed.

Now, change the value of the number to a negative integer. Let's say -5.

int number = -5;

If we run the program with the new value of number, the output will be:

The number is not positive.
Statement outside if...else block

Here, the value of number is -5. So the test expression evaluates to false. Hence code inside the body of else is executed.
### 3. Java if...else...if Statement

In Java, we have an if...else...if ladder, that can be used to execute one block of code among multiple other blocks.

if (condition1) {
  // codes
}
else if(condition2) {
  // codes
}
else if (condition3) {
  // codes
}
.
.
else {
  // codes
}

Here, if statements are executed from the top towards the bottom. When the test condition is true, codes inside the body of that if block is executed. And, program control jumps outside the if...else...if ladder.

If all test expressions are false, codes inside the body of else are executed.
How the if...else...if ladder works?
If the first test condition if true, code inside first if block is executed, if the second condition is true, block inside second if is executed, and if all conditions are false, the else block is executed
Working of if...else...if ladder
Example 4: Java if...else...if Statement
```java
class Main {
  public static void main(String[] args) {

    int number = 0;

    // checks if number is greater than 0
    if (number > 0) {
      System.out.println("The number is positive.");
    }

    // checks if number is less than 0
    else if (number < 0) {
      System.out.println("The number is negative.");
    }
    
    // if both condition is false
    else {
      System.out.println("The number is 0.");
    }
  }
}
```
Run Code

Output

The number is 0.

In the above example, we are checking whether number is positive, negative, or zero. Here, we have two condition expressions:

    number > 0 - checks if number is greater than 0
    number < 0 - checks if number is less than 0

Here, the value of number is 0. So both the conditions evaluate to false. Hence the statement inside the body of else is executed.

Note: Java provides a special operator called ternary operator, which is a kind of shorthand notation of if...else...if statement. To learn about the ternary operator, visit Java Ternary Operator.
### 4. Java Nested if..else Statement

In Java, it is also possible to use if..else statements inside an if...else statement. It's called the nested if...else statement.

Here's a program to find the largest of 3 numbers using the nested if...else statement.
Example 5: Nested if...else Statement
```java
class Main {
  public static void main(String[] args) {

    // declaring double type variables
    Double n1 = -1.0, n2 = 4.5, n3 = -5.3, largest;

    // checks if n1 is greater than or equal to n2
    if (n1 >= n2) {

      // if...else statement inside the if block
      // checks if n1 is greater than or equal to n3
      if (n1 >= n3) {
        largest = n1;
      }

      else {
        largest = n3;
      }
    } else {

      // if..else statement inside else block
      // checks if n2 is greater than or equal to n3
      if (n2 >= n3) {
        largest = n2;
      }

      else {
        largest = n3;
      }
    }

    System.out.println("Largest Number: " + largest);
  }
}
```
Run Code

Output:

Largest Number: 4.5

In the above programs, we have assigned the value of variables ourselves to make this easier.






### Java switch Statement

In this tutorial, you will learn to use the switch statement in Java to control the flow of your program’s execution with the help of examples.

The switch statement allows us to execute a block of code among many alternatives.

The syntax of the switch statement in Java is:

switch (expression) {

  case value1:
    // code
    break;
  
  case value2:
    // code
    break;
  
  ...
  ...
  
  default:
    // default statements
  }

How does the switch-case statement work?

The expression is evaluated once and compared with the values of each case.

    If expression matches with value1, the code of case value1 are executed. Similarly, the code of case value2 is executed if expression matches with value2.
    If there is no match, the code of the default case is executed.

Note: The working of the switch-case statement is similar to the Java if...else...if ladder. However, the syntax of the switch statement is cleaner and much easier to read and write.
Example: Java switch Statement

// Java Program to check the size
// using the switch...case statement
```java
class Main {
  public static void main(String[] args) {

    int number = 44;
    String size;

    // switch statement to check size
    switch (number) {

      case 29:
        size = "Small";
        break;

      case 42:
        size = "Medium";
        break;

      // match the value of week
      case 44:
        size = "Large";
        break;

      case 48:
        size = "Extra Large";
        break;
      
      default:
        size = "Unknown";
        break;

    }
    System.out.println("Size: " + size);
  }
}
```
Run Code

Output:

Size: Large

In the above example, we have used the switch statement to find the size. Here, we have a variable number. The variable is compared with the value of each case statement.

Since the value matches with 44, the code of case 44 is executed.

size = "Large";
break;

Here, the size variable is assigned with the value Large.

Recommended Reading: Create a Simple Calculator Using the Java switch Statement
Flowchart of switch Statement
Flowchart of the Java switch statement
Flow chart of the Java switch statement
break statement in Java switch...case

Notice that we have been using break in each case block.

 ...
case 29:
  size = "Small";
  break;
...

The break statement is used to terminate the switch-case statement. If break is not used, all the cases after the matching case are also executed. For example,
```java
class Main {
  public static void main(String[] args) {

    int expression = 2;

    // switch statement to check size
    switch (expression) {
      case 1:
        System.out.println("Case 1");

        // matching case
      case 2:
        System.out.println("Case 2");

      case 3:
        System.out.println("Case 3");

      default:
        System.out.println("Default case");
    }
  }
}
```
Run Code

Output

Case 2
Case 3      
### Default case

In the above example, expression matches with case 2. Here, we haven't used the break statement after each case.

Hence, all the cases after case 2 are also executed.

This is why the break statement is needed to terminate the switch-case statement after the matching case. To learn more, visit Java break Statement.
default case in Java switch-case

The switch statement also includes an optional default case. It is executed when the expression doesn't match any of the cases. For example,

class Main {
  public static void main(String[] args) {
  
    int expression = 9;
    
    switch(expression) {
        
      case 2:
        System.out.println("Small Size");
        break;

      case 3:
        System.out.println("Large Size");
        break;
            
      // default case
      default:
        System.out.println("Unknown Size");
    }
  }
}

Run Code

Output

Unknown Size

In the above example, we have created a switch-case statement. Here, the value of expression doesn't match with any of the cases.

Hence, the code inside the default case is executed.

default:
  System.out.println("Unknown Size);





##  Java for Loop

In this tutorial, we will learn how to use for loop in Java with the help of examples and we will also learn about the working of Loop in computer programming.

In computer programming, loops are used to repeat a block of code. For example, if you want to show a message 100 times, then rather than typing the same code 100 times, you can use a loop.

In Java, there are three types of loops.

    for loop
    while loop
    do...while loop

This tutorial focuses on the for loop. You will learn about the other type of loops in the upcoming tutorials.
Java for Loop

Java for loop is used to run a block of code for a certain number of times. The syntax of for loop is:

for (initialExpression; testExpression; updateExpression) {
    // body of the loop
}

Here,

    The initialExpression initializes and/or declares variables and executes only once.
    The condition is evaluated. If the condition is true, the body of the for loop is executed.
    The updateExpression updates the value of initialExpression.
    The condition is evaluated again. The process continues until the condition is false.

To learn more about the conditions, visit Java relational and logical operators.
Working of for loop in Java with flowchart
Flowchart of Java for loop
Example 1: Display a Text Five Times

// Program to print a text 5 times
```java
class Main {
  public static void main(String[] args) {

    int n = 5;
    // for loop  
    for (int i = 1; i <= n; ++i) {
      System.out.println("Java is fun");
    }
  }
}
```
Run Code

Output

Java is fun
Java is fun
Java is fun
Java is fun
Java is fun

Here is how this program works.
Iteration
					Variable
					Condition: i <= n
					Action
			
1st
					i = 1
n = 5
					true
					Java is fun is printed.
i is increased to 2.
			
2nd
					i = 2
n = 5
					true
					Java is fun is printed.
i is increased to 3.
			
3rd
					i = 3
n = 5
					true
					Java is fun is printed.
i is increased to 4.
			
4th
					i = 4
n = 5
					true
					Java is fun is printed.
i is increased to 5.
			
5th
					i = 5
n = 5
					true
					Java is fun is printed.
i is increased to 6.
			
6th
					i = 6
n = 5
					false
					The loop is terminated.
			
Example 2: Display numbers from 1 to 5

// Program to print numbers from 1 to 5
```java
class Main {
  public static void main(String[] args) {
  
    int n = 5;
    // for loop  
    for (int i = 1; i <= n; ++i) {
      System.out.println(i);
    }
  }
}
```
Run Code

Output

1
2
3
4
5

Here is how the program works.
Iteration
                	Variable
                	Condition: i <= n
                	Action
            
1st
                	i = 1
n = 5
                	true
                	1 is printed.
i is increased to 2.
            
2nd
                	i = 2
n = 5
                	true
                	2 is printed.
i is increased to 3.
            
3rd
                	i = 3
n = 5
                	true
                	3 is printed.
i is increased to 4.
            
4th
                	i = 4
n = 5
                	true
                	4 is printed.
i is increased to 5.
            
5th
                	i = 5
n = 5
                	true
                	5 is printed.
i is increased to 6.
            
6th
                	i = 6
n = 5
                	false
                	The loop is terminated.
            
Example 3: Display Sum of n Natural Numbers

// Program to find the sum of natural numbers from 1 to 1000.
```java
class Main {
  public static void main(String[] args) {
      
    int sum = 0;
    int n = 1000;

    // for loop
    for (int i = 1; i <= n; ++i) {
      // body inside for loop
      sum += i;     // sum = sum + i
    }
       
    System.out.println("Sum = " + sum);
  }
}
```
Run Code

Output:

Sum = 500500

Here, the value of sum is 0 initially. Then, the for loop is iterated from i = 1 to 1000. In each iteration, i is added to sum and its value is increased by 1.

When i becomes 1001, the test condition is false and sum will be equal to 0 + 1 + 2 + .... + 1000.

The above program to add the sum of natural numbers can also be written as

// Program to find the sum of natural numbers from 1 to 1000.
```java
class Main {
  public static void main(String[] args) {
      
    int sum = 0;
    int n = 1000;

    // for loop
    for (int i = n; i >= 1; --i) {
      // body inside for loop
      sum += i;     // sum = sum + i
    }
       
    System.out.println("Sum = " + sum);
  }
}
```
Run Code

The output of this program is the same as the Example 3.
Java for-each Loop

The Java for loop has an alternative syntax that makes it easy to iterate through arrays and collections. For example,

// print array elements 
```java
class Main {
  public static void main(String[] args) {
      
    // create an array
    int[] numbers = {3, 7, 5, -5};
    
    // iterating through the array 
    for (int number: numbers) {
       System.out.println(number);
    }
  }
}
```
Run Code

Output

3
7
5
-5

Here, we have used the for-each loop to print each element of the numbers array one by one.

In the first iteration of the loop, number will be 3, number will be 7 in second iteration and so on.

To learn more, visit Java for-each Loop.
Java Infinite for Loop

If we set the test expression in such a way that it never evaluates to false, the for loop will run forever. This is called infinite for loop. For example,

// Infinite for Loop
```java
class Infinite {
    public static void main(String[] args) {
      
        int sum = 0;

        for (int i = 1; i <= 10; --i) {
            System.out.println("Hello");
        }
    }
}
```
Run Code

Here, the test expression ,i <= 10, is never false and Hello is printed repeatedly until the memory runs out.



## Java for-each Loop

In this tutorial, we will learn about the Java for-each loop and its difference with for loop with the help of examples.

In Java, the for-each loop is used to iterate through elements of arrays and collections (like ArrayList). It is also known as the enhanced for loop.
for-each Loop Sytnax

The syntax of the Java for-each loop is:

for(dataType item : array) {
    ...
}

Here,

    array - an array or a collection
    item - each item of array/collection is assigned to this variable
    dataType - the data type of the array/collection

Example 1: Print Array Elements

// print array elements 
```java
class Main {
  public static void main(String[] args) {
      
    // create an array
    int[] numbers = {3, 9, 5, -5};
    
    // for each loop 
    for (int number: numbers) {
      System.out.println(number);
    }
  }
}
```
Run Code

Output

3
9
5
-5

Here, we have used the for-each loop to print each element of the numbers array one by one.

    In the first iteration, item will be 3.
    In the second iteration, item will be 9.
    In the third iteration, item will be 5.
    In the fourth iteration, item will be -5.

Example 2: Sum of Array Elements

// Calculate the sum of all elements of an array
```java
class Main {
 public static void main(String[] args) {
  
   // an array of numbers
   int[] numbers = {3, 4, 5, -5, 0, 12};
   int sum = 0;

   // iterating through each element of the array 
   for (int number: numbers) {
     sum += number;
   }
  
   System.out.println("Sum = " + sum);
 }
}
```
Run Code

Output:

Sum = 19

In the above program, the execution of the for each loop looks as:
Iteration
                	Variables
            
1
                	number = 3
sum = 0 + 3 = 3
            
2
                	number = 4
sum = 3 + 4 = 7
            
3
                	number = 5
sum = 7 + 5 = 12
            
4
                	number = -5
sum = 12 + (-5) = 7
            
5
                	number = 0
sum = 7 + 0 = 7
            
6
                	number = 12
sum = 7 + 12 = 19
            

As we can see, we have added each element of the numbers array to the sum variable in each iteration of the loop.



## Java while and do...while Loop

In this tutorial, we will learn how to use while and do while loop in Java with the help of examples.

In computer programming, loops are used to repeat a block of code. For example, if you want to show a message 100 times, then you can use a loop. It's just a simple example; you can achieve much more with loops.

In the previous tutorial, you learned about Java for loop. Here, you are going to learn about while and do...while loops.
## Java while loop

Java while loop is used to run a specific code until a certain condition is met. The syntax of the while loop is:

while (testExpression) {
    // body of loop
}

Here,

    A while loop evaluates the textExpression inside the parenthesis ().
    If the textExpression evaluates to true, the code inside the while loop is executed.
    The textExpression is evaluated again.
    This process continues until the textExpression is false.
    When the textExpression evaluates to false, the loop stops.

To learn more about the conditions, visit Java relational and logical operators.
Flowchart of while loop
Flowchart of while loop in Java
Flowchart of Java while loop
Example 1: Display Numbers from 1 to 5

// Program to display numbers from 1 to 5
```java
class Main {
  public static void main(String[] args) {

    // declare variables
    int i = 1, n = 5;

    // while loop from 1 to 5
    while(i <= n) {
      System.out.println(i);
      i++;
    }
  }
}
```
Run Code

Output

1
2
3
4
5

Here is how this program works.
Iteration
					Variable
					Condition: i <= n
					Action
			
1st
					i = 1
n = 5
					true
					1 is printed.
i is increased to 2.
			
2nd
					i = 2
n = 5
					true
					2 is printed.
i is increased to 3.
			
3rd
					i = 3
n = 5
					true
					3 is printed.
i is increased to 4.
			
4th
					i = 4
n = 5
					true
					4 is printed.
i is increased to 5.
			
5th
					i = 5
n = 5
					true
					5 is printed.
i is increased to 6.
			
6th
					i = 6
n = 5
					false
					The loop is terminated
			
Example 2: Sum of Positive Numbers Only

// Java program to find the sum of positive numbers
```java
import java.util.Scanner;

class Main {
  public static void main(String[] args) {
      
    int sum = 0;

    // create an object of Scanner class
    Scanner input = new Scanner(System.in);

    // take integer input from the user
    System.out.println("Enter a number");
    int number = input.nextInt();
	   
    // while loop continues 
    // until entered number is positive
    while (number >= 0) {
      // add only positive numbers
      sum += number;

      System.out.println("Enter a number");
      number = input.nextInt();
    }
	   
    System.out.println("Sum = " + sum);
    input.close();
  }
}
```
Run Code

Output

Enter a number
25
Enter a number
9
Enter a number
5
Enter a number
-3
Sum = 39

In the above program, we have used the Scanner class to take input from the user. Here, nextInt() takes integer input from the user.

The while loop continues until the user enters a negative number. During each iteration, the number entered by the user is added to the sum variable.

When the user enters a negative number, the loop terminates. Finally, the total sum is displayed.
## Java do...while loop

The do...while loop is similar to while loop. However, the body of do...while loop is executed once before the test expression is checked. For example,

do {
    // body of loop
} while(textExpression);

Here,

    The body of the loop is executed at first. Then the textExpression is evaluated.
    If the textExpression evaluates to true, the body of the loop inside the do statement is executed again.
    The textExpression is evaluated once again.
    If the textExpression evaluates to true, the body of the loop inside the do statement is executed again.
    This process continues until the textExpression evaluates to false. Then the loop stops.

Flowchart of do...while loop
Flowchart of do...while loop in Java
Flowchart of Java do while loop

Let's see the working of do...while loop.
Example 3: Display Numbers from 1 to 5

// Java Program to display numbers from 1 to 5
```java
import java.util.Scanner;

// Program to find the sum of natural numbers from 1 to 100.

class Main {
  public static void main(String[] args) {

    int i = 1, n = 5;

    // do...while loop from 1 to 5
    do {
      System.out.println(i);
      i++;
    } while(i <= n);
  }
}
```
Run Code

Output

1
2
3
4
5

Here is how this program works.
Iteration
					Variable
					Condition: i <= n
					Action
			
 
					i = 1
n = 5
					not checked
					1 is printed.
i is increased to 2.
			
1st
					i = 2
n = 5
					true
					2 is printed.
i is increased to 3.
			
2nd
					i = 3
n = 5
					true
					3 is printed.
i is increased to 4.
			
3rd
					i = 4
n = 5
					true
					4 is printed.
i is increased to 5.
			
4th
					i = 5
n = 5
					true
					6 is printed.
i is increased to 6.
			
5th
					i = 6
n = 5
					false
					The loop is terminated
			
Example 4: Sum of Positive Numbers

// Java program to find the sum of positive numbers
```java
import java.util.Scanner;

class Main {
  public static void main(String[] args) {
      
    int sum = 0;
    int number = 0;

    // create an object of Scanner class
    Scanner input = new Scanner(System.in);
	   
    // do...while loop continues 
    // until entered number is positive
    do {
      // add only positive numbers
      sum += number;
      System.out.println("Enter a number");
      number = input.nextInt();
    } while(number >= 0); 
	   
    System.out.println("Sum = " + sum);
    input.close();
  }
}
```
Run Code

Output 1

Enter a number
25
Enter a number
9
Enter a number
5
Enter a number
-3
Sum = 39

Here, the user enters a positive number, that number is added to the sum variable. And this process continues until the number is negative. When the number is negative, the loop terminates and displays the sum without adding the negative number.

Output 2

Enter a number
-8
Sum is 0

Here, the user enters a negative number. The test condition will be false but the code inside of the loop executes once.






## Java break Statement

In this tutorial, you will learn about the break statement, labeled break statement in Java with the help of examples.

While working with loops, it is sometimes desirable to skip some statements inside the loop or terminate the loop immediately without checking the test expression.

In such cases, break and continue statements are used. You will learn about the Java continue statement in the next tutorial.

The break statement in Java terminates the loop immediately, and the control of the program moves to the next statement following the loop.

It is almost always used with decision-making statements (Java if...else Statement).

Here is the syntax of the break statement in Java:

break;


## Java continue Statement

In this tutorial, you will learn about the continue statement and labeled continue statement in Java with the help of examples.

While working with loops, sometimes you might want to skip some statements or terminate the loop. In such cases, break and continue statements are used.

To learn about the break statement, visit Java break. Here, we will learn about the continue statement.
Java continue

The continue statement skips the current iteration of a loop (for, while, do...while, etc).

After the continue statement, the program moves to the end of the loop. And, test expression is evaluated (update statement is evaluated in case of the for loop).

Here's the syntax of the continue statement.

continue;

Note: The continue statement is almost always used in decision-making statements (if...else Statement).


## Java Arrays

In this tutorial, we will learn to work with arrays in Java. We will learn to declare, initialize, and access array elements with the help of examples.

An array is a collection of similar types of data.

For example, if we want to store the names of 100 people then we can create an array of the string type that can store 100 names.

String[] array = new String[100];

Here, the above array cannot store more than 100 names. The number of values in a Java array is always fixed.
How to declare an array in Java?

In Java, here is how we can declare an array.

dataType[] arrayName;

    dataType - it can be primitive data types like int, char, double, byte, etc. or Java objects
    arrayName - it is an identifier

For example,

double[] data;

Here, data is an array that can hold values of type double.

But, how many elements can array this hold?

Good question! To define the number of elements that an array can hold, we have to allocate memory for the array in Java. For example,

// declare an array
double[] data;

// allocate memory
data = new double[10];

Here, the array can store 10 elements. We can also say that the size or length of the array is 10.

In Java, we can declare and allocate the memory of an array in one single statement. For example,

double[] data = new double[10];

How to Initialize Arrays in Java?

In Java, we can initialize arrays during declaration. For example,

//declare and initialize and array
int[] age = {12, 4, 5, 2, 5};

Here, we have created an array named age and initialized it with the values inside the curly brackets.

Note that we have not provided the size of the array. In this case, the Java compiler automatically specifies the size by counting the number of elements in the array (i.e. 5).

In the Java array, each memory location is associated with a number. The number is known as an array index. We can also initialize arrays in Java, using the index number. For example,

// declare an array
int[] age = new int[5];

// initialize array
age[0] = 12;
age[1] = 4;
age[2] = 5;
..

Elements are stored in the array
Java Arrays initialization

Note:

    Array indices always start from 0. That is, the first element of an array is at index 0.
    If the size of an array is n, then the last element of the array will be at index n-1.

How to Access Elements of an Array in Java?

We can access the element of an array using the index number. Here is the syntax for accessing elements of an array,

// access array elements
array[index]

Let's see an example of accessing array elements using index numbers.
Example: Access Array Elements
```java
class Main {
 public static void main(String[] args) {
  
   // create an array
   int[] age = {12, 4, 5, 2, 5};

   // access each array elements
   System.out.println("Accessing Elements of Array:");
   System.out.println("First Element: " + age[0]);
   System.out.println("Second Element: " + age[1]);
   System.out.println("Third Element: " + age[2]);
   System.out.println("Fourth Element: " + age[3]);
   System.out.println("Fifth Element: " + age[4]);
 }
}
```
Run Code

Output

Accessing Elements of Array:
First Element: 12
Second Element: 4
Third Element: 5
Fourth Element: 2
Fifth Element: 5

In the above example, notice that we are using the index number to access each element of the array.

We can use loops to access all the elements of the array at once.
Looping Through Array Elements

In Java, we can also loop through each element of the array. For example,
Example: Using For Loop
```java
class Main {
 public static void main(String[] args) {
  
   // create an array
   int[] age = {12, 4, 5};

   // loop through the array
   // using for loop
   System.out.println("Using for Loop:");
   for(int i = 0; i < age.length; i++) {
     System.out.println(age[i]);
   }
 }
}
```
Run Code

Output

Using for Loop:
12
4
5

In the above example, we are using the for Loop in Java to iterate through each element of the array. Notice the expression inside the loop,

age.length

Here, we are using the length property of the array to get the size of the array.

We can also use the for-each loop to iterate through the elements of an array. For example,
Example: Using the for-each Loop
```java
class Main {
 public static void main(String[] args) {
  
   // create an array
   int[] age = {12, 4, 5};

   // loop through the array
   // using for loop
   System.out.println("Using for-each Loop:");
   for(int a : age) {
     System.out.println(a);
   }
 }
}
```
Run Code

Output

Using for-each Loop:
12
4
5





## Java Multidimensional Arrays

In this tutorial, we will learn about the Java multidimensional array using 2-dimensional arrays and 3-dimensional arrays with the help of examples.

Before we learn about the multidimensional array, make sure you know about Java array.

A multidimensional array is an array of arrays. Each element of a multidimensional array is an array itself. For example,

int[][] a = new int[3][4];

Here, we have created a multidimensional array named a. It is a 2-dimensional array, that can hold a maximum of 12 elements,
2-dimensional array in Java
2-dimensional Array

Remember, Java uses zero-based indexing, that is, indexing of arrays in Java starts with 0 and not 1.

Let's take another example of the multidimensional array. This time we will be creating a 3-dimensional array. For example,

String[][][] data = new String[3][4][2];

Here, data is a 3d array that can hold a maximum of 24 (3*4*2) elements of type String.
How to initialize a 2d array in Java?

Here is how we can initialize a 2-dimensional array in Java.

int[][] a = {
      {1, 2, 3}, 
      {4, 5, 6, 9}, 
      {7}, 
};

As we can see, each element of the multidimensional array is an array itself. And also, unlike C/C++, each row of the multidimensional array in Java can be of different lengths.
2d array example in Java with variable length
Initialization of 2-dimensional Array
Example: 2-dimensional Array
```java
class MultidimensionalArray {
    public static void main(String[] args) {

        // create a 2d array
        int[][] a = {
            {1, 2, 3}, 
            {4, 5, 6, 9}, 
            {7}, 
        };
      
        // calculate the length of each row
        System.out.println("Length of row 1: " + a[0].length);
        System.out.println("Length of row 2: " + a[1].length);
        System.out.println("Length of row 3: " + a[2].length);
    }
}
```
Run Code

Output:

Length of row 1: 3
Length of row 2: 4
Length of row 3: 1

In the above example, we are creating a multidimensional array named a. Since each component of a multidimensional array is also an array (a[0], a[1] and a[2] are also arrays).

Here, we are using the length attribute to calculate the length of each row.
Example: Print all elements of 2d array Using Loop
```java
class MultidimensionalArray {
    public static void main(String[] args) {

        int[][] a = {
            {1, -2, 3}, 
            {-4, -5, 6, 9}, 
            {7}, 
        };
      
        for (int i = 0; i < a.length; ++i) {
            for(int j = 0; j < a[i].length; ++j) {
                System.out.println(a[i][j]);
            }
        }
    }
}
```
Run Code

Output:

1
-2
3
-4
-5
6
9
7

We can also use the for...each loop to access elements of the multidimensional array. For example,
```java
class MultidimensionalArray {
    public static void main(String[] args) {

        // create a 2d array
        int[][] a = {
            {1, -2, 3}, 
            {-4, -5, 6, 9}, 
            {7}, 
        };
      
        // first for...each loop access the individual array
        // inside the 2d array
        for (int[] innerArray: a) {
            // second for...each loop access each element inside the row
            for(int data: innerArray) {
                System.out.println(data);
            }
        }
    }
}
```
Run Code

Output:

1
-2
3
-4
-5
6
9
7

In the above example, we are have created a 2d array named a. We then used for loop and for...each loop to access each element of the array.
How to initialize a 3d array in Java?

Let's see how we can use a 3d array in Java. We can initialize a 3d array similar to the 2d array. For example,

// test is a 3d array
int[][][] test = {
        {
          {1, -2, 3}, 
          {2, 3, 4}
        }, 
        { 
          {-4, -5, 6, 9}, 
          {1}, 
          {2, 3}
        } 
};

Basically, a 3d array is an array of 2d arrays. The rows of a 3d array can also vary in length just like in a 2d array.
Example: 3-dimensional Array
```java
class ThreeArray {
    public static void main(String[] args) {

        // create a 3d array
        int[][][] test = {
            {
              {1, -2, 3}, 
              {2, 3, 4}
            }, 
            { 
              {-4, -5, 6, 9}, 
              {1}, 
              {2, 3}
            } 
        };

        // for..each loop to iterate through elements of 3d array
        for (int[][] array2D: test) {
            for (int[] array1D: array2D) {
                for(int item: array1D) {
                    System.out.println(item);
                }
            }
        }
    }
}
```
Run Code

Output:

1
-2
3
2
3
4
-4
-5
6
9
1
2
3


## Java Class and Objects

In this tutorial, you will learn about the concept of classes and objects in Java with the help of examples.

Java is an object-oriented programming language. The core concept of the object-oriented approach is to break complex problems into smaller objects.

An object is any entity that has a state and behavior. For example, a bicycle is an object. It has

    States: idle, first gear, etc
    Behaviors: braking, accelerating, etc.

Before we learn about objects, let's first know about classes in Java.
Java Class

A class is a blueprint for the object. Before we create an object, we first need to define the class.

We can think of the class as a sketch (prototype) of a house. It contains all the details about the floors, doors, windows, etc. Based on these descriptions we build the house. House is the object.

Since many houses can be made from the same description, we can create many objects from a class.
Create a class in Java

We can create a class in Java using the class keyword. For example,

class ClassName {
  // fields
  // methods
}

Here, fields (variables) and methods represent the state and behavior of the object respectively.

    fields are used to store data
    methods are used to perform some operations

For our bicycle object, we can create the class as
```java
class Bicycle {

  // state or field
  private int gear = 5;

  // behavior or method
  public void braking() {
    System.out.println("Working of Braking");
  }
}
```
In the above example, we have created a class named Bicycle. It contains a field named gear and a method named braking().

Here, Bicycle is a prototype. Now, we can create any number of bicycles using the prototype. And, all the bicycles will share the fields and methods of the prototype.

Note: We have used keywords private and public. These are known as access modifiers. To learn more, visit Java access modifiers.
Java Objects

An object is called an instance of a class. For example, suppose Bicycle is a class then MountainBicycle, SportsBicycle, TouringBicycle, etc can be considered as objects of the class.
Creating an Object in Java

Here is how we can create an object of a class.

className object = new className();

// for Bicycle class
Bicycle sportsBicycle = new Bicycle();

Bicycle touringBicycle = new Bicycle();

We have used the new keyword along with the constructor of the class to create an object. Constructors are similar to methods and have the same name as the class. For example, Bicycle() is the constructor of the Bicycle class. To learn more, visit Java Constructors.

Here, sportsBicycle and touringBicycle are the names of objects. We can use them to access fields and methods of the class.

As you can see, we have created two objects of the class. We can create multiple objects of a single class in Java.

Note: Fields and methods of a class are also called members of the class.
Access Members of a Class

We can use the name of objects along with the . operator to access members of a class. For example,

class Bicycle {

  // field of class
  int gear = 5;

  // method of class
  void braking() {
    ...
  }
}

// create object
Bicycle sportsBicycle = new Bicycle();

// access field and method
sportsBicycle.gear;
sportsBicycle.braking();

In the above example, we have created a class named Bicycle. It includes a field named gear and a method named braking(). Notice the statement,

Bicycle sportsBicycle = new Bicycle();

Here, we have created an object of Bicycle named sportsBicycle. We then use the object to access the field and method of the class.

    sportsBicycle.gear - access the field gear
    sportsBicycle.braking() - access the method braking()

We have mentioned the word method quite a few times. You will learn about Java methods in detail in the next chapter.

Now that we understand what is class and object. Let's see a fully working example.
Example: Java Class and Objects
```java
class Lamp {
  
  // stores the value for light
  // true if light is on
  // false if light is off
  boolean isOn;

  // method to turn on the light
  void turnOn() {
    isOn = true;
    System.out.println("Light on? " + isOn);

  }

  // method to turnoff the light
  void turnOff() {
    isOn = false;
    System.out.println("Light on? " + isOn);
  }
}

class Main {
  public static void main(String[] args) {

    // create objects led and halogen
    Lamp led = new Lamp();
    Lamp halogen = new Lamp();

    // turn on the light by
    // calling method turnOn()
    led.turnOn();

    // turn off the light by
    // calling method turnOff()
    halogen.turnOff();
  }
}
```
Run Code

Output:

Light on? true
Light on? false

In the above program, we have created a class named Lamp. It contains a variable: isOn and two methods: turnOn() and turnOff().

Inside the Main class, we have created two objects: led and halogen of the Lamp class. We then used the objects to call the methods of the class.

    led.turnOn() - It sets the isOn variable to true and prints the output.
    halogen.turnOff() - It sets the isOn variable to false and prints the output.

The variable isOn defined inside the class is also called an instance variable. It is because when we create an object of the class, it is called an instance of the class. And, each instance will have its own copy of the variable.

That is, led and halogen objects will have their own copy of the isOn variable.
Example: Create objects inside the same class

Note that in the previous example, we have created objects inside another class and accessed the members from that class.

However, we can also create objects inside the same class.
```java
class Lamp {
  
  // stores the value for light
  // true if light is on
  // false if light is off
  boolean isOn;

  // method to turn on the light
  void turnOn() {
    isOn = true;
    System.out.println("Light on? " + isOn);

  }

  public static void main(String[] args) {
    
    // create an object of Lamp
    Lamp led = new Lamp();

    // access method using object
    led.turnOn();
  }
}
```
Run Code

Output

Light on? true

Here, we are creating the object inside the main() method of the same class.



## Java Methods

In this tutorial, we will learn about Java methods, how to define methods, and how to use methods in Java programs with the help of examples.
Java Methods

A method is a block of code that performs a specific task.

Suppose you need to create a program to create a circle and color it. You can create two methods to solve this problem:

    a method to draw the circle
    a method to color the circle

Dividing a complex problem into smaller chunks makes your program easy to understand and reusable.

In Java, there are two types of methods:

    User-defined Methods: We can create our own method based on our requirements.
    Standard Library Methods: These are built-in methods in Java that are available to use.

Let's first learn about user-defined methods.
Declaring a Java Method

The syntax to declare a method is:

returnType methodName() {
  // method body
}

Here,

    returnType - It specifies what type of value a method returns For example if a method has an int return type then it returns an integer value.

    If the method does not return a value, its return type is void.
    methodName - It is an identifier that is used to refer to the particular method in a program.
    method body - It includes the programming statements that are used to perform some tasks. The method body is enclosed inside the curly braces { }.

For example,

int addNumbers() {
// code
}

In the above example, the name of the method is adddNumbers(). And, the return type is int. We will learn more about return types later in this tutorial.

This is the simple syntax of declaring a method. However, the complete syntax of declaring a method is

modifier static returnType nameOfMethod (parameter1, parameter2, ...) {
  // method body
}

Here,

    modifier - It defines access types whether the method is public, private, and so on. To learn more, visit Java Access Specifier.
    static - If we use the static keyword, it can be accessed without creating objects.

    For example, the sqrt() method of standard Math class is static. Hence, we can directly call Math.sqrt() without creating an instance of Math class.

    parameter1/parameter2 - These are values passed to a method. We can pass any number of arguments to a method.

Calling a Method in Java

In the above example, we have declared a method named addNumbers(). Now, to use the method, we need to call it.

Here's is how we can call the addNumbers() method.

// calls the method
addNumbers();

Call a method in Java using the name the method followed by a parenthesis
Working of Java Method Call
Example 1: Java Methods
```java
class Main {

  // create a method
  public int addNumbers(int a, int b) {
    int sum = a + b;
    // return value
    return sum;
  }

  public static void main(String[] args) {
    
    int num1 = 25;
    int num2 = 15;

    // create an object of Main
    Main obj = new Main();
    // calling method
    int result = obj.addNumbers(num1, num2);
    System.out.println("Sum is: " + result);
  }
}
```
Run Code

Output

Sum is: 40

In the above example, we have created a method named addNumbers(). The method takes two parameters a and b. Notice the line,

int result = obj.addNumbers(num1, num2);

Here, we have called the method by passing two arguments num1 and num2. Since the method is returning some value, we have stored the value in the result variable.

Note: The method is not static. Hence, we are calling the method using the object of the class.
Java Method Return Type

A Java method may or may not return a value to the function call. We use the return statement to return any value. For example,

int addNumbers() {
...
return sum;
}

Here, we are returning the variable sum. Since the return type of the function is int. The sum variable should be of int type. Otherwise, it will generate an error.
Example 2: Method Return Type
```java
class Main {

// create a method
  public static int square(int num) {

    // return statement
    return num * num;
  }

  public static void main(String[] args) {
    int result;

    // call the method
    // store returned value to result
    result = square(10);

    System.out.println("Squared value of 10 is: " + result);
  }
}
```
Run Code

Output:

Squared value of 10 is: 100

In the above program, we have created a method named square(). The method takes a number as its parameter and returns the square of the number.

Here, we have mentioned the return type of the method as int. Hence, the method should always return an integer value.
Java method returns a value to the method call
Representation of the Java method returning a value

Note: If the method does not return any value, we use the void keyword as the return type of the method. For example,

public void square(int a) {
  int square = a * a;
  System.out.println("Square is: " + square);
}

Method Parameters in Java

A method parameter is a value accepted by the method. As mentioned earlier, a method can also have any number of parameters. For example,

// method with two parameters
int addNumbers(int a, int b) {
  // code
}

// method with no parameter
int addNumbers(){
  // code
}

If a method is created with parameters, we need to pass the corresponding values while calling the method. For example,

// calling the method with two parameters
addNumbers(25, 15);

// calling the method with no parameters
addNumbers()

Example 3: Method Parameters
```java
class Main {

  // method with no parameter
  public void display1() {
    System.out.println("Method without parameter");
  }

  // method with single parameter
  public void display2(int a) {
    System.out.println("Method with a single parameter: " + a);
  }

  public static void main(String[] args) {
    
    // create an object of Main
    Main obj = new Main();

    // calling method with no parameter
    obj.display1();
    
    // calling method with the single parameter
    obj.display2(24);
  }
}
```
Run Code

Output

Method without parameter
Method with a single parameter: 24

Here, the parameter of the method is int. Hence, if we pass any other data type instead of int, the compiler will throw an error. It is because Java is a strongly typed language.

Note: The argument 24 passed to the display2() method during the method call is called the actual argument.

The parameter num accepted by the method definition is known as a formal argument. We need to specify the type of formal arguments. And, the type of actual arguments and formal arguments should always match.
Standard Library Methods

The standard library methods are built-in methods in Java that are readily available for use. These standard libraries come along with the Java Class Library (JCL) in a Java archive (*.jar) file with JVM and JRE.

For example,

    print() is a method of java.io.PrintSteam. The print("...") method prints the string inside quotation marks.
    sqrt() is a method of Math class. It returns the square root of a number.

Here's a working example:
Example 4: Java Standard Library Method

public class Main {
  public static void main(String[] args) {
    
    // using the sqrt() method
    System.out.print("Square root of 4 is: " + Math.sqrt(4));
  }
}

Run Code

Output:

Square root of 4 is: 2.0

To learn more about standard library methods, visit Java Library Methods.
What are the advantages of using methods?

1. The main advantage is code reusability. We can write a method once, and use it multiple times. We do not have to rewrite the entire code each time. Think of it as, "write once, reuse multiple times".
Example 5: Java Method for Code Reusability
```java
public class Main {

  // method defined
  private static int getSquare(int x){
    return x * x;
  }

  public static void main(String[] args) {
    for (int i = 1; i <= 5; i++) {

      // method call
      int result = getSquare(i);
      System.out.println("Square of " + i + " is: " + result);
    }
  }
}
```
Run Code

Output:

Square of 1 is: 1
Square of 2 is: 4
Square of 3 is: 9
Square of 4 is: 16
Square of 5 is: 25

In the above program, we have created the method named getSquare() to calculate the square of a number. Here, the method is used to calculate the square of numbers less than 6.

Hence, the same method is used again and again.

2. Methods make code more readable and easier to debug. Here, the getSquare() method keeps the code to compute the square in a block. Hence, makes it more readable.




## Java Method Overloading

In this article, you’ll learn about method overloading and how you can achieve it in Java with the help of examples.

In Java, two or more methods may have the same name if they differ in parameters (different number of parameters, different types of parameters, or both). These methods are called overloaded methods and this feature is called method overloading. For example:

void func() { ... }
void func(int a) { ... }
float func(double a) { ... }
float func(int a, float b) { ... }

Here, the func() method is overloaded. These methods have the same name but accept different arguments.

Note: The return types of the above methods are not the same. It is because method overloading is not associated with return types. Overloaded methods may have the same or different return types, but they must differ in parameters.
Why method overloading?

Suppose, you have to perform the addition of given numbers but there can be any number of arguments (let’s say either 2 or 3 arguments for simplicity).

In order to accomplish the task, you can create two methods sum2num(int, int) and sum3num(int, int, int) for two and three parameters respectively. However, other programmers, as well as you in the future may get confused as the behavior of both methods are the same but they differ by name.

The better way to accomplish this task is by overloading methods. And, depending upon the argument passed, one of the overloaded methods is called. This helps to increase the readability of the program.
How to perform method overloading in Java?

Here are different ways to perform method overloading:
1. Overloading by changing the number of parameters
```java
class MethodOverloading {
    private static void display(int a){
        System.out.println("Arguments: " + a);
    }

    private static void display(int a, int b){
        System.out.println("Arguments: " + a + " and " + b);
    }

    public static void main(String[] args) {
        display(1);
        display(1, 4);
    }
}
```
Output:

Arguments: 1
Arguments: 1 and 4

2. Method Overloading by changing the data type of parameters
```java
class MethodOverloading {

    // this method accepts int
    private static void display(int a){
        System.out.println("Got Integer data.");
    }

    // this method  accepts String object
    private static void display(String a){
        System.out.println("Got String object.");
    }

    public static void main(String[] args) {
        display(1);
        display("Hello");
    }
}
```
Output:

Got Integer data.
Got String object.

Here, both overloaded methods accept one argument. However, one accepts the argument of type int whereas other accepts String object.

Let’s look at a real-world example:
```java
class HelperService {

    private String formatNumber(int value) {
        return String.format("%d", value);
    }

    private String formatNumber(double value) {
        return String.format("%.3f", value);
    }

    private String formatNumber(String value) {
        return String.format("%.2f", Double.parseDouble(value));
    }

    public static void main(String[] args) {
        HelperService hs = new HelperService();
        System.out.println(hs.formatNumber(500));
        System.out.println(hs.formatNumber(89.9934));
        System.out.println(hs.formatNumber("550"));
    }
}
```
When you run the program, the output will be:

500
89.993
550.00

Note: In Java, you can also overload constructors in a similar way like methods.

Recommended Reading: Java Constructor Overloading
Important Points

    Two or more methods can have the same name inside the same class if they accept different arguments. This feature is known as method overloading.
    Method overloading is achieved by either:
        changing the number of arguments.
        or changing the data type of arguments.
    It is not method overloading if we only change the return type of methods. There must be differences in the number of parameters.






## Java Constructors

In this tutorial, we will learn about Java constructors, their types, and how to use them with the help of examples.
What is a Constructor?

A constructor in Java is similar to a method that is invoked when an object of the class is created.

Unlike Java methods, a constructor has the same name as that of the class and does not have any return type. For example,

class Test {
  Test() {
    // constructor body
  }
}

Here, Test() is a constructor. It has the same name as that of the class and doesn't have a return type.

Recommended Reading: Why do constructors not return values
Example 1: Java Constructor
```java
class Main {
  private String name;

  // constructor
  Main() {
    System.out.println("Constructor Called:");
    name = "Programiz";
  }

  public static void main(String[] args) {

    // constructor is invoked while
    // creating an object of the Main class
    Main obj = new Main();
    System.out.println("The name is " + obj.name);
  }
}
```
Run Code

Output:

Constructor Called:
The name is Programiz

In the above example, we have created a constructor named Main(). Inside the constructor, we are initializing the value of the name variable.

Notice the statement of creating an object of the Main class.

Main obj = new Main();

Here, when the object is created, the Main() constructor is called. And, the value of the name variable is initialized.

Hence, the program prints the value of the name variables as Programiz.
Types of Constructor

In Java, constructors can be divided into 3 types:

    No-Arg Constructor
    Parameterized Constructor
    Default Constructor

## 1. Java No-Arg Constructors

Similar to methods, a Java constructor may or may not have any parameters (arguments).

If a constructor does not accept any parameters, it is known as a no-argument constructor. For example,

private Constructor() {
   // body of the constructor
}

Example 2: Java private no-arg constructor
```java
class Main {

  int i;

  // constructor with no parameter
  private Main() {
    i = 5;
    System.out.println("Constructor is called");
  }

  public static void main(String[] args) {

    // calling the constructor without any parameter
    Main obj = new Main();
    System.out.println("Value of i: " + obj.i);
  }
}
```
Run Code

Output:

Constructor is called
Value of i: 5

In the above example, we have created a constructor Main(). Here, the constructor does not accept any parameters. Hence, it is known as a no-arg constructor.

Notice that we have declared the constructor as private.

Once a constructor is declared private, it cannot be accessed from outside the class. So, creating objects from outside the class is prohibited using the private constructor.

Here, we are creating the object inside the same class. Hence, the program is able to access the constructor. To learn more, visit Java Implement Private Constructor.

However, if we want to create objects outside the class, then we need to declare the constructor as public.
Example 3: Java public no-arg constructors
```java
class Company {
  String name;

  // public constructor
  public Company() {
    name = "Programiz";
  }
}

class Main {
  public static void main(String[] args) {

    // object is created in another class
    Company obj = new Company();
    System.out.println("Company name = " + obj.name);
  }
}
```
Run Code

Output:

Company name = Programiz

Recommended Reading: Java Access Modifier
### 2. Java Parameterized Constructor

A Java constructor can also accept one or more parameters. Such constructors are known as parameterized constructors (constructor with parameters).
Example 4: Parameterized constructor
```java
class Main {

  String languages;

  // constructor accepting single value
  Main(String lang) {
    languages = lang;
    System.out.println(languages + " Programming Language");
  }

  public static void main(String[] args) {

    // call constructor by passing a single value
    Main obj1 = new Main("Java");
    Main obj2 = new Main("Python");
    Main obj3 = new Main("C");
  }
}
```
Run Code

Output:

Java Programming Language
Python Programming Language
C Programming Language

In the above example, we have created a constructor named Main(). Here, the constructor takes a single parameter. Notice the expression,

Main obj1 = new Main("Java");

Here, we are passing the single value to the constructor. Based on the argument passed, the language variable is initialized inside the constructor.
3. Java Default Constructor

If we do not create any constructor, the Java compiler automatically create a no-arg constructor during the execution of the program. This constructor is called default constructor.
Example 5: Default Constructor
```java
class Main {

  int a;
  boolean b;

  public static void main(String[] args) {

    // A default constructor is called
    Main obj = new Main();

    System.out.println("Default Value:");
    System.out.println("a = " + obj.a);
    System.out.println("b = " + obj.b);
  }
}
```
Run Code

Output:

Default Value:
a = 0
b = false

Here, we haven't created any constructors. Hence, the Java compiler automatically creates the default constructor.

The default constructor initializes any uninitialized instance variables with default values.
Type
					Default Value
			
boolean
					false
			
byte
					0
			
short
					0
			
int
					0
			
long
					0L
			
char
					\u0000
			
float
					0.0f
			
double
					0.0d
			
object
					Reference null
			

In the above program, the variables a and b are initialized with default value 0 and false respectively.

The above program is equivalent to:
```java
class Main {

  int a;
  boolean b;

   Main() {
    a = 0;
    b = false;
  }

  public static void main(String[] args) {
    // call the constructor
    Main obj = new Main();

    System.out.println("Default Value:");
    System.out.println("a = " + obj.a);
    System.out.println("b = " + obj.b);
  }
}
```
Run Code

The output of the program is the same as Example 5.
Important Notes on Java Constructors

    Constructors are invoked implicitly when you instantiate objects.
    The two rules for creating a constructor are:
    The name of the constructor should be the same as the class.
    A Java constructor must not have a return type.
    If a class doesn't have a constructor, the Java compiler automatically creates a default constructor during run-time. The default constructor initializes instance variables with default values. For example, the int variable will be initialized to 0
    Constructor types:
    No-Arg Constructor - a constructor that does not accept any arguments
    Parameterized constructor - a constructor that accepts arguments
    Default Constructor - a constructor that is automatically created by the Java compiler if it is not explicitly defined.
    A constructor cannot be abstract or static or final.
    A constructor can be overloaded but can not be overridden.

## Constructors Overloading in Java

Similar to Java method overloading, we can also create two or more constructors with different parameters. This is called constructors overloading.
Example 6: Java Constructor Overloading
```java
class Main {

  String language;

  // constructor with no parameter
  Main() {
    this.language = "Java";
  }

  // constructor with a single parameter
  Main(String language) {
    this.language = language;
  }

  public void getName() {
    System.out.println("Programming Langauage: " + this.language);
  }

  public static void main(String[] args) {

    // call constructor with no parameter
    Main obj1 = new Main();

    // call constructor with a single parameter
    Main obj2 = new Main("Python");

    obj1.getName();
    obj2.getName();
  }
}
```
Run Code

Output:

Programming Language: Java
Programming Language: Python

In the above example, we have two constructors: Main() and Main(String language). Here, both the constructor initialize the value of the variable language with different values.

Based on the parameter passed during object creation, different constructors are called and different values are assigned.

It is also possible to call one constructor from another constructor. To learn more, visit Java Call One Constructor from Another.





## Java Strings

In this tutorial, we will learn about Java strings, how to create them, and various methods of the String class with the help of examples.

In Java, a string is a sequence of characters. For example, "hello" is a string containing a sequence of characters 'h', 'e', 'l', 'l', and 'o'.

We use double quotes to represent a string in Java. For example,

// create a string
String type = "Java programming";

Here, we have created a string variable named type. The variable is initialized with the string Java Programming.
Example: Create a String in Java
```java
class Main {
  public static void main(String[] args) {
    
    // create strings
    String first = "Java";
    String second = "Python";
    String third = "JavaScript";

    // print strings
    System.out.println(first);   // print Java
    System.out.println(second);  // print Python
    System.out.println(third);   // print JavaScript
  }
}
```
Run Code

In the above example, we have created three strings named first, second, and third. Here, we are directly creating strings like primitive types.

However, there is another way of creating Java strings (using the new keyword). We will learn about that later in this tutorial.

Note: Strings in Java are not primitive types (like int, char, etc). Instead, all strings are objects of a predefined class named String.

And, all string variables are instances of the String class.
Java String Operations

Java String provides various methods to perform different operations on strings. We will look into some of the commonly used string operations.
1. Get length of a String

To find the length of a string, we use the length() method of the String. For example,
```java
class Main {
  public static void main(String[] args) {

    // create a string
    String greet = "Hello! World";
    System.out.println("String: " + greet);

    // get the length of greet
    int length = greet.length();

    System.out.println("Length: " + length);
  }
}
```
Run Code

Output

String: Hello! World
Length: 12

In the above example, the length() method calculates the total number of characters in the string and returns it. To learn more, visit Java String length().
2. Join Two Java Strings

We can join two strings in Java using the concat() method. For example,
```java
class Main {
  public static void main(String[] args) {

    // create first string
    String first = "Java ";
    System.out.println("First String: " + first);

    // create second
    String second = "Programming";
    System.out.println("Second String: " + second);

    // join two strings
    String joinedString = first.concat(second);

    System.out.println("Joined String: " + joinedString);
  }
}
```
Run Code

Output

First String: Java 
Second String: Programming     
Joined String: Java Programming

In the above example, we have created two strings named first and second. Notice the statement,

String joinedString = first.concat(second);

Here, the concat() method joins the second string to the first string and assigns it to the joinedString variable.

We can also join two strings using the + operator in Java. To learn more, visit Java String concat().
3. Compare two Strings

In Java, we can make comparisons between two strings using the equals() method. For example,
```java
class Main {
  public static void main(String[] args) {

    // create 3 strings
    String first = "java programming";
    String second = "java programming";
    String third = "python programming";

    // compare first and second strings
    boolean result1 = first.equals(second);

    System.out.println("Strings first and second are equal: " + result1);

    // compare first and third strings
    boolean result2 = first.equals(third);

    System.out.println("Strings first and third are equal: " + result2);
  }
}
```
Run Code

Output

Strings first and second are equal: true
Strings first and third are equal: false

In the above example, we have created 3 strings named first, second, and third. Here, we are using the equal() method to check if one string is equal to another.

The equals() method checks the content of strings while comparing them. To learn more, visit Java String equals().

Note: We can also compare two strings using the == operator in Java. However, this approach is different than the equals() method. To learn more, visit Java String == vs equals().
Escape character in Java Strings

The escape character is used to escape some of the characters present inside a string.

Suppose we need to include double quotes inside a string.

// include double quote 
String example = "This is the "String" class";

Since strings are represented by double quotes, the compiler will treat "This is the " as the string. Hence, the above code will cause an error.

To solve this issue, we use the escape character \ in Java. For example,

// use the escape character
String example = "This is the \"String\" class.";

Now escape characters tell the compiler to escape double quotes and read the whole text.
Java Strings are Immutable

In Java, strings are immutable. This means, once we create a string, we cannot change that string.

To understand it more deeply, consider an example:

// create a string
String example = "Hello! ";

Here, we have created a string variable named example. The variable holds the string "Hello! ".

Now suppose we want to change the string.

// add another string "World"
// to the previous tring example
example = example.concat(" World");

Here, we are using the concat() method to add another string World to the previous string.

It looks like we are able to change the value of the previous string. However, this is not true.

Let's see what has happened here,

    JVM takes the first string "Hello! "
    creates a new string by adding "World" to the first string
    assign the new string "Hello! World" to the example variable
    the first string "Hello! " remains unchanged

Creating strings using the new keyword

So far we have created strings like primitive types in Java.

Since strings in Java are objects, we can create strings using the new keyword as well. For example,

// create a string using the new keyword
String name = new String("Java String");

In the above example, we have created a string name using the new keyword.

Here, when we create a string object, the String() constructor is invoked. To learn more about constructor, visit Java Constructor.

Note: The String class provides various other constructors to create strings. To learn more, visit Java String (official Java documentation).
Example: Create Java Strings using the new keyword
```java
class Main {
  public static void main(String[] args) {

    // create a string using new
    String name = new String("Java String");


    System.out.println(name);  // print Java String
  }
}
```java
Run Code
Create String using literals vs new keyword

Now that we know how strings are created using string literals and the new keyword, let's see what is the major difference between them.

In Java, the JVM maintains a string pool to store all of its strings inside the memory. The string pool helps in reusing the strings.

1. While creating strings using string literals,

String example = "Java";

Here, we are directly providing the value of the string (Java). Hence, the compiler first checks the string pool to see if the string already exists.

    If the string already exists, the new string is not created. Instead, the new reference, example points to the already existed string (Java).
    If the string doesn't exist, the new string (Java is created.

2. While creating strings using the new keyword,

String example = new String("Java");

Here, the value of the string is not directly provided. Hence, a new "Java" string is created even though "Java" is already present inside the memory pool.
Methods of Java String

Besides those mentioned above, there are various string methods present in Java. Here are some of those methods:
```java
Methods
	Description
contains()
	checks whether the string contains a substring
substring()
	returns the substring of the string
join()
	join the given strings using the delimiter
replace()
	replaces the specified old character with the specified new character
replaceAll()
	replaces all substrings matching the regex pattern
replaceFirst()
	replace the first matching substring
charAt()
	returns the character present in the specified location
getBytes()
	converts the string to an array of bytes
indexOf()
	returns the position of the specified character in the string
compareTo()
	compares two strings in the dictionary order
compareToIgnoreCase()
	compares two strings ignoring case differences
trim()
	removes any leading and trailing whitespaces
format()
	returns a formatted string
split()
	breaks the string into an array of strings
toLowerCase()
	converts the string to lowercase
toUpperCase()
	converts the string to uppercase
valueOf()
	returns the string representation of the specified argument
toCharArray()
	converts the string to a char array
matches()
	checks whether the string matches the given regex
startsWith()
	checks if the string begins with the given string
endsWith()
	checks if the string ends with the given string
isEmpty()
	checks whether a string is empty of not
intern() 
	returns the canonical representation of the string
contentEquals()
	checks whether the string is equal to charSequence
hashCode()
	returns a hash code for the string
subSequence()
	returns a subsequence from the string
``` 






## Java Access Modifiers

In this tutorial, we will learn about the Java Access Modifier, its types, and how to use them with the help of examples.
What are Access Modifiers?

In Java, access modifiers are used to set the accessibility (visibility) of classes, interfaces, variables, methods, constructors, data members, and the setter methods. For example,

class Animal {
    public void method1() {...}

   private void method2() {...}
}

In the above example, we have declared 2 methods: method1() and method2(). Here,

    method1 is public - This means it can be accessed by other classes.
    method2 is private - This means it can not be accessed by other classes.

Note the keyword public and private. These are access modifiers in Java. They are also known as visibility modifiers.

Note: You cannot set the access modifier of getters methods.
Types of Access Modifier

Before you learn about types of access modifiers, make sure you know about Java Packages.

There are four access modifiers keywords in Java and they are:
Modifier
				Description
		
Default
				declarations are visible only within the package (package private)
		
Private
				declarations are visible within the class only
		
Protected
				declarations are visible within the package or all subclasses
		
Public
				declarations are visible everywhere
		
Default Access Modifier

If we do not explicitly specify any access modifier for classes, methods, variables, etc, then by default the default access modifier is considered. For example,

package defaultPackage;

```java
class Logger {
    void message(){
        System.out.println("This is a message");
    }
}
```
Run Code

Here, the Logger class has the default access modifier. And the class is visible to all the classes that belong to the defaultPackage package. However, if we try to use the Logger class in another class outside of defaultPackage, we will get a compilation error.
Private Access Modifier

When variables and methods are declared private, they cannot be accessed outside of the class. For example,
```java
class Data {
    // private variable
    private String name;
}

public class Main {
    public static void main(String[] main){

        // create an object of Data
        Data d = new Data();

        // access private variable and field from another class
        d.name = "Programiz";
    }
}
```
Run Code

In the above example, we have declared a private variable named name. When we run the program, we will get the following error:

Main.java:18: error: name has private access in Data
        d.name = "Programiz";
         ^

The error is generated because we are trying to access the private variable of the Data class from the Main class.

You might be wondering what if we need to access those private variables. In this case, we can use the getters and setters method. For example,
```java
class Data {
    private String name;

    // getter method
    public String getName() {
        return this.name;
    }
    // setter method
    public void setName(String name) {
        this.name= name;
    }
}
public class Main {
    public static void main(String[] main){
        Data d = new Data();

        // access the private variable using the getter and setter
        d.setName("Programiz");
        System.out.println(d.getName());
    }
}
```
Run Code

Output:

The name is Programiz

In the above example, we have a private variable named name. In order to access the variable from the outer class, we have used methods: getName() and setName(). These methods are called getter and setter in Java.

Here, we have used the setter method (setName()) to assign value to the variable and the getter method (getName()) to access the variable.

We have used this keyword inside the setName() to refer to the variable of the class. To learn more on this keyword, visit Java this Keyword.

Note: We cannot declare classes and interfaces private in Java. However, the nested classes can be declared private. To learn more, visit Java Nested and Inner Class.
Protected Access Modifier

When methods and data members are declared protected, we can access them within the same package as well as from subclasses. For example,
```java
class Animal {
    // protected method
    protected void display() {
        System.out.println("I am an animal");
    }
}

class Dog extends Animal {
    public static void main(String[] args) {

        // create an object of Dog class
        Dog dog = new Dog();
         // access protected method
        dog.display();
    }
}
```
Run Code

Output:

I am an animal

In the above example, we have a protected method named display() inside the Animal class. The Animal class is inherited by the Dog class. To learn more about inheritance, visit Java Inheritance.

We then created an object dog of the Dog class. Using the object we tried to access the protected method of the parent class.

Since protected methods can be accessed from the child classes, we are able to access the method of Animal class from the Dog class.

Note: We cannot declare classes or interfaces protected in Java.
## Public Access Modifier

When methods, variables, classes, and so on are declared public, then we can access them from anywhere. The public access modifier has no scope restriction. For example,
```java
// Animal.java file
// public class
public class Animal {
    // public variable
    public int legCount;

    // public method
    public void display() {
        System.out.println("I am an animal.");
        System.out.println("I have " + legCount + " legs.");
    }
}

// Main.java
public class Main {
    public static void main( String[] args ) {
        // accessing the public class
        Animal animal = new Animal();

        // accessing the public variable
        animal.legCount = 4;
        // accessing the public method
        animal.display();
    }
}
```
Run Code

Output:

I am an animal.
I have 4 legs.

Here,

    The public class Animal is accessed from the Main class.
    The public variable legCount is accessed from the Main class.
    The public method display() is accessed from the Main class.






## Java this Keyword

In this article, we will learn about this keyword in Java, how and where to use them with the help of examples.
this Keyword

In Java, this keyword is used to refer to the current object inside a method or a constructor. For example,
```java
class Main {
    int instVar;

    Main(int instVar){
        this.instVar = instVar;
        System.out.println("this reference = " + this);
    }

    public static void main(String[] args) {
        Main obj = new Main(8);
        System.out.println("object reference = " + obj);
    }
}
```
Run Code

Output:

this reference = Main@23fc625e
object reference = Main@23fc625e

In the above example, we created an object named obj of the class Main. We then print the reference to the object obj and this keyword of the class.

Here, we can see that the reference of both obj and this is the same. It means this is nothing but the reference to the current object.
Use of this Keyword

There are various situations where this keyword is commonly used.
Using this for Ambiguity Variable Names

In Java, it is not allowed to declare two or more variables having the same name inside a scope (class scope or method scope). However, instance variables and parameters may have the same name. For example,

class MyClass {
    // instance variable
    int age;

    // parameter
    MyClass(int age){
        age = age;
    }
}

In the above program, the instance variable and the parameter have the same name: age. Here, the Java compiler is confused due to name ambiguity.

In such a situation, we use this keyword. For example,

First, let's see an example without using this keyword:
```java
class Main {

    int age;
    Main(int age){
        age = age;
    }

    public static void main(String[] args) {
        Main obj = new Main(8);
        System.out.println("obj.age = " + obj.age);
    }
}
```
Run Code

Output:

obj.age = 0

In the above example, we have passed 8 as a value to the constructor. However, we are getting 0 as an output. This is because the Java compiler gets confused because of the ambiguity in names between instance the variable and the parameter.

Now, let's rewrite the above code using this keyword.
```java
class Main {

    int age;
    Main(int age){
        this.age = age;
    }

    public static void main(String[] args) {
        Main obj = new Main(8);
        System.out.println("obj.age = " + obj.age);
    }
}
```
Run Code

Output:

obj.age = 8

Now, we are getting the expected output. It is because when the constructor is called, this inside the constructor is replaced by the object obj that has called the constructor. Hence the age variable is assigned value 8.

Also, if the name of the parameter and instance variable is different, the compiler automatically appends this keyword. For example, the code:
```java
class Main {
    int age;

    Main(int i) {
        age = i;
    }
}

is equivalent to:

class Main {
    int age;

    Main(int i) {
        this.age = i;
    }
}
```
this with Getters and Setters

Another common use of this keyword is in setters and getters methods of a class. For example:
```java
class Main {
   String name;

   // setter method
   void setName( String name ) {
       this.name = name;
   }

   // getter method
   String getName(){
       return this.name;
   }

   public static void main( String[] args ) {
       Main obj = new Main();

       // calling the setter and the getter method
       obj.setName("Toshiba");
       System.out.println("obj.name: "+obj.getName());
   }
}
```
Run Code

Output:

obj.name: Toshiba

Here, we have used this keyword:

    to assign value inside the setter method
    to access value inside the getter method





## Java final keyword

In this tutorial, we will learn about Java final variables, methods and classes with examples.

In Java, the final keyword is used to denote constants. It can be used with variables, methods, and classes.

Once any entity (variable, method or class) is declared final, it can be assigned only once. That is,

    the final variable cannot be reinitialized with another value
    the final method cannot be overridden
    the final class cannot be extended

### 1. Java final Variable

In Java, we cannot change the value of a final variable. For example,
```java
class Main {
  public static void main(String[] args) {

    // create a final variable
    final int AGE = 32;

    // try to change the final variable
    AGE = 45;
    System.out.println("Age: " + AGE);
  }
}
```
Run Code

In the above program, we have created a final variable named age. And we have tried to change the value of the final variable.

When we run the program, we will get a compilation error with the following message.

cannot assign a value to final variable AGE
    AGE = 45;
    ^

Note: It is recommended to use uppercase to declare final variables in Java.
### 2. Java final Method

Before you learn about final methods and final classes, make sure you know about the Java Inheritance.

In Java, the final method cannot be overridden by the child class. For example,
```java
class FinalDemo {
    // create a final method
    public final void display() {
      System.out.println("This is a final method.");
    }
}

class Main extends FinalDemo {
  // try to override final method
  public final void display() {
    System.out.println("The final method is overridden.");
  }

  public static void main(String[] args) {
    Main obj = new Main();
    obj.display();
  }
}
```
Run Code

In the above example, we have created a final method named display() inside the FinalDemo class. Here, the Main class inherits the FinalDemo class.

We have tried to override the final method in the Main class. When we run the program, we will get a compilation error with the following message.

 display() in Main cannot override display() in FinalDemo
  public final void display() {
                    ^
  overridden method is final

### 3. Java final Class

In Java, the final class cannot be inherited by another class. For example,
```java
// create a final class
final class FinalClass {
  public void display() {
    System.out.println("This is a final method.");
  }
}

// try to extend the final class
class Main extends FinalClass {
  public  void display() {
    System.out.println("The final method is overridden.");
  }

  public static void main(String[] args) {
    Main obj = new Main();
    obj.display();
  }
}
```
Run Code

In the above example, we have created a final class named FinalClass. Here, we have tried to inherit the final class by the Main class.

When we run the program, we will get a compilation error with the following message.

cannot inherit from final FinalClass
class Main extends FinalClass {
                   ^





## Java Recursion

In this tutorial, you will learn about Java recursive function, its advantages and disadvantages.

In Java, a method that calls itself is known as a recursive method. And, this process is known as recursion.

A physical world example would be to place two parallel mirrors facing each other. Any object in between them would be reflected recursively.
How Recursion works?
A function is calling itself
Working of Java Recursion

In the above example, we have called the recurse() method from inside the main method. (normal method call). And, inside the recurse() method, we are again calling the same recurse method. This is a recursive call.

In order to stop the recursive call, we need to provide some conditions inside the method. Otherwise, the method will be called infinitely.

Hence, we use the if...else statement (or similar approach) to terminate the recursive call inside the method.
Example: Factorial of a Number Using Recursion
```java
class Factorial {

    static int factorial( int n ) {
        if (n != 0)  // termination condition
            return n * factorial(n-1); // recursive call
        else
            return 1;
    }

    public static void main(String[] args) {
        int number = 4, result;
        result = factorial(number);
        System.out.println(number + " factorial = " + result);
    }
}
```
Run Code

Output:

4 factorial = 24

In the above example, we have a method named factorial(). The factorial() is called from the main() method. with the number variable passed as an argument.

Here, notice the statement,

return n * factorial(n-1);

The factorial() method is calling itself. Initially, the value of n is 4 inside factorial(). During the next recursive call, 3 is passed to the factorial() method. This process continues until n is equal to 0.

When n is equal to 0, the if statement returns false hence 1 is returned. Finally, the accumulated result is passed to the main() method.



## Java instanceof Operator

In this tutorial, you will learn about Java instanceof operator in detail with the help of examples.

The instanceof operator in Java is used to check whether an object is an instance of a particular class or not.

Its syntax is

objectName instanceOf className;

Here, if objectName is an instance of className, the operator returns true. Otherwise, it returns false.
Example: Java instanceof
```java
class Main {

  public static void main(String[] args) {

    // create a variable of string type
    String name = "Programiz";
    
    // checks if name is instance of String
    boolean result1 = name instanceof String;
    System.out.println("name is an instance of String: " + result1);

    // create an object of Main
    Main obj = new Main();

    // checks if obj is an instance of Main
    boolean result2 = obj instanceof Main;
    System.out.println("obj is an instance of Main: " + result2);
  }
}
```
Run Code

Output

name is an instance of String: true
obj is an instance of Main: true

In the above example, we have created a variable name of the String type and an object obj of the Main class.

