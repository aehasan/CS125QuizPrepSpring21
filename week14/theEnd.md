# The End

### Concepts
* Algorithm Analysis, Lists, Hashing, Maps
* Trees and Recursion
* Sorting
### Concept Overview 
<details> <summary>Why do we study Big-O notation? </summary>
To understand the behavior of a function when the inputs get really large 
</details>

<details> <summary>T/F An algorithm with a runtime O(n) is faster than an algorithm with a runtime </summary>
True
</details>

<details> <summary>
Lists: What is one difference between lists and arrays? <br>
a. Lists can only hold ints while arrays can hold any data type <br>
b. The size of a list can change while the size of an array cannot <br>
c. Each object in a list always contains a pointer to the next object, but this is not the case with arrays <br>
d. There are no obvious differences between lists and arrays <br>
</summary>
Answer: (b). Lists can change in size while arrays cannot. A is simply not true, and c is only true for the linked list implementation of lists, but not all lists.
</details>

ArrayLists: What are the runtimes for the following methods in a typical ArrayList implementation?
get() <br>
set() <br>
add() *add at beginning* <br>
insert() *(insert in middle)* <br>
remove()
<details> <summary> get() and set() </summary>
Answer: O(1) - get() and set() are both simply array lookups for an ArrayList, and array lookups take constant time
</details>
</details>
<details> <summary> add() and insert() and remove() </summary>
Answer: O(n) - add() and insert() are the same for ArrayLists. add(), insert() and remove() involve copying values of the array into a new array of size length + 1 or length - 1. This copying involves a for loop so takes linear time in the size of the array
</details>

<details> <summary> LinkedLists: Linked lists maintain order by linking to a new Item object, each of which contain _______ and  _______. <br>
An index, a value <br>
A value, an object <br>
An index, a reference <br>
A value, a reference 
 </summary>
Answer: (d). The Item objects contain the current value and a reference to the next item object. 
</details>

<details> <summary> For which method does LinkedList have a faster runtime than ArrayList? Add (at front)
Get
Set
Insert (anywhere)
 </summary> 
Answer: a.  LinkedList has a time complexity of O(1) for adding an item at the front of the list. This is because adding an item to the front of a LinkedList simply involves moving the start reference. This is constant time. Adding an item at any index of an ArrayList has time complexity of O(n). 
</details>

<details> <summary> Hashing a unique object should result in a unique hash code
</summary>
Answer: True. Definition of hashing. 
</details>

<details> <summary>Hashing the same object multiple times can result in multiple hash codes
 </summary>
Answer: False. You have the same has for each object. 
</details>

<details> <summary> Hashing: When will collisions likely occur? </summary>
Answer: When there are more objects than possible hash codes
</details>

<details> <summary> The hashCode() method is inherited from the Object class  </summary>
Answer: True
</details>

<details> <summary> T/F Maps sometimes contain multiple values for the same key
 </summary>
Answer: False: Maps can only contain one value for each key
</details>

<details> <summary> Map keys and values can be any object, but not a primitive </summary>
Answer: True: Map keys and values can only be Objects. If you want to use a primitive, just use the object representation of that primitive (e.g., int → Integer).
</details>

<details> <summary> T/F Catching Exceptions: You can have multiple catch blocks in a try-catch statement </summary>
Answer: True
</details>

<details> <summary> T/F Catching Exceptions: You can have multiple try blocks in a try-catch statement </summary>
Answer: False
</details>

<details> <summary> T/F Catching Exceptions: If any of the catch blocks execute, the code following the try-catch statement will not execute </summary>
Answer: False - this is the point of the catch blocks, they make sure your program doesn’t simply quit if an exception is encountered 
</details>

<details> <summary> T/F Catching Exceptions: If an exception is thrown and not caught, the code following the try-catch statement will not execute </summary>
Answer: True - your code will not execute and it will be as if the try-catch statement wasn’t there at all
</details>

<details> <summary> What are the characteristics of recursion (think: three things you need) </summary>
Answer: base case (smallest possible input), recurisive case (defining function in terms of itself), must change it's state and move towards base state 
</details>

<details> <summary> What is the purpose of having a “main” method and a “helper” method in recursion? </summary>
Answer: The main method is called by the user to solve the problem. If there is also a helper method, no recursion is done in the main method. It is usually used to “set up” the problem for recursion, for example: creating helpful data structures, or throwing exceptions for certain cases that cannot be handled by recursion. The helper method is the recursive one. It is called by the main method and usually is private. 
</details>

<details> <summary> You have a tree of n nodes and you have to search through the entire tree for a value. What is the runtime? </summary>
Answer: O(n). Look at every node 
</details>

<details> <summary> You have a tree of n nodes and you have to search through the entire tree for a value. What is the runtime? </summary>
Answer: O(n). Look at every node 
</details>

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
  int f = z.get(n);
  int l = z.get(n + 1);
  for (int i = 0; i < n; i++) {
    int oop = z.get(i);
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






### Concept Overview and Practice
1. Write a program that given a binary tree and a value find the distance from the root to that value. Hint: This is a good time to use a helper function <br>
2. Write a program that given a binary tree determines if it is full. A tree is full if each node has two children except for leaf nodes.


You should know how to solve these problems <br>
  b) Create a static method named insertionSort, that takes in an array of Comparables and sorts them using insertion sort and returns the sorted array.
    <details>
   <summary>Spoiler!</summary>

   ```Java
   public class Sorter {
     public static Comparable[] insertionSort(Comparable[] arr) {
      int n = arr.length; 
      for (int i = 1; i < n; ++i) { 
        Comparable key = arr[i]; 
        int j = i - 1; 
        while (j >= 0 && arr[j].compareTo(key) > 0) { 
          arr[j + 1] = arr[j]; 
          j = j - 1; 
        } 
        arr[j + 1] = key; 
      }
      return arr;
    }
 }
   ```
  </details>
  <br></br>
  
  c) Create a static method named mergeSort, that takes in an array of ints, and sorts them using merge sort and returns the sorted array. This function also takes in an int start, and an int end. (Hint 1: You are allowed extend the Merge class from lecture to use the merge function, if you want!) (Hint 2: USE RECURSION)
  <details>
   <summary>Spoiler!</summary>

   ```Java
   public class Sorter extends Merge{

    public static int[] mergeSort(int[] arr, int start, int end) {
      if (end - start < 2) {
          int[] res = {arr[start]};
          return res;
        }
        int mid = (start + end) / 2;
        int[] left = mergeSort(arr, start, mid);
        int[] right = mergeSort(arr, mid, end);
        return merge(left, right);
     }
}
   ```
  </details>
  <br></br>

d) Create a static method named quickSort, that takes in an array of ints, an int low and int high inputs and sorts the array using quick sort and returns the sorted array. (Hint: You may need a helper method named [partition](https://cs125.cs.illinois.edu/lessons/quicksort/#HW/71)) (Hint 2: USE RECURSION)
<details>
   <summary>Spoiler!</summary>

   ```Java
   public class Sorter extends Merge{
  
   private static int partition(int[] values) {
      if (values == null || values.length == 0) {
        return -1;
      }
      int pivot = values[0], p1 = 1;
      for (int i = 1; i < values.length; i++) {
        if (values[i] < pivot) {
          if (i != p1) {  
            int temp = values[p1];
            values[p1] = values[i];
            values[i] = temp;
          } 
          p1++;
        }
      }

      values[0] = values[p1 - 1];
      values[p1 - 1] = pivot;

      return p1 - 1;
   }
 public int[] quickSort(int[] arr, int low, int high) {
      if (high == low) {
        return arr;
      }
      int pivot = partition(arr);
      int[] op = quickSort(arr, low, pivot - 1);
      op = quickSort(arr, pivot + 1, high);
      return op;
    }
}
   ```
  </details>
  <br></br>

  
  
### Helpful Videos on
* [Bubble Sort](https://www.youtube.com/watch?v=xli_FI7CuzA)
* [Insertion Sort](https://www.youtube.com/watch?v=JU767SDMDvA)
* [Merge Sort](https://www.youtube.com/watch?v=4VqmGXwpLqc)
* [Quick Sort](https://www.youtube.com/watch?v=Hoixgm4-P4M)



