# Week 9: <br> 
**Disclaimer: This document is meant to supplement other studying materials, not replace them**<br>

### Concepts
**This quiz prep will focus on covering what we view as the most difficult material these past couple weeks. Again it does not cover everything. Theres only so much that can be done in an hour**
   * Inheritance
   * Polymorphism
   * References/ Deep and Shallow Copies
   * Static
   * Interfaces
   
   If you need more practice with check out the the EMP site: https://cs199emp.netlify.app/dist/s21/2021-03-19.html#1
   
   You can use a code playground on the CS 125 website to follow along and test the code! https://cs125.cs.illinois.edu/

# Conceptual Check
<br>

### Inheritance
Simple enough we are pros at this
```Java
public class Pet {
  protected String petName;
  protected int age;
  Pet(String a, int b) {
    petName = a;
    age = b;
  }
  
  public int getAge() {
    return age;
  }
  
  public String getName() {
    return petName;
  }
  public boolean whosBigger(Pet a) {
    if (age < a.age) {
      return false;
    }
    return true;
  }
}

public class Dog extends Pet {
  public int treatLevel;
  Dog(String name, int age, int treat) {
    super(name, age);
    treatLevel = treat;
  
  }
  
  public boolean whosBigger(Dog a) {
    if (age < a.age) {
      return false;
    }
    return true;
  }
  
  public boolean goodDog() {
    return true;
  }
}

```
**Questions** <br>
1. Is the super call necessary <br>
2. What variables can we access with a Pet reference? What about with a Dog reference
### Polymorphism
Lets continue with the example above I will copy it below:
```Java
public class Pet {
  protected String petName;
  protected int age;
  Pet(String a, int b) {
    petName = a;
    age = b;
  }
  
  public int getAge() {
    return age;
  }
  
  public String getName() {
    return petName;
  }
  public boolean whosBigger(Pet a) {
    if (age < a.age) {
      return false;
    }
    return true;
  }
}

public class Dog extends Pet {
  public int treatLevel;
  Dog(String name, int age, int treat) {
    super(name, age);
    treatLevel = treat;
  
  }
  
  public boolean whosBigger(Dog a) {
    if (age < a.age) {
      return false;
    }
    return true;
  }
  
  public boolean goodDog() {
    return true;
  }
}

```
Let us walk through what happens when we execute the following line: <br>
```Pet xyz = new Dog();```
As we have learned before, the ``new`` key word is what actually makes the object. So from this we can clearly see weve made a new Dog object. This is drawn below:<br>
 <img width="727" alt="Screen Shot 2021-03-27 at 11 59 20 PM" src="https://user-images.githubusercontent.com/59402383/112742921-7e12fe00-8f58-11eb-97d0-7befd21762d0.png"> <br>
 Then we have said Hey Java, masquerade this ``Dog`` Object as a ``Pet``. Effectively placing walls around all the Dog specific components and only keeping the ``Pet`` ones. This can be seen below: <br>
<img width="722" alt="Screen Shot 2021-03-28 at 12 02 25 AM" src="https://user-images.githubusercontent.com/59402383/112742982-fc6fa000-8f58-11eb-9629-36d8c32f68af.png"> <br>
Run through a couple examples of this in the java Compiler. Do you really understand whats going on. <br>

**Questions** <br>
1. Can you repeat the process above for Up-Casting
2. Test this one out in the compiler to be ultra-certain. Which version of ``whosBigger()`` do we have? The ``Dog`` version or the ``Pet`` version? Do you see why?

### References/ Copying
Objects in Java are **only** made when you use the **new** keyword. <br>
Deep Copies: References point to completely distinct Objects. Changing one doest change the other. <br>
Shallow Copies: References point to the same Object. Changing One changes the other. <br>
```Java
Dog[] myArray = new Dog[4];
for (int i = 0; i < myArray.size(); i++) {
  myArray[i] = new Dog("Travis", 3, 3);
}
```
What kind of copy is this? See the drawing below for a clearer example: <br>
<img width="808" alt="Screen Shot 2021-03-28 at 12 25 50 AM" src="https://user-images.githubusercontent.com/59402383/112743348-355d4400-8f5c-11eb-921f-761e0f2568d7.png"> <br>
What about: <br>
```Java
Dog[] myArray = new Dog[4];
Dog hm = new Dog("Sam", 3, 3);
for (int i = 0; i < myArray.size(); i++) {
  myArray[i] = hm;
}
```
<img width="778" alt="Screen Shot 2021-03-28 at 12 28 27 AM" src="https://user-images.githubusercontent.com/59402383/112743397-89682880-8f5c-11eb-9714-b9f294e8222c.png">

### Static (AKA Class Methods)
Static allows us to change variables across all instances of a class. Play around with the example below:
```Java
public class Utility {
  public static int j = 0;
  public static void counter() {
    j++;
  }
}
```
**Questions**
1. How do we call Static methods?
2. When is making Static methods appropiate?

### Interfaces
This remains fresh in your heads so this part will be quite short <br>

1. If a class implements an Interface it agrees to Implement all the methods of that Interface
2. Using interfaces allow us to take advantage of some polymorphic abilities:

```Java
public class Dog extends Pet implements Comparable {
  public int treatLevel;
  Dog(String name, int age, int treat) {
    super(name, age);
    treatLevel = treat;
  
  }
   public boolean whosBigger(Dog a) {
    System.out.println("Im in Dog");
    if (age < a.age) {
      return false;
    }
    return true;
  }
  
  public boolean goodDog() {
    return true;
  }
  //say we Implemented compareTo() here.
}
```
We can then say:
``Comparable j = new Dog();``

# Practice Problems
<br></br>

1. Override the standard .equals() method for the Dog class above. A dog is equal if it has the same name, age, and treat level.
2. Implement the compareTo() method for the Dog class above using age to determine who is larger or smaller.
3. Make a copy() function for the Dog class above that returns an array of deep copies.
4. If time allows: Pratice Exam.


Feedback: https://forms.gle/yJLaYFaBtthPf3AP6 <br>







