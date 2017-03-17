## Code Review
-Expression is the smallest evaluation, produces a value, a statement is a combination of expressions, produces an action.

- To check duplicate and only get unique values:
  .filter(function (x, i, a) {
    var authorArray =  a.indexOf(x) === i;
    return authorArray;
- .split(' ').length string method that would take a string and put each word into an array separated by commas and give you the word count.

- object literal shorthand:
  - return { keyName, otherKeyName } =
    {keyName: keyName, otherKeyName: otherKeyName}
- Arrow function - replace function keyword in a specific way.
  - function sayHi() {
    console.log('hi');
  }
  var sayHi = () => {
    console.log('hi)
  }
  var createGreeting = (name) => {
    return `Hi ${name}!`;
  }
  - Arrow functions generally replace anonymous functions, they are rarely put in the global scope and defined like above. 
  - Shorthand: if you have ONLY ONE argument, you don't need the parentheses:
    - var createGreeting = name => {
    return `Hi ${name}!`;
  }
  - If the function expression is ONLY ONE LINE, you can leave off the braces and CANNOT include return, as it is the default.
    - var createGreeting = name => `Hi ${name}!`; - can take multiple arguments, need (parens.) 
    - Same as the arrow function on line 25. 
  - Important Catch: arrow functions don't create their own context. 
  - CAN'T use it on the prototype
  
##Testing
  - Makes sure our code works. 
  - Checks that introducing new features or refactoring didn't break anything.
  - Make sure it works in different environments
  - Compare a program to a specification or set of expectations
  - Test driven development: write tests first, and make program match those specifications.
  - Types (from broad to specific): Good tests have a mix.
    - End to End testing
        - Benefits
          - automates an applications behavior in real world scenarios
          - traces data across different parts of the app
        - Drawbacks
          - brittle
          - harder to isolate what caused the test to fail. you can only see that it failed. 
    - Integration testing
    - Unit Testing
      - breaks application down to smaller testable pieces.
      - Benefits
        - requires the dev to write more modular, loosely coupled code
        - points to where an app failed. More specific
      - Drawbacks
        - requires the dev to write more modular, loosely coupled code ;)
        - Units passing tests doesn't necessarily mean they play well together.
  - Writing tests: Check behavior against expectation and report results. 
    - tools: testing framework, and assertion library
    - Testing framework
      - Predefined functions and mehtods to set up your tests and report the results:
        - function for an individual test
          - A way to group like tests
          - ways to manage special cases like async calls
    - Assertion library
      - What compares the result to the expectation. A simple assertion library will evaluate an expression and throw an error if it evaluates to false. 
    - Tests have four parts
      - Setup: create environment for test
      - Exercise: executing functionality
      - Verify: check if results are as expected
      - Teardown: reset the environment. 
    - In most programs, functions are our Units, ideally pure functions (consistent with lack of side effects).
    - To write testable functions, take our unpredictable or random generation parts of the function. 
    - Mocking
      - Sometimes, in order to verify certain behaviors, we have to "mock" out arguments/functions to make something work just for the test. 
  - we're not testing whether javascript is working, we're testing if our code is working