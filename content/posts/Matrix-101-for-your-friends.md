+++
title = "Matrix 101 for your friends"
date = 2021-07-28
lastmod = 2021-08-02
description = "A guide for your Discord user to understand principles of Matrix and its ecosystem."
tags = ["Matrix","Discord"]
categories = ["Guides","Matrix","Posts"]
+++

{{< toc >}}

In recent years the Matrix protocol, messaging service, decentralised conversation store or whatever you want to call it has been gaining a lot of traction as a
replacement in many communities for many reasons, it might be because IRC isn't cutting it or you are using a service which doesn't respect your privacy or has
horrible security.

However many technical terms or user choices are hard to understand for newcomers, because of this I made this guide (is it one? 🤔) in hopes you can pick the
service up easily.

## Terminology

### Server and Guilds

For starters, Discord has made a good job on picking up the term _Server_ and misusing it, when your favorite youtuber Timmy says _"Join my Discord **Server**"_
you are not really joining his _server_ but Discord's server which hosts Timmy's guild.

Other services might have done the same or different...

> **What do you mean by guild?**

Yes, the correct term would be guilds, even the Discord developer documentation [says so](https://discord.com/developers/docs/resources/guild).

In Matrix, a **room** could be considered the equivalent of **a single Discord channel**, and
[currently Spaces](https://element.io/blog/spaces-the-next-frontier/) could be considered a "Guild" equivalent, altough it's not exactly the same.

I might add that in the past we had "communities" and "badges" but you will rarely see them now.

![A meme of old times, rest in peace badges, we will miss you](images/posts/Matrix-101-for-your-friends/Old_meme.webp)

### Homeservers and their relationship with Matrix

Because matrix is [federated](https://en.wikipedia.org/wiki/Distributed_social_network) and not centralized, you will be presented with the term of homeservers.

Homeservers are **physical servers** controlled by an individual or a collective (organizations, companies, governments, etc), this means that nobody will ever
control 100% of the federation!

Some _public_ homeservers are: the [KDE server](https://community.kde.org/Matrix), [the Matrix server](https://matrix.org),
[envs.net server](https://envs.net/), etc.

Now that you had a quick overview of what are homeserver you will understand that when your friend Tim says "I am on matrix", it could mean:

- His account is hosted on matrix.org.
- You can contact him on the matrix protocol, but not necesarily on matrix.org.

### Clients and their relationship with Element

The same way Discord has **unofficial** clients (i.e the program you download to connect to their server) like [Ripcord](https://cancel.fm/ripcord/), there are
many clients to connect to Matrix.

However because Matrix is an open standard,
[nobody can't ban you](https://old.reddit.com/r/discordapp/comments/8tukek/ripcord_unofficial_native_discord_client_no/e1toruy/?context=8&depth=9) and actually
they encourage their creation, here is for example one table [showcasing some of them](https://matrix.org/clients/).

You might hear about the Element client, many people view it as the "official" client since quite a few matrix developers also work on that client and because
it's the client with the most features currently. It is quite mature and it _just werks_.

## Homeservers

### What server to pick

I recommend for a new user to pick [matrix.org](https://matrix.org), the only downside is probably lag since everyone is using it, if you want to change a
homeserver (and also offload some of the bandwith from them haha) my rules of thumb for choosing are:

- There is an organization that is capable to host it and maintain it (servers don't grow in trees :P).

- They have a good upkeep.

- ...or your friends Timmy & Bob are shilling X server.

There is not an official list of all the possible servers (there are hundreds!) but there are some
[unofficial ones](https://www.hello-matrix.net/public_servers.php).

### Self-hosting

> What is selfhosting? Answer: <https://wikipedia.org/wiki/Self-hosting_(web_services)>

If you are able to host it yourself, go ahead! But you should also consider the risks.

You can find all the [documentation on their webpage](https://matrix.org/docs/guides/installing-synapse). Or you could
[pay someone to do it for you](https://element.io/pricing). You might also want to use a VPS, but that's out of scope for this section.

### Migrating from your server

Nomad identities are not implemented yet (I think), this tool is currently what we have --> <https://ems.element.io/tools/matrix-migration>.

## Clients

As I said, Element is the most feature complete client so you will probably want to start with this one. However you might not like it for X or Y, so you can
choose another client!

### Alternative clients

The best way of picking a client is using the official comparison chart! --> <https://matrix.org/clients-matrix>

If you are looking for my opinion, here is a quick overview of the most popular ones:

- Fluffychat:

  Good on Android, very laggy on desktop. The UX feels as _glossy_ as in Element, it supports a "custom" type of emojis that no other client implement (even
  Element, which is weird).

- Gomuks:

  This is a Terminal client (i.e Windows Terminal, Alacritty, etc), so if you are not it cya!. It supports ASCII image rendering and you can download them with
  shortcuts if you were curious about that.

- Nheko reborn:

  Not a lot to say about this one, but that it's written in Qt at contrast Element is made on Electron, which some groups dislike.

What you should look for primarily is that it **supports E2EE**, since that's one of the main benefits of Matrix.

## Encryption keys

> Oh here we go again.

After you make your account in Element there will be 3~ pop-ups **read them**:

- There is one asking for desktop notifications if you are on the web client.

- Another asks you if you want to enable telemetry.

- The third pop-up asks you to "save your keys", or something along these lines. **That one is important**:

  - You either save your keys into a file safely.

  - You either copy that key into your clipboard, I recommend that you store it on your password manager if possible

I might be slightly wrong on that last part since it has been months after I signed up, but I am sure you will pick it up!

That key will be important to verify your device in other clients you might be logging in, some clients allow you to verify with Emojis (😎😎😎) but if they
don't support it you will have to import that key.

If your key is lost then all your messages are now lost 😢, you gotta reset the keys on settings... and this time be careful...

## Some leaving notes

- On desktop, you can make a [config.json](https://github.com/vector-im/element-web/blob/develop/docs/config.md). Some things it allows you to are:

  - Enable labs features([like Math notation with KaTeX](https://katex.org))

  - [Make or choose a custom theme.](https://github.com/aaronraimist/element-themes)

    If you are on the web version, you will have to use the configuration made by whoever is hosting it. You could also use
    [Element develop to obtain labs](https://develop.element.io/), instead of using the normal URL <https://element.io>.

- Element was used to be called Riot.im, but was changed because issues with the game company... and also the real riots 😳.

- There are some "problematic servers", be wary of joining them since these servers might be not allowed to interact with other servers
  ([called servers ACL](https://matrix.org/docs/guides/moderation#banning-servers-from-rooms-server-acls)).

- [Some rooms are "bridged"](https://matrix.org/bridges/) which means you can interact with people from other platforms! a bridged user normally will have a
  weird MXID such as @\_discord_563563485638563:example.com which you can infer it's a Discord.

Have fun :)

## Didn't quite get it all? Read the official FAQ

<https://matrix.org/faq/>
