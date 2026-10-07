=w21/08/2026

Status : #baby 

Tags : 


# Python
## Notes 21/08/2026
- Python was created by **Guido van Rossum** and first released in **1991**.
- command to run python is :-
```
python <filename.py>
```
- 

## Notes 24/08/2026
### DataTypes
| Data Type  | Example   | Common Use             |
| ---------- | --------- | ---------------------- |
| `int`      | `18`      | Whole numbers          |
| `float`    | `5.8`     | Decimal numbers        |
| `str`      | `"Rahul"` | Text                   |
| `bool`     | `True`    | True/false information |
| `NoneType` | `None`    | Absence of a value     |
- in string opening quote will only work as closing quote
- make sure of case sensitivity in python bool (True)
- **Dry Run :** ?
- 
## Notes 25/08/2026
### Arithmetic Operators
- Addition of string is called ==String Concatenation==
- divide operator gives output in float only
```
a=10
b=25
print(a/b)
```
- `/` : is ==division==
- `//` : is ==floor division== (gives output in integer round off)
- `%` : is ==modulus== (gives reminder)
- `**`: is ==Exponent== 

## Notes 26/08/2026
- Indexing
```
P   Y   T   H   O   N
0   1   2   3   4   5  (forward order)
-6  -5  -4  -3  -2  -1 (Reverse Indexing)
```
- indexing program example
```
a="PYTHON"
print(a[3])
```
- length of string `len(variable)`
```
a="PYTHON"
print(len(a))
```
- string slicing 
```

variable[start (deafult = start or 0):end (deafult = last index+1) (ending index is not counted) :step(deafult = 1) (cannot = 0) (negative steps will go reverse)]

```
- how following will be stored
```
a="python"
b=a            b will point same object as a
b=a[:]         b will point new object which is a copy of a
```
- string concatenation
```
first_name = "gudio"
last_name = "rosium"
full_name = first_name + " " + last_name
print(full_name)
```

## Notes 26/08/2026
- diff between mutable and immutable
- method = functions
- `string.method()` (eg. method can be upper , lower, etc. )
	- use of casefold
	- find will give -1 when (and difference between )


## Notes 02/09/2026
In Python 3, string comparison uses lexicographic (Unicode/ASCII) order, character by character:
- "aB" vs "Ab"
- First char: 'a' (97) vs 'A' (65) → 97 > 65 → 'a' > 'A'
- Result: True
'a' (lowercase) has a higher Unicode code point than 'A' (uppercase), so "aB" > "Ab" evaluates to True.

`Remember A=65 and a=97`

in bool **False** = None , 0 , "" and all else is `True`
in case of multi operator `not > and > or

- Dry Run Following
	- not 0 and 1 or None and ""
		- 1 and 1 or None and ""
		- 1 or None and ""
		- 1 or 0
		- 1 (True)
## Notes 04/09/2026


```
f-strings also provide a convenient way to control the number of decimal places.

```


Example:

```python
price = 99.5678

print(f"{price:.2f}")
```

Output:

```
99.57
```

Here:

```
:.2f
```

means:
```
- `f` → floating-point formatting
- `2` → show two digits after the decimal point
```

- separator in print
- 


## Notes 04/09/2026
- for loop
```python
for variable in iterable:
	#loop block
```
- where 
	- for :-
		- The keyword that starts the loop.
	- variable :- 
		- A temporary name you choose to represent the current item in the sequence.
	- in :- 
		- The keyword that connects your variable to the iterable.
	- iterable :- 
		- The collection or sequence you want to loop through (e.g., a list, string, dictionary, or range).
		- Working in own words
			- for loop will put index(start to end) of output or index(start to end) of any list , string , dictionary , etc.


## Notes 16/09/2026
* while loop

```python
initialization
while condition:
    #loop block
    update
```

* where
   * initialization :-
      * Sets the starting value of the variable used in the condition, done once before the loop begins.
   * while :-
      * The keyword that starts the loop.
   * condition :-
      * A boolean expression checked before every iteration; loop runs only while this is True.
   * update :-
      * Statement inside the loop block that changes the variable, moving it toward making the condition False (prevents infinite loop).
   * Working in own words
      * while loop keeps repeating the block as long as the condition stays true — you control start (initialization), continuation (condition), and progress (update) manually, unlike for loop where the iterable handles start-to-end automatically.



---
### Further link
- 
---
### References
- 