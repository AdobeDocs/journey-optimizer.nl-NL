---
title: Belangrijke informatie over gebeurtenissen met betrekking tot Beslissingsbeheer
description: Meer informatie over de belangrijkste informatie die met elke Beslissingsbeheergebeurtenis wordt verzonden.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 07be59e8-e994-4854-8089-25614d005dbe
source-git-commit: 14ab70aa32f4f7978b8c72b3981d3b55f56fd08b
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 78%

---

# Belangrijke informatie over gebeurtenissen met betrekking tot Beslissingsbeheer {#events-key-information}

Elke gebeurtenis die wordt verzonden wanneer een besluit wordt genomen, bevat vier belangrijke gegevenspunten die u voor analyse en rapportagedoeleinden kunt gebruiken.

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: naam en ID van de alternatieve aanbieding als er geen persoonlijke aanbieding is geselecteerd;
* **[!UICONTROL Placement]**: naam, id en kanaal van de plaatsing die voor de aanbieding wordt gebruikt;
* **[!UICONTROL Selections]**: naam en id van de voor het profiel geselecteerde aanbieding;
* **[!UICONTROL Activity]**: Naam en ID van de beslissing.

Daarnaast kunt u ook de **[!UICONTROL identityMap]** en **[!UICONTROL Timestamp]**-velden gebruiken om informatie op te halen over het profiel en het tijdstip waarop de aanbieding is geleverd.

Raadpleeg voor meer informatie over alle XDM-velden die bij elke beslissing worden verzonden, [deze sectie](xdm-fields.md).
