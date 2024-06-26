---
solution: Journey Optimizer
product: journey optimizer
title: Inhoudssjablonen testen
description: Leer hoe u de rendering van sommige sjablonen voor e-mailinhoud kunt testen
feature: Templates
topic: Content Management
role: User
level: Beginner
source-git-commit: 59c675dd2ac94b6967cfb3a93f74b2016a090190
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# Sjablonen voor e-mailinhoud testen {#test-template}

U kunt de rendering van sommige van uw e-mailsjablonen testen, ongeacht of deze zijn gemaakt op basis van een blanco sjabloon of op basis van een bestaande inhoud. Volg de onderstaande stappen om dit te doen.

1. Open de lijst met inhoudssjablonen via **[!UICONTROL Content Management]** > **[!UICONTROL Content Templates]** en selecteer een e-mailsjabloon.

1. Klikken **[!UICONTROL Edit content]** van de **[!UICONTROL Template properties]**.

1. Klikken **[!UICONTROL Simulate Content]** en selecteer een testprofiel om de rendering te controleren. [Meer informatie](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

1. U kunt een bewijs verzenden om uw inhoud te testen en het door sommige interne gebruikers te laten goedkeuren alvorens het in een reis of een campagne te gebruiken.

   * Klik hiertoe op de knop **[!UICONTROL Send proof]** en voert u de in [deze sectie](../content-management/proofs.md).

   * Voordat u de proefdruk verzendt, moet u de optie [e-mailoppervlak](../configuration/channel-surfaces.md) die wordt gebruikt om uw inhoud te testen.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Het bijhouden van wijzigingen wordt momenteel niet ondersteund bij het testen van sjablonen voor e-mailinhoud. Dit houdt in dat volggebeurtenissen, UTM-parameters en landingspagina-koppelingen niet effectief zijn in de proefdrukken die vanuit een sjabloon worden verzonden. Om het volgen te testen, [de inhoudssjabloon gebruiken](../email/use-email-templates.md) in een e-mail en [een bewijs verzenden](../content-management/preview-test.md#send-proofs).
