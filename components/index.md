---
layout: default
title: Components
edit_link: https://github.com/driftyco/learn-angular2/edit/gh-pages/components/index.md
tweet: "How to use components in Angular 2"
---

In Angular 2, Components are the main way we build and specify elements and logic on the page.

In Angular 1, we achieved this through directives, controllers, and scope. In Angular 2, all those concepts
are combined into Components.

### A simple component

Let's start with a very simple component that lists out our name:

```javascript
import {Component, View} from 'angular2/angular2'

@Component({
  selector: 'my-name'
})
@View({
  template: "<div>Hello my name is {{name}}. <button (click)="sayMyName()">Say my name</button></div>"
})
export class MyNameComponent {
  constructor() {
    this.name = 'Max'
  }
  sayMyName() {
    console.log('My name is', this.name)
  }
}
```

When we use the `<my-name></my-name>` tag in our HTML, this component will be created,
our constructor called, and rendered.

The way that an Angular application is started is by passing a root component to
the `bootstrap()` method. Let's add that to our code so that we can test it out.

```javascript
import {Component, View, bootstrap} from 'angular2/angular2'

@Component({
  selector: 'my-name'
})
@View({
  template: "<div>Hello my name is {{name}}. <button (click)="sayMyName()">Say my name</button></div>"
})
export class MyNameComponent {
  constructor() {
    this.name = 'Max'
  }
  sayMyName() {
    console.log('My name is', this.name)
  }
}
bootstrap(MyNameComponent);
```
