
# The End

### Concepts
* Algos

### EMP Session Links 
* [EMP 11-17](https://cs199emp.netlify.app/dist/2020-11-19.html)





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



