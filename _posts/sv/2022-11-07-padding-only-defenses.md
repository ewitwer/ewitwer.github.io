---
title: Padding-only Defenses Add Delay in Tor
description: Proceedings of the 21st Workshop on Privacy in the Electronic Society
date: 2022-11-07 08:06:16 +0200
categories: [publications]
tags: [research, lang-en]
lang: sv
---

**Bakgrund:** Identifiering av webbplatser via fingeravtryck (en krånglig översättning av engelskans *website fingerprinting*) är en grupp metoder som syftar till att identifiera vilka sajter en användare besöker genom en krypterad tunnel (tänk VPN eller Tor). Ett vanligt scenario är att någon angripare avlyssnar länken mellan användarens dator och tunnelns ingångspunkt, fångar in den krypterade trafiken och listar ut vilken webbsida den motsvarar med hjälp av klassificeringsmodeller. Detta fungerar på grund av att trafiken, trots kryptering, innehåller vissa mönster som kännetecknar den underliggande webbsidan. Vissa åtgärder – så kallade försvar – går ut på att dessa mönster kan förändras och göras oidentifierbara genom att skicka fyllnadspaket (*padding packets*) som inte tillhör den riktiga data som webbläsaren behöver för att visa upp webbsidan. De kallas fyllnadsbaserade försvar (*padding-only defenses*).

**Beskrivning:** Artikeln är en kritik av det vanliga antagandet att fyllnadsbaserade försvar inte orsakar fördröjningar i trafiken och att användaren därför inte behöver vänta längre på att en webbsida ska laddas, något som man helst vill undvika med tanke på att färre personer kommer använda försvar om deras upplevelse försämras. Vi gör experiment med nätverkssimulatorn Shadow för att visa att fyllsnadsbaserade försvar faktiskt skapar fördröjningar när de rullas ut i stor skala i Tor. Vi rekommenderar slutligen att systemutvecklare inte utesluter försvar som medvetet skapar fördröjningar då de kan erbjuda bättre integritetsskydd än fyllnadsbaserade försvar som ändå ligger till grund för fördröjningar i verkligheten.

[Här hittar du artikeln](/assets/pdf/2022-wpes.pdf){:target="_blank"}
