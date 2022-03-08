---
title: Over de Expressieeditor
description: Leer hoe u met de Expressieeditor werkt.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 1%

---

# Over de Expressieeditor {#build-personalization-expressions}

De uitdrukkingsredacteur is het middelstuk van de verpersoonlijking in [!DNL Journey Optimizer]. Het is beschikbaar in elke context waarin u personalisatie als e-mail, push en aanbiedingen moet definiëren.

In de interface van de uitdrukkingsredacteur, zult u, alle gegevens selecteren schikken aanpassen en bevestigen om een aangepaste verpersoonlijking voor uw inhoud tot stand te brengen.

![](assets/perso_ee1.png)

In het linkergedeelte van het scherm wordt een domeinkiezer weergegeven waarmee u de bron voor personalisatie kunt selecteren.

![](assets/perso_ee3.png)

Beschikbare bronnen zijn:

* **[!UICONTROL Profile attributes]** : Hiermee worden alle verwijzingen weergegeven die zijn gekoppeld aan het profielschema dat wordt beschreven in [Adobe Experience Platform Data Model (XDM)-documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target=&quot;_blank&quot;}.
* **[!UICONTROL Segment memberships]** : maakt een lijst van alle segmenten die in de dienst van de Segmentatie van Adobe Experience Platform worden gecreeerd. Meer informatie over segmentatie is beschikbaar [hier](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Offer decisions]** : geeft een overzicht van alle aanbiedingen verbonden aan een specifieke plaatsing. Selecteer de plaatsing en voeg de aanbiedingen in uw inhoud in. Voor volledige documentatie over het beheren van aanbiedingen raadpleegt u [deze sectie](../messages/deliver-personalized-offers.md).
* **[!UICONTROL Contextual attributes]** : wanneer de **Bericht** wordt gebruikt in een reis, zijn de contextuele reisgebieden beschikbaar door dit menu. Meer informatie in [deze sectie](personalization-use-case.md).
* **[!UICONTROL Helper functions]** : Hiermee worden alle hulpfuncties weergegeven die beschikbaar zijn om bewerkingen uit te voeren op gegevens, zoals berekeningen, gegevensopmaak of conversies, voorwaarden en deze te manipuleren in de context van personalisatie. Meer informatie in [deze sectie](functions/functions.md).

Bij selectie wordt de verwijzing toegevoegd in de editor.

>[!NOTE]
>
>Het infopictogram naast &quot;+&quot;pictogram opent omhoog tooltip die meer details voor elke variabele verstrekt.
>
>U kunt uw meest gebruikte kenmerken aan favorieten toevoegen. Meer informatie in [deze sectie](personalization-favorites.md).

In het volgende voorbeeld, laat de uitdrukkingsredacteur u de profielen selecteren die hun verjaardag vandaag hebben dan de aanpassing voltooien door een specifieke aanbieding op te nemen die aan deze dag beantwoordt.

![](assets/perso_ee2.png)

Zodra uw verpersoonlijkingsuitdrukking klaar is, moet u het hebben door de Redacteur van de Uitdrukking worden bevestigd. Meer informatie in [deze sectie](personalization-validation.md).
