# WEEK 28: How Computers Think & Basic Building Blocks

## Hour 1: Computer Fundamentals

### Part 1: How Computers Actually Work (20 minutes)

![Key Internal Computer Components](https://i.ytimg.com/vi/FQfcAm0FnWU/maxresdefault.jpg)

#### What happens when you run a program?
When you double-click a program or type `python myprogram.py`, here's what happens:

1. **Loading**: The operating system finds your program file and loads it into memory (RAM)
2. **Execution**: The CPU starts reading and executing instructions one by one
3. **Processing**: The CPU performs calculations, moves data around, and interacts with other parts of the computer
4. **Output**: Results are displayed on screen, saved to files, or sent over networks

**Analogy**: Think of it like following a recipe:
- The recipe (your code) tells you what to do
- You (the CPU) follow the instructions step by step
- The ingredients (data) get transformed into the final dish (output)

#### Memory (RAM) vs Storage (Hard Drive)
- **RAM (Memory)**: Like your desk workspace - fast access, but temporary
  - Programs run here
  - Data being actively used lives here
  - Gets cleared when computer turns off
  
- **Storage (Hard Drive)**: Like filing cabinets - permanent but slower
  - Programs are stored here when not running
  - Your documents, photos, videos live here
  - Keeps data even when computer is off

**Key Point**: When you run a program, it gets copied from storage into memory.

#### CPU: The Brain That Follows Instructions
The CPU is like a very fast, very literal assistant:
- Reads instructions one at a time
- Performs basic operations: add, subtract, compare, move data
- Makes decisions based on conditions
- Repeats operations when told to loop

**Important**: The CPU doesn't "understand" what your program does - it just follows instructions exactly as written.

#### Interactive Demo: Hello World Walkthrough
Let's trace what happens with this simple program:

```python
name = "Alice"
print("Hello, " + name)
```

Step by step:
1. Program loaded into memory
2. CPU reads first line: creates a space in memory labeled "name"
3. CPU stores the text "Alice" in that space
4. CPU reads second line: gets value from "name" space
5. CPU combines "Hello, " with "Alice"
6. CPU sends "Hello, Alice" to the screen

### Part 2: Binary and Data Representation (20 minutes)

#### Why Computers Use 1s and 0s
Computers are made of millions of tiny switches that can be either ON or OFF:
- ON = 1
- OFF = 0

Everything in a computer is represented using combinations of these 1s and 0s.

#### How Different Types of Data Are Stored

**Numbers**:
- 5 in binary: 101
- 10 in binary: 1010
- Each position represents a power of 2

**Text**:
- Each letter has a number assigned (ASCII/Unicode)
- 'A' = 65, which is 1000001 in binary
- 'B' = 66, which is 1000010 in binary

**Images**:
- Each pixel has color values (Red, Green, Blue)
- Each color is a number (0-255)
- These numbers become binary

#### Fun Activity: Convert Your Name to Binary
Let's convert "Hi" to binary:
- H = 72 = 1001000
- i = 105 = 1101001
- Space between letters in computer memory

#### Understanding Data Types
Because everything is stored as 1s and 0s, we need to tell the computer how to interpret them:

```python
age = 17          # Integer - whole number
height = 5.8      # Float - decimal number
name = "Alice"    # String - text
is_student = True # Boolean - True/False
```

Each type is stored differently in memory and supports different operations.

### Part 3: From Code to Running Program (20 minutes)

#### Compilation vs Interpretation

**Compiled Languages (like C, C++)**:
- Code is translated to machine language all at once
- Creates an executable file
- Runs very fast
- Errors found during compilation

**Interpreted Languages (like Python)**:
- Code is translated line by line as it runs
- No separate executable file
- Slightly slower but more flexible
- Errors found during execution

**Java (Special Case)**:
- Compiled to "bytecode" (intermediate form)
- Bytecode is interpreted by Java Virtual Machine
- "Compile once, run anywhere"

#### Why This Matters for Learning
Python shows you errors as you run the program, making it easier to learn and debug.

#### Understanding Error Messages
Error messages are the computer's way of saying "I don't understand what you want me to do."

Common error types:
- **SyntaxError**: You wrote something the computer can't parse
- **NameError**: You used a variable that doesn't exist
- **TypeError**: You tried to do something with the wrong type of data

**Example**:
```python
# This will cause a NameError
print(first_name)  # first_name was never defined
```

Error message: "NameError: name 'first_name' is not defined"

Translation: "You asked me to print something called 'first_name', but I don't know what that is."

## Hour 2: Variables and Data Types Deep Dive

### Part 1: Variables as Containers (20 minutes)

#### Memory Addresses and Variable Names
When you create a variable, the computer:
1. Reserves some space in memory
2. Gives that space an address (like a house address)
3. Associates your variable name with that address

```python
student_name = "Alice"
```

What really happens:
- Computer finds empty space in memory (let's say address 1000)
- Stores "Alice" at address 1000
- Creates a mapping: student_name → address 1000

#### Why We Need Different Types

**Integers** (whole numbers):
```python
age = 17
students_in_class = 25
```
- Used for counting, indexing
- Support math operations: +, -, *, //, %

**Floats** (decimal numbers):
```python
height = 5.8
temperature = 98.6
```
- Used for measurements, precise calculations
- Support math operations: +, -, *, /, **

**Strings** (text):
```python
name = "Alice"
message = "Hello, world!"
```
- Used for text, labels, user input
- Support text operations: +, *, len(), upper(), lower()

**Booleans** (True/False):
```python
is_student = True
has_homework = False
```
- Used for flags, conditions, logic
- Result of comparisons: ==, !=, <, >, <=, >=

#### Practice: Student Profile
Let's create variables for a student:

```python
# Personal information
first_name = "Alice"
last_name = "Johnson"
age = 17
grade_level = 11

# Academic information
gpa = 3.8
is_honor_roll = True
favorite_subject = "Computer Science"

# Calculate graduation year
current_year = 2024
years_until_graduation = 12 - grade_level
graduation_year = current_year + years_until_graduation

print(f"{first_name} {last_name} will graduate in {graduation_year}")
```

### Part 2: How Data Flows in Programs (20 minutes)

#### Input → Processing → Output Pattern
Every program follows this basic pattern:

1. **Input**: Get data from somewhere (user, file, internet)
2. **Processing**: Do something with that data (calculate, transform, analyze)
3. **Output**: Show or save the results

#### Example: Temperature Converter
Let's trace through this program step by step:

```python
# Input
celsius = float(input("Enter temperature in Celsius: "))

# Processing
fahrenheit = (celsius * 9/5) + 32

# Output
print(f"{celsius}°C is {fahrenheit}°F")
```

**Step-by-step execution**:
1. Program asks user for input
2. User types "25"
3. `input()` returns "25" (string)
4. `float()` converts "25" to 25.0 (number)
5. Variable `celsius` gets value 25.0
6. Calculate: (25.0 * 9/5) + 32 = 45.0 + 32 = 77.0
7. Variable `fahrenheit` gets value 77.0
8. Print statement displays: "25.0°C is 77.0°F"

#### Tracing Exercise
Always trace through your programs with specific values:

```python
# Let's trace with x = 5
x = 5
y = x * 2      # y = 10
x = x + 1      # x = 6
z = x + y      # z = 6 + 10 = 16
print(z)       # Prints: 16
```

### Part 3: Common Mistakes and Debugging (20 minutes)

#### Type Errors and How to Fix Them

**Common mistake**: Trying to do math with strings
```python
# Wrong
age = "17"
next_year = age + 1  # Error: can't add string and number

# Right
age = int("17")  # or age = 17
next_year = age + 1
```

**Common mistake**: Forgetting to convert input
```python
# Wrong
number = input("Enter a number: ")
doubled = number * 2  # If user enters "5", result is "55"

# Right
number = int(input("Enter a number: "))
doubled = number * 2  # If user enters "5", result is 10
```

#### Variable Naming Best Practices

**Good names**:
```python
student_count = 25
first_name = "Alice"
is_passing = True
```

**Bad names**:
```python
x = 25          # What does x represent?
n = "Alice"     # n could be anything
flag = True     # What kind of flag?
```

**Rules**:
- Use descriptive names
- Use lowercase with underscores
- Don't use reserved words (if, for, while, etc.)
- Be consistent

#### Debugging Practice
Let's fix this broken code together:

```python
# Broken code
First_name = "alice"
last_name = "johnson"
Age = 17
print("Hello, " + first_name + " " + last_name)
print("You are " + Age + " years old")
```

**Problems**:
1. Inconsistent variable naming (First_name vs first_name)
2. Trying to concatenate string and integer

**Fixed code**:
```python
first_name = "Alice"
last_name = "Johnson"
age = 17
print("Hello, " + first_name + " " + last_name)
print("You are " + str(age) + " years old")
# Or use f-strings: print(f"You are {age} years old")
```
