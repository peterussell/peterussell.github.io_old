---
layout: post
title:  "WXDecoder Motivation"
date:   2017-06-18 22:27:00
categories: programming, wxdecoder
---

For the last few months I've spent my spare time building an aviation
weather tool called [WXDecoder][wxd], and want to give a brief
overview of what it does, why I think it's important to work on, and
what the future looks like.

# Background

METARs are a type of aviation weather report. They come in a
quick-to-read, but somewhat cryptic format:

![METAR](/assets/images/2017-06-18/ksql-metar.png)

Pilots with more than a handful of hours are pretty adept at reading
the encoded format, but the process can be difficult and error-prone
either for new or rusty pilots, or when the METAR includes infrequently
used codes which need to be looked up. If you didn't know 'FC' meant
funnel cloud and went flying anyway, it could be a bad day.

# WXDecoder

I aim to include three things that I'd seen in other products, but not
combined with a modern interface.

 1. Decode METARs into 'plain' English.
     * Help new pilots learn how to read METARs.
     * Provide a quick method to look up infrequently used codes.<br>
   ![Decoded METAR](/assets/images/2017-06-18/kbfd.png)
 2. Display METARs from multiple airports as a list on a single screen.
     * This helps with cross-country planning. Being able to quickly
       type in weather stations along the route and see them all
       displayed *simultaneously* is a big win for situational awareness.<br>
   ![Multiple METARs](/assets/images/2017-06-18/multiple-metars.png)
 3. Provide tooltips explaining what the components of the report mean,
    and what conditions cause them to be included.<br>
   ![Automated Description](/assets/images/2017-06-18/description.png)

# Future Plans?

WXDecoder is still very much under active development. The major
upcoming components are:

 1. Complete decoders for all pieces of the METAR. The major components
    are complete, but some Remarks still need to be done.
 2. Provide support for METARs outside the US. Particularly New Zealand,
    where I'll want to be using it :)
 3. Add descriptions for all components.
 4. Add login ability, to allow users to save their sets of home airports,
    or ones they use frequently for cross country flights.
 5. And then the rest of the backlog...<br>
   ![Trello Backlog](/assets/images/2017-06-18/trello.png)

# Closing Remarks

I've been excited about this project for a while and really happy it's
now living on the internet. Even in its alpha-stage infancy I've
found it really useful for my preflight briefings.

I welcome feedback, bug reports, criticism, and if you're interested
in dev updates please follow [@wxdecoder][twitter] on Twitter.

[wxd]: http://www.wxdecoder.com/
[twitter]: https://twitter.com/wxdecoder
