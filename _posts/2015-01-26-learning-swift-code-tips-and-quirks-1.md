---
layout: post
title:  "Learning Swift: Code tips and quirks #1"
date:   2015-01-26 9:45:00
categories: ios development
---

January's brought a few distractions, but I'm still riding that iOS bandwagon
into the sunset (perhaps sunrise would be the better metaphor). I'm progressing
through the [codewithchris.com][cwc] tutorial series, which is very good and
thorough so far.

I've just finished lesson 10, which has started to dive into writing Swift code.
At this point I thought it'd be a good time to write a few little notes about
format and quirks:

 - variable naming follows the convention

        var variable-name:variable-type

   For example:

        var someName:String

   The type isn't compulsory, but nice if you know the type in advance
 - when calling a method, the first arg doesn't need to be named, but subsequent ones do

        flyPlane("RV4", orientation: "Upside Down", reason: "More fun")

 - to link a UIView object in the storyboard to an *IBOutlet* property on a class:
    - open the 'Assistant Editor' - bow tie icon, top right of Xcode
    - CTRL+click-and-drag the object in the storyboard over to the code window

Swift seems like a fun language and quite straight-forward to wrap my head
around so far. I'm looking forward to delving into something a bit
more substantial once I've grokked enough to be dangerous.

[cwc]: http://codewithchris.com/1-introduction-to-the-tools-and-materials/
