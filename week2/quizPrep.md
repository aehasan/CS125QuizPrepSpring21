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
#Arrays
  * Arrays in Java are a way of ordering data, ***and they are indexed starting at 0***
  * Once the length of an array has been declared it cannot be changed
  * There are two ways to declare an array in Java. These examples focus on int arrays
   ```java
   1. int[] myArray = new int[length];
   2. int[] myArray = {1,2,3};
   ```
  * To access the values in the array you should use the [] operators
  * Out of Bounds errors meaning you are accesing an invalid value!!!
  Ex:
  ```java
  int[] myArray = new int[7];
  myArray[7] = 3;
  ```
  <br></br>
  # Loops
  A couple types of loops we have learned in this cass:
  ```java
  (for int i = 0; i < 7; i++) {
  // i is only accesible in here
  }
  
  int i = 0;
  
  while (i < 7) {
  i++
  }
  
  //and then we have the enhanced for loop
 int[] myArray = new int[7];
for (int i : myArray) {
  System.out.println(i);
}
```
Dont forget about:
Break - Stops executing a loop entirely
Continue - Skips to the next iteration

#Functions
Allow us to use a piece of code over and over again
  

