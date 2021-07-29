+++
title = "Matrix 101 for your friends"
date = 2021-07-28
description = "A guide for your Discord user to understand principles of Matrix and its ecosystem"
tags = ["Matrix","Discord"]
categories = ["Guides","Matrix","Articles","Posts"]
+++

In recent years the Matrix protocol, messaging service, decentralised conversation store or whatever you want to call it has been gaining a lot of traction as a replacement in many communities for many reasons, it might be because IRC isn't cutting it or you are using a propietary service.

However many technical terms or technologies are not very well understood, for this reason I made this guide in hopes you can pick the service up easily.

## Terminology

### Server and Guilds

For starters, Discord has made a good job on picking up the term _Server_ and misusing it, when your favorite youtuber Timmy says *"Join my Discord **Server**"* you are not really joining his *server* but Discord's server which hosts Timmy's guild.

Other services might have done the same or different...

> **Wait guild?**

Yes, they are called guilds, even the Discord documentation [says so](https://discord.com/developers/docs/resources/guild).

In Matrix, a **room** is the equivalent to **a single Discord channel**, and [currently Spaces](https://element.io/blog/spaces-the-next-frontier/) could be considered a "Guild" equivalent, altough it's not exactly the same. I might add that in the past we had "communities" and "badges" but you will rarely see them now.

### Homeservers and Matrix

A homeserver is **the server** of an individual or a collective (organizations and companies are welcome), for this reason <https://matrix.org> does not control the entirety of the [Federation](https://en.wikipedia.org/wiki/Distributed_social_network)... this is the power of decentralization™ ladies and gentlemen.

So when little Timmy says "I am on matrix", it could mean:

* His account is hosted on matrix.org
* You can contact him on the matrix protocol, but not necesarily on matrix.org.

Get it now?

### Clients and Element

The same way Discord has unofficial clients like [Ripcord](https://cancel.fm/ripcord/), Matrix has many clients, the only difference is that Matrix will not ban you and instead encourages the creation of them!.

The "main" client for Matrix is [Element](https://element.io). But hopefully more clients will catch up to feature parity :)

## Homeservers

### Choosing your server

If you want to play safe pick matrix.org but expect some lag since everyone is using it, if not, my rule of thumb for choosing a homeserver is:

* There is an organization behind it that is able to run it.

* Said organization is financially stable.

* There is an upkeep of at least 90%

* ...or your friends Timmy & Bob are shilling X server.

Some examples are kde.org, matrix.org, etc.

There is not official list of all the possible servers but there are some [unofficial ones](https://www.hello-matrix.net/public_servers.php).

### Self-hosting

If you are able to host it yourself, go ahead!

You can find all the documentation on <https://matrix.org>. Or you could [pay someone to do it for you](https://element.io/pricing).

There are risks and benefits of self-hosting, it's all up to your ability to read the manuals and your piggy bank.

### Changing servers

Nomad identities are not implemented yet (I think), this tool is currently what we have --> <https://ems.element.io/tools/matrix-migration>

## Clients (a.k.a. the program you download to connect.)

> The most feature full client currently it's Element, you can either use the Desktop version or the Web client. The technologies are the same as Discord in regards to using Electron for the desktop client, so if you are not into that, pick other. Some parts of this guide will be focused on Element.

### Choosing your client

The best way of picking a client is using the official comparison chart! --> <https://matrix.org/clients-matrix>

> Nooo don't do this, choose for me!

Pick one of these:

* Element (Electron)

* Fluffychat (Flutter)

* Gomuks (I hope you enjoy the Terminal)

* Nheko reborn (Qt)

What you should look for primarily is that it **supports E2EE, since that's one of the main benefits of Matrix**

## Encryption keys

After you make your account in Element there will be 3~ pop-ups **read them**:

* There is one asking for desktop notifications if you are on the web client.

* Another asks you if you want to enable telemetry.

* The third pop-up asks you to "save your keys", or something along these lines. **That one is important**:

  * You either save your keys into a file safely.

  * You either copy that key into your clipboard, I recommend that you store it on your password manager if possible

I might be slightly wrong on that last part since it has been months after I signed up, but I am sure you will pick it up :)

That key will be important to verify your device in other clients you might be logging in, you can also verify with **emojis**! (I am not kidding).

If your key is lost then all your messages are now lost :(, you gotta reset the keys on settings... and this time be careful...

## Some leaving notes

* On desktop, you can make a [config.json](https://github.com/vector-im/element-web/blob/develop/docs/config.md). Some things it allows you to are:

  * Enable labs features([like Math notation with KaTeX](https://katex.org))

  * [Make or choose a custom theme.](https://github.com/aaronraimist/element-themes)

    If you are on the web version, you will have to use the configuration made by whoever is hosting it. You could also use [Element develop to obtain labs](https://develop.element.io/), instead of using the normal URL <https://element.io>.

* Element was used to be called Riot.im, but was changed because issues with *that* other Riot, and before that it was Vector (I think).

* There are some "problematic servers", be wary of joining them since these servers might be not allowed to interact with other servers ([called servers ACL](https://matrix.org/docs/guides/moderation#banning-servers-from-rooms-server-acls)).

* [Some rooms are "bridged"](https://matrix.org/bridges/) which means you can interact with people from other platforms!

Have fun :)

## Didn't quite get it all? Read the official FAQ

<https://matrix.org/faq/>
