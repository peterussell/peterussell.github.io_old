---
layout: post
title:  "Peggy Update: REST server"
date:   2016-01-03 23:45:00
categories: peggy
---

Peggy now has a (very rudimentary) REST server API, which I've muddled together using
node.js and Express. Despite my relative inexperience, it took a lot less time than I was expecting,
although figuring out how to get React and Redux into the mix took a little extra learning time.

The goal tonight was to put together a quick proof-of-concept, and get the webapp (React/Redux)
sending requests and writing out responses.

This is the resulting webapp UI (polished, I know).

<img src="/assets/images/2016-01-03/peggy-rest-server-screenshot.png">

The REST server expects a POST with a JSON body looking like:

    {
      userID: 'some-id-string',
      command: 'go north', // for example
    }

The server (in its current incarnation) looks at the command and returns a JSON object containing
a simple status, a message field indicating the result, and a new position, something like:

    {
      status: 'success',
      message: 'Executing command go north',
      newPosition: 'in the north (from rest-server)'
    }

This is what the response object looks like in Chrome dev tools:

<img src="/assets/images/2016-01-03/response-body.png">

On the webapp end, the Redux action dispatcher and reducer have been modified to fire off a REST
request using the fetch API (also pretty straight forward, [David Walsh's fetch API page][fetch-api]
was a big help), then add the result to the Redux state.

Ultimately the REST server will be plumbed into the C++ game server, and act as a marshall
between the webapp (ie. user) and the actual processing done by the game server.

As always it's all open-sourcey, so feel free to git clone from [github.com/peterussell/peggy2][gh].
To get the REST server running, you'll need to cd into the rest-server directory, install the npm
packages, then start the server (default port 3000).

    cd <peggy-base-dir>/rest-server
    npm install
    node app.js

<img src="/assets/images/2016-01-03/starting-the-server.png">

The next goal is to update the UI to display a history of commands entered by the user and responses
from the server.

[fetch-api]: https://davidwalsh.name/fetch
[gh]: https://github.com/peterussell/peggy2
