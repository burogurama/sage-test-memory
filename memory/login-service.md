# Login service

What is known about the login service, from earlier runs.

- The service validates the password field before it reaches the database layer.
- The login page returns a 500 when the password field is empty; it should reject the empty password earlier with a 400.
- On ticket 8ff-5 (id 2373), `validate_login` raised IndexError on an empty password because it indexed `password[0]` without a length check; fixed in login.py with `if not password or password[0].isspace(): return False`, all tests pass, PR https://github.com/burogurama/sage-test-app/pull/2.
