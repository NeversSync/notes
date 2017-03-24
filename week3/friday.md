## Lecture

- Arrow Functions
  - if one argument, no need for parens. 
  - if only one line of code in braces, no need for braces. If no braces, return is implied. Ideally only use this in replacement of anonymous function. 
  - reduce can be useful to streamline operations where you are searching through a large array for something. If you turn that array into an object with each item as a property, you can then search through the object very efficiently (just one operation) for the desired value/property.
  - context, closures, higher order functions, prototype- the big scary adv. javascript concepts.
  
  ### context
  - this
    - can have different values depending on location.
    - used in the prototype - refers an instance of contructor.
    - used in jQuery, but it is different, it is the normal 'this' being altered by the library.
    - used in constructors too, slightly different than prototype.
    - 'this' always points to an object or nothing. never a string, function, array, boolean, ect.
    - value of this is determiend by where and how the function it is in was called. When passing functions into other functions the value of 'this' becomes a moving target.
    - strict mode prevents accidentally assigning properties to the window by preventing you from using this in the global scope.
    - There are not actually 'constructor functions', what is different is how they are called using the 'new' keyword.
    - single/double underscore - things that are not meant to change. (__proto__)
    - When you use the 'new' keyword, there are hidden actions taken; assigns this to an object, assignes this.__proto__ = constructor.prototype, returns 'this'.
    - .call, .bind, .apply- allow the function caller to reassign the value of 'this' for that function.
      - function.call({name: 'passed by call'}); - same with .apply()
      - usually used in trickery to get array method to work in ways that they normally don't.
      - .bind() returns another function, make this have the same value no matter where the function is called. How we make sure that somethign has same value for 'this' when we pass functions around multiple times/places.
    - Arrow functions don't create their own context like normal functions. Can't use them for the prototype for this reason. they don't take the value of 'this' from where they are called. also why they work well for functional methods or in forEach, ect.
    - 