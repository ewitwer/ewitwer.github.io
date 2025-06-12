---
title: "Understanding and Improving Video Fingerprinting Attack Accuracy under Challenging Conditions"
description: Proceedings of the 23rd Workshop on Privacy in the Electronic Society
date: 2024-10-14 15:20:19 +0200
categories: [publications]
tags: [research, lang-en]
lang: en
---

**Background:** *Video fingerprinting*, similar to the more well-known website fingerprinting, is a class of techniques used to identify which videos a user is watching by analyzing the associated network traffic. A common setting involves an attacker that monitors the link between the user's device and a video server, collects the encrypted traffic, and determines which video the (hidden) communication contents correspond to via classification models. This works because the traffic, despite encryption, contains characteristic patterns that are unique to the underlying video. While many video fingerprinting attacks have been presented, the vast majority have not been evaluated under varied network conditions, and there is a lack of studies with a specific focus on challenging network conditions.

**Description:** The paper adapts two prominent website fingerprinting attacks to work better against video traffic, one of which outperforms the previous state-of-the-art attack by notable margins in several areas. These two attacks are then used to evaluate the effects of varied network conditions, which vantage points training and testing data are collected from, and differences in live latency against attacks. The impacts of observation time (sample length), number of training samples, and training time are also considered. We leverage the results to provide insights into how the performance of attacks is affected by various factors.

[Link to paper](/assets/pdf/2024-wpes.pdf){:target="_blank"}
