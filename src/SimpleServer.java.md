## Simple Server 💻

### Overview 💻

This simple Java program creates an HTTP server that responds to requests with a basic HTML response. It serves as a starting point for building more complex server applications.

### Table of Contents 📝

* **Overview**
* **Prerequisites**
* **Getting Started**
    * Running the Server
    * Handling HTTP Requests
* **Example Usage**
* **Troubleshooting**
* **Contributing**
* **License**

### Prerequisites ⚙️

* Java 8 or later

### Getting Started 🚀

#### Running the Server

To run the server, follow these steps:

1. Open a terminal window.
2. Clone the repository containing the code: `git clone https://github.com/username/simple-server`.
3. Navigate to the project directory: `cd simple-server`.
4. Compile the program: `javac -cp .:lib/* SimpleServer.java`.
5. Run the program: `java -cp .:lib/* SimpleServer`.
6. The server will start on port `8000` by default.

#### Handling HTTP Requests

The server uses the `HttpHandler` interface to handle HTTP requests. The `MyHandler` class implements this interface and defines how to respond to incoming requests. When a client sends a request to the server, the `handle` method in `MyHandler` is called. This method sends a simple HTML response to the client.

### Example Usage 💻

Send a GET request to the server:

```
$ curl http://localhost:8000
<h1>Hello from Simple Server!</h1>
```

### Troubleshooting 🚧

* If the server doesn't start, check that you have Java installed and that the port `8000` is not already in use.
* If you get an error when compiling the program, make sure you have the Java Development Kit (JDK) installed and that the classpath includes the necessary libraries.

### Contributing 🤝

Contributions are welcome! Please read our [contributing guidelines](CONTRIBUTING.md) before submitting a pull request.

### License 📄

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.