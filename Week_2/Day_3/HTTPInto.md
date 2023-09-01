## HTTP Into

### Summary

HyperText is the HT in HTTP and HTML. Hypertext is text that contains links to other texts.

</br>

HTTP is a proocol used to read and write resources (data) in a simple text-based manner. It can be used for all sorts of documents including JavaScript files, CSS, and anything that our browser is capable of downloading (PDFs, etc).

</br>

HTTP is a request-response based protocol. A client makes a request to an HTTP server and at the same time sends a message asking for a specific resource. The server will send it back as a response. A server cannot send a response if the client doesn't ask for a resource.

</br>

There are 9 HTTP request methods but 4 are most important:

1. GET: used to "get" data from the server.
2. POST: used to create new data.
3. PUT: used for editing existing data on the server. 
4. DELETE: used to delete existing data.

</br>

HTTP has status codes that the server will send to the client if there is a problem. A status code is a 3 digit number and there are lots of different status codes available. The main status codes are:
* 200: "Everything is good"
* 201: "The request has succeeded and a new resource has been created as a result."
* 404: "Resource was not found."
* 500: "The server had an error."