---
title: Afbakening en beperkingen
description: Meer informatie over beslissingsinstructies en -beperkingen.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 8%

---

# Afbakening en beperkingen {#decisioning-guardrails}

Houd rekening met de volgende instructies en beperkingen om een optimaal gebruik van de beslissingsbevoegdheid te waarborgen.

De volledige lijst van [!DNL Journey Optimizer] guardrails &amp; beperkingen is beschikbaar in [ deze sectie ](../start/guardrails.md).

## Beslissingsverzoeken {#decision-requests}

| Guardrail | Limiet |
| ------- | ------- |
| Op code gebaseerde API-aanvraag voor ervaring met beslissingsbeleid met Edge-segmentatie | 1500 |
| Op code gebaseerde API-aanvraag voor ervaring met beslissingsbeleid waarbij Edge-segmentatie niet wordt gebruikt | 5000 |

## Itemverzamelingen {#item-collections}

| Guardrail | Limiet |
| ------- | ------- |
| Items verzamelen | 10K |
| Totaal aantal aanbiedingen per objectverzameling | 500 |

## Beslissingsbeleid {#decision-policy}

| Guardrail | Limiet |
| ------- | ------- |
| Aantal selectiestrategieën en handmatige items per beslissingsbeleid | 10 |
| Maximumaantal aangeboden objecten per beslissingsbeleid | 30 |

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
| Aantal aangepaste kenmerken per catalogusschema van aanbiedingen | 100 |
| Totaal aantal aangeboden objecten | 10K |
| Totaal aantal plaatsen | 1K |
| AI-waarderingsmodel | 5 |
| Frequentieregels - Maximumaantal regels voor aftopping per aanbieding | 10 |
