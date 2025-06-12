---
title: "Raising the Bar: Improved Fingerprinting Attacks and Defenses for Video Streaming Traffic"
description: Proceedings on Privacy Enhancing Technologies
date: 2024-07-20 12:19:20 +0200
categories: [publications]
tags: [research, lang-en]
lang: en
---

**Background:** *Video fingerprinting*, similar to the more well-known website fingerprinting, is a class of techniques used to identify which videos a user is watching by analyzing the associated network traffic. A common setting involves an attacker that monitors the link between the user's device and a video server, collects the encrypted traffic, and determines which video the (hidden) communication contents correspond to via classification models. This works because the traffic, despite encryption, contains characteristic patterns that are unique to the underlying video. While many video fingerprinting attacks have been presented, few studies have focused on defenses.

**Description:** The paper is an evaluation of several attacks against undefended video traffic, two website fingerprinting defenses adapted to the video context, and a tailored defense, Scrambler. It provides a number of insights related to attack efficacy in different scenarios, which defense techniques may be most promising, and the effects of factors such as code execution time and congestion control. These insights represent a solid starting point for future work on video fingerprinting defenses.

[Link to paper](/assets/pdf/2024-pets.pdf){:target="_blank"}
