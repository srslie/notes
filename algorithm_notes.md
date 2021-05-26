# Algorithm Notes

## Big-Θ Notation

  Refers to a metric of run-time and efficiency, especially regarding solutions that require iterating or sorting.

  Important to know what different functions cost in order to run, especially with a big data set or something that will create an unpleasant delay for a user or other dependent programs.

  Big Θ of N is far better than big O of N squared.

  [khan academy article](https://www.khanacademy.org/computing/computer-science/algorithms/asymptotic-notation/a/big-o-notation)


## Binary Tree

  A data structure of a tree with nodes, where each node has at most two children (hello, binary) that are called left child and right child.

                          1
                   2              3
                4     5        6      7
             8 9    10 11    12 13   14 15

## BFS (Breadth First Search) vs DFS (Depth First Search)

  These search methods are used to for graph traversals and are generally exemplified when thinking of trees (such as the binary tree above).



## Read about google file and bigtable

## Hashing functions and hashtables 

  Generally a more efficient way to access data vs simple arrays

## Quicksort, MergeSort, InsertionSort, BubbleSort

  Sorting data is expensive: time consuming and takes up memory. In order to 


## Coupling vs Cohesion

  **coupling**: the degree to which different aspects rely on each other
  **cohesion**: the degree to which elements are related and belong together

  **view model** tightly couples templates to display logic


  ## GREP

    grep was originally a Unix command-line utility for searching through sets of plain-text data for matches to regular expressions.

    The name comes from the ed command g/re/p (globally search for a regular expression and print matching lines)

    integration, end to end, unit tests 
    used to be a pyramid
    kent dodd testing trophy

    flexbox 1-d plane
    -good for nav bar because it's nav

    grid helps set in x and y axis

    not all one or the other, depends on the problem, right tool for right problem use them as compliments


    authentication vs authorization

    authentication is "are you who you say you are?"

    Authrorization is: are you allowed to do this?

    generators and iterators
    look it up

this and using this
concrete examples

var and let 
how it's hoisted, blocks, etc

currying partially applying a function

popular tools in react and why

redux questions

trending techs
typescript
nextJs, gatsby
boom of react frameworks
spvelt 

Logical nullish assignment (??=)
^coalesing

BIG 0
- look at the time complexity 
- any constants/coeffiencents are factored out, they don't add complexity with scaling, they just are

- addition => multiplication => exponential
- subtraction => division => logarithmic
- so log of N is less than N because essentially it reverse-exponentially gets smaller

linearithmic complexities are much worse than linear, but not by much

polynomial complexities and onward are generally really bad and we want to not

big O, big Omega, big Theta

Complexities LEAST TO MOST:

O(1) - constant time
o(log N) - logarithmic -  binary search
O(N) - linear
O(N log N) - linearithmic - mergesort and quicksort
O(N ^ 2) - polynomial quadrtic - bubble
O(2 ^ 2) - polynomial cubic
O(c^n) - exponential
O(n!) - n factorial

algorithms that are recursive or trees generally depend on degree (the number of nodes coming off another node)

we try to figure out the complexity based on how many times it calls itself, to whatever height (how big the tree is, how deep it goes)

big-o - recursion
- recursion is difficult to an
- if degree=1 then it's just O(height)
- big O(degree^height)


HOW TO GUESS
- to look at the constraints, max input!
- upper bound ^
- lower bound (min input)
  - lowerbound is tricker, theoretical

Space complexity:

- simple variables take up constant space: it's not based on the input

- linear space : copying and slicying parts of array (substrings) cost both time and space

- slicing costs O(N) time and O(N) space where N is the length of the stuff

- if you call a function that returns an input: if it's a copy of that input, so doesn't mutate, that will additionally take up time and space

- recusion takes space
- iterative Depth First Search requires a stack and there is O(N) space

-things that add space 
  - adding elements to a data structure (making an object, etc)
  - copying data structures, including slicing
  - functions that return a new data structure vased on the input
  - recursion

