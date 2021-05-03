# The End

## Concepts
* Algorithm Analysis, Lists, Hashing, Maps
* Trees and Recursion
* Sorting
## Concept Overview 
### Big-O Notation
<details> <summary>Why do we study Big-O notation? </summary>
To understand the behavior of a function when the inputs get really large 
</details>

<details> <summary>T/F An algorithm with a runtime O(logn) is considered faster than an algorithm with a runtime O(n) </summary>
True
</details>
<details> <summary>T/F An algorithm with a runtime O(logn) is always faster than an algorithm with a runtime O(n) </summary>
False</details>

### Linked Lists and Array Lists
<details> <summary>
What is one difference between lists and arrays? <br>
a. Lists can only hold ints while arrays can hold any data type <br>
b. The size of a list can change while the size of an array cannot <br>
c. Each object in a list always contains a pointer to the next object, but this is not the case with arrays <br>
d. There are no obvious differences between lists and arrays <br>
</summary>
Answer: (b). Lists can change in size while arrays cannot. A is simply not true, and c is only true for the linked list implementation of lists, but not all lists.
</details>

What are the runtimes for the following methods in a typical ArrayList implementation? <br>
* get() <br>
* set() <br>
* add() *add at beginning* <br>
* insert() *(insert in middle)* <br>
* remove()
<details> <summary> get() and set() </summary>
Answer: O(1) - get() and set() are both simply array lookups for an ArrayList, and array lookups take constant time
</details>
</details>
<details> <summary> add() and insert() and remove() </summary>
Answer: O(n) - add() and insert() are the same for ArrayLists. add(), insert() and remove() involve copying values of the array into a new array of size length + 1 or length - 1. This copying involves a for loop so takes linear time in the size of the array
</details>

<details> <summary> Linked lists maintain order by linking to a new Item object, each of which contain _______ and  _______. <br>
a. An index, a value <br>
b. A value, an object <br>
c. An index, a reference <br>
d. A value, a reference 
 </summary>
Answer: (d). The Item objects contain the current value and a reference to the next item object. 
</details>

<details> <summary> For which method does LinkedList have a faster runtime than ArrayList? <br>
a. Add (at front) <br>
b. Get <br>
c. Set <br>
d. Insert (anywhere) <br>
 </summary> 
Answer: a.  LinkedList has a time complexity of O(1) for adding an item at the front of the list. This is because adding an item to the front of a LinkedList simply involves moving the start reference. This is constant time. Adding an item at any index of an ArrayList has time complexity of O(n). 
</details>

### Hashing and HashCodes
<details> <summary> T/F Hashing a unique object should result in a unique hash code
</summary>
Answer: True. Definition of hashing. 
</details>

<details> <summary> T/F Hashing the same object multiple times can result in multiple hash codes
 </summary>
Answer: False. You have the same has for each object. 
</details>

<details> <summary> Hashing: When will collisions likely occur? </summary>
Answer: When there are more objects than possible hash codes
</details>

<details> <summary> T/F The hashCode() method is inherited from the Object class  </summary>
Answer: True
</details>

### Maps
<details> <summary> T/F Maps sometimes contain multiple values for the same key
 </summary>
Answer: False: Maps can only contain one value for each key
</details>

<details> <summary> T/F Map keys and values can be any object, but not a primitive </summary>
Answer: True: Map keys and values can only be Objects. If you want to use a primitive, just use the object representation of that primitive (e.g., int → Integer).
</details>

### Catching Exceptions
<details> <summary> T/F You can have multiple catch blocks in a try-catch statement </summary>
Answer: True
</details>

<details> <summary> T/F You can have multiple try blocks in a try-catch statement </summary>
Answer: False
</details>

<details> <summary> T/F If any of the catch blocks execute, the code following the try-catch statement will not execute </summary>
Answer: False - this is the point of the catch blocks, they make sure your program doesn’t simply quit if an exception is encountered 
</details>

<details> <summary> T/F If an exception is thrown and not caught, the code following the try-catch statement will not execute </summary>
Answer: True - your code will not execute and it will be as if the try-catch statement wasn’t there at all
</details>

### Recursion
<details> <summary> What are the characteristics of recursion (think: three things you need) </summary>
Answer: base case (smallest possible input), recurisive case (defining function in terms of itself), must change it's state and move towards base state 
</details>

<details> <summary> What is the purpose of having a “main” method and a “helper” method in recursion? </summary>
Answer: The main method is called by the user to solve the problem. If there is also a helper method, no recursion is done in the main method. It is usually used to “set up” the problem for recursion, for example: creating helpful data structures, or throwing exceptions for certain cases that cannot be handled by recursion. The helper method is the recursive one. It is called by the main method and usually is private. 
</details>

### Tree Runtimes
<details> <summary> You have a tree of n nodes and you have to search through the entire tree for a value. What is the runtime? </summary>
Answer: O(n). Look at every node 
</details>

<details> <summary> You have a tree of n nodes and you have to search through the entire tree for a value. What is the runtime? </summary>
Answer: O(n). Look at every node 
</details>

### Sorting Algorithms
<details> <summary> What is bubble sort? </summary>
Answer: starting at first element go through array an compare pairs of values and swap if needed. then repeat starting at the second element. repeat this all the until second to last element. 
</details>

<details> <summary> What is bubble sort best case and worst case? </summary>
Answer:  Best case is an already sorted array (O(n)). Worst case when a value is in the spot furthest from where it should be ((O(n^2)).
</details>

Evaluate the runtime: <br>
```java
public void f(int n) {
  for (int i = 0; i < n; i ++) {
    for(int j = i; j < n; j++) {
      for (int z = j; z < n; z++) {
        break
      }
    }
  }
}
```
```java
public void z(LinkedList j, int n) {
  int f = j.get(n);
  int l = j.get(n + 1);
  for (int i = 0; i < n; i++) {
    int oop = j.get(i);
  }
}
```
Determine the best implementations: <br>
I want to store info in an Array-Like data structure. I expect to be reading from the data-structure more then I am writing to it. <br>
I have stored info in an unkown List. It appears that calls to getItem are not constant. What kind of List is this? <br>
I want to implement a sorting algorithm in O(nlogn) time. Which one should I use. <br>

Describe the sorting algorithm and identify a worst input if any: <br>
Insertion Sort <br>
Merge Sort <br>
Quick Sort <br>






## Concept Overview and Practice
1. Practice Exam
2. Given a tree or a linkedlist of objects map the number of times each object appears in a Map<Object, Integer>
3. Open Problem session
## Shameless Plug
1. Please leave some feedback in the feedback form. The semesters over so if you wanna leave some constructive criticism please do!
2. Maybe become an assistant next semester?!
