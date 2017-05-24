---
layout: post
title:  "Peggy Returns!"
date:   2015-12-28 20:33:00
categories: peggy
---

The [Image Workstation][iws] app I've been working on is now installed our awesome test
hospital and from what I've heard things seem to be going well. Aside from just being good
news, it also means [one more thing ticked off the list][lb30-tech].

All of a sudden I have a bit more time to work on the little text adventure game I started
on a few years ago (and, also, ahem, never finished). My goal is to get a really, *really*
minimal prototype working, which entails:

 - starting the game
 - navigating a map of 4 rooms
 - collecting 2 items
 - getting to the 'final' room which completes the game, if you have the 2 items

The tiny scope of this first implementation is intentional, with the idea that it should make
it small enough to get finished quickly. After that I can add more bits and pieces but
there should (almost) always be a working platform to build off.

A good chunk of the game engine (in C++) already exists from earlier days, although I've
probably forgotten a lot of C++ since then. For now I'm concentrating on getting a web
UI working using React with Redux.

<img src="/assets/images/2015-12-28/peggy2-ui.png" width="300">

I'll be the first to admit I have no idea what I'm doing, but I've put the source on [Github][gh]
anyway in case anyone wants to have a nosey. If you want to download and run it, something
like this should work:

    git clone https://github.com/peterussell/peggy2
    cd peggy2
    npm install
    npm run example server.js

Then hit http://localhost:5050.

[iws]: http://peterussell.me/programming/2015/11/04/Image-Workstation-Update.html
[lb30-tech]: http://peterussell.me/programming/2015/09/14/Life-Before-30-Technology.html
[gh]: https://github.com/peterussell/peggy2
