---
solution: Journey Optimizer
product: journey optimizer
title: Gebruiksgevallen van landingspagina
description: Ontdek de meest gebruikelijke gebruiksgevallen bij bestemmingspagina's in Journey Optimizer
feature: Landing Pages, Subscriptions
topic: Content Management
role: User
level: Intermediate
keywords: landen, landingspagina, hoofdletter gebruiken
exl-id: 8c00d783-54a3-45d9-bd8f-4dc58804d922
source-git-commit: 4de37520b3ea7842d7f385f38c07cdf4984a5939
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 1%

---

# Gebruiksgevallen van landingspagina {#lp-use-cases}

Hieronder ziet u enkele voorbeelden van het gebruik van [!DNL Journey Optimizer] het landen van pagina&#39;s om uw klanten te hebben binnen of uit van het ontvangen van wat of elk van uw mededelingen kiezen.

## Abonneren op een service {#subscription-to-a-service}

Een van de meest gebruikelijke gebruiksgevallen is het uitnodigen van uw klanten om [abonneren op een service](subscription-list.md) (zoals een nieuwsbrief of een gebeurtenis) door een landingspagina. De belangrijkste stappen worden weergegeven in de onderstaande grafiek:

![](assets/lp_subscription-uc.png)

Stel bijvoorbeeld dat u volgende maand een gebeurtenis organiseert en een registratiecampagne voor een gebeurtenis wilt starten<!--to keep your customers that are interested updated on that event-->. Hiervoor stuurt u een e-mail met een koppeling naar een bestemmingspagina waarmee uw ontvangers zich kunnen registreren voor deze gebeurtenis. De gebruikers die zich registreren, worden toegevoegd aan de abonnementenlijst die u voor dit doel hebt gemaakt.

### Een openingspagina instellen {#set-up-lp}

1. Maak de abonnementenlijst van de gebeurtenisregistratie, waarin de geregistreerde gebruikers worden opgeslagen. Leer hoe u een abonnementenlijst maakt [hier](subscription-list.md#define-subscription-list).

   ![](assets/lp_subscription-uc-list.png)

1. [Een openingspagina maken](create-lp.md) om uw ontvangers in staat te stellen zich voor uw gebeurtenis te registreren.

   ![](assets/lp_create-lp-details.png)

1. De registratie configureren [primaire landingspagina](create-lp.md#configure-primary-page).

1. Bij het ontwerpen van de [pagina-inhoud plaatsen](design-lp.md), selecteert u de abonnementenlijst die u hebt gemaakt om deze bij te werken met de profielen die het selectievakje voor registratie inschakelen.

   ![](assets/lp_subscription-uc-lp-list.png)

1. Maak een pagina &#39;Bedankt&#39; die aan de ontvangers wordt weergegeven wanneer ze het registratieformulier verzenden. Leer hoe u landingssubpagina&#39;s kunt configureren [hier](create-lp.md#configure-subpages).

   ![](assets/lp_subscription-uc-thanks.png)

1. [Publiceren](create-lp.md#publish) de openingspagina.

1. In een [reis](../building-journeys/journey.md), voegt u een **E-mail** activiteit om verkeer naar de registratie landingspagina te drijven.

   ![](assets/lp_subscription-uc-journey.png)

1. [De e-mail ontwerpen](../email/get-started-email-design.md) om aan te geven dat de registratie nu geopend is voor uw gebeurtenis.

1. [Een koppeling invoegen](../email/message-tracking.md#insert-links) in uw berichtinhoud. Selecteren **[!UICONTROL Landing page]** als de **[!UICONTROL Link type]** en kiest u [landingspagina](create-lp.md#configure-primary-page) die u voor registratie hebt gemaakt.

   ![](assets/lp_subscription-uc-link.png)

   >[!NOTE]
   >
   >Om uw bericht te kunnen verzenden, zorg ervoor de het landen pagina u selecteert nog niet verlopen is. Leer hoe u de vervaldatum kunt bijwerken [in deze sectie](create-lp.md#configure-primary-page).

   Als de ontvangers eenmaal een e-mail hebben ontvangen en op de koppeling naar de bestemmingspagina klikken, worden ze doorgestuurd naar de pagina &#39;Bedankt&#39; en worden ze toegevoegd aan de abonnementenlijst.

### Een bevestigingsbericht verzenden {#send-confirmation-email}

Bovendien kunt u een bevestigingsbericht verzenden naar de ontvangers die zich hebben geregistreerd voor uw gebeurtenis. Volg de onderstaande stappen om dit te doen.

1. Een andere maken [reis](../building-journeys/journey.md). U kunt dit rechtstreeks vanaf de bestemmingspagina doen door op de knop **[!UICONTROL Create journey]** knop. [Meer informatie](create-lp.md#configure-primary-page)

   ![](assets/lp_subscription-uc-create-journey.png)

1. Ontvouw de **[!UICONTROL Events]** categorie en zet een **[!UICONTROL Audience Qualification]** op uw canvas. [Meer informatie](../building-journeys/audience-qualification-events.md)

1. Klik in het dialoogvenster **[!UICONTROL Audience]** en selecteer de abonnementenlijst die u hebt gemaakt.

   ![](assets/lp_subscription-uc-confirm-journey.png)

1. Voeg een bevestigingsbericht van uw keuze toe en verzend het door de reis.

   ![](assets/lp_subscription-uc-confirm-email.png)

Alle gebruikers die zich voor uw gebeurtenis hebben geregistreerd, ontvangen het bevestigingsbericht.

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## Openingspagina voor landen {#opt-out}

Om uw ontvangers in staat te stellen zich af te melden voor uw communicatie, kunt u een koppeling naar een bestemmingspagina opnemen in uw e-mails.

>[!NOTE]
>
>Meer informatie over het beheren van de toestemming van uw ontvangers en waarom dit belangrijk is in [deze sectie](../privacy/opt-out.md).

### Uitschakelen, beheer {#opt-out-management}

Het is een wettelijke vereiste dat ontvangers de mogelijkheid krijgen om zich niet meer te abonneren op het ontvangen van communicatie van een merk. Meer informatie over de toepasselijke wetgeving vindt u in het [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target="_blank"}.

Daarom moet u altijd een **afmelden, koppeling** in elke e-mail die naar ontvangers wordt verzonden:

* Nadat u op deze koppeling hebt geklikt, worden de ontvangers naar een bestemmingspagina geleid, inclusief een knop om te bevestigen dat ze het programma willen afsluiten.
* Als u op de knop Weigeren klikt, worden de profielgegevens bijgewerkt met deze informatie.

### Optie om e-mail te weigeren configureren {#configure-opt-out}

Volg onderstaande stappen om de ontvangers van een e-mail in staat te stellen zich af te melden voor uw communicatie via een bestemmingspagina:

1. Maak uw openingspagina. [Meer informatie](create-lp.md)

1. Definieer de primaire pagina. [Meer informatie](create-lp.md#configure-primary-page)

1. [Ontwerp](design-lp.md) de inhoud van de primaire pagina: de specifieke landingspagina gebruiken **[!UICONTROL Form]** component, een component definiëren **[!UICONTROL Opt-out]** selectievakje en kies voor bijwerken **[!UICONTROL Channel (email)]**: het profiel dat het selectievakje Weigeren inschakelt op de bestemmingspagina wordt uitgeschakeld voor alle communicatie.

   ![](assets/lp_opt-out-primary-lp.png)

   <!--You can also build your own landing page and host it on the third-party system of your choice.-->

1. Een bevestiging toevoegen [subpagina](create-lp.md#configure-subpages) die wordt weergegeven aan de gebruikers die het formulier verzenden.

   ![](assets/lp_opt-out-subpage.png)

   >[!NOTE]
   >
   >Zorg ervoor dat u naar de subpagina in de primaire pagina&#39;s verwijst **[!UICONTROL Call to action]** van de **[!UICONTROL Form]** component. [Meer informatie](design-lp.md)

1. Zodra u vormde en de inhoud van uw pagina&#39;s bepaalde, [publish](create-lp.md#publish) de openingspagina.

1. [Een e-mailbericht maken](../email/get-started-email-design.md) tijdens een reis.

1. Selecteer tekst in uw inhoud en [een koppeling invoegen](../email/message-tracking.md#insert-links) gebruiken van de contextafhankelijke werkbalk. U kunt ook een koppeling op een knop gebruiken.

1. Selecteren **[!UICONTROL Landing page]** van de **[!UICONTROL Link type]** vervolgkeuzelijst en selecteert u de [landingspagina](create-lp.md#configure-primary-page) die u hebt gemaakt voor het uitschakelen.

   ![](assets/lp_opt-out-landing-page.png)

   >[!NOTE]
   >
   >Om uw bericht te kunnen verzenden, zorg ervoor de het landen pagina u selecteert nog niet verlopen is. Leer hoe u de vervaldatum kunt bijwerken [in deze sectie](create-lp.md#configure-primary-page).

1. Publish en voer de reis. [Meer informatie](../building-journeys/journey.md).

1. Als een ontvanger op de koppeling voor het opzeggen van het abonnement in de e-mail klikt nadat het bericht is ontvangen, wordt de bestemmingspagina weergegeven.

   ![](assets/lp_opt-out-submit-form.png)

   Indien de ontvanger het vakje aankruist en het formulier verzendt:

   * De ontvanger van het gekozen-uit wordt opnieuw gericht aan het scherm van het bevestigingsbericht.

   * De profielgegevens worden bijgewerkt en zullen geen mededelingen van uw merk tenzij opnieuw geabonneerd ontvangen.

Als u wilt controleren of de keuze van het corresponderende profiel is bijgewerkt, gaat u naar het Experience Platform en opent u het profiel door een naamruimte voor identiteiten en een bijbehorende identiteitswaarde te selecteren. Meer informatie in het dialoogvenster [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target="_blank"}.

![](assets/lp_opt-out-profile-choice.png)

In de **[!UICONTROL Attributes]** kunt u zien dat de waarde voor **[!UICONTROL choice]** is gewijzigd in **[!UICONTROL no]**.

De gegevens over de opt-out worden opgeslagen in de **Dataset voor goedgekeurde service**. [Meer informatie over gegevenssets](../data/get-started-datasets.md)

>[!NOTE]
>
>Als de samenvoegmethode voor uw standaard [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target="_blank"} **[!UICONTROL Profiles]** samenvoegbeleid is **[!UICONTROL Dataset Precedence]**, zorgt u ervoor dat de **[!UICONTROL AJO Consent Service Dataset]** en om aan het in het fusiebeleid voorrang te geven. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#dataset-precedence-profile){target="_blank"}
>
>Zelfs als er geen batches aan deze gegevensset zijn toegevoegd, zal deze nog steeds de informatie over opt-in/opt-out bevatten.



**Zie ook:**

* [Eén klik op Weigeren](../email/email-opt-out.md#one-click-opt-out-link)
* [Koppeling Weigeren in koptekst van e-mail](../email/email-opt-out.md#unsubscribe-header)

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../privacy/opt-out.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../privacy/opt-out.md#unsubscribe-header)

////////


## Leverage landing page submission event {#leverage-lp-event}

You can use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.

To do this, you need to create an event containing the landing page submission information and use it in a journey. Follow the steps below.

1. Go to **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**, and in the **[!UICONTROL Events]** section, select **[!UICONTROL Manage]**.

    ![](assets/lp_subscription-uc-configurations.png)

1. The list of events displays. Select **[!UICONTROL Create Event]**.

    ![](assets/lp_subscription-uc-create-event.png)

1. The event configuration pane opens on the right side of the screen. Configure a rule-based unitary event. [Learn more](../event/about-creating.md)

1. Define the schema: select **[!UICONTROL AJO Email Tracking Experience Event Schema v.1]** (available by default in [!DNL Journey Optimizer]).

    ![](assets/lp_subscription-uc-event-schema.png)

1. In the **[!UICONTROL Fields]** section, select the following elements:

    * **[!UICONTROL _experience]** > **[!UICONTROL customerJourneyManagement]** > **[!UICONTROL messageInteraction]** > **[!UICONTROL Interaction Type]**
    
    * **[!UICONTROL _experience]** > **[!UICONTROL customerJourneyManagement]** > **[!UICONTROL messageInteraction]** > **[!UICONTROL Landing Page Details]** > **[!UICONTROL Landing Page ID]**

    ![](assets/lp_subscription-uc-event-fields.png)

1. Click inside the **[!UICONTROL Event ID condition]** field. Using the simple personalization editor, define the condition for the **[!UICONTROL Interaction Type]** and **[!UICONTROL Landing Page ID]** fields. This will be used by the system to identify the events that will trigger your journey.

    ![](assets/lp_subscription-uc-event-id-condition.png)

    >[!NOTE]
    >
    >To find the landing page ID, you can insert the landing page as a link into an email and select the source code from the contextual toolbar to display the landing page information.
    >
    >![](assets/lp_subscription-uc-lp-id.png)

1. Save your changes.

1. Create a [journey](../building-journeys/journey.md). You can do it directly from the landing page by clicking the **[!UICONTROL Create journey]** button. Learn more [here](create-lp.md#configure-primary-page)

    ![](assets/lp_subscription-uc-event-create-journey.png)

1. In the journey, unfold the **[!UICONTROL Events]** category and drop the event that you created into the canvas. Learn more [here](../building-journeys/audience-qualification-events.md)

    ![](assets/lp_subscription-uc-journey-event.png)

1. Unfold the **[!UICONTROL Actions]** category and drop an email action into the canvas.

    ![](assets/lp_subscription-uc-journey-email.png)

///How do you use the information from the event to send an email to the users? -->
