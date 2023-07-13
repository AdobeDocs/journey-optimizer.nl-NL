---
solution: Journey Optimizer
product: journey optimizer
title: Gebeurtenissen van Audience Qualification
description: Meer informatie over kwalificatiegebeurtenissen voor het publiek
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: kwalificatie, evenementen, publiek, reis, platform
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 0%

---

# Gebeurtenissen van Audience Qualification {#segment-qualification}

## Informatie over publiekskwalificatiegebeurtenissen{#about-segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Kwalificatiegebeurtenissen voor het publiek"
>abstract="Met deze activiteit kunt u luisteren naar de inzendingen en uitgangen van profielen in Adobe Experience Platform-kijkers om ervoor te zorgen dat individuen op reis gaan of vooruit gaan."

Met deze activiteit kunt u luisteren naar de inzendingen en uitgangen van profielen in Adobe Experience Platform-kijkers om ervoor te zorgen dat individuen op reis gaan of vooruit gaan. Raadpleeg de volgende secties voor meer informatie over het maken van doelgroepen [sectie](../audience/about-audiences.md).

Laten we zeggen dat je een &quot;zilveren klant&quot; publiek hebt. Met deze activiteit, kunt u alle nieuwe zilveren klanten een reis maken en hen een reeks gepersonaliseerde berichten verzenden.

Dit type gebeurtenis kan als eerste stap of later in de reis worden geplaatst.

>[!IMPORTANT]
>
>Onthoud dat het publiek in Adobe Experience Platform één keer per dag wordt berekend (**partij** publiek) of in realtime (**gestreamd** publiek, met gebruik van de optie Frequentie publiek van Adobe Experience Platform).
>
>Als het geselecteerde publiek wordt gestreamd, zullen de individuen die tot dit publiek behoren de reis in real time kunnen betreden. Als het publiek een batch is, kunnen mensen die net voor dit publiek zijn gekwalificeerd de reis invoeren wanneer de publieksberekening op Adobe Experience Platform wordt uitgevoerd.
>
>U kunt gebeurtenisveldgroepen niet gebruiken voor reizen die beginnen met een leespubliek, een kwalificatie Audience of een activiteit voor een zakelijke gebeurtenis.


1. De **[!UICONTROL Events]** categorie en zet een **[!UICONTROL Audience Qualification]** op uw canvas.

   ![](assets/segment5.png)

1. Voeg een **[!UICONTROL Label]** aan de activiteit. Deze stap is optioneel.

1. Klik in het dialoogvenster **[!UICONTROL Audience]** en selecteer het publiek dat u wilt gebruiken.

   >[!NOTE]
   >
   >U kunt de kolommen in de lijst aanpassen en sorteren.

   ![](assets/segment6.png)

   Als het publiek eenmaal is toegevoegd, wordt de opdracht **[!UICONTROL Copy]** kunt u de naam en de id kopiëren:

   `{"name":"Loyalty membership“,”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. In de **[!UICONTROL Behaviour]** , kiest u of u wilt luisteren naar de publieksinvoer, de uitgang of beide.

   >[!NOTE]
   >
   >Let op: **[!UICONTROL Enter]** en **[!UICONTROL Exit]** komt overeen met de **Gerealiseerd** en **Verlaat** statistieken over de participatie van het publiek in Adobe Experience Platform. Raadpleeg voor meer informatie over het evalueren van een publiek de [Documentatie voor segmentatieservice](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

1. Selecteer een naamruimte. Dit is alleen nodig als de gebeurtenis als eerste stap van de reis wordt geplaatst. Het veld wordt standaard voorgevuld met de laatst gebruikte naamruimte.

   >[!NOTE]
   >
   >U kunt alleen een naamruimte selecteren die is gebaseerd op personen. Als u een naamruimte voor een opzoektabel hebt gedefinieerd (bijvoorbeeld: ProductID-naamruimte voor een productzoekopdracht), is deze niet beschikbaar in het dialoogvenster **Naamruimte** vervolgkeuzelijst.

   ![](assets/segment7.png)

De nuttige lading bevat de volgende contextinformatie, die u in voorwaarden en acties kunt gebruiken:

* het gedrag (ingang, uitgang)
* het tijdstempel van de kwalificatie
* de publieks-id

Wanneer u de expressieeditor gebruikt in een voorwaarde of handeling die volgt op een **[!UICONTROL Audience Qualification]** activiteit, hebt u toegang tot **[!UICONTROL AudienceQualification]** knooppunt. U kunt kiezen tussen **[!UICONTROL Last qualification time]** en de **[!UICONTROL status]** (Enter of exit).

Zie [Condition-activiteit](../building-journeys/condition-activity.md#about_condition).

![](assets/segment8.png)

Een nieuwe reis die een publiekskwalificatiegebeurtenis omvat is operationeel tien minuten nadat u het hebt gepubliceerd. Dit tijdinterval beantwoordt aan het geheime voorgeheugen verfrist interval van de specifieke dienst. Daarom moet u tien minuten wachten voordat u deze reis gebruikt.

## Best practices {#best-practices-segments}

De **[!UICONTROL Audience Qualification]** door deze activiteit kunnen personen die gekwalificeerd of gediskwalificeerd zijn voor een Adobe Experience Platform-publiek onmiddellijk worden toegelaten tot de reis.

De ontvangstsnelheid van deze informatie is hoog. Uit de uitgevoerde metingen blijkt een snelheid van 10.000 ontvangen gebeurtenissen per seconde. Als gevolg hiervan moet u er zeker van zijn dat u begrijpt hoe pieken in de toegang kunnen optreden, hoe u ze kunt vermijden en hoe u uw reis voor hen gereed kunt maken.

### Batchpubliek{#batch-speed-segment-qualification}

Wanneer het gebruiken van publiekskwalificatie voor een partijpubliek, merk op dat een piek van ingang op het tijdstip van de dagelijkse berekening zal gebeuren. De grootte van de piek hangt af van het aantal personen dat het publiek dagelijks binnenkomt (of verlaat).

Als het batchpubliek bovendien pas wordt gecreëerd en onmiddellijk wordt gebruikt in een reis, kan de eerste batch van de berekening een zeer groot aantal personen de reis binnenkomen.

### Gestroomd publiek{#streamed-speed-segment-qualification}

Wanneer het gebruiken van publiekskwalificatie voor gestroomd publiek, is er minder risico om grote pieken van ingangen/uitgangen te krijgen toe te schrijven aan de ononderbroken evaluatie van het publiek. Toch, als de publieksdefinitie ertoe leidt dat een groot volume van klanten tezelfdertijd kwalificeert, zou er ook een piekperiode kunnen zijn.

Raadpleeg voor meer informatie over streamingsegmentatie [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/streaming-segmentation.html#api)

### Overbelasting voorkomen{#overloads-speed-segment-qualification}

Hier volgen een paar voorbeelden van beste praktijken die zullen helpen om overladende systemen te vermijden leveraged in reizen (gegevensbronnen, douaneacties, kanaalactiviteiten).

Niet gebruiken in een **[!UICONTROL Audience Qualification]** , een batchgroep die direct na de creatie ervan aanwezig is. Hiermee wordt de eerste rekenpiek vermeden. Merk op dat er een gele waarschuwing in het reiscanvas zal zijn als u op het punt staat om een publiek te gebruiken dat nooit is berekend.

![](assets/segment-error.png)

Plaats een plafondregel voor gegevensbronnen en handelingen die tijdens reizen worden gebruikt om overbelasting te voorkomen. Meer informatie in [Journey Orchestration-documentatie](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html){target="_blank"}. De bijschilderregel hoeft niet opnieuw te worden uitgevoerd. Als u het opnieuw moet proberen, moet u een alternatief pad in de reis gebruiken door de doos te controleren **[!UICONTROL Add an alternative path in case of a timeout or an error]** in omstandigheden of acties.

Voordat u het publiek in een productiereis gaat gebruiken, moet u altijd eerst het aantal personen evalueren dat elke dag voor dit publiek in aanmerking komt. Om dit te doen, kunt u controleren **[!UICONTROL Audience]** menu, opent u het publiek en bekijkt u het **[!UICONTROL Profiles over time]** grafiek.

![](assets/segment-overload.png)
