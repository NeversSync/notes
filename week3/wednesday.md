## Lecture
- If something is working, but inconsistently, have to click twice, ect. Strong indicator of an Async problem. 

- logical operator OR stores the first truthy value it gets to || the last thing there. 
'' || 0 || false = false.
'' || '0' || false = '0'.
'' || true || '' = true
- Turnery operator
  - expression ? true : false - if expression is true, it will be first value after ?, otherwise the last value.
  - Mostly useful for assigning variables
  - var name = fauAnimal === 'narwhal' ? 'tom' : 'aaron';
- callback && callback()- if there isnt anything passed into the callback, don't call it.

- node gives two functions to use 
  - require - brings in packages from node modules. 
  - process - information on what is going on around out program. 
  - process.env - an object as property on process where we can store sensitive information, like API tokens.
  - GITHUB_TOKEN="token" node. 
  - const PORT = process.env.PORT || 3000;
    - if server is deployed somewhere, like heroku, which will decide which port to run the server on so it doesn't "double up", this allows us to set it up correctly because we don't know which port it will choose. If we are running it locally for development, we use 3000. 
- Heroku
  - everything you set to the config is available as a property on process.env, good way to set secret info.
  heroku config:set TIMES=2
  heroku config