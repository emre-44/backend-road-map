# What is HTTP?

## Understanding HTTP: The Language of the Web

If you've ever clicked a link or typed a web address, you've used HTTP. Standing for **Hypertext Transfer Protocol**, it’s the foundation of data communication on the World Wide Web. Think of it as the set of rules—the language—that your browser (the client) and a web server use to talk to each other.

It’s an **application layer protocol**, meaning it operates on top of the underlying networking layers (like TCP/IP). Its classic job is to transfer hypertext (like HTML) via hyperlinks, but today it handles everything from images and videos to API data.

## How It Works: The Request-Response Cycle

HTTP operates on a simple **request-response model**:  

    1. The Client Makes a Request: Your browser asks the server for specific information.

    2. The Server Sends a Response: The server answers with the requested data, an error, or a status update.

A key characteristic is that HTTP is **stateless**. By default, the protocol doesn’t remember past interactions. Each command is independent. While modern versions (HTTP/1.1 and above) keep the connection open longer for multiple requests (persistent connections), the server still treats each request as a fresh, unrelated event unless extra mechanisms (like cookies) are used.

## Breaking Down an HTTP Request

When you type a URL, your browser sends a request packed with specific data. Here is what is inside:  

 **HTTP Method (The Verb):** This tells the server what action to perform.

    GET: "Please send me this data." This is the most common method for loading webpages.

    POST: "Here is some data for you to process." Used for submitting forms, logins, or uploading files.

    Other methods include PUT, DELETE, etc.

    URL: The specific address or path the request is being sent to.

    HTTP Version: e.g., HTTP/1.1, HTTP/2.

**Request Headers:** These are key-value pairs containing "metadata" about the request. They tell the server things like:

    What browser you are using (User-Agent).

    What type of data the client accepts (Accept: text/html).

    The website you came from (Referer).

**Request Body:** This is optional. It is used mainly with `POST` or `PUT` methods to send actual data to the server (e.g., the username and password you just typed into a form).

## Breaking Down an HTTP Response

The server’s reply contains the following:

    HTTP Status Code: A crucial three-digit number that summarizes the outcome of the request.

        1xx (Informational): The request is received and continuing.

        2xx (Success): The request was successfully processed. The most familiar is 200 OK.

        3xx (Redirection): The resource moved. The client needs to try a different URL.

        4xx (Client Error): Something is wrong with the request. The classic 404 Not Found means the server couldn't find what was requested.

        5xx (Server Error): The server failed to fulfill a valid request due to an internal error.

**Response Headers:** Similar to request headers, these contain metadata about the response (e.g., the server type, the content type Content-Type: text/html, and how long to cache the data).

**Response Body:** This is usually the payload. For a successful GET request, this is the HTML code that the browser renders into the visual webpage you see.

## HTTP and Security (DDoS)

Because HTTP is the gateway to almost every modern application, it is a prime target for attacks.
**DDoS attacks** can be launched over HTTP by flooding a server with huge volumes of seemingly legitimate `GET` or `POST` requests. The server spends all its resources trying to respond to these fake requests, causing it to crash or become unavailable to real users. Because these attacks look like normal traffic, they are classified as **Layer 7 (Application Layer)** attacks.

**Sources:**  
- https://www.cloudflare.com/en-gb/learning/ddos/glossary/hypertext-transfer-protocol-http/ 