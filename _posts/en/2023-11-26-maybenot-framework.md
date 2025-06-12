---
title: "Maybenot: A Framework for Traffic Analysis Defenses"
description: Proceedings of the 22nd Workshop on Privacy in the Electronic Society
date: 2023-11-26 12:18:19 +0200
categories: [publications]
tags: [research, lang-en]
lang: en
---

**Background:** *Website fingerprinting* is a class of techniques used to identify which websites a user is visiting through an encrypted tunnel (such as a VPN or Tor). A common setting involves an attacker that monitors the link between the user's device and the tunnel's entry point, collects the encrypted traffic, and determines which website the (hidden) communication contents correspond to via classification models. This works because the traffic, despite encryption, contains certain patterns that characterize the underlying web page. Certain defenses are based on the idea that these patterns can be changed and rendered unidentifiable by sending dummy *padding packets* that do not correspond to the actual data the web browser needs to display the web page. These are called *padding-only defenses*.

Tor has implemented a circuit padding framework (described [here](https://torproject.gitlab.io/torspec/padding-spec.html){:target="_blank"}) in their C codebase. It uses non-deterministic finite state machines to represent padding-only defenses, where *events* describe what is happening on a connection and *actions* result in padding packets being sent. However, it is limited in its ability to express even padding-only defenses, and based on insights from [prior work]({% post_url 2022-11-07-padding-only-defenses %}), it would be desirable to include features such as blocking of packets - artificially induced latency - for better protection and support for more defenses. The Maybenot framework is based on these ideas; it is a standalone state machine framework, built in Rust, which can be included as a library and used to represent both padding and blocking defenses with probabilistic finite state machines.

**Description:** The paper describes the Maybenot framework, a bare-bones simulator, and evaluation of some sample defenses from my bachelor's thesis. A technical report which specifies the framework in more detail is available on [arXiv](https://arxiv.org/abs/2304.09510){:target="_blank"}.

[Link to paper](/assets/pdf/2023-wpes.pdf){:target="_blank"}
