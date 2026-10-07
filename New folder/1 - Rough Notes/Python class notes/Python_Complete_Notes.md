# Python Notes By - Divyansh Gupta


## What Is Python
- **High-level, general-purpose** programming language 
- Writes **instructions for computers** 
- Created by **Guido van Rossum** → released **1991** 
- Designed for **readability and simplicity** 

## Important characteristics of Python
- **High-level**: No direct hardware management required 
- **Interpreted**: Code executed by Python runtime 
- **Dynamically typed**: Variable types declared implicitly 

## Why Is Python Popular
- **Easy to read** beginner-friendly syntax 
- **General-purpose** utility across industries 
- Massive collection of **libraries and tools** 

## Python Use Cases
- **Web Development** 
- **Machine Learning** 
- **Data Science** 

## Large library ecosystem
- **math** → mathematical operations 
- **pandas** → data analysis 
- **tensorflow** → machine learning 

## What Is Source Code
- **Human-readable code** written by a programmer 
- **Not directly understood** by CPU 
- Typically uses **.py extension** 

## What Is Machine Code
- **Low-level instructions** executed directly by CPU 
- Represented in **binary values** (0, 1) 
- **CPU-specific** → architecture dependent 

## How Does a Programming Language Execute Code
- **Compiler**
  - Translates source code into **machine code or intermediate representation** 
  - Translation occurs **before execution** 
- **Interpreter**
  - Reads and executes code through **runtime system** 
  - Executes **bytecode** via virtual machine 

## How Python Converts Source Code and Executes It
- **Source Code** (.py) → **Python Compiler** → **Bytecode** → **Python Virtual Machine** (PVM) → **Execution** 

## Running a Python Program
- **Method 1: Run From Terminal**
  - Open terminal in **file folder** 
  - Execute: **python hello.py** (or python3) 
  - Runtime starts → processes file → **outputs result** 
- **Running a Python Program in Visual Studio Code**
  - Create **.py file** 
  - Open file in **Visual Studio Code** 
  - Execute via **Run Python File** button or integrated terminal 
  - Requires local **Python installation** (VS Code is only an editor) 

## Comments in Python
- Text **ignored** during normal program execution 
- Explains code logic to **programmers** 
- Single-line indicator: **#** 
- Can follow statements **after code** on the same line 

## Basic Python Syntax
- **Syntax**: Rules for writing valid code 
- **print**: Built-in Python function 
- **" "** (Quotes): Defines a string 
- **( )** (Parentheses): Used for function calls 

---

## Variable
- **Variable**: a named place/reference used to store or keep a value so that we can use that value later
- **Purpose**: give meaningful names to values -> code easier to understand
- **Flexibility**: can refer to different types of values (text, whole number, decimal)

## Assignment
- **Assignment**: process of giving a value to a variable
- **Operator**: `=` symbol
- **Direction**: happens from Right to Left -> value on right assigned to variable on left
- **Mistake to avoid**: `=` does not mean mathematical equality ("same as")

## Reassignment
- **Reassignment**: assigning a new value to an existing variable
- **Result**: variable refers to the new value -> previous value is no longer current
- **Use case**: when a value needs to change during program execution

## Variable naming rules
- **Letters**: allowed in names
- **Numbers**: allowed -> but cannot start with a number
- **Underscore**: `_` allowed -> useful for readability
- **Spaces**: cannot contain spaces
- **Case-sensitive**: uppercase and lowercase treated as different names
- **Python keywords**: cannot use reserved words (e.g., `if`, `class`)

## Naming convention
- **Definition**: recommended ways of writing names for consistency and readability
- **Rules vs Conventions**: rules = what we *can* write -> conventions = what we *should* write
- **Meaningful names**: name should communicate what the value represents
- **Abbreviations**: avoid unnecessary abbreviations
- **Consistency**: use one naming style consistently throughout a program

## snake_case
- **Usage**: Python commonly recommends snake_case for variables
- **Casing**: use lowercase letters
- **Separation**: separate multiple words using underscores

## Multiple assignment
- **Definition**: assigning values to multiple variables in a single statement
- **Matching positions**: multiple values are assigned in corresponding positions (e.g., `name, age = "Rahul", 18`)
- **Same value**: identical value can be assigned to multiple variables at once (e.g., `x = y = z = 0`)

---

## 2.3 Data Types
- **Objective**: Understand basic data types (`int`, `float`, `str`, `bool`, `None`) and `type()`
- **1. What Is a Data Type?**: Tells us what kind of value we are working with
  - **Why Do Data Types Matter? (any 3)**:
    - Determine how information is represented (e.g., age = `18`)
    - Tell Python how to treat the value (e.g., text vs number)
    - Distinguish state (e.g., `True`/`False`)
- **2. Integer**: Whole number without a decimal part
  - **Examples**: `10`, `-7`, `0`
  - **Important Point**: `18` is an integer, `18.0` is a float
- **3. Floating-Point Numbers**: Number containing a decimal part
  - **Examples**: `5.8`, `-2.75`, `0.5`
  - **Integer vs Floating-Point Number**: `10` (int) vs `10.0` (float)
  - **Example**: `age = 18` (int), `height = 5.8` (float)
- **4. Strings**: Sequence of characters used to represent text
  - **Example**: `name = "Rahul"`
  - **More Examples**: `"Patna"`, `"Hello Python"`
- **5. Single Quotes and Double Quotes**:
  - **Double Quotes**: `"Rahul"`
  - **Single Quotes**: `'Rahul'` (Both represent strings)
- **6. Strings Can Contain Spaces**: `"Rahul Kumar"` is a single string value
- **7. String vs Number**:
  - **Easy Way to Remember**: `18` → integer, `"18"` → string (quotes make the difference)
- **8. Boolean Values**: Represents one of two possible states (`True` or `False`)
  - **Example**: `is_student = True`
  - **Everyday Examples (any 3)**:
    - Student is present → `True`
    - User is logged in → `True`
    - Door is open → `False`
- **9. Boolean Values Are Case-Sensitive**: Must use uppercase first letter (`True`/`False`, not `true`/`false`)
- **10. None**: Special value representing absence of a value
  - **Everyday Example**: Student record where result is not entered yet (`result = None`)
  - **Important**: Not equal to `0`, `False`, or `""`
- **11. Basic Data Types at a Glance (any 3)**:
  - `int`: `18`
  - `float`: `5.8`
  - `str`: `"Rahul"`
- **12. What Is type()?**: Built-in function to identify a value's type
  - **Example**: `print(type(18))` → `<class 'int'>`
- **13. Using type() with Different Values**:
  - **Integer**: `<class 'int'>`
  - **Floating-Point Number**: `<class 'float'>`
  - **String**: `<class 'str'>`
  - **Boolean**: `<class 'bool'>`
  - **None**: `<class 'NoneType'>`
- **14. Understanding type() Output**: Focus on the core word (`int`, `float`, `str`, `bool`, `NoneType`)
- **15. Basic Type Identification**: Identifying the type of value we are working with
  - **Example**: `a = 10` → `type(a)` is `int`
- **16. Important Difference: 10, 10.0, and "10"**:
  - **Why? (any 3)**:
    - `10` is a whole number (`int`)
    - `10.0` has a decimal (`float`)
    - `"10"` is inside quotes (`str`)
- **17. Another Important Difference: True, "True", and None**:
  - `True` → `bool`
  - `"True"` → `str`
  - `None` → `NoneType`
- **18. Variables Can Refer to Different Types**: Reassigning a variable can change its current data type (`value = 10` then `value = "Python"`)
- **19. A Complete Example**: Shows all 5 basic types and checking their types using `type()`
- **20. Common Beginner Mistakes**:
  - **Mistake 1: Confusing 18 with "18"**: Number vs Text
  - **Mistake 2: Confusing 10 with 10.0**: `int` vs `float`
  - **Mistake 3: Writing Boolean Values Incorrectly**: `true` instead of `True`
  - **Mistake 4: Confusing None with 0**: Absence of value vs integer zero
  - **Mistake 5: Confusing None with "None"**: `NoneType` vs `str`
  - **Mistake 6: Confusing True with "True"**: `bool` vs `str`
- **21. Quick Comparison**: Maps values like `18`, `18.5`, `"18"`, `True`, `None` to their respective types
- **22. Key Points to Remember (any 3)**:
  - Data type tells us what kind of value we are working with
  - `type()` identifies the type
  - `10`, `10.0`, and `"10"` are three different types
- **Quick Revision Activity**: Identify types for `int`, `float`, `str`, `bool`, `None`

## 2.4 Python Type Casting
- **Objective**: Understand type casting, why it's used, and how to convert to `int`, `float`, `str`
- **1. What Is Type Casting?**: Converting a value from one data type to another
  - **Easy Way to Remember**: `"25"` → string, `25` → integer
- **2. Why Do We Use Type Casting?**: To change values into a usable format (e.g., text `"18"` into math-ready `18`)
- **3. Converting to an Integer Using int()**:
  - **Example: String to Integer**: `int("85")` → `85`
  - **Example: Float to Integer**: `int(99.8)` → `99`
  - **Important Point**: `int()` removes the decimal part; it does **not** round
- **4. Converting to a Floating-Point Number Using float()**:
  - **Example: Integer to Float**: `float(18)` → `18.0`
  - **Example: String to Float**: `float("5.8")` → `5.8`
- **5. Converting to a String Using str()**:
  - **Example: Integer to String**: `str(101)` → `"101"`
  - **Example: Float to String**: `str(5.8)` → `"5.8"`
- **6. Checking the Type Before and After Conversion**: Use `type()` to verify the change
- **7. Common Type Conversions (any 3)**:
  - `"25"` → `int("25")` → `25`
  - `18` → `float(18)` → `18.0`
  - `99.8` → `int(99.8)` → `99`
- **8. Important Rules for Beginners**:
  - **Rule 1: A number written inside quotation marks is a string**: `"10"` is text
  - **Rule 2: int() needs a whole-number string**: `int("hello")` will crash
  - **Rule 3: Use float() for decimal-number strings**: `int("5.8")` will crash
- **9. A Complete Example**: Shows converting string/int to int/float/str and verifying with `type()`
- **10. Common Beginner Mistakes**:
  - **Mistake 1: Thinking printed values always show their type**: `"25"` prints as `25` but is still a string
  - **Mistake 2: Expecting int() to round a decimal number**: `int(7.9)` becomes `7`, not `8`
  - **Mistake 3: Forgetting quotation marks for a string**: `25` is int, `"25"` is str
- **11. Key Points to Remember (any 3)**:
  - Type casting converts a value to another type
  - `int()` removes the decimal part
  - Use `type()` to check a value's data type
- **Quick Revision Activity**: Identify result and type of conversions like `int("50")`, `float(10)`, `str(5.5)`

---

## Introduction & Arithmetic Operators
- **Supported types**: `int`, `float`, `bool`, `str` (special behavior)
- **Unsupported types**: `None` (raises `TypeError`)
- **Available operators**: `+`, `-`, `*`, `/`, `//`, `%`, `**`

## Addition `+`
- **int + float**: Returns `float`
- **str + str**: **Concatenates** strings
- **str + number**: Raises **TypeError**
  - Requires conversion: `str(18)`

## Subtraction `-`
- **Subtracting float**: Returns `float`
- **Subtracting negatives**: Becomes **addition**
  - Formula: `a - (-b) = a + b`

## Multiplication `*`
- **int * float**: Returns `float`
- **str * int**: **Repeats** string sequence
- **str * float**: Raises **TypeError** (requires integer count)

## Division `/`
- **Return type**: Always returns **float** (even `int / int`)
- **Division by zero**: Raises **ZeroDivisionError**

## Floor Division `//`
- **Floor behavior**: Rounds down toward **negative infinity**
- **Not truncation**: Does not simply remove decimal toward zero
- **Negative operands**: `-10 // 3` → **-4**
- **Zero division**: Raises **ZeroDivisionError**

## Modulus `%`
- **Return value**: Remainder of division
- **Formula**: `a == (a // b) * b + (a % b)`
- **Negative operands**: Result matches **divisor's sign**
  - `-10 % 3` → **2**
  - `10 % -3` → **-2**
- **Zero division**: Raises **ZeroDivisionError**

## Exponentiation `**`
- **Power of zero**: Always returns **1** (`10 ** 0` → 1)
- **Negative exponent**: Returns **reciprocal** (`2 ** -2` → `1 / (2 ** 2)` → 0.25)
- **Edge case**: Unparenthesized negative base is evaluated **after exponentiation**
  - `-2 ** 2` → `-(2 ** 2)` → **-4**
  - `(-2) ** 2` → **4** (use parentheses for negative base)

## Operator Precedence
- **Order of evaluation**: Highest to lowest priority
  1. `()` → **Parentheses** (explicit control)
  2. `**` → **Exponentiation**
  3. `*`, `/`, `//`, `%` → **Multiplication/Division group**
  4. `+`, `-` → **Addition/Subtraction group**
- **Same precedence**: Evaluated **left to right**

## Operations on `bool`
- **Internal representation**: `bool` is subclass of `int`
  - `True` → **1**
  - `False` → **0**
- **Addition**: `True + True` → **2**
- **Multiplication**: `False * 5` → **0**
- **Division**: `True / 2` → **0.5**
- **Best practice**: Avoid treating booleans as numbers intentionally

## Operations on `None`
- **Value meaning**: Absence of value (not `0` or `False`)
- **Arithmetic operations**: Raises **TypeError** (`None + 5`)
- **String operations**: Raises **TypeError** (`"Age: " + None`)

## Operations on Strings
- **str + str**: **Concatenation** allowed
- **str * int**: **Repetition** allowed
- **str - str**: Raises **TypeError**
- **str / str**: Raises **TypeError**
- **str % int**: Performs **old-style string formatting** (`"Hello %s" % name`)

## Mixed Type Operations & Precision
- **int and float**: Mixed arithmetic always returns **float**
- **Floating-point precision**: Decimals stored as **binary fractions**
- **Inexact results**: `0.1 + 0.2` → `0.30000000000000004`
- **Exact arithmetic**: Requires **`decimal` module**

## Practical Examples & Common Mistakes
- **Even/Odd check**: Use modulus (`number % 2 == 0` for even)
- **Mistake**: Using `^` for power
  - `^` is **bitwise XOR**
  - `**` is **exponentiation**
- **Mistake**: Assuming `//` removes decimal
  - Remember it rounds to **negative infinity**
- **Mistake**: Expecting `/` to return integer
  - Always returns **float**

---

## Introduction & Basics
- **String**: Sequence of characters used to store text
- **String creation**: Use single `' '` or double `" "` quotes
- **Spaces**: Stored and treated as **characters**
- **Empty string**: Contains zero characters (`""`)
- **Sequence property**: Characters stored in order using an **index**

## String Indexing
- **Zero-based indexing**: First character is always index `0`
- **Negative indexing**: Starts from the end of the string
  - **Important distinction**: `0` → first character, `-1` → last character
- **Edge cases**: Accessing non-existent index raises **IndexError**

## String Slicing
- **Syntax**: `string[start:stop]` 
- **Inclusion rules**: `start` is included, `stop` is excluded
- **Omitted start**: Starts from the beginning (`[:3]`)
- **Omitted stop**: Goes until the end (`[2:]`)
- **Copying**: `[:]` creates a full copy of the string
- **Negative slices**: Works normally (stop index still excluded)
- **Step parameter**: `string[start:stop:step]` controls movement
  - **Step 1**: Moves one character at a time
  - **Step 2**: Selects every second character
- **Reversing**: `[::-1]` moves right to left
- **Important slicing rule**: `start` → included, `stop` → excluded, `step` → movement

## String Length & Operations
- **Length**: `len()` returns total character count (including spaces)
- **Length vs index**: First index = `0`, Last index = `len(string) - 1`
- **Concatenation**: `+` joins strings together
- **Mixed concatenation**: String + integer raises **TypeError** (requires `str()`)
- **Repetition**: `*` repeats string (requires integer count)
- **Immutability**: Characters cannot be changed after creation (raises **TypeError**)

## Case Conversion Methods
- **Methods**: Functions associated with an object (`string.method()`)
- **Case conversion types**: `upper()`, `lower()`, `capitalize()`
- **upper()**: Converts all letters to uppercase
- **lower()**: Converts all letters to lowercase
- **capitalize()**: First character uppercase, remaining lowercase
- **title()**: First character of each word uppercase
- **swapcase()**: Swaps uppercase to lowercase and vice versa
- **casefold()**: Aggressive lowercase for case-insensitive comparisons

## Searching in Strings
- **Search operators**: `in`, `not in`, `find()`
- **in operator**: Returns `True` if substring exists
- **not in**: Returns `True` if substring does not exist
- **find()**: Returns index of first occurrence
  - **Important**: Returns `-1` if not found (no error)
- **index()**: Returns index of first occurrence
  - **Difference**: Raises **ValueError** if not found
- **count()**: Returns total number of occurrences
- **startswith()**: Checks if string begins with specific value
- **endswith()**: Checks if string ends with specific value

## Replacing Text
- **replace()**: `string.replace(old, new)`
- **Multiple occurrences**: Replaces all matching occurrences by default
- **Limiting replacement**: `replace(old, new, count)` replaces only specific number of times

## Comparison & Whitespace
- **Case-sensitive**: Searches and comparisons strictly respect case
- **Comparison operators**: `<, >, <=, >=, ==, !=` check character ordering
- **Equality**: `==` checks value equality (do not confuse with `=` assignment)
- **Whitespace**: Spaces, tabs, and newlines alter comparison results
- **strip()**: Removes whitespace from both ends
- **lstrip()**: Removes whitespace from left side only
- **rstrip()**: Removes whitespace from right side only

## Escape Characters & Multi-Line
- **New line**: `\n`
- **Tab**: `\t`
- **Double quote**: `\"`
- **Single quote**: `\'`
- **Raw strings**: `r` prefix treats backslashes literally (used for paths/regex)
- **Multi-line strings**: Created using triple quotes (`"""` or `'''`)
- **Membership verification**: `in` and `not in` verify substring presence

## Functions, Formatting & Immutability
- **Useful string methods**: `find()`, `split()`, `strip()`
- **len()**: Built-in function for character count
- **str()**: Converts numeric/other values to string
- **String formatting**: **f-strings** (`f"Text {var}"`) easily combine variables and text
- **split()**: Breaks string into a **list** (optional separator)
- **join()**: Combines iterable items into a **single string**
- **Return behavior**: Methods always return **new strings**
- **Immutability example**: Original string remains unmodified after applying methods (e.g., `text.upper()`)

## Common Mistakes
- **Mistake 1**: Forgetting zero-based indexing (first char is `0`, not `1`)
- **Mistake 2**: Forgetting slice `stop` is excluded
- **Mistake 3**: Using invalid index (raises **IndexError**)
- **Mistake 4**: Trying to change a character directly (raises **TypeError**)
- **Mistake 5**: Using `+` between string and integer (raises **TypeError**)
- **Mistake 6**: Forgetting that string searches are strictly **case-sensitive**

## Quick Revision
- **String Basics**: Immutable sequences of text characters
- **Indexing**: Starts at `0`, negative starts at `-1`
- **Slicing**: `start` included, `stop` excluded
- **Length**: Spaces count as characters
- **Concatenation**: Join using `+`
- **Repetition**: Repeat using `*`
- **Case Conversion**: `upper()`, `lower()`, `title()`, `capitalize()`, `swapcase()`, `casefold()`
- **Searching**: `find()` returns `-1`, `index()` raises error
- **Replacing**: `replace(old, new)`
- **Whitespace**: `strip()` cleans surrounding spaces
- **Splitting and Joining**: `split()` creates lists, `join()` creates strings
- **Important Errors**: **IndexError** (bad index), **TypeError** (mutating/mixed types), **ValueError** (index not found)

## Quick Reference Table
- **Create string**: `"Python"`
- **Index / Negative**: `text[0]` / `text[-1]`
- **Slice / Step**: `text[1:4]` / `text[::2]`
- **Reverse**: `text[::-1]`
- **Length**: `len(text)`
- **Concatenation**: `"Hello" + "World"`
- **Repetition**: `"Hi" * 3`
- **Cases**: `text.upper()`, `text.lower()`, `text.capitalize()`, `text.title()`
- **Search / Find**: `"A" in text`, `text.find("A")`
- **Count**: `text.count("a")`
- **Starts / Ends**: `text.startswith("Py")`, `text.endswith("on")`
- **Replace**: `text.replace("old", "new")`
- **Whitespace**: `text.strip()`
- **Split / Join**: `text.split()`, `" ".join(words)`
- **Convert**: `str(value)`

## Final Revision Points
- **Immutability rule**: String methods return new strings; they never modify the original variable
- **Search differences**: `find()` yields `-1` when absent, `index()` crashes with **ValueError**
- **Type mixing**: Always use `str()` or **f-strings** when combining numbers with strings

---

## Boolean and Logical Expressions
- **Objective**: Understand boolean values, operators, combinations, and truthiness
- **1. Boolean Values**: Represent states (`True` or `False`)
  - **Example**: `is_student = True`, `is_logged_in = False`
- **1.1 Case-Sensitive**: Must use uppercase first letter (`True`, not `true`)

## Comparison Operators
- **2. Comparison Operators**: Compare values to return Boolean results
- **3. Common Operators (any 3)**:
  - `==` (Equal to)
  - `!=` (Not equal to)
  - `>` (Greater than)
- **4. Equal to `==`**: Checks if values are identical
  - **Important: `=` vs `==`**: `=` is assignment, `==` is comparison
- **5. Not Equal to `!=`**: Checks if values are different
- **6. Greater Than `>`**: Checks if left is strictly larger
- **7. Less Than `<`**: Checks if left is strictly smaller
- **8. Greater Than or Equal to `>=`**: Includes equality
- **9. Less Than or Equal to `<=`**: Includes equality
- **10. Quick Practice**: `a == b` → `False`, `a != b` → `True`

## Boolean Expressions
- **11. Definition**: Expression that evaluates to `True` or `False`
- **11.1 With Variables**: Evaluates stored states (`age >= 18`)
- **12. With Strings**: Compares text equality (`name == "Rahul"`)
- **13. Combining Expressions**: Join multiple checks using logical operators

## Logical Operators: `and`, `or`, `not`
- **14. `and`**: `True` only when **both** are true
  - **Basic Example**: `True and False` → `False`
- **14.1 Truth Table for `and`**:
  - **Easy Rule**: Everything must be `True`
- **15. `and` with Comparisons**: Evaluates both sides (`age >= 18 and age <= 60`)
- **16. `or`**: `True` when **at least one** is true
  - **Examples**: `True or False` → `True`, `False or False` → `False`
- **16.1 Truth Table for `or`**:
  - **Easy Rule**: At least one must be `True`
- **17. `or` with Comparisons**: Evaluates either side (`age < 18 or age > 60`)
- **18. `not`**: Reverses the Boolean value
  - **Examples**: `not True` → `False`
  - **Easy Rule**: Reverse the result
- **18.1 `not` with Comparison**: Flips condition output (`not age < 18`)
- **19. Truth Tables Together**: 
  - **and**: Both must be `True`
  - **or**: One must be `True`
  - **not**: Flips state

## Combining Conditions & Precedence
- **20. Combining Conditions**: Linking multiple boolean tests
- **20.1 Two with `and`**: Both requirements must pass
- **20.2 Two with `or`**: Only one requirement must pass
- **20.3 Using `not`**: Inverts test result
- **21. More Than Two**: Chain multiple checks (`age >= 18 and has_id and has_ticket`)
- **22. Mixing `and` / `or`**: Use both in a single statement
- **23. Parentheses**: Explicitly controls evaluation order for clarity
- **24. Operator Precedence**: Order is **`not` → `and` → `or`**
  - **Example**: `True or False and False` → `and` executes first → `True`

## Truthiness
- **25. Basic Truthiness**: How values behave in Boolean contexts
  - **Truthy Values**: `True`, non-zero numbers, non-empty strings
  - **Falsy Values**: `False`, `0`, `""` (empty string), `None`
- **26. With `bool()`**: Function to show Boolean representation
  - **More Examples**: `bool(1)` → `True`, `bool("")` → `False`, `bool(None)` → `False`
- **27. Truthiness Table**:
  - **Truthy**: `True`, `1`, `-1`, `10`, `"Python"`
  - **Falsy**: `False`, `0`, `""`, `None`
- **28. Truthiness vs Data Type**: Different concepts (`0` is type `int`, but its truthiness is `False`)

## Complete Example & Mistakes
- **29. Complete Example**:
  - **Step 1**: Assign variable (`age = 20`)
  - **Step 2**: Assign Boolean (`is_student = True`)
  - **Step 3**: Compare condition (`adult = age >= 18` → `True`)
  - **Step 4**: Logical combine (`adult and is_student` → `True`)
- **30. Common Beginner Mistakes**:
  - **Mistake 1**: Confusing `=` (assign) with `==` (compare)
  - **Mistake 2**: Confusing `==` (equal) with `!=` (not equal)
  - **Mistake 3**: Reversing `>` and `<`
  - **Mistake 4**: Forgetting `>=` and `<=` include equality
  - **Mistake 5**: Thinking `and` means "one is true" (requires both)
  - **Mistake 6**: Thinking `or` requires both to be true (requires one)
  - **Mistake 7**: Forgetting `not` reverses the result
  - **Mistake 8**: Confusing `0` (int) with `False` (bool)
  - **Mistake 9**: Confusing empty string `""` (falsy) with string `"False"` (truthy)

## Summary
- **31. Quick Comparison**: Operators (`==`, `>`, etc.), Logic (`and`, `or`, `not`), and Truthiness concepts
- **32. Key Points (any 3)**:
  - **Point 1**: Boolean values strictly represent `True` or `False`
  - **Point 2**: Precedence evaluation is `not` → `and` → `or`
  - **Point 3**: Truthiness and data type are separate concepts
- **Quick Revision Activity**: Practice evaluating combined expressions and basic truthiness values

---

## Input and Output Basics
- **Objective**: Understand `input()`, `print()`, multiple inputs, type conversion, formatting, and f-strings
- **Input** → Data flows from **user to program** (`input()`)
- **Output** → Program **displays data** to user (`print()`)

## `input()`
- **Takes data**: Reads from keyboard
  - Example: `name = input()`
- **With a message**: Displays a **prompt message**
  - Example: `name = input("Enter your name: ")`
- **Important behavior**: Always returns a **string** (`str`) by default
- **Checking type**: Use `type()` to verify (returns `<class 'str'>` even for digits)

## `print()`
- **Displays information**: Outputs text to screen
  - Example: `print("Hello")`
- **Printing variables**: Displays **stored values**
- **Printing multiple values**: Separate with **commas**
  - Automatically inserts **space** between values

## `input()` and `print()` Together (Simple Map)
- **User enters data** → `input()` → **Stored in variable** → `print()` → **Output displayed**

## Multiple Inputs
- **Separate variables**: Each piece of info requires its **own `input()`** call
- **Independent storage**: Values stored separately (`first_name`, `last_name`)
- **One line input**: Use **`.split()`** to separate values
  - Separates pieces using **spaces by default**
- **Numeric inputs**: `.split()` returns **strings**
  - Requires **type conversion** for mathematical operations

## Type Conversion
- **Definition**: Changes value from **one data type** to another
- **`int()`**: Converts suitable value to **integer** (`<class 'int'>`)
- **Converting input to integer**: Wrap input directly (`int(input())`)
- **Why it's needed**: Without it, `+` **joins strings** (`"10" + "20" = "1020"`)
- **Correct addition**: Converted integers perform **mathematical addition**
- **`float()`**: Converts suitable value to **floating-point** (`<class 'float'>`)
- **Taking float input**: Wrap input directly (`float(input())`)
- **`str()`**: Converts value to **string** (`<class 'str'>`)
- **Common examples**: `int("25")` → `25`, `str(25.5)` → `"25.5"`
- **Limitation**: Input must be **valid numeric representation** (cannot convert `"hello"`)

## Formatted Output & f-Strings
- **Formatted output**: Presents information in **clear, readable form**
- **f-Strings**: Created by placing **`f` before quotes**
- **Basic example**: Place variables inside braces (`f"Hello {name}"`)
- **With expressions**: Evaluates code inside braces (`f"Sum = {a + b}"`)
- **With arithmetic**: Calculates math directly (`f"Total = {price * qty}"`)
- **With floats**: Works identically with decimal numbers
- **Formatting decimal places**: Use `:.2f` inside braces
  - `f` → floating-point formatting
  - `2` → show **two decimal places** (`f"{price:.2f}"`)
- **Combined flow**: Read input → convert type → format with f-string → print
- **Complete example (Simple Bill)**: Take string, float, int inputs → calculate total → display using f-strings

## Advanced Multiple Input
- **One line with conversion**: `map(int, input().split())`
  - **What happens here?**:
    - `input()` → takes full line
    - `.split()` → separates values
    - `map(int, ...)` → applies **integer conversion** to each
- **Beginner approach**: Use **separate input statements** for clarity before using `map()`

## `print()` Parameters
- **`sep` parameter**: Changes **separator** between multiple values
  - Default: space (`" "`)
  - Example: `print("A", "B", sep="-")`
- **`end` parameter**: Controls **ending character**
  - Default: new line (`\n`)
  - Example: `print("A", end=" ")`

## Common Beginner Mistakes
- **Mistake 1**: Assuming `input()` returns number (it returns **string**)
- **Mistake 2**: Doing math on **string input** (joins instead of adding)
- **Mistake 3**: Forgetting the **`f`** in f-strings
- **Mistake 4**: Forgetting **curly braces** around f-string variables
- **Mistake 5**: Using `int()` for **decimal strings** (must use `float()`)
- **Mistake 6**: Assuming `"20"` and `20` are identical (different **data types**)
- **Mistake 7**: Converting **invalid text** (`int("hello")`)

## Summary & Review
- **Quick Comparison**:
  - `input()` → Take input
  - `print()` → Display output
  - `int()`/`float()`/`str()` → Type conversion
  - `.split()` → Separate pieces
  - `f"..."` → Format string
  - `sep`/`end` → Control print behavior
- **Key Points (any 3)**:
  - `input()` always returns a **string by default**
  - Without conversion, `+` performs **string concatenation**
  - f-strings evaluate variables and math **inside curly braces**
- **Quick Revision Activity (Simple Map)**:
  - **Take input** → **Convert type** → **Store variable** → **Calculate** → **Display formatted output**

---

## What Are Conditional Statements?
- **Purpose**: make decisions based on conditions
- **Behavior**: True → execute block, False → skip or execute other block
- **Example scenarios**:
  - Pass → success message
  - Age >= 18 → allow continue
  - Positive number → display message
  - Correct password → welcome message

## Conditions in Python
- **Boolean evaluation**: produces `True` or `False`
- **Example**: `age >= 18` is `True` if 20, `False` if 15

## The `if` Statement
- **Syntax**: `if condition:` followed by indented block
- **`if` keyword**: starts the statement
- **Condition**: Boolean expression to check
- **Colon `:`**: marks the start of the block
- **Indented statement**: executes only if condition is `True`

## First `if` Example
- **Setup**: `age = 20`, condition `if age >= 18:`
- **Evaluation**: `20 >= 18` → `True`
- **Execution**: prints "You are an adult."

## What Happens When the Condition Is False?
- **Behavior**: skips the indented block completely
- **Result**: no output/action for that block

## Indentation in `if`
- **Purpose**: identifies which statements belong to the block
- **Multiple statements**: grouped together by identical indentation
- **Consistency**: must use same indentation level (4 spaces recommended)

## The `if-else` Statement
- **Purpose**: choose exactly one of two alternatives
- **Syntax**: `if condition:` block `else:` block
- **Example**: `16 >= 18` → `False` → skips `if`, runs `else` block

## `if` with a Number
- **Positive check**: `if number > 0:`
- **Evaluation**: `10 > 0` → `True` (Positive), `-5 > 0` → `False` (Not positive)

## `if` vs `if-else`
- **`if`**: action happens only when true (no alternative)
- **`if-else`**: exactly one of two blocks will execute

## The `if-elif-else` Statement
- **Purpose**: handle more than two possible situations
- **Syntax**: `if` → `elif` → `else`
- **Execution flow**: checks top to bottom
- **Branch selection**: first `True` condition executes, remaining skipped

## Order Matters in `if-elif-else`
- **Rule**: highest or most specific thresholds must come first
- **Reason**: Python stops checking after the first `True` condition

## Is `else` Mandatory?
- **Rule**: optional
- **Behavior**: if omitted and no conditions are `True`, nothing executes

## Multiple `elif` Statements
- **Rule**: unlimited `elif` branches allowed
- **Evaluation**: checks sequentially top to bottom

## Nested Conditions
- **Definition**: `if` statement placed inside another `if` statement
- **Walkthrough**: outer condition `True` → enters block → checks inner condition
- **With `else`**: outer `else` handles outer failure, inner `else` handles inner failure
- **Why use**: when decisions depend on previous decisions
- **Drawback**: too many levels reduce readability

## Multiple Conditions
- **`and` operator**: all combined conditions must be `True`
- **`or` operator**: at least one condition must be `True`
- **`not` operator**: reverses Boolean result (`not False` → `True`)
- **Combining**: mix operators to evaluate complex states
- **Parentheses**: used to group conditions and clarify precedence (`not` → `and` → `or`)

## Separate `if` Statements vs `if-elif-else`
- **Separate `if`**: checked independently → multiple blocks can execute
- **`if-elif-else`**: checked in order → maximum one block executes

## Practical Examples
- **Even/Odd**: `number % 2 == 0`
- **Pass/Fail**: `marks >= 40`
- **Grade**: `if-elif-else` chain descending (>=90, >=75, etc.)
- **Login**: `username == "admin" and password == "1234"`
- **Eligibility**: `age >= 18 and has_id`
- **Nested Decision**: outer check for pass, inner check for specific grade

## Common Beginner Mistakes
- **Missing colon**: `:` required immediately after condition
- **Missing indentation**: conditional block lines must be indented
- **Assignment vs Comparison**: use `==` for comparison, not `=`
- **Separate `if` over `elif`**: causes multiple unwanted true blocks to run
- **Wrong `elif` order**: lower thresholds first block higher ones
- **Over-nesting**: too deep is confusing → combine with `and`/`or` instead
- **Confusing `and`/`or`**: `and` requires all, `or` requires one
- **Forgetting `not`**: completely reverses the truth value

## Quick Comparison Table
- **`if`**: execute block when true
- **`if-else`**: choose between 2 alternatives
- **`if-elif-else`**: choose among multiple alternatives
- **Nested `if`**: decision inside another decision
- **Multiple conditions**: checking >1 requirement
- **`and`**: all true
- **`or`**: ≥1 true
- **`not`**: reverses result

## Key Points to Remember
- **Core purpose**: allow programs to make decisions
- **Execution flow**: `if-elif-else` checks top-to-bottom, stops at first `True`
- **Syntax rules**: `:` required, indentation defines blocks, `=` assigns vs `==` compares

## Quick Revision Activity
- **Goal**: mentally trace complex Boolean expressions (`age >= 18 and marks >= 40`)
- **Action**: identify individual conditions, results, combined logic, and executed block

---

## 2.10 For Loops (Objective)
- **Objective**: Understand iteration, `for` loops, `range()`, string iteration, and nested loops

## Iteration Basics
- **Iteration**: Repeating a specific code block multiple times
- **Why need it**: Prevents manual code duplication
  - Useful for **processing collections** (like strings)
  - Automates **repetitive math** (e.g., sum 1 to 100)
- **Loop types**: `for` and `while`
- **Basic syntax**: `for variable in sequence:` -> indented block
- **Loop variable**: Automatically gets a **new value** every iteration

## `range()` Function
- **Purpose**: Generates an integer sequence
- **Stop value**: Always **excluded**
- **range(stop)**: Starts at `0` (default) -> increments by `1` (default)
- **range(start, stop)**: Begins at `start` -> ends just before `stop`
- **range(start, stop, step)**: Controls increment amount
- **Positive step**: Moves values **forward**
- **Negative step**: Moves values **backward**
  - **Negative step rule**: Start value must be > stop value
- **Quick examples**: 
  - 1 to 10: `range(1, 11)`
  - Evens: `range(2, 11, 2)`
  - Odds: `range(1, 11, 2)`

## Practice Patterns
- **Sum calculation**: Accumulator variable (`total = 0`) updated inside loop (`total = total + i`)
  - **Dry run**: Trace `i` and `total` state step-by-step per iteration
- **Multiplication table**: Print `number * i` dynamically
- **String iteration**: Loop processes exactly **one character** at a time (`for char in word:`)
  - **Counting**: Update `count = count + 1` per character
  - **Searching**: Use `if` inside loop (`if char == "a":`)
- **Combining for/if**: Loop generates sequence -> `if` filters them (e.g., `if i % 2 == 0:`)

## Nested Loops
- **Definition**: A loop inside another loop
- **Execution rule**: Inner loop runs **completely** for every single outer iteration
  - Total runs = outer limit × inner limit
- **Row-column relationship**:
  - **Outer loop**: Controls rows
  - **Inner loop**: Controls columns (items per row)
- **print() placement**:
  - Inner loop: `print(..., end="")` keeps items on **same line**
  - Outer loop: Empty `print()` moves to **next row**
- **Dynamic inner loop**: Use outer variable as inner limit (`range(1, row + 1)`)
  - Adjusts shape per row (e.g., expanding triangle pattern)

## Common Mistakes & FAQs
- **Mistake**: Expecting **stop value** to be included
- **Mistake**: Missing or incorrect **indentation**
- **Mistake**: Wrong **start/stop** boundaries
- **Mistake**: Mismatching start/stop with **step direction**
- **Mistake**: Confusing **outer (rows)** vs inner (columns) control
- **Mistake**: Misplacing `print()` indentation (breaks grid shape)
- **FAQ: Stop included?**: No
- **FAQ: Step of 2?**: Increases value by 2
- **FAQ: Negative step?**: Yes, moves backward
- **FAQ: Loop strings?**: Yes, character by character
- **FAQ: Nested loop?**: A loop placed inside another

## `for` vs `while`
- **Prefer `for`**:
  - Known **repetition count**
  - Iterating through a **sequence/string**
  - Fixed start/stop ranges
- **Prefer `while`**:
  - Repetition depends on a **condition**
  - **Unknown** repetition count
  - Stopping depends on **changing data**

## Key Takeaways
- **range()**: Stop excluded, step controls direction/increment
- **Nested loops**: Inner fully executes per outer step
- **Strings**: Inherently iterable sequence of characters
- **Loop choice**: Known count -> `for`, condition-based -> `while`
