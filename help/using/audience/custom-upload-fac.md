---
solution: Journey Optimizer
product: journey optimizer
title: Aangepaste upload (CSV) en federatieve compositie van publiek
description: Leer belangrijke informatie en beste praktijken terwijl het werken met het uploaden van de Douane (CSV) en Federated publiek van de Samenstelling van de Publiek.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
source-git-commit: 26d311802236a1f9e8f6273c1291bcb54138aad2
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 2%

---

# Aangepaste upload (CSV) en federatieve compositie van publiek {#csv-fac}

## Info over Aangepaste upload en Federatieve Audience Composition {#about}

Naast segmentdefinities en publiekscompositie kunt u in [!DNL Journey Optimizer] doelgroepen genereren en instellen door deze uit een CSV-bestand te importeren of gegevens uit uw gegevenspakhuis te gebruiken.

* **Douane uploadt**: Invoer een publiek gebruikend een Csv- dossier. Leer hoe te om publiek in de documentatie van de Dienst van de Segmentatie van Adobe Experience Platform [ in te voeren ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience) {target="_blank"}.

* **Federated Audience Composition**: De datasets van de federatie direct van uw bestaand gegevenspakhuis om het publiek en de attributen van Adobe Experience Platform allen in één systeem te bouwen en te verrijken. Gelieve te lezen de gids op [ Federated de Samenstelling van het Publiek ](https://experienceleague.adobe.com/en/docs/federated-audience-composition/using/home).

  >[!AVAILABILITY]
  >
  >Federated Audience Composition is momenteel alleen beschikbaar voor een set organisaties (beperkte beschikbaarheid). Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

U kunt deze doelgroep in Journey Optimizer activeren of activeren naar een bestemming die wordt ondersteund door Adobe Experience Platform

➡️ [ ontdekt deze eigenschappen in video ](#video)

## Lees hier meer {#must-read}

Deze sectie bevat belangrijke informatie waarmee u rekening kunt houden wanneer u werkt met Aangepast uploaden (CSV-bestanden) en Federatieve publiek compositie.

* **Voorproef en proefdruksteun:** momenteel, wordt de voorproef en de proef niet gesteund voor publiek dat gebruikend CSV wordt gecreeerd uploadt of Federated de Samenstelling van het Publiek. Houd dit in gedachten wanneer u uw campagnes plant.

* **de vertraging van de Activering:** het publiek is klaar voor gebruik in Journey Optimizer recht nadat het opnemen voltooit. Hoewel dit meestal binnen een uur ligt, is het afhankelijk van enige variabiliteit.

* **Geactiveerde verslagen &amp; identiteitsstitching:** Elk verslag in het publiek wordt geactiveerd, met inbegrip van om het even welke duplicaten. Tijdens de volgende UPS-profielexport worden deze records aan identiteitsstitching onderworpen. Hierdoor kan het aantal geactiveerde records afwijken van het aantal profielen na identiteitsstitching.

* **richtend nieuwe profielen:** wanneer een gelijke niet tussen een verslag en een profiel van UPS wordt gevonden, wordt een nieuw leeg profiel gecreeerd. Dit profiel is gekoppeld aan de verrijkingskenmerken die zijn opgeslagen in het datumpeer. Omdat dit nieuwe profiel leeg is, zijn velden die doorgaans worden gebruikt in Journey Optimizer (bijvoorbeeld PersonalEmail.address, mobilePhone.number) leeg en kunnen deze daarom niet worden gebruikt voor het opgeven van doelen.

  Om dit op te lossen, kunt u het &quot;uitvoeringsgebied&quot;(of &quot;uitvoeringsadres&quot;afhankelijk van het kanaal) in de kanaalconfiguratie als &quot;identityMap&quot;specificeren. Hierdoor wordt gegarandeerd dat het kenmerk dat wordt gekozen als de identiteit bij het maken van een publiek, het kenmerk is dat wordt gebruikt voor het maken van een doelaccount in Journey Optimizer.

## Hoe kan ik-video&#39;s {#video}

Leer hoe u publiek in CSV-indeling kunt uploaden naar Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3421714?quality=12)

Meer informatie over Federated Audience Composition.

>[!VIDEO](https://video.tv.adobe.com/v/3432261?quality=12)
