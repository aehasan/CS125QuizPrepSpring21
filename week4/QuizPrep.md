# Week 4 Quiz Prep

Bad news: *Midterm* coming that combines all the stuff from this unit.

Good news: No weekly voices

### Concepts

* Strings
* Algorithms
* Asserts
* Null safety
* Arrays and multidimensional arrays
* Functions
* Loops
* Conditional expressions
* Variables and types

### Make sure to go over previous quiz reviews

* [week 3 quiz prep](https://github.com/ranchncarrots/CS125QuizPrepSpring21/blob/main/week3/QuizPrep.md)
* [week 2 quiz prep](https://github.com/ranchncarrots/CS125QuizPrepSpring21/blob/main/week2/quizPrep.md)
* [week 1 quiz prep](https://github.com/ranchncarrots/CS125QuizPrepSpring21/blob/main/week1/quizPrep.md)

### Useful EMP

* [Feb 19: Assertions, Do-While Statements, Switch Statements, and More Multidimensional/String Problems](https://cs199emp.netlify.app/dist/s21/2021-02-19.html)
* [Feb 16: MORE Multidimensional Arrays, MORE Strings and String Functions, and null](https://cs199emp.netlify.app/dist/s21/2021-02-16.html)
* [Feb 12: Multidimensional Arrays, Strings and Algorithms, and More Functions ](https://cs199emp.netlify.app/dist/s21/2021-02-12.html)
* [Feb 9: Function Overloading, Void Return, Strings](https://cs199emp.netlify.app/dist/s21/2021-02-09.html)
* [Feb 5: Algorithms, Functions, While Loops, and Error Types](https://cs199emp.netlify.app/dist/s21/2021-02-05.html)
* [Feb 2: Compound Conditional Statements, Arrays, and For Loops](https://cs199emp.netlify.app/dist/s21/2021-02-02.html)
* [Jan 29: Variables/Datatypes, Operations on Variables, and Conditional Statements and Expressions](https://cs199emp.netlify.app/dist/s21/2021-01-29.html)

### Practice Midterm
* [Practice Midterm](https://cs125.cs.illinois.edu/quizzes/)

## Weightage

The midterm/exam actually has the same weight as each quiz, but it has a month worth of content. It is the same format as the quizzes; it is just cumulative. 

## Concept Overview: Errors 
* Checkstyle errors: You wrote some code that was not up to our beauty standards.
* Compiler/syntax errors: You wrote something that Java does not understand. 
  * ex: system.out.pritnln
* Runtime errors: Java doesn’t notice any issues at first, but once the code is running, something goes wrong
  * ex: loops that don’t end, array index out of bounds
* Testing errors: Your code didn't accomplish its task.

## Conceptual questions 

1. Lets say you have a function `int factorial(int n)` but you realize that factorial doesn't not work for negative numbers. How will you add an assert statement to verify this?

2. Does type inference make mistakes? What are the pros and cons of using it?

3. What happens if we don't check for `null`? 

4. What data types can be `null` and what can't?

5. How is a `String` different from a `char[]`?

6. How can we make a 4d array of doubles with dimensions 10x50x5x2?

7. When to use `.length` and when to use `.length()`?
8. When to use `==` and when to use `.equals()`? 

## Reading documentation

In the quizzes you can't use the general internet unlike when doing homework. This is to ensure that no one directly looks up all the basic level questions online. 

However, we don't want this class to be a memorize fest, so we allow the official `Java` documentation by the makers themselves. Learning how to read documentation is an important skill and you can watch Geoff's video on it [here](https://cs125.cs.illinois.edu/lessons/Spring2021/015_strings#strings-as-objects).

For the midterm you get access to the [String](https://docs.oracle.com/en/java/javase/14/docs/api/java.base/java/lang/String.html) documentation. 

For each, use the documentation _only_ to figure out how to do the following and which function will you use:

1. Check if a String `name` contains `"125"` inside it.

2. Split a String `phoneNumber` based on `"-"` in the middle.

3. Convert a string `courseName` to lower case.

## Combining it all together!

_(NOTICE: background story not necessary for the practice, you can jump right to **To solve**)_

You are a code bricklayer at &#x03BB;alve&#x00AE; doing some tedious data analysis job. Every day your boss GabeN electronically throws a pile of unprocessed csv data files  at you, and if you don't finish compiling them by the end of the day, you know you are done. Well, job is easy, life  is tough.

Today however, GabeN is particularly mean and he gives you a single txt file unprocessed to the point that it is like from the stone age. The file contains this week's game sales and is very important to Lord GabeN. You decide to load the file and it appears as a single String looks like this.
```java
String sales = """
Call Of Coding CXXV,6.67,3.2
Computer-Science: Good Overloading,3.44,-5.5
Float Guys,10.56,68.2
Data 2,0.0,0.0""";
```
You recognize that each line is a game and for each line, the three fields separated by commas are

  > _name, sales(million dollars), percentage change(%)_

##### 1. Parsing the sales
 * **To solve**: You need to parse the sales by line and store them in an array of String (don't worry about parsing each field within a line yet!). What would you do?

##### 2. Check for errors
Dave somehow gives you a cleaner copy of this week's sales. He clearly wants you to check whether there exists errors on the reporting numbers. You dare not ask GabeN why he gives you the unprocessed file while there exists a cleaner one.

You decide to store the cleaner copy in the same format as yours with the follow code. **For your convenience, Dave preserves the order of games so you won't mess up**.
```java
String[] refSales = getDavesCopy();
```
  * **To solve**: Write a function _checkErrors_ that takes two String arrays as parameters and compares both the sale number and the percentage change. If there is any error, report **false**, otherwise report **true**.  (_hint: comparing two Strings str1 and str2, you should use str1.equals(str2)_)


##### 3. Report to GabeN
  * **To solve**: Write a function _report_ to translate each sale to a sentence describing its status and print it out. The function should return **void**. The translated sentence should look like this:
  ```bash
  [Game Name] total sale is $[sale number] mil. Comparing to last week, it changes [percent change]%.
  ```


