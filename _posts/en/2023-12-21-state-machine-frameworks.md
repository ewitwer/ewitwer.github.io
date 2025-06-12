---
title: "State Machine Frameworks for Website Fingerprinting Defenses: Maybe Not"
description: "Undergraduate honors thesis, University of Minnesota–Twin Cities"
date: 2023-08-11 05:09:15 +0200
categories: [publications]
tags: [research, lang-en]
lang: en
---

**Background:** *Website fingerprinting* is a class of techniques used to identify which websites a user is visiting through an encrypted tunnel (such as a VPN or Tor). A common setting involves an attacker that monitors the link between the user's device and the tunnel's entry point, collects the encrypted traffic, and determines which website the (hidden) communication contents correspond to via classification models. This works because the traffic, despite encryption, contains certain patterns that characterize the underlying web page. Certain defenses are based on the idea that these patterns can be changed and rendered unidentifiable by sending dummy *padding packets* that do not correspond to the actual data the web browser needs to display the web page. These are called *padding-only defenses*.

Tor has implemented a circuit padding framework (described [here](https://torproject.gitlab.io/torspec/padding-spec.html){:target="_blank"}) in their C codebase. It uses non-deterministic finite state machines to represent padding-only defenses, where *events* describe what is happening on a connection and *actions* result in padding packets being sent. However, it is limited in its ability to express even padding-only defenses, and based on insights from [prior results]({% post_url 2022-11-07-padding-only-defenses %}), it would be desirable to include features such as blocking of packets - artificially induced latency - for better protection and support for more defenses. The [Maybenot framework]({% post_url 2023-11-26-maybenot-framework %}) is based on these ideas; it is a standalone state machine framework, built in Rust, which can be included as a library and used to represent both padding and blocking defenses with probabilistic finite state machines.

**Description:** The paper is an evaluation of the feasibility of state machine frameworks in general for traffic analysis defenses, using Maybenot. This research is done in the context of Tor's ongoing work on Arti, a reimplementation of Tor in Rust - in which a traffic analysis defense framework is to be included (see [here](https://gitlab.torproject.org/tpo/core/arti/-/issues/63){:target="_blank"}). I provide insights into the features needed to build a traffic analysis defense framework that can support effective defenses and touch on important design considerations and challenges. My conclusion is that several possibilities should be carefully explored before picking a defense framework, as it's harder – at least from a bureaucratic perspective – to replace an existing system than to implement it in the first place. I also recommend some enhancements to the Maybenot framework, which are now included in v2.

[Link to paper](/assets/pdf/2023-thesis.pdf){:target="_blank"}
