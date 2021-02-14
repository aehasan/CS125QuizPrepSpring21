# Week 3 quiz prep
**Disclaimer: This document is meant to supplement other studying materials, not replace them**<br>

### Concepts
   * Multi-Dimensional arrays
   * Strings
   * More Functions
   * CS Voices
   <br></br>
   
   You can use a code playground on the CS 125 website to follow along and test the code! https://cs125.cs.illinois.edu/
   

# Conceptual Overview
**The Conceptual Overview is much shorter this week. Moving forward there will be little conceptual overview and more conceptual questions. You must review the CS 125 daily lessons to prep for the quiz.**
<br></br>
## Multi-Dimensional Arrays
Multi-Dimensional arrays are a cool new way to store data. They are initialized is followed:
```Java
//you can have as many dimesions as you want
int[][] myArray = new int[SIZE][SIZE];
```
**Concept Check**: Can I find the value in a null array?

We can access a multi-dimensional array as followed:
```Java
int[][] myArray = new int[3][3];

for (int i = 0; i < myArray.length; i++) {
  for (int j = 0; j < myArray[i].length; j++) {
    myArray[i][j] = 3;
  }
}
//What does the above code do?
```
**Concept Check**: Can you trace the for loops in the above code snippet?

In some practice questions later on, we may refer to a 2-D array in rows or columns. However as Geoff said this must be come up with on a problem to problem basis.

  <br></br>
  ## Strings
  A standard way of string text. Initialized with:
  ```java
  String myString = "UofI";
  ```
  You can also add strings together in java to concatenate them:
  ```java
  String myString = "pay";
  String mySecondString = "day";
  String finalString = myString + mySecondString;
  ```
  Concept Check: What is the string in finalString?<br>
  ```Java
  String ope ;
  ```
  Concept Check: What is the current value of ope?
  

 <br></br>
 # Practice Problems
 **I will add solutions after the quiz prep session Monday.**<br>

 
 1. Write a function that takes in an array of Strings formatted as "LastName,firstName". if the passed in Array is null return null. Otherwise return a 2-D array. In the first dimension is everyones Last name. In the second dimension is the corresponding first name.
  <br></br>
 2. Write a function that takes in an array of Strings as its first argument, and a string as its second argument. If either argument is null return -1. Otherwise determine how many Strings in the array start with the string in the second argument. **You are not allowed to use the contains function**
   <br></br>
 3. Use **Method Overloading** and write two area functions. One where the passed in argument is a radius (area of a circle), and another where you are passed in a base and a height(area of a triangle).
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

5. Write a function that takes in two strings and a char. If any argument is null return null. Then determine which String contains that specific char the most, and return the string. If both strings contain the char the same amount of times, return either string.


  
  


