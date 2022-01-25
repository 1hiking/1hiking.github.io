+++
title = "A quick change to featured posts in Hugo"
date = 2022-01-24
description = "A small variable change to a guide about adding featured posts in Hugo"
tags = ["Web-dev", "Development"]
categories = ["Guides","Posts"]
+++

I have been recently looking about how to add latests posts in my index page, since it has a giant space that has no purpose. I quickly glanced at this
[article by Damien](https://damien.co/blog/2020-06-13-hugo-featured-posts-list/) in which he shared this snippet of code:

```HTML
{{ range first 3 ( where .Site.Pages "Type" "in" site.Params.mainSections )}}
...
{{ end }}
```

However, it should add `.Site.RegularPages` instead of `.Site.Pages` because as the [Hugo documentation states](https://gohugo.io/variables/site/#site-pages),
.Site.Pages will include _everything_ which could lead to unexpected entries, such as a list entry, while RegularPages will only include _regular_ pages.

I write this post in the hopes that anyone who has this problem will be able to find a quick fix.
