---
title: Een bericht publiceren en wijzigen
description: Leer hoe u uw berichten publiceert en bijwerkt
snippet: y
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 116e2223-a806-4f68-9a8c-c0bde6008010
source-git-commit: ca4c2d916a2ebde643656b4573e34d6bb64053fa
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 2%

---

# Uw berichten publiceren {#publish-manage-messages}

## Een bericht publiceren {#publish-message}

Zodra uw bericht is gecreeerd, kunt u het publiceren om het voor uitvoering ter beschikking te stellen.

>[!CAUTION]
>
>Controleer en los waarschuwingen op voordat u ze publiceert. [Meer informatie](alerts.md)

![](assets/publish-message.png)

Zodra uw bericht wordt gepubliceerd, wordt het toegevoegd aan de berichtlijst met **[!UICONTROL Published]** status.

Het is nu gereed om te worden geactiveerd door een of meer [reizen](building-journeys/journey.md).

>[!NOTE]
>
>Wanneer u een aanbod, een fallback-aanbieding, een verzameling van aanbiedingen of een besluit van een aanbieding bijwerkt waarnaar direct of indirect wordt verwezen in een gepubliceerd bericht, worden de updates nu automatisch weerspiegeld in het bijbehorende bericht, zonder dat u het bericht opnieuw hoeft te publiceren. [Meer weten over aanbiedingen](offers/get-started/starting-offer-decisioning.md)

## Een alleen-lezen bericht bijwerken {#modify-message}

Na publicatie wordt een bericht alleen-lezen weergegeven. U kunt het nog steeds bijwerken door een nieuw concept van dat bericht te maken.

Op deze manier kunt u bijvoorbeeld inhoud bijwerken of een probleem verhelpen zonder de hele reis waar uw bericht wordt gebruikt opnieuw te publiceren.

>[!NOTE]
>
>De conceptversie kan worden bewerkt terwijl de gepubliceerde versie nog wordt gepubliceerd en actief is.

Een gepubliceerd bericht bijwerken:

1. Selecteer in de berichtenlijst het bericht dat u wilt openen.

1. Klik op **[!UICONTROL Modify]**.

   ![](assets/message-modify.png)

1. Bevestig uw keuze. Er wordt een conceptversie van het bericht gemaakt.

   ![](assets/message-modify-v2.png)

1. Bewerk de inhoud of wijzig de instellingen naar wens.
1. Klik op **[!UICONTROL Publish]**. Deze actie zal de nieuwe versie van het bericht publiceren dat voor de volgende uitvoeringen zal worden gebruikt.

Zodra de nieuwe versie wordt gepubliceerd, op de volgende API vraag, zal een nieuwe berichtuitvoering worden geproduceerd. Het volgende binnenkomende profiel zal de nieuwe versie ontvangen.

<!--For batch messages, the audience/segment being processed in the previous execution will not be affected by the new version. Only the next incoming API call with an audience/segment will generate a new message execution with the new version. -->
