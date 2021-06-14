---
title: Informatie over databronnen
description: Een databron configureren
feature: Databronnen
topic: Beheer
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 86%

---

# Informatie over databronnen {#concept_s1s_dqt_52b}

![](../assets/do-not-localize/badge.png)

>[!CONTEXTUALHELP]
>id="jo_datasources"
>title="Informatie over databronnen"
>abstract="De databronconfiguratie wordt altijd uitgevoerd door een technische gebruiker. Met de databronconfiguratie kunt u een verbinding met een systeem definiëren om extra informatie op te halen die in uw journey’s wordt gebruikt voor parameter- en personalisatiedata in acties en het definiëren van voorwaarden, tijdzones en aangepaste wachttijden."

Met de databronconfiguratie kunt u een verbinding met een systeem definiëren om extra informatie op te halen die in uw journey’s wordt gebruikt voor:

* [het definiëren van voorwaarden](../building-journeys/condition-activity.md)
* parameter- en personalisatiedata in [acties](../action/action.md)
* [het definiëren van aangepaste wachttijden](../building-journeys/wait-activity.md#custom)
* [het definiëren van tijdzones](../building-journeys/timezone-management.md)

Deze configuratie is niet vereist als uw journey’s alleen lokale data uit een gebeurtenispayload gebruiken. Bijvoorbeeld, als uw reis uit een gebeurtenis wordt samengesteld die door een berichtactiviteit wordt gevolgd die slechts gegevens van de gebeurtenis gebruikt, is er geen behoefte om een gegevensbron te vormen.

Er zijn twee soorten databronnen:

* De vooraf geconfigureerde Adobe Experience Platform-databron die de verbinding met de realtimeservice van het klantprofiel definieert. Dit is een ingebouwde databron. Zie [deze pagina](../datasource/adobe-experience-platform-data-source.md).
* De externe databronnen waarmee u een verbinding met externe systemen kunt definiëren. Dit zijn databronnen die u kunt maken. Zie [deze pagina](../datasource/external-data-sources.md).

Voor elke databron definieert u de informatie die u wilt ophalen met behulp van veldengroepen. Veldengroepen zijn reeksen velden die uit een databron kunnen worden opgehaald. Zie [deze pagina](../datasource/configure-data-sources.md#define-field-groups).

Voor meer informatie over het configureren van een Adobe Experience Platform-databron en een externe databron en hoe u gegevens in een journey kunt vinden en gebruiken, bekijkt u deze [zelfstudievideo](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/configure-data-sources.html).
