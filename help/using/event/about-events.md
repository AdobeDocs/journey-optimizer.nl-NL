---
title: Informatie over gebeurtenissen
description: Meer informatie over gebeurtenissen
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '829'
ht-degree: 50%

---

# Informatie over gebeurtenissen{#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Informatie over gebeurtenissen"
>abstract="Een gebeurtenis is gekoppeld aan een persoon en heeft betrekking op het gedrag van een persoon (bijvoorbeeld: iemand heeft een product gekocht, een winkel bezocht, een website verlaten, enz.) of op iets dat verband houdt met een persoon (bijvoorbeeld: iemand heeft 10.000 loyaliteitspunten verdiend). Dit is waar Journey Optimizer naar zal luisteren tijdens reizen om de beste volgende acties te ordenen."

Met de gebeurtenisconfiguratie kunt u de informatie definiëren die door [!DNL Journey Optimizer] als gebeurtenissen wordt ontvangen. U kunt meerdere gebeurtenissen gebruiken (in verschillende stappen van een reis) en verschillende reizen kunnen dezelfde gebeurtenis gebruiken.

>[!CAUTION]
>
>Gebeurtenisconfiguratie is **verplicht** en moet worden uitgevoerd door een **gegevensengineer**.

U kunt twee typen gebeurtenissen configureren:

* **Unitair** gebeurtenissen: deze gebeurtenis is gekoppeld aan een persoon . Ze hebben betrekking op het gedrag van een persoon (bijvoorbeeld iemand heeft een product gekocht, een winkel bezocht, een website verlaten, enz.) of op iets dat verband houdt met een persoon (bijvoorbeeld: iemand heeft 10.000 loyaliteitspunten verdiend). Dit is waar [!DNL Journey Optimizer] op let tijdens journey’s om vervolgens de beste acties te orkestreren. Uniforme gebeurtenissen kunnen op regels zijn gebaseerd of door het systeem worden gegenereerd. Als u wilt leren hoe u een eenheidsgebeurtenis maakt, raadpleegt u deze [page](../event/about-creating.md).

* **Zakelijk** gebeurtenissen: een bedrijfsgebeurtenis is een gebeurtenis die, in tegenstelling tot een eenheidsgebeurtenis, niet aan een specifiek profiel is gekoppeld. Het kan bijvoorbeeld een nieuwsbericht, een sportupdate, een wijziging of annulering van een vlucht, een inventarisatie, weersomstandigheden, enz. zijn. Hoewel deze gebeurtenissen niet specifiek zijn voor een profiel, kunnen ze van belang zijn voor elk aantal profielen: personen die zich hebben geabonneerd op bepaalde nieuwsonderwerpen, passagiers op een vlucht, consumenten die geïnteresseerd zijn in een product uit de buitenwereld, enz. Zakelijke gebeurtenissen zijn altijd op regels gebaseerd. Wanneer u een bedrijfsgebeurtenis tijdens een rit neerzet, wordt automatisch een **Segment lezen** activiteit direct na. Als u wilt leren hoe u een bedrijfsgebeurtenis maakt, raadpleegt u deze [page](../event/about-creating-business.md).


>[!NOTE]
>
>Als u een gebeurtenis bewerkt die in een concept- of live journey wordt gebruikt, kunt u alleen de naam en de beschrijving wijzigen of payloadvelden toevoegen. We hanteren een strikte beperking voor de bewerking of het opstellen van concept- of live journey’s om te voorkomen dat journey’s worden afgebroken.

➡️ [Ontdek deze functie in video](#video)

## Type gebeurtenis-id{#event-id-type}

Voor bedrijfsgebeurtenissen, is het type van gebeurtenisidentiteitskaart altijd regel-gebaseerd.

Voor eenheidsgebeurtenissen zijn er twee typen gebeurtenis-id:

* **Op regels gebaseerde** gebeurtenissen: dit type gebeurtenis genereert geen eventID. Door de eenvoudige expressie-editor te gebruiken bepaalt u eenvoudig een regel die door het systeem zal worden gebruikt om de relevante gebeurtenissen te identificeren die uw journeys zullen triggeren. Deze regel kan zijn gebaseerd op elk veld dat beschikbaar is in de gebeurtenispayload, bijvoorbeeld de locatie van het profiel of het aantal items dat is toegevoegd aan de winkelwagen van het profiel.

   >[!CAUTION]
   >
   >Een beperkingsregel wordt bepaald voor op regels gebaseerde gebeurtenissen. Deze beperkt het aantal gekwalificeerde gebeurtenissen dat een journey kan verwerken, tot 5000 per seconde voor een bepaalde organisatie. Het komt overeen met Journey Optimizer SLA&#39;s. Raadpleeg uw Journey Optimizer-licenties en [Journey Optimizer-productbeschrijving](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).

* **Door het systeem gegenereerde** gebeurtenissen: deze gebeurtenissen vereisen een eventID. Dit eventID-veld wordt automatisch gegenereerd wanneer de gebeurtenis wordt gemaakt. Het systeem dat de gebeurtenis pusht, moet geen ID genereren, het moet overgaan naar degene die in de voorvertoning van de payload beschikbaar is.

Journey Optimizer vereist dat gebeurtenissen worden gestreamd of gebatcheerd naar Adobe Experience Platform. Deze gegevens hoeven niet noodzakelijkerwijs naar het Real-Time Profile te gaan. Als u de gebeurtenissen wilt gebruiken voor segmentatie of opzoeken in een aparte journey, raden we u aan de dataset voor profiel in te schakelen.

## Datacyclus {#data-cycle}

Gebeurtenissen zijn POST-API-aanroepen. Gebeurtenissen worden naar Adobe Experience Platform verzonden via de API&#39;s voor streaming insluiting. De URL-bestemming van gebeurtenissen die via API’s voor transactionele berichten worden verzonden, wordt een inlet genoemd. De payload van gebeurtenissen volgt de XDM-indeling.

De payload bevat informatie die vereist is voor de Streaming Ingestie-API&#39;s om te werken (in de header) en de informatie die vereist is voor [!DNL Journey Optimizer] werk en informatie voor reizen (bijvoorbeeld in het lichaam, de hoeveelheid verlaten wagen). Er zijn twee modi voor streamingopname, geverifieerd en niet-geverifieerd. Raadpleeg [deze koppeling](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html)voor meer informatie over streamingopname-API’s.

Na aankomst door Streaming Ingestie APIs, stromen de gebeurtenissen in de interne dienst genoemd Pijpleiding en dan in Adobe Experience Platform. Als in het het gebeurtenisschema de markering voor real-timeklantprofielservice is ingeschakeld en een dataset-id eveneens de markering voor real-timeklantprofiel heeft, stroomt deze naar de real-timeklantprofielservice.

Voor door het systeem gegenereerde gebeurtenissen, filtert de Pipeline gebeurtenissen die een lading bevatten [!DNL Journey Optimizer] eventID&#39;s (zie het proces voor het maken van gebeurtenissen hieronder) verstrekt door [!DNL Journey Optimizer] en opgenomen in gebeurtenislading. Voor op regel-gebaseerde gebeurtenissen, identificeert het systeem de gebeurtenis gebruikend de eventID voorwaarde. Er wordt naar deze gebeurtenissen geluisterd door [!DNL Journey Optimizer] en de bijbehorende journey wordt geactiveerd.

## Instructievideo&#39;s {#video}

Leer hoe te om een gebeurtenis te vormen, specificeer het het stromen eindpunt en de lading voor een gebeurtenis.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Begrijp de toepasselijke gebruiksscenario&#39;s voor bedrijfsgebeurtenissen. Leer hoe u een journey bouwt met behulp van een bedrijfsgebeurtenis en welke aanbevolen procedures u toepast.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
