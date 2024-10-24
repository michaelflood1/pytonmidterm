# pyton and pyton accessories

What is the behaviour of the following program?

```python
#What is the behaviour of the following program?

num = 25
s = 'There are ' + num + ' students in the class.'
print(s)
#raises exception. concating str with int


#What is the behaviour of the following program?
with open("file.txt", "w") as fp:
  fp.write("Hello!")

  #Which data structure would you choose to store a collection of users associated with their phone numbers, so that it is easy to find someone's name when you know their number?

  dict

  #Look at the following piece of code:

def add(a, b):
  return a + b

add([1, 2, 3], [4, 5, 6])

#TRUE: raises an exception; FALSE: no exception
False

#How do you add an element to an existing set `my_var`?
my_var.add(element)


#output is?
a = 10
def hello():
  a = 23 #scoped to function

hello()
print(a)

#Select the pieces of code that will sort the list `my_list` in decreasing order, and keep the result in `my_list`:
my_list = sorted(my_list, reverse=True)
my_list.sort(reverse=True)


#How many return values does the "my_function" have?
def my_function(arg1, arg2, arg3="quiz"):
  return "hello", "goodbye"
  #1

def my_function(arg1, arg2, arg3="quiz"):
  return "hello"
  #3



```

## pyton basics

Python is strongly but dyanmically typed language
the correct type of a variable can only be known at runtime
DO NOT USE PLAY BUTTON TO RUN CODE UNLESS YOU HAVE A HUGE GIGABRAIN
run code by

    python script.py
    python3 script.py

### variables
declare assign set a variable by

    my_variable = "something"

! global variables are bad use functions args and return values
a variable assigned inside a function is scoped to the function
use meaningful names of at least 4 characters
all variables have a type.

    type(my_variable)

#### naming

    variables = snakecase = my_great_variable
    constants should be uppercase i.e NUMBER_OF_ATTEMPS = 2

### numeric types
number Transform (=cast) one type to the other

    round_number = 20
    float_number = 42.4
    string_number = "100"
    int(float_number) # 42
    int(string_number) # 100 (not '100' !)
    float(round_number) # 20.0

due to binary  representation of floating point rounding errors can happen

    0.1+0.1+0.1 !=0.3

types int,float,complex
- can do arithmetics + - * /
- interger division and modulo 13 // 3 == 4 14 % 3 == 2 (14 = 4*3 + 2)

complex math is done by import math, math.sqrt, math.pow, math.log

### booleans (True or false only)
None is a built in value and is neither True nor false is the only python "Nonetype" represents the absence of value

    == equality
    != inequality
    = variable assignment
    not (a and b) == not a or not b
    not a and not b == neither a nor b

### conditions
if
```python

if condition:
    #runs if condition True
elif another:
    # runs if condition it False and another is True
else:
    #runs if condition is false and another false

# one liner if
can_drink = True if age > 19 else False

#while
count = 0
while count < 5:
    print(count)
    count += 1  # Increment to avoid infinite loop

count = 0
while count < 3:
    print(count)
    count += 1
else:
    print("Finished!")

# one line while
count = 0; 
while count < 3: print(count); count += 1

#for 
for i in range(5):
    print(i)

fruits = ['apple', 'banana', 'cherry']
for fruit in fruits:
    print(fruit)

for i in range(3):
    print(i)
else:
    print("Loop completed!")

[print(i) for i in range(3)]

```

### collections
list ordered mutable
 tuples ordered not mutable
 sets not ordered mutable
 dict key: value pairs similar to hashmaps

 ### lists/tuples
 list is a collection of ordered elemnts (sequence)
 list type = list
 tuple type = tuple 
 once defines you cant change tuple values

 ```python

  Lists
my_list = [4, 5, 6]
another_list = list(1, 2, 3) # Another way to define a list
my_list.append("something") # Add an element at the end of the list
my_list[0] # Access an element by its position in the list
(starts at 0)
my_list[2] = "hello" # Change values
new_list = my_list + another_list # Concatenate lists with +
my_list.extend(another_list) # Similar to above, but modifies in place!
# Tuples
my_tuple = (1, 2, 3)
another_tuple = tuple("hello", "world")
my_tuple[1] # like lists
my_tuple[0] = 0 # ERROR! Tuples are immutabl
```

### sets

    my_set = set(1,1,1,2,3) # Sets do not allow duplicates and the stored values are 1 2 3
    set[0] = #error sets are not ordered or indexed


### iteration lists

    my_list = [1,2,3,4]
    for value in my_list:
        print("value:", value)

avoid iterating with indexes i.e

    for idx in range(len(my_list)):
        print("value:", my_list[idx])

    USEFUL
    my_list = [1, 2, 3, 4, "hello"]
    len(my_list) # Number of elements in the list
    5 in my_list # False: 5 is not in the list
    "hello" in my_list # True

### dictionaries
type is dict
useful data type maps keys to values
not ordered can not sort
dictionary[my_key] access the element at key my_key in dictionary
dict methods keys() values() items() update()

    my_dict = {"hello": "goodbye", 1234: "sunshine"}
    my_dict = dict((("hello", "goodbye"), (1234, "sunshine")))
    my_dict["hello"] # 'goodbye'
    my_dict["test"] = "something" # Add values to the dict
    my_dict[1234] = "rain" # Keys are unique
    my_dict.keys() # List of keys
    my_dict.values() # List of values
    my_dict.items() # List of key/value pair

### iteration dictionaries

    for key,value in my_dict.items():
        print("key:",key, " - Value:", value)
    or
    for key in my_dict.keys():
        print("key:", key, " - Value:", my_dict[key])
    or loop off value
    for value in my_dict.values():
        print("Value:", value)

### Strings
type str define with '', "". """""".
usefule methods split join upper lower isnumeric isalpha isalnum
f strings for printing and other whatnots to keep variables inside

    f"Hello {name}, nice to meet you!

    my_string = "hello world"
    my_string[0] # 'h'
    my_string[0] = "H" # ERROR! Strings are immutable
    my_string.upper() # 'HELLO WORLD'
    my_string.split(' ') # ['hello', 'world']
    ' '.join(['hello', 'world']) # 'hello world'
    'HELLO WORLD'.lower() # 'hello world'
    'world' in my_string # True

### iteration strings

    for letter in my_string:
        print(letter)

string to number conversion

    my_string = "12345"
    int(my_string)

    my_string = "sadasd"
        CAN NOT MOVE LETTERS INTO INT

## fUNCITONS
Functions have parameters/recieve arguments
return a value (of any type)

    def register_student(student_id, name, international=False, scholarship=False):
    # Do something with the parameters
    return True

The function register_student has 4 args (parameters)
student_id and name are postional arguments meaning the need to be entered in order
internation and scholarship are keyword arguments, optional to input as they have preset values. can be returned in any order

all functions return "something" using the return statement
if no return statement the funciton returns None (absence of value)

one value is returned but can be a collection (list dict set tuple etc)

### exceptions
errors in code raise exceptions
can be manually raised by devs
you can catch exceptions using try/except

    try:
        value = 10 / int(input("Enter a divisor: "))
    except ValueError:
        print("Input must be a number!")
    except ZeroDivisionError:
        print("Cannot divide by zero!")

DO NOT LEAVE EMPTY statements i.e

    try:
        result =1/0
    except:
        pass

is bad
arithmeticerror
attributeerro
importerror
indexerror
keyerror
namerror
typerror
valueerror
filenotfounderror

### files and paths
file type doesnt matter a file is a file
it is common to distinguish binary files and text files
other useful file methods 
file.tell() returns current position of pointer
file.seek(offset, whence) move file to specific position offset = bytes to move when 0 start 1 current 2 end
Relative paths: Path("folder/example.txt")
absolute paths Path("/home/user/example.txt")
Path.cwd = current working directory
"path.exists() "path".is_file() .is_dir() Path("filename").touch() makes empty  file .mkdir makes folder
for file in Path(".").iterdir():



    from pathlib import Path

    if Path("example.txt").exists():
        print("File exists!")
    else:
        print("File not found.")


    with open("my_file.txt", "r") as fp:
        data = fp.read
    with open("example.txt", "r") as file:
        for line in file:
             print(line, end='')
    with open("example.txt", "r") as file:
            lines = file.readlines()  # Returns a list of lines
                 print(lines)
    with open("example.txt", "w") as file:
        file.write("This will overwrite the file content.\n")
    with open("example.txt", "a") as file:
         file.write("Adding a new line.\n")
     p = Path("folder") / "subfolder" / "file.txt"
            print(p)  # folder/subfolder/file.txt
    p = Path("example.txt")
         if p.exists():
             p.unlink()  # Delete the file
     p = Path("empty_folder")
        if p.exists():
            p.rmdir()  # Remove the directory if it's empty
    p1 = Path("example.txt")
    p2 = Path("./example.txt")
        print(p1 == p2)  # True if both refer to the same path

### modules/import
code is executed on import

    import logic.computer.aimbot as bot
    bot.shoot()

     Contents of my_print.py
    MY_MESSAGE = "Hello!"
    def my_print_func(text):
    print(MY_MESSAGE)
    print(text)

    # Contents of main.py
    import my_print
    def main():
    my_print.my_print_func("Example.")
    print(my_print.MY_MESSAGE)

use import to import another piece of code
lookup order = standard lib
modules to know 
os 
sys - argv 
 math 
 random .random() returns random float in range. random.randint(a,b) returns random integer between a,b .shuffle(x) shuffles sequence
  csv 
  pathlib
   json
    import math
    or
    from math import sqrt

### debugging
use the debugger, print, read the error messages, run cde every change, do not make multiple changes at once, one problem at a time

### docstring and documentation
docstrings
- documenting module classes functions
- syntax = """ text """ or ''' text '''
- accesed via __doc__
- located at beginning of class module or function

inline comments
- explains lines of code
- syntax # text
- not programmatically accessible
- anywhere in code

### init.py and packages
a python package is a folder with init.oy in it
marks directory as a python package allowing you to import from that dir
any code written in ___init___.py will be executed when imported
can define what is available using the __all__ list
python -m my_package.my_module - preferred way
python my_package/my_module.py 


    my_package/
        __init__.py # 1 per dir
        module1.py
        module2.py
        "subpackag"
            __init__.py #hypothetical subpackage to show u need new init per dir


    # __init__.py
        # can import other modules into init py . before module indicates relative import (look in same package dir)
    from .module1 import My_Class
    from .module2 import my_function
    __all__ = ["My_Class", "my_function"]

     # module1.py
        class MyClass:
             def greet(self):
                  return "Hello from MyClass!"
    #module2.py
        def my_function():
            return "Hello from my_function!"

    # main.py
    from my_package import My_Class, my_function
    obj = My_Class()
    def main():
        print(obj.greet()) #outputs Hello from MyClass
        print(my_function())  #outputs hello from my_fnction
    if __name__ == "__main__":
    main()
    
### enviorenment set up
py - m venv venv
this runs the venv module creates a folder called venv
./venv/Scripts/activate.bat in windows command line
.\venv\Scripts\activate.ps1 (Windows Powershell)
source venv/bin/activate (Linux/macOS)
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

when venv is active you can run python programs using just python
use pip install pytest to get pytest library
run program 

    python my_file.py arg arg arg




    
### pytest unit testing
automated , makes sure erthing works, one button approach, do not validate how objexts interact, operate at lowest level possible(validate basic elements)
fast easy help with reading code TEST DRIVEN DEVELOPMENT TDD =write tests before / same time as program
untested = broken
unittest is testing framework provided by python
pytest is better than unittest
pytest is a pythong Package
pip install pytest
running pytest

    test_*.py #runs all that match a pattern
    *_test.py # same

    or just type pytest

tests are functions/methods whose name start with test_

    def test_thingy():
        pass
    or
    class TestSomething
        def test_thing2(self): 
            pass

test examples

    def test_add_values():
        result = add_values(2,3)
        assert result == 5

    ## exception checks
    def test_add_values_invalid():
        with pytest.raises(TypeError):
            result = add_values([1],[2])

Unit tests
- helps developers understand the code
- developers can find bugs more easily using unit tests
- unit tests are fast to run (typically a few seconds)
- aim for 80 percent code coverage
### mocks fixtures patching
#### fixtures
common to create objects and run dif methods to check behaviours
each test function tests a specific feature of the classs
you may end up creating the same object over and over in all of your tests functions
fixtures are meant to solve the problem they allow u to define objects that can be reused in dif test functions

    import pytest
    @pytest.fixture
    def bank():
        bank = Bank("BCIT Bank")
        return bank
    def test_bank(bank):
        assert bank.name == "BCIT Bank"

defined by decorator @pytest.fixture
regular funcitons
value returned is the fixture that you use in test functions
to make test use a fixture use its name as argument in test function

### mocks and patching

how to test child class without testing parent
Unit tests should only test a specific class or function, and not the dependencies of that code.
There are some elements that you do not need to isolate: you don't have to test if super() works, or if a list
is really a list, for instance.

monkeypatch fixture is available by default in Pytest
you can use it in test functions
similar to setattr

```py
#problem balance
def test_bank_customer_total_balance():
tim = BankCustomer("Tim")
account = BankAccount("Test", 1000)
tim.add_account(account)
assert tim.total_balance == 1000
#fix
def test_bank_customer_total_balance(monkeypatch):
tim = BankCustomer("Tim")
account = BankAccount("Test", 1000)
tim.add_account(account)
monkeypatch.setattr(BankAccount, "balance", 1000) #fix for test
assert tim.total_balance == 1000
```
we can now pass the test without fixing issue in the code
useful and efficient for simple issues sometimes we need stronger methodds for that we use mocks

### input method

    @patch("builtins.input", side_effect=["abc", "def"])
    def test_example(mock_input):
        value1 = input()
        value2 = input()
        assert value1 == "abc"
        assert value2 == "def
@patch patches the builtin input method
replaces it with a mock (mock_input)
this mock has a side affect it returns abd first time it is called and def the second time
mock input makes the input method non interactive and predictable

### open function
common method
does not depend on local files whose content you dont control
unit test will patch open to control the content on which the program operates
can be complicated to create a mock object every time because open is a standalone function
can also be used as with open
python comes with mock_open
use in combo with patch
```py
from unittest.mock import mock_open, patch
FILE_CONTENTS="line1\nline2\nline3\n"
@patch("builtins.open", new_callable=mock_open, read_data=FILE_CONTENTS)
def test_open(mock_file):
with open("my_file.txt", "r") as fp:
data = [line.strip() for line in fp.readlines()]
assert data[0] == "line1"
assert data[1] == "line2"
```
### arg unpacking
There are situations where a function can take a variable number of arguments.
Or situations where all arguments to a specific function call are already available in a dictionary or a list
Python has a mechanism for "unpacking" these arguments
Syntax is *args (for an iterable) and **kwargs (for a dictionary
Functions take positional and keyword arguments. The typical way to use them is:

    def func(pos1, pos2, pos3, keyword1="value1", keyword2=None, keyword3=42)
    pass
    pos1 , pos2 and pos3 are positional arguments.

they are required.
you don't have to provide their names when calling the function.
func(1, "b", None) is a valid call.
keyword1 , keyword2 and keyword3 are keyword arguments.
they are not required.
if not provided, they take default values.
Positional arguments always come before keyword arguments.
*args is a list of positional arguments.
**kwargs is a dictionary of keyword/value arguments/parameters
```py
    def func(*args):
    print(args)
    func("yes", 2) # prints ["yes", 2]

    def func(**kwargs):
    print(kwargs)
    func(example="yes", value=2) # prints {"example": "yes", "value": 2}

    my_list = ["yes", 2]
    my_dict = {"example": "yes", "value": 2}
    func(*my_list) # equivalent to func("yes", 2)
    func(**my_dict) # equivalent to func(example="yes", value=2)
    func("example", *my_list, keyword1="value1", **my_dict)
    kwargs = {}
    if difficulty in ("easy", "medium", "hard"):
        kwargs["difficulty"] = difficulty
    if category in get_categories():
        kwargs["category"] = category
    if number.isdigit():
      kwargs["number"] = int(number)
         get_questions(**kwargs)
```

### coverage
uses coverage library
pip install pytest-cov
module =>  pytest --cov=add
package ->  pytest --cov=.
for an html report=> pytest --cov=. --cov-report=html

### object oriented programming
class = defines a general category (book car)
object or instance is a thing created out of a class
attributes are values for specific object
methods are behaviours or capabilities of a class
state is the current values of attribues of an object

book = class harry potter = instance of book
### modelization
how we describe an object
bank = account money id number
### encapsulation(and visibility)
state of an object should only be changed by object itself
use methods to alter state instead of changing attribute
_"attribute" means private
private means only object changes it
using private attributes and methods to change state is called encapsulation
### abstraction
the implementation of the behaviours of the object is the responsibility of the class
other objects should not depend upon private attributes or methods
only should use public inteerface of class (non private methods and attributes)

### class syntax
class MyClassName:
    def __init__(self, attr,attr,attr)
        self.attr = ""
        self.attr = ""
        self.attr = ""

        class Student:
    def __init__(self, name, student_number):
        if not name or type(name) is not str:
                raise AttributeError("Name cannot be empty!")
            self.name = name
            self.student_number = student_number
            self.program = "CIT"
            def display(self):
            print(f"{self.name}, {self.student_number} - {self.program})
            john = Student("John Doe", "A01234567")
            john.display()
            bob = Student("Bobby", "A4432890")
            bob.display()

### self
all funcs defined in a class are methods
they recieve implicit parameter self which represence the current instance
allows encapsulation. each instance has its own version of the class attributes
never use self outside of class block

john.display() calls the method display on the object john .
In the display method, self is equal to john !

bob.display() calls the method display on the object bob .
In the display method, self is now equal to bob 

### python PROPERTY
Python has a decorator which makes encapsulation and abstraction easier.
You can use the @property decorator on a method, and then it will behave as an attribute. This allows you to
implement getters very easily.

    Defining a Getter: Use the @property decorator to define a method that will be called when you access the attribute.
    Defining a Setter: Use the @<property_name>.setter decorator to define a method that will be called when you set the attribute.
    Defining a Deleter: Use the @<property_name>.deleter decorator to define a method that will be called when you delete the attribute.

```python
class Circle:
    def __init__(self, radius):
        self._radius = radius  # Use a private attribute

    @property
    def radius(self):
        """Getter for the radius property."""
        return self._radius

    @radius.setter
    def radius(self, value):
        """Setter for the radius property."""
        if value < 0:
            raise ValueError("Radius cannot be negative.")
        self._radius = value

    @property
    def area(self):
        """Calculate area based on the radius."""
        return 3.14159 * (self._radius ** 2)

# Using the Circle class
circle = Circle(5)
print(circle.radius)  # Output: 5
print(circle.area)    # Output: 78.53975

circle.radius = 10    # Set a new radius
print(circle.area)    # Output: 314.159

# circle.radius = -5  # This would raise ValueError
#or

class Student:
[...]
@property
def program(self):
return self.program_name
@program.setter
def program(self, value):
if value not in ("CIT", "CST", "BTech"):
raise ValueError("Invalid program name!")
self.program_name = value
john = Student("John Doe", "A01234567")
print(john.program) # Runs the getter method (@property)
john.program = "Btech" # Runs the setter method (@property.setter)
john.program = "something" # Raises an Exception! (in @property.setter)

```


### static methods vs class methods

You can define methods that are common to all objects of the same class.
Static methods do not get any reference to the class or object
Class methods receive a reference to the class when called directly from the class name
This reference is typically called cls
Use the @staticmethod decorator for static methods (no reference)
Use the @classmethod decorator for class methods (reference to the class)

```python
class Student:
[...]
@staticmethod
def check_program(value):
# This is a static method. It does not receive an implicit argument.
# It does not have access or know about the class / instance
return value in ("CIT", "CST", "BTech")
Student.check_program("CIT") # will return True
john = Student("John Doe", "A01234567")
john.check_program("CIT") # will also return True

class Employee:
    company_name = "Tech Solutions"  # Class variable

    def __init__(self, name, salary):
        self.name = name
        self.salary = salary

    @classmethod
    def get_company_name(cls):
        """Return the company name."""
        return cls.company_name

    @classmethod
    def from_string(cls, emp_string):
        """Create an Employee instance from a string."""
        name, salary = emp_string.split('-')
        return cls(name, float(salary))

class Vehicle:
    wheels = 0  # Class variable

    def __init__(self, name):
        self.name = name

    @classmethod
    def set_wheels(cls, num_wheels):
        """Set the number of wheels for the class."""
        cls.wheels = num_wheels

    @classmethod
    def display_info(cls):
        """Display information about the class."""
        print(f"A {cls.__name__} has {cls.wheels} wheels.")

# Using the class methods
Vehicle.set_wheels(4)         # Set wheels for Vehicle class
Vehicle.display_info()        # Output: A Vehicle has 4 wheels.

# Subclassing
class Bicycle(Vehicle):
    pass

Bicycle.set_wheels(2)         # Set wheels for Bicycle class
Bicycle.display_info()        # Output: A Bicycle has 2 wheels.

# wheels is a class variable that can be accessed and modified by all instances of the class and its subclasses.
# This method sets the wheels variable for the class. When called on Vehicle, it sets Vehicle.wheels to 4. When called on Bicycle, it sets Bicycle.wheels to 2.


```

### class variables
Class variables are attributes that are common to all objects of the same class.
They are defined in class block, but outside any methods.
The previous example uses a class variable PROGRAMS
Class methods have access to class variables (but not instance variables)
Static methods do not have access to class variables, nor instance variables


### object relations
#### composition
a hand has 5 fingers we choose to use a composition relationship
think sql primary and foreign keys
fingers need hands hands dont need finger

```python
class Finger:
def flick(self):
print("Oh no.")
class Hand:
def __init__(self):
self._fingers = [Finger() for _ in range(5)]
def thumbs_up(self):
self._fingers[0].flick()


```
### aggregation
```python
class Driver:
def __init__(self, name):
self.name = name
class Car:
def __init__(self, driver):
self._driver = driver
#you can associate objects when creating the car
tim = Driver("Tim")
my_car = Car(tim)
my_car = Car(driver=tim) # Also works
```
in a composition relationship, composite objects are usually created when the main object is created (in the
__init__ method).
But it can also happen elsewhere ( def add_finger(self) ).
In aggregation relationships, there are usually methods in the public interface that allow to associate /
disassociate objects. They can sometimes be related to setters.

### inheritence
used when several objects are part of the same family
i.e 
vehicle
- brand str
- model str
- mileage float
- - - - - - - -
- driver() none
- stop(distance float) none

cars and suvs are different vehicles in the vehicle family but a distinct sub genre

```python
class Vehicle:
def drive(self):
pass
def stop(self, distance):
self._mileage += distance
class Car(Vehicle):
""" Car will automatically INHERIT from all attributes and methods of Vehicle """
pass
class SUV(Vehicle):
""" SUV will automatically INHERIT from all attributes and methods of Vehicle
But you can add attributes / methods too """
is_awd = True
```

all attributes and methods of the parent class are inherited by the child class
if an attribute is defined in the paren and child class, the child has precedence
you can travel up the inheritance tree using super()
this gives access to parent class and emthods

```python
class Car:
def __init__(self, model, brand, mileage=0):
self.brand = brand
self.model = model
self.mileage = mileage
class Chevrolet:
def __init__(self, model, mileage=0):
super().__init__(model, "Chevrolet", mileage)
```
inheritance limitations
should be used sparingly because it can get very complicated trying to understand your tree
can oft be replaced by composition
useful when used to create better versions of python types

```python
class Student:
def __init__(self, grades):
self._grades = Grades(grades)
@property
def does_pass(self):
return self._grades.average > 50
tim = Student(grades=[83, 90, 74, 23])
print(tim.does_pass) # True
```

### inheritance to create abstract classes

```py
class Animal:
def __init__(self, name):
self._name = name
def sound(self):
raise NotImplementedError("Abstract method for animal sound must be implemented by the child class")
def show_name(self):
print(self._name)
class Cow(Animal):
def sound(self):
return "MOO"
class Dog(Animal):
def sound(self):
return "WOOF"
```
animal can be cow or dog but both make sound 
animal() is just an object that coincidentally has a matching method available
isinstance(daisy, animal) returns True even though daisy is a cow due to inheritance tree

```py
from abc import abstractmethod, ABC
class Animal(ABC):
def __init__(self, name):
self._name = name
@abstractmethod
def sound(self):
pass
def show_name(self):
print(self._name)
```
### class diagrams
classes and objects have attributes and behaviours
uml diagrams
- name of class
- attributes and type
- methods wit parameters and type return value and type

objects do not exist by themselves they exist in context
hand has fingers
finger belongs to hand

```
# aggregation is line from driver to car line starting at car has outlined circle (not filled in) (can live seperately)
# composition is car to engine line from car has solid black circle at car

    +-----------------+
    |      Car        |
    +-----------------+
    | - model: str    |
    | - year: int     |
    | - engine: Engine|
    +-----------------+
    | + start()       |
    | + stop()        |
    | + get_info(): str |
    +-----------------+

            |
            |
            | contains
            |
            v
    +-----------------+
    |     Engine      |
    +-----------------+
    | - type: str     |
    | - horsepower: int|
    +-----------------+
    | + start()       |
    | + stop()        |
    +-----------------+
```
### dunder double underscore magic methods
Everything is an object.
The base type (class) in Python is object .
Python defines several built-in methods (enclosed by __ : the "dunder" - double underscore)
### Object Initialization and Representation

    __init__(self, ...): Constructor method; initializes a new instance of the class.
    __str__(self): Returns a user-friendly string representation of the object (used by print()).
    __repr__(self): Returns an official string representation of the object (used by repr() and in the interactive interpreter).
    __del__(self): Destructor method; called when an object is about to be destroyed

### Attribute Access and Management

    __getattr__(self, name): Called when accessing an attribute that doesn't exist.
    __setattr__(self, name, value): Called when setting an attribute's value.
    __delattr__(self, name): Called when deleting an attribute.
    __hasattr__(self, name): Called to check if an attribute exists.

### Container Methods

    __len__(self): Returns the length of the object (used by len()).
    __getitem__(self, key): Allows indexing to access elements (e.g., obj[key]).
    __setitem__(self, key, value): Allows indexing to set elements (e.g., obj[key] = value).
    __delitem__(self, key): Allows deletion of indexed elements (e.g., del obj[key]).
    __iter__(self): Returns an iterator for the object (used in loops).
    __next__(self): Returns the next item from the iterator.

 ###   Mathematical Operations

    __add__(self, other): Defines behavior for addition (e.g., +).
    __sub__(self, other): Defines behavior for subtraction (e.g., -).
    __mul__(self, other): Defines behavior for multiplication (e.g., *).
    __truediv__(self, other): Defines behavior for true division (e.g., /).
    __floordiv__(self, other): Defines behavior for floor division (e.g., //).
    __mod__(self, other): Defines behavior for modulo operation (e.g., %).
    __pow__(self, other): Defines behavior for exponentiation (e.g., **).
    __neg__(self): Defines behavior for unary negation (e.g., -obj)

   ### Comparison Operations

    __eq__(self, other): Defines behavior for equality (e.g., ==).
    __ne__(self, other): Defines behavior for inequality (e.g., !=).
    __lt__(self, other): Defines behavior for less than (e.g., <).
    __le__(self, other): Defines behavior for less than or equal to (e.g., <=).
    __gt__(self, other): Defines behavior for greater than (e.g., >).
    __ge__(self, other): Defines behavior for greater than or equal to (e.g., >=)

 ###   Other Useful Dunder Methods

    __call__(self, ...): Allows an instance of the class to be called as a function.
    __hash__(self): Returns a hash value of the object (used by hash()).
    __bool__(self): Defines behavior for truth value testing (used by bool())

###  Context Management

    __enter__(self): Defines behavior for entering a context (used in with statements).
    __exit__(self, exc_type, exc_val, exc_tb): Defines behavior for exiting a context  


```py
class MyList:
    def __init__(self, data):
        self.data = data

    def __len__(self):
        return len(self.data)

my_list = MyList([1, 2, 3])
print(len(my_list))  # Output: 3

class Person:
    def __init__(self, name):
        self.name = name

    def __str__(self):
        return f"Person: {self.name}"

person = Person("Alice")
print(person)  # Output: Person: Alice

class CustomDict:
    def __init__(self):
        self.data = {'key1': 'value1', 'key2': 'value2'}

    def __getitem__(self, key):
        return self.data[key]

custom_dict = CustomDict()
print(custom_dict['key1'])  # Output: value1

class Multiplier:
    def __init__(self, factor):
        self.factor = factor

    def __call__(self, x):
        return x * self.factor

double = Multiplier(2)
print(double(5))  # Output: 10

class NumberSet:
    def __init__(self):
        self.numbers = {1, 2, 3, 4, 5}

    def __contains__(self, item):
        return item in self.numbers

number_set = NumberSet()
print(3 in number_set)  # Output: True
print(6 in number_set)  # Output: False

class Countdown:
    def __init__(self, start):
        self.current = start

    def __iter__(self):
        return self

    def __next__(self):
        if self.current <= 0:
            raise StopIteration
        else:
            self.current -= 1
            return self.current + 1

countdown = Countdown(3)
for number in countdown:
    print(number)  # Output: 3, 2, 1


```
### csv and json

csv
Typical and easy way to represent tabular data.
Use it with import csv .
Read from files with a reader (or DictReader ).
Write to files with a writer (or DictWriter ).

    import csv
    with open("file.csv", encoding="utf-8") as fp:
    reader = csv.reader(fp) # or DictReader
    for row in reader:
    print(row)

to write csv files use writer and write lists/tuples
better! use DictWriter
- requires fields to be provided as a list
- writes header row with .writeheader()
- takes dicts and write rows

    example = {"name": "Tim", "grade": 25}
    fields = list(example.keys())
    with open("output.csv", "w", encoding="utf-8", newline="") as fp:
        writer = DictWriter(fp, fields=fields)
        writer.writeheader()
        writer.writerow(example)

### json
JSON: JavaScript Object Notation
One of the many ways to represent data
Similar to the way JavaScript represents data internally
Very heavily used for communications between clients and servers using ReSTful APIs
Pros
Lightweight and very flexible
Language independent
Easy to read and write (even by humans)
Flat (text format)
Cons
Very flexible – no validation
No comments
Hard to "debug

JSON data types
Key / value pairs
Keys are strings
Values can be:
strings
numbers (integer, floating)
objects (= another JSON block)
arrays
special (booleans, null)

    { # object dict
        "name": "Alice", #string
        "age": 30, #number int/float
        "city": "New York",
        "skills": [ # array - list
            "Python",
            "Data Analysis",
            "Machine Learning"
        ]
    }
### json in python
```py
import json
with open("input.json") as fp:
json.load(fp)
value = """["JSON list", {"keyword": "value"}]"""
data = json.loads(value)
with open("output.json", "w") as fp:
json.dump(data, fp)
print(json.dumps(data))
```
python js mapping
dict - object
list,tuple - array
str - string
int,long,float - number
boolean - boolean
None - null

### Using JSON to represent class instances
There is no built in way to serialize or deserialize Python classes
Use the built-in conversion for the Python primitive types
Serialization: create a to_json method that returns a JSON string
converts the state into a Python dict or list, serialize to JSON
Create a to_dict method that return a dictionary
Deserialization: convert from JSON
Create a class method from_json method that takes in a JSON string
Deserialize the string to a dict or list
Create an instance, and set the instance attributes to the values from the dict / list

### Definitions:
Serialization: creating JSON from data
Deserialization: creating data from JSON
The json library supports the serialization / deserialization of several Python native data types.


### httpx 
http client for python allwas http requests supports connection pooling session managing asynch requests
pip install httpx
get requests

    import httpx

    response = httpx.get('https://api.example.com/data')

    # Check the status code
    print(response.status_code)  # Output: 200 for a successful request

    # Access response content
    print(response.json())  # Assuming the response is JSON

post request

    data = {'key': 'value'}
    response = httpx.post('https://api.example.com/submit', json=data)

    print(response.status_code)  # Output: 201 for created
    print(response.json())  # Check the response

timeouts

    try:
        response = httpx.get('https://api.example.com/data', timeout=5.0)
    except httpx.TimeoutException:
        print("The request timed out.")

copy parameters

    params = {'search': 'query', 'limit': 10}
    response = httpx.get('https://api.example.com/search', params=params)

    print(response.json())

custom headers

    headers = {'Authorization': 'Bearer YOUR_TOKEN'}
    response = httpx.get('https://api.example.com/protected', headers=headers)

    print(response.json())

using sessions

    with httpx.Client() as client:
    response1 = client.get('https://api.example.com/data')
    response2 = client.get('https://api.example.com/other')

    print(response1.json())
    print(response2.json())

asynch requests

    import httpx
    import asyncio

    async def fetch_data(url):
        async with httpx.AsyncClient() as client:
            response = await client.get(url)
            return response.json()

    async def main():
        urls = ['https://api.example.com/data1', 'https://api.example.com/data2']
        tasks = [fetch_data(url) for url in urls]
        results = await asyncio.gather(*tasks)
        print(results)

    # Run the async main function
    asyncio.run(main())


### beautiful soup

used for parsing html and xml
navigation is easy

pip install beautifulsoup4, requests

importing libs and loading html

    import requests
    from bs4 import BeautifulSoup

    # Fetch the HTML content (example URL)
    url = 'https://example.com'
    response = requests.get(url)

    # Load the HTML content into BeautifulSoup
    soup = BeautifulSoup(response.text, 'html.parser')

using find

    # Extracting the title
    title = soup.find('title').text
    print(f"Title: {title}")  # Output: Title: Example Page

    # Extracting the first paragraph
    first_paragraph = soup.find('p').text
    print(f"First Paragraph: {first_paragraph}")  # Output: First Paragraph: This is a simple example.

using select

        # Extracting the header using a CSS selector
    header = soup.select('h1')[0].text
    print(f"Header: {header}")  # Output: Header: Welcome to Example Page

    # Extracting the link using a class selector
    link = soup.select('a[href]')[0]['href']
    print(f"Link: {link}")  # Output: Link: https://example.com/about

    # Extracting all paragraphs
    paragraphs = soup.select('p.description')
    for para in paragraphs:
        print(para.text)  # Output: This is a simple example.


combined 

        # Finding all links in paragraphs
    for para in soup.find_all('p'):
        links = para.select('a')
        for link in links:
            print(link['href'])  # Output: Will print any links inside paragraphs

Return Type:

    .find() returns the first matched element, while .select() returns a list of all matched elements.

Selector Type:

    .find() uses tag names and attributes for matching, while .select() uses CSS selectors, which can be more versatile.

Use Case:

    Use .find() for quick searches for single elements, and use .select() for more complex queries or when you need multiple elements


class examples
```python
import re

import httpx
from bs4 import BeautifulSoup

class Book:
    # Class variable - holds all the field names
    FIELDS = ["title", "price", "available", "rating", "upc", "url"]

    def __init__(self, url):
        print("--- BOOK ---", url)
        
        # Get the page
        response = httpx.get(url)
        # Parse the HTML
        soup = BeautifulSoup(response.text, "html.parser")
        
        # Set attributes
        self.url = url  # Store the URL of the book page
        self.soup = soup  # Store the BeautifulSoup object for further parsing
        
        # Extract the title of the book
        title = soup.find("h1")
        if not title:
            raise RuntimeError  # Raise an error if title not found
        self.title = title.text  # Store the title text

        # Extract the price of the book
        price = soup.select(".product_main p.price_color")
        if not price:
            raise RuntimeError  # Raise an error if price not found
        # Convert price to a float by filtering numeric characters and the decimal point
        self.price = float("".join([let for let in price[0].text if let.isnumeric() or let == "."]))
        
        # Extract the availability of the book
        avail = soup.select(".product_main p.availability")
        if not avail:
            raise RuntimeError  # Raise an error if availability not found
        # Use regex to find the number of available copies
        self.available = int(re.search(r"In stock \((\d+) available\)", avail[0].text.strip()).group(1))

        # Extract the UPC of the book
        self.upc = soup.find("th", string="UPC").next_sibling.text

        # Map star ratings from strings to integers
        _ratings = {"one": 1, "two": 2, "three": 3, "four": 4, "five": 5}
        # Extract rating class and map to numeric value
        self.rating = [
            _ratings[c.lower()]
            for c in soup.find("p", attrs={"class": "star-rating"}).attrs["class"]
            if c.lower() in _ratings
        ].pop()  # Get the last value in the list (the rating)


    def to_dict(self):
        # Convenience method - return fields as a dictionary
        return {field: getattr(self, field) for field in self.FIELDS}


# Import necessary modules for scraping
import csv
from urllib.parse import urljoin

import httpx
from bs4 import BeautifulSoup

from book import Book  # Import the Book class from the book module

def scrape(url="https://books.toscrape.com/index.html"):
    # An array to hold all the book objects
    books = []

    # The CSV file we write to
    out = open("books.csv", "w", newline="")
    # Create a CSV writer object with the field names from the Book class
    writer = csv.DictWriter(out, fieldnames=Book.FIELDS)
    writer.writeheader()  # Write the header to the CSV file

    keep_going = True  # Flag to control the loop
    while keep_going:
        # Main loop for scraping each page of books
        print("--- INDEX PAGE ---", url)
        
        response = httpx.get(url)  # Fetch the HTML content of the page
        
        soup = BeautifulSoup(response.text, "html.parser")  # Parse the HTML
        # Find book links and create book objects
        for book in soup.select(".product_pod h3 a"):            
            book_url = urljoin(url, book.attrs["href"])  # Construct the full book URL
            book_obj = Book(book_url)  # Create a Book object for the book URL
            # Add the book object to the list
            books.append(book_obj)
            # Write the book object data to the CSV file
            writer.writerow(book_obj.to_dict())
            
        # Find the next page link
        next_link = soup.select("li.next a")
        
        if not next_link or len(next_link) == 0:
            # No link found - we stop the loop
            keep_going = False  # Set the flag to stop the loop
        else:
            # Update the URL with the next page link and continue the loop
            url = urljoin(url, next_link[0].attrs["href"])
    
    out.close()  # Close the CSV file after writing all data
    return books  # Return the list of book objects


if __name__ == "__main__":
    books = scrape()  # Call the scrape function when the script is executed


```
