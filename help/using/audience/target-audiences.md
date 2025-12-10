---
solution: Journey Optimizer
product: journey optimizer
title: Informatie over Adobe Experience Platform-publiek
description: Leer hoe u met het publiek van Adobe Experience Platform kunt werken
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 78b95ccd-bc28-46cd-937a-f68e3f34cc1e
source-git-commit: 24d66f146ea3ed0e89a3b928b805bc53a70a8895
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Activering van het publiek in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

U kunt in campagnes selecteren en reizen om het even welk publiek dat gebruikend segmentdefinities, douane wordt geproduceerd uploadt, samenstellingswerkschema&#39;s of Federated de Samenstelling van de Publiek wordt geproduceerd.

## Afbeeldingen en beperkingen {#guardrails}

* **het Schild van de Gezondheidszorg of Privacy en het Schild van de Veiligheid** - het gebruik van publiek en attributen van publiekssamenstelling is momenteel niet beschikbaar met het Schild van de Gezondheidszorg of Privacy en het Schild van de Veiligheid. [&#x200B; Leer hoe te om de attributen van de kijkverrijking in  [!DNL Journey Optimizer]](../audience/about-audiences.md#enrichment) te gebruiken

* **uploadt de Douane &amp; Federated de Samenstelling van het Publiek** - voor de upload van de Douane en het Federatieve publiek van de Samenstelling van de Publiek, gelieve nota te nemen van de volgende gidsen:

   * **Voorproef en proefdruksteun:** momenteel, worden de voorproef en de proef niet gesteund voor publiek dat gebruikend CSV wordt gecreeerd uploadt of Federated de Samenstelling van het Publiek. Houd dit in gedachten wanneer u uw campagnes plant.

   * **richtend nieuwe profielen:** wanneer een gelijke niet tussen een verslag en een Verenigd profiel van de Dienst van het Profiel wordt gevonden, wordt een nieuw leeg profiel gecreeerd. Dit profiel is gekoppeld aan de verrijkingskenmerken die zijn opgeslagen in het datumpeer. Omdat dit nieuwe profiel leeg is, zijn velden die doorgaans worden gebruikt in [!DNL Journey Optimizer] (bijvoorbeeld PersonalEmail.address, mobilePhone.number) leeg. Daarom kunnen deze velden niet worden gebruikt voor doelframes.

     Om dit op te lossen, kunt u het &quot;uitvoeringsgebied&quot;(of &quot;uitvoeringsadres&quot;afhankelijk van het kanaal) in de kanaalconfiguratie als &quot;identityMap&quot;specificeren. Dit zorgt ervoor dat het kenmerk dat wordt gekozen als de identiteit bij het maken van een publiek, het kenmerk is dat wordt gebruikt voor het opgeven van doelen in [!DNL Journey Optimizer] .

   * **Geactiveerde verslagen &amp; identiteitsstitching:** Elk verslag in het publiek wordt geactiveerd, met inbegrip van om het even welke duplicaten. Tijdens de volgende Verenigde het profieluitvoer van de Dienst van het Profiel, gaan deze verslagen door identiteit stitching. Hierdoor kan het aantal geactiveerde records afwijken van het aantal profielen na identiteitsstitching.

## Activeringsvertraging van soorten publiek {#activation}

Soorten publiek zijn direct na inname klaar voor gebruik in [!DNL Journey Optimizer] . Hoewel dit meestal binnen een uur ligt, is het afhankelijk van enige variabiliteit. Het publiek dat uit samenstellingen voortvloeit, moet 24 uur na publicatie beschikbaar zijn.

Voor het publiek dat het resultaat is van batchsegmentatietaken, kan de activering vertraagd zijn vanwege variabiliteit in de inname van batch. Voor ritten voor lezers die dagelijks worden gepland, kunt u een tijdvenster in de reiseigenschappen bepalen om ervoor te zorgen dat nieuwe publieksgegevens beschikbaar zijn vóór de uitvoering van de reis.

Als de segmentatietaak niet binnen het bepaalde tijdvenster wordt voltooid, wordt de reis overgeslagen tot het volgende exemplaar. [&#x200B; Leer hoe te om een Lezen-publiek reis &#x200B;](../building-journeys/read-audience.md) te plannen

## Doelpubliek in [!DNL Journey Optimizer]

U kunt het publiek op verschillende manieren gebruiken in **[!DNL Journey Optimizer]** :

* Kies een publiek voor a **campagne**, waar het bericht wordt verzonden naar alle individuen die tot het geselecteerde publiek behoren. [&#x200B; Leer hoe te om het publiek van een campagne &#x200B;](../campaigns/create-campaign.md#define-the-audience-audience) te bepalen.

* Gebruik a **Gelezen publiek** orkestactiviteit in een reis om alle individuen in het publiek te maken de reis ingaan en de berichten ontvangen inbegrepen in uw reis. Laten we zeggen dat je een &quot;zilveren klant&quot; publiek hebt. Met deze activiteit, kunt u alle zilveren klanten tot een reis maken. U kunt hen dan een reeks gepersonaliseerde berichten verzenden. [&#x200B; Leer hoe te om Gelezen publieksactiviteit &#x200B;](../building-journeys/read-audience.md#configuring-segment-trigger-activity) te vormen.

  Voor ritten die publiek gebruiken van publiekssamenstelling of douane uploadt, zijn de profielattributen zo vers zoals de laatste partijevaluatie bij reisingang. Nochtans, na a **wacht** activiteit, verfrist de reis profielattributen van de Verenigde Dienst van het Profiel (UPS), die de recentste beschikbare gegevens ophaalt, wat profielattributen tijdens reisuitvoering kunnen veranderen. [&#x200B; Leer meer over profiel zich na een Wacht activiteit &#x200B;](../building-journeys/wait-activity.md#profile-refresh) vernieuwt

* Gebruik de **activiteit van de Voorwaarde** in een reis om voorwaarden te bouwen die op publiekslidmaatschap worden gebaseerd. [&#x200B; leer hoe te om publiek in voorwaarden &#x200B;](../building-journeys/condition-activity.md#using-a-segment) te gebruiken.

* Gebruik de **gebeurtenisactiviteit van de Kwalificatie van het publiek 0&rbrace; &lbrace;in een reis om individuen te maken ingaan of zich voorwaarts in de reis gebaseerd op de kijkposten van Adobe Experience Platform en uitgang.** U kunt bijvoorbeeld alle nieuwe zilverklanten een reis laten maken en hun berichten sturen. [&#x200B; Leer hoe te om een de kwalificatieactiviteit van het Publiek te vormen &#x200B;](../building-journeys/audience-qualification-events.md).

  >[!NOTE]
  >
  >Vanwege het batchkarakter van publiek dat is gemaakt met gebruik van compositieworkflows, aangepaste upload of Federated Audience Composition, kunt u deze soorten publiek niet als doelgroep instellen in een &#39;Audience Qualification&#39;-activiteit. Alleen publiek dat is gemaakt met behulp van segmentdefinities kan in deze activiteit worden gebruikt.

## Activering van niet-ondersteunde publiekstypen in [!DNL Journey Optimizer]

Alleen publiek dat is gemaakt in het portal Publiek kan rechtstreeks worden ingezet op reizen en campagnes in [!DNL Journey Optimizer] . [&#x200B; leer meer op beschikbare publiekstypes &#x200B;](../audience/about-audiences.md#types).

Als u profielen van een niet gesteund publiek, zoals een publiek van Customer Journey Analytics moet richten, moet u het in een nieuwe segmentdefinitie in het Portaal van de Publiek verpakken. De gedetailleerde informatie over hoe te om publiek in een segmentdefinitie toe te voegen is beschikbaar in de [&#x200B; documentatie van de Bouwer van het Segment &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/segmentation/ui/segment-builder#adding-audiences){target="_blank"}

Wacht tot de segmentatieevaluatie is voltooid en gebruik deze vervolgens tijdens uw reizen en campagnes.
