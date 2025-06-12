---
title: Padding-only Defenses Add Delay in Tor
description: Proceedings of the 21st Workshop on Privacy in the Electronic Society
date: 2022-11-07 08:06:16 +0200
categories: [publications]
tags: [research, lang-en]
lang: en
---

**Background:** *Website fingerprinting* is a class of techniques used to identify which websites a user is visiting through an encrypted tunnel (such as a VPN or Tor). A common setting involves an attacker that monitors the link between the user's device and the tunnel's entry point, collects the encrypted traffic, and determines which website the (hidden) communication contents correspond to via classification models. This works because the traffic, despite encryption, contains certain patterns that characterize the underlying web page. Certain defenses are based on the idea that these patterns can be changed and rendered unidentifiable by sending dummy *padding packets* that do not correspond to the actual data the web browser needs to display the web page. These are called *padding-only defenses*.

**Description:** The paper is a critique of the widely held assumption that padding-only defenses don't cause delay in web traffic and that the user therefore doesn't have to wait longer for the web page to load, something that must be avoided because its negative effects on user experience result in lower adoption of defense techniques. We run experiments using the Shadow network simulator to show that padding-only defenses do, in fact, cause delays - and, potentially, even worse effects - when deployed at scale in Tor. We recommend in our conclusions that system developers seriously consider adding support for and adopting defenses that explicitly create delays, as they can provide better privacy protection than padding-only defenses, which result in delays in practice anyway.

[Link to paper](/assets/pdf/2022-wpes.pdf){:target="_blank"}
