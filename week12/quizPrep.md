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
If the number or the target is less than 0, throw an ``IllegalArgumentException``.
Hint: You can use ``number % 10`` to get the last digit and ``number / 10`` to get rid of the last digit.

Here are some example inputs and outputs:
```java
System.out.println(countTimesNumberAppears(707, 7)); // Prints 2
System.out.println(countTimesNumberAppears(123, 8));  // Prints 0
System.out.println(countTimesNumberAppears(-1, -1));    // Throws IllegalArgumentException
```

<details>
  <summary>Recursion without helper method solution </summary>

  ```java
public static int countTimesNumberAppears(int num, int target) {
    if (num == 0) {
      return 0;
    }
    if (num < 0 || target < 0) {
      throw new IllegalArgumentException();
    }
    int count = 0;
    if (num % 10 == target) {
      count = 1;
    }
    return count + countTimesNumberAppears(num / 10, target);
}
  ```
</details>

<details>
  <summary>Recursion with helper method and passing in count solution </summary>

  ```java
 public int countTimesNumberAppears(int num, int lookingFor) {
    if (num <= 0 || lookingFor <= 0) {
      throw new IllegalArgumentException();
    }
    return helper(num, lookingFor, 0);
}
public int helper(int num, int lookingFor, int count) {
    if (num == 0) { 
      return count;
    }
    if (num % 10 == lookingFor) {
      return helper(num / 10, lookingFor, count + 1);
    } else {
      return helper(num / 10, lookingFor, count);
    }
}
  ```
</details>

<details>
  <summary>Recursion without helper method and without passing in count solution </summary>

  ```java
public int countTimesNumberAppears(int num, int lookingFor) {
    if (num <= 0 || lookingFor <= 0) {
      throw new IllegalArgumentException();
    }
    return helper(num, lookingFor);
}
public int helper(int num, int lookingFor) {
    if (num == 0) {
      return 0;
    }
    if (num % 10 == lookingFor) {
      //System.out.println("one match");
      return 1 + helper(num / 10, lookingFor);
    } else {
      //System.out.println("no match");
      return 0 + helper(num / 10, lookingFor);
    }
}
  ```
</details>

<br></br>

2. Write a function called ``binaryTreeEvenSum`` that takes in a ``BinaryTree<Integer>`` and returns the sum of the even values of the BinaryTree.
Make sure you include ``import cs125.trees.BinaryTree;`` above your code.
Here are some text cases: 
```java
System.out.println(binaryTreeEvenSum(new BinaryTree<>(2, 6, 6)));  // Prints 14
System.out.println(binaryTreeEvenSum(new BinaryTree<>(2, 6, 5))); // Prints 8
System.out.println(binaryTreeEvenSum(new BinaryTree<>(2)));      // Prints 2
```
<details>
  <summary>Solution</summary>

  ```java
import cs125.trees.BinaryTree;
public int binaryTreeEvenSum(BinaryTree<Integer> tree) {
    if (tree == null) {
      return 0;
    }
    int toAdd = 0;
    if (tree.getValue() % 2 == 0) {
      toAdd = tree.getValue();
    }
    return toAdd + binaryTreeEvenSum(tree.getLeft()) + binaryTreeEvenSum(tree.getRight());
}
  ```
</details>
<br>
Feedback: https://forms.gle/yJLaYFaBtthPf3AP6 <br>
