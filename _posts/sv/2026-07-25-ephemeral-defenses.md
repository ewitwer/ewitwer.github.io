---
title: "Ephemeral Network-Layer Fingerprinting Defenses"
description: Proceedings on Privacy Enhancing Technologies
date: 2026-07-25 00:00:00 +0200
categories: [publications]
tags: [research, lang-en]
lang: sv
---

**Bakgrund:** *Website fingerprinting* är ett sätt att ta reda på vilka webbplatser en person besöker genom en krypterad tunnel (tänk VPN eller Tor-nätverket). Ett vanligt scenario är att en angripare avlyssnar länken mellan personens dator och tunnelns ingångspunkt, fångar in den krypterade trafiken och sedan listar ut vilken webbsida den motsvarar med hjälp av klassificeringsmodeller. Detta är möjligt på grund av att webbtrafik, trots kryptering, innehåller mönster som kännetecknar det underliggande innehållet.

De flesta föreslagna åtgärder – så kallade försvar – utvärderas genom att de ställs mot en angripare som har tillgång till trafik som är skyddad av försvaret och kan träna klassificeringsmodeller på den. Angriparen antas med andra ord veta vilket försvar en person använder och hur det är uppbyggt.

**Sammanfattning:** Artikeln beskriver ett system som kan snabbt generera tillfälliga, anslutningsbundna försvar för Maybenot-ramverket, vilket tar bort angriparens möjlighet att träna på skyddad trafik. Detta kan ses som en tillämpning av Kerckhoffs princip på försvar mot trafikanalys, där försvaret betraktas som en nyckel. Simuleringar indikerar att de genererade försvaren fungerar väl i ett flertal scenarion (website fingerprinting, video fingerprinting och handskakningar i Tor) och kan nå en rimlig balans mellan effektivitet och belastning på nätverket. Försvaren behöver inte heller vara begränsade till att skydda mot förvalda attacker eller i specifika situationer/nätverksförhållanden.


[Link to paper](/assets/pdf/2026-pets.pdf){:target="_blank"}
