---
title: Aan de slag met Beslissingsbeheergebeurtenissen
description: Leer hoe u Beslissingsbeheerrapporten maakt in Adobe Experience Platform.
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 47%

---

# Aan de slag met Beslissingsbeheergebeurtenissen {#monitor-offer-events}

Telkens wanneer Beslissingsbeheer een besluit neemt voor een bepaald profiel, wordt informatie over deze gebeurtenissen automatisch naar Adobe Experience Platform verzonden.

Op deze manier kunt u deze gegevens exporteren om ze te analyseren in uw eigen rapportagesysteem. U kunt de Adobe Experience Platform [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=nl) ook gebruiken in combinatie met andere tools voor verbeterde analyse- en rapportagedoeleinden.

De datasets met gebeurtenissen van het Besluit Management zijn toegankelijk vanuit Adobe Experience Platform **[!UICONTROL Datasets]** -menu. Eén dataset wordt automatisch gemaakt bij het invullen van elk van uw instanties.

![](../../assets/events-datasets-list.png)

Deze gegevensbestanden zijn gebaseerd op de **[!UICONTROL ODE DecisionEvents]** schema, dat alle XDM gebieden bevat die worden vereist om informatie van Beslissingsbeheer naar Adobe Experience Platform te verzenden.

>[!NOTE]
>
>Merk op dat de datasets van ODE DecisionEvents **niet-profieldatasets** zijn, wat betekent dat ze niet in Experience Platform kunnen worden opgenomen voor gebruik door het realtimeklantprofiel.

**Verwante onderwerpen:**

* [Belangrijke informatie over gebeurtenissen met betrekking tot Beslissingsbeheer](../reports/key-information.md)
* [Toegang tot gebeurtenissen van XDM-velden](../reports/xdm-fields.md)
