# Week 3 quiz prep
**Disclaimer: This document is meant to supplement other studying materials, not replace them**<br>

### Concepts
   * Objects, objects, more objects
   <br></br>
   
   You can use a code playground on the CS 125 website to follow along and test the code! https://cs125.cs.illinois.edu/
   

# Conceptual Check
<br></br>
## Multi-Dimensional Arrays

Do you understand the difference between an instance, a class, and an object?
<br></br>
What Does a constructor do? Do you understand how they work?
<br></br>
How many constructors can we have?
<br></br>
What are instance variables and methods?
<br></br>
If I make two objects of the same class will they operate independently?
<br></br>
How do we format our class names?
<br></br>
 # Practice Problems
 **I will add solutions after the quiz prep session Monday.**<br>

 
 1. You are responsible for what your class stores. I will only explain how we interface with it and what we want it to do. Create a class called `` BabyDfa ``. You will make two methods one called ``insert`` which accepts one int argument either 0 or 1 and is void. The other called ``isTrue`` which returns a boolean and takes no arguments. If the last two times we called insert the arguments were a 1 followed by a 0 `` isTrue `` should return true, else return false. That doesnt make much sense so view the example below.
 Ex:
```
	BabyDfa mu = new BabyDfa();
  mu.insert(1);
  mu.insert(0);
  mu.isTrue(); //returns true
  mu.insert(0);
  mu.isTrue() // returns false
```

  <br></br>
 2. Write a class called `` MPGLeft``. Its constructor should take in two values, the number of gallons of fuel left in a car as a double, and the miles per gallon the car gets also as an int. It should not have a default constructor. Your goal is to create a method `` milesDriven`` that takes in the number of new miles the car has driven and then returns the number of gallons we have left as a double.
   <br></br>
 3. Use **Method Overloading** and write two area functions. One where the passed in argument is a radius (area of a circle), and another where you are passed in a base and a height(area of a triangle).
 <details>
	<summary>Spoiler!</summary>
  
  ```java
 double area(double radius) {
  return 3.14 * radius * radius;
}

double area(double base, double height) {
  return .5 * base * height;
  
}
  
  ```
  </details>
    <br></br>
4. Write a function that finds the sum of a 2D int Array. Wait no, thats too easy. Lets add a few rules. In this example we will refer to our 2D array in rows and columns, since it is appropiate here.
```java
int[][] myArray = new Int[4][4]
//Do a bunch of stuff.
When we map out our 2D array lets say it looks something like this
{1,2,3,4} [0]
{2,2,6,4} [1]
{9,8,2,7} [2]
{6,3,7,1} [3]
```

  
The rules are simple. If the first number in the row is larger then the last number we dont sum it. So in the above array Lets say we are at ``myArray[0][someThing]`` Since ``myArray[0][0] < myArray[0][3]`` we go ahead and sum that row. <br>
<details>
	<summary>Spoiler!</summary>
  
  ```java
  int summer(int[][] passedIn) {
  int sum = 0;
  for (int i = 0; i < passedIn.length; i++) {
    for (int j = 0; j < passedIn.length; j++) {
      if (passedIn[i][0] < passedIn[i][passedIn.length - 1]) {
        sum += passedIn[i][j];
      }
    }
  }
  
  return sum;
}
```
 </details>



FeedBack: https://forms.gle/yJLaYFaBtthPf3AP6 
  



