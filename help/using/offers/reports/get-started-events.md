---
title: Aan de slag met Beslissingsbeheergebeurtenissen
description: Leer hoe u Beslissingsbeheerrapporten maakt in Adobe Experience Platform.
feature: Aanbiedingen
topic: Integraties
role: User
level: Beginner
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 47%

---

# Aan de slag met Beslissingsbeheergebeurtenissen {#monitor-offer-events}

Telkens wanneer Beslissingsbeheer een besluit neemt voor een bepaald profiel, wordt informatie over deze gebeurtenissen automatisch naar Adobe Experience Platform verzonden.

Op deze manier kunt u deze gegevens exporteren om ze te analyseren in uw eigen rapportagesysteem. U kunt de Adobe Experience Platform [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=nl) ook gebruiken in combinatie met andere tools voor verbeterde analyse- en rapportagedoeleinden.

De datasets met de gebeurtenissen van het Beheer van het Besluit zijn toegankelijk van Adobe Experience Platform **[!UICONTROL Datasets]** menu. Eén dataset wordt automatisch gemaakt bij het invullen van elk van uw instanties.

![](../../assets/events-datasets-list.png)

Deze datasets zijn gebaseerd op het **[!UICONTROL ODE DecisionEvents]** schema, dat alle gebieden XDM bevat die worden vereist om informatie van het Beheer van het Besluit naar Adobe Experience Platform te verzenden.

>[!NOTE]
>
>Merk op dat de datasets van ODE DecisionEvents **niet-profieldatasets** zijn, wat betekent dat ze niet in Experience Platform kunnen worden opgenomen voor gebruik door het realtimeklantprofiel.

**Verwante onderwerpen:**

* [Belangrijke informatie over gebeurtenissen met betrekking tot Beslissingsbeheer](../reports/key-information.md)
* [Toegang tot gebeurtenissen van XDM-velden](../reports/xdm-fields.md)
