# 🌐 Simple Server Java Code Documentation 🌐

## Table of Contents

- [Description](#description)
- [Setup and Usage](#setup-and-usage)
- [Code Structure](#code-structure)
- [API Reference](#api-reference)
- [Example Usage](#example-usage)
- [Known Limitations](#known-limitations)
- [Contributions](#contributions)

## Description

This code base provides a simple HTTP server implementation in Java using the `HttpServer` API. It serves a static HTML response to all incoming requests. This server can be used for testing or as a basis for building more complex web applications. 🛠️

## Setup and Usage

To run the server, follow these steps:

1. Ensure you have Java installed on your system.
2. Clone or download this repository.
3. Open a terminal window and navigate to the repository directory.
4. Run the `javac SimpleServer.java` command to compile the Java source code.
5. Run the `java SimpleServer` command to start the server.

The server will start listening on port 8000 by default. You can change this port by modifying the `port` variable in the `main` method of the `SimpleServer` class.

## Code Structure

The code is organized into a single Java file, `SimpleServer.java`, which contains the following classes:

- `SimpleServer`: The main class that creates and starts the HTTP server.
- `MyHandler`: An implementation of the `HttpHandler` interface that handles incoming HTTP requests.

## API Reference

### `SimpleServer` Class

| Method | Description |
|---|---|
| `main(String[] args)` | Entry point to the application. |

### `MyHandler` Class

| Method | Description |
|---|---|
| `handle(HttpExchange exchange)` | Handles an incoming HTTP request and sends a static HTML response. |

## Example Usage

The following code demonstrates how to use the `SimpleServer` class:

```java
import java.net.InetSocketAddress;

import com.sun.net.httpserver.HttpServer;

public class Main {
    public static void main(String[] args) throws IOException {
        int port = 8000; // Change this if needed
        HttpServer server = HttpServer.create(new InetSocketAddress(port), 0);
        server.createContext("/", new MyHandler());
        server.start();
        System.out.println("Server started on port " + port);
    }
}
```

This code creates a server that listens on port 8000 and serves a static HTML response to all incoming requests.

## Known Limitations

- The server only serves a static HTML response.
- The server does not support HTTPS.
- The server does not support handling request parameters or POST data.

## Contributions

Contributions to this code base are welcome! Please see the [CONTRIBUTING.md](CONTRIBUTING.md) file for details on how to contribute.