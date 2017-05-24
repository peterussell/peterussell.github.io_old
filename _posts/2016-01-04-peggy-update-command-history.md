---
layout: post
title:  "Peggy Update: Command History"
date:   2016-01-04 21:27:00
categories: peggy
---

The web UI now shows a history of commands that have been entered, and the response from the REST
server for the command.

<img src="/assets/images/2016-01-04/ui-with-history.png" width="400">

Each time the Redux Reducer is called, we grab the command and push it on to a 'commandHistory'
array, which is then returned with the new state. The result is all the history then ends up
in the state returned to the view.

There could well be a better way to do this (for example, does the command history even need to
be a part of the state, or should it just be appended in the view? It's not really *state* after
all), but hey, it's working for now!

The view took a bit of wrapping my head around JSX, specifically how to use the <array>.map() function inside
a React Component to render more Components (hint: it's easy to do, as long as you don't want line
breaks..), but I emerged the victor, and that - also - is working for now.

Here's a shot of home.jsx showing the React component nesting, of note are:

    <CommandHistory history={commandHistory} />
    <CommandHistoryItem value={line} />

(I agree, the names of the props need some work. But trying to think of three variations on the word
'history item' wasn't a good late-evening exercise).

home.jsx:

<img src="/assets/images/2016-01-04/react-components.png">

Next up I'm going to clean up the JSON request and response objects a bit to more closely model
what we'd actually expect from the game server. Because we're starting out simply this will
likely be something like

    request = {
      timestamp: // date/time,
      commandID: // a GUID or similar, to map responses to requests
      userID: pete,
      command: go north
    }

    response = {
      timestamp: // date/time,
      commandID: // GUID sent on the request
      result: 'pete has gone north, over a cliff, and has died'
    }

After that it should be about time to start plumbing the REST server into the C++ game server,
and the real fun begins.
