---
title: Een bericht toevoegen in een journey
description: Een bericht toevoegen in een journey
feature: Journeys
topic: Contentmanagement
role: User
level: Intermediate
source-git-commit: 7937c3b7c9247868a7a506991850537493a76cf1
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 10%

---

# Een bericht toevoegen in een journey

[!DNL Journey Optimizer] berichtmogelijkheden zijn ingebouwd. U hoeft alleen uw inhoud te ontwerpen en uw bericht te publiceren. Zie [deze sectie](../get-started-content.md). Vervolgens voegt u eenvoudig een push- of e-mailbericht toe dat is ontworpen met Journey Optimizer.

Als u een systeem van derden gebruikt om uw berichten te verzenden, kunt u een douaneactie tot stand brengen. Meer informatie vindt u in deze [sectie](../action/action.md).

## Berichtactiviteit toevoegen

1. Zoals altijd, begin uw reis met een gebeurtenis of een **Read Segment** activiteit.

   ![](../assets/jo-message0.png)

1. Sleep in de sectie **Handelingen** van het palet een **Bericht**-activiteit naar het canvas.

   ![](../assets/jo-message1.png)

1. Voeg een label en beschrijving toe.

   ![](../assets/jo-message2.png)

1. Klik in het veld **Bericht**. De lijst met beschikbare berichten die in Journey Optimizer zijn ontworpen, wordt weergegeven. U kunt de lijst filteren op status.

   ![](../assets/jo-message3.png)

1. Kies een bericht en klik **Select**. U kunt een nieuw bericht direct van dit scherm tot stand brengen door **Create bericht** te klikken.

   ![](../assets/jo-message4-ter.png)

   Als u uw bericht wilt controleren, kunt u **Open het bericht** pictogram in het **Bericht** gebied klikken. Het bericht wordt geopend op een nieuw tabblad.

   ![](../assets/jo-message4-bis.png)

1. Voeg de volgende stappen aan uw reis toe.

## E-mailparameters en push-parameters

In de secties **[!UICONTROL Email parameters]** en **[!UICONTROL Push parameters]** worden alleen-lezen velden weergegeven. U voert typisch deze configuratie uit wanneer het creëren van het bericht. Zie [deze sectie](../get-started-content.md).

![](../assets/jo-message4.png)

Als u een specifieke waarde wilt forceren, kunt u het pictogram **Inschakelen van parameteroverschrijving** rechts van het veld gebruiken. Deze optie kan nuttig zijn voor testdoeleinden. Voor een e-mailbericht kunt u bijvoorbeeld uw e-mailadres toevoegen. Nadat u de reis hebt gepubliceerd, wordt het e-mailbericht naar u verzonden.
