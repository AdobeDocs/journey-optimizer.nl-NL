---
title: Weigeren beheren
description: Meer informatie over het beheren van opt-out en privacy
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 049dbf7f4939bfc6db677000fee1cfb6dbdceb39
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 0%

---

# Weigeren beheren {#consent}

Gebruiken [!DNL Journey Optimizer] om de toestemming van uw ontvangers voor communicatie te volgen en te begrijpen hoe zij met uw merk willen werken door hun voorkeuren en abonnementen te beheren. <!--Their preferences and subscriptions are handled through Consent management.-->

Regels zoals de GDPR bepalen dat u aan specifieke vereisten moet voldoen voordat u informatie van de Onderwerpen van Gegevens kunt gebruiken. Bovendien moeten betrokkenen hun toestemming te allen tijde kunnen wijzigen.

**Waarom is het belangrijk?**

* Als u deze voorschriften niet naleeft, brengt u juridische risico&#39;s met zich mee voor uw merk.
* Het helpt u vermijden verzendend ongevraagde mededelingen naar uw ontvangers, die hen zouden kunnen maken uw berichten als spam merken en uw reputatie schaden.

Meer informatie over het beheren van privacy en de toepasselijke regels in het dialoogvenster [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html){target=&quot;_blank&quot;}.

<!--* Recipients should be able to opt-in/opt-out from receiving electronic communication through one or more channel
* Recipients expect the brand to offer preference centre capability that controls how brand should engage with them (example: channel of communication, invasive and non-invasive tracking etc). This helps to fulfil regulatory obligations and also facilitates quality engagement with recipient. 
* The third category is the capability to offer subscription to recipients (newsletter, etc)-->

## Uitschakelen, beheer {#opt-out-management}

Het is een wettelijke vereiste dat ontvangers de mogelijkheid krijgen om zich af te melden voor het ontvangen van communicatie van een merk. Meer informatie over de toepasselijke wetgeving vindt u in het [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}.

Daarom moet u altijd een **afmelden, koppeling** in elke e-mail die naar ontvangers wordt verzonden:

* Nadat u op deze koppeling hebt geklikt, worden de ontvangers naar een bestemmingspagina geleid, inclusief een knop om te bevestigen dat ze het programma willen afsluiten.
* Nadat u op de knop Weigeren hebt geklikt, wordt een Adobe I/O-aanroep uitgevoerd om de profielgegevens bij te werken met deze gegevens. [Meer informatie hierover](#consent-service-api).

### Koppeling voor annuleren toevoegen {#add-unsubscribe-link}

Voer de onderstaande stappen uit om een koppeling voor afmelden toe te voegen:

1. Bouw uw openingspagina voor abonnementen.

1. De gastheer het op het derdesysteem van uw keus.

1. [Een bericht maken](../../help/using/create-message.md) in [!DNL Journey Optimizer].

   <!--The link to your landing page should contain a static URL and the profile ID.-->

1. Selecteer tekst in de inhoud en voeg een koppeling in met behulp van de contextafhankelijke werkbalk.

   ![](assets/opt-out-insert-link.png)

1. Selecteren **[!UICONTROL Unsubscription link]** van de **[!UICONTROL Link type]** vervolgkeuzelijst.

   ![](assets/opt-out-link-type.png)

1. In de **[!UICONTROL Link]** , plakt u de koppeling naar de bestemmingspagina.

   ![](assets/opt-out-link-url.png)

1. Klik op **[!UICONTROL Save]**.

1. Sla uw inhoud op en [uw bericht publiceren](../../help/using/publish-manage-message.md).

   >[!NOTE]
   >
   >De URL van de landingspagina van derden bevat drie parameters waarmee de voorkeuren van de profielen via een aanroep van Adobe I/O worden bijgewerkt. &#x200B; [Meer informatie in deze sectie](#consent-service-api).

1. Verzend uw bericht met de verbinding aan uw landende pagina door [reis](building-journeys/journey.md).

1. Zodra het bericht wordt ontvangen, als de ontvanger de unsubscribe verbinding klikt, wordt uw landende pagina getoond.

   ![](assets/opt-out-lp-example.png)

1. Als de ontvanger op de knop Weigeren klikt op de bestemmingspagina (hier de **Abonnement opzeggen** (knop), worden de profielgegevens bijgewerkt via een [Adobe I/O-oproep](#opt-out-api).

   De ontvanger van de optie-uit wordt dan opnieuw gericht aan een bevestigingsberichtscherm erop wijzend dat het kiezen uit succesvol was.

   ![](assets/opt-out-confirmation-example.png)

   Dit heeft tot gevolg dat deze gebruiker geen communicatie van uw merk ontvangt, tenzij hij opnieuw een abonnement neemt.

Als u wilt controleren of de keuze van het corresponderende profiel is bijgewerkt, gaat u naar het Experience Platform en opent u het profiel door een naamruimte voor identiteiten en een bijbehorende identiteitswaarde te selecteren. Meer informatie in het dialoogvenster [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

![](assets/opt-out-profile-choice.png)

In de **[!UICONTROL Attributes]** tab, kunt u de waarde zien voor **[!UICONTROL choice]** is gewijzigd in **[!UICONTROL no]**.

<!--The opt-out URL is resolved upon each recipient receiving the message. It is then personalized with the relevant encrypted parameters (profile ID, profile name, journey ID, sandbox ID, and message execution ID).-->

### Uitschakelen van API-aanroep {#opt-out-api}

Nadat de ontvanger heeft uitgeschakeld, klikt u op de koppeling voor het opzeggen van het abonnement, een Adobe I/O API <!--Consent service API to capture the encrypted data and-->wordt aangeroepen om de voorkeur van het corresponderende profiel bij te werken.

Deze vraag van de POST van Adobe I/O is als volgt:

Eindpunt: platform.adobe.io/journey/imp/consent/preferences
<!--This is the new AEP specific AEP for consent instead of the AJO consent API that was previously used: cjm.adobe.io/imp/consent/preferences-->

Parameters query:

* **param**: bevat de gecodeerde lading
* **sig**: handtekening <!--which signature?-->
* **pid**: gecodeerde profiel-id

Deze parameters zijn beschikbaar via de unsubscribe-koppeling die naar de ontvanger is verzonden, bijvoorbeeld de URL waarmee de landingspagina van derden voor een bepaalde ontvanger wordt geopend:

![](assets/opt-out-parameters.png)

<!--QUESTION: How do you get the URL built for each recipient? Do you have to wait until each targeted recipient receives the unsubscribe link or can you deduce it in advance? Is it done automatically upon the API call or do you have to do something manually for each profile? In other words will the LP automatically include the 3 parameters or do you have to insert something manually? Still not completely clear-->

Eisen voor koptekst:

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* autorisatie (gebruikerstoken van uw technische account) <!--How do you find this information? And other header elements?-->

Instantie van aanvraag:

```
{
   "marketing": [
       {
            "type": "email",           
            "choice": "no",          
            "scope": "channel"       
        }
    ],
 
}
```

<!--The Consent service /-->[!DNL Journey Optimizer] will <!--decrypt and-->use these parameters to update the corresponding profile's choice.
<!--and provide an answer back to the landing page.-->

## Eén klik op Weigeren {#one-click-opt-out}

Omdat veel klanten op zoek zijn naar een eenvoudiger proces om hun abonnement op te zeggen, kunt u ook een link met één muisklik toevoegen aan uw e-mailinhoud. Deze verbinding zal uw ontvangers toelaten om van uw mededelingen snel af te zien, zonder aan een landende pagina worden opnieuw gericht waar zij moeten bevestigen het kiezen uit.

Leer hoe u een koppeling om te weigeren toevoegt aan uw berichtinhoud in [deze sectie](message-tracking.md#one-click-opt-out-link).

Zodra uw bericht door [reis](building-journeys/journey.md)Als een ontvanger op de koppeling om te weigeren klikt, wordt zijn profiel onmiddellijk uitgeschakeld.

## Koppeling in koptekst opzeggen {#unsubscribe-email}

Als de e-mailclient van de ontvangers ondersteuning biedt voor het weergeven van een niet-geabonneerde koppeling in de e-mailheader, worden e-mails verzonden met [!DNL Journey Optimizer] neemt deze koppeling automatisch op.

De koppeling voor afmelden wordt bijvoorbeeld als volgt weergegeven in Gmail:

![](assets/unsubscribe-email.png)

Afhankelijk van de e-mailclient heeft het klikken op de koppeling voor het afmelden van abonnementen in de header een van de volgende gevolgen:

* Het corresponderende profiel wordt direct uitgeschakeld en deze keuze wordt in het Experience Platform bijgewerkt. Meer informatie in het dialoogvenster [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

* Dit heeft hetzelfde effect als klikken op de koppeling Abonnement opzeggen in de e-mailinhoud: de ontvanger wordt omgeleid naar een bestemmingspagina met een knop om te bevestigen dat hij of zij het programma afsluit. Meer informatie over beheer van opt-out in [deze sectie](#opt-out-management).

## Push opt-out-beheer {#push-opt-out-management}

Push-ontvangers kunnen hun abonnement opzeggen via hun apparaten zelf.

Ze kunnen er bijvoorbeeld voor kiezen om meldingen te stoppen wanneer ze worden gedownload of wanneer ze uw app gebruiken. Op dezelfde manier kunnen ze de meldingsinstellingen wijzigen via het mobiele besturingssysteem.
