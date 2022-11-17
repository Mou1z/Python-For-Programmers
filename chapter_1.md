# Python for Programmers
This is a mini-course designed for people who already have at least a basic understanding of programming. This course distills the fundamental knowledge and principles of Python Programming into one short guide which can enable you to start using Python on a practical scale and kickstart your Python Programming career as quickly as possible.

There are two major versions of Python namely Python 2 and Python 3. This guide uses Python 3 since is the most recent version and has more features.

## Getting Started
Python was designed with user convenience in mind. It greatly emphasizes on user readability and ease of use which means that it is quite easy to use. Let's look at an example of how we can show the words "Hello World" on the screen using C++ (you don't have to worry about understanding the C++ code):
```c++
#include <iostream>

int main () {
    std::cout << "Hello World" << endl;
    return 1;
}
```
If we run the above C++ code, it will show "Hello World" in the output console. In Python however, doing this is much simpler - all we need is one line of code to print some text on the screen:
```py
print ("Hello World")
```
Before getting into coding another important thing to understand about Python is that it is an 'interpreted language' which means that it is executed on the go while languages like C++ are known as 'compiled languages' that have to be compiled into .exe (executable) files first and then executed. 

For following along with this guide it is suggested that you follow a more hands-on approach and perform the practice tasks that are mentioned through out the guide. For that you can either use some online interpreter such as [Programiz Online Interpreter](https://www.programiz.com/python-programming/online-compiler/), or you can set up Python on your own system.

For setting up Python on your computer, you can download the latest available version of Python from the [official Python website](https://www.python.org/downloads/).

You can link any suitable IDE or Editor to the Python Interpreter and start coding there. Visual Studio Code is the recommended editor for Python. Here is an Official Microsoft guide on [Setting Up Python for VSCode](https://code.visualstudio.com/docs/python/python-tutorial).


#### Showing Output

One of the most used features of programming is the print statement, which can show some output text in the console. It can help in debugging or coding in general so it is important to understand how it works in Python before getting into the guide because it will be needed throughout the guide.

Once you are done setting up Python, try printing some lines of text in the output console. The most basic line of code in Python is:
```py
print ("Hello World")
```
The print function also supports escape sequences like the **new line character** `\n`. Using the new line character we can show text in multiple lines:

Code:
```py
print ("This is the first line.\nThis is the second line.");
```
Output:
```
This is the first line.
This is the second line.
```

By default the print function appends the new line character to the end of the statement so if we write:
```py
print ("First Line")
print ("Second Line")
```
The output will be:
```
First Line
Second Line
```
We can change this behaviour of the print function so that it doesn't append the `\n` to the end of each statement by default but it will be explained in the later sections.

We can use commas (`,`) to include multiple output values and we can use the plus (`+`) sign to join multiple strings.

Code:
```py
print ("C", "O", "D" + " E") 
```
Output:
```
C O D E
```
Note that Python automatically adds a space between the comma separated values.

Following is a list of all the escape sequences supported by the language:
| Escape Sequence | Meaning |
|--|--|
| \' | Single quote  |
| \" | Double quote |
| \n | New Line |
| \\ | Backslash Character |
| \r | Carriage Return |
| \t | Horizontal Tab |
| \v | Vertical Tab |
| \uxxxx | 16-bit UNICODE character in hex format
| \Uxxxxxxxx | 32-but UNICODE character in hex format

For the sake of practice you can try printing the following pattern on the output:
1. Unicode Exercise
```
Here is a checkmark: ✓
```
Hint: Use UNICODE escape character to print the checkmark and the python emoji. The Hex value for the checkmark is `2713`.

## Variables and Data Types
Python supports all the basic data types which other languages have to offer however there are some additional unique data types as well. Following is a list of data types Python currently supports:

| Category | Type(s) Keyword |
|--|--|
| Numeric | int, float, complex |
| Sequences | list, tuple, range |
| Mapping | dict |
| Set | set, frozenset |
| Boolean | bool |
| Binary | bytes, bytearray, memoryview |
| None / Null | None |

We will explore all the types in relevant detail however let's first explore variables.

### Using Variables
In Python creating variables is very simple and variables are not type dependent which means they can hold any kind of (valid) value at any time. For creating variables we the following syntax:
```py
my_variable = value
```
Note that it's not possible to create variables without assigning them a value unlike some strictly typed languages like C# or C++. However you can assign a Null (`None`) value to a variable as a dummy value. Something like:
```py
my_variable = None
```
It is also important to note that we can assign a value of type different than what the variable has been initially or previously assigned. For-example we can assign a string value to a variable that was previously holding an integer:
```
my_var = 9
print (my_var)
my_var = "Nine"
print (my_var)
```
Output:
```
9
Nine
```

There is a concept of scopes in Python similar to other language with some differences. The differences will be highlighted when we're exploring conditionals and functions.

A general trick for declaring multiple variables (or assigning values to multiple variables) at once is:
```py
var_1, var_2, var_3 = 1, 2, 3
```
Python assigns the corresponding values on the right side to the variables on the left. The above code is equivalent to the following (with some differences):
```py
var_1 = 1
var_2 = 2
var_3 = 3
```
One advantage of this feature is that we can easily swap values of the variables without needing to create a third variable. 
Code:
```py
value_a = 1
value_b = 2

print ("A: " + value_a, "A: " + value_b)

value_a, value_b = value_b, value_a

print (value_a, value_b)
```
Output:
```
1 2
2 1
```
This is a very useful feature which is often used when we have to swap the values. Python assigns the value `value_b` to `value_a` and in the same statement it assigns the value of `value_a` to `value_b`. Since these operations are performed in a single step we don't have to worry about creating an intermediate variable.
