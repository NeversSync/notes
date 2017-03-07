# Tuesday Notes

- Pseudo elements: 
  - ::after ::before, ect. 
  - creates a new element in the place specified. Can change the content with 'content:'
  - ::after is useful for clearfix. content: ""; 
  - don't need double colon anymore.
- Attribute selectors - use brackets. https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors
  - [class] {
    color: white;
  } - this would change text color to white on any element with a class.
  - Looks for exact match when using equals.
  - , separated list in css applies to all things in the comma separated list. Using a space selects only pieces that are children, ect.

## JQuery
  - DOM - a tree-like model of the document/html made of a series of interlinked objects with parent child relationships
  - Working with the dom, fiding elements, changing them, adding and removing them, reading attributes and values, navigating the tree, managing user interactions, event, ect. Is what Jquery make easier and more powerful. 
  - showed up around 2006, one of its main purposes at first was to level the differences of working with different browsers.
  - Using libraries do have an overhead, they add a lot of lines of code (aprx 6000) to remove a small number of lines of code if you didn't use them.
  - $('selector string').actionToPerform(args); 
  - The only thing that makes it into the global namespace from the JQuery file is the $. 
  - Pass it a string that is a CSS selector.
  - method overloading- when something acts differently depending on how you use it/what you pass into the arguments. JQuery uses this a ton. you can get the height by passing no arguments, if you use an argument you will set the height.
  
