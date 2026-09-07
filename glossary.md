## Glossary

**argument:** A value provided to a function when the function is called.

**arithmetic operator:** A symbol, such as `+` or `*`, that denotes an arithmetic operation such as addition or multiplication.

**assignment statement:** A statement that assigns a value to a variable using `=`.

**augmented assignment:** An assignment statement that combines an operation with assignment, such as `+=` or `*=`.

**block:** One or more statements indented to indicate that they are part of another statement, such as a loop, conditional statement, or function definition.

**body:** The sequence of statements inside a compound statement, such as a function definition or loop.

**Boolean:** A type, `bool`, with two values: `True` and `False`.

**Boolean expression:** An expression whose value is either `True` or `False`.

**branch:** One of the alternative sequences of statements in a conditional statement.

**bug:** An error in a program.

**built-in function:** A function provided by Python without the need to import a module, such as `print`, `len`, or `type`.

**chained conditional:** A conditional statement with a series of alternative branches, usually written with `if`, one or more `elif` clauses, and optionally `else`.

**comment:** Text included in a program that provides information about the program but has no effect on its execution. A Python comment begins with `#`.

**concatenation:** Joining two strings end-to-end, for example with the `+` operator.

**condition:** The Boolean expression in a conditional statement that determines which branch runs.

**conditional statement:** A statement that controls the flow of execution depending on a condition.

**configuration value:** A value that controls how a program operates and is intended to be easy to change.

**constant:** A name for a value that is not intended to change while a program runs. Python does not enforce constants, but uppercase names are the conventional notation.

**`continue` statement:** A statement that stops the current loop iteration and immediately begins the next iteration.

**counter:** A variable used to count something, usually initialized to zero and then incremented.

**data type:** A category of values. Types in this tutorial include integers (`int`), floating-point numbers (`float`), strings (`str`), Booleans (`bool`), lists (`list`), and dictionaries (`dict`). Also called a **type**.

**debugging:** The process of finding and correcting errors.

**dependency:** A module or package that a program relies on.

**delimiter:** A character or string used to indicate where a string should be divided.

**dictionary:** An object that contains key-value pairs, also called items.

**docstring:** A string at the beginning of a module, function, class, or method that documents it.

**dot operator:** The operator `.`, used to access a variable, function, or method associated with a module or object.

**element:** One of the values in a list or another sequence.

**`else` block:** A block that runs if the preceding `try` block completes without raising an exception, or the alternative branch of a conditional statement.

**enumerate:** A built-in function that produces an index and the corresponding value for each element in a sequence.

**evaluate:** Perform the operations in an expression in order to compute a value.

**`except` block:** An exception handler that runs when a matching exception is raised in a `try` block.

**exception:** An error that is detected while a program is running.

**exception handler:** A block of code that runs in response to a matching exception.

**execute:** Run a statement and do what it says.

**exponentiation:** Raising one number to the power of another. Python uses the operator `**` for exponentiation.

**expression:** A combination of variables, values, function calls, and operators that is evaluated to produce a value.

**extend:** A list method that adds every element from another sequence to the end of an existing list. It modifies the list and returns `None`.

**`finally` block:** A block that runs when execution leaves a `try` statement, whether or not an exception occurred. It is normally used for cleanup.

**floating-point:** A type, `float`, used to represent finite-precision approximations to real numbers.

**format specification:** Instructions inside an f-string replacement field that control how a value is displayed, such as `.3f` for three digits after the decimal point.

**formatted string literal (f-string):** A string prefixed with `f` that can include expressions inside braces, such as `f"sample size: {n}"`.

**function:** A named sequence of statements that performs a useful operation. A function may or may not take arguments and may or may not produce a return value.

**function call:** An expression, or part of an expression, that runs a function. It consists of the function name followed by an argument list in parentheses.

**function definition:** A statement that creates a function. It begins with the keyword `def`.

**header:** The first line of a compound statement, such as a function definition, conditional statement, or loop. A header normally ends with a colon.

**IDE (integrated development environment):** An application that provides tools for writing, running, and debugging programs.

**immutable:** Describes an object whose value cannot be changed after the object is created.

**import statement:** A statement that makes the code in a module available to the current program.

**increment:** Increase the value of a variable by a specified amount.

**indentation:** Spaces at the beginning of a line that Python uses to identify a block.

**index:** An integer used to select an element in a sequence. Python indices start at `0`; negative indices count backward from the end.

**`IndexError`:** An exception raised when a sequence index is outside the valid range.

**infinite loop:** A loop without a predefined end, such as `while True`. It continues until interrupted or terminated by another statement or exception.

**integer:** A type, `int`, that represents whole numbers with arbitrary precision.

**integer division:** The operation performed by `//`, which divides two numbers and rounds down to an integer.

**invocation:** An expression, or part of an expression, that calls a method using the dot operator.

**item:** In a dictionary, another name for a key-value pair.

**iteration:** One execution of the body of a loop.

**join:** A string method that combines a sequence of strings and inserts a specified separator between them.

**key:** The first part of a key-value pair, used to look up the corresponding value in a dictionary.

**key-value pair:** An association between a key and its corresponding value in a dictionary.

**`KeyError`:** An exception raised when a requested key is not present in a dictionary.

**`KeyboardInterrupt`:** An exception normally raised when the user interrupts a running Python program by pressing `Ctrl+C`.

**keyword:** A word reserved by Python to specify program structure, such as `def`, `for`, `if`, `elif`, `else`, `in`, and `return`.

**list:** An object that contains a sequence of values.

**list comprehension:** A concise expression that creates a list by transforming or selecting elements from a sequence or another collection.

**local variable:** A variable defined inside a function that can be accessed only inside that function.

**loop:** A statement that runs one or more statements repeatedly.

**loop body:** The block of statements that runs during each iteration of a loop.

**loop variable:** A variable defined in the header of a `for` loop that refers to one element at a time.

**main function:** A function, conventionally named `main`, that coordinates the main work of a program.

**main guard:** The conditional statement `if __name__ == "__main__":`, used to run main code only when a Python file is executed as a script.

**mapping:** A relationship in which each element of one set corresponds to an element of another set. A dictionary is Python's built-in mapping type.

**membership operator:** An operator, such as `in` or `not in`, that tests whether a collection contains a value or a dictionary contains a key.

**method:** A function associated with an object and called using the dot operator, such as `results.append(4)`.

**modulus operator:** The operator `%`, which returns the remainder when one number is divided by another.

**module:** A file that contains Python code, including function definitions and sometimes other statements. A module can be imported by another Python file.

**name:** An identifier used to refer to a value, such as a variable or function name. Python names are case-sensitive.

**`NameError`:** An exception raised when Python is asked to use a name that is not defined.

**`None`:** A special value used to represent the absence of a value. A function with no explicit `return` statement returns `None`.

**object:** Something a variable can refer to. An object has a type and a value.

**operand:** One of the values on which an operator operates.

**operator:** A symbol that represents a computation, such as `+`, `//`, `**`, or `>=`.

**operator precedence:** The rules that determine the order in which operators in an expression are evaluated.

**output:** Information a program displays or otherwise produces. In this tutorial, output is usually displayed with `print`.

**package:** A collection of related modules organized so they can be imported together.

**parameter:** A name used inside a function to refer to a value passed as an argument.

**`pass` statement:** A statement that does nothing when executed. It is commonly used as a placeholder where Python syntax requires a statement.

**PEP 8:** The official style guide for Python code, covering conventions for layout, whitespace, comments, naming, and readability.

**program:** A set of instructions that performs a computation or solves a task. A program may consist of one script or many files.

**propagate:** Continue passing an exception outward through active function calls until a matching exception handler is found or the program terminates.

**pseudorandom:** Describes values generated by a deterministic algorithm that are designed to behave like random values.

**Python interpreter:** The program that reads and executes Python code.

**range:** An immutable sequence of integers, commonly used to control loop iterations or generate indices. The stop value is excluded.

**relational operator:** An operator that compares its operands: `==`, `!=`, `>`, `<`, `>=`, or `<=`.

**representation:** A string form of a value intended to show how it is represented. In an f-string, the conversion flag `!r` requests this form.

**return value:** The result of a function. When a function call is used as an expression, its return value becomes the value of that expression.

**runtime error:** An error that occurs while a program is running. In Python, runtime errors generally raise exceptions.

**scope:** The part of a program in which a name can be accessed.

**script:** Usually, a Python source file intended to be executed directly.

**separator:** A character or string inserted between elements when they are joined into a string.

**sequence:** An ordered collection of values in which each value is identified by an integer index.

**slice:** A part of a sequence selected with a range of indices. A slice includes its start index but excludes its stop index.

**source code:** The text of a program written in a programming language.

**source file:** A file that contains source code. Python source files normally use the extension `.py`.

**split:** A string method that divides a string at a specified delimiter and returns a list of strings.

**standard library:** The collection of modules and packages supplied with Python, including `math` and `random`.

**statement:** One or more lines of code that represent a command or action.

**string:** A type, `str`, that represents an immutable sequence of Unicode characters used as text.

**string literal:** A sequence of characters enclosed in quotation marks directly in the source code.

**substring:** A sequence of characters contained within a larger string.

**syntax error:** An error that makes a program impossible to parse and therefore impossible to run.

**third-party package:** Code distributed separately from Python that must normally be installed before it can be imported.

**trace:** Follow the execution of a program step by step, recording changes in variables and any output or errors.

**traceback:** A report that identifies where an exception occurred and lists the active function calls.

**true division:** The operation performed by `/`, which produces a floating-point result in Python 3.

**`try` statement:** A statement that executes a block of code and can specify handlers for exceptions and code that runs afterward.

**type:** A category of values; see **data type**.

**type conversion:** Creating a value of one type from a value of another type, such as converting a string to a floating-point number with `float`.

**`TypeError`:** An exception raised when an operation or function receives a value of an inappropriate type.

**update:** An assignment statement that gives a new value to a variable that already exists rather than creating a new variable.

**value:** An object, such as an integer, floating-point number, string, Boolean, list, or dictionary, that a program can manipulate.

**`ValueError`:** An exception raised when an operation receives a value of the correct type but an inappropriate value, such as text that cannot be converted to a number.

**variable:** A name that refers to a value.

**`while` loop:** A loop that repeatedly executes its body as long as its condition is true.
