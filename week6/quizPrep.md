# Week 6: <br> 
**pog: PolymOrphismisGreat**<br>
**Disclaimer: This document is meant to supplement other studying materials, not replace them**<br>

### Concepts
   * Static
   * Inheritance 
     * Overriding  
   * Polymorphism 
     * Upcasting (implicit)
     * Downcasting (explicit) (use instanceof operator)
   ```Java
   class CoolSkills;
   class Coding extends CoolSkills;
   class LearningJava extends Coding;
   class Polymorphism extends LearningJava;
   ```
   
   You can use a code playground on the CS 125 website to follow along and test the code! https://cs125.cs.illinois.edu/
   

# Conceptual Check
<br>

Story Time: What happens when we cast? <br>
<br>
One day Timothy woke up and went "Wow I want to challenge myself today" so he decided to learn how to cast objects in Java. Timothy made a couple of classes documented below: <br>
```java
public class Shape {
  String type;
  double area;
}

public class Triangle extends Shape {
 int sideOne;
 int sideTwo;
 int sideThree;
}

public class Square extends Shape {
 int squareSideOne;
 int squareSideTwo;
 int squareSideThree;
 int squareSideFour;
}
```
Wow Timothy thought. I am so smart. As a CS major Timothy has only one friend, the compiler. Timothy likes the compiler because he does whatever Timothy wants.<br>
Timothy waltz's up to the compiler and reads off this line: <br>
``Shape waitWhat = new Square();`` <br>
**Do you know what is going on here**<br>


Wow the compiler thought, what a useless thing to do. But as the compiler he listened anyway. Timothy then tells the compiler to: <br>
``waitWhat.squareSideOne;``<br>
**Do you know what will happen**<br>


The compiler doesnt know what to do. Even though the compiler is holding a square it is told to think of it as a shape. The compiler feels confused and doesnt know what to do. So it spits out some useless jargon. Timothy is confused. He feels forsaken, and goes to bed. That night Timothy had a wonderful dream about a place where CS majors congregate. It was called Stack Overflow. Timothy wakes up and rushes to his computer, and learns some new tricks. Do you understand the following:<br>
``waitWhat instanceof Square;``<br>
``Square postCast = (Square) waitWhat;``<br>
Timothy has solved his problem. The End.<br>
<br>
**Disclaimer: The opinions displayed in this story may not be the opinions of the entirety of the CS 125 Course Staff, or that of the writer, and are simply there as very bad comedy.** <br>
<br>
Do you also understand Up-Casting?<br>
How Does static affect variables?<br>
How Does static affect methods?<br>
**Quiz Prep: Design a class that uses both static methods and variables**

# Practice Problems
<br></br>
1. Create a class called ``WowThatWasAGoodStory`` with one static int variable called ``goodRating``. Create one static method called ``provideGoodRating`` that only accepts positive integers(Duh) and returns the changed int. Do you see why both need to be static? <br></br>
2. There was a lot of confusion on the IsEquals homework so lets do a similar problem. Create a class called ``Address`` that has four variables all should be private. ``Int: apt/house number``, ``String: Street``, ``String: Town``, ``Int: ZipCode``. Then override the isEquals method following standard conventions. Do you see why you can access private variables inside this method? <br></br>
3. Create a static method in a new ``Utility`` class called ``isItInTheZoo``, that returns a String. We have defined a general ``Animal`` class and some more specific animals that extend it below. Feel free to copy this into the playground. ``isItInTheZoo`` accepts an object and returns ``you goofed`` if you pass in anything other then an animal. If you passed in an Animal class and only an Animal class return ``Too General``. If you passed in any of the more specific Animals return the name of the Animal. <br></br>


```Java
public class Animal {
 public String animalSound;
 public boolean coldBlooded;
}

public class Zebra extends Animal {
 public int numberOfStripes;
}

public class Bear extends Animal {
 public int numberOfFishEaten;
}
```

FeedBack: https://forms.gle/yJLaYFaBtthPf3AP6 
  




