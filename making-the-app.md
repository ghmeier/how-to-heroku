#Making the App

We're set up and now it's time to start our app.

#### Making index.js

Let's make a file called `index.js` in `hello-world/`, and open it in your favorite text editor.

We'll add a few lines and review what they do:
```javascript
var http = require("http");
var PORT = process.env.PORT || 3000;

//create server object
var app = http.createServer(function(req,res){
  console.log("Received Request");
  res.send("Hello World");
});

//start server
console.log("Starting Server on Port "+PORT);
app.listen(PORT);
```

__What does that do?__

1. Import the http library
2. Set our port to 3000 (we'll get to this later)
3. Creates a server that responds with 'Hello World' to every request.
4. Starts the server on port 3000

__Now we test.__
```bash
$ node index.js
Starting Server on Port 3000
```

With the server started, we can go to [http://localhost:3000](http://localhost:3000) 
