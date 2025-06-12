---
title: "Maybenot: A Framework for Traffic Analysis Defenses"
description: Proceedings of the 22nd Workshop on Privacy in the Electronic Society
date: 2023-11-26 12:18:19 +0200
categories: [publications]
tags: [research, lang-en]
lang: es
---

**Contexto:** El término "huella digital de sitios web" (*website fingerprinting*) se refiere a varias técnicas para identificar el sitio web al que un usuario está navigando, a tráves del tráfico de datos cifrado que se envía entre la computadora del usuario y un servidor intermedio (puede ser una VPN o un nodo de la red Tor) en camino al o del servidor web. Esto funciona porque el tráfico de datos contiene varios patrones reconocibles resultados de la composición y otras características únicas de cada página web. El proceso de identificación suele involucrar la IA en la forma de modelos de clasificación. Algunas defensas contra el *website fingerprinting* se basan únicamente en el uso de paquetes de relleno (*padding packets*), es decir, la inyección de paquetes adicionales en el tráfico de datos para cambiar sus patrones. Tales defensas se conocen como defensas sólo relleno (*padding-only defenses*).

Tor ha lanzado un sistema para el relleno de circuitos (*circuit padding framework*, describido [aquí](https://torproject.gitlab.io/torspec/padding-spec.html){:target="_blank"}) en su código C. Representa defensas sólo relleno por medio de autómatas finitos no deterministas, en los cuales *eventos* describen lo que sucede en la conexión y *acciones* resultan en que paquetes de relleno se envíen. Sin embargo, el sistema tiene limitaciones en cuanto a las defensas que pueden ser implementadas en él - ni siquiera algunas defensas sólo relleno se encuentran en esta categoría - y [estudios previos]({% post_url 2022-11-07-padding-only-defenses %}) ilustran que sería deseable incluir funciones tales como el bloqueo de paquetes - la introducción artificial de atrasos - para aumentar la protección contra ataques y posibilitar la implementación de más defensas. El sistema [Maybenot]({% post_url 2023-11-26-maybenot-framework %}) tiene su base en estas ideas. Es una biblioteca escrita en Rust que puede ser incluida en cualquier aplicación y ofrece herramientas para implementar defensas de relleno y bloqueo con autómatas probabilísticos.

**Descripción:** El artículo describe Maybenot, un simulador básico para evaluaciones preliminares y algunas defensas que evalué para mi tesis de licenciatura. Un reporte técnico que especifica el sistema con más detalles está disponible en [arXiv](https://arxiv.org/abs/2304.09510){:target="_blank"}.

[Aquí encuentras el artículo](/assets/pdf/2023-wpes.pdf){:target="_blank"}
