---
title: "Deep Dive into JavaScript"
date: 2025-11-08
---

It's been a busy month! Between diving deep into JavaScript engine improvements with the Rhino team, implementing DOM APIs, and chasing down some tricky bugs, I've had my hands full. The result of all this work is HtmlUnit 4.18.0, which was released on October 30, 2025. Let me walk you through what I've been working on.

## 🚀 Version 4.18.0 (October 30, 2025)

This latest release continues our commitment to better JavaScript compatibility and modern web standards support.

### Core JavaScript Engine Improvements

I've been heavily involved with the Rhino team this cycle, and we've delivered another great batch of improvements:

**Enhanced ECMAScript Support:**
- Let statements inside switch statements now work correctly - a common pattern in modern JavaScript
- Global symbol registry fully implemented, improving symbol handling across scopes
- Regular expression improvements for better pattern matching
- Yield* statement handling improved for generator functions
- Built-in methods now correctly have no 'prototype' property, matching the spec
- Function.length calculation fixed for default arguments and rest parameters

These changes bring HtmlUnit's JavaScript engine significantly closer to full ECMAScript compliance, making it much better at handling modern JavaScript frameworks and libraries.
It's been a lot of work getting these edge cases right!

And there's already more in the pipeline - the Rhino team is already working on additional JavaScript features that will land in upcoming versions.

### DOM Improvements

**DOMMatrixReadOnly Enhancements:**
I've implemented several key methods for DOMMatrixReadOnly:
- `isIdentity()` method for checking identity matrices
- `toString()` now returns proper string representation
- `toJSON()` implemented for JSON serialization support

**XMLHttpRequest Updates:**
- `getAllResponseHeaders()` now uses '\r\n' as delimiter in Firefox and Firefox ESR, matching real browser behavior

### Firefox Updates

**Compatibility Changes:**
- MutationEvent support removed for Firefox 144, aligning with browser deprecation
- Browser version simulation updated to match current Firefox releases

### Bug Fixes

- Fixed the evaluation of proxy autoconf JavaScript code (this was a regression from the previous version that needed addressing)
- Various small improvements and stability enhancements throughout the codebase

Check out the [full release notes](https://www.htmlunit.org/changes-report.html#a4.18.0) for complete details, and as always, visit our [GitHub repository](https://github.com/HtmlUnit/htmlunit) to report issues or contribute!

Happy testing! 🧪