---
solution: Journey Optimizer
product: journey optimizer
title: Werken met reisgebeurtenissen
description: Leer hoe u met gebeurtenissen tijdens uw reizen kunt werken
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: gebeurtenissen, gebeurtenis, reis, definitie, begin
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: bfcc7b1544a0d58af8ac1ac69e777a3ff894bbdf
workflow-type: tm+mt
source-wordcount: '1570'
ht-degree: 15%

---

# Werken met reisgebeurtenissen {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Reisevenementen"
>abstract="Een gebeurtenis is gekoppeld aan een persoon en Het heeft betrekking op het gedrag van een persoon (bijvoorbeeld een persoon kocht een product, bezocht een winkel, verlaat een website, enz.) of iets dat met een persoon verband houdt (bijvoorbeeld een persoon bereikte 10.000 loyaliteitspunten). Journey Optimizer luistert naar monitaire gebeurtenissen tijdens reizen om de beste volgende acties te ordenen."

Gebruik gebeurtenissen om ritten individueel te activeren, waarbij realtime berichten aan elke gebruiker worden gegeven wanneer deze de reis betreden.

>[!IMPORTANT]
>
>Voor gebeurtenisvereisten en beperkingen (het stromen, de Dienst van de Vraag, partijingestie), zie [&#x200B; de guardrails van de Reis - Gebeurtenissen &#x200B;](../start/guardrails.md#events-g).

In de gebeurtenisconfiguratie, vormt u de gebeurtenissen die in de reizen worden verwacht. De gegevens van de binnenkomende gebeurtenissen worden genormaliseerd volgens het Adobe Experience Data Model (XDM). Gebeurtenissen komen van de Streaming Ingestie-API&#39;s voor geverifieerde en niet-geverifieerde gebeurtenissen (zoals Adobe Mobile SDK-gebeurtenissen). U kunt meerdere gebeurtenissen gebruiken (in verschillende stappen van een reis) en verschillende reizen kunnen dezelfde gebeurtenis gebruiken.

De configuratie van de gebeurtenis is **verplicht** en moet door een ingenieur van Gegevens worden uitgevoerd.

U kunt twee soorten gebeurtenissen vormen: **Eenheids gebeurtenissen** en **Bedrijfs gebeurtenissen**.

➡️ [Ontdek deze functie in video](#video)

## Unitaire gebeurtenissen {#unitary-events}

**de Eenheid** gebeurtenissen zijn verbonden met een persoon. Ze hebben betrekking op het gedrag van een persoon (bijvoorbeeld een persoon kocht een product, bezocht een winkel, verlaat een website, enz.) of iets dat met een persoon verband houdt (bijvoorbeeld een persoon bereikte 10.000 loyaliteitspunten). Dit is waar [!DNL Journey Optimizer] tijdens reizen naar luistert om de beste volgende acties te ordenen. Uniforme gebeurtenissen kunnen op regels zijn gebaseerd of door het systeem worden gegenereerd. Leren hoe te om een eenheidsgebeurtenis tot stand te brengen, verwijs naar deze [&#x200B; pagina &#x200B;](../event/about-creating.md).

Eenheidstrajecten (te beginnen met een evenement of een kwalificatie van het publiek) bevatten een begeleidend element dat voorkomt dat ritten bij dezelfde gebeurtenis meerdere keren ten onrechte worden gestart. De ingang van het profiel wordt tijdelijk geblokkeerd door gebrek gedurende 5 minuten. Bijvoorbeeld, als een gebeurtenis een reis bij 12 :01 voor een specifiek profiel teweegbrengt en een andere bij 12 :03 aankomt (of het de zelfde gebeurtenis of verschillende is die de zelfde reis teweegbrengen) die reis niet opnieuw voor dit profiel zal beginnen.

## Zakelijke gebeurtenissen {#business-events}

**Bedrijfs** gebeurtenissen zijn niet verbonden met een specifiek profiel. Het kan bijvoorbeeld een nieuwsbericht, een sportupdate, een wijziging of annulering van een vlucht, een inventarisatie, weersomstandigheden, enz. zijn. Hoewel deze evenementen niet specifiek zijn voor een profiel, kunnen ze van belang zijn voor elk aantal profielen: personen die zich op bepaalde nieuwsonderwerpen hebben geabonneerd, passagiers op een vlucht, klanten die geïnteresseerd zijn in een product uit de voorraad, enz. Zakelijke gebeurtenissen zijn altijd op regels gebaseerd. Wanneer u een bedrijfsgebeurtenis in een reis laat vallen, voegt het automatisch a **Gelezen publiek** activiteit rechts na.Leer hoe te om een bedrijfsgebeurtenis [&#x200B; op deze pagina &#x200B;](../event/about-creating-business.md) tot stand te brengen.


## Type gebeurtenis-id {#event-id-type}

Voor **zaken** gebeurtenissen, is het type van gebeurtenisidentiteitskaart altijd op regel-gebaseerd.

Voor **unitaire** gebeurtenissen, zijn er twee soorten gebeurtenisidentiteitskaart:

* **Op regels gebaseerde** gebeurtenissen: dit type gebeurtenis genereert geen eventID. Door de eenvoudige expressie-editor te gebruiken bepaalt u eenvoudig een regel die door het systeem zal worden gebruikt om de relevante gebeurtenissen te identificeren die uw journeys zullen triggeren. Deze regel kan zijn gebaseerd op elk veld dat beschikbaar is in de gebeurtenispayload, bijvoorbeeld de locatie van het profiel of het aantal items dat is toegevoegd aan de winkelwagen van het profiel.

  >[!CAUTION]
  >
  >Een beperkingsregel wordt bepaald voor op regels gebaseerde gebeurtenissen. Het beperkt het aantal gekwalificeerde gebeurtenissen dat een reis tot 5.000 per seconden kan verwerken voor een bepaalde Organisatie. Het komt overeen met Journey Optimizer SLA&#39;s. Verwijs naar uw Journey Optimizer vergunning gevend en [&#x200B; Beschrijving van het Product van Journey Optimizer &#x200B;](https://helpx.adobe.com/nl/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

* **Door het systeem gegenereerde** gebeurtenissen: deze gebeurtenissen vereisen een eventID. Dit eventID-veld wordt automatisch gegenereerd wanneer de gebeurtenis wordt gemaakt. Het systeem dat de gebeurtenis pusht, moet geen ID genereren, het moet overgaan naar degene die in de voorvertoning van de payload beschikbaar is.

>[!NOTE]
>
>Journey Optimizer vereist dat gebeurtenissen worden gestreamd naar Data Collection Core Service (DCCS) om een reis te kunnen activeren. Gebeurtenissen die in partij worden opgenomen, gebeurtenissen die via **de Dienst van de Vraag** worden opgenomen, of gebeurtenissen van interne datasets van Journey Optimizer (de Terugkoppeling van het Bericht, E-mail het Volgen, enz.) kunnen niet worden gebruikt om een reis teweeg te brengen. Voor gebruiksgevallen waar u gestreamde gebeurtenissen niet kunt krijgen, gelieve een publiek te bouwen dat op die gebeurtenissen wordt gebaseerd en de **Gelezen activiteit van het Publiek** in plaats daarvan te gebruiken. De kwalificatie van het publiek kan technisch worden gebruikt, maar kan stroomafwaartse uitdagingen veroorzaken die op de gebruikte acties worden gebaseerd. Deze gegevens hoeven niet noodzakelijkerwijs naar het Real-Time Profile te gaan. Als u de gebeurtenissen voor segmentatie zou willen gebruiken, adviseren wij u de dataset voor profiel toelaat.

## Datacyclus {#data-cycle}

Gebeurtenissen zijn POST-API-aanroepen. Gebeurtenissen worden naar Adobe Experience Platform verzonden via de API&#39;s voor streaming-insluiting. De URL-bestemming van gebeurtenissen die via transactie-API&#39;s worden verzonden, wordt een &quot;inlet&quot; genoemd. De payload van gebeurtenissen volgt de XDM-indeling.

De payload bevat informatie die vereist is voor de Streaming Ingestie-API&#39;s om te werken (in de koptekst) en de informatie die [!DNL Journey Optimizer] nodig heeft om te werken en informatie die moet worden gebruikt tijdens reizen (in het lichaam, bijvoorbeeld de hoeveelheid achtergelaten winkelwagentje). Er zijn twee modi voor streamingopname, geverifieerd en niet-geverifieerd. Raadpleeg [deze koppeling](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=nl-NL){target="_blank"}voor meer informatie over streamingopname-API’s.

Na aankomst door Streaming Ingestie APIs, stromen de gebeurtenissen in de interne dienst genoemd Pijpleiding en dan in Adobe Experience Platform. Als in het het gebeurtenisschema de markering voor real-timeklantprofielservice is ingeschakeld en een dataset-id eveneens de markering voor real-timeklantprofiel heeft, stroomt deze naar de real-timeklantprofielservice.

Voor door het systeem gegenereerde gebeurtenissen filtert de Pipeline gebeurtenissen met een lading die [!DNL Journey Optimizer] eventIDs bevat (zie het proces van de gebeurtenisverwezenlijking hieronder) die door [!DNL Journey Optimizer] wordt verstrekt en in gebeurtenislading bevat. Voor op regel-gebaseerde gebeurtenissen, identificeert het systeem de gebeurtenis gebruikend de eventID voorwaarde. Er wordt naar deze gebeurtenissen geluisterd door [!DNL Journey Optimizer] en de bijbehorende journey wordt geactiveerd.


## Over de doorvoer van Journey-gebeurtenissen {#event-thoughput}

Adobe Journey Optimizer ondersteunt een piekvolume van 5.000 reisgebeurtenissen per seconde op organisatieniveau, voor alle sandboxen. Dit quotum is op alle gebeurtenissen van toepassing die in actieve reizen worden gebruikt, die **Levende** omvatten, **Droog looppas**, **Gesloten** en **Gepauzeerde** reizen. Wanneer dit quotum is bereikt, worden nieuwe gebeurtenissen in de wachtrij geplaatst met een verwerkingssnelheid van 5.000 per seconde. De maximumtijd een gebeurtenis kan in de rij uitgeven is **24 uren**.

Voor meer details op de tarieven van de reisverwerking en hoe de verschillende vervoerstypes productie beïnvloeden, verwijs naar [&#x200B; deze sectie &#x200B;](../building-journeys/entry-management.md#journey-processing-rate).

De volgende typen gebeurtenissen worden geteld voor de 5.000 TPS-quota:

* **Externe Eenheid Gebeurtenissen**: Omvat zowel op regel-gebaseerd als op systeem-geproduceerde gebeurtenissen. Als de zelfde ruwe gebeurtenis voor veelvoudige regeldefinities kwalificeert, elke gekwalificeerde regel telt als afzonderlijke gebeurtenis. Meer informatie vindt u hieronder.

* **Gebeurtenissen van de Kwalificatie van het publiek van het publiek**: Als het zelfde het stromen publiek in veelvoudige reizen wordt gebruikt, telt elk gebruik afzonderlijk. Als u bijvoorbeeld hetzelfde publiek gebruikt in een publiekskwalificatie-activiteit in twee reizen, resulteert dat in twee getallen gebeurtenissen.

* **Gebeurtenissen van de Reactie**: Gebeurtenissen die door profielreacties (geopende e-mail, geklikte e-mail, enz.) binnen een reis worden teweeggebracht.

* **Bedrijfs Gebeurtenissen**: Gebeurtenissen niet verbonden aan een specifiek profiel, maar aan een zaken-verwante gebeurtenis.

* **Gebeurtenissen van Analytics**: Als de [&#x200B; integratie met Adobe Analytics om reizen &#x200B;](about-analytics.md) te teweegbrengen is toegelaten, zijn deze gebeurtenissen ook inbegrepen.

* **Hervatten Gebeurtenissen**: De technische gebeurtenis teweeggebracht wanneer een profiel van een gepauzeerde reis hervat. Leer meer over [&#x200B; herstellend gepauzeerde reizen &#x200B;](../building-journeys/journey-pause.md#journey-resume-steps).

* **wacht de Gebeurtenissen van de Voltooiing van de Knoop**: Wanneer een profiel een wachttijdknoop weggaat, wordt een technische gebeurtenis geproduceerd om de reis te hervatten.

>[!NOTE]
>
>Met uitzondering van gebeurtenissen voor wachten en hervatten, tellen alle andere gebeurtenistypen ook mee voor de quota wanneer deze worden gebruikt op reizen die zijn gebaseerd op leessoorten.

### Informatie over onbewerkte gebeurtenissen die in aanmerking komen voor meerdere regeldefinities

Dezelfde onbewerkte gebeurtenis kan in aanmerking komen voor meerdere regeldefinities tijdens reizen. Wanneer een gebeurtenis in de **sectie van het Beleid** wordt gevormd, voor het zelfde gebeurtenisschema, kunnen de veelvoudige gebeurtenisregels worden bepaald. We hebben bijvoorbeeld een aankoopgebeurtenis met velden stad en purchaseValue. Laten we de volgende scenario&#39;s in overweging nemen:

1. Een gebeurtenis **E1** genoemd `newYorkPurchases` wordt gecreeerd met een regeldefinitie die zeggen dat `city=='New York'`. Dit evenement kan in tien reizen worden gebruikt, maar zal nog steeds slechts als één gebeurtenis worden geteld, wanneer het komt.

1. Nu zeggen wij dat een gebeurtenis **E2** genoemd `highValuePurchases` met `purchaseValue > 1000` als regeldefinitie ook, op het zelfde gebeurtenisschema wordt gecreeerd dan **E1**. In dit geval wordt dezelfde inkomende gebeurtenis aan de hand van twee regels geëvalueerd: `newYorkPurchases` en `highValuePurchases` . Nu kan het gebeuren dat een aankoop in New York ook een aankoop van hoge waarde is.

   In dit geval zal Journey Optimizer tot twee gebeurtenissen, **E1** en **E2**, uit de zelfde inkomende gebeurtenis leiden, die deze enige inkomende gebeurtenistelling als twee gebeurtenissen zullen maken.

   Merk op dat deze gebeurtenissen beginnen geteld te worden wanneer zij in een actieve reis, met inbegrip van **Levende**, **Droog looppas**, **Gesloten** en **Gepauzeerde** reis worden gebruikt.

## Een gebeurtenis bijwerken en verwijderen {#update-event}


Vermijd het breken van bestaande reizen, wanneer u een gebeurtenis uitgeeft die in a **wordt gebruikt Ontwerp**, **Levend** of **Gesloten** reis, kunt u de naam, de beschrijving slechts veranderen of ladingsgebieden toevoegen.

Om het even welke die gebeurtenis in **wordt gebruikt Levende**, **Ontwerp** of **gesloten** reizen kunnen niet worden geschrapt. Als u een gebruikte gebeurtenis wilt verwijderen, moet u de ritten met deze gebeurtenis stoppen en/of deze verwijderen uit de conceptritten waar deze wordt gebruikt. U kunt het veld **[!UICONTROL Used in]** controleren. Het toont het aantal reizen die die bepaalde gebeurtenis gebruiken. U kunt klikken op de knop **[!UICONTROL View journeys]** om de lijst met corresponderende journey’s weer te geven.

## Hoe kan ik-video&#39;s {#video}

Leer hoe te om een gebeurtenis te vormen, specificeer het het stromen eindpunt en de lading voor een gebeurtenis.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Begrijp de toepasselijke gebruiksscenario&#39;s voor bedrijfsgebeurtenissen. Leer hoe u een journey bouwt met behulp van een bedrijfsgebeurtenis en welke aanbevolen procedures u toepast.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
