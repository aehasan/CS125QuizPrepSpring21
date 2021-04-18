# Week 12: <br> 
**Disclaimer: This document is meant to supplement other studying materials, not replace them**<br>

### Concepts
   * Exceptions
   * Recursion
   * Trees 
   * Exams are cumulative. You should have a strong understanding of past material (References, Polymorphism, etc.). If not, ask for help!
   
   If you need more practice with recursion, go to the EMP site: https://cs199emp.netlify.app/dist/s21/2021-04-16.html#1
   
   You can use a code playground on the CS 125 website to follow along and test the code! https://cs125.cs.illinois.edu/
   
# Conceptual Check
<br>

What programming construct do we use to handle exceptions? <br>

What are the types of exceptions? Generally, which exceptions do we handle and which ones do we not handle?<br>
    <details>
    <summary>Helpful Image for Exceptions</summary>
    <img src="/images/Exception-in-java.png" alt="drawing" width="600"/>
    </details>
  
What are some examples of exceptions? <br>

What are the three things that all successful recursive algorithms have?<br>

Define these terms in the context of trees: parent, child, root, leaf, level, depth/height
    <details>
    <summary>Helpful Image for Trees</summary>
    <img src="/images/binary_tree.jpg" alt="drawing" width="600"/>
    </details>
    
What makes a ``BinaryTree`` unique compared to other trees? <br>

# Practice Problems

1. Write a function called ``countTimesNumberAppears`` that takes in two ints: one representing the number and the other 
representing the target number. Using recursion, return the number of times that the target is in the number. 
If the number or the target is less than or equal to 0, throw an ``IllegalArgumentException``.
Hint: You can use ``number % 10`` to get the last digit and ``number / 10`` to get rid of the last digit.

Here are some example inputs and outputs:
```java
countTimesNumberAppears(717, 7);  // Returns 2
countTimesNumberAppears(123, 8);  // Returns 0
countTimesNumberAppears(0, 0);    // Throws IllegalArgumentException
```
<br></br>

2. Write a function called ``binaryTreeEvenSum`` that takes in a ``BinaryTree<Integer>`` and returns the sum of the even values of the BinaryTree.
Make sure you include ``import cs125.trees.BinaryTree;`` above your code.
Here are some text cases: 
```java
System.out.println(binaryTreeEvenSum(new BinaryTree<>(2, 6, 6)));  // Prints 14
System.out.println(binaryTreeEvenSum(new BinaryTree<>(2, 6, 5))); // Prints 8
System.out.println(binaryTreeEvenSum(new BinaryTree<>(2)));      // Prints 2
```
<br>
Feedback: https://forms.gle/yJLaYFaBtthPf3AP6 <br>
