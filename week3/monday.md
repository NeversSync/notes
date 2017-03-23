## Lecture
### IIFE
- Immediately invoked function expression
- Function that runs right away. 
  - syntax:
  (function() {
  })();
- To create a scope, encapsulation, not redefining vars. 
- function declarations are hoisted, function expressions are not.
- function expressions happen when you assign a function to a variable. 
- Function expressions: arguments, callbacks (async). 
- Encapsulation
  - namespacing/closures. 
- The more files you get and more lines you get, the more complicated it gets to keep track of what is in the global scope and what is referencing things in other files. IIFE's help avoid accidentally polluting global namespace and organizing functionality.

- Global variables immediately become a property on the window object. Setting things to the window object makes them a global variable. 
- To use window object within IIFE structure, use a "module system" like:
  (function(module) {
    const viewObj = {};
    module.viewObj = viewObj;
  })(window);
  - now viewObj is global as a property on the window object.
- in practice wrap whoel fiels in IIFE's, pass in window, what you assign to window inside the IIFE determines what it is available globally.

### testing
- Don't try to completely recreate the entire environment of the element you are testing, just check one behavior that shows that it is working as expected.

### Controller
- role spans both the client and server side
- Central role: takes interaction from the view, makes requests based on the interaction with the model, tells which view to render and gives it the appropriate data. 
- Resources- each sub route or type of data that an app uses. "articles", "projects", ect. These map to our models.
- Client side routing
  - When using a single page application, we don't want the browser to make the requests, we want to intercept the request using a library, translate it into an ajax call, and then render the right information to the page. Script interrupts user navigations, breaks down the pieces, calls the proper funciton to handle it, and changes the view to display the correct thing, all from the same index.html, no RELOAD.
- Controller is list of functions waiting to be called, generally one controller for each resource (ArticlesController, BlogController, ect)
- Something like showing/hiding a dropdown menu may or may not be handled by the controller, things like form submits, page changes, ect will.
- page.js
  - library we will use to handle routing. 
  - short circuits navigation of the browser and intercepts the navigation, grabs the url and calls the appropriate function, which is the handler/controller for that resource/action. That controller speaks to the model, gets the appropriate data back from the model and changes the view. View just deals with making data look a certain way.
  - page('/test', function() {}); page(); 
    -takes two arguments, path, and function. call page() at the bottom of the routing section of code, this initializes page functionality. 
  - under the hood, page is updating url without actually causing navigation.
  - There is a difference now between the navigation within the page, and the requests being made by the browser. 
