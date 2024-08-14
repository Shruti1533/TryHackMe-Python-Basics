# TryHackMe-Python-Basics

## Task 1: Introduction to Python

Although programming isn’t required to succeed in security, it’s a great skill to have. As the “Scripting for Pentesters” module demonstrates, being able to program allows you to create security tools and scripts that will aid you in hacking, defending, and analyzing.

### This room will teach you:
- Variables
- Loops
- Functions
- Data Structures
- If Statements
- Files

---

## Task 2: Hello World

To begin, let’s create a simple program that outputs some text.

```python
# This is an example comment
print("Hello World")
```

As you can see from the example code block above, it’s just one line (shown on line 2), and when we run this code, it will output the text "Hello World". Let's break this down:

- **Line 1** is a comment, a line starting with a hashtag `#` symbol and is not run by the computer.
- We can control what is output to the screen by using the `print()` statement. Anything inside the parentheses `()` will be output.
- Since we are printing a string, we enclose it in double quotations `""`.

On the code editor, print "Hello World". What is the flag?

**Flag:** `THM{PRINT_STATEMENTS}`

---

## Task 3: Mathematical Operators

Let’s now cover mathematical operators and how they can be applied to Python. Like a calculator, there are operations such as adding, subtracting, multiplying, and dividing; using Python, we can code our calculator; after all, programming is just writing rules for the computer to follow given specific inputs and conditions. The table below shows the different operations.
![Alt text](https://github.com/Shruti1533/TryHackMe-Python-Basics/blob/main/maths%20op.png)


Now that we know basic mathematical operators, let’s move on to comparison operators; these play a big part in Python and will be built upon when we look at loops and if statements. These operators are used to evaluate a program's condition at a particular state.
![Alt text](https://github.com/Shruti1533/TryHackMe-Python-Basics/blob/main/maths%202.png)


### Example Exercises:
- **Print the result of `21 + 43`. What is the flag?**  
  Flag: `THM{ADDITI0N}`
- **Print the result of `142–52`. What is the flag?**  
  Flag: `THM{SUBTRCT}`
- **Print the result of `10 * 342`. What is the flag?**  
  Flag: `THM{MULTIPLICATION_PYTHON}`
- **Print the result of `5` squared. What is the flag?**  
  Flag: `THM{EXP0N3NT_POWER}`

---

## Task 4: Variables and Data Types

Variables allow you to store and update data in a computer program. You have a variable name and store data to that name.

```python
food = "ice cream"
money = 2000
```

In the example above, we have two variables:
- The variable `food` stores the string `"ice cream"`.
- The variable `money` stores the number `2000`.

Variables are powerful as you can change them throughout your program. Below is an example:

```python
age = 30
age = age + 1
print(age)
```

Notice, on line 2, the way we update a variable, on the left, and we have the already created variable name “age” followed by the = operator. On the right, we have what we’re setting the variable to; in our case, the age variable (which is currently set to 30) is being increased by 1.

Let’s talk about Data Types, which is the type of data being stored in a variable. You can store text, or numbers, and many other types. The data types to know are:
- **String** — Used for combinations of characters, such as letters or symbols.
- **Integer** — Whole numbers.
- **Float** — Numbers that contain decimal points or fractions.
- **Boolean** — Used for data that is restricted to `True` or `False` options.
- **List** — Series of different data types stored in a collection.
![Alt text](https://github.com/Shruti1533/TryHackMe-Python-Basics/blob/main/data%20types.png)

### Example Exercise:
In the code editor, create a variable called `height` and set its initial value to `200`. Add `50` to the `height` variable and print the value.

```python
height = 200
height = height + 50
print(height)
```

**Flag:** `THM{VARIABL3S}`

---

## Task 5: Logical and Boolean Operators
![Alt text]([URL_to_your_image](https://github.com/Shruti1533/TryHackMe-Python-Basics/blob/main/logical%20and%20boolean.png))

Let’s look at a few Python code examples:

```python
a = 1
if a == 1 or a > 10:
    print("a is either 1 or above 10")

name = "bob" 
hungry = True
if name == "bob" and hungry == True:
    print("bob is hungry")
elif name == "bob" and not hungry:
    print("Bob is not hungry")
else:
    print("Not sure who this is or if they are hungry")
```

---

## Task 6: (Shipping Project) Introduction to If Statements

Using “if statements” allows programs to make decisions. They let a program chose a decision based on a condition. Below is an example of how an if statement can be used to determine the section of code (which print statement) to use.
![Alt text](https://github.com/Shruti1533/TryHackMe-Python-Basics/blob/main/if.png)

```python
if age < 17:
    print('You are NOT old enough to drive')
else:
    print('You are old enough to drive')
```

There are some key components we note from our code example above:

The if keyword indicates the beginning of the if statement, followed by a set of conditions.
The if statement is only run if the condition (or sets of conditions) is true. In our example, it’s age < 17; if that condition is true (age is below 17), the code within the if statement runs. Per the example, if certain conditions are not met, the program can default to running code shown in the else part of the if statement.
A colon : marks the end of the if statement.
Note the indentation. Anything after the colon that is indented, is considered part of the if statement, which the program will execute.
In this exercise, we will code a small application that calculates and outputs the shipping cost for a customer based on how much they’ve spent.

In the code editor, click on the “shipping.py” tab and follow the instructions to complete this task.

### Example Project:

In this project, you’ll create a program that calculates the total
cost of a customers shopping basket, including shipping.

— If a customer spends over $100, they get free shipping
— If a customer spends < $100, the shipping cost is $1.20 per kg of the baskets weight

Print the customers total basket cost (including shipping) to complete this exercise.

```python
customer_basket_cost = 34
customer_basket_weight = 44
total_cost = 0

if customer_basket_cost < 100:
    total_cost = total_cost + customer_basket_cost + 1.20 * customer_basket_weight
    print(total_cost)
else:
    total_cost = total_cost + customer_basket_cost
    print(total_cost)
```

**Flag:** `THM{IF_STATEMENT_SHOPPING}`

---

## Task 7: Loops

In programming, loops allow programs to iterate and perform actions a number of times. There are two types of loops, `for` and `while` loops.

### While Loops

```python
i = 1
while i <= 10:
    print(i)
    i = i + 1
```

### For Loops

```python
websites = ["facebook.com", "google.com", "amazon.com"]
for site in websites:
    print(site)
```

### Example Exercise:
Code a loop that outputs every number from `0` to `50`.

```python
for i in range(100):
    print(i)
```

**Flag:** `THM{L00PS_WHILE_FOR}`

---

## Task 8: (Bitcoin Project) Introduction to Functions

As programs grow, functions help to avoid repetitive code. A function is a block of code that can be called at different places in your program.

```python
def sayHello(name):
    print("Hello " + name + "! Nice to meet you.")
sayHello("ben")
```

### Key Components of Functions:
- **def keyword**: Indicates the beginning of a function.
- **Function name**: Defined by the programmer.
- **Parentheses `()`**: Holds input values (parameters).
- **Colon `:`**: Marks the end of the function header.
- **Indentation**: Anything after the colon that is indented is part of the function.

### Example Project:

Write a function to convert Bitcoin to USD and determine if the value falls below $30,000.

```python
investment_in_bitcoin = 1.2
bitcoin_to_usd = 40000

def bitcoinToUSD(bitcoin_amount, bitcoin_value_usd):
    usd_value = bitcoin_amount * bitcoin_value_usd
    return usd_value

investment_in_usd = bitcoinToUSD(investment_in_bitcoin, bitcoin_to_usd)
if investment_in_usd <= 30000:
    print("Investment below $30,000! SELL!")
else:
    print("Investment above $30,000")
```

**Flag:** `THM{BITC0IN_INVESTOR}`

---

## Task 9: Files

In Python, you can read and write from files.

### Reading Files:
```python
f = open("file_name", "r")
print(f.read())
```

### Writing to Files:
```python
f = open("demofile1.txt", "a")  # Append to an existing file
f.write("The file will include more text..")
f.close()

f = open("demofile2.txt", "w")  # Creating and writing to a new file
f.write("demofile2 file created, with this content in!")
f.close()
```

### Example Exercise:
Write Python code to read the `flag.txt` file.

**Flag:** `THM{F1LE_R3AD}`

---

## Task 10: Imports

In Python, we can import libraries, which are collections of files that contain functions.

```python
import datetime
current_time = datetime.datetime.now()
print(current_time)
```

### Popular Libraries:
- **Request** — Simple HTTP library.
- **Scapy** — Send, sniff, dissect, and forge network packets.
- **Pwntools** — CTF & exploit development library.
