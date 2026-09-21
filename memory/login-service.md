# Login service

What is known about the login service, from earlier runs.

- The service validates the password field before it reaches the database layer.
- The login page returns a 500 when the password field is empty; it should reject the empty password earlier with a 400.
