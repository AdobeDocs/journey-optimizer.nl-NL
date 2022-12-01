---
solution: Journey Optimizer
product: journey optimizer
title: Een e-mail maken
description: Leer hoe u een e-mail maakt in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: b7b333e96e0f4b32a0f94c3f1e67f0f3d3fc2816
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 5%

---

# Een e-mail maken {#create-email-bis}

Voer de onderstaande stappen uit om een e-mail te maken.

## 1. Een e-mailbericht maken voor een reis of campagne

Een **[!UICONTROL Email]** actie ondernemen op een reis of een campagne, en de onderstaande stappen volgen op basis van uw zaak.

>[!BEGINTABS]

>[!TAB Een e-mail toevoegen aan een reis]

1. Open uw reis en sleep vervolgens een **[!UICONTROL Email]** van de **[!UICONTROL Actions]** in het palet.

1. Geef basisinformatie op over je bericht (label, beschrijving, categorie).

1. Kies de optie [e-mailoppervlak] te gebruiken.

   ![](assets/email_journey.png)

Voor meer informatie over hoe te om een reis te vormen, verwijs naar [deze pagina](../building-journeys/journey-gs.md).

>[!TAB Een e-mail toevoegen aan een campagne]

1. Maak een nieuwe geplande of door API geactiveerde campagne en selecteer **[!UICONTROL Email]** als uw handeling.

1. Kies de optie [e-mailoppervlak] te gebruiken.

   ![](assets/email_campaign.png)

1. Klik op **[!UICONTROL Create]**.

1. Voer de stappen uit om een e-mailcampagne te maken.

   ![](assets/email_campaign_steps.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->

Voor meer informatie over hoe te om een campagne te vormen, verwijs naar [deze pagina](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## Uw e-mailinhoud definiëren

1. Van het reis of scherm van de campagneconfiguratie, klik **[!UICONTROL Edit content]** om de e-mailinhoud te configureren. [Meer informatie]

   ![](assets/email_campaign_edit_content.png)

1. In de **[!UICONTROL Header]** van de **[!UICONTROL Edit content]** scherm, de **[!UICONTROL From name]**, **[!UICONTROL From email]** en **[!UICONTROL BCC]** Het veld komt van het e-mailoppervlak dat u hebt geselecteerd. [Meer informatie] <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. U kunt een onderwerpregel toevoegen. Typ onbewerkte tekst rechtstreeks in het desbetreffende veld of gebruik de optie [Expression-editor](../personalization/personalization-build-expressions.md) om uw onderwerpregel aan uw wensen aan te passen.

1. Klik op de knop **[!UICONTROL Edit email body]** om uw inhoud te gaan samenstellen met de [!DNL Journey Optimizer] E-mailontwerper. [Meer informatie]

   ![](assets/email_designer_edit_email_body.png)

   U kunt ook op de knop **[!UICONTROL Code Editor]** om uw eigen inhoud in gewone HTML te coderen gebruikend het pop-up venster dat toont.

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >Als u al inhoud hebt gemaakt of geïmporteerd via de e-mailontwerper, wordt deze inhoud weergegeven in HTML.

## Een voorvertoning van uw e-mail bekijken

Nadat de inhoud van uw bericht is gedefinieerd, kunt u deze voorvertonen om de weergave van uw e-mail te bepalen en de instellingen voor de personalisatie te controleren met testprofielen. [Meer informatie]

![](assets/email_designer_edit_simulate.png)

U moet ook waarschuwingen controleren in het bovenste gedeelte van de editor.  Sommige zijn eenvoudige waarschuwingen, maar andere kunnen voorkomen dat u het bericht gebruikt. [Meer informatie](alerts.md).

## Uw e-mailinhoud valideren

Wanneer uw e-mail klaar is, voltooi de configuratie van uw [reis](../building-journeys/journey-gs.md) of [campagne](../campaigns/create-campaign.md) en activeren om het bericht te verzenden.

>[!NOTE]
>
>Om het gedrag van uw ontvangers door e-mailopeningen en/of interactie te volgen, zorg ervoor dat de specifieke opties in **[!UICONTROL Tracking]** het gedeelte van de reis [e-mailactiviteit](../building-journeys/journeys-message.md) of in de e-mail [campagne](../campaigns/create-campaign.md).

U moet ook waarschuwingen controleren in het bovenste gedeelte van de editor.  Sommige zijn eenvoudige waarschuwingen, maar andere kunnen voorkomen dat u het bericht gebruikt. [Meer informatie](alerts.md)

