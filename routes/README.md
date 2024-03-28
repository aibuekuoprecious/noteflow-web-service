```markdown
## Serving Index Page (Roots) Router

This module defines an Express.js router for handling requests related to serving the index page of a web application.

- It imports necessary modules such as `express` for creating the router and `path` for manipulating file paths.
- It creates a router instance using `express.Router()`.
- It defines a GET route that matches requests to the root path (`/`) or requests ending with `/index.html` or `/index` with optional `.html` extension.
- When a request matches any of these patterns, it sends the `index.html` file located in the `views` directory relative to the current file's directory.

Finally, it exports the router instance to be used in an Express.js application to handle requests for the index page.

## Notes Router

This module defines an Express.js router for handling CRUD operations related to notes in a web application.

- It imports necessary modules such as `express` for creating the router and `notesController` for handling different CRUD operations.
- It creates a router instance using `express.Router()`.
- It defines routes using the `router.route()` method for the root path (`/`).
- For each HTTP request method (`GET`, `POST`, `PATCH`, `DELETE`), it specifies the corresponding controller function from `notesController` to handle the request.

Finally, it exports the router instance to be used in an Express.js application to handle CRUD operations for notes.

## Users Router

This module defines an Express.js router for handling CRUD operations related to users in a web application.

- It imports necessary modules such as `express` for creating the router and `usersController` for handling different CRUD operations.
- It creates a router instance using `express.Router()`.
- It defines routes using the `router.route()` method for the root path (`/`).
- For each HTTP request method (`GET`, `POST`, `PATCH`, `DELETE`), it specifies the corresponding controller function from `usersController` to handle the request.

Finally, it exports the router instance to be used in an Express.js application to handle CRUD operations for users.
```