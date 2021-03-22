# Week 8: <br> 
**Disclaimer: This document is meant to supplement other studying materials, not replace them**<br>

### Concepts
   * Interfaces
   * Abstract Classes
   * Exams are cumulative. You should have a strong understanding of past material(References, Polymorphism, etc.). If not, ask for help!
   
   If you need more practice, go to the EMP site: https://cs199emp.netlify.app/
   
   You can use a code playground on the CS 125 website to follow along and test the code! https://cs125.cs.illinois.edu/

# Conceptual Check
<br>


When a class implements an interface, what is the promise that is made?<br>

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

2. Create a class called ``ArraySum`` that implements comparable. The ``ArraySum`` constuctor takes in an Int Array which you should ``assert`` is not ``null``. It should implement a method ``sum`` that sums the stored array. You should implement the ``compareTo`` method based off of which array has the larger sum. <br>
3. Shorter: Can you create a ``Utility`` class that has a class method ``isGreaterThan``. This takes in two objects that implement ``Comparable`` and returns the larger one. <br>


4. Create an abstract ``Pet`` class. Use your imagination and think about some methods ``Pet`` should have, sprinkling in some abstract methods. What behavior do you notice?  <br>
5. **Bonus**: We will have a little bit more fun with Kleene stars. Create an interface called ``KleeneStarDetector`` that has one method ``detector``. Create a class that implements this interface. ``detector`` takes in three arguments, the final string, the original string, and the amount of times it was repeated. If the original string repeated x times equals the first argument return true, else return false.
```
Example:
detector("CSCSCS","CS",3) \\return true
detector("","CS",0) \\return true
detector("CS","CS",2) \\return false
```



FeedBack: https://forms.gle/yJLaYFaBtthPf3AP6 <br>






