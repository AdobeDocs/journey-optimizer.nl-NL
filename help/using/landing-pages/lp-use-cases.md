---
title: Gebruiksgevallen van landingspagina
description: Ontdek de meest gebruikelijke gebruiksgevallen bij bestemmingspagina's in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 0%

---

# Gebruiksgevallen van landingspagina

Hieronder ziet u voorbeelden van hoe u kunt gebruiken [!DNL Journey Optimizer] het landen van pagina&#39;s om uw klanten te hebben binnen of uit van het ontvangen van wat of elk van uw mededelingen kiezen.

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## Abonnement op een service {#subscription-to-a-service}

De belangrijkste stappen om uw ontvangers ertoe aan te zetten zich op de dienst te abonneren zijn hieronder vermeld.

![](../assets/lp_subscription-uc.png)

Stel bijvoorbeeld dat u volgende maand een gebeurtenis organiseert en een registratiecampagne voor een gebeurtenis wilt starten om uw klanten die geïnteresseerd zijn, op de hoogte te houden van die gebeurtenis.

1. Maak de abonnementenlijst van de gebeurtenisregistratie. Meer informatie over [abonnementenlijsten](subscription-list.md)

1. [Een openingspagina maken](create-lp.md), waardoor de ontvangers zich kunnen registreren voor uw gebeurtenis.

1. Configureer en ontwerp de openingspagina voor registratie, inclusief de koppeling naar de abonnementenlijst. Meer informatie over het samenstellen van de [primaire landingspagina](create-lp.md#configure-primary-page)

1. Maak een pagina voor bedankt die aan de ontvangers wordt weergegeven wanneer ze het registratieformulier verzenden. Meer informatie over [subpagina&#39;s landen](create-lp.md#configure-subpages)

1. Maak een e-mailbericht. Meer informatie over [berichten maken](../create-message.md)

1. [Een koppeling invoegen](../message-tracking.md#insert-links) in uw bericht. Selecteren **[!UICONTROL Landing page]** als de **[!UICONTROL Link type]** en kiest u [landingspagina](create-lp.md#configure-primary-page) die u voor registratie hebt gemaakt.

   ![](../assets/lp_subscription-uc-link.png)

1. Sla uw inhoud op en [uw bericht publiceren](../publish-manage-message.md).

1. Uw bericht verzenden via een [reis](../building-journeys/journey.md) om aan te geven dat de registratie nu is geopend voor uw gebeurtenis en om het verkeer naar de bestemmingspagina van de registratie te leiden.

   Als de ontvangers eenmaal een e-mail hebben ontvangen en op de koppeling naar de bestemmingspagina klikken, worden ze doorgestuurd naar de pagina Bedankt en worden ze toegevoegd aan de abonnementenlijst.

1. U kunt een bevestigingsbericht verzenden naar de ontvangers die zich hebben geregistreerd voor uw gebeurtenis. Om dit te doen, stuur het door een andere reis gebruikend **[!UICONTROL Segment qualification]** en selecteer de abonnementenlijst die u als segment hebt gemaakt.

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

Om de ontvangers van een bericht toe te laten om van uw mededelingen door een het landen pagina af te melden, volg de hieronder stappen.

1. Stel uw [landingspagina](create-lp.md). Specifieke landingspagina&#39;s gebruiken **[!UICONTROL Form]** component, een component definiëren **[!UICONTROL Opt-out]** selectievakje en kies voor bijwerken **[!UICONTROL Channel (email)]**: Het profiel dat het vak Weigeren op de bestemmingspagina controleert, wordt uit al uw communicatie verwijderd. [Meer informatie](design-lp.md)

   <!--You can also build your own landing page and host it on the third-party system of your choice. To keep?-->

1. [Een bericht maken](../create-message.md) in [!DNL Journey Optimizer].

1. Selecteer tekst in uw inhoud en [een koppeling invoegen](../message-tracking.md#insert-links) gebruiken van de contextafhankelijke werkbalk. U kunt ook een koppeling op een knop gebruiken.

   ![](../assets/lp_opt-out-insert-link.png)

1. Selecteren **[!UICONTROL Landing page]** van de **[!UICONTROL Link type]** vervolgkeuzelijst.

1. Selecteer [landingspagina](create-lp.md#configure-primary-page) die u hebt gemaakt voor het uitschakelen.

   ![](../assets/lp_opt-out-landing-page.png)

1. Klik op **[!UICONTROL Save]**.

1. Sla uw inhoud op en [uw bericht publiceren](../publish-manage-message.md).

1. Uw bericht verzenden via een [reis](../building-journeys/journey.md).

1. Zodra het bericht wordt ontvangen, als de ontvanger de unsubscribe verbinding klikt, wordt uw landende pagina getoond.

   <!--![](../assets/lp_opt-out-lp-example.png)-->

1. Als de ontvanger op de koppeling om te weigeren klikt op de bestemmingspagina, worden de profielgegevens bijgewerkt en ontvangen deze geen communicatie van uw merk tenzij u opnieuw een abonnement neemt.

   <!--The opted-out recipient is then redirected to a confirmation message screen indicating that opting out was successful.-->

   <!--![](../assets/lp_opt-out-confirmation-example.png)-->

Als u wilt controleren of de keuze van het corresponderende profiel is bijgewerkt, gaat u naar het Experience Platform en opent u het profiel door een naamruimte voor identiteiten en een bijbehorende identiteitswaarde te selecteren. Meer informatie in het dialoogvenster [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

![](../assets/lp_opt-out-profile-choice.png)

In de **[!UICONTROL Attributes]** tab, kunt u de waarde zien voor **[!UICONTROL choice]** is gewijzigd in **[!UICONTROL no]**.

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../message-tracking.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../consent.md#unsubscribe-email)
-->