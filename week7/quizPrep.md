# Week 7: <br> 
**pog: PolymOrphismisGreat**<br>
**Disclaimer: This document is meant to supplement other studying materials, not replace them**<br>

### Concepts
   * Everything covered last week has a high likelihood of being on an exam
   * References and Polymorphism
   
   You can use a code playground on the CS 125 website to follow along and test the code! https://cs125.cs.illinois.edu/
   

# Conceptual Check
<br>


What is the difference between reference equality and object equality. How are they called?<br>
When a function takes in an object what is it really taking in?<br>
```java
void one(FillerObject o) {
  o.addOne();
}


void one(Int i) {
  i++;
}
```
What do arrays of objects store? Do you understand the behavioral implications when compared to numbers? See the example below<br>
```java
class Basic() {
  int i = 0;
  void incrementI() {
    i++;
  }
  Basic example = new Basic[4];
  //At this point we have created an array of what? Have we created ANY person objects.
  
  for(int i = 0; i < example.length; i++) {
    example[i] = new Basic();
  }
  //How many objects are in example?
  //what if i did:
  Basic holder = new Basic();
  for(int i = 0; i < example.length; i++) {
    example[i] = holder;
  }
}
```
Do you understand the idea of making shallow and deep copies of the array shown above?
**Quiz Prep: Design a class that uses both static methods and variables**

# Practice Problems
<br></br>
1. Here is a book class: <br>
```java
public class Book {
  //make sure these are private on the exam 
  public String author;
  public String title;
  public int pageNumbers;
  //constructor is obviously public
  public Book(String setAuthor, String setTitle, int setPageNumbers) {
    author = setAuthor;
    title = setTitle;
    pageNumbers = setPageNumbers;
  }
}
```
Create a class that extends the book class in any way you see fit. Have a bookshelf that stores an array of Book objects. Downcast the book object to unlock the unique properties of the class you created. <br></br>
2. Define a copy constructor for the Book object above. Your copy constructor should take in one book object. Create an array of only book objects and use it to create a new array with deep copies. <br></br>
3. Create a Pet class with a method ``getType`` that returns the String "Pet". The pet class also has a method ``noise`` that returns a string, in this case ``null``. Create a class ``Dog`` that extends ``Pet``. ``Dog`` overrides ``getType`` and returns the String ``Dog``. Dog also has its own method ``Bark`` that takes in no arguments and returns the String ``Woof``. <br>
Then try out:<br>
```
Pet j = new Dog();
j.getType();
j.Bark();
```
FeedBack: https://forms.gle/yJLaYFaBtthPf3AP6 
  





