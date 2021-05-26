# Typescript

Resources: https://exploringjs.com/tackling-ts/ch_typescript-workflows.html#the-structure-of-typescript-projects

- transcompile typescript files (.ts) into Javascript via ```tsc``` in the terminal

- Give 'type' annotations to function parameters
  ```
  function myFunc(param1:string) {
  }
  ```

- Set optional parameters 
  ```
  function myFunc(param1?:number) {
    codestuff
  }
  ```

- Set default values
  ```
  function myFunc(param1:string = 'muffins', param2?:number = 3) {
    codestuff
  }
  ```

- Specify return types for functions, including if they don't return anything
  ```
  function myFunc(param1:boolean):void {
    codestuff
  }

  function myFunc(param1:number):number {
    codestuff
  }
  ```

- shows errors when compiling on specific lines or for specific things
  ```
  terminal command: node
  terminal command: tsc
  ```

- assign types to arrays, two different ways ```Array<T>``` or ```type[]```
  ```
  let exampleArray: string[] = ['strings', 'things']
  let otherExample: Array<number> = [1, 2, 3]
  let exampleBools: boolean[] = [true, false, true]
  ```

- empty arrays are valid for any specified type
  ```
  let exampleArray: string[] = []
  let otherExample: Array<number> = []
  let exampleBools: boolean[] = []
  //all would be valid, not compiler errors
  ```

- assign types to nested (multi-dimensional arrays) by stacking ```type[][][]``` as needed, it will ensure all the nested layers are of that type

  ```
  let exampleArray: string[][] = [
    ['strings', 'things'], 
    ['other', 'words']
  ]
  let exampleBools: boolean[][][] = [
    [[true, false], [true, true]],
     true, 
     false
  ]

  let exampleTupleArray: [number, boolean][] = [
    [9, false],
    [10, true],
    [10, false]
  ]
  ```

- **Tuple** an array with elements of different, specific types
  - the types assignment specify the length and orders of the different types and will show errors if either are wrong
  ```
  const exampleTuple: [string, number, boolean, string] = ['Hi', 5, true, 'friend']
  ```
  - tuples are arrays, and have .length property, can use an index, etc. But you can't assign an array to a tuple even if the types match, because Typescript sees it as a fundmentally different 'type'
  ```
  let tup: [string, string] = ['hi', 'bye'];
  let arr: string[] = ['there','there'];
  tup = ['there', 'there']; // No Errors.
  tup = arr; // Type Error! An array cannot be assigned to a tuple.
  ``` 
  - you cannot add additional unaccounted for types to a tuple, it is set to the length explicitly set out when the tuple variable is declared
  - in order to add something to a set tuple, you can concat it to another array and create a more general typed array
  ```
  let tup: [number, number] = [2, 3]
  let nowItsAnArry = tup.concat([3, 4])
  //[2, 3, 3, 4]
  ```
- 
  