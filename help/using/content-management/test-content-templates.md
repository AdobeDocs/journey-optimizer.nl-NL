---
solution: Journey Optimizer
product: journey optimizer
title: Inhoudssjablonen testen
description: Leer hoe u de rendering van sommige sjablonen voor e-mailinhoud kunt testen
feature: Templates
topic: Content Management
role: User
level: Beginner
exl-id: 01726ab6-f581-4d19-aedd-2541bc0f27c6
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# Sjablonen voor e-mailinhoud testen {#test-template}

U kunt de rendering van sommige van uw e-mailsjablonen testen, ongeacht of deze zijn gemaakt op basis van een blanco sjabloon of op basis van een bestaande inhoud. Volg de onderstaande stappen om dit te doen.

1. Open de lijst met inhoudssjablonen via het menu **[!UICONTROL Content Management]** > **[!UICONTROL Content Templates]** en selecteer een e-mailsjabloon.

1. Klik **[!UICONTROL Edit content]** van **[!UICONTROL Template properties]**.

1. Klik op **[!UICONTROL Simulate Content]** en selecteer een testprofiel om de rendering te controleren. [Meer informatie](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

1. U kunt een bewijs verzenden om uw inhoud te testen en het door sommige interne gebruikers te laten goedkeuren alvorens het in een reis of een campagne te gebruiken.

   * Om dit te doen, klik de **[!UICONTROL Send proof]** knoop en volg de stappen die in [ worden beschreven deze sectie ](../content-management/proofs.md).

   * Alvorens de proef te verzenden, moet u de [ e-mailconfiguratie ](../configuration/channel-surfaces.md) selecteren die zal worden gebruikt om uw inhoud te testen.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Het bijhouden van wijzigingen wordt momenteel niet ondersteund bij het testen van sjablonen voor e-mailinhoud. Dit houdt in dat volggebeurtenissen, UTM-parameters en landingspagina-koppelingen niet effectief zijn in de proefdrukken die vanuit een sjabloon worden verzonden. Om het volgen te testen, [ gebruik het inhoudsmalplaatje ](../email/use-email-templates.md) in e-mail en [ verzend een proef ](../content-management/preview-test.md#send-proofs).
