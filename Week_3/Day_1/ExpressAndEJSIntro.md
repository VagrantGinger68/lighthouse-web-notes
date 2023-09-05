## Express and EJS

### Express

Express provides addition functionality compared to a basic HTTP server with Node. Express helps with routing and integrating other libraries into our prject.

A basic Express server setup looks like this:
```js
const express = require("express");
const app = express();
const PORT = 8080; // default port 8080

app.get("/", (req, res) => {
  res.send("Hello!");
});

app.listen(PORT, () => {
  console.log(`Example app listening on port ${PORT}!`);
});
```

The "/" in the app.get refers to the homepage of our website.

</br>

### Template Engine (EJS)

Templates are files that define the presentation of a web app's data separately form the server logic. This allows us to define the HTML of particular pages seperate from the logic in the Express server.

Templates are helpful because:
* They keep server logic seperate from HTML, making it easier to modify or debug one without affecting the other.
* They separate different parts of an HTML document into different files, which helps keep the length of HTML files short and easier to work with.

for EJS we use <% %> to hold javascript code, <%= %> to display a JavaScript variable, and <%- %> to include a partial (ex: header or footer HTML code).