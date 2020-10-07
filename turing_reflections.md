# Turing Journal Reflections

---

### Mod 1 - Week 1

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
