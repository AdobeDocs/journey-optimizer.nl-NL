---
title: Een bericht publiceren en wijzigen
description: Leer hoe u uw berichten publiceert en bijwerkt
snippet: y
feature: Journeys
topic: Contentmanagement
role: User
level: Intermediate
source-git-commit: 7eceb7292c127c1b16a564fc19d0fc091808ee35
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 4%

---

# Uw berichten {#publish-manage-messages} publiceren

## Een bericht {#publish-message} publiceren

Zodra uw bericht is gecreeerd, kunt u het publiceren om het voor uitvoering ter beschikking te stellen.

>[!CAUTION]
>
>Controleer en los waarschuwingen op voordat u ze publiceert. [Meer informatie](alerts.md).

![](assets/publish-message.png)

Zodra uw bericht wordt gepubliceerd, wordt het toegevoegd aan de berichtlijst met de status **[!UICONTROL Published]**.

Het is nu klaar om door één of meerdere [reizen](building-journeys/journey.md) teweeggebracht te worden.

## Een alleen-lezen bericht {#modify-message} bijwerken

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
