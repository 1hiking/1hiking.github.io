+++
title = "Matrix Stickers"
date = 2021-09-17
description = "Posting information about Matrix Stickers."
tags = ["Matrix"]
categories = ["Matrix","Posts"]
+++

{{< toc >}}

You possibly don't know matrix stickers. e I have collected over these past few months some JSON's, curiously I have found 2 types of "stickers", so I will
share and discuss them. Moreover I will also explain how some clients implement stickers.

Let's open the dev console!

## The m.room.message "hack"

This type of sticker is more of a inline message, you probably have seen this variant if a room has a discord bridge bot and users in the Discord room post
custom emojis.

Here is the JSON data:

```JSON
{
"body" : "sticker name",
"format" : "org.matrix.custom.html",
"formatted_body" : "<img data-mx-emoticon=\"\"
src =\ "mxc://example.org/hashid\" alt = \"sticker name\" title = \"sticker name\" height= \"12345\" vertical-align = \"middle\" />",
 "msgtype": "m.text"
}
```

Here is one real example, courtesy of Jaafar.

```JSON
{
    "body": ":jerma: ",
    "format": "org.matrix.custom.html",
    "formatted_body": "<img data-mx-emoticon=\"\" src=\"mxc://kde.org/6b7facfc815238e85175193ffe9a2bf5c46fb35c\" alt=\":jerma:\" title=\":jerma:\" height=\"32\" vertical-align=\"middle\" />",
    "msgtype": "m.text"
}
```

Which will print you a Jerma amogus "sticker". I would personally not use these, however they are very easy to craft

![An image demonstrating the Jerma sticker on Element](images/posts/Matrix-Stickers/Jerma_sticker.png)

## The real method: m.sticker

> Implemented on this [Pull Request](https://github.com/matrix-org/matrix-doc/pull/1158)

This solution is much more clean and human readable, one popular implementation is the Element's sticker picker for example.

Why `m.sticker` and not `m.room.sticker`? Well, because
["i explicitly asked rick to s/m.room.sticker/m.sticker/g in some flu-riddled malaise last week"](https://github.com/matrix-org/matrix-doc/pull/1158#issuecomment-373335074)

```JSON
{
    "body": "Landing",
    "info": {
      "mimetype": "image/png",
      "thumbnail_info": {
        "mimetype": "image/png",
        "h": 200,
        "w": 140,
        "size": 73602
      },
      "h": 200,
      "thumbnail_url": "mxc://matrix.org/sHhqkFCvSkFwtmvtETOtKnLP",
      "w": 140,
      "size": 73602
    },
    "url": "mxc://matrix.org/sHhqkFCvSkFwtmvtETOtKnLP"
}
```

And here is how it looks:

![An image demonstrating the Bunny sticker on Element](images/posts/Matrix-Stickers/Bunny_sticker.png)

## Implementation examples

> This section won't go over a lot of technical details but instead provide a general overview of how some clients add stickers.

- Element uses their own "Integration Manager" to provide a service for stickers, which in turn connects to scalar.vector.im. You will then be able to choose
  from a limited collection of sticker packs, my favorite pack is the KDE one 😎.

![The integration manager, as viewed on the settings. Showing information and allowing the user to toggle it](images/posts/Matrix-Stickers/Integration_manager.png)

- Fluffychat has a very interesting implementation, they have both room stickers _and_ user stickers, I suspect the room's stickers are stored on whatever
  server they are hosted at, and similarly user stickers are stored on your homeserver.

![The Fluffychat sticker creator as viewed on settings](images/posts/Matrix-Stickers/Fluffychat_stickers.png)

> Sadly I believe my homeserver (KDE) does not allow for user stickers, and about that, I think user stickers are just inline messages. (research needed!)

## The Future of Stickers

Currently if you want to make your own stickerpicker it's using this [project](https://github.com/maunium/stickerpicker) (By the way I have not been able to
pull dependencies on Windows, heeelpp). However this is not user friendly.

An interesting Pull Request for "Image Packs" is being discussed on [GitHub](https://github.com/matrix-org/matrix-doc/pull/2545) and hopefully it will be merged
once it's stable.

Also see: <https://matrix.org/blog/2021/07/23/this-week-in-matrix-2021-07-23>
