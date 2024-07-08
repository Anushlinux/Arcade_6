# Arcade_6

# HTTP Server with Panic Recovery

This Go program demonstrates a simple HTTP server that handles panics and recovers from them. The server listens on port 3000 and responds to three different routes:

- /: Returns a simple "Hello!" message.
- /panic/: Triggers a panic and demonstrates how the server recovers from it.
- /panic-after/: Returns a "Hello!" message and then triggers a panic, demonstrating how the server recovers from it even after sending a response.

The server uses a middleware function to recover from panics and return a 500 Internal Server Error response to the client.

# Prerequisites
- Go 1.16
- Internet connection

# Installation
- Clone the repository
```bash
git clone
```
# Routes
- /: Returns a simple "Hello!" message.
- /panic/: Triggers a panic and demonstrates how the server recovers from it.
- /panic-after/: Returns a "Hello!" message and then triggers a panic, demonstrating how the server recovers from it even after sending a response.

# Panic Recovery Mechanism
The recoverMw function is a middleware that wraps the main application handler. It uses a deferred function to catch any panics that occur during the execution of the application handler. If a panic is caught, it logs the error and returns a 500 Internal Server Error response to the client.

