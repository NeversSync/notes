# Monday Lecture Notes

### MVC
  - Model View Controller
    - View = display/ presentation scheme
    - Model = source material or data
    - Controller = interaction, behavior management
  - A design pattern/template
  - Organizing code based on what the code is doing within the project
  - When you can accomplish your task in many different ways (writing script directly into HTML), you have to decide which approach to take and why.
  - Adding a higher level of abstraction - giving jobs/roles to the parts of our code.

### Scalable Modular Architecture for CSS
  - As app gets more complex and big, if it is scalable it will adjust to fit the performance needs regardless of size/complexity.
  - Not a library, its a organizational method/concept/philosophy
  - Separation of View components. Keeping like-styles together. 
  - BASE CSS file with foundational styling. fonts, font sizes, general styling, color palette, ect.
  - LAYOUT - classes (some Id's) header, footer, placement.
  - MODULE - internal, smaller components, navigation, headings, ul, ect.
  - More important than doing the exact SMACCS structure is that there is consistentcy in how you decide what pieces go where within your structure.

### Responsive design notes
  - Add comment with "TODO:" to be able to search for them and work through them in code base using command+shift+F
  - Add multiple classes and make sure the classes clearly describe what they are doing to what.
  - Keep styling in CSS and turn them on and off with javascript instead of writing the CSS into the js.
  - Skeleton css framework. foundation, bootstrap, 960.gs 

## Media Queries
  - <meta name="viewport" content="width-device-width, initual-scale=1">
  - 