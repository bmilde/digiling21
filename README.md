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
```python

The print functions and others are always available, they are built in functions of the python interpreter.

The input function can be used to request user input on the command line:

input('What is your name? ') # the () <- are executing the function. Parameters are inside the () and can be seperated by a , 

name = input('What is your name? ')
print('Hi ')

print('Hi ' + name)



type conversion

birth_year = input('Birth year:')
age = 2021 - birth_year


--> error

birth_year = '1987'

builtin functions: type conversion

print(type(birth_year))

course = ‘Python for beginners’

course = ‘Python's ...’

text = ''' ''''



course = ‘Python for beginners’
          01234

print(course[0])


print(course[-1])


print(course[0:3])

'Pyt'

print(course[1:])


print(course[:5])

first = 'Alan'
last = 'Smithee'
address = 'ABC street 1'

msg = 'Hi ' + first + ' ' + last + ', ' + 'your package has been sent to: ' + address

print(msg)

msg = f'hi {first} {last}, your package has been sent to: {address}'

print(msg)

string methods

course = 'Python for beginners'

len(course)

.find()
.upper()
.lower()

functions vs. methods

print(course.upper())

print(course.find('o'))

print(course.find('O'))

print(course.find('beginners'))

in

.replace('beginners', 'absolute beginners')

.title()

import math
math.log()


celcius = 

if celcius > 26.0:

elif

else


If statements - excercise: names , excercise: convert

while loops

i = 1
while i <=5:
    print(i) ->  print('*' * i)
    i = i+1

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
