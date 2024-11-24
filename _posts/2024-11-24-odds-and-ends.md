---
title: "odds and ends"
date: 2024-11-24
---

It's like always, if you have a closer look you will find some things to fix or tidy up.

DOMTokenList add()/remove() are able to handle an arbitrary amount of tokens; spend some time to write more tests and fix this.

For more tidy I decided to rewrite Plugin/PluginArray/MimeType/MimeTypeArray. These classes are more or less static in the current browsers.
Therefore Htmlunit no longer supports changing the Browser in this regard. This is also the final nail in the coffin of Flash.
And while I'm on that, the method pdfViewerEnabled is now also supported.

Our Codestyletest uses the wrong encoding when reading the source. How could I have missed it all the time?

And another shock - the class HostParentOfMTest is not there. How could I have missed it all the time?



For some time i had this more or less disabled data driven test for request parameter handling. Looks like i have no time to
fix this during the next weeks. To tidy up, I reverted this for now. Git will remember it for me.

stay tuned

RBRi