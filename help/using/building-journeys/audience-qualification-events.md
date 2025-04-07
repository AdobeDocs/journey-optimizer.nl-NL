---
solution: Journey Optimizer
product: journey optimizer
title: Gebeurtenissen in verband met de kwalificatie van het publiek
description: Leer hoe u kwalificatiegebeurtenissen voor het publiek gebruikt en configureert
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: kwalificatie, evenementen, publiek, reis, platform
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: ce05723342af3e0016965df7fb7a2e0b79856f6f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Gebeurtenissen in verband met de kwalificatie van het publiek {#segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="kwalificatiegebeurtenissen voor het publiek"
>abstract="Met deze activiteit kunt u luisteren naar de inzendingen en uitgangen van profielen in Adobe Experience Platform-kijkers om ervoor te zorgen dat individuen op reis gaan of vooruit gaan."

## Informatie over publiekskwalificatiegebeurtenissen{#about-segment-qualification}

Met deze activiteit kunt u luisteren naar de inzendingen en uitgangen van profielen in Adobe Experience Platform-kijkers om ervoor te zorgen dat individuen op reis gaan of vooruit gaan. Voor meer informatie over publieksverwezenlijking, verwijs naar deze [ sectie ](../audience/about-audiences.md).

Laten we zeggen dat je een &quot;zilveren klant&quot; publiek hebt. Met deze activiteit, kunt u alle nieuwe zilveren klanten een reis maken en hen een reeks gepersonaliseerde berichten verzenden.

Dit type gebeurtenis kan als eerste stap of later in de reis worden geplaatst.

➡️ [ ontdekt deze eigenschap in video ](#video)

### Belangrijke opmerkingen {#important-notes-segment-qualification}

* De reizen van de Kwalificatie van het publiek zijn hoofdzakelijk ontworpen om met het stromen publiek te werken: deze combinatie zal een betere ervaring in real time waarborgen. Wij adviseren sterk dat u slechts **het stromen publiek** in de activiteit van de Kwalificatie van het Publiek gebruikt.

  Nochtans, als u partij ingestie gebaseerde attributen in uw het stromen publiek, of een partijpubliek voor een reis van de Kwalificatie van het Publiek wilt gebruiken, overweeg de tijdspanwijdte voor publieksevaluatie/activering - een partijpubliek of het stromen publiek die partij ingebedde attributen gebruiken zou klaar moeten zijn om in **activiteit van de Kwalificatie van het Publiek op rond** te gebruiken **na voltooiing van uw segmentatietaak (deze baan die (deze die één dag in de tijd wordt bepaald door uw beheerder van de Adobe-organisatie).**

* Onthoud dat het publiek van Adobe Experience Platform of eens per dag (**partij** publiek) of in real time (voor **gestroomd** publiek wordt berekend, gebruikend de Hoge optie van het Publiek van de Frequentie van Adobe Experience Platform).

   * Als het geselecteerde publiek wordt gestreamd, zullen de individuen die tot dit publiek behoren de reis in real time kunnen betreden.
   * Als het publiek een batch is, kunnen mensen die net voor dit publiek zijn gekwalificeerd de reis invoeren wanneer de publieksberekening op Adobe Experience Platform wordt uitgevoerd.

  Als beste praktijken, adviseren wij daarom slechts het stromen publiek in de activiteit van de Kwalificatie van het publiek van het a **te gebruiken**. Voor de gevallen van het partijgebruik, gelieve te gebruiken a **[gelezen publiek](read-audience.md)** activiteit.

  >[!NOTE]
  >
  >Vanwege de batchaard van publiek dat is gemaakt met gebruik van compositieworkflows en aangepaste upload, kunt u deze soorten publiek niet als doelgroep instellen in de activiteit ‘Kwalificatie van publiek’. Alleen publiek dat is gemaakt met behulp van segmentdefinities kan in deze activiteit worden gebruikt.

* De groepen van het de gebeurtenisgebied van de ervaring kunnen niet in ritten worden gebruikt die met a **Gelezen Publiek**, a **de Kwalificatie van het Publiek** of a **BedrijfsGebeurtenis** activiteit beginnen.

* Wanneer het gebruiken van de Kwalificatie van het publiek **activiteit van het 0} {in een reis, kan die activiteit tot 10 minuten duren om actief te zijn en aan profielen te luisteren die of het publiek ingaan weggaan.**


Zie ook ](#best-practices-segments) hieronder de beste praktijken van de Kwalificatie van het publiek 0}.[

### De activiteit configureren {#configure-segment-qualification}

Voer de volgende stappen uit om de **[!UICONTROL Audience Qualification]** -activiteit te configureren:

1. Ontvouw de categorie **[!UICONTROL Events]** en zet een **[!UICONTROL Audience Qualification]** -activiteit neer op uw canvas.

   ![](assets/segment5.png)

1. Voeg een **[!UICONTROL Label]** toe aan de activiteit. Deze stap is optioneel.

1. Klik in het veld **[!UICONTROL Audience]** en selecteer het publiek dat u wilt gebruiken.

   >[!NOTE]
   >
   >U kunt de kolommen in de lijst aanpassen en sorteren.

   ![](assets/segment6.png)

   Nadat het publiek is toegevoegd, kunt u met de knop **[!UICONTROL Copy]** de naam en de id van het publiek kopiëren:

   `{"name":"Loyalty membership","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. Kies in het veld **[!UICONTROL Behaviour]** of u wilt luisteren naar de publieksinvoer, het afsluit of beide.

   >[!NOTE]
   >
   >Merk op dat **[!UICONTROL Enter]** en **[!UICONTROL Exit]** aan de **Realized** beantwoorden en **Uitgegeven** status van de publieksparticipatie van Adobe Experience Platform. Voor meer op hoe te om een publiek te evalueren, verwijs naar de [ documentatie van de Dienst van de Segmentatie ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results) {target="_blank"}.

1. Selecteer een naamruimte. Dit is alleen nodig als de gebeurtenis als eerste stap van de reis wordt geplaatst. Het veld wordt standaard voorgevuld met de laatst gebruikte naamruimte.

   >[!NOTE]
   >
   >U kunt alleen een naamruimte selecteren die is gebaseerd op personen. Als u een namespace voor een raadplegingslijst (bijvoorbeeld: ProductID namespace voor een raadpleging van het Product) hebt bepaald, zal het niet in **Namespace** dropdown lijst beschikbaar zijn.

   ![](assets/segment7.png)

De nuttige lading bevat de volgende contextinformatie, die u in voorwaarden en acties kunt gebruiken:

* het gedrag (ingang, uitgang)
* het tijdstempel van de kwalificatie
* de publieks-id

Wanneer u de expressie-editor gebruikt in een voorwaarde of handeling die volgt op een **[!UICONTROL Audience Qualification]** -activiteit, hebt u toegang tot het **[!UICONTROL AudienceQualification]** -knooppunt. U kunt kiezen tussen **[!UICONTROL Last qualification time]** en **[!UICONTROL status]** (Enter of exit).

Zie [ de activiteit van de Voorwaarde ](../building-journeys/condition-activity.md#about_condition).

![](assets/segment8.png)

Een nieuwe reis die een **gebeurtenis van de Kwalificatie van het Publiek** omvat is operationeel tien minuten nadat u het hebt gepubliceerd. Dit tijdinterval beantwoordt aan het geheime voorgeheugen verfrist interval van de specifieke dienst. Daarom moet u tien minuten wachten voordat u deze reis gebruikt.

## Best practices {#best-practices-segments}

De **[!UICONTROL Audience Qualification]** -activiteit maakt het mogelijk dat personen die gekwalificeerd of gediskwalificeerd zijn voor een Adobe Experience Platform-publiek, direct toegang krijgen tot de reis.

De ontvangstsnelheid van deze informatie is hoog. Uit de uitgevoerde metingen blijkt een snelheid van 10.000 ontvangen gebeurtenissen per seconde. Als gevolg hiervan moet u er zeker van zijn dat u begrijpt hoe pieken in de toegang kunnen optreden, hoe u ze kunt vermijden en hoe u uw reis voor hen gereed kunt maken.

### Batchpubliek {#batch-speed-segment-qualification}

Wanneer het gebruiken van de Kwalificatie van het Publiek voor een partijpubliek, merk op dat een piek van ingang op het tijdstip van de dagelijkse berekening zal gebeuren. De grootte van de piek hangt af van het aantal personen dat het publiek dagelijks binnenkomt (of verlaat).

Als het batchpubliek bovendien pas wordt gecreëerd en onmiddellijk wordt gebruikt in een reis, kan de eerste batch van de berekening een zeer groot aantal personen de reis binnenkomen.

### Gestroomd publiek {#streamed-speed-segment-qualification}

Wanneer het gebruiken van de Kwalificatie van het Publiek voor gestroomd publiek, is er minder risico om grote pieken van ingangen/uitgangen te krijgen toe te schrijven aan de ononderbroken evaluatie van het publiek. Toch, als de publieksdefinitie ertoe leidt dat een groot volume van klanten tezelfdertijd kwalificeert, zou er ook een piekperiode kunnen zijn.

Vermijd het gebruik van open en verzend gebeurtenissen met streaming segmentatie. In plaats daarvan, gebruik echte user-activity signalen zoals kliks, aankopen, of baken gegevens. Voor frequentie of suppression logica, gebruik bedrijfsregels eerder dan verzendt gebeurtenissen. [Meer informatie](../audience/about-audiences.md#open-and-send-event-guardrails)

Voor meer informatie bij het stromen segmentatie, verwijs naar [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/streaming-segmentation.html#api).

### Overbelasting voorkomen {#overloads-speed-segment-qualification}

Hier volgen een paar voorbeelden van beste praktijken die zullen helpen om overladende systemen te vermijden leveraged in reizen (gegevensbronnen, douaneacties, kanaalactiviteiten).

Gebruik in een **[!UICONTROL Audience Qualification]** -activiteit niet meteen na het maken een publiek in een batch. Hiermee wordt de eerste rekenpiek vermeden. Merk op dat er een gele waarschuwing in het reiscanvas zal zijn als u op het punt staat om een publiek te gebruiken dat nooit is berekend.

![](assets/segment-error.png)

Plaats een plafondregel voor gegevensbronnen en handelingen die tijdens reizen worden gebruikt om overbelasting te voorkomen. Leer meer in [ documentatie van Journey Orchestration ](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html) {target="_blank"}. De bijschilderregel hoeft niet opnieuw te worden uitgevoerd. Als u het opnieuw moet proberen, moet u een alternatief pad in de reis gebruiken door het vakje **[!UICONTROL Add an alternative path in case of a timeout or an error]** in voorwaarden of acties te controleren.

Voordat u het publiek in een productiereis gaat gebruiken, moet u altijd eerst het aantal personen evalueren dat elke dag voor dit publiek in aanmerking komt. U kunt dit doen door het menu **[!UICONTROL Audience]** te selecteren, het publiek te openen en vervolgens naar de **[!UICONTROL Profiles over time]** -grafiek te kijken.

![](assets/segment-overload.png)

## Hoe kan ik-video {#video}

Begrijp de toepasselijke gebruiksgevallen voor reizen van de Kwalificatie van het Publiek in deze video. Leer hoe u een reis maakt met de kwalificatie &#39;Audience Qualification&#39; en welke best practices u kunt toepassen.

>[!VIDEO](https://video.tv.adobe.com/v/3425028?quality=12)
