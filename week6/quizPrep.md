# Week 6: <br> 
**pog: PolymOrphismisGreat**<br>
**Disclaimer: This document is meant to supplement other studying materials, not replace them**<br>

### Concepts
   * Static
   * 
   ```Java
   class CoolSkills;
   class Coding extends CoolSkills;
   class Java extends Coding;
   class Polymorphism extends Java;
   ```
   
   You can use a code playground on the CS 125 website to follow along and test the code! https://cs125.cs.illinois.edu/
   

# Conceptual Check
<br></br>

Story Time: What happens when we cast? <br>
One day Timothy woke up and went "Wow I want to ~~be misterable~~ challenge myself today" so he decided to learn how to cast objects in Java. Timothy made a couple of classes documented below: <br>
```java
public class Shape {
  String type;
  double area;
}

public class Triangle {
 int sideOne;
 int sideTwol
 int sideThree;
}

public class Square {
 int squareSideOne;
 int squareSideTwo;
 int squareSideThree;
 int squareSideFour;
}
```
Wow Timothy thought. I am so smart. As a CS major Timothy has only one friend, the compiler. Timothy likes the compiler because he does whatever Timothy wants.<br>
Timothy waltz's up to the compiler and reads off this line: <br>
``Shape waitWhat = new Square()`` <br>
**Do you know what is going on here**<br>
Wow the compiler thought, what a useless thing to do. But as the compiler he listened anyway. Timothy then tells the compiler to: <br>
``waitWhat.squareSideOne``<br>
**Do you know what will happen**<br>
The compiler doesnt know what to do. Even though the compiler is holding a square it is told to think of it as a shape. The compiler feels confused and doesnt know what to do. So it spits out some useless jargon. Timothy is confused. He feels forsaken, and goes to bed. That night Timothy had a wonderful dream about a place where CS majors congregate. It was called Stack Overflow. Timothy wakes up and rushes to his computer, and learns some new tricks. Do you understand the following<br>
``waitWhat instanceof Sqare``<br>
``Square postCast = (Square) waitWhat``<br>
Timothy has solved his problem. The End.

FeedBack: https://forms.gle/yJLaYFaBtthPf3AP6 
  




