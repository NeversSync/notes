# Thursday Lecture Notes
- If you are not using one of th tree traversal jquery method or the Jquery function itself, then we are not getting things from back the DOM, we are doing something to what we already have. 
- If there is a length of zero in a console log for what you are getting in a jquery call then there is nothing there.
- if you call .attr(); on a set of elements, it will only target the first element in the set. 
- Take time upfront to understand what is happening and run small pieces of code often to verify each step, this will save time and headaches in the long run.
- Data-"attributes" have something in html that is not necessarily relevant to the HTML. They are useful to track down particular elements/information from js/jq.
- To get back anything from the dom, you are passing a string of css into the jquery function,find, or parents. Stick to those and get selectors right. attr., value, text, ect, are not returning a node, even if they still give you a jquery object.
- Selectors: anything the same CSS rule would apply to should be the selector used.
- Find is only appending selector/s to what you have already selected.

- Template string- use backticks, can include other types of quotes and they will remain part of the string. 
- Only use the $ in naming for a jquery object that has a DOM node in it.
- Inside of a backtick string(template string) add ${}, all code inside of braces will be evaluated first and then the value will be added as a string inside of the string.
- "this" inside an event handler is refering to the DOM node that fired off the event.
- 

#add this to portfolio tab nav handler
 - $('.main-nav .tab:first').click();
 - add event into tab content handler function call