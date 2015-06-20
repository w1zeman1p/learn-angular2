---
layout: default
title: Arrow Functions
edit_link: https://github.com/driftyco/learn-angular2/edit/gh-pages/es6/arrow-functions.md
tweet: "ES6/TypeScript Arrow Functions"
---

Arrow functions make it easy to write anonymous functions, and also bind to the current
context.

```javascript
class MyClass {
  constructor() {
    this.name = 'Max';

    setTimeout(() => {
      // This prints "Max" since arrow functions bind to our current "this" context.
      console.log(this.name);
    });
  }
}
```

This is like writing:

```javascript
var _this = this;
setTimeout(function() {
  console.log(_this.name);
});
```

But much cleaner.
