---
solution: Journey Optimizer
product: journey optimizer
title: Profielbeheer
description: Leer hoe u profielinvoer beheert
feature: Journeys
role: User
level: Intermediate
keywords: terugkeer, reis, profiel, terugkerend
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: c235e7cd77e50a15a12f6ed14e51ca4185ecb7c2
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Profielbeheer {#entry-management}

Nieuwe reizen zijn standaard geschikt voor herbinnenkomst. U kunt de optie uitschakelen voor &#39;één opname&#39;-reizen, bijvoorbeeld als u een eenmalige gift wilt aanbieden wanneer een persoon een winkel betreedt. In dat geval, wilt u niet de klant de reis kunnen opnieuw ingaan en de aanbieding opnieuw ontvangen.

![](assets/journey-re-entrance.png)

Wanneer een reis eindigt, is zijn status **[!UICONTROL Closed]**. Nieuwe individuen kunnen de reis niet meer betreden. Personen die al op reis zijn, maken de reis normaal af.

Na de standaard globale onderbreking van 30 dagen, schakelt de reis naar **Voltooid** status.  [Meer informatie](journey-gs.md#global_timeout).


## Eenheidstreizen{#entry-unitary}

Eenheidstrajecten (te beginnen met een evenement of segmentkwalificatie) bevatten een geleider die voorkomt dat ritten voor dezelfde gebeurtenis meerdere keren ten onrechte worden gestart. De terugkeer van het profiel wordt tijdelijk geblokkeerd door gebrek gedurende 5 minuten. Als bijvoorbeeld een evenement om 12.01 uur een reis voor een bepaald profiel start en een ander om 12.03 uur aankomt (ongeacht of het dezelfde gebeurtenis is of een andere gebeurtenis die dezelfde reis veroorzaakt), zal die reis niet opnieuw beginnen voor dit profiel.

Daarnaast:

* Als re-entry wordt toegelaten, kan een profiel een reis verscheidene keren ingaan, maar kan het niet doen tot zij dat vorige geval van de reis volledig verlaten.

* Als re-entry gehandicapt is, kan een profiel niet veelvoudige tijden de zelfde reis ingaan

## Reizen van segmenten lezen{#entry-read-segment}

In een leesegment reis:

* Voor eenmalige ritten: het profiel wordt slechts eenmaal ingevoerd .

* Voor terugkerende ritten: het profiel gaat de reis op elke herhaling in, als zij in het segment/verwachte status zijn. Als ze nog onderweg waren vanaf een eerdere herhaling, zullen ze deze vanaf het begin opnieuw starten.

Bij zakelijke gebeurtenissenreizen die beginnen met een **Segment lezen** activiteit: wetende dat deze reis op de ontvangst van een bedrijfsgebeurtenis gebaseerd is, als het profiel in het verwachte segment wordt gekwalificeerd, zullen zij de reis voor elke ontvangen bedrijfsgebeurtenis ingaan, die betekent dat dit profiel veelvoudige tijden in de zelfde reis, tezelfdertijd, maar in de context van verschillende bedrijfsgebeurtenissen kan zijn.