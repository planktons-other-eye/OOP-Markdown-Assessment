### Slideshow 1

---

#### Objects

-can be a variable, data structure, function, or method *(a location in memory having a value that can be referenced by an identifier)*

-an instance of a class where the object can either be a variable, function, data structure, or combo

-recall an Object is an **instance**

**States:** characteristics, measurable data of Object

**Behaviour:** available functionality of object, what can it do? 

**Object's data:** attributes 

**Object's code:** methods

Example of class Dog with methods and attributes: 

    Dog attributes: 
        -name
        -colour
        -isHungry
    Dog methods:
        -bark()
        -sleep()
        -eat()

#### Object-oriented programming:

-designs programs with cretion of Objects

-creates an object that can be defined and provides functionality

-focuses on how to manipulate the data of the object rather than the logic required to manipulate them

**Class:** abstract description of all objects that can be made from this set class where an object can be instantiated from

**Class** contains: 
* Attributes: object's accessible tools
* Fields: variables that belong to an object/class
    1. type 1: belongs to instance of a class
    2. type 2: belongs to class itself 
* Methods: functions that the class or object can call

**To create a Class:**
1. Define name of class in caps
2. In code block define attributes
3. Assign variable with instantiation of class to interact with it

Example: 

```python
    class Person:
        pass
    student = Person() #student is now a Person Object
    print(student)
```

A class can have methods:

```python
    class Person: 
        def greet(self):
            print("Hello, how are you?")
    individual = Person()
    individual.greet()
```

**def __init__(self):** ---> the initialization method
    -the init method is executed as soon as object of class is instantiated 
    -does initialization for the object's attribues 
    -self parameter is used to denote that the method is applied to and accessible for the object itself 
    -self will also treat its own attributes as local
    -DOUBLE underscore is a key hidden feature allows overwriting of python features and hidden content

Example: 

```python
    class Person:
        def __init__(self, name):
            self.name = name

        def greet(self): #self is always required 
            print("Hello, my name is", self.name)

    bob = Person("Bob")
    bob.greet()'''
```

_-A list is an object in python 3_

#### Practice

1: Implement Person class, needs to create a Person with a last name, create method to set birth year, create method to print age 

```python
    class Person: 

        def __init__(self, lastname, age):
            self.lastname = lastname 
            self.age = age

        def greet(self):
            print("Hi my name is", self.lastname)

        def bday(self, year):
            self.year = year
            return year

        def ages(self):
            print("My age is", self.age)

    p = Person("bob", 12)
    p.greet()
    print(p.bday(2005))
    p.ages()
```

2: Create your own class

```python
    class Dog:

        def __init__(self, name, breed, age):
            self.name = name 
            self.breed = breed 
            self.age = age 

        def greet(self):
            print("Woof, my name is", self.name + ". I am a", self.breed + " and I am", self.age)

    doggy = Dog("Bob", "Mutt", 2)
    doggy.greet()
```

*End of notes*
