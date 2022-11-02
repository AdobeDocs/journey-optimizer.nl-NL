---
solution: Journey Optimizer
product: journey optimizer
title: Profielbeheer
description: Leer hoe u profielinvoer beheert
feature: Journeys
role: User
level: Intermediate
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Profielbeheer {#entry-management}

Op een eengemaakte reis:

* Als re-entry wordt toegelaten, kan een profiel een reis verscheidene keren ingaan, maar kan het niet doen tot hij dat vorige geval van de reis volledig verliet.

* Als re-entry gehandicapt is, kan een profiel niet veelvoudige tijden de zelfde reis ingaan

Raadpleeg deze voor meer informatie over het opnieuw invoeren van profielen [sectie](../building-journeys/journey-gs.md#change-properties).

In een leesegment reis:

* Voor eenmalige ritten: het profiel wordt slechts eenmaal ingevoerd .
* voor terugkerende ritten: het profiel gaat de reis op elke herhaling in, als hij zich in het segment/de verwachte status bevindt. Als hij nog onderweg was van een eerdere herhaling, zal hij het vanaf het begin opnieuw starten.

In zakelijke gebeurtenissenritten die beginnen met een leesegment:

In het besef dat deze reis gebaseerd is op de ontvangst van een bedrijfsevenement, als het profiel in het verwachte segment gekwalificeerd is, zal hij de reis voor elke ontvangen bedrijfsgebeurtenis ingaan, die betekent dat dit profiel veelvoudige tijden in de zelfde reis, tezelfdertijd, maar in de context van verschillende bedrijfsgebeurtenissen kan zijn.

Eenheidstrajecten (te beginnen met een evenement of segmentkwalificatie) bevatten een geleider die voorkomt dat ritten voor dezelfde gebeurtenis meerdere keren ten onrechte worden gestart. De terugkeer van het profiel wordt tijdelijk geblokkeerd door gebrek gedurende 5 minuten. Als bijvoorbeeld een evenement om 12.01 uur een reis voor een bepaald profiel start en een ander om 12.03 uur aankomt (ongeacht of het dezelfde gebeurtenis is of een andere gebeurtenis die dezelfde reis veroorzaakt), zal die reis niet opnieuw beginnen voor dit profiel.
