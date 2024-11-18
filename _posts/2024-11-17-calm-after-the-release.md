---
title: "calm after the release"
date: 2024-11-17
---

Ok, ok, the headline was the wish, not the reality for this week.

First there was a new regression in neko - [Lowercase property gets ignored in DOM parser](https://github.com/HtmlUnit/htmlunit-neko/issues/127).

Then I did many minor things for HtmlUnit mainly in the area of js support.

After that I spend some time on the Document.createElement() function. There is a clear specification for valid element names.
But guess what the browsers are doing... Finally I gave up and did a simple hack based on unicode isLetter() to implement something that
is similar to the browsers. But now I'm trapped in the java-unicode-support trap. The tests are passing only if you use the rigth
jdk (mean the matching unicode support). What a ....

As a real highligh I attended the [50.TAV](https://fg-tav.gi.de/veranstaltung/50-tav). Two really inspiring days!

And finally the Chrom/Edge 131 update is done.

Stay tuned

RBRi