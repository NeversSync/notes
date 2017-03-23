## Lecture
- REST
  - Representational State Transfer
- REST verbs: maps to something we want to do to a given resource. 
  - act on a "noun"/resource
  - GET; fetch a resource
  - POST: send info about new resource
  - PUT: send info about changing a resource
  - DELETE: remove a resource. 
  - There are more. 
  - Resource Oriented Architecture - the way we get resources is oriented around the resource themselves and acting on them with different REST verbs. 
- HTTP 
  - like GPS for knowledge
- Each 'endpoint' is a route made of a noun and a verb. 
- Requests do no have "memory"
- App state and transition:
  - get: asks for the current state
  - POST, PATCH, PUT, DELETE: changes the state. 
  - GET and DELETE don't have a body, so you include the id in the url
  - PUT/PATCH/POST do have a body, you could include the id in the body.

- Examples of endpoints:
  - GET /articles
  - GET /articles/:id
  - POST /articles
  - PUT /articles/id
  - DELETE /articles/id
  - GET /users/id
  - GET /articles/users/id
  - GET /articles/id/comments
- don't push tokens into public sphere, don't commit it, add the token to your .gitignore
- 
$.ajax('https:api.github.com/users/neverssync', {
  method: 'GET',
  headers: {
    Authorization: `token ${token}` - stored in a variable in a gitignored file.
  } 
})
  .then((res) => {
    console.log(res)
  })
  .catch(err => console.error)