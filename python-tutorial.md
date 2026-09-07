# Python and Programming Basics: A Tutorial

**Author:** Johan Odelius, Operation and Maintenance Engineering, Luleå University of Technology (LTU)

## Learning outcomes

This tutorial develops the concepts needed to read, reason about, and write short Python programs. The aim is to understand the rules of Python as well as how to structure code when writing programs.

After working through the tutorial, you should be able to:

- run a Python script and trace its execution to predict its output
- create and update variables
- distinguish between data types such as integers, floating-point numbers, strings, and Booleans
- use assignment statements, arithmetic operators, and relational operators
- work with lists and dictionaries
- write loops, conditional statements, and functions
- import and use modules from the Python standard library, such as `math` and `random`
- organize a script into imports, configuration, function definitions, and main code
- write readable code and use comments to document purpose, assumptions, and logic
- interpret common errors such as `NameError`, `KeyError`, and `SyntaxError`.

**Python style:** The examples in this tutorial follow [PEP 8, the official Style Guide for Python Code](https://peps.python.org/pep-0008/).

Definitions of technical terms are available in the [Python glossary](glossary.md).

Change the examples and rerun code examples many times: experimentation is part of learning programming.

### Acknowledgements
This tutorial was developed with assistance from OpenAI Codex, which was used to review explanations, code examples, exercises, and terminology. All AI-assisted content was reviewed and revised by the author, who takes responsibility for the final material.

## Python
You need access to Python 3 to complete this tutorial. You can run the introductory examples in an IDE, a notebook environment, or the Python interpreter.

### Editor and interpreter

Python code is called **source code**. Two different tools are involved when working with source code:

* a **code editor** is used to write and modify source code
* the **Python interpreter** reads and executes the source code

An editor does not execute Python by itself. When you select **Run**, the editor sends the code to the Python interpreter. The interpreter performs the specified operations and displays any output or error messages in a console.

An **IDE**, such as Spyder, combines an editor, access to the interpreter, a console, and debugging tools in one application.

Python code can be executed in two main ways.

In **interactive mode**, you enter and execute one statement at a time. The Python interpreter commonly displays a prompt containing three greater-than signs:

```text
>>> print("Hello, Python!")
Hello, Python!
```

The `>>>` characters are the interpreter prompt and are not part of the Python code.

In **script mode**, source code is saved in a file whose name ends in `.py`. The interpreter then executes the statements in the file:

```python
print("Hello, Python!")
```

For example, the file might be saved as `hello.py` and executed from a terminal:

```console
python hello.py
```

A notebook provides another interface to the interpreter. Code is divided into cells that can be executed individually, with the output displayed below each cell.


## Exercises
Exercises are available [here](exercises.md)


---

## 1. Values, variables, and data types

A Python program consists of instructions called **statements**. One of the simplest statements displays a value with the built-in `print(...)` function:

```python
print("Hello, Python!")
```

Output:

```text
Hello, Python!
```

Here, `"Hello, Python!"` is a value. Values have different data types:

| Type | Meaning | Examples |
|---|---|---|
| `int` | Integer (whole number) with arbitrary precision | `-3`, `0`, `42` |
| `float` | Finite-precision floating-point approximation to a real number | `2.5`, `-0.01` |
| `str` | Immutable sequence of Unicode characters used to represent text | `"Python"`, `'Johan'` |
| `bool` | Boolean truth value | `True`, `False` |

### Assigning values to variables

A **variable** is a name that refers to a value. An **assignment statement** uses `=` to assign the value on the right to the variable on the left:

```python
course_code = "D0023B"
credits = 7.5
number_of_students = 17
is_complete = False
```

For example, read

```python
number_of_students = 17
```

as “assign the value `17` to the variable `number_of_students`.” It does not state a mathematical equality. After the assignment, the name can be used to retrieve the value:

```python
print(number_of_students)
```

Output:

```text
17
```

Use `type(...)` to inspect a value's data type:

```python
print(type(number_of_students))
```

### Names are case-sensitive

Python treats uppercase and lowercase letters as different characters. Therefore `x` and `X` are different names.

```python
x = 7
print(X)
```

This produces a `NameError` because only lowercase `x` exists. The requested uppercase name is undefined.

Case sensitivity also applies to built-ins and functions:

```python
print("works")
# Print("fails")  # NameError: name 'Print' is not defined
```

### Names and strings are not the same

Quotation marks create a string literal:

```python
name = "Johan"
print(name)     # retrieves the value associated with name
print("name")   # prints the literal characters n-a-m-e
```

Output:

```text
Johan
name
```

### Updating a variable

An **update** is an assignment statement that gives a new value to a variable that already exists:

```python
x = 10
x = 12
print(x)
```

Output:

```text
12
```

The second assignment makes `x` refer to `12` instead of `10`.

---


## 2. Operators and expressions
An expression is code that evaluates to a value. For example, `x + 3` and `name + "!"` are expressions.

### Arithmetic operators

| Operator | Meaning | Example | Result |
|---|---|---|---:|
| `+` | Addition | `7 + 3` | `10` |
| `-` | Subtraction | `7 - 3` | `4` |
| `*` | Multiplication | `7 * 3` | `21` |
| `/` | True division | `7 / 3` | `2.333...` |
| `//` | Integer division | `7 // 3` | `2` |
| `%` | Remainder | `7 % 3` | `1` |
| `**` | Exponentiation | `3 ** 2` | `9` |

**Integer division** divides two numbers and rounds down to an integer:

```python
print(7 // 3)    # 2
print(-7 // 3)   # -3, not -2
```

That distinction matters with negative values.

Variables can be used in expressions, and the result can be assigned to another variable:

```python
x = 5
y = x + 3
print(y)
```

Output:

```text
8
```

Python evaluates the right-hand side first. It retrieves the value of `x`, adds `3`, and then assigns the result to `y`.

### Assignment and relational operators are different

```python
x = 5       # assignment: make x refer to 5
x == 5      # comparison: evaluate whether x equals 5
```

Common **relational operators** are:

| Operator | Meaning |
|---|---|
| `==` | equal to |
| `!=` | not equal to |
| `<` | less than |
| `<=` | less than or equal to |
| `>` | greater than |
| `>=` | greater than or equal to |

Relational operators produce Boolean values:

```python
temperature = 18
print(temperature > 20)
```

Output:

```text
False
```

### Augmented assignment

An augmented assignment statement combines an operation with assignment. For example:

```python
count = 5
count += 1

print(count)
```

Output:

```text
6
```

For numbers, this is equivalent to:

```python
count = count + 1
```

Python provides augmented assignment statements for several arithmetic operations:

| Statement | Numeric equivalent |
|---|---|
| `x += y` | `x = x + y` |
| `x -= y` | `x = x - y` |
| `x *= y` | `x = x * y` |
| `x /= y` | `x = x / y` |
| `x //= y` | `x = x // y` |
| `x %= y` | `x = x % y` |
| `x **= y` | `x = x ** y` |

Python does not use the `++` or `--` operators found in languages such as C, C++, and Java.

---

## 3. Execution order and tracing

Python executes statements **from top to bottom**, one at a time. A variable must be assigned before Python tries to use it.

```python
x = 5
y = 10
print(x + y)
```

Output:

```text
15
```

Python performs three actions:

1. Assign the integer `5` to `x`.
2. Assign the integer `10` to `y`.
3. Retrieve both values, add them, and print the result.

Order matters:

```python
print(z)
z = 5
```

This fails on the first line because `z` has not yet been assigned:

```text
NameError: name 'z' is not defined
```

---

## 4. Comments

A **comment** is explanatory text ignored by Python. A comment begins with `#` and continues to the end of the line.

```python
# Convert temperature from Celsius to Kelvin
kelvin = 20 + 273.15

sample_size = 120  # Number of samples after filtering
```

Useful comments explain **why** the code exists or record information that the code alone does not express clearly. Good subjects include intent, assumptions, units, data limitations, and non-obvious decisions.

Less useful: repeat what the code already says
```python
base_cost = 1000

# Multiply the base cost by 1.2
adjusted_cost = base_cost * 1.2
```
More useful: explain why this observation should be counted
```python
base_cost = 1000

# Include the 20% overhead
adjusted_cost = base_cost * 1.2
```

Follow these practical guidelines:

- Keep comments accurate when the code changes. An outdated comment is worse than no comment.
- Prefer clear variable and function names; do not use comments to compensate for unclear names.
- Put a comment immediately above the code it explains. A short end-of-line comment is suitable for units or brief context.
- Explain decisions and assumptions rather than translating every statement into natural language.
- Follow [PEP 8](https://peps.python.org/pep-0008/#inline-comments) for inline comments: use at least two spaces between the statement and the comment, followed by one space after `#`


---

## 5. Conditional execution

A **conditional statement** chooses which block to execute based on a **Boolean expression**:

```python
x = 5
y = 10

if x > y:
    print("x is greater")
else:
    print("y is greater or equal")
```

Output:

```text
y is greater or equal
```

The **condition** `x > y` is `False`, so Python skips the first **branch** and executes the `else` branch.

Note: Variables must exist before the condition

This version fails:

```python
if x > y:
    print("x is greater")
else:
    print("y is greater")

x = 5
y = 10
```

Python must evaluate `x > y` before it can choose a branch. At that moment, `x` and `y` are undefined, so execution stops with a `NameError`. The assignments at the bottom are never reached.

### More than two cases

Use `elif` for additional mutually exclusive cases:

```python
x = 15
y = 10

if x > y:
    print("x is greater")
elif x < y:
    print("y is greater")
else:
    print("x and y are equal")
```

Only the first branch whose condition is `True` is executed.

---

## 6. Lists: ordered collections

A list stores an ordered sequence of values:

```python
measurements = [12.1, 11.8, 12.4, 12.0]
```

The number of elements is obtained with the built-in function `len(...)`:

```python
print(len(measurements))
```

Output:

```text
4
```

`len` works with many collection types, including strings, lists, and dictionaries.

### Indexing starts at zero

```python
labels = ["control", "treatment", "placebo"]

print(labels[0])   # control
print(labels[1])   # treatment
print(labels[2])  # placebo
print(labels[-1])  # placebo
```

An index identifies one element. The first element has index `0` and `-1` means the final element.

### Slicing

A slice extracts a subsequence:

```python
values = [1, 2, 3, 4, 5]
print(values[1:4])
```

Output:

```text
[2, 3, 4]
```

The rule is **start included, stop excluded**. In `values[1:4]`, Python includes indices `1`, `2`, and `3`, but **not** `4`.

Useful forms include:

```python
print(values[:3])   # [1, 2, 3]
print(values[2:])   # [3, 4, 5]
print(values[::2])  # [1, 3, 5]
print(values[::-1]) # [5, 4, 3, 2, 1]
```

The full pattern is `sequence[start:stop:step]`.

### Modifying lists

```python
results = []
results.append(4)
results.append(9)
print(results)
```

Output:

```text
[4, 9]
```

`append(...)` is a **method** that adds one element to the end of the existing list. The expression `results.append(4)` is a method **invocation**.

## 7. Strings

A string (`str`) is an immutable sequence of Unicode characters used to represent textual data.

```python
title = "IoT-Enabled Condition Monitoring and Maintenance Technologies"
```

### Length

The built-in function `len` returns the number of characters in a string:

```python
print(len(title))
```

Strings support positional access using zero-based indices. Negative indices count backward from the end of the string.

```python
print(title[0])   # I
print(title[-1])  # s
```

A slice extracts part of a string. Its general form is:

```python
string[start:stop:step]
```

The start position is included, while the stop position is excluded:

```python
print(title[:11])   # IoT-Enabled
print(title[-12:])  # Technologies
print(title[::-1])  # Reversed string
```

### Immutability

Strings are immutable, which means that their characters cannot be changed after the string has been created. Assigning a new value to a string index raises a `TypeError`:

```python
text = "hello"
text[0] = "H"
```

```text
TypeError: 'str' object does not support item assignment
```

Instead, construct a new string:

```python
text = "H" + text[1:]
print(text)
```

Output:

```text
Hello
```

### String concatenation

The `+` operator concatenates strings by joining them end-to-end:

```python
first_name = "Johan"
greeting = "Hello, " + first_name + "!"

print(greeting)
```

Output:

```text
Hello, Johan!
```

Both operands must be strings. Concatenating a string and an integer directly raises a `TypeError`:

```python
participants = 15
message = "Participants: " + participants
```

### String formatting with f-strings

A formatted string literal, or f-string, begins with `f`. Expressions inside braces are evaluated and inserted into the string.
F-strings can insert values of different types without explicit string conversion:

```python
course_code = "D0023B"
participants = 15

message = f"{course_code} has {participants} participants."
print(message)
```

Output:

```text
D0023B has 15 participants
```

Example with format specification:
```python
sensor_id = 104
amplitude = 0.04812

log_entry = f"Sensor {sensor_id}: peak = {amplitude:.3f} m/s²"
print(log_entry)
```

Output:

```text
Sensor 104: peak = 0.048 m/s²
```

`.3f` displays the floating-point value with three digits after the decimal point.


### Common string methods

A method is a function associated with an object. String methods do not modify the original string because strings are immutable. Instead, they return new strings.

```python
raw = "  Signal Type: Acceleration  \n"

cleaned = raw.strip() 
lowercase = cleaned.lower()
uppercase = cleaned.upper()
normalized = cleaned.replace("Signal Type", "signal_type")

print(cleaned)
print(lowercase)
print(uppercase)
print(normalized)
```

Output:

```text
Signal Type: Acceleration
signal type: acceleration
SIGNAL TYPE: ACCELERATION
signal_type: Acceleration
```

Common string methods include:

| Method | Purpose |
|---|---|
| `strip()` | Remove whitespace from the beginning and end |
| `lower()` | Convert characters to lowercase |
| `upper()` | Convert characters to uppercase |
| `replace(old, new)` | Replace occurrences of one substring with another |

### Strings and lists
String methods can be used to convert between text and lists.

Consider a record in which a comma separates a sensor identifier from a measurement:

```python
record = "sensor_104,0.048"
```

The string method `split` divides the string at the specified delimiter and returns a list of strings:

```python
parts = record.split(",")
print(parts)
```

Output:

```text
['sensor_104', '0.048']
```

The comma is the **delimiter**. It determines where the string is divided. The delimiter itself is not included in the resulting elements.

The elements can be accessed using list indices:

```python
sensor_id = parts[0]
amplitude_text = parts[1]

print(sensor_id)
print(amplitude_text)
```

Output:

```text
sensor_104
0.048
```

Although `amplitude_text` looks like a number, it is still a string because `split` returns strings. Convert it to a floating-point number before performing numerical calculations:

```python
amplitude_value = float(amplitude_text)
print(f"Squared amplitude = {amplitude_value ** 2 :.3f}")
```

Output:

```text
Squared amplitude = 0.096
```

The string method `join` combines a sequence of strings into one string. The string before `.join(...)` is inserted between the elements:

```python
normalized = ": ".join([sensor_id, amplitude_text])
print(normalized)
```

Output:

```text
sensor_104: 0.048
```

In this example, `": "` is the separator. The original list is not modified; `join` returns a new string.


---

## 8. Loops and repeated computation

A `for` loop processes each element in a sequence. The name after `for` is the **loop variable**:

```python
numbers = [1, 2, 3, 4, 5]
squared = []

for n in numbers:
    squared.append(n ** 2)

print(squared)
```

Output:

```text
[1, 4, 9, 16, 25]
```

Trace the loop iteration by iteration:

| Iteration | `n` | Value appended | `squared` afterward |
|---:|---:|---:|---|
| 1 | 1 | 1 | `[1]` |
| 2 | 2 | 4 | `[1, 4]` |
| 3 | 3 | 9 | `[1, 4, 9]` |
| 4 | 4 | 16 | `[1, 4, 9, 16]` |
| 5 | 5 | 25 | `[1, 4, 9, 16, 25]` |

### Indentation defines the loop body

Python uses indentation to group statements:

```python
for n in [1, 2, 3]:
    print(n)
print("finished")
```

The indented **block** is the body of the loop and runs three times. The unindented call runs once after the loop.

### A more compact form: list comprehension

Once the explicit loop is clear, the same transformation can be expressed as:

```python
squared = [n ** 2 for n in numbers]
```

List comprehensions are concise, but an ordinary loop is often easier to read when learning or debugging.

### Looping with an index

In some situations, we need the index of each element. `range` generates a sequence of integers and is commonly used in `for` loops when integer indices are needed or when a calculation must be repeated a specific number of times.

Like indexing and slicing, range starts at 0 by default and excludes its stop value. Therefore, range(5) generates the integers from 0 up to, but not including, 5.
```python
for i in range(5):
    print(i)
```

Output:

```text
0
1
2
3
4
```

`range` can be called in three forms:

```python
range(stop)
range(start, stop)
range(start, stop, step)
```

- `start` is the first integer and defaults to `0`
- `stop` is excluded
- `step` is the difference between consecutive integers and defaults to `1`
- `step` cannot be `0`

The expression `range(len(numbers))` generates the valid indices from `0` to `len(numbers) - 1`.

```python
numbers = [1, 2, 3, 4, 5]
squared = []

for i in range(len(numbers)):
    squared.append(numbers[i] ** 2)

print(squared)
```

Use `enumerate` if both the index and value are needed
```python
numbers = [1, 2, 3, 4, 5]
squared = []

for i, number in enumerate(numbers):
    print(i, number)
    squared.append(number ** 2)

print(squared)
```


---

## 9. Dictionaries: key–value mappings

A **dictionary** is a mapping that contains key-value pairs, also called **items**:

```python
course = {
    "code": "D0023B",
    "name": "IoT-Enabled Condition Monitoring and Maintenance Technologies",
    "credits": 7.5,    
    "participants": 15
}
```

Retrieve a value using its key:

```python
print(course["credits"])
```

Output:

```text
7.5
```

The expression inside brackets is a key, not a numeric position. 

### Missing keys and safe lookup

```python
print(course["period"])
```

This raises a `KeyError` because the dictionary has no key named `"period"`.

When a key may be absent, one can use `get(...)`:

```python
print(course.get("period"))  # None
print(course.get("period", "Not specified"))  # Not specified
print(course.get("period", 0))  # 0
```

Choose default values carefully. For example, representing an unknown value as `0` could make missing data appear to be a valid observation.

### Testing whether a key exists
The membership operator `in` tests whether a dictionary contains a key. It produces a Boolean value and can be can be used in conditional statements.

```python
if "period" in course:
    print(course["period"])
else:
    print("Period not specified")
```

Testing membership is useful when the script should behave differently depending on whether a key exists. 

### Adding and updating items

An assignment to a new key adds an item. An assignment to an existing key updates its value:

```python
course["period"] = 1
course["participants"] = 17

print(course["period"])  # 1
print(course["participants"])  # 17
```

The first assignment adds a new item because `"period"` is not already a key. The second assignment updates the value associated with the existing key `"participants"`.

### Iterating through dictionary items

The dictionary method `items()` provides the key-value pairs so that they can be processed in a loop:

```python
course = {
    "code": "D0023B",
    "name": "IoT-Enabled Condition Monitoring and Maintenance Technologies",
    "credits": 7.5,
    "participants": 15
}

for key, value in course.items():
    print(f"Course {key}: {value}")
```

Output:

```text
Course code: D0023B
Course name: IoT-Enabled Condition Monitoring and Maintenance Technologies
Course credits: 7.5
Course participants: 15
```

On each iteration, `items()` provides one `(key, value)` pair. Python unpacks the pair into the loop variables `key` and `value`.

Dictionaries preserve insertion order, so the items are processed in the order in which they were added to the dictionary.


### Combining lists and dictionaries

Lists and dictionaries can be combined to represent structured data. In this example, each element in the list is a dictionary representing one course:

```python
courses = [
    {
        "code": "D0023B",
        "name": "IoT-Enabled Condition Monitoring and Maintenance Technologies",
        "credits": 7.5,
        "participants": 15
    },
    {
        "code": "D7021B",
        "name": "Reliability and Maintenance Engineering",
        "credits": 7.5,
        "participants": 22
    }
]

total_credits = 0

for course in courses:
    total_credits += course["credits"]

print(f"Total credits: {total_credits}")
```

Output:

```text
Total credits: 15.0
```

On each iteration, `course` refers to one dictionary. The expression `course["credits"]` retrieves the credit value, which is added to the accumulator `total_credits`.

---


## 10. Functions

A **function** is a named sequence of statements that performs a useful operation. A **function definition** uses the keyword `def` to create a function:

```python
def greet(name):
    return f"Hello, {name}!"

message = greet("Johan")
print(message)
```

Output:

```text
Hello, Johan!
```

The first line is the function **header**, and the indented sequence of statements is its **body**. Other key terms are:

- `greet` is the function's name;
- `name` is a parameter: a local name used by the function;
- `"Johan"` is the argument supplied when calling the function;
- `greet("Johan")` is a function call;
- `return` sends a return value back to the caller.

### `return` and `print` have different roles

```python
def square(value):
    return value ** 2

result = square(4)
print(result)
```

`return` makes `16` available to the rest of the program as a **return value**. `print` displays it. A function can calculate a useful value without displaying anything.

Compare:

```python
def display_square(value):
    print(value ** 2)

result = display_square(4)
print(result)
```

Output:

```text
16
None
```

Because `display_square` has no explicit `return`, it returns the special value `None`.

### Local scope

A parameter exists only inside its function:

```python
def display_square(value):
    result = value ** 2  # 'result' is a local variable
    print(result)

print(display_square(3))
print(result)  # NameError: name 'result' is not defined
```

---

## 11. Importing modules

A **module** is a file that contains Python code, including variables and function definitions. An **import statement** makes code from a module available in the current script.

Python includes a **standard library**: a collection of modules supplied with Python. For example, the `math` module provides mathematical constants and functions:

```python
import math

radius = 3
area = math.pi * radius ** 2
print(area)
```

The expression `math.pi` accesses the variable `pi` in the `math` module. The function call `math.sqrt(25)` accesses and calls the function `sqrt` from that module. The `.` is called the **dot operator**.

```python
import math

print(math.sqrt(25))
```

Output:

```text
5.0
```

The `random` module provides functions for generating pseudorandom values:

```python
import random

die_roll = random.randint(1, 6)
print(die_roll)
```

The output can be any integer from `1` through `6`.

Place import statements near the beginning of a script. This makes its dependencies visible and ensures that imported names are available before they are used.

### Built-in functions and standard-library modules

These categories are related but different:

- Built-in functions such as `print`, `len`, and `type` are available without an import statement.
- Standard-library modules such as `math` and `random` are supplied with Python but must be imported before use.
- Third-party packages are installed separately and then imported. They are outside the scope of this tutorial.

---

## 12. Scripts, programs, and code structure

The terms **script** and **program** overlap, and the distinction is not absolute:

- A **script** is usually a Python source file, ending in `.py`, that is intended to be executed directly. It often automates a task or performs an analysis.
- A **program** is the complete set of instructions used to solve a problem. A small program may consist of a single script and a larger program may contain many modules, packages, tests, and data files.
- A `.py` file is a **module** when another file imports it. The same file can be executed as a script in one context and imported as a module in another.

### Script structure

There is no single structure for every Python program, but a small reusable script commonly follows this order:

1. A short description of the script's purpose
2. Import statements
3. Constants or configuration values
4. Function definitions
5. The main code

A simple script might be structured as follows:

```python
"""Calculate the area of a circle."""

import math


DEFAULT_RADIUS = 3


def circle_area(radius):
    return math.pi * radius ** 2


area = circle_area(DEFAULT_RADIUS)
print(f"Area: {area}")
```
In this example:
- The opening **module docstring** describes the file's purpose
- The import statement appears before code that uses the `math` module
- `DEFAULT_RADIUS` is a configuration value
- Uppercase names conventionally indicate constants that are not intended to change while the program runs
- The function definition creates `circle_area`, but its body does not run until the function is called
- The final two statements constitute the main code

#### Using a `main` function
For a script that may grow or be imported by another module, the main operations can be placed in a function conventionally named `main`:

```python
"""Calculate the area of a circle."""

import math


DEFAULT_RADIUS = 3


def circle_area(radius):
    return math.pi * radius ** 2


def main():
    area = circle_area(DEFAULT_RADIUS)
    print(f"Area: {area}")


if __name__ == "__main__":
    main()
```
In this version:

- `main` coordinates the program's main code
- `__name__` is a variable that Python defines automatically
- When the file is executed directly, `__name__` has the value `"__main__"`
- The condition `__name__ == "__main__"` is called the **main guard**
- When the file is imported as a module, the condition is false and `main` is not called automatically
- Functions such as `circle_area` remain available to the importing module

For a very short, single-use script, a `main` function and main guard may be unnecessary. 

### Integrated example: calculating root mean square

Nested lists and dictionaries can represent measurements from multiple sensors. Before combining measurements, values expressed in different units must be converted to a common unit.

```python
import math

STANDARD_GRAVITY = 9.81


def square_values(values):
    return [value ** 2 for value in values]


def mean(values):
    return sum(values) / len(values)


def root_mean_square(values):
    return math.sqrt(mean(square_values(values)))


payload = [
    {
        "sensor_type": "Acceleration",
        "sensor_id": 1,
        "unit": "g",
        "values": [3.22, 4.56, 6.59, 5.12, 8.15, 5.88]
    },
    {
        "sensor_type": "Acceleration",
        "sensor_id": 2,
        "unit": "m/s²",
        "values": [3.22, 4.56, 6.59, 5.12, 8.15, 5.88]
    }
]

all_values = []

for sensor in payload:
    if sensor['sensor_type'] != "Acceleration":
        continue

    if sensor["unit"].upper() == "G":
        sensor_values = [
            value * STANDARD_GRAVITY
            for value in sensor["values"]
        ]
    elif sensor["unit"] == "m/s²":
        sensor_values = sensor["values"]
    else:
        raise ValueError(f"Unsupported unit: {sensor['unit']}")

    all_values.extend(sensor_values)

rms = root_mean_square(all_values)

print(f"Root mean square: {rms:.3f} m/s²")
```

Output:

```text
Root mean square: 40.424 m/s²
```

The program performs four main steps:

1. Iterate through the sensor dictionaries
2. Convert values expressed in `g` to `m/s²`
3. Add the converted values to one list
4. Calculate the root mean square of the combined values

The `continue` statement stops the current loop iteration and immediately begins the next one. It does not terminate the entire loop. 
The method `extend` adds every element from `sensor_values` to `all_values`. This differs from `append`, which add the entire list as one nested element. 

---

## 13. Common errors and how to diagnose them

Errors are diagnostic information, not merely failed attempts. An error detected while a program is running is an **exception**. The exception message identifies its type and usually includes a **traceback** showing where it occurred.

### `NameError`

Python was asked to use a name that is not currently defined.

```python
print(total)
```

Check for:

- use before assignment;
- spelling differences;
- uppercase/lowercase differences;
- a variable defined only inside another scope.

### `KeyError`

A requested dictionary key does not exist.

```python
scores = {"A": 10}
print(scores["B"])
```

Check the available keys with `scores.keys()`, test membership with `"B" in scores`, or use `scores.get(...)` when absence is expected.

### `IndexError`

A sequence index is outside the valid range.

```python
values = [10, 20]
print(values[2])
```

The valid indices are `0` and `1`.

### `TypeError`

An operation received an inappropriate type.

```python
print("sample size: " + 20)
```

One correction is an f-string:

```python
print(f"sample size: {20}")
```

### `SyntaxError`

Python cannot parse the code as valid Python grammar.

```python
if x > 3
    print(x)
```

The colon after the condition is missing. A `SyntaxError` concerns code structure; an undefined variable in otherwise valid code is instead a `NameError`.

### A practical debugging sequence

1. Read the final line of the error message and identify the error type.
2. Locate the line Python reports.
3. Inspect names, values, and types immediately before that line.
4. Reduce the expression into smaller parts if necessary.
5. Change one thing, rerun, and confirm the result.

### Handling exceptions with `try` and `except`

A program can use a `try` statement to handle an exception that is expected and recoverable.

Consider converting text into a floating-point number:

```python
raw_amplitude = "0.048"

try:
    amplitude = float(raw_amplitude)
except ValueError:
    print(f"Cannot convert {raw_amplitude!r} to a number")
else:
    print(f"Amplitude = {amplitude:.3f}")
```

Output:

```text
Amplitude = 0.048
```

Python first executes the statements in the `try` block. If `float(raw_amplitude)` raises a `ValueError`, Python stops executing that block and runs the matching `except` block. If no exception occurs, the `except` block is skipped and the optional `else` block runs.

If the input is changed, the exception is handled:

```python
raw_amplitude = "not available"

try:
    amplitude = float(raw_amplitude)
except ValueError:
    print(f"Cannot convert {raw_amplitude!r} to a number")
else:
    print(f"Amplitude = {amplitude:.3f}")
```

Output:

```text
Cannot convert 'not available' to a number
```

The expression `{raw_amplitude!r}` inserts the representation of the string, including its quotation marks.

Follow these principles when handling exceptions:

- Catch exceptions only when the program can respond meaningfully
- Catch a specific exception type, such as `ValueError` or `KeyError`
- Keep the `try` block limited to the statements that might raise the expected exception
- Do not use exception handling to conceal programming errors
- Do not use a bare `except:` unless there is a specific and well-justified reason

A `SyntaxError` is normally detected before the program begins executing. Therefore, a syntax error in the script itself cannot be handled by surrounding the invalid code with `try` and `except`.

### Handling a user interruption

A `while` loop repeats its body as long as its condition is `True`. The condition can be the Boolean value `True` itself, creating an infinite loop:

```python
import time
while True:
    print("This continues until the loop is interrupted")
    time.sleep(1)
```
where `time.sleep(1)` pauses execution for one second.

Long-running scripts can be interrupted by pressing `Ctrl+C`. Python responds by raising a `KeyboardInterrupt` exception.

```python
import time

sample_count = 0

print("Monitoring started. Press Ctrl+C to stop.")

try:
    while True:
        time.sleep(1)
        sample_count = sample_count + 1
        print(f"Collected sample {sample_count}")
except KeyboardInterrupt:
    print("\nMonitoring stopped by the user")
finally:
    print(f"Total samples collected: {sample_count}")
    print("Closing the monitoring session")
```

The program performs the following steps:

1. `while True` starts a loop without a predefined end
2. `time.sleep(1)` pauses execution for one second
3. The counter is updated and its value is displayed
4. Pressing `Ctrl+C` raises `KeyboardInterrupt`
5. The matching `except` block handles the interruption
6. The `finally` block runs before the `try` statement finishes

The output depends on when the user interrupts the program:

```text
Monitoring started. Press Ctrl+C to stop.
Collected sample 1
Collected sample 2
Collected sample 3
^C
Monitoring stopped by the user
Total samples collected: 3
Closing the monitoring session
```

A `finally` block is normally used for necessary cleanup, such as closing files, releasing resources, or reporting the final state. It runs when execution leaves the `try` statement, whether or not an exception occurred. If an exception is not handled, the `finally` block still runs before that exception continues to propagate.

Catching `KeyboardInterrupt` is useful when a long-running script should shut down cleanly. 

---
