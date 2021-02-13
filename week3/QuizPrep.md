# Week 2 Quiz Prep
**Disclaimer: This document is meant to supplement other studying materials, not replace them**<br>

### Concepts
   * Multi-Dimensional arrays
   * Strings
   * More Functions
   * CS Voices
   <br></br>
   
   You can use a code playground on the CS 125 website to follow along and test the code! https://cs125.cs.illinois.edu/
   

# Conceptual Overview
**The Conceptual Overview is much shorter this week. There is not much content to memorize however it is important you practice**
<br></br>
## Multi-DimensionalArrays
Multi-Dimensional arrays are a cool new way to store data. They are initialized is followed:
```Java
//you can have as many dimesions as you want
int[][] myArray = new int[SIZE][SIZE];
```
**Concept Check**:What would happen if we didnt set the array equal to anything?

We can access a multi-dimensional array as followed:
```Java
int[][] myArray = new int[3][3];

for (int i = 0; i < myArray.length; i++) {
  for (int j = 0; j < myArray[i].length;j++) {
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
  String myString = "bruuuh"
  ```
  You can also add strings together in java to concatenate them:
  ```java
  ```
  

 <br></br>
 # Practice Problems
 **I will add solutions after the quiz prep session Monday.**
 
 1. Write a function that prints out all the values of an array that is passed in.
 <details>
	<summary>Spoiler!</summary>
	
```java
	void printArray(int[] a) {
	  for (int i : a) {
           System.out.println(i);
 	  }
  
	}
	
```
</details>
   <br></br>
2. Write a function that takes in two arrays, and then returns the array that has the largest sum
 <details>
	<summary>Spoiler!</summary>
	
```java
	int[] returnLargestSum(int[] one, int[] two) {
  	  int sumOne = 0;
  	  int sumTwo = 0;
  
  	  for (int i : one) {
    		sumOne += i;
  	  }
  	  for (int i = 0; i < two.length; i++) {
    		sumTwo += two[i];
 	  }
  
  	  if (sumOne > sumTwo) {
    		return one;
  	  } else {
    	       return two;
  	  }
	}
	
```
</details>

  <br></br>
  
3. Uh oh. It appears a football player is deflating the footballs again >:(. Write a function that accepts an array of football pressures. If a PSI in the array is below 12.5 return true, otherwise return false.
 <details>
	<summary>Spoiler!</summary>
	
```java
	boolean bradyDetector(double[] one) {
 	  for (double i : one) {
    	    if (i < 12.5) {
     	      return true;
    	    }
  	  }
  
  	return false;
	}

	
```
</details>


   <br></br>
4. Write a function that accepts an int array, index, and an int value. Then change the index to the value and return the new array.
 <details>
	<summary>Spoiler!</summary>
	
```java
	int[] changeValue(int[] myArray, int index, int value) {
  	   myArray[index] = value;
  	   return myArray;
	}


	
```
</details>

  <br></br>

5. **Hard**: Write a function that determines if the passed in array has repeated numbers. Brute Force is a completely acceptable solution.

 <details>
	<summary>Spoiler!</summary>
	
```java
	boolean areThereRepeats(int[] passedIn) {
  	   for (int i = 0; i < passedIn.length; i++) {
    		for (int j = 0; j < passedIn.length; j++) {
      		  if (i != j) {
        
        	     if (passedIn[i] == passedIn[j]) {
                        return true;
       		     }
      		  }
    		}
  	     }
 	   return false;
	}


	
```
</details>

  <br></br>


  
  


