1. What is C++?
C++ is a programming language used to build:
Software
Games
Applications
System programs
Competitive programming solutions
Data Structures & Algorithms


2. Your first C++ program
Create a file:
hello.cpp

Write:
#include <iostream>
using namespace std;
int main() {
    cout << "Hello, World!";
    return 0;
}

Output
Hello, World!

3. Understand every line
Line 1
#include <iostream>
iostream gives us input/output functionality.
It allows us to use:
cout
cin

Think:
iostream
   ↓
Input + Output
   ↓
cin + cout

Line 2
using namespace std;
std is the standard namespace in C++.
This allows us to write:

cout
instead of:
std::cout
For beginners, we'll use:
using namespace std;

Line 3
int main() {
main() is the starting point of a C++ program.
When your program runs, execution starts from:
main()
The { starts the body of the function.

Line 4
cout << "Hello, World!";
cout means character output.
It prints something on the screen.
Example:
cout << "Pallavi";

Output:
Pallavi
Line 5
return 0;

It tells the operating system that the program finished successfully.
For now, remember:
return 0; = program completed successfully.

Line 6
}
This closes main().

4. Very important syntax
C++ is case-sensitive.
This:
cout
is correct.

This:
Cout

is different and will cause an error.
Also remember the semicolon:
cout << "Hello";
Usually, a C++ statement ends with:
;

5. Print multiple things
Try:
#include <iostream>
using namespace std;
int main() {
    cout << "My name is Pallavi";
    cout << "I am learning C++";
    cout << "I am studying MCA";
    return 0;
}

The output will appear on the same line.
To move to a new line
cout << "My name is Pallavi" << endl;
cout << "I am learning C++" << endl;
cout << "I am studying MCA" << endl;

Output:
My name is Pallavi
I am learning C++
I am studying MCA

endl
endl means end the current line.

You can also use:
cout << "Hello\n";


🧠 C++ Basics at a Glance
| Concept  | Meaning         | Example                    | Remember          |
| -------- | --------------- | -------------------------- | ----------------- |
| `int`    | Whole number    | `int age = 22;`            | 🔢 Number         |
| `float`  | Decimal         | `float marks = 85.5;`      | 🔢 Decimal        |
| `double` | Precise decimal | `double price = 99.999;`   | 🎯 More precision |
| `char`   | One character   | `char grade = 'A';`        | 🔤 Single         |
| `string` | Text            | `string name = "Pallavi";` | 📝 Text           |
| `bool`   | True/False      | `bool pass = true;`        | ✅ / ❌             |
| `cout`   | Display output  | `cout << age;`             | 📤 Output         |
| `cin`    | Take input      | `cin >> age;`              | 📥 Input          |

📦 Variable = Box
Think like this:

          VARIABLE
             ↓
      ┌─────────────┐
      │     22      │
      └─────────────┘
             ↑
           age

Code:
int age = 22;
Formula
DATA TYPE + VARIABLE NAME + VALUE
      ↓          ↓           ↓
     int        age          22
📥 Input & 📤 Output
             C++
              │
       ┌──────┴──────┐
       ↓             ↓
     cin            cout
       ↓             ↓
    INPUT          OUTPUT
       ↓             ↓
    Keyboard       Screen

Input
cin >> age;
Output
cout << age;
Easy trick

cin = IN 📥
cout = OUT 📤

🔢 Data Types Chart
DATA TYPES
    │
    ├── int
    │     └── 10, 25, 100
    │
    ├── float
    │     └── 10.5, 85.5
    │
    ├── double
    │     └── 10.555555
    │
    ├── char
    │     └── 'A', 'B', '7'
    │
    ├── string
    │     └── "Pallavi"
    │
    └── bool
          └── true / false
➕ Arithmetic Operators
| Symbol | Meaning   | Example  | Result |
| ------ | --------- | -------- | -----: |
| `+`    | Add       | `10 + 3` |   `13` |
| `-`    | Subtract  | `10 - 3` |    `7` |
| `*`    | Multiply  | `10 * 3` |   `30` |
| `/`    | Divide    | `10 / 3` |    `3` |
| `%`    | Remainder | `10 % 3` |    `1` |

⭐ Most Important for DSA
% = REMAINDER

Example:

10 ÷ 3

Quotient  = 3
Remainder = 1

Therefore:
10 % 3 = 1

You'll use % for:

Even / Odd
   ↓
number % 2

Last digit
   ↓
number % 10

Digit problems
   ↓
number % 10
🔄 Increment & Decrement
x++  →  increase by 1
x--  →  decrease by 1

Example:
int x = 5;

x++;
Before → 5
  ↓
 x++
  ↓
After  → 6

And:

x--;
Before → 5
  ↓
 x--
  ↓
After  → 4
Remember
++ → UP ⬆️
-- → DOWN ⬇️

📝 C++ Syntax Recall

#include <iostream>
using namespace std;
int main() {
    // Your code
    return 0;
}
=============================================================================
1. if Statement

Definition	
if is used to execute code when a condition is true.
Syntax
	if (condition) { }
Example
	if (age >= 18) { cout << "Adult"; }
Remember
	if = check condition

Condition
   ↓
 TRUE? ─── YES ──→ Execute if block
   │
   NO
   ↓
 Skip


2. if-else

Definition
	Used when there are two possible outcomes.
Syntax
	if (condition) { } else { }
Example	
Check whether a person is an adult or minor.
Remember

if = yes, else = no
if (age >= 18) {
    cout << "Adult";
}
else {
    cout << "Minor";
}

Output
Adult
if age = 20.

3. else if

Definition
	Used to check multiple conditions.
Syntax	
    if (...) { } else if (...) { } else { }
Example	
    Grade calculation
Remember	
    Multiple choices
    if (marks >= 90) {
    cout << "A";
}
else if (marks >= 75) {
    cout << "B";
}
else if (marks >= 50) {
    cout << "C";
}
else {
    cout << "Fail";
}


Example
marks = 82
     ↓
82 >= 90 ❌
     ↓
82 >= 75 ✅
     ↓
Output = B
4. Comparison Operators ⭐

| Operator | Definition            | Example  | Result |
| -------- | --------------------- | -------- | ------ |
| `==`     | Equal to              | `5 == 5` | `true` |
| `!=`     | Not equal             | `5 != 3` | `true` |
| `>`      | Greater than          | `5 > 3`  | `true` |
| `<`      | Less than             | `3 < 5`  | `true` |
| `>=`     | Greater than or equal | `5 >= 5` | `true` |
| `<=`     | Less than or equal    | `3 <= 5` | `true` |

5. = vs == 🚨
| Symbol | Definition          | Example   |
| ------ | ------------------- | --------- |
| `=`    | Assigns a value     | `x = 10;` |
| `==`   | Compares two values | `x == 10` |

6. Logical AND &&
| Part           | Details                                         |
| -------------- | ----------------------------------------------- |
| **Definition** | Returns true when **both conditions are true**. |
| **Syntax**     | `condition1 && condition2`                      |
| **Example**    | `age >= 18 && age <= 60`                        |
| **Remember**   | AND = BOTH                                      |


7. Logical OR ||
| Part           | Details                                               |   |             |
| -------------- | ----------------------------------------------------- | - | ----------- |
| **Definition** | Returns true when **at least one condition is true**. |   |             |
| **Syntax**     | `condition1                                           |   | condition2` |
| **Example**    | `day == 1                                             |   | day == 7`   |
| **Remember**   | OR = ANY ONE                                          |   |             |

if (day == 1 || day == 7) {
    cout << "Weekend";
}

8. Logical NOT !
| Part           | Details                       |
| -------------- | ----------------------------- |
| **Definition** | Reverses a Boolean condition. |
| **Syntax**     | `!condition`                  |
| **Example**    | `!isStudent`                  |
| **Remember**   | NOT = REVERSE                 |

9. Arithmetic Operators
| Operator | Definition     | Example | Answer |
| -------- | -------------- | ------- | -----: |
| `+`      | Addition       | `5 + 2` |    `7` |
| `-`      | Subtraction    | `5 - 2` |    `3` |
| `*`      | Multiplication | `5 * 2` |   `10` |
| `/`      | Division       | `5 / 2` |   `2`* |
| `%`      | Remainder      | `5 % 2` |    `1` |

1. What is a Loop?
Definition
A loop is used to execute a block of code repeatedly until a condition becomes false.

Easy Example
Instead of writing:

cout << "Hello" << endl;
cout << "Hello" << endl;
cout << "Hello" << endl;
cout << "Hello" << endl;
cout << "Hello" << endl;

We can use a loop:

for (int i = 1; i <= 5; i++) {
    cout << "Hello" << endl;
}
Remember
Loop = Repeat code

2. Types of Loops
                 LOOPS
                   |
        +----------+----------+
        |          |          |
       for       while     do-while
        |          |          |
     Known      Condition   Runs at
     repeats    checked     least once

3. for Loop ⭐⭐⭐
Definition

A for loop is used when you generally know how many times you want to repeat something.

Syntax
for (initialization; condition; update) {
    // code
}
Example
for (int i = 1; i <= 5; i++) {
    cout << i << endl;
}
Output
1
2
3
4
5
4. Understand for Loop

Look at:

for (int i = 1; i <= 5; i++)

It has 3 parts:

for ( initialization ; condition ; update )
       ↓                ↓          ↓
     Start            Check      Change
Example
int i = 1
   ↓
Start from 1

i <= 5
   ↓
Continue while i is <= 5

i++
   ↓
Increase i by 1
5. for Loop Dry Run ⭐

Code:

for (int i = 1; i <= 5; i++) {
    cout << i << endl;
}

Dry run:

i = 1
1 <= 5 → TRUE → print 1
i++

i = 2
2 <= 5 → TRUE → print 2
i++

i = 3
3 <= 5 → TRUE → print 3
i++

i = 4
4 <= 5 → TRUE → print 4
i++

i = 5
5 <= 5 → TRUE → print 5
i++

i = 6
6 <= 5 → FALSE → STOP
6. while Loop
Definition

A while loop repeatedly executes code while a condition is true.

Syntax
while (condition) {
    // code
}
Example
int i = 1;

while (i <= 5) {
    cout << i << endl;
    i++;
}
Output
1
2
3
4
5
Remember
while = Check first → Then execute
7. while Loop Flow
       Start
         ↓
    Check condition
         ↓
      TRUE?
      /   \
    YES    NO
     ↓      ↓
   Code    STOP
     ↓
   Update
     ↓
 Check again
8. do-while Loop
Definition

A do-while loop executes the code at least once, then checks the condition.

Syntax
do {
    // code
} while (condition);
Example
int i = 1;

do {
    cout << i << endl;
    i++;
} while (i <= 5);
Output
1
2
3
4
5

What is OOP?
OOP = Object-Oriented Programming
OOP is a programming approach where we organize programs using classes and objects.

 Example
Think about a Student.

A student has:
Properties → name, age, marks
Behaviors  → study(), attendClass(), giveExam()

In C++:
Class  → Blueprint
Object → Real instance of the blueprint
4 Main Pillars of OOP
              OOP
               |
    ┌──────────┼──────────┐
    ↓          ↓          ↓
Encapsulation Inheritance Polymorphism
               |
          Abstraction
Quick Recall
Concept	Simple Meaning
Encapsulation	Binding data + functions together
Inheritance	Reusing properties/functions of another class
Polymorphism	One name, many forms
Abstraction	Showing important details and hiding complexity

1. Class
A class is a blueprint/template for creating objects.

Syntax
class ClassName {
    // data
    // functions
};
Example
#include <iostream>
using namespace std;

class Student {
public:
    string name;
    int age;
};

Here Student is a class.

2. Object
Definition

An object is an instance of a class.

Example
Student s1;

Here:

Student → Class
s1      → Object

Complete example:

#include <iostream>
using namespace std;

class Student {
public:
    string name;
    int age;
};

int main() {
    Student s1;

    s1.name = "Pallavi";
    s1.age = 21;

    cout << s1.name << endl;
    cout << s1.age;

    return 0;
}
Output
Pallavi
21
3. Encapsulation
Definition

Encapsulation means wrapping data and functions together inside a class and controlling access to the data.

Example:

class Student {
private:
    int marks;

public:
    void setMarks(int m) {
        marks = m;
    }

    int getMarks() {
        return marks;
    }
};

Here marks is protected from direct access.

private data
     ↓
setMarks()
     ↓
getMarks()

This is commonly used to protect data.

4. Access Specifiers

C++ has three important access specifiers:

public
private
protected
Specifier	Accessible from outside class?
public	Yes
private	No
protected	No

Example:

class Student {
public:
    string name;

private:
    int marks;
};

You can do:

s1.name = "Pallavi";

But not:

s1.marks = 90;

because marks is private.

5. Inheritance
Definition

Inheritance allows one class to acquire properties and functions from another class.

Parent Class
     ↓
Child Class
Example
class Animal {
public:
    void eat() {
        cout << "Eating";
    }
};

class Dog : public Animal {
};

Now Dog inherits from Animal.

int main() {
    Dog d;

    d.eat();

    return 0;
}
Output
Eating
Remember
Animal → Parent/Base Class
Dog    → Child/Derived Class
6. Polymorphism
Definition

Polymorphism means:

One name, many forms.

Example:

same function name
        ↓
different behavior

There are two major types:

Compile-time Polymorphism
        ↓
Function Overloading

Run-time Polymorphism
        ↓
Function Overriding
Function Overloading Example
class Calculator {
public:
    int add(int a, int b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }
};

Same function name:

add()

but different parameters.

7. Abstraction
Definition

Abstraction means hiding unnecessary implementation details and showing only the required functionality.

Real-life example:

When you use an ATM:

You see:
Enter PIN
Withdraw Money
Check Balance

You don't need to know the internal banking system.

Similarly, in programming:

User
 ↓
Function
 ↓
Complex internal code

The user only needs to know how to use the function.

OOP Master Chart
OOP
│
├── Class
│   └── Blueprint
│
├── Object
│   └── Instance of class
│
├── Encapsulation
│   └── Data + Functions together
│
├── Inheritance
│   └── Reuse parent class
│
├── Polymorphism
│   └── One name, many forms
│
└── Abstraction
    └── Hide complexity
Easy Memory Trick
E I P A

E → Encapsulation
I → Inheritance
P → Polymorphism
A → Abstraction
