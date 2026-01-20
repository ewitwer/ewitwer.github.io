---
title: "Ephemeral Network-Layer Fingerprinting Defenses"
description: Proceedings on Privacy Enhancing Technologies
date: 2026-07-25 00:00:00 +0200
categories: [publications]
tags: [research, lang-en]
lang: en
---

**Background:** *Website fingerprinting* is a technique used to identify which websites a user is visiting through an encrypted tunnel (such as a VPN or the Tor network). A common setting involves an adversary that monitors the link between the user's device and the tunnel's entry point, collects the encrypted traffic, and determines which website it correspond to via classification models. This works because the traffic, despite encryption, contains patterns that characterize the underlying content.

Most defense studies evaluate against an adversary that can train classification models on defended traffic. That is, these studies implicitly assume that an adversary knows which defense targeted users have and how it works.

**Summary:** The paper presents a technique for quick generation of unique, per-connection defenses for the Maybenot framework, which removes the website fingerprinting adversary's typically assumed advantage of being able to train on traffic with the same defense as a targeted user. This is essentially an application of Kerckhoffs's principle to traffic analysis defenses, where defenses are treated as secret keys. Simulations indicate that ephemeral defenses work well in multiple scenarios (website fingerprinting, video fingerprinting, and circuit handshakes in Tor) and can achieve reasonable trade-offs between protection and overhead. Also, ephemeral defenses need not be tightly bound to any specific attack, situation, or network conditions.


[Link to paper](/assets/pdf/2026-pets.pdf){:target="_blank"}
