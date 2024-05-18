**Table of Contents**

* [Overview](#overview)
* [Main Method](#main-method)
* [MyHandler Class](#myhandler-class)

**Overview**

The `SimpleServer` class demonstrates how to create a basic HTTP server using the Java API. It responds to HTTP GET requests with a simple HTML message. 🏃‍♀️

**Main Method**

*   **Purpose:** Entry point of the program.
*   *   `port`: Integer specifying the port number for the server (default: 8000).
*   *   `server`: Instance of `HttpServer` class representing the server.
*   *   `InetSocketAddress`: Defines the IP address and port number for the server.
*   *   `"/"`: Defines the root path (/) for the server.
*   *   `MyHandler()`: Creates an instance of the `MyHandler` class to handle requests.
*   *   `server.start()`: Starts the server.
*   *   `System.out.println(...)`: Prints a message indicating the server has started.

**MyHandler Class**

*   **Purpose:** Handles HTTP requests and generates responses.
*   *   **implements HttpHandler**: Specifies that this class implements the `HttpHandler` interface.
*   *   **handle(...)**: Overrides the `handle` method from the `HttpHandler` interface.
    *       *   `exchange`: Instance of `HttpExchange` class representing the current request.
    *       *   `String response`: Hardcoded HTML content to be sent as the response.
    *       *   `exchange.getResponseHeaders().set(...)`: Sets the "Content-Type" header to "text/html".
    *       *   `exchange.sendResponseHeaders(...)`: Sends the response headers with the status code (200) and response length.
    *       *   `os`: OutputStream object for writing the response body.
    *       *   `os.write(...)`: Writes the response content to the output stream.
    *       *   `os.close()`: Closes the output stream.