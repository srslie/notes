# Ruby Notes

To comment in Ruby:
``` #=> ```

## Data Types

Data types are called Classes, and specific variables are instances of that class or a classes

 Object:
  - 4 is an instance of the Integer class.
  - 4 is an Integer object

Integers are whole numbers without decimals, negative or positive, can have underscores for readability instead of commas

floats are numbers with decimals.

## Variables

Varibles are declared 

``` example_var = 455```

Variables can hold any datatype and switch (dynamic typing) when reassigned

Local Variables must
 - start with a lowercase Letter
 - only contain letters, numbers, and underscores
 - use snake-case (all lowercase with _ between)

## Numbers

For integers:

``` 
+ addition
* multiplication
% modulo
/ division
#even? (method)
#odd? (method)
== equality
<= less than or equal to
>= greater than or equal to
!= not equal
```

for floats:

```
#round (method)
4.0 == 4
```

## Strings

Any characters with double or single quotes, so long as they match

```
Methods:
#length
#chars
#upcase
#downcase
#capitalize

Interpolation:
name = "Gary"
"My name is #{name}"
#=> "My name is Gary"
```
Interpolation can be used with any integer, value, or expression.

Concatonation is done using ```+```

Substrings can be referenced by index (starting at 0-index), going to whatever index from beginning or end
```
alphabet = "abcdefg"
alphabet[0] 
#=> "a"
alphabet[0..3]
#=> "abcd"
alphabet[3..-1]
#=> "ef"
```

## Changing Data Types

It's tricky to do this as the results can be finicky and hard to get errors; avoid if possible.

```.to_f``` change to a float
```.to_i``` change to an Integer
```.to_s``` change to a string

```
"a string!".to_i
#=> 0
"15 cows".to_i
#=> 15
" 4".to_f
#=> 4.0
"_4".to_f
#=> 0.0
```

## Arrays

Ordered lists, separated by commas, held in [square brackets]

Can hold any number of elements, or be empty, and elements can be any data type, and mixed

Mixed data types (tuples, in some languages) can be harder to work with; avoid if possible.

Methods:
```
array[0]
length/count/size
push/pop
shift/unshift
delete_at
insert
join
```