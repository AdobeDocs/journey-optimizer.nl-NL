---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met gegevensbronnen
description: Leer hoe u aan de slag kunt met gegevensbronnen
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: gegevens, bron, reis, platform
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: d498f32a42b13bfdee20f32a589dd31c77d88fa8
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 50%

---

# Aan de slag met gegevensbronnen {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Informatie over databronnen"
>abstract="De databronconfiguratie wordt altijd uitgevoerd door een technische gebruiker. Met de databronconfiguratie kunt u een verbinding met een systeem definiëren om extra informatie op te halen die in uw journey’s wordt gebruikt voor parameter- en personalisatiedata in acties en het definiëren van voorwaarden, tijdzones en aangepaste wachttijden."

Met de databronconfiguratie kunt u een verbinding met een systeem definiëren om extra informatie op te halen die in uw journey’s wordt gebruikt voor:

* [conditiedefinitie](../building-journeys/condition-activity.md)
* parameter- en personalisatiedata in [acties](../action/action.md)
* [aangepaste wachtdefinitie](../building-journeys/wait-activity.md#custom)
* [tijdzonedefinitie](../building-journeys/timezone-management.md)

➡️ [ ontdekt deze eigenschap in video ](#video)

Deze configuratie is niet vereist als uw journey’s alleen lokale data uit een gebeurtenispayload gebruiken. Bijvoorbeeld, als uw reis uit een gebeurtenis bestaat die door een activiteit van de kanaalactie wordt gevolgd die slechts gegevens van de gebeurtenis gebruikt, is er geen behoefte om een gegevensbron te vormen.

Er zijn twee soorten databronnen:

* De **pre-gevormde** gegevensbron van Adobe Experience Platform die de verbinding aan de Dienst van het Profiel van de Klant in real time bepaalt. Dit is een ingebouwde databron. Zie [deze pagina](../datasource/adobe-experience-platform-data-source.md).
* De **externe** gegevensbronnen die u toestaan om een verbinding aan externe systemen te bepalen. Dit zijn databronnen die u kunt maken. Zie [deze pagina](../datasource/external-data-sources.md).

>[!NOTE]
>
>Aangezien de reacties nu worden gesteund, zou u douaneacties in plaats van gegevensbronnen voor externe gegevensbronnen moeten gebruiken-gevallen. Voor meer informatie over reacties, zie deze [ sectie ](../action/action-response.md)

Voor elke databron definieert u de informatie die u wilt ophalen met behulp van veldengroepen. Veldengroepen zijn reeksen velden die uit een databron kunnen worden opgehaald. Zie [deze pagina](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Schemarelaties worden niet ondersteund voor gegevensbronnen.

Voor meer informatie over hoe te om een Source van Gegevens van Adobe Experience Platform en een externe gegevensbron te vormen en hoe te om gegevens in een reis te vinden en te gebruiken, deze [ zelfstudie video ](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html?lang=nl-NL){target="_blank"}  bekijken.

## Hoe kan ik-video {#video}

Begrijp wat een databron is en leer hoe u Experience Platform en externe databronnen kunt configureren.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

