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
source-git-commit: 62c0c1f46b5bd575102d9f27037cb6add1355ba2
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# Activering van het publiek in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

U kunt in campagnes selecteren en reizen om het even welk publiek dat gebruikend segmentdefinities, douane wordt geproduceerd uploadt, samenstellingswerkschema&#39;s of Federated de Samenstelling van de Publiek wordt geproduceerd.

>[!AVAILABILITY]
>
>Het gebruik van soorten publiek en kenmerken van de samenstelling van het publiek is momenteel niet beschikbaar voor gebruik met het gezondheidsschild of het privacyschild. [&#x200B; Leer hoe te om de attributen van de kijkverrijking in Journey Optimizer te gebruiken &#x200B;](../audience/about-audiences.md#enrichment)

## Activeringsvertraging van soorten publiek {#activation}

Soorten publiek zijn direct na inname klaar voor gebruik in Journey Optimizer. Hoewel dit meestal binnen een uur ligt, is het afhankelijk van enige variabiliteit. Het publiek dat uit samenstellingen voortvloeit, moet 24 uur na publicatie beschikbaar zijn.

Voor het publiek dat het resultaat is van batchsegmentatietaken, kan de activering vertraagd zijn vanwege variabiliteit in de inname van batch. Voor ritten voor lezers die dagelijks worden gepland, kunt u een tijdvenster in de reiseigenschappen bepalen om ervoor te zorgen dat nieuwe publieksgegevens beschikbaar zijn vóór de uitvoering van de reis. Als de segmentatietaak niet binnen het bepaalde tijdvenster wordt voltooid, wordt de reis overgeslagen tot het volgende exemplaar. [&#x200B; Leer hoe te om een Lezen-publiek reis &#x200B;](../building-journeys/read-audience.md) te plannen

## Aangepaste upload en Federatieve Audience Composition

Houd rekening met de volgende instructies voor het publiek Aangepaste upload en Federatieve Audience Composition:

* **Voorproef en proefdruksteun:** momenteel, wordt de voorproef en de proef niet gesteund voor publiek dat gebruikend CSV wordt gecreeerd uploadt of Federated de Samenstelling van het Publiek. Houd dit in gedachten wanneer u uw campagnes plant.

* **richtend nieuwe profielen:** wanneer een gelijke niet tussen een verslag en een Verenigd profiel van de Dienst van het Profiel wordt gevonden, wordt een nieuw leeg profiel gecreeerd. Dit profiel is gekoppeld aan de verrijkingskenmerken die zijn opgeslagen in het datumpeer. Omdat dit nieuwe profiel leeg is, zijn velden die doorgaans worden gebruikt in Journey Optimizer (bijvoorbeeld PersonalEmail.address, mobilePhone.number) leeg en kunnen deze daarom niet worden gebruikt voor het opgeven van doelen.

  Om dit op te lossen, kunt u het &quot;uitvoeringsgebied&quot;(of &quot;uitvoeringsadres&quot;afhankelijk van het kanaal) in de kanaalconfiguratie als &quot;identityMap&quot;specificeren. Hierdoor wordt gegarandeerd dat het kenmerk dat wordt gekozen als de identiteit bij het maken van een publiek, het kenmerk is dat wordt gebruikt voor het maken van een doelaccount in Journey Optimizer.

* **Geactiveerde verslagen &amp; identiteitsstitching:** Elk verslag in het publiek wordt geactiveerd, met inbegrip van om het even welke duplicaten. Tijdens de volgende Verenigde het profieluitvoer van de Dienst van het Profiel, zullen deze verslagen door identiteit stitching gaan. Hierdoor kan het aantal geactiveerde records afwijken van het aantal profielen na identiteitsstitching.

## Doelpubliek in [!DNL Journey Optimizer]

U kunt het publiek op verschillende manieren gebruiken in **[!DNL Journey Optimizer]** :

* Kies een publiek voor a **campagne**, waar het bericht wordt verzonden naar alle individuen die tot het geselecteerde publiek behoren. [&#x200B; Leer hoe te om het publiek van een campagne &#x200B;](../campaigns/create-campaign.md#define-the-audience-audience) te bepalen.

* Gebruik a **Gelezen publiek** orkestactiviteit in een reis om alle individuen in het publiek te maken de reis ingaan en de berichten ontvangen inbegrepen in uw reis. Laten we zeggen dat je een &quot;zilveren klant&quot; publiek hebt. Met deze activiteit, kunt u alle zilveren klanten een reis maken en hen een reeks gepersonaliseerde berichten verzenden. [&#x200B; Leer hoe te om Gelezen publieksactiviteit &#x200B;](../building-journeys/read-audience.md#configuring-segment-trigger-activity) te vormen.

  >[!NOTE]
  >
  >Elke reis die een publiek van publiekssamenstelling of douane uploadt in de activiteit van het &quot;Gelezen publiek&quot;gebruikt zal profielattributen zo vers zoals de laatste partijevaluatie hebben. Dit omvat toestemming/onderdrukking tijdens de reis.

* Gebruik de **activiteit van de Voorwaarde** in een reis om voorwaarden te bouwen die op publiekslidmaatschap worden gebaseerd. [&#x200B; leer hoe te om publiek in voorwaarden &#x200B;](../building-journeys/condition-activity.md#using-a-segment) te gebruiken.

* Gebruik de **gebeurtenisactiviteit van de Kwalificatie van het publiek 0&rbrace; &lbrace;in een reis om individuen te maken ingaan of zich voorwaarts in de reis gebaseerd op de kijkposten van Adobe Experience Platform en uitgang.** U kunt bijvoorbeeld alle nieuwe zilverklanten een reis laten maken en hun berichten sturen. Voor meer op hoe te om deze activiteit te gebruiken, verwijs naar [&#x200B; hoe te om een de kwalificatieactiviteit van het Publiek te vormen &#x200B;](../building-journeys/audience-qualification-events.md).

  >[!NOTE]
  >
  >Vanwege het batchkarakter van publiek dat is gemaakt met gebruik van compositieworkflows, aangepaste upload of Federated Audience Composition, kunt u deze soorten publiek niet als doelgroep instellen in een &#39;Audience Qualification&#39;-activiteit. Alleen publiek dat is gemaakt met behulp van segmentdefinities kan in deze activiteit worden gebruikt.
