+++
title = "Playing with the CSS Paint API"
date = 2022-02-11
lastmod = 2022-02-14
description = "Experimenting with the new Paint API part of CSS Houdini."
tags = ["Web-dev", "Development"]
categories = ["Articles","Posts"]
+++

{{< toc >}}

Some weeks ago while studying about CSS, I stumbled upon <https://houdini.how> and it seems as a fun feature to experiment and integrate in your projects in the
future.

## What is it?

The same way HTML has the DOM, CSS has the CSS Object Model (CSSOM) and the CSS Houdini group are developing APIs that are meant to allow developers to make use
of it in the form of Worklets, these can be reusable and shared between projects. It's basically a way to allow developers to not wait for a browser standard
and instead develop their own little features.

Currently Paint is the first one of the APIs which has received a W3C recommendation, it is available on Chromium natively and on Firefox currently through a polifyll script.

## How to create one

To create a worklet first load it with the following script:

```JS
// main.js
if ("paintWorklet" in CSS) { //This if can be skipped if wanted.
    CSS.paintWorklet.addModule("worklet.js");
    //...
}
```

Now that your worklet is loaded, we can begin with the following boilerplate:

```JS
// worklet.js
const WORKLET = "feature";

class Feature {
  static get inputProperties() {
    return [`--${WORKLET}-gum`, `--${WORKLET}-gam`, `--${WORKLET}-gemmo`];
  }
    paint(context, geometry, properties) {

    }
}
registerPaint(`feature`, Feature);
```

First as its name suggests `registerPaint()` will register the name of our feature so it can be accessed in CSS (I will showcase this later) and we also put
down a class; in which we will pass two methods: `inputProperties()` where we will return our custom properties and `paint()` where all the fun stuff begins.

But before programming anything, we first have to register our properties!

Let's go back to `main.js` and for each variable we will add this following snippet:

```JS
// main.js
if ("registerProperty" in CSS) {
    CSS.registerProperty({
        name: "--feature-gam",
        syntax: "<number>", // Optional
        initialValue: "", // Optional
        inherits: true,
    });
    //...
}
```

The types we can add on syntax can be found on [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Values_and_Units), I highly suggest to set it to avoid
any parsing errors.

Now going back to `paint()`, there are three arguments: ctx, geometry and properties.

- `ctx` behaves almost exactly like the HTML5 Canvas API, you can just use [this handbook](https://bucephalus.org/text/CanvasHandbook/CanvasHandbook.html) as a
  reference of what you may be able to do.
- `geometry` from what I understand allows you to get the size and width of the HTML element (can anyone confirm?).
- `properties` allows you to access the data from the CSS custom properties, if you didn't set a syntax as explained before expect errors.

Now that the JS is out of the way, let's go to our CSS file and add a div with our worklet:

```CSS
/* main.css */
.my-funny-div {
    /* you can also use background-image ! */
    background: paint(feature);
    --feature-gum: 12
    --feature-gam : 10%
    /*... */
}
```

As a quick showcase, see my [random circles demo](https://css-paint-circles.netlify.app/).
