---
title: "HtmlUnit 4.14.0 - 4.17.0: Summer of Progress"
date: 2025-10-10
---

# HtmlUnit 4.14.0 - 4.17.0: Summer of Progress

It's been an incredibly productive few months for HtmlUnit! Between July and October 2025, we've released four significant versions (4.14.0, 4.15.0, 4.16.0, and 4.17.0) packed with improvements, new features, and important bug fixes. A major highlight across these releases is the outstanding work from the Rhino team, delivering substantial JavaScript engine improvements that bring HtmlUnit closer to modern ECMAScript compliance. Let's dive into the highlights!

## 🚀 Version 4.17.0 (October 5, 2025)

**Core JavaScript Improvements:**
- Multiple Rhino engine fixes including better string handling, array method improvements, and enhanced typed array support

**CSS and DOM Enhancements:**
- CSS parsing improvements to support :has(), :is(), and :where()
- BroadcastChannel, DOMMatrix and DOMMatrixReadOnly stubs replaced by a real implementation
- Support for htmx 2.0.3-2.0.7

**Core WebClient Enhancements:**
- Chrome/Edge 140, Firefox 142

## 🚀 Version 4.16.0 (August 29, 2025)

This release focused on runtime improvements:

**JavaScript Engine Updates:**
- Several fixes for calling bind() in the interpreter (regression from 4.14.0)
- spread for object literals implemented
- Multiple Rhino engine updates including better function handling and property resolution

**Core WebClient Enhancements:**
- Use our own 'fork' of the current brotli source code. This makes some fixes available that are done in the code base but not release so far.
- Use our own StringUtils at more places to be compatible with older commons lang versions.

## 🚀 Version 4.15.0 (August 17, 2025)


**Testing and Quality:**
- WebAssert messages have been thoroughly reviewed and improved across the board
- Better error messages make debugging significantly easier

**JavaScript Engine Updates:**
- TypedArray.from and TypedArray.of implemented

**Core WebClient Enhancements:**
- Chrome/Edge 139, Firefox 141
- The parser for the refresh header has been rewritten. Thanks to a series of additional tests, we are now much closer to real browsers

## 🚀 Version 4.14.0 (July 30, 2025)

**Major Announcement: jsoup-bridge**
The biggest news is the introduction of our new sister project '[jsoup-bridge](https://github.com/HtmlUnit/htmlunit?tab=readme-ov-file#jsoup-bridge)'! This bridge enables seamless integration between HtmlUnit and jsoup, combining the strengths of both libraries.

**JavaScript Engine:**
- Significant Rhino engine updates including better ES6+ support
- Enhanced function handling and prototype chain resolution
- Improved array and object manipulation

**Core WebClient Enhancements:**
- Chrome/Edge 138, Firefox 140
- New WebClinet.waitForBackgroundJavaScriptStartingBefore(final long delayMillis, final long timeoutMillis) that combines a overall timeout with waiting for js tasks starting before. Based on this impl the test suite of the Jenkins project now runs much faster.

**Code Cleanup:**
- Removed deprecated classes and methods
- Streamlined codebase for better maintainability
- Switch to jUnit 5

## Thank You!

Special thanks to our core contributors the RhinoTeam, René Schwietzke, and the entire community for their continued support and contributions. Your bug reports, pull requests, and feedback make HtmlUnit better with every release!

---

As always, you can download the latest version from Maven Central or check out the full [changes report](https://www.htmlunit.org/changes-report.html) for complete details.

Happy testing!

RBRi
