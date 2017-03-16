##code review
### namespacing
- keeping functionality for one part of the model of a program (Article) as properties/method on a constructor. This avoid poluting the global scope with lots of variables/function names, it only introduces the name of the constructor. also organizes the code by functionality and keeps methods that apply to all instances together. Things that are made to act on just one instance should be on the prototype of the constructor instead. 

### Functional Programming
- Why:
  - Effects + Logic = Side effects
  - cleaner code
    - easier to read, modify and debug
  - Getting the same output for a given input. 
- What;
  - Immutability and Mutability (strings, numbers)
    - cant change after set. Fancy way to say changeable or not. ex: array methods .forEach, filter, slice) that don't change original array. Array methods that change(sort, reverse, splice)
  - Declarative vs. Imperative code
    - describe what you want (declarative)
    - how, the steps to get it done (imperative)
  - stateless (pure) function - consistently get the same output for a given input every time.
  - first-class functions - passing functions into other functions and taking functions as values. functions are objects and can be used like objects.
  
  - Array methods:
    - forEach(function(<each item in array>){})
      -call the function for each item in the array
    - map(function() {})
      - creates new array with results from function in it.
    - filter(function(){})
      - take condition in function and checks if it is truthy/falsey for each item and returns items that are true.
    - reduce(function(acc<value that gets changed with every pass through new item>, curr<current item>){}, 0<starting value of accumulator>)
      - goes through each item and runs function that can accumulate a value based on each pass through item and also has current item functionality.
    - You can chain these together.
    