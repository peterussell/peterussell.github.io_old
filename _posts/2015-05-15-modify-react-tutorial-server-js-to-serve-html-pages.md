---
layout: post
title:  "How to modify React tutorial's server.js to serve HTML pages"
date:   2015-05-15 16:53:00
categories: react, programming
---

([I don't want your life story, take me to the solution](#solution))

I've been playing with [React][react], a JavaScript UI-ish framework
from Facebook, by working through [this tutorial][tutorial]. Part of
the tutorial involves running a small server to serve up a file called
comments.json. The server's provided in a number of languages, I've been
using the JavaScript implementation (server.js) with [Node.js][node].

Because the server *only* serves comments.json, I accessed index.html directly
from my local file system via file:///<path-to-index.html>. When index.html (served
from my file system) requests comments.json from the node server it results in
a Cross Origin Request, which Chrome kindly prevents you from doing. This nasty
thing turns up in the console:

        XMLHttpRequest cannot load file:///<path>/comments.json?_=1431734605857.
        Cross origin requests are only supported for protocol schemes:
        http, data, chrome, chrome-extension, https, chrome-extension-resource.

<a name="solution" />
**The quick solution** is to modify server.json to also serve index.html, then
request index.html from the server, eg. http://localhost:3000/index.html.

1. open server.js in your favorite text editor
2. find this section:

        app.get('/comments.json', function(req, res) {
          fs.readFile('comments.json', function(err, data) {
            res.setHeader('Content-Type', 'application/json');
            res.send(data);
          });
        });

3. immediately below that, insert this:

        app.get('/index.html', function(req, res) {
          fs.readFile('index.html', function(err, data) {
            res.setHeader('Content-Type', 'text/html');
            res.send(data);
          });
        });

4. save and close server.js, restart the server, browse to http://localhost:3000/index.html (or whatever your local server port/path combo is)

[react]: https://facebook.github.io/react/
[tutorial]: https://facebook.github.io/react/docs/tutorial.html
[node]: https://nodejs.org/
