---
title: Landing page use cases
description: Ontdek de meest gebruikelijke gebruiksgevallen bij bestemmingspagina's in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
exl-id: 8c00d783-54a3-45d9-bd8f-4dc58804d922
source-git-commit: bbc2adabac63ffb813ea2630f29aec552fc3f4df
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 1%

---

# Gebruiksgevallen van landingspagina {#lp-use-cases}

Below are some examples of how you can use [!DNL Journey Optimizer] landing pages to have your customers opt in/out from receiving some or all of your communications.

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## Abonnement op een service {#subscription-to-a-service}

One of the most common use cases consists in inviting your customers to [subscribe to a service](subscription-list.md) (such as a newsletter or an event) through a landing page. De belangrijkste stappen worden weergegeven in de onderstaande grafiek:

![](../assets/lp_subscription-uc.png)

For example, let&#39;s say you organize an event next month and you want to launch an event registration campaign<!--to keep your customers that are interested updated on that event-->. Hiervoor stuurt u een e-mail met een koppeling naar een bestemmingspagina waarmee uw ontvangers zich kunnen registreren voor deze gebeurtenis. De gebruikers die zich registreren, worden toegevoegd aan de abonnementenlijst die u voor dit doel hebt gemaakt.

### Startpagina instellen

1. Maak de abonnementenlijst van de gebeurtenisregistratie, waarin de geregistreerde gebruikers worden opgeslagen. Leer hoe u een abonnementenlijst maakt [hier](subscription-list.md#define-subscription-list).

   ![](../assets/lp_subscription-uc-list.png)

1. [Een openingspagina maken](create-lp.md) om uw ontvangers in staat te stellen zich voor uw gebeurtenis te registreren.

1. De registratie configureren [primaire landingspagina](create-lp.md#configure-primary-page).

1. Bij het ontwerpen van de [pagina-inhoud plaatsen](design-lp.md), selecteert u de abonnementenlijst die u hebt gemaakt om deze bij te werken met de profielen die het selectievakje voor registratie inschakelen.

   ![](../assets/lp_subscription-uc-lp-list.png)

1. Maak een pagina &#39;Bedankt&#39; die aan de ontvangers wordt weergegeven wanneer ze het registratieformulier verzenden. Leer hoe u landingssubpagina&#39;s kunt configureren [hier](create-lp.md#configure-subpages).

   ![](../assets/lp_subscription-uc-thanks.png)

1. [Publiceren](create-lp.md#publish) de openingspagina.

1. [Een e-mailbericht maken](../create-message.md) om aan te geven dat de registratie nu geopend is voor uw gebeurtenis.

1. [Een koppeling invoegen](../message-tracking.md#insert-links) in uw berichtinhoud. Selecteren **[!UICONTROL Landing page]** als de **[!UICONTROL Link type]** en kiest u [landingspagina](create-lp.md#configure-primary-page) die u voor registratie hebt gemaakt.

   ![](../assets/lp_subscription-uc-link.png)

1. Sla uw inhoud op en [uw bericht publiceren](../publish-manage-message.md).

1. Uw bericht verzenden via een [reis](../building-journeys/journey.md) om het verkeer naar de registratiepagina van de landing te leiden.

   ![](../assets/lp_subscription-uc-journey.png)

   Als de ontvangers eenmaal een e-mail hebben ontvangen en op de koppeling naar de bestemmingspagina klikken, worden ze doorgestuurd naar de pagina &#39;Bedankt&#39; en worden ze toegevoegd aan de abonnementenlijst.

### Een bevestigingsbericht verzenden {#send-confirmation-email}

Bovendien kunt u een bevestigingsbericht verzenden naar de ontvangers die zich hebben geregistreerd voor uw gebeurtenis. Hiervoor voert u de volgende stappen uit.

1. Create another [journey](../building-journeys/journey.md). U kunt dit rechtstreeks vanaf de bestemmingspagina doen door op de knop **[!UICONTROL Create journey]** knop. Learn more [here](create-lp.md#configure-primary-page)

   ![](../assets/lp_subscription-uc-create-journey.png)

1. Unfold the **[!UICONTROL Events]** category and drop a **[!UICONTROL Segment Qualification]** activity into your canvas. Meer informatie [hier](../building-journeys/segment-qualification-events.md)

1. Click in the **[!UICONTROL Segment]** field and select the subscription list that you created.

   ![](../assets/lp_subscription-uc-confirm-journey.png)

1. Selecteer het bevestigingsbericht van uw keuze en verzend het door de reis.

   ![](../assets/lp_subscription-uc-confirm-email.png)

Alle gebruikers die zich voor uw gebeurtenis hebben geregistreerd, ontvangen het bevestigingsbericht.

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## Afmelden {#opt-out}

Om uw ontvangers in staat te stellen zich af te melden voor uw communicatie, kunt u een koppeling naar een bestemmingspagina opnemen in uw e-mails.

Meer informatie over het beheren van de toestemming van uw ontvangers en waarom dit belangrijk is in [deze sectie](../consent.md).

### Uitschakelen, beheer {#opt-out-management}

Het is een wettelijke vereiste dat ontvangers de mogelijkheid krijgen om zich af te melden voor het ontvangen van communicatie van een merk. Meer informatie over de toepasselijke wetgeving vindt u in het [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}.

Daarom moet u altijd een **afmelden, koppeling** in elke e-mail die naar ontvangers wordt verzonden:

* Nadat u op deze koppeling hebt geklikt, worden de ontvangers naar een bestemmingspagina geleid, inclusief een knop om te bevestigen dat ze het programma willen afsluiten.
* Als u op de knop Weigeren klikt, worden de profielgegevens bijgewerkt met deze informatie.

### Optie om te weigeren configureren {#configure-opt-out}

Volg onderstaande stappen om de ontvangers van een e-mail in staat te stellen zich af te melden voor uw communicatie via een bestemmingspagina.

1. Create your landing page. [Meer informatie](create-lp.md)

1. Definieer de primaire pagina. [Meer informatie](create-lp.md#configure-primary-page)

1. [Ontwerp](design-lp.md) de inhoud van de primaire pagina: de landingspagina-specifiek gebruiken **[!UICONTROL Form]** component, een component definiëren **[!UICONTROL Opt-out]** selectievakje en kies voor bijwerken **[!UICONTROL Channel (email)]**: Het profiel dat het vak Weigeren op de bestemmingspagina controleert, wordt uit al uw communicatie verwijderd.

   ![](../assets/lp_opt-out-primary-lp.png)

   <!--You can also build your own landing page and host it on the third-party system of your choice. To keep?-->

1. Een bevestiging toevoegen [subpagina](create-lp.md#configure-subpages) die wordt weergegeven aan de gebruikers die het formulier verzenden.

   ![](../assets/lp_opt-out-subpage.png)

   >[!NOTE]
   >
   >Zorg ervoor dat u naar de subpagina in de primaire pagina&#39;s verwijst **[!UICONTROL Call to action]** van de **[!UICONTROL Form]** component. [Meer informatie](design-lp.md)

1. Zodra u vormde en de inhoud van uw pagina&#39;s bepaalde, [publish](create-lp.md#publish) de openingspagina.

   ![](../assets/lp_opt-out-publish.png)

1. [Een e-mailbericht maken](../create-message.md) in [!DNL Journey Optimizer].

1. Selecteer tekst in uw inhoud en [een koppeling invoegen](../message-tracking.md#insert-links) gebruiken van de contextafhankelijke werkbalk. U kunt ook een koppeling op een knop gebruiken.

   ![](../assets/lp_opt-out-insert-link.png)

1. Selecteren **[!UICONTROL Landing page]** van de **[!UICONTROL Link type]** vervolgkeuzelijst en selecteert u de [landingspagina](create-lp.md#configure-primary-page) die u hebt gemaakt voor het uitschakelen.

   ![](../assets/lp_opt-out-landing-page.png)

1. Sla uw inhoud op en [uw bericht publiceren](../publish-manage-message.md).

1. Stuur je bericht door een reis. [Meer informatie](../building-journeys/journey.md).

1. Als een ontvanger op de koppeling voor het opzeggen van het abonnement in de e-mail klikt nadat het bericht is ontvangen, wordt de bestemmingspagina weergegeven.

   ![](../assets/lp_opt-out-submit-form.png)

   Indien de ontvanger het vakje aankruist en het formulier verzendt:

   * De ontvanger van het gekozen-uit wordt opnieuw gericht aan het scherm van het bevestigingsbericht.

   * De profielgegevens worden bijgewerkt en zullen geen mededelingen van uw merk tenzij opnieuw geabonneerd ontvangen.

To check that the corresponding profile&#39;s choice has been updated, go to Experience Platform and access the profile by selecting an identity namespace and a corresponding identity value. Meer informatie in het dialoogvenster [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

![](../assets/lp_opt-out-profile-choice.png)

In the **[!UICONTROL Attributes]** tab, you can see the value for **[!UICONTROL choice]** has changed to **[!UICONTROL no]**.

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../message-tracking.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../consent.md#unsubscribe-email)
-->
