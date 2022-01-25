+++
title = "A nice table of contents"
date = 2022-01-20
description = "Making a nice table of contents with an underrated html element"
tags = ["Web-dev", "Development"]
categories = ["Guides","Posts"]
+++

Until now, I have used the following snippet to make a table of contents.

```HTML
<div class="toc">
  <p>Table of Contents</p>

  {{- .Page.TableOfContents }}
</div>

```

However, when you have a lot of sections it becomes a bit annoying for the visitor to scroll to read.

An easy solution would be to use JS to detect a click and expand the table, or using CSS :hover events but in each case you will add unnecessary complexity as
the project grows.

Another alternative is just putting the table at the sides of the article, like on [Josh Comeau website](https://www.joshwcomeau.com/).

Nonetheless on [this post](https://blog.edfloreshz.dev/articles/linux/system76/cosmic-panel/) I discovered _maybe_ a hidden gem of HTML5: the `<details>` tag.
This tag has [great browser support](https://caniuse.com/details) and for such it would not make sense to not want to use it on any new project.

The new code now looks like this:

```HTML
<details>
  <summary>Table of Contents</summary>

{{- .Page.TableOfContents }}

</details>

```

On the CSS side I would add these little changes:

```CSS
summary {
  user-select: none;
}

summary:hover {
  cursor: pointer;
}
```
