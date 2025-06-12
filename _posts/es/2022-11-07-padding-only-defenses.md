---
title: Padding-only Defenses Add Delay in Tor
description: Proceedings of the 21st Workshop on Privacy in the Electronic Society
date: 2022-11-07 08:06:16 +0200
categories: [publications]
tags: [research, lang-en]
lang: es
---

**Contexto:** El término "huella digital de sitios web" (*website fingerprinting*) se refiere a varias técnicas para identificar el sitio web al que un usuario está navigando, a tráves del tráfico de datos cifrado que se envía entre la computadora del usuario y un servidor intermedio (puede ser una VPN o un nodo de la red Tor) en camino al o del servidor web. Esto funciona porque el tráfico de datos contiene varios patrones reconocibles resultados de la composición y otras características únicas de cada página web. El proceso de identificación suele involucrar la IA en la forma de modelos de clasificación. Algunas defensas contra el *website fingerprinting* se basan únicamente en el uso de paquetes de relleno (*padding packets*), es decir, la inyección de paquetes adicionales en el tráfico de datos para cambiar sus patrones. Tales defensas se conocen como defensas sólo relleno (*padding-only defenses*).

**Descripción:** Este artículo es una crítica del supuesto común que defensas sólo relleno no causen atrasos en el envío del tráfico de datos y, por consecuencia, que el usuario tenga que esperar más para descargar una página web, lo cual no es deseable porque resulta en que no tantas personas quisieran emplear defensas. Hacemos experimentos con el simulador de redes Shadow para proveer evidencia que indica que defensas sólo relleno sí ocasionan atrasos, cuando se aplican a gran escala en Tor. Recomendamos en las conclusiones que se consideren con seriosidad defensas que de manera explícita utilicen atrasos para mejorar la privacidad.

[Aquí encuentras el artículo](/assets/pdf/2022-wpes.pdf){:target="_blank"}
