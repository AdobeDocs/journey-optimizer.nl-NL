---
solution: Journey Optimizer
product: journey optimizer
title: De expressie-editor
description: Leer hoe u met de Expressieeditor werkt.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expression, editor, about, start
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 1%

---

# De expressie-editor {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="De expressie-editor"
>abstract="Met de Expressieeditor kunt u alle gegevens selecteren, rangschikken, aanpassen en valideren om een aangepaste personalisatie voor uw inhoud te maken."

De redacteur van de Uitdrukking is het middelstuk van de verpersoonlijking in [!DNL Journey Optimizer]. Het is beschikbaar in elke context waarin u personalisatie als e-mail, push en aanbiedingen moet definiëren.

In de interface van de uitdrukkingsredacteur, zult u, alle gegevens selecteren schikken aanpassen en bevestigen om een aangepaste verpersoonlijking voor uw inhoud tot stand te brengen.

![](assets/perso_ee1.png)

In het linkergedeelte van het scherm wordt een domeinkiezer weergegeven waarmee u de bron voor personalisatie kunt selecteren.

![](assets/perso_ee3.png)

Beschikbare bronnen zijn:

* **[!UICONTROL Profile attributes]** : Hiermee worden alle verwijzingen weergegeven die zijn gekoppeld aan het profielschema dat wordt beschreven in [Adobe Experience Platform Data Model (XDM)-documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"}.
* **[!UICONTROL Segment memberships]** : maakt een lijst van alle segmenten die in de dienst van de Segmentatie van Adobe Experience Platform worden gecreeerd. Meer informatie over segmentatie is beschikbaar [hier](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target="_blank"}.
* **[!UICONTROL Offer decisions]** : geeft een overzicht van alle aanbiedingen verbonden aan een specifieke plaatsing. Selecteer de plaatsing en voeg de aanbiedingen in uw inhoud in. Voor volledige documentatie over het beheren van aanbiedingen raadpleegt u [deze sectie](../email/add-offers-email.md).
* **[!UICONTROL Contextual attributes]** : Wanneer een activiteit van de kanaalactie (E-mail, duw, SMS) in een reis wordt gebruikt, zijn de contextafhankelijke reisgebieden beschikbaar door dit menu. Meer informatie in [deze sectie](personalization-use-case.md).
* **[!UICONTROL Helper functions]** : Hiermee worden alle hulpfuncties weergegeven die beschikbaar zijn om bewerkingen uit te voeren op gegevens, zoals berekeningen, gegevensopmaak of conversies, voorwaarden en deze te manipuleren in de context van personalisatie. Meer informatie in [deze sectie](functions/functions.md).

Klik op + om een kenmerk toe te voegen aan de editor.

>[!NOTE]
>
>Met het ovaalmenu naast het pictogram &quot;+&quot; kunt u meer details voor elke variabele ophalen en uw meest gebruikte kenmerken toevoegen aan [favorieten](personalization-favorites.md).

![](assets/attribute-details.png)

In het volgende voorbeeld, laat de uitdrukkingsredacteur u de profielen selecteren die hun verjaardag vandaag hebben dan de aanpassing voltooien door een specifieke aanbieding op te nemen die aan deze dag beantwoordt.

![](assets/perso_ee2.png)

Zodra uw verpersoonlijkingsuitdrukking klaar is, moet u het hebben door de redacteur van de Uitdrukking worden bevestigd. Meer informatie in [deze sectie](personalization-validation.md).
