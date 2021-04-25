
# Quiz Prep Week 14 

### Concepts
* [Bubble Sort](https://cs125.cs.illinois.edu/lessons/sorting/#bubble-sort)
* [Insertion Sort](https://cs125.cs.illinois.edu/lessons/sorting/#insertion-sort)
* [Merge Sort](https://cs125.cs.illinois.edu/lessons/mergesort/)
* [Quick Sort](https://cs125.cs.illinois.edu/lessons/quicksort/)
* [Binary Search](https://cs125.cs.illinois.edu/lessons/binarysearch/)

### EMP Session Links 
* [EMP 11-17](https://cs199emp.netlify.app/dist/2020-11-19.html)

### What is the runtime complexity of the following algorithms
* Bubble Sort <details> <summary> </summary> O(n^2) </details>
* Insertion Sort <details> <summary> </summary> O(n^2) </details>
* Merge Sort <details> <summary> </summary> O(n*log n) </details>
* Quick Sort 
  <details> <summary> Best Case </summary> O(n*log n) </details> 
  <details> <summary> Average Case </summary> O(n*log n) </details> 
  <details> <summary> Worst Case </summary> O(n^2) </details>


### Concept Overview and Practice

1) Create a public class named Sorter and add the following functions
  
  a) Create a static method named bubbleSort, that takes in an array of Comparables and sorts them using bubble sort and returns the sorted array. 
    <details>
   <summary>Spoiler!</summary>

   ```Java
   public class Sorter {
    
    public static Comparable[] bubbleSort(Comparable[] arr) {
      int n = arr.length; 
      for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
          if (arr[j].compareTo(arr[j + 1]) > 0) { 
            Comparable temp = arr[j]; 
            arr[j] = arr[j + 1]; 
            arr[j + 1] = temp; 
          } 
        }
      }
      return arr;
    }
 }
   ```
  </details>
  <br></br>
  
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

2) Given a sorted array of Comparables, and a Comparable object as inputs, write a function binarySearch that returns the index of the object in the array. If the object is not present in the array, return -1. If the array is null or empty, or if the object is null also return -1
  <details>
   <summary>Spoiler!</summary>

   ```Java
  int binarySearch(Comparable[] arr, Comparable x) {
    if (arr == null || arr.length == 0 || x == null) {
      return -1;
    }
    int left = 0;
    int right = arr.length - 1;

    while (left <= right) {
      int mid = left + (right - left) / 2;
      if (arr[mid].equals(x)) {
        return mid;
      }
      if (arr[mid].compareTo(x) < 0) {
        left = mid + 1;
      }
      if (arr[mid].compareTo(x) > 0) {
        right = mid - 1;
      }
    }
    return -1;
  }
   ```
  </details>
  <br></br>
  
  
### Helpful Videos on
* [Bubble Sort](https://www.youtube.com/watch?v=xli_FI7CuzA)
* [Insertion Sort](https://www.youtube.com/watch?v=JU767SDMDvA)
* [Merge Sort](https://www.youtube.com/watch?v=4VqmGXwpLqc)
* [Quick Sort](https://www.youtube.com/watch?v=Hoixgm4-P4M)


