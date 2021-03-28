# Week 8: <br> 
**Disclaimer: This document is meant to supplement other studying materials, not replace them**<br>

### Concepts
   * Interfaces
   * Abstract Classes
   * Exams are cumulative. You should have a strong understanding of past material(References, Polymorphism, etc.). If not, ask for help!
   
   If you need more practice with interfaces and abstract classes & methods, go to the EMP site: https://cs199emp.netlify.app/dist/s21/2021-03-19.html#1
   
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

1. Create an interface called ``KleeneStar``. The ``KleeneStar`` interface has one method called ``kleenify`` that takes in one string and an ``int``. Create a new class of your choice that implements this interface. Assert the passed in string is not null. Your Kleene star function should print out the string the amount of times as the int. See the example below:
```
kleenify("CS", 0) \\ prints out nothing
kleenify("CS", 1) \\ Prints out CS
kleenify("CS", 2) \\ prints out CSCS
```
A Kleene star is actually an important topic in computational theory. If this interests you [Click Here](https://en.wikipedia.org/wiki/Kleene_star#:~:text=In%20mathematical%20logic%20and%20computer,as%20the%20free%20monoid%20construction.)
<details>

```java
public interface KleeneStar {
  void kleenify(String arg1, int arg2);
}

public class Stargirl implements KleeneStar {
  public void kleenify(String arg1, int arg2) {
    assert (arg1 != null);
    for (int i = 0; i < arg2; i++) {
      System.out.print(arg1);
    }
  }
}

```


</details>


2. Create a class called ``ArraySum`` that implements ``Comparable``. The ``ArraySum`` constuctor takes in an Int Array which you should ``assert`` is not ``null``. It should implement a method ``sum`` that sums the stored array. You should implement the ``compareTo`` method based off of which array has the larger sum. <br>
<details>

```java
public class ArraySum implements Comparable {
  int[] myArray;
  int summer;
  public ArraySum(int[] j) {
    assert j != null;
    myArray = j;
  }
  
  public void sum() {
    int sum = 0;
    for (int i = 0; i < myArray.length; i++) {
      sum += myArray[i];
    }
    summer = sum;
  }
  
  public int compareTo(Object o) {
    assert (o instanceof ArraySum);
    ArraySum other = (ArraySum) o;
    sum();
    other.sum();
    
    if (summer < other.summer) {
      return -1;
    }
    if (summer == other.summer) {
      return 0;
    }
    
    return 1;
  }
}
```

</details>

3. Shorter: Can you create a ``Utility`` class that has a class method ``isGreaterThan``. This takes in two objects that implement ``Comparable`` and returns the larger one. <br>
<details>
  
 ```java
  public class Utility {
  public static Comparable isGreaterThan(Comparable one, Comparable two) {
    if (one.compareTo(two) < 0) {
      return two;
    }
    return one;
  }
}
```
</details>


4. Create an abstract ``Pet`` class and implement it in two different classes. Use your imagination and think about some methods ``Pet`` should have, sprinkling in some abstract methods. What behavior do you notice?  <br>
<details>
  
  ```java
  public abstract class Pet {
  public abstract String name();
  public abstract String type();
  
  public int numberOfFeet() {
    return 4;
  }
}

public class Cat extends Pet {
  public String name() {
    return "Josh"
  }
  public String type() {
    return "Cat"
  }
}
```
</details>

5. **Bonus**: We will have a little bit more fun with Kleene stars. Create an interface called ``KleeneStarDetector`` that has one method ``detector``. Create a class that implements this interface. ``detector`` takes in three arguments, the final string, the original string, and the amount of times it was repeated. If the original string repeated x times equals the first argument return true, else return false.
```
Example:
detector("CSCSCS","CS",3) \\return true
detector("","CS",0) \\return true
detector("CS","CS",2) \\return false
```
<details>
  
  ```java
  public class Off implements KleeneStarDetector {
  public boolean detector(String mutated, String original, int multiplier) {
    assert mutated != null;
    assert original != null;
    
    int originalLength = original.length();
    int newLength = mutated.length();
    if (newLength != originalLength * multiplier) {
      return false;
    }
    int currentStart = 0;
    int currentEnd = original.length();
    for (int i = 0; i < multiplier; i++) {
      System.out.println(mutated.substring(currentStart, currentEnd));
      if (!mutated.substring(currentStart, currentEnd).equals(original)) {
        return false;
      }
      currentStart += original.length();
      currentEnd += original.length();
    }
    return true;
  }
}
```
 </details>



Feedback: https://forms.gle/yJLaYFaBtthPf3AP6 <br>







