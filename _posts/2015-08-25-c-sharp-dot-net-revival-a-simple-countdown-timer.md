---
layout: post
title:  "C#.Net Revival: A simple Countdown Timer"
date:   2015-8-25 22:15:00
categories: programming
---

Over the last year or so I've been working on a Winforms app to pull images from a piece
of medical imaging hardware and print them to a network printer. At the genesis of the project
I was doing a lot of C#.Net development which made it a great choice of platform (back then 
at least), but I've since spent more and more of my so-called 'professional' life knee-deep in 
other languages and I feel a bit ... rusty.

In an attempt to quell the demons of stagnation I embarked upon a simple countdown timer
to get back into playing with Winforms, threads, and events.

The program has a main form with two buttons: Start and Stop. Start spawns a new thread that
opens a 'counter' window, counts down from 10 (and yes, only 10) then closes. Start can be pressed
multiple times resulting in multiple counter windows, each of which does the same. The stop button
closes the oldest window. All active threads are displayed in a text area on the main form.

Although fairly simple (and kinda useless) it was a good exercise to get back in the C# swing.

If you need a fork to create the next big MMORPG, [the source is on Github][github].

[github]: https://github.com/peterussell/CountdownApp