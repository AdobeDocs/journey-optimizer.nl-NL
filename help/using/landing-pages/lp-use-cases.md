---
title: Gebruiksgevallen van landingspagina
description: Ontdek de meest gebruikelijke gebruiksgevallen bij bestemmingspagina's in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
exl-id: 8c00d783-54a3-45d9-bd8f-4dc58804d922
source-git-commit: 88b037e079a46e10f7ee4715e78e5edc5a34a6ce
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 1%

---

# Gebruiksgevallen van landingspagina

Hieronder ziet u enkele voorbeelden van het gebruik van [!DNL Journey Optimizer] het landen van pagina&#39;s om uw klanten te hebben binnen of uit van het ontvangen van wat of elk van uw mededelingen kiezen.

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## Abonnement op een service {#subscription-to-a-service}

Een van de meest gebruikelijke gebruiksgevallen is het uitnodigen van uw klanten om [abonneren op een service](subscription-list.md) (zoals een nieuwsbrief of een gebeurtenis) door een landingspagina. De belangrijkste stappen worden weergegeven in de onderstaande grafiek:

![](../assets/lp_subscription-uc.png)

Stel bijvoorbeeld dat u volgende maand een gebeurtenis organiseert en een registratiecampagne voor een gebeurtenis wilt starten<!--to keep your customers that are interested updated on that event-->. Hiervoor stuurt u een e-mail met een koppeling naar een bestemmingspagina waarmee uw ontvangers zich kunnen registreren voor deze gebeurtenis. De gebruikers die zich registreren, worden toegevoegd aan de abonnementenlijst die u voor dit doel hebt gemaakt.

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

1. Een andere maken [reis](../building-journeys/journey.md). U kunt dit rechtstreeks vanaf de bestemmingspagina doen door op de knop **[!UICONTROL Create journey]** knop. Meer informatie [hier](create-lp.md#configure-primary-page)

   ![](../assets/lp_subscription-uc-create-journey.png)

1. De **[!UICONTROL Events]** categorie en een **[!UICONTROL Segment Qualification]** op uw canvas. Meer informatie [hier](../building-journeys/segment-qualification-events.md)

1. Klik in het dialoogvenster **[!UICONTROL Segment]** en selecteer de abonnementenlijst die u hebt gemaakt.

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
