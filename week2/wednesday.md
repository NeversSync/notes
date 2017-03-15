## Server/Database lecture
- "curl" - command line command that sends a GET request to a url, it prints out the body of the response from the server. 
- "endpoint" - location of a given resource, in a url: .com/"endpoint".
- Clients: anything that can make a request/receive response from server. Browser, curl, jquery, ajax, ect.  
- Server: app was the server, app.listen started it. It is not Node or Express, they are just related tools. Another form of an event listener, listening for incoming requests on the backend.  
- Server is a program.
- Server makes request (url, method, headers) to server, server asks for data from database, database send data back to server, server sends response (headers, status, body) back to client.
- 127.0.0.1 is alias for localhost - both point to your local machine.
- Shorthand for Ajax- "$.get('/url') 
  - this is a form of a "promise". A promise is something that represents an asyc process. Promises have a primary method called ".then"- .then takes two functions (optional), one to call for sucess, other for error.
    - another primary method on promises is ".catch"- same as .then, but the first argument is inherently "null", second is a function. this essentially is just an error handler. Normally later in the chain of promise .then() handlers, so if anything goes wrong along the chain, the catch stops the chain and the catch handles it.
    - .catch is an example of syntactic sugar- another way to do something else that is already there but is easier to use or understand.
- 'let' = a variable that has block level scope, similar to scope of variables within a function, but can be used in an if/for block and create block level scope there where 'var' would not.
- Use const for global variables at the top of the file, use let everywhere else. 

## SQL
- Persistence layer- to store data beyond browser sessions. 
- Database
  - an organized collection of data. 
  - Database Management Systems DBMS have different types of internal architectures, but mostly use tables.
  - Mongo (documents) are a rapidly growing alternative. 
  - column of table is a field, row is a record.
  - record/field relationship is basically key/value pairs
  - SQL 
    - Structure Query Language. Designed for managing data. 
    - overall query is a statement, then there are clauses that narrow down query, sometimes containing expressions that evaluate. 
    - CREATE TABLE example(
      column1 INTEGER PRIMARY KEY(TYPE), 
      column2 VARCHAR(50),
      column3 DATE NOT NULL
    );
    - 