## User Schema

This module defines a Mongoose schema for a user in the application.

- It requires the `mongoose` library for interacting with MongoDB.
- It defines a Mongoose schema called `userSchema` with fields for `username`, `password`, `roles`, and `active`.
- The `username` and `password` fields are required strings.
- The `roles` field is an array of strings with a default value of `"Employee"`, `"Manager"`, or `"Admin"`.
- The `active` field is a boolean with a default value of `true`.
- It exports the Mongoose model for the 'User' collection using the defined schema.

This schema defines the structure and behavior of user documents in the MongoDB database for the application.

## Note Schema

This module defines a Mongoose schema for a note in the note-taking application.

- It requires the `mongoose` library for interacting with MongoDB and the `mongoose-sequence` plugin for generating auto-incrementing ticket numbers.
- It defines a Mongoose schema called `noteSchema` with fields for `user` (referencing a user), `title`, `text`, and `completed`.
- The `user` field is a reference to a user document in the 'User' collection.
- All fields except `user` are required.
- The `completed` field defaults to `false`.
- It includes timestamps for when the note was created and last updated.
- It applies the `mongoose-sequence` plugin to auto-increment the `ticket` field starting from 500.
- Finally, it exports the Mongoose model for the 'Note' collection using the defined schema.

This schema defines the structure and behavior of note documents in the MongoDB database for the application.