---
title: "Maybenot: A Framework for Traffic Analysis Defenses"
description: Proceedings of the 22nd Workshop on Privacy in the Electronic Society
date: 2023-11-26 12:18:19 +0200
categories: [publications]
tags: [research, lang-en]
lang: sv
---

**Bakgrund:** Identifiering av webbplatser via fingeravtryck (en krånglig översättning av engelskans *website fingerprinting*) är en grupp metoder som syftar till att identifiera vilka sajter en användare besöker genom en krypterad tunnel (tänk VPN eller Tor). Ett vanligt scenario är att någon angripare avlyssnar länken mellan användarens dator och tunnelns ingångspunkt, fångar in den krypterade trafiken och listar ut vilken webbsida den motsvarar med hjälp av klassificeringsmodeller. Detta fungerar på grund av att trafiken, trots kryptering, innehåller vissa mönster som kännetecknar den underliggande webbsidan. Vissa åtgärder – så kallade försvar – går ut på att dessa mönster kan förändras och göras oidentifierbara genom att skicka fyllnadspaket (*padding packets*) som inte tillhör den riktiga datan som webbläsaren behöver för att visa upp webbsidan. De kallas fyllnadsbaserade försvar (*padding-only defenses*).

Tor har implementerat ett ramverk för fyllnaden av kretsar (*circuit-padding framework*, beskrivet [här](https://torproject.gitlab.io/torspec/padding-spec.html){:target="_blank"}) i sin C-kod. Det använder icke-deterministiska ändliga tillståndsmaskiner för att representera fyllnadsbaserade försvar, där *event* beskriver händelser i anslutningen och *aktioner* resulterar i att fyllnadspaket skickas. Ramverket är dock begränsat vad gäller sitt stöd för olika försvar - inte ens vissa fyllnadsbaserade försvar kan implementeras - och [tidigare studier]({% post_url 2022-11-07-padding-only-defenses %}) pekar på att det vore önskvärt att koda in funktioner som möjliggör blockering av paket - avsiktlig artificiell fördröjning - för att bättre skydda mot trafikanalysis och stödja flera försvar. Ramverket [Maybenot]({% post_url 2023-11-26-maybenot-framework %}) har sitt ursprung i dessa idéer. Det är ett självständigt bibliotek skrivet i Rust som kan inkluderas i vilket program som helst och tillämpar en förbättrad modell som kan representera både fyllnads- och blockeringsbaserade försvar som probabilistiska ändliga tillståndsmaskiner.

**Beskrivning:** Artikeln beskriver Maybenot, en enkel simulator för preliminär evaluering och ett par försvar från min kandidatuppsats. En teknisk rapport som specificerar ramverket i större detalj är tillgänglig på [arXiv](https://arxiv.org/abs/2304.09510){:target="_blank"}.

[Här hittar du artikeln](/assets/pdf/2023-wpes.pdf){:target="_blank"}
