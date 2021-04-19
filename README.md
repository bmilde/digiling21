# digiling21

Install Python from Python.org

We use [PyCharm](https://www.jetbrains.com/pycharm/) in the course.

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

True / False: boolean values. Case sensisive!

(Its also possible to store more complex objects in variables and we'll discuss this in the future)

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
name = input('What is your name? ')
print('Hi ' + name + '!')

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

A variables can be 

To solve this issue we can use builtin functions that concert a particular type (type conversion).

You can check that the type of birth year is string, by using the type function:

```python
print(type(birth_year))
```

```python
birth_year = input('Birth year:')
age = 2021 - birth_year
print('Your age is:' + age)
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

celcius = 

if celcius > 26.0:

elif

else


If statements - excercise: names , excercise: convert

while loops

```python
i = 1
while i <=5:
    print(i) ->  print('*' * i)
    i = i+1
```

while

else:


exercise loops #1
Guessing game: (break statement)
random.random()

exercise loops #2, car

> help
> start
> stop
> exit

for num in [0, 1, 2, 3, 4]:
    print(num)

range(5)
range(5, 10)
range(5, 10, 2)

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
