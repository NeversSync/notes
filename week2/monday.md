# Monday lecture
### HTTP
- hpertext transfer protocol
- hypertext is structured text that uses logical links hyperlinks) between nodes containing text. 
- Think of separate webpages
- The foundation of data communication for the world wide web. 

### URL 
- Uniform Resource Locator- A file path essentially. Some parts of it resolve to an IP, or a location of something at that IP. 
- A Question mark denotes a Query string. Query strings are Key/Value pairs/parameters.
- Protocol goes before the two slashes (https:), after top level domain you have a path to the various files inside the website. then a .fileformat. Then a named anchor, then query string of parameters. 

### Making an HTTP request. 
- 3 parts
  - URL - where
  - Method (GET) - kind of information, standardization of structure for requests.
  - Headers (sender info: user agent, cookies, ect) - additional info regarding request. 
- Server: receives requests and send responses
- Browser(client): sends requests and receives responses. There are other clients.
- This is the internet! 
- When server receives the request, it builds a response and sends it back the client.
- A web server at its foundation is something that receives requests and sends responses. It doesn't need to be a computer in a server farm somewhere, it can be on your computer. 

### RESPONSE
- Status code (200, 301, 404(400+= error codes) 500+=server errors ect) - tells the client what kind of response it is. 
- Headers (info about server and file sent) 
- Body - content
- Keeping things as single page applications saves having to send lots of requests every do you do anything/change pages, front loads instead and makes it faster.

- JSON - turn js object into strings. "dehydrate" "serialize"
- Reconstitute it later when needed.
- JSON is how we structure requests. 
- JSON mostly took over XML - which is more readable, ore object oriented, "lighter". 
- Requests/responses are just big strings. JSON is how we turn requests from objects into strings and on server side, back into objects, ect. 

Var obj = {name: 'dave', type: 'sloth'}
JSON.stringify(obj)
or 
jsonString = JSON.stringify(obj)
JSON.parse(jsonString)

### AJAX
- Asychronous Javascript And XML
- But its mostly JSON these days
- Making requests within script is know as AJAX
- Don't reload the whole page, only request for the data we want/need based on events/ect. 
- AJAX is about asycnhronous requests - callback based. Undetermined amount of time. 
- To make AJAX call:
  - method on Jquery function: - constructing a request
    - $.ajax({
      url: 'http://pokeapi.co/api/v2/pokemon/1',
      method: 'GET',
      success: function(data) {
        console.log(data);
      },
      error: function(err) { - error handler, do this if there is error
        console.log('in error handler', err);
      }
    });

  - Synchronis code runs first. Nothing Asyc happens before all of your sync code is done running. So, if you want to do anything with the response of one AJAX callback, you need to do it within the original callback function. Hence, the "pyramid of doom". 
