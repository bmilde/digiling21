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
is_published = True #or
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

.find("beginners")

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

Example: Test if word is contained in string. This example also uses the *in* operator, to test if a string is contained in another string.

```python

course = 'Python for beginners'

if 'beginners' in course:
    print('This is a beginners course')
elif 'advanced' in course:
    print('This is an advanced course')
```


## while loops

```python
i = 1
while i <=5:
    print(i) ->  print('*' * i)
    i = i+1
```

In a while loop, all intended statements are looped until the condition at the top returns False (= is no longer valid / True). You can read it as: do this while <some condition is still met>.

*break* can be used to abort a loop. *continue* can be used to break the current flow through the loop to restart the next iteration at the top of the loop.

A while loop can use an else: part as well, that is executed if no *break* occured.

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

Import statements: additional functionality can be loaded with the import statement. General syntax is import <package>. For example, to generate and print a random number between 0.0 (inclusive) and 1.0 (exclusive):

```python
import random
print(random.random())
```

exercise loops #2, simulate a car.

# 23. April

## for loops

Another very frequent loop in Python is the *for* loop. It is usually a more convient way to describe a loop over a sequence, try the following code:

```python
for num in [0, 1, 2, 3, 4]:
    print(num)
```

In the above example, a list is used to describe the sequence that is iterated on. In each run through the for loop, num changes according to the items in the list. You can store sequences of any Python types/objects in a list. You'll often encounter list with basic types such as intergers, strings or float. For example [0, 1, 2, 3, 4] is a list of 5 integer numbers.

Since iterating over a sequence of incrementing integers is a very common thing to do, Python has the short hand function range(...):

```python
range(5) # iterator that iterates over [0, 1, 2, 3, 4] 
range(5, 10) # iterator that iterates over [5, 6, 7, 8, 9]
range(5, 10, 2) # iterator that iterates over [5, 7, 9]
```

This means, to print the numbers 

```python
for num in range(5):
    print(num)
```

And from 0 to 99:

```python
for num in range(100):
    print(num)
```

*WIP* the following text is work in progress and not yet completed *WIP*

excerise prices: sum prices with a for loop:

```python
prices = [4.99, 12.0, 0.79, 19.99]
sum = 0.0

for ...

print("sum:",sum)
```

loops: nested for loops

```python
numbers = [5, 2, 5, 2, 2]

for x_count in numbers:
   print('*'*x_count)

   output = ''
```

excercise: replace '*'*x_count with a for loop

## lists

In the previous excercise, we encountered a list of floats. Lists can have elements of any type in Python. In particular and very relevant to this course, a list of strings can also be defined, for example:

```python
names = ['Sofia', 'Bob' , 'Eva', 'Adam' ]
```

This defines a list of four names. Try these:

```python
print(names)
print(names[2])
print(names[2:])
```

Similarly to slicing in a string, the [] operator can also be applied to lists. Indexing starts at 0 and counts the elements of the list:

```python
names = ['Sofia', 'Bob' , 'Eva', 'Adam' ]
            0       1       2       3
```

Lists can also be nested, i.e. a list can also contain other lists:

```python
names = [['Sofia', 'Eva'], ['Bob', 'Adam']]
```

Try these:

```python
print(names[0])
print(names[1])
```

Items can be inserted, removed and appended to a list:

```python
names = ['Sofia', 'Bob' , 'Eva', 'Adam' ]

names.insert(0, 'Nina')
print(names)
names.remove(0)
print(names)
names.append('John')
print(names)
```

Try these list methods, what do they do?

.pop()

.clear()

.index("Bob")

The *in* operator can also be used on list items, to check if a particular element is contained in a list, e.g.

```python
if 'Bob' in names:
    print('Bob is in the list of names!')
```

Lists can also be sorted, reversed and copied:

```python
names.sort()
print(names)
names.reverse()
print(names)
names_copy = names.copy()
print(names_copy)
```

A string can also be split by white space into a list, try this:

```python
test = 'This is a test'.split()
print(test)
```

Closer look: lists exercise

Write a program to remove repeating entries from this list:

```python
numbers = [4,5,5,3,3,4]
```

## tuples

Tuples are like lists, but the elements can't be changed after the tuple was created. Tuples are *immutable* in Python, while lists are *mutable*. A tuple is created with () instead of [].

```python
coordinates = (4, 3)
```

## unpacking

```python
x = coordinates[0]
y = coordinates[1]

x, y = coordinates

print(x*y)
```

## Dictionaries (dicts)

Dictionaries store key/value pairs in Python. Searching for a key in a dictionary is very efficient in Python and fast even if a dictionary is really big. For example, to create a phonetic dictionary in Python, the keys would be words and the values the IPA sequence for a word. Another example would be telephone book, where the names are

```python
telephone_book = {'Adam':'+49 48264869', 'Eva':'+49 4738384', 'Bob':'+49 685685685', }
```

Dictionaties are initialized with {} containing a list of key:value pairs. Additional entries can also be added later on:

```python
telephone_book['Alice'] = '+49 567373577'
```

To retrieve the value for the key 'Bob', you can do:

name = 'Bob'
print(telephone_book[name])

#or

print(telephone_book['Bob'])

The *in* operator can be used to check if a key is in a dictionary:

```python
if 'Bob' in telephone_book:
    print('Bob is in the telephone book!', telephone_book['Bob'])
else:
    print('Bob is not in the telephone book :(', telephone_book['Bob'])
```

A dictionary can also be empty at first, with key/values added later on:

```python
empty_dictionary = {}
```

## dicts exercise 1

Write a digit converter, that translates a sequence of digits into words, for example: 02585 -> "zero two five eight five"

# 30. April

## functions

```python
def unique(input_list):
    new_list = []
    for item in input_list:
        if item not in new_list:
            new_list.append(item)
    return new_list
    
print(unique([5,5,5,42,5,3,42]))
```

```python
def add(num1, num2):
    return num1+num2
    
print(add(4,6))
```

The def statement can be used to declare your own functions. This encapsulates functionality, that you can later reuse.

Syntax is:

```python
def functioname():
```

or 

```python
def functioname(argument1):
```

or

```python
def functioname(argument1, argument2):
```

Any code inside the function is indented one level. The return keyword is used to end the function call and return one or more objects. 

```python
    return elem
```

After your function is declared, you can use your function by calling it with the name you have given it, followed by () and potential arguments:

```python
functioname(argument1, argument2)
```

# dicts + functions exercise 2

Write a smiley converter, that converts :) and :(, :D in a text into emoticons: 😞 😃 😛 

This is similar to dicts exercise 1. However, this time write a new function that takes a string as input and produces the new string with the replacements as output. Then call your function to test it and print some example results.

# Working with files

In python, we use the following syntax to open a text file and read it line by line:

```python
with open('names.txt') as names:
    for line in names:
        print(line)
```

The open() function is builtin, similar to print input etc. The second argument to open is by default 'r' for read, so the above is identical to:


```python
with open('names.txt', 'r') as names:
    for line in names:
        print(line)
```

Text files can also be written to:

```python
with open('numbers.txt', 'w') as numbers_out:
    for number in range(10):
        numbers_out.write(str(number) + '\n') # The '\n' character makes a new line. While print automatically appends a new line, .write() does not do this.
```

```python
with open('names.txt') as names, open('names_upper.txt','w') as names_out:
    for line in names:
        namesout.write(line.upper())
```

# dicts exercise 3

Load the names dataset from http://shapecatcher.com/names.zip

We want to analyzse the distribution of characters at the end of English female and male names.

You can start from this template, that reads the two files female.txt and male.txt line by line (and just prints the content):

```python
def analyse(names_file):
    with open(names_file) as names_female:
        for line in names_female:
            if line[-1] == '\n':
                line = line[:-1]
            name = line
            print(name)

analyse("names/female.txt")
analyse("names/male.txt")
```

# May 6

# Names solution 1

```python
def get_second_element(item):
    return item[1]

def analyse(names_file):
    corp = {}
    with open(names_file) as names:
        for line in names:
            line = line.strip() # -> strips \n
            last_character = line[-1]
            
            if last_character not in corp:
                corp[last_character] = 1
            else:
                corp[last_character] += 1

    corp_sorted = dict(sorted(corp.items(),
                              reverse=True,
                              key=get_second_element))

    print(corp_sorted)
```

# Default dicts

Default dicts are like regular dictionaries, but every key that is not available is automatically generated and initialized (to zero for int):

```python
from collections import defaultdict

dd = defaultdict(int)

print(dd["test"])

```

# Names solution 2

```python
from collections import defaultdict

def get_second_element(item):
    return item[1]

def analyse(names_file):
    corp = defaultdict(int)
    with open(names_file) as names:
        for line in names:
            line = line.strip() # -> strips \n
            last_character = line[-1]
            corp[last_character] += 1

    corp_sorted = dict(sorted(corp.items(),
                              reverse=True,
                              key=get_second_element))

    print(corp_sorted)

print('female names:')
analyse("names/female.txt")

print('male names:')
analyse("names/male.txt")
```

# Shakespeare corpus

Load the shakespeare dataset from http://shapecatcher.com/shakespeare.zip

We will work with Spacy, a module for various NLP tasks:

```python
import spacy
  
spacy.cli.download("en_core_web_sm")

nlp = spacy.load("en_core_web_sm")

with open("shakespeare.txt") as input_file:
  text = input_file.read()

shakespeare_corpus = nlp(text)

for token in shakespeare_corpus:
    print(token)
```

Excercise: What are the most frequent words in Shakespears complete works?

# May 21
              
## Plotting with matplotlib/pyplot
              
Install matplotlib first, you should be able to write:
              
```python
import   matplotlib           
```     
              
In PyCharm and it should automatically suggest to install matplotlib. In this course we'll use a subpackage of matplotlib called *pyplot*, that provides an easy interface to the plotting functionailty in matplotlib.
              
Examples to create line plots:
              
```python
import matplotlib.pyplot as plt

x_data = [4., 7., 9., 15.7]
y_data = [x*x for x in x_data]

x_data2 = [x/2.5 for x in x_data]

plt.title("My first plot")

plt.plot(x_data, y_data, 'o-', color='green')
plt.plot(x_data2, y_data, 'x-', color='red')

plt.xlabel("number of tries")
plt.ylabel("seconds")

plt.legend(["Experiment 1","Experiment 2"], loc="lower right")           
```              

Histogram plot example using 1000 artifically generated datapoints, normally distributed:

```python
import numpy as np             
import matplotlib.pyplot as plt         

# generate a random list with normally distributed datapoints, mean of 100 and sigma of 15              
mu = 100.
sigma = 15.
x = mu + sigma * np.random.randn(1000)
              
print(x) # random numbers centered around 100
              
# plot a histogram with 100 bars              
plt.hist(x, 100)

plt.show()
```

Example plotting frequency/rank of words in a vocabulary dictionary:            
              
```python
# this would usually be generated from real data, needs to be sorted!              
vocabulary = {'the':523, 'cat':235, 'dog':132}

# generate a list with 1,2,3 for the ranks in the x axis              
x_data = list(range(1,4))
              
# retrieve the frequency of words from the dictionary              
y_data = [vocabulary[word] for word in vocabulary]

# check that data looks correct:              
print(x_data)
print(y_data)

# plot it as a green line (g) with oval data markers (o) and a line connecting the data points (-)
plt.plot(x_data, y_data, 'go-')
              
# manually set limits on the axis:
plt.xlim(1,10)              

# show the plot the user              
plt.show()
```              

# 27 May              

We will start with a new corpus, a dataset of movie reviews from IMDB. Download it here https://shapecatcher.com/IMDBdata.zip 
              
This dataset contains reviews + sentiment (positive / negative). We want to find out which words (adjectives) are frequently used in positive reviews and which ones are used in negative reviews. We would also like to see if there are different patterns in how long (number of words) a negative or positive reviews is and would like to plot the lengths in a histogram plot to learn more about this.
              
This new dataset is in csv format. Csv stand for comma separated values and is a common format for tabular data. There is also a nice Python module to read csv files:
              
```python
import csv

with open('IMDB Dataset.csv', newline='') as csvfile:
    reader = csv.reader(csvfile)
    for row in reader:
        print('text:',row[0])
        print('sentiment:',row[1])    
```              
  
This, we try to structure our code into functions:
       
```python              
import csv

def process_csv():
    with open('IMDB Dataset.csv', newline='') as csvfile:
        reader = csv.reader(csvfile)
        for row in reader:
            print('text:',row[0])
            print('sentiment:',row[1])

if __name__ == "__main__":
    process_csv()
```
              
Typically a larger Python program has multiple functions, potentially distributed accross many files. The main file will have a statement (if __name__ == "__main__") at the end, this is the main entry point of the program.              
