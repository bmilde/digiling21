# digiling21

Install Python from Python.org, choose an installer based on your OS.

We use [PyCharm](https://www.jetbrains.com/pycharm/) in the course. It's a great and free source code editor for Python that makes your life easier. Similar to a word processor for text it has integrated spell checking and can help you solve programming errors while you type.

# 16. April

A Python script is interpreted from top to bottom. The Python interpreter reads your source code and translates it on the fly into machine code that your computer understands. There is no compilation step, since the code is interpreted at runtime.

Open PyCharm, make a new project (uncheck the checkbox that says something about main.py). Now add a new Python file by right clicking in the project tree on the left side and chose new Python file. You can give it any name you want, by convention the Python script that should be executed in a project is often named main.py .

## Variables

```python
greeting = 'hello world'
greeting = 'how are you?'
print(greeting)
```

store simple values in memory:

```python
count = 7
rating = 4.9
name = 'Benjamin'
is_published = True or
is_published = False 
```

True / False: boolean values. Case sensisive! true / false will give an error. The 4 most basic types in Python are:

Integers (int): 42

Floating numbers (float): 4.67869

Strings (str): 'test'

Boolean (bool): True or False

They are used depending on the information that you need to store in memory. Its also possible to store more complex objects in variables and we'll discuss this in the future.

Excercise:

We check in a patient named Alan Smithee. 
He's 30 years old and is a new patient.

```python
name = 'Alan Smithee'
# or
name = "Alan Smithee"
age = 30
is_new_patient = True
```

Strings store text in Python, they are declared with either ' or ". The text is placed inside '...' or "...".

## Print functions

```python
print('Hello World!')
```

The print functions and others are always available, they are built in functions of the python interpreter.

The input function can be used to request user input on the command line:

```python
input('What is your name? ') # the () <- are executing the function. Parameters are inside the () and can be seperated by a , 
```

This program asks the users name and says hi <name>!
          
```python
name = input('What is your name? ')
print('Hi ' + name + '!')
```

Strings can be concatenated with +

## Type conversion

```python
birth_year = input('Birth year:')
age = 2021 - birth_year
print('Your age is:' + age)
```

--> this will results in a type_error

Because internally, Python will store the birth year as:

```python
birth_year = '1987'
```

A variable can be of any type. Not all operations work on all types, in particular combining two different types may be ambigious. To solve this issue we can use builtin functions that concert a particular type (type conversion) and explicity tell Python how to handle a calculation:

```python
int('1987') # -> 1987
```

There are more type functions:

```python
int('7')  # -> 7
float('5.9') # -> 5.9
str(5.9)  # -> "5.9"
```

You can check that the type of birth year is string, by using the type function:

```python
print(type(birth_year))
```

The complete program, that calculates the age correctly with type conversions:

```python
birth_year = input('Birth year:')
age = 2021 - int(birth_year)
print('Your age is:' + str(age))
```

# Strings

```python
course = 'Python for beginners'
course = 'Python's ...' #-> error, python doesn
course = "Python's ..." #-> correct way to store a string containing a '
course = 'Python\'s ...' #-> alternative, use \ to backspace the '
```

Triple quotes can be used for very long lines of text:

```python
text = '''Very long line of text
that can also span
multiple lines'''
```

## String indexing

```python
course = ‘Python for beginners’
          01234
```

The slicing operator [] can be used to 'slice' individual characters from a string, or slice a sequence of characters from a string. Each character in a string has an index, starting from 0.

```python
print(course[0])
```

-> 'P'

```python
print(course[-1])
```

Slice the last character with -1 (counts backwards from the end).
-> 's'

```python
print(course[0:3])
```

Use [x:y] to select a range of characters from x to y:

-> 'Pyt'

```python
print(course[1:])
```

Or [x:] to select from x till the end.

```python
print(course[:5])
```

Or [:y] to select from the beginning to y.

```python
first = 'Alan'
last = 'Smithee'
address = 'ABC street 1'

msg = 'Hi ' + first + ' ' + last + ', ' + 'your package has been sent to: ' + address

print(msg)
```

String formatting is more convienent, when you have to combine many strings. You can copy content from variables into the string using {}:

```python
msg = f'hi {first} {last}, your package has been sent to: {address}'
print(msg)
```

## String methods

```python
course = 'Python for beginners'
```

Returns the length of a string:

```python
len(course)
```

Try these methods:

.find()

.upper()

.lower()

functions vs. methods: strings and other object have methods that are particular to the the object. For example a string has methods that over objects don't have in Python. Such methods are called with the variable name (or string directly), follow by a . and the method name, then (). Or (arg1), (arg1, arg2) if there are any arguments. See these examples:

```python
course = 'Python for beginners'
print(course.upper())
print(course.lower())
print(course.title())
print(course.find('o'))
print(course.find('O'))
print(course.find('beginners'))
```

The replace function is useful to replace any occurence of a string with another:

```python
.replace('beginners', 'absolute beginners')
```

## If statements

if statements can be used to conditionally execute another block of python code. The condtional code is intended by one level. The geneneral synytax is:

```python
if <condition>:
    <conditional block of code>
    ...
elif <condition2>:
    <conditional block of code>
    ...
elif <condition3>:
    <conditional block of code>
    ...
else:
    <conditional block of code, if none of the above was True>
```

There can be multiple optional else if (elif) statements. They will only execute the conditioal code if none of the previous condition were met and the current condition is true. Once one if or elif executes the conditional block, none of the other statements will be checked. There can only be one optional else statement, that will exceute if *none* of the if or elif conditions was met.

Code example, depending on the temperature, print a different message to the user:

```python
if celsius < 0:
    print("It's freezing!!! :( You need a jacket. A warm one.")
elif celsius < 22.0:
    print(':(')
else:
    print('You only need a t-shirt')
    print(':)')
```

If statements - excercise: convert

Excercise: ask the user

Solution:

```python
command = input('Convert meter to feet (mtf)'
                ' or feet to meters (ftm)?'
                ' Please answer: ftm or mtf! ')

if command == 'ftm':
    feet = input('Please input feet:')
    meter = float(feet) / 3.28408
    print('result in meters is:', meter)
elif command == 'mtf':
    meter = input('Please input meters:')
    feet = float(meter) * 3.28408
    print('result in feet is:', feet)
else:
    print('Not a valid command!')
```

## while loops

```python
i = 1
while i <=5:
    print(i) ->  print('*' * i)
    i = i+1
```

while

else:

*break* can be used to abort a loop. *continue* can be used to break the current flow through the loop.



exercise loops #1
Guessing game exercise: (while loop with break statement)

Solution:

```python
import random

random_num = random.random()
random_num *= 10.0
secret = int(random_num)

# keep track if the user won or lost
has_lost = True

# Give the user 3 tries to guess the secret
while counter < 3:
    counter += 1
    secret_test = input("What is the secret number (0-9)? ")
    if secret == int(secret_test):
        print("Wow yes thats true! You have won")
        has_lost = False
        break
    print("Remaining tries:", 3-counter)

if has_lost:
    print("Guessed wrong 3 times, you lost.")
```

Import statements: additional functionality can be loaded with the import statement. General syntax is import <random>.

random.random()

exercise loops #2, simulate a car:

# 23. April

## for loops

```python
for num in [0, 1, 2, 3, 4]:
    print(num)
```

```python
range(5)
range(5, 10)
range(5, 10, 2)
```

```python
for num in range(5):
    print(num)
```

excerise prices


loops: nested for loops


numbers = [5, 2, 5, 2, 2]

for x_count in numbers:
   print('*'*x_count)

   output = ''
for count in range(x_count)_


names = ['Sofia', 'Bob' , 'Eva', 'Adam' ]

print(names)

print(names[2])

names[2:]



names = [['Sofia', 'Eva'], ['Bob', 'Adam']]

for row in names:



names = ['Sofia', 'Bob' , 'Eva', 'Adam' ]

names.insert(0, 'Nina')
names.remove

.pop())
.clear()
.index("Bob")

in operator

.sort()    (in place)
.reverse()

.copy()

Closer look: lists exercise: numbers = [4,5,5,3,3,4]


tuples - immutable

unpacking

coordinates = (4, 3)

x = coordinates[0]
y = coordinates[1]

x, y = coordinates

print(x*y)

dicts

exercise #1

digit converter

.split()

smiley converter

:)

with open():

grand exercise
