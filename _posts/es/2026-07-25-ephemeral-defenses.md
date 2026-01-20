---
title: "Ephemeral Network-Layer Fingerprinting Defenses"
description: Proceedings on Privacy Enhancing Technologies
date: 2026-07-25 00:00:00 +0200
categories: [publications]
tags: [research, lang-en]
lang: es
---

**Contexto:** El término "huella digital de sitios web" (*website fingerprinting*) se refiere a varias técnicas para identificar el sitio web al que un usuario está navigando, a tráves del tráfico de datos cifrado que se envía entre la computadora del usuario y un servidor intermedio (puede ser una VPN o un nodo de la red Tor) en camino al o del servidor web. Esto funciona porque el tráfico de datos contiene patrones reconocibles resultados de la composición y otras características únicas de la página web. El proceso de identificación suele involucrar la IA en la forma de modelos de clasificación.

La mayoría de estudios sobre defensas contra el *website fingerprinting* evalúan su efectividad frente a un adversario capaz de entrenar modelos de clasificación sobre tráfico protegido. Es decir, estos estudios asumen implícitamente que el adversario conoce qué defensa el usuario utiliza y cómo funciona.

**Descripción:** El artículo presenta un sistema que genera defensas temporales que sólo se usarán en una conexión, lo cual elimina la posibilidad de entrenar modelos de clasificación sobre tráfico que está protegido con la misma defensa que el usuario objetivo tiene. Se puede considerar una aplicación del principio de Kerckhoffs, en la cual defensas se tratan como claves. Simulaciones indican que defensas temporales funcionan bien en varias situaciones (website fingerprinting, video fingerprinting y el handshake de circuitos en Tor) y que alcanzan un buen equilibrio entre efectividad y carga de la red. Las defensas no se limitan a ataques, situaciones o condiciones de red específicos.


[Link to paper](/assets/pdf/2026-pets.pdf){:target="_blank"}
