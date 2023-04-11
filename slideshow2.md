### Slideshow 2

---
**Encapsulation** --> Info hiding: restricting the access to the classes/object's certain attributes and methods

  -used for data protection
  -restricting certain methods to be callable 
  -use double underscores as a prefix to hide attributes and methods

#### Example of encapsulation: 

    class Student:
        def __init__(self, name, num):
            self.name = name
            self.num = num 

        def __studentnum(self):
            return self.num

    s = Student("bob", 198)
    print(s.__studentnum()) #will cause error because encapsulated 

#### The importance of encapsulation: 

    class Student:
        def __init__(self, name):
            self.name = name

    s = Student("Bob")
    print(s.name) # Bob
    s.name = "Mel"
    print(s.name) # Mel

_Attribute can be changed if not encapsulated (can change private data like passwords)_ 

</br>
</br>

**A setter and a getter when using encapsulated attributes:**

    class Student:
        def __init__(self, name):
            self.__name = name

        def setname(self, new_name):
            self.__name = new_name

        def getname(self):
            return self.__name


</br>

**Overloading:** two methods in one class have the same method name, but different parameters

**Overriding:** two methods have the same name and parameters

-overriding allows the child class to **provide specific implementation for a method** that exists in the parent class

_**-there is no overloading in python**_

**Polymorphism:** a method that can be used across different classes and objects that is dependent on the parameters 

#### Example of two different classes with the same method:

    class Bear:
        def sound(self):
            print("Roar")
    class Dog:
        def sound(self):
            print("Woof")

    def makeSound(animalType):
        animalType.sound()

    bears = Bear()
    dogs = Dog()

    makeSound(bears)
    makeSound(dogs)

-therefore two diff classes can have same methods, *Polymorphism*

-overriding can be seen in inherited classes modifying inherited methods 

#### Override and polymorphism with python

-we can have 2 diff classes with same attributes and methods 

-we can have a child override methods inherited by the parent where the child could utilize the method differently 

#### Example: 

    class Dog:
        def __init__(self, name):
            self.__name = name 

        def __str__(self):
            return (f"Woof, I'm {self.__name}")

    corgi = Dog("pup")
    print(pup) #makes object printable 

**Benefits of overriding built-in methods and operators:**

-start to manipulate how the Object behaves when met with built-in methods and operators 

</br>

**__repr__() base function:** return a string conatining a prinatble representation of an object, allows us to present a printable version of our object, while __str__ allows us to convert our object to string

_End of notes_
