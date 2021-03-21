# Week 8: <br> 
**Disclaimer: This document is meant to supplement other studying materials, not replace them**<br>

### Concepts
   * Interfaces
   * Abstract Classes
   * Exams are cumulative. You should have a strong understanding of past material(References, Polymorphism, etc.). If not, ask for help!
   
   You can use a code playground on the CS 125 website to follow along and test the code! https://cs125.cs.illinois.edu/
   

# Conceptual Check
<br>


When a class implements an interface what is the promise that is made?<br>

Can a class implement an interface and extend a class?<br>

How many interfaces can we implement? <br>

How do you declare an interface? <br>

Can you instantiate an abstract class? <br>

What are abstract methods? <br>



# Practice Problems
<br></br>
1. Create an interface called ``KleeneStar``. The ``KleeneStar`` interface has one method called ``Kleenify`` that takes in one string and an ``int``. Create a new class of your choice that implements this interface. Assert the passed in string is not null. Your Kleene star function should print out the string the amount of times as the int. See the example below:
```
Kleenify("CS", 0) \\ prints out nothing
Kleenify("CS", 1) \\ Prints out CS
Kleenify("CS", 2) \\ prints out CSCS
```
A Kleene star is actually an important topic in computational theory. If this interests you [Click Here](https://en.wikipedia.org/wiki/Kleene_star#:~:text=In%20mathematical%20logic%20and%20computer,as%20the%20free%20monoid%20construction.)

2. Create a class called ``ArraySum`` that implements comparable. The ArraySum constuctor takes in an Int Array which you should ``assert`` is not ``null``. It should implement a method ``sum`` that sums the stored array. You should implement the ``compareTo`` method based off of which class has the larger sum. <br>



3. Create two classes an abstract ``Pet`` class and a non-abstract ``Shape`` class. Use your imagination and think about some methods ``Pet`` should have. Shape should have a constuctor that takes in an ``Int`` which is the number of sides. The method ``numberOfSides`` should return the number of sides. It should also have an ``abstract`` method called shapeType. Are you aware of what this means? <br>



FeedBack: https://forms.gle/yJLaYFaBtthPf3AP6 <br>






