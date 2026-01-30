---
title: Afbakening en beperkingen
description: Meer informatie over beslissingsinstructies en -beperkingen.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
version: Journey Orchestration
source-git-commit: 5be6ecd85b0b45e01f7a27e0ffc55a2c6a22bcea
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 6%

---

# Afbakening en beperkingen {#decisioning-guardrails}

Houd rekening met de volgende instructies en beperkingen om een optimaal gebruik van de beslissingsbevoegdheid te waarborgen.

De volledige lijst van [!DNL Journey Optimizer] guardrails &amp; beperkingen is beschikbaar in [&#x200B; deze sectie &#x200B;](../start/guardrails.md).

## Beslissingsverzoeken {#decision-requests}

| Guardrail | Limiet |
| ------- | ------- |
| Op code gebaseerde API-aanvraag voor ervaring met beslissingsbeleid met Edge-segmentatie | 1500 |
| Op code gebaseerde API-aanvraag voor ervaring met beslissingsbeleid waarbij Edge-segmentatie niet wordt gebruikt | 5000 |
| Max. aantal oppervlakte-URI&#39;s per Edge-beslissingsverzoek | 30 |

## Beslissingsitems {#decision-items}

| Guardrail | Limiet |
| ------- | ------- |
| Totaal aantal beslissingsitems | 10K |
| Maximale grootte van items inclusief kenmerken (1 kB), max. 30 kenmerken | 1 kB |
| Frequentieregels - Maximumaantal bijschriftregels per beslissingsitem | 10 |

## Itemverzamelingen {#item-collections}

| Guardrail | Limiet |
| ------- | ------- |
| Items verzamelen | 10K |
| Totaal aantal beslissingspunten per collectie | 500 |

## Beslissingsbeleid {#decision-policy}

| Guardrail | Limiet |
| ------- | ------- |
| Aantal selectiestrategieën en handmatige items per beslissingsbeleid | 10 |
| Max. aantal besluitvormingsitems geretourneerd per beslissingsbeleid | 30 |

## Subsidiabiliteitsregels {#eligibility-rules}

| Guardrail | Limiet |
| ------- | ------- |
| Totaal aantal besluitvormingsregels en rangschikkingsformules | 10K gecombineerd |
| Maximumaantal profielkenmerken per regel | 25 |
| Max. aantal kenmerken van contextgegevens per regel | 30 |
| Maximale grootte van de pql-regel | 15 K (UTF-8) |
| Max. aantal nestniveaus | 30 |

## Beoordelingsformule {#ranking-formulas}

| Guardrail | Limiet |
| ------- | ------- |
| Maximale grootte van de rangschikkingsformule PQL | 8 K (UTF-8) |
| Max. aantal profielkenmerken | 25 |
| Max. aantal kenmerken van contextgegevens | 30 |
| Max. aantal nestniveaus | 30 |

## Overige {#others}

| Guardrail | Limiet |
| ------- | ------- |
| Aantal aangepaste kenmerken per itemcatalogusschema | 100 |
| Totaal aantal plaatsen | 1K |
| AI-waarderingsmodel | 5 |

## Configuraties {#configurations}

Het totale aantal configuraties dat Beslissende steun kan niet 20.000 overschrijden.

De totale configuratiegraad is het totale aantal [&#x200B; het begrenzen regels &#x200B;](items.md#capping) die in uw zandbak bestaan.
