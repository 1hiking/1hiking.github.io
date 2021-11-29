+++
title = "Archinstall is nice"
date = 2021-09-12
description = "Explaining my dislike for some Arch based distros and archinstall, a new alternative when installing Arch Linux."
tags = ["Linux","Security"]
categories = ["Articles","Posts"]
draft = true
+++

Since the creation and (somewhat) popularization of GNU/Linux there has been
many distributions created for different purposes such as Debian, Fedora, SUSE,
Alpine, etc. But one of them has stood out, of course I am talking about....

## Arch Linux (btw)

One of the main reasons for the adoption of Arch it's the simplicity and the Do
It Yourself philosophy however, in comparison with other DIY distributions like
Gentoo or Linux From Scratch (which is more of a giant man page rather than a
distro...) Arch includes binary packages, removing the process of compilation
that in some hardware might be slow.

Over time, people have done "Arch-based" distributions with the purpose of
making it easier for new users to receive most of the Arch benefits such as the
AUR or the Arch wiki without having to "dig their own pool", but I would not use
almost all of these distributions at _all_ due to many problems...

## The friendly distros

There are many distributions such as Garuda and EndeavourOS which instead of
dropping you to a root shell and letting you configure your installation they
include a graphical installer and some also include extra configuration panels,
while this sounds good I have a grip against these distributions.

## The bloat

Many of these distros apart from presenting a common Calamares installer, do a
lot of stuff that's just bloat, adding icon packs, themes, their own control
panels, etc. This just eliminates the DIY philosophy of Arch which one of the
primary reasons it's sucessful to begin with. I am not complaining that theming
is bad, but is it really worth making a distro for this?

Side-note: Trying to use some of these distros on a VM is very laggy, I barely
was able to navigate on live environments.

## The system management

One popular example of a distro gone horribly wrong is Manjaro,
[they have done so many issues in the past](https://github.com/kruug/manjarno)
both in security and in profesionalism, they went as far as accidentally
DDoS'ing the AUR.

Garuda once accidentally wiped your
[home directory](https://forum.garudalinux.org/t/after-deactivate-hidpi-my-home-dir-got-wipe/3748),
they also use the chaotic-aur, but it fundamentally
[not safe to use](https://www.reddit.com/r/archlinux/comments/i9mope/what_is_the_general_consensus_of_chaoticaur_is_it/g1hl9nm/).

## The community

A distribution being abandoned it's not uncommon, it might be due to lack of
funding, the maintainers are no longer interested, which is exactly what
happened to [Antergos](https://itsfoss.com/antergos-linux-discontinued/), and
why EndeavourOS was made.

Going back to Manjaro, they kicked one of
[their treasurer after questioning funds](https://archived.forum.manjaro.org/t/change-of-treasurer-for-manjaro-community-funds/154888)...

## archinstall

There are possible many other problems which I have not found, but I really
can't feel comfortable using these distros, yet the quest for making Arch
_easier_ it's still on, or it was until `archinstall` was revealed on April's
Fool Day (what a coincidence right?).

By reading the [wiki](https://wiki.archlinux.org/title/Archinstall) we can see
that it does it's job really well, another feature is being able to
import/export profiles since they are saved on a JSON format.

I find this tool booth useful for people who already know how to install Arch
but can't be bothered to do everything again, to new users who find difficulty
when reading the wiki.

I give it an 8/10
