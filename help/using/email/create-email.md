---
solution: Journey Optimizer
product: journey optimizer
title: Een e-mail maken
description: Leer hoe u een e-mail maakt in Journey Optimizer
feature: Email
topic: Content Management
role: User
level: Beginner
keywords: maken, e-mail, starten, reizen, campagne
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 2%

---

# Een e-mail maken {#create-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="E-mailontwerp"
>abstract="Definieer de onderwerpregel van uw e-mail en open de e-mailtoepassing Designer om de inhoud van de e-mail te maken."


## Een e-mailactie toevoegen {#email-action}

Een e-mail maken in [!DNL Journey Optimizer], voegt u een **[!UICONTROL Email]** actie op een reis of een campagne. Volg vervolgens de onderstaande stappen, afhankelijk van uw zaak.

>[!BEGINTABS]

>[!TAB Een e-mail toevoegen aan een reis]

1. Open uw reis en sleep vervolgens een **[!UICONTROL Email]** van de **[!UICONTROL Actions]** in het palet.

1. Geef basisinformatie op over je bericht (label, beschrijving, categorie).

1. Kies de optie [e-mailoppervlak](email-settings.md) te gebruiken.

   ![](assets/email_journey.png)

   Het veld wordt standaard voorgevuld met het laatste oppervlak dat door de gebruiker voor dat kanaal wordt gebruikt.

>[!NOTE]
>
>Met de optie Send-Time optimalisatie kunt u het beste tijdstip voorspellen waarop u het bericht wilt verzenden om de betrokkenheid te maximaliseren op basis van de historisch geopende bestanden en klikt u op percentages. [Leer hoe u met SendTime Optimization werkt](../building-journeys/journeys-message.md#send-time-optimization)

Voor meer informatie over hoe te om een reis te vormen, raadpleeg [deze pagina](../building-journeys/journey-gs.md).

>[!TAB Een e-mail toevoegen aan een campagne]

1. Maak een nieuwe geplande of door API geactiveerde campagne en selecteer **[!UICONTROL Email]** als uw handeling.

1. Kies de optie [e-mailoppervlak](email-settings.md) te gebruiken.

   ![](assets/email_campaign.png)

1. Klik op **[!UICONTROL Create]**.

1. Voer de stappen uit om een e-mailcampagne te maken, zoals de eigenschappen van de campagne, [publiek](../audience/about-audiences.md), en [schema](../campaigns/create-campaign.md#schedule).

   ![](assets/email_campaign_steps.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->

Voor meer informatie over hoe te om een campagne te vormen, raadpleeg [deze pagina](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## Uw e-mailinhoud definiëren {#define-email-content}

<!-- update the quarry component with right ID value-->

>[!CONTEXTUALHELP]
>id="test_id"
>title="E-mailinhoud configureren"
>abstract="Maak de inhoud van uw e-mail. Definieer het onderwerp en gebruik vervolgens de e-mailtoepassing van de Designer om de tekst van de e-mail te maken en aan te passen."

1. Van het reis of scherm van de campagneconfiguratie, klik **[!UICONTROL Edit content]** om de e-mailinhoud te configureren. [Meer informatie](get-started-email-design.md)

   ![](assets/email_campaign_edit_content.png)

   In de **[!UICONTROL Header]** van de **[!UICONTROL Edit content]** scherm, de **[!UICONTROL From name]**, **[!UICONTROL From email]** en **[!UICONTROL BCC]** worden geconfigureerd in het e-mailoppervlak dat u hebt geselecteerd. [Meer informatie](email-settings.md) <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. Voeg een onderwerpregel voor uw bericht toe. Om de onderwerpregel met de verpersoonlijkingsredacteur te vormen en te personaliseren, klik **[!UICONTROL Open personalization dialog]** pictogram. [Meer informatie](../personalization/personalization-build-expressions.md)

1. Klik op de knop **[!UICONTROL Edit email body]** om toegang te krijgen tot e-mail Designer en uw inhoud te gaan samenstellen. [Meer informatie](get-started-email-design.md)

   ![](assets/email_designer_edit_email_body.png)

1. Als u in een campagne werkt, kunt u ook op de knop **[!UICONTROL Code Editor]** om uw eigen inhoud in gewone HTML te coderen gebruikend het pop-up venster dat toont.

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >Als u al inhoud hebt gemaakt of geïmporteerd via de e-mail-Designer, wordt deze inhoud weergegeven in HTML.

## Waarschuwingen controleren {#check-email-alerts}

Terwijl u berichten ontwerpt, worden waarschuwingen weergegeven in de interface (rechtsboven op het scherm) wanneer er geen toetseninstellingen aanwezig zijn.

![](assets/email_journey_alerts_details.png)

>[!NOTE]
>
>Als deze knop niet wordt weergegeven, is er geen melding gevonden.

De instellingen en elementen die door het systeem zijn gecontroleerd, worden hieronder weergegeven. U zult ook informatie over hoe te om uw configuratie aan te passen om de overeenkomstige kwesties op te lossen vinden.

Er kunnen twee typen waarschuwingen optreden:

* **Waarschuwingen** verwijzen naar aanbevelingen en beste praktijken, zoals:

   * **[!UICONTROL The opt-out link is not present in the email body]**: het toevoegen van een koppeling om uw abonnement op te zeggen aan uw e-mailadres is een aanbevolen werkwijze. Leer hoe u deze kunt configureren in [deze sectie](../privacy/opt-out.md#opt-out-management).

     >[!NOTE]
     >
     >E-mailberichten van het type Marketing moeten een opt-out-koppeling bevatten, die niet vereist is voor transactiemeldingen. De berichtcategorie (**[!UICONTROL Marketing]** of **[!UICONTROL Transactional]**) wordt gedefinieerd op de [kanaaloppervlak](email-settings.md#email-type) niveau en wanneer [het bericht maken](#create-email-journey-campaign) van een reis of een campagne.

   * **[!UICONTROL Text version of HTML is empty]**: vergeet niet om een tekstversie van uw e-mailhoofdtekst te definiëren, omdat deze wordt gebruikt wanneer HTML-inhoud niet kan worden weergegeven. Leer hoe u de tekstversie maakt in [deze sectie](text-version-email.md).

   * **[!UICONTROL Empty link is present in email body]**: controleer of alle koppelingen in uw e-mail correct zijn. Leer hoe u inhoud en koppelingen kunt beheren in [deze sectie](content-from-scratch.md).

   * **[!UICONTROL Email size has exceeded the limit of 100KB]**: voor optimale aflevering moet u ervoor zorgen dat de e-mailgrootte niet groter is dan 100 kB. Leer hoe u e-mailinhoud kunt bewerken in [deze sectie](content-from-scratch.md).

* **Fouten** voorkomen dat u de reis/campagne test of activeert zolang deze niet is opgelost, zoals:

   * **[!UICONTROL The subject line is missing]**: E-mailonderwerpregel is verplicht. Leer hoe u het kunt definiëren en personaliseren in [deze sectie](create-email.md).

  <!--HTML is empty when Amp HTML is present-->

   * **[!UICONTROL The email version of the message is empty]**: deze fout wordt weergegeven wanneer de e-mailinhoud niet is geconfigureerd. Leer hoe u e-mailinhoud ontwerpt in [deze sectie](get-started-email-design.md).

   * **[!UICONTROL Surface doesn't exist]**: u kunt uw bericht niet gebruiken als het geselecteerde oppervlak wordt verwijderd na het maken van het bericht. Als deze fout optreedt, selecteert u een ander oppervlak in het bericht **[!UICONTROL Properties]**. Meer informatie over kanaaloppervlakken in [deze sectie](../configuration/channel-surfaces.md).

>[!CAUTION]
>
>Als u de reis/campagne wilt testen of activeren via e-mail, moet u alle **fout** waarschuwingen.

## Uw e-mail controleren en verzenden

Zodra de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om een voorvertoning ervan weer te geven, proefdrukken te verzenden en de rendering ervan in populaire desktops, mobiele en webclients te beheren. Als u gepersonaliseerde inhoud hebt ingevoegd, kunt u met behulp van testprofielgegevens controleren hoe deze inhoud in het bericht wordt weergegeven.

Om dit te doen, klik **[!UICONTROL Simulate content]** Voeg vervolgens een testprofiel toe om uw bericht te controleren met behulp van de gegevens van het testprofiel.

![](assets/email_designer_edit_simulate.png)

Gedetailleerde informatie over het selecteren van testprofielen en het weergeven van een voorvertoning van de inhoud is beschikbaar in het dialoogvenster [Inhoud beheren](../content-management/preview-test.md) sectie.

Wanneer uw e-mail klaar is, voltooi de configuratie van uw [reis](../building-journeys/journey-gs.md) of [campagne](../campaigns/create-campaign.md)en activeer deze om het bericht te verzenden.

>[!NOTE]
>
>Om het gedrag van uw ontvangers door e-mailopeningen en/of interactie te volgen, zorg ervoor dat de specifieke opties in **[!UICONTROL Tracking]** het gedeelte van de reis [e-mailactiviteit](../building-journeys/journeys-message.md) of in de e-mail [campagne](../campaigns/create-campaign.md).<!--to move?-->

<!--

## Define your email content {#email-content}

Use [!DNL Journey Optimizer] Email Designer to [design your email from scratch](../email/content-from-scratch.md). If you have an existing content, you can [import it in the Email Designer](../email/existing-content.md), or [code your own content](../email/code-content.md) in [!DNL Journey Optimizer]. 

[!DNL Journey Optimizer] comes with a set of [built-in templates](email-templates.md) to help you start. Any email can also be saved as a template.

Use [!DNL Journey Optimizer] personalization editor to personalize your messages with profiles' data. For more on personalization, refer to [this section](../personalization/personalize.md).

Adapt the content of your messages to the targeted profiles by using [!DNL Journey Optimizer] dynamic content capabilities. [Get started with dynamic content](../personalization/get-started-dynamic-content.md)

## Email tracking {#email-tracking}

If you want to track the behavior of your recipients through openings and/or clicks on links, enable the following options: **[!UICONTROL Email opens]** and **[!UICONTROL Click on email]**. 

Learn more about tracking in [this section](message-tracking.md).

## Validate your email content {#email-content-validate}

Control the rendering of your email, and check personalization settings with test profiles, using the preview section on the left-hand side. For more on this, refer to [this section](preview.md).

![](assets/messages-simple-preview.png)

You must also check alerts in the upper section of the editor.  Some of them are simple warnings, but others can prevent you from using the message. 

-->

