---
solution: Journey Optimizer
product: journey optimizer
title: Werken met reisgebeurtenissen
description: Leer hoe u met gebeurtenissen tijdens uw reizen kunt werken
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: gebeurtenissen, gebeurtenis, reis, definitie, begin
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: c2f32533027e374a1df26943e7c5acd4e1d13869
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 29%

---

# Werken met reisgebeurtenissen {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Reisevenementen"
>abstract="Een gebeurtenis is gekoppeld aan een persoon en Dit heeft betrekking op het gedrag van een persoon (een persoon heeft voorbeeld een product gekocht, een winkel bezocht, een website verlaten, enz.) of iets wat met een persoon in verband staat (een persoon heeft bijvoorbeeld 10.000 loyaliteitspunten bereikt). Journey Optimizer luistert naar monitaire gebeurtenissen tijdens reizen om de beste volgende acties te ordenen."

Gebeurtenissen stellen u in staat om reizen individueel te starten en realtime berichten te verzenden aan elke gebruiker wanneer deze de reis betreedt.

In de gebeurtenisconfiguratie, vormt u de gebeurtenissen die in de reizen worden verwacht. De gegevens van de binnenkomende gebeurtenissen worden genormaliseerd volgens het Adobe Experience Data Model (XDM). Gebeurtenissen komen van de Streaming Ingestie-API&#39;s voor geverifieerde en niet-geverifieerde gebeurtenissen (zoals Adobe Mobile SDK-gebeurtenissen). U kunt meerdere gebeurtenissen gebruiken (in verschillende stappen van een reis) en verschillende reizen kunnen dezelfde gebeurtenis gebruiken.

U kunt twee soorten gebeurtenissen vormen: **Eenheids gebeurtenissen** en **Bedrijfs gebeurtenissen**.


➡️ [ ontdekt deze eigenschap in video ](#video)

## Unitaire gebeurtenissen {#unitary-events}

**de gebeurtenissen van 0&rbrace; Eenheids &lbrace;worden verbonden aan een persoon.** Ze hebben betrekking op het gedrag van een persoon (bijvoorbeeld een persoon heeft een product gekocht, een winkel bezocht, een website verlaat, enz.) of op iets dat met een persoon verband houdt (bijvoorbeeld een persoon heeft 10 000 loyaliteitspunten bereikt). Dit is waar [!DNL Journey Optimizer] tijdens reizen naar luistert om de beste volgende acties te ordenen. Uniforme gebeurtenissen kunnen op regels zijn gebaseerd of door het systeem worden gegenereerd. Leren hoe te om een eenheidsgebeurtenis tot stand te brengen, verwijs naar deze [ pagina ](../event/about-creating.md).

Eenheidstrajecten (te beginnen met een evenement of een kwalificatie van het publiek) bevatten een begeleidend element dat voorkomt dat ritten bij dezelfde gebeurtenis meerdere keren ten onrechte worden gestart. De ingang van het profiel wordt tijdelijk geblokkeerd door gebrek gedurende 5 minuten. Als bijvoorbeeld een evenement om 12.01 uur een reis voor een bepaald profiel start en een ander om 12.03 uur aankomt (ongeacht of het dezelfde gebeurtenis is of een andere gebeurtenis die dezelfde reis veroorzaakt), zal die reis niet opnieuw beginnen voor dit profiel.

## Zakelijke gebeurtenissen {#business-events}

**Bedrijfs** gebeurtenissen zijn niet verbonden met een specifiek profiel. Het kan bijvoorbeeld een nieuwsbericht, een sportupdate, een wijziging of annulering van een vlucht, een inventarisatie, weersomstandigheden, enz. zijn. Hoewel deze evenementen niet specifiek zijn voor een profiel, kunnen ze van belang zijn voor elk aantal profielen: personen die zich op bepaalde nieuwsonderwerpen hebben geabonneerd, passagiers op een vlucht, klanten die geïnteresseerd zijn in een product uit de voorraad, enz. Zakelijke gebeurtenissen zijn altijd op regels gebaseerd. Wanneer u een bedrijfsgebeurtenis in een reis laat vallen, voegt het automatisch a **Gelezen publiek** activiteit rechts na.Leer hoe te om een bedrijfsgebeurtenis [ op deze pagina ](../event/about-creating-business.md) tot stand te brengen.

## Aanbevelingen

De configuratie van de gebeurtenis is **verplicht** en moet door een ingenieur van Gegevens worden uitgevoerd.

Als u wilt voorkomen dat bestaande reizen worden onderbroken en een gebeurtenis bewerkt die wordt gebruikt in een concept of live reis, kunt u alleen de naam, de beschrijving of ladingsvelden wijzigen.

## Type gebeurtenis-id {#event-id-type}

Voor **zaken** gebeurtenissen, is het type van gebeurtenisidentiteitskaart altijd op regel-gebaseerd.

Voor **unitaire** gebeurtenissen, zijn er twee soorten gebeurtenisidentiteitskaart:

* **Op regels gebaseerde** gebeurtenissen: dit type gebeurtenis genereert geen eventID. Door de eenvoudige expressie-editor te gebruiken bepaalt u eenvoudig een regel die door het systeem zal worden gebruikt om de relevante gebeurtenissen te identificeren die uw journeys zullen triggeren. Deze regel kan zijn gebaseerd op elk veld dat beschikbaar is in de gebeurtenispayload, bijvoorbeeld de locatie van het profiel of het aantal items dat is toegevoegd aan de winkelwagen van het profiel.

  >[!CAUTION]
  >
  >Een beperkingsregel wordt bepaald voor op regels gebaseerde gebeurtenissen. Het beperkt het aantal gekwalificeerde gebeurtenissen dat een reis tot 5.000 per seconden kan verwerken voor een bepaalde Organisatie. Het komt overeen met Journey Optimizer SLA&#39;s. Verwijs naar uw Journey Optimizer vergunning gevend en [ Beschrijving van het Product van Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).

* **Door het systeem gegenereerde** gebeurtenissen: deze gebeurtenissen vereisen een eventID. Dit eventID-veld wordt automatisch gegenereerd wanneer de gebeurtenis wordt gemaakt. Het systeem dat de gebeurtenis pusht, moet geen ID genereren, het moet overgaan naar degene die in de voorvertoning van de payload beschikbaar is.

>[!NOTE]
>
>Journey Optimizer vereist dat gebeurtenissen worden gestreamd naar Data Collection Core Service (DCCS) om een reis te kunnen activeren. Gebeurtenissen die worden ingevoerd in batch of gebeurtenissen uit interne Journey Optimizer-gegevenssets (Berichtfeedback, E-mailtracking, enz.) kunnen niet worden gebruikt om een reis te activeren. Voor gebruiksgevallen waar u gestreamde gebeurtenissen niet kunt krijgen, gelieve een publiek te bouwen dat op die gebeurtenissen wordt gebaseerd en de **Gelezen activiteit van het Publiek** in plaats daarvan te gebruiken. De kwalificatie van het publiek kan technisch worden gebruikt, maar kan stroomafwaartse uitdagingen veroorzaken die op de gebruikte acties worden gebaseerd. Deze gegevens hoeven niet noodzakelijkerwijs naar het Real-Time Profile te gaan. Als u de gebeurtenissen wilt gebruiken voor segmentatie of opzoeken in een aparte journey, raden we u aan de dataset voor profiel in te schakelen.

## Datacyclus {#data-cycle}

Gebeurtenissen zijn POST-API-aanroepen. Gebeurtenissen worden naar Adobe Experience Platform verzonden via de API&#39;s voor streaming-insluiting. De URL-bestemming van gebeurtenissen die via transactie-API&#39;s worden verzonden, wordt een &quot;inlet&quot; genoemd. De payload van gebeurtenissen volgt de XDM-indeling.

De payload bevat informatie die vereist is voor de Streaming Ingestie-API&#39;s om te werken (in de koptekst) en de informatie die [!DNL Journey Optimizer] nodig heeft om te werken en informatie die moet worden gebruikt tijdens reizen (in het lichaam, bijvoorbeeld de hoeveelheid achtergelaten winkelwagentje). Er zijn twee modi voor streamingopname, geverifieerd en niet-geverifieerd. Raadpleeg [deze koppeling](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html){target="_blank"}voor meer informatie over streamingopname-API’s.

Na aankomst door Streaming Ingestie APIs, stromen de gebeurtenissen in de interne dienst genoemd Pijpleiding en dan in Adobe Experience Platform. Als in het het gebeurtenisschema de markering voor real-timeklantprofielservice is ingeschakeld en een dataset-id eveneens de markering voor real-timeklantprofiel heeft, stroomt deze naar de real-timeklantprofielservice.

Voor door het systeem gegenereerde gebeurtenissen filtert de Pipeline gebeurtenissen met een lading die [!DNL Journey Optimizer] eventIDs bevat (zie het proces van de gebeurtenisverwezenlijking hieronder) die door [!DNL Journey Optimizer] wordt verstrekt en in gebeurtenislading bevat. Voor op regel-gebaseerde gebeurtenissen, identificeert het systeem de gebeurtenis gebruikend de eventID voorwaarde. Er wordt naar deze gebeurtenissen geluisterd door [!DNL Journey Optimizer] en de bijbehorende journey wordt geactiveerd.

## Hoe kan ik-video&#39;s {#video}

Leer hoe te om een gebeurtenis te vormen, specificeer het het stromen eindpunt en de lading voor een gebeurtenis.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Begrijp de toepasselijke gebruiksscenario&#39;s voor bedrijfsgebeurtenissen. Leer hoe u een journey bouwt met behulp van een bedrijfsgebeurtenis en welke aanbevolen procedures u toepast.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
