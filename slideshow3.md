### Slideshow 3

---

**Inheritance:** when an object or class is based on another class, where its features are from a parent class 

-can be like a hierarchy or could be a hybrid (mixing types of inheritances)

**Types:**
* Single inheritance: from a single parent
* Multiple inheritance: from multiple parents
   1. Multi-generational
   2. Multi-parent
   3. Mixture of 1 and 2 
* Multilevel: from another subclass

</br>

#### Child class: 

  -a child will recieve all attributes and methods of parent    
  -a child can then enhance itself with new attributes and new methods   
  -can also override attributes and methods for their own liking    
  -child doesn't need a new __init__ unless needs new attributes   
  -child doesn't need to reinstate the parent methods unless you override them   
  
</br>

#### Single inheritance example:

```python
    class Parent:
        #code block 
    class Child(Parent):

        def __init__(self, param, param2):
            Parent.__init__(self, param):
            self.param2 = param2
```

#### Example:

```python
    class Person:
        def __init__(self, name):
            self.__name = name 
        def get_name (self):
            return self.__name 

    class Student(Person):
        def __init__(self, name, num):
            Person.__init__(self, name)
            self.__sNum = num 
        def get_stud_name(self):
```

</br>
</br>

**super()** ---> built-in method for classes to refer to parent class 
    -prevents us from doing ParentClass.method(self)

#### Example of super():

```python
    class Person:
        def __init(self, name):
            self.__name = name 
    class Student(Person):
        def __init__(self, name, num):
            super().__init__(name)
            self.__sNum = num 
```           
</br>

#### Polymorphism in inherited classes: 

```python
    class Parent:
        def method(self):
            pass
    class Child(Parent):
        def method(self):
            #this is same method name but polymorphed into something else 
```
_End of notes_
