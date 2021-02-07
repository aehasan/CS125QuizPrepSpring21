# Week 2 Quiz Prep

**Disclaimer: This document is meant to supplement other studying materials, not replace them**<br>

### Concepts
   * Arrays
   * Loops
   * Functions
   * CS Voices
   <br></br>
   

# Conceptual Overview
(These will be shorter from now on in the interesting of making more practice problems)
<br></br>
## Arrays
  * Arrays in Java are a way of ordering data, ***and they are indexed starting at 0***
  * The last element of the array is at the index of the array's length - 1, not the array's length 
  * Once the length of an array has been declared it cannot be changed
  * There are two ways to declare an array in Java. These examples focus on int arrays
   ```java
   1. int[] myArray = new int[3]; //type[] varName = new type[length]; 
   2. int[] myArray = {1,2,3}; //initialize and declare in one line 
   ```
  * To access the values in the array you should use the [] operators
  * Out of Bounds errors meaning you are accesing an invalid value!!!
  Ex:
  ```java
  int[] myArray = new int[7];
  myArray[7] = 3;  //Error >:(
  ```
  <br></br>
  ## Loops
  A couple types of loops we have learned in this cass:
  ```java
  int i = 0;
  while (i < 7) {
    i++;
  }
  
  for (int i = 0; i < 7; i++) {
    // i is only accesible in here
  }
  
  //enhanced for loop
 int[] myArray = new int[7];
 for (int i : myArray) {
    System.out.println(i);
 }
```
Dont forget about:</br>
Break - Stops executing a loop entirely</br>
Continue - Skips to the next iteration
<br></br>
## Functions
Allow us to use a piece of code over and over again
  **Important: The code in the function is not executed until it is called**
 ```java
 void myFunction() {
  System.out.println("isnt java cool");
 }
 ```
 This will do nothing unless you call it like below: 
 ```java
 void myFunction() {
  System.out.println("isnt java cool");
 }
 myFunction();
 ```
 
 Functions can also take in arguments:
 ```java
 void myFunction(int a) {
  System.out.println(a);
 }
 ```
 Functions can also return values.
 **These are not the same as print statements**
 When a return is executed we exit the function
 Ex:
 ```java
 int myFunction() {
  return 7;
  //everything below here will not be executed
 }
 ```
 <br></br>
 # Practice Problems
 **I will add solutions after the quiz prep session Monday.**
 
 1. Write a function that prints out all the values of an array that is passed in.
   <br></br>
2. Write a function that takes in two arrays, and then returns the array that has the largest sum
  <br></br>
  
3. Uh oh. It appears a football player is deflating the footballs again >:(. Write a function that accepts an array of football pressures. If a PSI in the array is below 12.5 return true, otherwise return false.
   <br></br>
4. Write a function that accepts an int array, index, and an int value. Then change the index to the value and return the new array.
  <br></br>

5. **Hard**: Write a function that determines if the passed in array has repeated numbers. Brute Force is a completely acceptable solution.

  
  

