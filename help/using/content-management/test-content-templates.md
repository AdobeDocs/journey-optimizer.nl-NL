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
source-git-commit: 22a8742bf9000ed1cc8437d7ac89747276284dbf
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# Sjablonen voor e-mailinhoud testen {#test-template}

U kunt de rendering van sommige van uw e-mailsjablonen testen, ongeacht of deze zijn gemaakt op basis van een blanco sjabloon of op basis van een bestaande inhoud. Volg de onderstaande stappen om dit te doen.

1. Open de lijst met inhoudssjablonen via het menu **[!UICONTROL Content Management]** > **[!UICONTROL Content Templates]** en selecteer een e-mailsjabloon.

1. Klik **[!UICONTROL Edit content]** van **[!UICONTROL Template properties]**.

1. Klik op **[!UICONTROL Simulate Content]** en selecteer een testprofiel om de rendering te controleren. [Meer informatie](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

   >[!NOTE]
   >
   >Met [!DNL Journey optimizer] kunt u ook verschillende varianten van uw inhoudssjablonen testen door deze te bekijken en proefdrukken te verzenden met behulp van voorbeeldinvoergegevens die vanuit een CSV-/JSON-bestand zijn geüpload of handmatig zijn toegevoegd. [ leer hoe te om inhoudvariaties ](../test-approve/simulate-sample-input.md) te simuleren

1. U kunt een bewijs verzenden om uw inhoud te testen en het door sommige interne gebruikers te laten goedkeuren alvorens het in een reis of een campagne te gebruiken.

   * Om dit te doen, klik de **[!UICONTROL Send proof]** knoop en volg de stappen die in [ worden beschreven deze sectie ](../content-management/proofs.md).

   * Alvorens de proef te verzenden, moet u de [ e-mailconfiguratie ](../configuration/channel-surfaces.md) selecteren die zal worden gebruikt om uw inhoud te testen.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Het bijhouden van wijzigingen wordt momenteel niet ondersteund bij het testen van sjablonen voor e-mailinhoud. Dit houdt in dat volggebeurtenissen, UTM-parameters en landingspagina-koppelingen niet effectief zijn in de proefdrukken die vanuit een sjabloon worden verzonden. Om het volgen te testen, [ gebruik het inhoudsmalplaatje ](../email/use-email-templates.md) in e-mail en verzend een proef gebruikend testprofielen, of steekproefinputgegevens die van een CSV/JSON- dossier worden geupload, of manueel worden toegevoegd. [ Leer hoe te voorproef en uw inhoud te testen ](../content-management/preview-test.md)
