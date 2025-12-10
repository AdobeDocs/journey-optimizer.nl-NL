---
solution: Journey Optimizer
product: journey optimizer
title: Verticale uitlijning en opvulling aanpassen in Journey Optimizer
description: Leer hoe u de verticale uitlijning en opvulling kunt aanpassen
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: verticale uitlijning, e-maileditor, opvulling
exl-id: 1e1d90ff-df5d-4432-a63a-a32d0d281d48
source-git-commit: 4817b7426abf202c886b7fd63d59aa0f245e5496
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# Verticale uitlijning en opvulling aanpassen {#alignment-and-padding}

In dit voorbeeld passen we opvulling en verticale uitlijning aan binnen een structuurcomponent die uit drie kolommen bestaat.

1. Selecteer de structuurcomponent rechtstreeks in de e-mail of met behulp van de **[!UICONTROL Navigation tree]** -component die beschikbaar is in het linkermenu.

1. Klik in de werkbalk op **[!UICONTROL Select a column]** en kies de werkbalk die u wilt bewerken. U kunt deze ook selecteren in de boomstructuur.

   De bewerkbare parameters voor die kolom worden weergegeven op het tabblad **[!UICONTROL Styles]** .

   ![](assets/alignment_2.png)

1. Selecteer onder **[!UICONTROL Alignment]** de optie **[!UICONTROL Top]** , **[!UICONTROL Middle]** of **[!UICONTROL Bottom]** .

   ![](assets/alignment_3.png)

1. Definieer onder **[!UICONTROL Padding]** de opvulling voor alle zijden.

   Selecteer **[!UICONTROL Different padding for each side]** als u de opvulling wilt verfijnen. Klik op het vergrendelingspictogram om de synchronisatie te verbreken.

   ![](assets/alignment_4.png)

1. Ga op dezelfde manier te werk om de uitlijning en opvulling van de andere kolommen aan te passen.

1. Sla uw wijzigingen op.

>[!TIP]
>
>Zorg ervoor dat bij het ontwerpen van e-mailinhoud voor Gmail op Android-apparaten de opvulling van kolommen wordt gebruikt in plaats van grote, vaste marges. Bij Gmail op Android worden te grote afbeeldingen en marges vaak onjuist weergegeven, waardoor de lay-out overloopt of de scheidingslijnen afnemen. Gebruik een kleinere afbeeldingsbreedte of gebruik op kolom gebaseerde opvulling voor een consistente weergave.

## Fragmentopvulling beheren met breedbandnavigatie {#fragment-padding-breadcrumb}

Wanneer het werken met [&#x200B; fragmenten &#x200B;](../content-management/fragments.md) in E-mail Designer, kunt u verborgen of residuele opvulling tegenkomen die mobiel het teruggeven verschillend dan Desktop beïnvloedt. Dit is met name gemeenschappelijk wanneer de fragmenten zijn ontgrendeld of wanneer [&#x200B; overerving &#x200B;](use-visual-fragments.md#break-inheritance) gebroken is, aangezien de leftover het stileren in de onderliggende kolom of tekstcomponenten kan blijven.

Zo kunt u overvulopvulling in fragmenten identificeren en bewerken:

1. Gebruik **[!UICONTROL Navigation tree]** of klik direct op elementen in de redacteur om elke ouderstructuur of kolom binnen uw fragment te selecteren. Zo kunt u verborgen opvulling of marge zoeken die specifiek is voor mobiele apparaten.

1. Na het selecteren van het element in de broodkruimel, navigeer aan het **[!UICONTROL Styles]** lusje op het recht.

1. Controleer de **[!UICONTROL Padding]** -instellingen en verwijder of pas de opvulling zo nodig aan om de mobiele uitlijning te corrigeren.

1. Als er zich problemen met de uitlijning blijven voordoen wanneer u fragmenten opnieuw gebruikt, herhaalt u dit proces voor andere kolommen of tekstcomponenten in het fragment.

>[!NOTE]
>
>Dit gedrag wordt verwacht wanneer fragmenten herhaaldelijk worden ingevoegd en verwijderd, omdat opmaakregels zich kunnen ophopen. Controleer altijd de opvullingswaarden met behulp van de breedbandnavigatie, vooral wanneer u zich richt op mobiele apparaten.