---
title: Beheersbeheerinstructies en beperkingen
description: Meer informatie over richtlijnen en beperkingen voor het beheer van beslissingen.
badge: label="Verouderd" type="Informative"
feature: Decisioning
role: User
level: Intermediate
exl-id: d2872bd3-42f8-4744-bb5b-41c49340098a
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 6%

---

# Beheersbeheerinstructies en beperkingen {#decision-management-guardrails}

Houd rekening met de volgende voorzorgsmaatregelen en beperkingen om een optimaal gebruik van het besluitvormingsbeheer te waarborgen.

De volledige lijst van [!DNL Journey Optimizer] guardrails &amp; beperkingen is beschikbaar in [ deze sectie ](../start/guardrails.md).

## Beslissingsverzoeken

De leveringstijd komt overeen met het aantal beslissingsreacties dat binnen een bepaalde tijd door de app-service van het beslissingsbeheer kan worden geleverd.

| Guardrail | Limiet |
| ------- | ------- |
| API-aanvragen voor besluitvorming per seconde | 500 per organisatie |
| Edge-API-aanvragen voor besluitvorming per seconde met Edge Segmentation | 1.500 per organisatie |
| Edge-API-aanvragen voor besluitvorming per seconde zonder Edge-segmentatie | 5.000 per organisatie |
| Teruggestuurde voorstellen per reactie | Maximaal 30 per beslissingsbereik of 100 in totaal |
| Maximumaantal biedregels per aanvraag | 100 |

## Besluiten

| Guardrail | Limiet |
| ------- | ------- |
| Totaal besluiten | 10K |
| Live beslissingen | 1K |
| Plaatsingen per beslissing | 30 |

## Verzamelingen

| Guardrail | Limiet |
| ------- | ------- |
| Aanbiedingen per verzameling | 500 |
| Verzamelingen | 10K |
| Verzamelingen per beslissing | 30 |

## Verzamelingsaanduidingen

| Guardrail | Limiet |
| ------- | ------- |
| Verzamelingskwalificatie per aanbieding of verzameling | 20 |
| Totaal aantal verzamelingskwalificaties | 1.000 |

## Aanbiedingen

| Guardrail | Limiet |
| ------- | ------- |
| Totaal aantal aanbiedingen | 10K |
| Max aantal van **actieve** aanbiedingen per zandbak | 10K |
| Maximale grootte van aanbiedingen inclusief kenmerken (1 kB), max. 30 kenmerken | 1 kB |
| Maximale representatiegrootte aanbieding (totaal voor alle stages) | 1 kB |

## Subsidiabiliteitsregels

| Guardrail | Limiet |
| ------- | ------- |
| Totale besluitvormingsregels en rangschikkingsformules | 10K gecombineerd |
| Maximumaantal profielkenmerken per regel | 25 |
| Max. aantal kenmerken van contextgegevens per regel | 30 |
| Maximale grootte van PQL-regel | 15 K (UTF-8) |
| Max. aantal nestniveaus | 30 |

## Beoordelingsformule

| Guardrail | Limiet |
| ------- | ------- |
| Maximale grootte van de rangschikkingsformule PQL | 8 K (UTF-8) |
| Max. aantal profielkenmerken | 25 |
| Max. aantal kenmerken van contextgegevens | 30 |
| Max. aantal nestniveaus | 30 |

## Overige

| Guardrail | Limiet |
| ------- | ------- |
| Plaatsen | 1000 |
| AI-classificatiemodel | 5 |
| Frequentiecorrectie - Maximumaantal bijschriftregels per aanbieding | 10 |

## Configuraties {#configurations}

Het totale aantal configuraties dat door het beheer van Besluit wordt ondersteund, mag niet meer bedragen dan 20.000.

De totale configuratiegraad is het totale aantal [ het begrenzen regels ](offer-library/add-constraints.md#capping) die in uw zandbak bestaan. Voor elke het in kaart brengen regel die over alle [ plaatsen ](offer-library/creating-placements.md) wordt toegepast, moet de regel over alle plaatsen worden vermenigvuldigd verbonden aan de gespecificeerde aanbieding.
