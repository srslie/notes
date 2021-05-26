Javascript Notes
================

## Table of Contents:

  * [Overview] (#overview)

  1. [Data Types](#dataTypes)
  2. [Functions](#functions)
  3. [Conditionals](#conditionals)
  4. [Loops](#loops)
  5. [Objects](#objects)
  6. [Methods](#methods)

  * [Glossary](#glossary)

## Overview <a name="overview"></a>
Javascript is an object-oriented language and was originally made for the web, so it's generally used for websites and is compatible and carried by most internet browsers instead of having to be downloaded or compiled like many languages. But it can do anything a full language can do. There are different versions

One process for technical challenges-
- Read the prompt
- READ IT AGAIN, out loud if you are comfortable
- Write down the overall goal as you understand it
- in your words- Write down your input (what data type is it?, what else do you notice?)- Write down the output (what do they want back? What data type? How is it formatted?)- Write down any questions I have about the prompt- Then start my pseudocode- - What's the first thing I need to do?- - What data do I need? What type is it? Where does it live?- - Are there any conditions I'm checking for? - - identify any sticking points, and try to break them into individual googles- - etc etc

## Scope

Javascript is read by each browser's different JavaScript Engine or RunTime Environment.

Javascript is read line by line  in the order they're written.

It is a single-threaded language, meaning, it must finish executing each line of code before it moves on to the next: only one task is executed at a time.

Variables used in functions must be declared and assigned to the value you want used before the function that uses them runs. While any declared variable name gets hoisted, the assignment of its value stays wherever it was written.

Function declarations are special and get hoisted.
```
function example() {
  do this
};
```

Function expressions are treated more like variables and do not.

 ```
 var example = () {
   do this
 }
 ```
Hoisting and Creation Phase
-

Execution stack follows the First-In-Last-Out (FILO) semantics. Once a function is created, the execution context is pushed to the stack. Once the function has returned, the call is popped off the stack

## Data Types <a name="dataTypes"></a>

Primative:
- string
- boolean
- number (float or integer)
- null
- undefined
- Symbol

these are immutable (cannot be altered), are not objects (have no methods)

Complex:
- array
- object
- function

Use typeOf() to find out what type it is

Dynamic vs Static: dynamic types can change as you put it in, but static you have to explicitly state the type of data and it cannot changes

JS uses duck typing

Type Coercion

`+bool` converts the Boolean to an integer. false = 0, true = 1.


Multidimensional array

 Array = [ [

{key: pair if I want}{bitch}{yeah}],

[{moreodat}],

...

]
## Functions <a name="functions"></a>

Variadic functions are functions that support varying numbers of arguments. (arity: the number of arguments or operands taken by a function or operation in math, also called adicity and degree in logic or philosophy or valency in linguistics--fun fact)

rest parameters are sorta 'all the rest' parameters, it allows you to use the spread syntax (...) to imply that there are an indefinite number of parameters that could be optionally added to the function call

its 
```
function myFun(a,  b, ...manyMoreArgs) {
  console.log("a", a)
  console.log("b", b)
  console.log("manyMoreArgs", manyMoreArgs)
}

myFun("one", "two", "three", "four", "five", "six")

// Console Output:
// a, one
// b, two
// manyMoreArgs, ["three", "four", "five", "six"]
```

There are three main differences between rest parameters and the arguments object:

- The arguments object is not a real array, while rest parameters are Array instances, meaning methods like sort, map, forEach or pop can be applied on it directly;
- The arguments object has additional functionality specific to itself (like the callee property).
- The ...restParam bundles all the extra parameters into a single array, therefore it does not contain any named argument defined before the ...restParam. Whereas the arguments object contains all of the parameters -- including all of the stuff in the ...restParam -- unbundled.

## Conditionals <a name="conditionals"></a>

## Loops <a name="loops"></a>

## Objects <a name="objects"></a>



## Methods <a name="methods"></a>

String.seach(YOUCANUSESEDSYNTAXHERE)

Example.search(/Alice) or (/^A)  

### Array Methods
push
pop
unshift
shift
slice
splice
includes
concat

### localStorage Methods

localStorage.setItem(); takes two arguments—a key and value (key must be string)—and stores the given value under the provided key.
localStorage.getItem(); gets an item from storage based on the key provided.
localStorage.removeItem(); takes a key and removes that key and its associated value from storage.
localStorage.clear(); removes all items from storage for that domain.

### JSON methods

JSON.parse

## Glossary <a name="glossary"></a>

* Data Type A kind of data, defined by the values it can hold and the operations that can be done on it

* Primitive type A kind of data type. Primitives in Javascript are [string, number, boolean, null, undefined, symbol]. Also know as a simple data type

* Variable A container for a value. The main building block for all programming

* Declare Creating a new variable (distinct from assignment)

* Assignment Assigning a value to a variable

* Concatenation The binding of multiple strings together using the + string operator

* Interpolation The process of injecting a variable directly into a string.

* Template literal Template literals are string literals that provide an easy way to interpolate a variable or expression into a string.

* Operator Symbols that are used to assign, compare, and perform operations

* Statement A single piece of code that accomplishes one task or action

* Expression A statement that produces a value

* Conditional An expression that evaluates to true or false, or a control flow statement that executes code

* Function A predefined and reusable group of behavior

* Declare/Define The initial writing of a function
Call/Invoke Running a function

* Parameters The variables declared when a function is declared/defined

* Arguments The variables passed to a function when it’s called/invoked

* Literal A way of declaring a data structure and its values at the same time

* Array Used to store a collection of data items/multiple values under a single variable name

* Element A single item stored in an array. An element can be of any data type.

* Bracket Notation How we access individual elements of an array. Either to express the element, or assign a new element.

* TDD Test Driven Development / Design
Assertion An expression containing some testable logic

* Assertion Library A package of assertion functionality. Usually distinct from a Testing Framework

* Testing Framework A library that determines how tests are organized and executed

* Red/Green Testing - a workflow for testing your code, in which we write and fail tests (red) before we write any implementation code to pass the test (green)

* Array Used to store a collection of data items/multiple values under a single variable name

* Element A single item stored in an array. An element can be of any data type.

* Loops A quick and easy way to do something repeatedly

* Control Flow The order in which the computer executes statements in a script. The order of execution can change whenever the computer runs across the (extremely frequent) structures that change the control flow, such as conditionals and loops.

* Bracket Notation How we access individual elements of an array. Either to express the element, or assign a new element.

* Array Prototype - methods that are built specifically for arrays. They help us change the arrays themselves or get certain information out of them.

* Mutator - methods that mutate, or change, the original array

* Accessor - methods that do not mutate the original array, rather just give us some information about the array

DOM - Document Object Model, the JS interface used to interact with HTML
interface - a shared boundary across which two separate components exchange information.
node - a basic unit of a data structure; often contains data and is linked to other nodes
tree - a basic structure that describes relationships between pieces of information (nodes); composed of related nodes in an organized structure

TDD Test Driven Development / Design
Assertion An expression containing some testable logic
Assertion Library A package of assertion functionality. Usually distinct from a Testing Framework
Testing Framework A library that determines how tests are organized and executed
Red/Green Testing - a workflow for testing your code, in which we write and fail tests (red) before we write any implementation code to pass the test (green)

pseudocoding Literally, fake code! Writing out steps to solve a problem or achieve functionality, without writing actual code
terms of art Technical vocabulary, the words and terms that accurately describe code
eustress Beneficial stress; the motivating sensation of discomfort that occurs when you don’t know something, which compels you to figure it out (different from distress, which paralyzes)

Event Handlers Functions that will run when an event happens
Event Propagation Roughly, the order in which different DOM elements are notified of an event
Event Capturing Part of the event propagation model wherein listeners are fired from the top the DOM tree, down
Event Targeting Part of the event propagation model wherein listeners are fired on the source of the event
Event Bubbling Part of the event propagation model wherein listeners are fired from the target of the event, up
Event Delegation The process of using event propagation to handle events at a higher level in the DOM than the element on which the event originated

Client-side Storage Storage on the client (usually the browser)
Server-side storage Storage on the server
localStorage An implementation of Client-side Storage
JSON (JavaScript Object Notation) a syntax for serializing objects, arrays, numbers, strings, booleans, and null

## MOD 2 - Lessons Glossary
Data Type A type of data, e.g., String, Object, Boolean, etc.
Primitives / Simple Data Types Basic data types like String, Boolean, Number
Complex Data Types Data types that are not Primitives. E.g., Objects, Arrays
Object A data structure made up of Keys and Values
Key The name used to refer to a Value in an Object
Value The value referenced by a Key in an Object
Array A list of values
Function A grouping of executable code. Can be manipulated just like any other Object
Method A function that’s defined as a property of an object
Scope Where variables are accessible
Parameters The variables a function says it will take in when it runs. Declared inside parens
Arguments The actual variables a function uses when it runs

TDD Test Driven Development / Design
Assertion An expression containing some testable logic
Assertion Library A package of assertion functionality. Usually distinct from a Testing Framework
Testing Framework A library that determines how tests are organized and executed
Red Green Refactor The process of writing a failing test, making it pass, then refactoring the tests and/or implementation with confidence
Test Phases A test that is organized into the phases [Setup, Execution, Assertion, Teardown*

JavaScript Engine/Interpreter A program that executes JavaScript code. Most commonly used in web browsers
Hoisting The process of implicitly moving the declaration of variables and functions to the top of their scope
Creation Phase The phase where the interpreter sets aside some space in memory to store any variables and functions we might need access to.
Execution Phase The phase where the interpreter executes Javascript code, line-by-line.
Execution Call Stack A tool (data structure) for the interpreter to keep track of its place in a script that calls multiple functions


