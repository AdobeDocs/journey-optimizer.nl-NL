---
title: Informatie over gebeurtenissen
description: Meer informatie over gebeurtenissen
feature: Gebeurtenissen
topic: Beheer
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 32%

---

# Informatie over gebeurtenissen{#concept_gfj_fqt_52b}

![](../assets/do-not-localize/badge.png)

>[!CONTEXTUALHELP]
>id="jo_events"
>title="Informatie over gebeurtenissen"
>abstract="Een gebeurtenis is gekoppeld aan een persoon en heeft betrekking op het gedrag van een persoon (bijvoorbeeld: iemand heeft een product gekocht, een winkel bezocht, een website verlaten, enz.) of op iets dat verband houdt met een persoon (bijvoorbeeld: iemand heeft 10.000 loyaliteitspunten verdiend). Dit is waar [!DNL Journey Optimizer] op let tijdens journey’s om vervolgens de beste acties te orkestreren."

Met de gebeurtenisconfiguratie kunt u de informatie definiëren die door [!DNL Journey Optimizer] als gebeurtenissen wordt ontvangen. U kunt meerdere gebeurtenissen gebruiken (in verschillende stappen van een reis) en verschillende reizen kunnen dezelfde gebeurtenis gebruiken.

>[!CAUTION]
>
>Gebeurtenisconfiguratie is **verplicht** en moet worden uitgevoerd door een **technische gebruiker**.

U kunt twee typen gebeurtenissen configureren:

* **Unitaryevents:**  deze gebeurtenis is gekoppeld aan een persoon . Ze hebben betrekking op het gedrag van een persoon (bijvoorbeeld iemand heeft een product gekocht, een winkel bezocht, een website verlaten, enz.) of op iets dat verband houdt met een persoon (bijvoorbeeld: iemand heeft 10.000 loyaliteitspunten verdiend). Dit is waar [!DNL Journey Optimizer] op let tijdens journey’s om vervolgens de beste acties te orkestreren. Uniforme gebeurtenissen kunnen op regels zijn gebaseerd of door het systeem worden gegenereerd. Als u wilt leren hoe u een eenheidsgebeurtenis maakt, raadpleegt u deze [pagina](../event/about-creating.md).

* **** Zakelijke gebeurtenissen: een bedrijfsgebeurtenis is een gebeurtenis die, in tegenstelling tot een eenheidsgebeurtenis, niet aan een specifiek profiel is gekoppeld. Het kan bijvoorbeeld een nieuwsbericht, een sportupdate, een wijziging of annulering van een vlucht, een inventarisatie, weersomstandigheden, enz. zijn. Hoewel deze gebeurtenissen niet specifiek zijn voor een profiel, kunnen ze van belang zijn voor elk aantal profielen: personen die zich hebben geabonneerd op bepaalde nieuwsonderwerpen, passagiers op een vlucht, consumenten die geïnteresseerd zijn in een product uit de buitenwereld, enz. Zakelijke gebeurtenissen zijn altijd op regels gebaseerd. Wanneer u een bedrijfsgebeurtenis in een reis laat vallen, voegt het automatisch een **Gelezen segment** activiteit direct na toe. Als u wilt leren hoe u een bedrijfsgebeurtenis maakt, raadpleegt u deze [pagina](../event/about-creating-business.md).


>[!NOTE]
>
>Als u een gebeurtenis bewerkt die in een concept- of live journey wordt gebruikt, kunt u alleen de naam en de beschrijving wijzigen of payloadvelden toevoegen. We hanteren een strikte beperking voor de bewerking of het opstellen van concept- of live journey’s om te voorkomen dat journey’s worden afgebroken.

## Type gebeurtenis-id{#event-id-type}

Voor bedrijfsgebeurtenissen, is het type van gebeurtenisidentiteitskaart altijd regel-gebaseerd.

Voor eenheidsgebeurtenissen zijn er twee typen gebeurtenis-id:

* **Op regels** gebaseerde gebeurtenissen: dit type gebeurtenis genereert geen eventID. Gebruikend de eenvoudige uitdrukkingsredacteur, bepaalt u eenvoudig een regel die door het systeem zal worden gebruikt om de relevante gebeurtenissen te identificeren die uw reizen zullen teweegbrengen. Deze regel kan worden gebaseerd op elk veld dat beschikbaar is in de gebeurtenislading, bijvoorbeeld de locatie van het profiel of het aantal items dat is toegevoegd aan het winkelwagentje van het profiel.

   >[!CAUTION]
   >
   >Een afschilderingsregel wordt bepaald voor op regel-gebaseerde gebeurtenissen. Het beperkt het aantal gekwalificeerde gebeurtenissen dat een reis kan verwerken tot 5000 per seconde voor een bepaalde Organisatie (ORG). Het komt overeen met Journey Optimizer SLA&#39;s. Zie deze [pagina](https://helpx.adobe.com/legal/product-descriptions/journey-orchestration.html).

* **System-** generateDefents: deze gebeurtenissen vereisen een eventID. Dit veld eventID wordt automatisch gegenereerd wanneer de gebeurtenis wordt gemaakt. Het systeem dat de gebeurtenis duwt zou geen identiteitskaart moeten produceren, zou het moeten overgaan beschikbaar in de voorproef van de lading.

## Datacyclus {#section_r1f_xqt_pgb}

Gebeurtenissen zijn POST-API-aanroepen. Gebeurtenissen worden naar Adobe Experience Platform verzonden via de API&#39;s voor streaming insluiting. De URL-bestemming van gebeurtenissen die via API’s voor transactionele berichten worden verzonden, wordt een inlet genoemd. De payload van gebeurtenissen volgt de XDM-indeling.

De nuttige lading bevat informatie die door Streaming Ingestie-API&#39;s wordt vereist om te werken (in de koptekst) en de informatie die door [!DNL Journey Optimizer] wordt vereist om te werken en informatie die tijdens reizen moet worden gebruikt (in het lichaam, bijvoorbeeld, de hoeveelheid een verlaten wagen). Er zijn twee modi voor streamingopname, geverifieerd en niet-geverifieerd. Raadpleeg [deze koppeling](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html)voor meer informatie over streamingopname-API’s.

Na aankomst door Streaming Ingestie APIs, stromen de gebeurtenissen in de interne dienst genoemd Pijpleiding en dan in Adobe Experience Platform. Als in het het gebeurtenisschema de markering voor real-timeklantprofielservice is ingeschakeld en een dataset-id eveneens de markering voor real-timeklantprofiel heeft, stroomt deze naar de real-timeklantprofielservice.

Voor door het systeem gegenereerde gebeurtenissen, filtert de Pipeline gebeurtenissen die een lading hebben die [!DNL Journey Optimizer] eventIDs bevat (zie het proces van de gebeurtenisverwezenlijking hieronder) die door [!DNL Journey Optimizer] wordt verstrekt en in gebeurtenislading bevat. Voor op regel-gebaseerde gebeurtenissen, identificeert het systeem de gebeurtenis gebruikend de eventID voorwaarde. Er wordt naar deze gebeurtenissen geluisterd door [!DNL Journey Optimizer] en de bijbehorende journey wordt geactiveerd.
