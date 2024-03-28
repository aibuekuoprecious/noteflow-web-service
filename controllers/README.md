## Notes Module

This file contain functions to handle CRUD operations for notes. It requires the `Note` and `User` models, as well as the `express-async-handler` middleware.

- `getAllNotes`: Retrieves all notes from the database, adds the username to each note, and sends the response.
- `createNewNote`: Creates a new note with the provided data and stores it in the database.
- `updateNote`: Updates an existing note with the provided data.
- `deleteNote`: Deletes a note from the database based on the provided ID.

Each function corresponds to a specific HTTP request method (`GET`, `POST`, `PATCH`, `DELETE`) and route (`/notes`), and they are accessed with the appropriate access level (Private). The module exports these functions to be used as route handlers in an Express.js application.

## Users Module

This file contain functions to handle CRUD operations for users. It requires the `User` and `Note` models, as well as the `express-async-handler` and `bcrypt` libraries.

- `getAllUsers`: Retrieves all users from the database, excluding their passwords, and sends the response.
- `createNewUser`: Creates a new user with the provided data and stores it in the database after hashing the password.
- `updateUser`: Updates an existing user with the provided data, including password hashing if a new password is provided.
- `deleteUser`: Deletes a user from the database based on the provided ID after checking if the user has any assigned notes.

Each function corresponds to a specific HTTP request method (`GET`, `POST`, `PATCH`, `DELETE`) and route (`/users`), and they are accessed with the appropriate access level (Private). The module exports these functions to be used as route handlers in an Express.js application.