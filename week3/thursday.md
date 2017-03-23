## Lecture
- difference between calling and passing functions
- writing function that takes function as argument
- tracing stack of functions and what the pieces evaluate to.

## Middleware 
- Global State: what is going on in the application, current values of globals, count, ect.
- context object is what is passed in to page() function by default. Convention is to name is "ctx". You can use context to send information across different parts of an app regarding state. context is an object that represents information about the state we are transitioning from. 
- Params - an object that is a property on context object. 
  page(/one/:something) - must be matched in achor tag href (href="/one/42"). Once achor is clicked, params will have property "something:42".
  - on params objects gets stored the infromation in the url/path we set.
- We use the url to send across information about our state.  
- Write click handler in each module as method on global variable the prevents default on anchor click and use a page call with template string path (`/one/${count}`); 
- Adding to the middleware chain;
  - Can write functions that take (ctx, next) as arguments, then that function as the second argument in a page call. Must call next() in the function.