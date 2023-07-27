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
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 1%

---


# Profielbeheer {#entry-management}

Er zijn twee belangrijke soorten reizen:

* op gebeurtenissen gebaseerde reizen: om te beginnen met een evenement, zijn deze reizen uniform, ze zijn verbonden met één persoon. Wanneer het evenement wordt ontvangen, komt de persoon de reis binnen. [Meer informatie](#entry-unitary)
* leest u eens voor wat u moet lezen : om te beginnen met een leestoond , zijn dit batchreizen . Personen die tot het publiek behoren, nemen allemaal dezelfde reis. Deze reizen kunnen terugkeren of eenmalig zijn. [Meer informatie](#entry-read-segment)

In beide reistypes kan een profiel niet meerdere keren tegelijk aanwezig zijn in dezelfde reis.

## Eenheidstreizen{#entry-unitary}

Bij unitaire reizen kunt u het opnieuw betreden in- of uitschakelen:

* Als re-entry wordt toegelaten, kan een profiel een reis verscheidene keren ingaan, maar kan het niet doen tot hij dat vorige geval van de reis volledig verliet.

* Als re-entry gehandicapt is, kan een profiel niet veelvoudige tijden de zelfde reis ingaan

Nieuwe reizen zijn standaard geschikt voor herbinnenkomst. U kunt de optie uitschakelen voor &#39;één opname&#39;-reizen, bijvoorbeeld als u een eenmalige gift wilt aanbieden wanneer een persoon een winkel betreedt. In dat geval, wilt u niet de klant de reis kunnen opnieuw ingaan en de aanbieding opnieuw ontvangen. Wanneer een reis eindigt, is zijn status **[!UICONTROL Closed]**. Nieuwe individuen kunnen niet langer de reis betreden. Personen die al op reis zijn, maken de reis normaal af. [Meer informatie](journey-gs.md#entrance)

![](assets/journey-re-entrance.png)

Na de standaard globale onderbreking van 30 dagen, schakelt de reis naar **Voltooid** status. Nieuwe individuen kunnen niet langer de reis betreden. Personen die al op reis zijn, maken de reis normaal af.Vanwege de 30-daagse reistijd, wanneer het niet is toegestaan om de reis opnieuw te betreden, kunnen we er niet voor zorgen dat de heringstop meer dan 30 dagen werkt. Aangezien we alle informatie over personen die 30 dagen na hun binnenkomst de reis hebben betreden, verwijderen, kunnen we niet weten dat de persoon eerder, meer dan 30 dagen geleden, is binnengekomen. [Meer informatie](journey-gs.md#global_timeout).

Eenheidstrajecten (te beginnen met een evenement of een kwalificatie van het publiek) bevatten een begeleidend element dat voorkomt dat ritten bij dezelfde gebeurtenis meerdere keren ten onrechte worden gestart. De terugkeer van het profiel wordt tijdelijk geblokkeerd door gebrek gedurende 5 minuten. Als bijvoorbeeld een evenement om 12.01 uur een reis voor een bepaald profiel start en een ander om 12.03 uur aankomt (ongeacht of het dezelfde gebeurtenis is of een andere gebeurtenis die dezelfde reis veroorzaakt), zal die reis niet opnieuw beginnen voor dit profiel.

De sleutel wordt ook gebruikt om te controleren of een persoon op reis is. Een persoon kan namelijk niet op twee verschillende plaatsen op dezelfde reis zijn. Als gevolg hiervan staat het systeem niet toe dat dezelfde sleutel, bijvoorbeeld de sleutel CRMID=3224, zich op verschillende plaatsen op dezelfde reis bevindt.

## Reizen voor het publiek lezen{#entry-read-segment}

In een leestoegang:

* Voor niet-terugkerende ritten: het profiel komt slechts eenmaal binnen.

* Voor terugkerende reizen: standaard komen alle profielen van de doelgroep op elke terugkerende reis in. Ze moeten de reis afmaken voordat ze in een ander voorval kunnen terugkeren.

>[!NOTE]
>
>Er zijn twee opties beschikbaar voor terugkerende publiekstrajecten. De **Herkomst forceren bij herhaling** met deze optie worden alle profielen die nog aanwezig zijn op de reis automatisch afgesloten bij de volgende uitvoering. De **Incrementeel lezen** deze optie is alleen van toepassing op de personen die sinds de laatste uitvoering van de reis in het publiek zijn gekomen . Zie dit [sectie](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

Bij zakelijke gebeurtenissenreizen die beginnen met een **Lees publiek** activiteit: wetende dat deze reis op de ontvangst van een bedrijfsgebeurtenis gebaseerd is, als het profiel in het verwachte publiek wordt gekwalificeerd, zullen zij de reis voor elke ontvangen bedrijfsgebeurtenis ingaan, die betekent dat dit profiel veelvoudige tijden in de zelfde reis, tezelfdertijd, maar in de context van verschillende bedrijfsgebeurtenissen kan zijn.