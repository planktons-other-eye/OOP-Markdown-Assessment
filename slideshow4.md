### Slideshow 4

---

**Iterable objects:** objects that we can iterate through like a sequence (ie. strings and lists can be indexed through using for loops)

#### Example: printing all cards in deck 

    class Deck:
        def __iter__(self):
            return self

        def __next__(self):
            self.__index += 1
            if self.__index == len(self.__cards):
                self.__index = -1 #index reset 
                raise StopIteration 
            else:
                return self.__cards[self.__index]
 
</br>

__iter__() ---> allows object to be iterable, when invoked upon, usually by a for loop, commonly just returns itself 

__next__() ---> allows us to get next value when iterating 
    -common practice is to set index attribute to -1, increment index attribute by 1 until self.__index is equal to length of sequence, when end is reached, raise StopIteration 

</br>
</br>
</br> 

#### Overview of Object Oriented Programming: 

**Object Oriented Programming:** focuses on the creation of custom classes for special objects 

**Class:** description of a new object that can be made, classes contain attributes and methods 
    -attributes: variables/data that belongs to the class
    -methods: functions that the object can use and call for 

**Object:** an instance of a class that can be used within a program, an object may have access to the attributes and methods for that class

**Encapsulation --->** _Info hiding:_ restricting the access to the classes/objects certain attributes and methods, used for data protection and restricting certain methods to be callable, use __ as a prefix of the method to do this

**Inheritance:** when an object or class is based on another class, where its features are from the parent class 
1. Single inheritance: one parent
2. Multiple inheritance: multiple parents
3. Multilevel inheritance: from another subclass 
    -inheritance can be like a hierarchy or like a hybrid 

**Polymorphism:** method that can be used across different classes and objects that is dependent on the parameters 
    -we can have 2 diff classes with same attributes and methods 
    -we can have child override methods from the parent so the child can utilize them differently 
    
*End of notes*

