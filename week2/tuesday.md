## Code Review
- CORS Error- browser protection that doesn't allow a client to make a request to another client to protect against use of malicious scripts. 
  - http://stackoverflow.com/questions/25923796/cors-error-with-jquery

## Node
- Server side environment built on chrome's javascript engine
- Single threaded
- Can access the filesystem, can write and retreive files on local filesystem.
- Enabled javascript to be important because of its unique filesystem functionality.
- Can use node in the terminal as a REPL/Console. Type node and hit enter, then write js. Doesn't have browser based obects like Window/document, ect. 
- Can run files from the terminal with: node "file name", result of file will show in terminal
- npm - node package manager. to install/store information/libraries for a project.
- "npm init" creates a package.json file with boiler plate that will live in your project directory. 
- npm install --save express
- npm is also a service that stores all the packages you can use "CLI's" command line interfaces that you can use npm as a command to install.
- "const" is a variable that you cannot overwrite. declared at the top of files because of that.
- app.listen takes two arguments, port number, and a function to call when it successfully connects. 
- at this point run node server.js and it should run the server and wait for a request in the terminal. server built!
- if you make changes on the server side, you have to restart your server to have those changes register.
- you can't get to any files that aren't served up- ".static" method on app allows whole directory to be accessed by browser. 
- app.use introduces something called Middleware - functions that the request and reponse objects get passed through.  
