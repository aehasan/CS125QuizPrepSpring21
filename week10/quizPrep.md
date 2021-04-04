# Week 10: <br> 
**Disclaimer: This document is meant to supplement other studying materials, not replace them**<br>

### Concepts
   * Linked Lists
   * Array Lists
   * Asymptotic run time
   * Exams are cumulative. You should have a strong understanding of past material(References, Polymorphism, etc.). If not, ask for help!
   
   If you need more practice with interfaces and abstract classes & methods, go to the EMP site: https://cs199emp.netlify.app/dist/s21/2021-03-19.html#1
   
   You can use a code playground on the CS 125 website to follow along and test the code! https://cs125.cs.illinois.edu/

# Conceptual Check
<br>


What is the Big-O run time of get in a Linked List as opposed to an array-list. Do you get why?<br>

What is the Big-O run time to insert at the beginning or end of a linked list? How about an array list? Why?<br>

Can you draw out how we would insert something into the middle of a linked list? What index do we need to walk too? <br>

You are given a list that appears to have non-constant times for insert. Which kind of linked list is it? <br>



# Practice Problems
<br></br>

1. Let us modify the existing linked class below. Write a function called ``evenSum`` that takes in the head of another linked list. Go through both lists and sum only the values at even indeces of your list and the other list. You will need to copy the following code into your playground:
```java
public class SimpleLinkedList {
  private class Item {
    private Object value;
    private Item next;

    Item(Object setValue, Item setNext) {
      value = setValue;
      next = setNext;
    }
  }

  private Item start;
  private int size;

  public SimpleLinkedList(Object[] values) {
    assert values != null;
    for (int i = values.length - 1; i >= 0; i--) {
      add(0, values[i]);
    }
    size = values.length;
  }

  public int size() {
    return size;
  }


  public void add(int index, Object value) {
    assert index >= 0 && index <= size;
    
    if (index == 0) {
      start = new Item(value, start);
    } else {
      Item nextItem = start;
      for (int i = 0; i < index - 1; i++) {
        nextItem = nextItem.next;
      }
      nextItem.next = new Item(value, nextItem.next);
    }
    size++;
        
  }
}

```
<br>
An example of how we want this function to work:
```Java
LinkedList j = new LinkedList();
LinkedList f = new LinkedList();
//add some values
j.evenSum(f) // goes through and sums the even values of j and f.
```
<br>
2. Edit the Linked List function above to include an ``insert()`` function that takes two arguments an ``Object value`` and a ``int index``. Assert that the index is of the proper values(for you to figure out) and insert appropiatley.


3. Let us make a new different array-list. In this case``add`` only supports adding to the end of the Array List. And takes in one argument ``Object value`` . After each add instead of create an array that is one bigger, it will create an array that is two times as big every once in a while. Can you see the advantage to this? It will also support ``delete`` which takes in no arguments and deletes an element from the back of the list. Basic starter code is attached below. <br>
```java
public class SimpleArrayList {
  private Object[] list;
  public SimpleArrayList(Object[] arr) {
    assert arr != null;
    list = arr;
  }
  
  public Object[] getValues() {
    return list;
  }
  
  public int size() {
    return list.length;
  }
}
```

4. **Hard** Modify the Linked List code above to override the `isEquals()` method. Two linked lists are equal if they have the same value at every index <br>


Feedback: https://forms.gle/yJLaYFaBtthPf3AP6 <br>







