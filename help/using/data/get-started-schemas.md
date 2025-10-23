---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met schema's
description: Meer informatie over het gebruik van Adobe Experience Platform-schema's in Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: schema's, platform, gegevens, structuur
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Aan de slag met schema&#39;s {#schemas-gs}

[!DNL Adobe Journey Optimizer] baseert zich op **schema&#39;s van Adobe Experience Platform** om de structuur van gegevens op een verenigbare en herbruikbare manier te beschrijven. Een schema biedt een abstracte definitie van een echt object (zoals een persoon) en geeft aan welke gegevens in elke instantie van dat object moeten worden opgenomen (zoals naam, geboortedatum, enzovoort). Wanneer het gegeven in Experience Platform wordt opgenomen, is het altijd gestructureerd volgens een **schema XDM**.

## Standaard- en modelgebaseerde schema&#39;s

Er zijn twee soorten schema&#39;s in Adobe Experience Platform:

* **Standaard schema&#39;s** zijn hiërarchische schema&#39;s die klassen en gebiedsgroepen gebruiken om verslag of tijd-reeksgegevens te vangen.

  Een standaardschema bestaat uit:

   * A **klasse** (die het gegevensgedrag bepaalt: verslag of tijd-reeks).
   * Één of meerdere **gebiedsgroepen** (die specifieke gebieden aan het schema toevoegen).

  In Journey Optimizer, worden de standaardschema&#39;s typisch gebruikt om **individuele mensen en hun attributen** te vertegenwoordigen, vangen **tijd-reeksen interactie** zoals kliks, aankopen, of logins, en macht **Real-Time Profiel van de Klant** voor segmentatie en verpersoonlijking.

  ➡️ [&#x200B; Leer om een standaardschema in deze video &#x200B;](#video-schema) tot stand te brengen en te vormen (video)

* **model-gebaseerde schema&#39;s** zijn vlakke, niet-hiërarchische schema&#39;s die geen klassen of gebiedsgroepen gebruiken. Zij worden gebruikt om verslaggegevens voor relationele entiteiten te vangen en worden hoofdzakelijk gebruikt in [!DNL Journey Optimizer] **Geordende campagnes**.

  Voorbeelden van relationele entiteiten zijn:
   * Boeken, contracten of abonnementen
   * Producten of catalogi
   * Winkels, locaties of partners

  Met model-gebaseerde schema&#39;s, kunt u één bericht per entiteit (b.v., per boek, per abonnement) verzenden, segmenten creëren die op entiteitattributen (b.v., productcategorie, opslagplaats) worden gebaseerd, en adressability verbeteren door alle contacten te bereiken verbonden aan een entiteit.

  Hoe modelgebaseerde schema&#39;s werken:

   1. **creeer schema&#39;s manueel of de invoer via DDL**
   1. **schema&#39;s van de Verbinding** om verhoudingen tussen entiteiten en mensen (b.v., loyaliteitstransacties te bepalen verbonden aan leden, beloningen verbonden aan merken).
   1. **Samenvatting gegevens** in uw dataset van gesteunde bronnen.

  ➡️ [&#x200B; Leer hoe te om op model-gebaseerde schema&#39;s en datasets &#x200B;](../orchestrated/gs-schemas.md) te beheren
➡️ [&#x200B; worden begonnen met Geordende campagnes &#x200B;](../orchestrated/gs-schemas.md)

## Hoe kan ik-video{#video-schema}

Leer hoe u een standaardschema maakt, veldgroepen toevoegt, aangepaste veldgroepen maakt en configureert.

>[!VIDEO](https://video.tv.adobe.com/v/334461?quality=12)

>[!MORELIKETHIS]
>
>* [&#x200B; creeer een schema, een dataset en neemt gegevens op om de profielen van de Test in Journey Optimizer toe te voegen &#x200B;](../audience/creating-test-profiles.md)
>* [&#x200B; XDM overzicht van het Systeem &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"}
>* [&#x200B; Beste praktijken voor gegevens modelleren &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=nl-NL){target="_blank"}
>* [&#x200B; creeer een schema gebruikend de Registratie API van het Schema &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=nl-NL){target="_blank"}
>* [&#x200B; bepaal een verband tussen twee schema&#39;s gebruikend de Redacteur van het Schema &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=nl-NL){target="_blank"}
