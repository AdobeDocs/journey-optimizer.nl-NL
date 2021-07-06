---
title: Aangepaste handelingen gebruiken
description: Leer hoe u aangepaste handelingen kunt gebruiken
feature: Journeys
topic: Contentmanagement
role: User
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 2%

---

# Aangepaste handelingen gebruiken {#section_f2c_hbg_nhb}

Als u een douaneactie gebruikt, zult u, in read-only, de **[!UICONTROL URL Configuration]** en **[!UICONTROL Authentication]** parameters zien die in het scherm van de actieconfiguratie worden bepaald (zie [deze pagina](../action/about-custom-action-configuration.md)).

>[!NOTE]
>
>U kunt geen verzameling doorgeven in parameters voor aangepaste handelingen. Als de douaneactie inzamelingen verwacht, zal het niet werken. Let ook op dat de parameters een verwacht formaat hebben (voorbeeld: tekenreeks, decimaal, enz.). U moet deze verwachte formaten zorgvuldig respecteren.

In **[!UICONTROL Action parameters]** sectie, zult u de berichtparameters zien die als _&quot;Variabele&quot;_ worden bepaald. Voor deze parameters kunt u definiëren waar deze informatie moet worden opgehaald (voorbeeld: gebeurtenissen, gegevensbronnen), geeft u waarden handmatig door of gebruikt u de geavanceerde expressie-editor voor gevallen van geavanceerd gebruik. Gevallen van geavanceerd gebruik kunnen gegevensmanipulatie en ander functiegebruik zijn. Zie [Adobe Journey Orchestration documentatie](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html){target=&quot;_blank&quot;}.
