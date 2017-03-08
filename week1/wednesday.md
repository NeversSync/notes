# Wednesday Lecture Notes
### Callback Function
- Most of the time it is a function that is getting passed into another function. 
- what makes it a callback is that it doesn't happen right at the time of page load. They are waiting for something else to finish. A foundational example of asychronous programming. A.k.a Asychronous Callbacks.
- High Order Functions - we can pass functions around like a variable.

### Events/jQuery
- Jquery uses .on for events.
  $el.on('click', functionName); - adding event listener and registering the event handler function to that listener.
- You can add event listeners to elements that are not created yet with the .on method:
  - $('main').on('eventtype', 'css selector', function (anonymous or named)); will select main and put a event listener/handler onto it and all its children that match the css selector.
- In order to work with the item that was clicked, you have to rewrap it in a variable that holds $(this);
- "this" equals event.target. It refers to the raw DOM node, not the jquery object wrapped reference to it.
  - var $clickedDiv = $(this); 
- Walking The DOM = start somewhere, got to common ancestor, and move down to desired child (with find() or something similar).

### Single page application (instead of server side rendering)
  - Rather than sending a request to the server and getting back a new page, and doing that again with every change. we are front-loading all the content and then hiding/showing sections of it based on user interaction. This makes applications much faster, more modular, and feel more "applicationy"