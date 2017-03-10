# Friday Lecture 
### Code Review
- When reading documentation, isntead of just poking aroudn to fix the current problem, try to spend some time to understand a bigger picture, how it is organized, how to understand it, what is happening, ect.
- Method overloading- when a method behaves differently depending on what is passed into it. .attr(); sets or gets depending on number/type of arguments, $ is the most overloaded. 
- Declare variable towards top of their scope, even if they are empty.

### Week review
- MVC
  - model view controller. we have been focusing on the view this week. controller is interaction, model is a reference/model of the data, view is what is seen. 

- Responsive design
  - %, media queries. based on screen size. 
  - meta tag for media queries. 
  - min-width (mobile first), max-width (desktop)- used in the media queries

- SMACCS - scalable moduler architechture for CSS
  - A philosophy/structure/convention for organizing css code in a project.
  - not a library
  - base- global, layout- large scale layout, module- pieces of app.
  - use a reset- meyer or normalize. 
  - target the same element in different files bus only apply module-like or layout-like styles to them in those respective files.

- CSS Selectors
  - attribute, class, id, element, pseudo selectors (:hover).
  - , separated lists, space delimited lists, [attribute selectors]. 

- DOM
  - Document Object Model
  - html represented as a tree of objects(corresponding to nodes) that is used as a way to interact with it with js, jquery, ect.

- JQuery
  - Javascript Library
  - prewritten code
  - $ (alias for jquery function)
  - Can pass css selcetor as a string, html string, DOM node
  - Methods:
    - .on (events)
    - .find .parent/s (traversal) 
    - .attr .text .css (css atributes)
    - .show .hide .fadeIn (effects)
  - Traversal (walking the DOM) 
    - normally happens when you don't know where you are starting (events)
    - Normally start from this.
      - all levels down : .find (selector)
      - all leves up : .parents (selector)
      - 1 level down : .children()
      - 1 level up : .parent()
    - Look through the ancestors for the common element, then look through the children (find) to find the element you want to target.
    - $(this).parents('ancestor element').find('child element desired');
  - .on(event,[selector], function)
    - $('.main-nav').on('click', '.tab', clickHandler);
    