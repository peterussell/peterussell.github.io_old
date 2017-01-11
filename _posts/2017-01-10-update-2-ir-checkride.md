---
layout: post
title:  "Checkrides, APIs, V7s"
date:   2017-01-10 21:46:00
categories: life
---

# In Review...

**Flying**

The spirit of Jimmy Doolittle has smiled upon me and I'm happy to
report the instrument rating checkride was a success. The ride was
a 3 hour oral, and 2.2 hour flight test, split over two days
due to a failed turn coordinator. It was a fun, though fairly
intense checkride, but I'm really happy to have done the rating.

I've decided to go for the commercial multi-engine rating, and set up
[cpl.peterussell.me][cpl] for study notes and flight debriefs. Looking
back on instrument training I wish I'd been more rigorous about
documenting flight debriefs, so now's my chance to make good.

The tailwheel time has been slowly building. We've had pretty rubbish
weather lately, but I've managed to squeeze in flights on most sunny
days. The logbook says 9.7 hours and I'm starting to feel comfortable
in the SportCub, definitely some of the most fun flying I've done.

**WX Decoder**

The first version of the REST API is now live. It supports
decoding METARs (avation weather reports) for two basic use cases:

 1. As a user, I want to specify an airport ID. The website should fetch the
    latest METAR, decode it, and return it to me.

    > example for Portland (KPDX): [api.wxdecoder.com/metar/decode/kpdx][wxd-api-pdx]

 2. As a user, I have METAR text which I want to decode. I want some way
    to submit raw METAR text to the website, then the website should decode
    the text into a friendly format and return that decoded text to me.
    * This one requires including the raw METAR string in the body of a GET
      request to...

      > [api.wxdecoder.com/metar/decode][wxd-api]

The REST API is written with the Django REST Framework (DRF), deployed on
Heroku. Feel free to play around with it, and if you see any issues or
have suggestions you can get me [@nz_pete][twitter].

**Climbing**

A bit more training and a bit less drinking beer (boo) is paying off, I
climbed my first - ever - V7 indoors last week. I've been working a
second which should go in the next session or two. Progress.

I've also been asking around about outdoor spots, and signed up to the
[Carver Climbing Club][ccc] - apparently is an excellent spot close
to Portland. Now to wait for the weather gods and spend some more time
climbing plastic. Really looking forward to getting outside.

**Reading**

[High Altitude: Mountaineer, Airline Pilot, Modern-day Adventurer][ha] by
[Mike Allsop][stuff]

# This Week..

* **Flying**
  * Review the aerodynamics chapter of the [Pilot's Handbook][phak]
* **WX Decoder**
  * Set up a project in Trello, write up the backlog items
  * Have a basic UI working, text input field with an output label
  * Publish the UI
* **Climbing**
  * Finish the second V7


[cpl]: http://cpl.peterussell.me
[wxd-api-pdx]: http://api.wxdecoder.com/metar/decode/kpdx
[wxd-api]: http://api.wxdecoder.com/metar/decode
[twitter]: https://twitter.com/nz_pete
[ccc]: http://www.carverclimbingclub.org
[phak]: https://www.faa.gov/regulations_policies/handbooks_manuals/aviation/phak/
[ha]: http://www.goodreads.com/book/show/18595506-high-altitude
[stuff]: http://www.stuff.co.nz/national/9267885/Living-the-high-life
