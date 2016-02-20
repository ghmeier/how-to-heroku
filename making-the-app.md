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
  res.end("Hello World");
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

With the server started, we can go to [http://localhost:3000](http://localhost:3000) and we'll see: `Hello World`

__Commit our changes:__ 
```bash
$ git add index.js
$ git commit -am 'Built my first node server'
[master (root-commit) 90273e6] Built my first node server
 1 file changed, 10 insertions(+)
 create mode 100644 index.js
```

__Create our package.json__

Make a new file in `hello-world/` called `package.json` and fill it with:
```javascript
{
  "name": "hello-world",
  "version": "0.0.1",
  "description": "Our first node server",
  "keywords": [
    "node"
  ],
  "homepage": "https://github.com/<github-username>/hello-world",
  "author": "<your name/identifying info>",
  "contributors": [],
  "repository": {
    "type": "git",
    "url": "git://github.com/<github-username>/hello-world.git"
  },
  "bugs:": "https://github.com/<github-username>/hello-world/issues",
  "engines": {
    "node": ">= v4.3.0"
  },
  "dependencies": {
    //Add dependencies.
  },
  "license": "MIT",
  "scripts": {
    "start": "node index.js"
  }
}
```

Now, to start your server using: 
```
$ npm start
> hello-world@0.0.1 start /home/garret.meier/git/hello-world
> node index.js

Starting Server on Port 3000
```

Add package.json and commit changes.

####Let's make it accessible
Having things only on you machine is old news, we can let everyone see our beautiful server. Having heroku installed and set up  means we can deploy this with one command:
```bash
$ git push heroku master`
Lots of deployment code....
.....
remote: Verifying deploy... done.
To https://git.heroku.com/ghmeier-hello-world.git
 * [new branch]      master -> master
```

Head to `http://<github-username>-hello-world.herokuapp.com/` to check it out!!

####What next?
We all we have to do to deploy is commit our changes and push to the heroku remote! Heroku also has solid documentation if you want something more complex. 

*[How can we extend our server now?](/extending-your-application.md)*
