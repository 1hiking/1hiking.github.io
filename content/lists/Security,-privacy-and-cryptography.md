+++
title = "Security, privacy and cryptography"
description = "A non-complete list about various security topics and what should be avoided."
lastmod = 2021-07-26
tags = ["Security", "Privacy", "Cryptography", "Linux", "PGP", "Email"]
categories = ["Lists"]
+++

{{< toc >}}

This page collects many URLs which write about various topics about security,
privacy, cryptography, etc, or in the same way I do, collect more websites to
validate their arguments for or against a technology or an ideology. I have **no
affiliation** with none of these sites and I just maintain it for my own
pleasure.

Consider making a threat model that fits your needs and not randomly copypasting
configuration settings or installing programs for the sake of it, some of which
could be considered
[security theater](https://en.wikipedia.org/wiki/Security_theater)

Please don't randomly post these links to try and win an argument war (~~like I
do huehuehehehuehe~~), read the articles and make **your own conclusions**.

## Browsers

> This section is not greatly in-depth, for more information read the articles
> made by duck and madaidan, which are linked here.

### Ungoogled-Chromium

- [ungoogled-chromium by duck](https://qua3k.github.io/ungoogled/)
  [[Archive Link]](https://web.archive.org/web/20210628080942/https://qua3k.github.io/ungoogled/)

- [Disables Control Flow integrity](https://github.com/Eloston/ungoogled-chromium/commit/7f238719fa0a16e40559df36988aecf0082a8cf3)

  - [Explanation of why this is not ideal.](https://clang.llvm.org/docs/ControlFlowIntegrity.html)
  <!-- TODO: Aslr is disabled, but where? * [Disables Address space layout randomization](https://github.com/ungoogled-software/ungoogled-chromium-archlinux/commit/7f34e646009e66258e3d567728d0ac209ea7556c)

  * [Explanation of why this is not ideal.](https://wikipedia.org/wiki/Address_space_layout_randomization)

  Based on ducks comments they use the upstream PKGBUILD and use sys libs -->

### Firefox

- [Fission still has a long way to go and doesn't fix all the issues present. See their bug tracker](https://wiki.mozilla.org/Project_Fission)

- [Lack of sandbox in Android](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196)

- [Firefox and Chromium by madaidan](https://madaidans-insecurities.github.io/firefox-chromium.html)

## Browser extensions (also known as addons)

> Privacy extensions could increase your attack surface, at any moment the
> developer could sell the extension or a vulnerability could be disclosed that
> might affect your security and privacy.

- [Privacy Badger Is Changing to Protect You Better by Andrés Arrieta, Bennett Cyphers, et al.](https://www.eff.org/deeplinks/2020/10/privacy-badger-changing-protect-you-better)

- [Nano Adblock sells out and the new developers add malicious code.](https://github.com/NanoAdblocker/NanoCore/issues/362#issuecomment-709428210)

- Adblock sells out, literally type it in your search engine...
  <https://duckduckgo.com/?q=adblock+sell+out>

- There are probably more cases that I have not reported...

## Cryptography

> Cryptography is a very overlooked topic when it comes to security, mainly
> because there is a high barrier of entry for newcomers.

- [cr.yp.to](https://cr.yp.to/)
  [[Archive Link]](https://web.archive.org/web/20210508215838/https://cr.yp.to/)

- [OpenSSL wiki: Elliptic Curve Cryptography](https://wiki.openssl.org/index.php/Elliptic_Curve_Cryptography)

  - Use ECC over RSA if possible.

## Miscellaneous

> Some webpages which I recommend reading but don't have a dedicated section
> (yet).

- [Security & Privacy Evaluations by madaidan](https://madaidans-insecurities.github.io/)
  [[Archive Link]](https://web.archive.org/web/20210615142831/https://madaidans-insecurities.github.io/)

- [The Six Dumbest Ideas in Computer Security](https://www.ranum.com/security/computer_security/editorials/dumb/)
  [[Archive Link]](https://web.archive.org/web/20210612220427/http://www.ranum.com/security/computer_security/editorials/dumb/)

## PGP, Email and the family

> I consider Pretty Good Privacy to be very archaic technology that has not
> greatly adapted to modern needs and thus it should be avoided when possible,
> here are many views from professionals and researchers.

- [Let PGP Die: Why We Need a New Standard for Email Encryption by Sven Taylor](https://restoreprivacy.com/let-pgp-die/)
  [[Archive Link]](https://web.archive.org/web/20210719175620/https://restoreprivacy.com/let-pgp-die/)

- [Whonix wiki: Issues with PGP](https://www.whonix.org/wiki/OpenPGP#Issues_with_PGP)
  [[Archive Link]](https://web.archive.org/web/20210420201147/https://www.whonix.org/wiki/OpenPGP#Issues_with_PGP%5B%5BArchive%2520Link%5D%5D())

- [The PGP Problem by Latacora](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html)
  [[Archive Link]](https://web.archive.org/web/20210526211311/https://latacora.micro.blog/2019/07/16/the-pgp-problem.html)

- [Stop Using Encrypted Email by Latacora](https://latacora.micro.blog/2020/02/19/stop-using-encrypted.html)
  [[Archive Link]](https://web.archive.org/web/20210526211254/https://latacora.micro.blog/2020/02/19/stop-using-encrypted.html)

- [efail: Outdated Crypto Standards are to blame by hanno](https://blog.hboeck.de/archives/893-efail-Outdated-Crypto-Standards-are-to-blame.html)
  [[Archive Link]](https://web.archive.org/web/20210127130530/https://blog.hboeck.de/archives/893-efail-Outdated-Crypto-Standards-are-to-blame.html)

## Open/Closed Source beliefs

> Because there are many programs that are secure _and_ open source, many people
> make the correlation that all FOSS programs are secure by default, which is
> untrue.

- [The illusion of open source](https://web.archive.org/web/20210112132451/https://blog.blueboxsec.org/post/the-illusion-of-open-source/)
  (Archive.org since main page has a faulty cert)

- [Closed Source Conspiracy by Joanna Rutkowska](https://blog.invisiblethings.org/2009/01/26/closed-source-conspiracy.html)
  [[Archive Link]](https://web.archive.org/web/20180831193438/https://blog.invisiblethings.org/2009/01/26/closed-source-conspiracy.html)
