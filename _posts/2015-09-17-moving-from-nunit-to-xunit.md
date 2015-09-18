---
layout: post
title:  "Moving from NUnit to xUnit"
date:   2015-9-17 18:18:00
categories: programming
---

I swore it would never be me. I'd always have unit test coverage, not like those other chumps
who churn out code with no guarantees against regression or fickleness. Alas, I'm now one such
chump.

The need to rapidly add features to the IWS meant I never quite 'found the time' to write unit
tests (let's not even talk about integration or stress tests...). I knew it would require writing
new interfaces for the filesystem and database (at least) to allow mock objects. Daunting stuff.
But now Lady Time (Lady Time? That's a thing, right?) has caught up to me, and having
fixed a few  I-already-fixed-that bugs it's time to go back and repay that never-sleeping technical
debt.

As part of that I've moved from NUnit, which I've used for a long time in a number of projects,
to its newer incarnation [xUnit][xunit].

One major difference so far is the xUnit doesn't contain test setup and teardown methods, methods
decorated with `[TextFixtureSetUp]` and `[TestFixtureTearDown]` attributes respectively whose job is
to run code within these methods before and after each test. The idea is to avoid writing duplicate
code at the start and end of each test method.

In pursuing the truth of SetUp and TearDown's demise I came across [this article][setupteardown] from
James Newkirk, team lead on NUnit, which talks about why using SetUp and TearDown methods is
a bad idea. I have mixed feelings, but we'll leave that as an exercise for the reader.

xUnit otherwise seems fairly straightforward and quite nice. I won't delve into its innards here (there are
[plenty of better places][xunit-tutorials] on the internet for that. It's two quick NuGet installations
(one for xUnit and one for the test runner), and Bob's your Uncle.

So, advice from a chump: don't be a chump, pay your technical debt up front.

[xunit]: https://xunit.github.io/
[setupteardown]: http://jamesnewkirk.typepad.com/posts/2007/09/why-you-should-.html
[xunit-tutorials]: http://stackoverflow.com/questions/9006615/are-there-any-good-documentations-books-tutorials-for-xunit-net
