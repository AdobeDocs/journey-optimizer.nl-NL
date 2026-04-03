---
solution: Journey Optimizer
product: journey optimizer
title: AEM-inhoudsfragmenten
description: Leer hoe u AEM Content Fragments kunt openen en beheren
topic: Content Management
role: User
level: Beginner
source-git-commit: 4f7e36a6cc19e4138e867950e34c5a5e6452b364
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Aan de slag met Adobe Experience Manager-inhoudsfragmenten {#aem-fragments}

>[!AVAILABILITY]
>
>Voor klanten in de gezondheidszorg is de integratie alleen mogelijk na het in licentie geven van het Journey Optimizer Healthcare Shield- en Adobe Experience Manager Enhanced Security-add-on-aanbod.

Door Adobe Experience Manager as a Cloud Service te integreren met Adobe Journey Optimizer, kunt u nu uw AEM-inhoudsfragmenten naadloos opnemen in uw Journey Optimizer-inhoud. Deze gestroomlijnde verbinding vereenvoudigt het proces van toegang tot en gebruik van AEM-inhoud, waardoor persoonlijke en dynamische campagnes en reizen kunnen worden gemaakt.

Meer over de Fragmenten van de Inhoud van AEM leren, verwijs naar [&#x200B; Werkend met de Fragmenten van de Inhoud &#x200B;](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} in de documentatie van Experience Manager.

## Levenscyclus van inhoudsfragment

![](assets/do-not-localize/AEM_CF.png)

Inhoudsfragmenten volgen verschillende fasen in de levenscyclus, afhankelijk van de Adobe Experience Manager-laag waarin ze voorkomen. [&#x200B; leer meer in de documentatie van Adobe Experience Manager &#x200B;](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

De inhoud wordt gecreeerd en op de **rij van de Auteur** geleid, waar de fragmenten statussen zoals Nieuw, Ontwerp, Gepubliceerd, Gewijzigd, of Unpublished kunnen hebben. Deze statussen zijn slechts op de **rij van de Auteur** van toepassing en steunen inhoudsverwezenlijking en overzicht.

Wanneer een tevreden Fragment wordt gepubliceerd, wordt een exemplaar gecreeerd op **publiceer rij** en blootgesteld door een openbaar, niet voor authentiek verklaard eindpunt. Journey Optimizer integreert exclusief met dit **publiceer rij**.

Als gevolg hiervan heeft Journey Optimizer alleen oppervlakken van Gepubliceerde of Gewijzigde inhoudsfragmenten en wordt altijd de meest recente gepubliceerde versie gebruikt. Wijzigingen die na publicatie worden aangebracht, worden pas in Journey Optimizer doorgevoerd als het inhoudsfragment opnieuw wordt gepubliceerd.
