---
solution: Journey Optimizer
product: journey optimizer
title: Informatie over databronnen
description: Een databron configureren
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 73%

---

# Databronnen {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Informatie over databronnen"
>abstract="De databronconfiguratie wordt altijd uitgevoerd door een technische gebruiker. Met de databronconfiguratie kunt u een verbinding met een systeem definiëren om extra informatie op te halen die in uw journey’s wordt gebruikt voor parameter- en personalisatiedata in acties en het definiëren van voorwaarden, tijdzones en aangepaste wachttijden."

Met de databronconfiguratie kunt u een verbinding met een systeem definiëren om extra informatie op te halen die in uw journey’s wordt gebruikt voor:

* [het definiëren van voorwaarden](../building-journeys/condition-activity.md)
* parameter- en personalisatiedata in [acties](../action/action.md)
* [het definiëren van aangepaste wachttijden](../building-journeys/wait-activity.md#custom)
* [het definiëren van tijdzones](../building-journeys/timezone-management.md)

➡️ [Ontdek deze functie in video](#video)

Deze configuratie is niet vereist als uw journey’s alleen lokale data uit een gebeurtenispayload gebruiken. Bijvoorbeeld, als uw reis uit een gebeurtenis bestaat die door een activiteit van de kanaalactie wordt gevolgd die slechts gegevens van de gebeurtenis gebruikt, is er geen behoefte om een gegevensbron te vormen.

Er zijn twee soorten databronnen:

* De vooraf geconfigureerde Adobe Experience Platform-databron die de verbinding met de realtimeservice van het klantprofiel definieert. Dit is een ingebouwde databron. Zie [deze pagina](../datasource/adobe-experience-platform-data-source.md).
* De externe databronnen waarmee u een verbinding met externe systemen kunt definiëren. Dit zijn databronnen die u kunt maken. Zie [deze pagina](../datasource/external-data-sources.md).

Voor elke databron definieert u de informatie die u wilt ophalen met behulp van veldengroepen. Veldengroepen zijn reeksen velden die uit een databron kunnen worden opgehaald. Zie [deze pagina](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Schemarelaties worden niet ondersteund voor gegevensbronnen.

Voor meer informatie over hoe te om een Gegevensbron van Adobe Experience Platform en een externe gegevensbron te vormen en hoe te om gegevens in een reis te vinden en te gebruiken, bekijk dit [zelfstudievideo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target=&quot;_blank&quot;}.

## Hoe kan ik-video {#video}

Begrijp wat een databron is en leer hoe u Experience Platform en externe databronnen kunt configureren.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

