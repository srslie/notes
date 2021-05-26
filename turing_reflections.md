# Turing Journal Reflections

---
### Mod 1 - Week 4

**What is the difference between inline, block and inline-block?**
  Inline is an element that takes up only the space between the tags. Blocks take up the whole width of the parent element container, and can contain inline elements inside of them. Inline blocks behave like inline elements but have added benefits of being able to style them with height and width fixing like a block.
**List out three elements that are block level by default.**
  <nav>
  <form>
  <p>

  https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements#:~:text=By%20default%2C%20block%2Dlevel%20elements,complex%20set%20of%20content%20categories.

**List out three elements that are inline level by default.**
  <label>
  <img>
  <span>
    https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements
**Write down at least one question you have about the display property for class tomorrow.**
What is the run-in box?
https://developer.mozilla.org/en-US/docs/Web/CSS/display



### Mod 1 - Week 3

We're making people feel included by and large. Interruption seems like the biggest issue. My biases are generally that people will speak up if they need something, so shyer people may get lost. I also don't feel technically behind so people who are struggling more might have a different experience. I should talk less during class to make space, generally let others take the reins when partnering since I know I'll go do it myself later, be better at delegating tasks/learning during group projects, and make more space for others in peer-peer interactions, especially making sure not to interrupt anyone.


On document.querySelectorAll()

**How is this method similar to document.querySelector()?**
  -They both grab/refer to elements of the html that match the css selector that was given as the argument.
**How does it differ?**
  -document.querySelector() only grabs the first matching element from the argument given, the document.querySelectorAll returns all of them.
**What does document.querySelectorAll() return?**
  -returns the node list of all the elements matching or children of the selector given as a argument; it's an object similar to an array, but with some methods. It returns a static node list that occurs once the document.querySelectorAll is called. It can be iterated over used array.forEach and converted into an array using array.from

  Also  has this: who knows what it does? document.querySelectorAll(':scope .outer .inner')

  1. all paragraph elements
  2. the last 2 ps

### Mod 1 - Week 2

**Pseudocoding seems like it slows down the coding process. Why would anyone bother doing it?**
It helps clarify the steps you need to take and the end goal.
**What is a benefit of spending your time pseudocoding?**
It saves time in the long run.
**What are the characteristics of solid, beneficial pseudocode?**
Specific, it uses the terms of art, short and concise lines.
What was helpful about your partners’ pseudocode? What was confusing?
If you were to explain to a non-developer what pseudocoding is, and if you needed to teach them to be able to pseudocode, what would you tell them?


**What is your first reaction to seeing this? Do you want to write code?**
Yes, I just want to write code.
**If you were to explain what to do to a very simple, very literal, very well-meaning, helpful, but silly robot, what would you tell it to do?**
First create a function to iterate through all the elements of the array. In each iteration, create a conditional checking if the length of the string is longer than 5 letters. If the condition is true, splice it out. At the end of iterating, return the array.

Attempt to write some pseudocode!

**What skill do you have that you are proud of? Perhaps a recipe you’re good at, or a sick kick flip on a skateboard, or maybe you’re very good at remembering people’s names, or you play an instrument.**
Reciting some gud pooitry. Keep cat alive using robots! using tablesaw with smaller woods.
**Do you remember what it was like when you first began learning the skill?**
I was bad and it was hard and sometimes demotivating. I kept fucking up and having to restart. Not the cat thing.
**Although it may feel easy now, or like something you’ve always been good at, push yourself to describe the work you had to put in to achieve proficiency!**


**How would you describe HTML to someone who has never heard of it before?**
Skeleton and content of a webpage.
**What is an HTML attribute and why would you use one?**
**Why is it important to be consistent with your use of white space and indentation when writing HTML?**
**What is the purpose of semantic HTML?**
**What questions do you still have about HTML?**
### Mod 1 - Week 1

**What is your understanding of why testing is important**

It's important as a safety net, making sure everything works as intended. It also makes for better code so that is decoupled (chunked for readability and functionality) and hopefully on target for a desired output.

**What are the steps of TDD?**
  1. Think and write tests
  2. red - try to run the test, fail
  3. green - write the code to pass test
  4. green - make sure no old tests fail
  4. green - refactor and pass all tests
  5. repeat

**What are the benefits to testing your code?**
**What is the Red/Green testing workflow? Why do we use this process?**
**What is Mocha? What is Chai? Write an example of the code that comes from Chai.**
**How do we export something from a file for testing?**
**How do we import something into another file for testing?**

What is your understanding of why testing is important?
Explain the steps of TDD in your own words.

**To start, go ahead and make an object or two.**
```
  var bed = {
    size: 'full',
    made: false,
    brand: 'Bear',
    sleepNumber: 4
  }

  var cow = {
    name: 'Gerry',
    breed: 'normal cow',
    age: 24
    favoriteSpots: ['under the tree', 'in the meadow']
  }
```
**How do you create an object using literal notation?**

  You use key-value pairs to denote the properties of the object, with the (keyName, colon, value,) and commas after each pair and wrapped in the curly braces:
```
  var objectName = {
    key: 'pairValue',
    key1: 12,
    key2: false,
    key3: ['example', 'array']
  }

```
**What is an object and what is it made up of?**

  An object is a data type used to store key-value pairs, or properties, and function to be used on those properties, or methods.

**When we assign a function as the value of a key inside an object, what do we call it?**

  We call it a method.

---

**What is a statement?**

  A statement is an individual instruction that the computer can follow, often best followed by a semicolon.

**What is an expression?**

  An expression is a statement that produces a single value. Often the result of operators acting some modification on a value or values to create a single output.It produces a single value, so it can be written wherever a value is expected (like in template literals).

**Give examples of both.**

A statement could be:
```
  'string';
  42;
  console.log('hi');
```

An expression could be:
```
  4 + 4;
  var cat = 'Gravy';
  3 < 5;
```
**Has your understanding of the differences between statements and expressions changed at all?**

  Yes, all expressions are statements but only some statements are expressions. Because an expression returns a value, it can be used in place of a value within code.

**What questions remain?**

  What are all the possible places you can use an expression value?

**Where might you ask that question?**

  Google. Stack Overflow. The Slack for our cohort. Class.

---

**What are the five primitive data types we learned about today?**

  1. boolean
  2. undefined
  3. null
  4. number
  5. string

  6. symbol (didn't learn about it today)

**How are variables useful and what is an example of one that has a value assigned to it?**

  Variables are useful as placeholders for values or operations you want to reference later or in other code, and you don't want to type out the information each time. An example is:```var cat = 'Gracie'```

**Write out an example of string concatenation.**
```
  var num = 3
  'I have ' + num + ' horses!'
```
**Now write that same example using a template literal.**
```
  var num = 3
  `I have ${num} horses!`
```
**Write out the basic structure of an if/else conditional.**
```
  if (condition to be met) {
    if met, complete this action
  } else {
    do this
  }
```
**Write down at least one question you have coming out of this lesson.**

  Why aren't we learning let and const now and using var instead?
