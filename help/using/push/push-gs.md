---
solution: Journey Optimizer
product: journey optimizer
title: Stroom van pushberichten in Adobe Journey Optimizer
description: De gegevensstroom van pushmeldingen en componenten begrijpen
topic: Mobile
feature: Push, Overview
role: Admin
level: Intermediate
exl-id: 9718c4b6-2558-4dfd-9d8f-f8845def19ba
source-git-commit: 5b8d26b4fbc323308b5a49672f9d30298756ccf9
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 1%

---

# Gegevensstroom van pushmeldingen en componenten {#get-started-push}

Deze pagina helpt u bij het instellen en begrijpen van de belangrijkste services en workflows die betrokken zijn bij pushberichten in [!DNL Journey Optimizer] .


>[!AVAILABILITY]
>
>Het nieuwe **Mobiele onboarding snelle beginwerkschema** is nu beschikbaar. Met deze nieuwe productfunctie kunt u de Mobile SDK snel configureren om gegevens van mobiele gebeurtenissen te verzamelen en te valideren en om mobiele pushberichten te verzenden. Dit vermogen is toegankelijk via de homepage van de Inzameling van Gegevens als openbare bèta. [Meer informatie](mobile-onboarding-wf.md)
>

Leer hoe te om pushberichten op [ tot stand te brengen deze pagina ](create-push.md).

De stappen om drukkanaal in [!DNL Adobe Journey Optimizer] te vormen zijn gedetailleerd op [ deze pagina ](push-configuration.md).

De volgende afbeelding toont de systemen en services die bij de bijbehorende gegevensstromen betrokken zijn en geeft aan hoe pushberichten vanuit een end-to-end servicestandpunt worden geleverd.

![](assets/push-flow.png)

1. Registratie van uw merk mobiele app (Android of iOS) met Apple-APN&#39;s en Google FCM-pushberichten
1. De diensten van het overseinen produceren een duptoken, dat, een herkenningsteken is dat [!DNL Adobe Journey Optimizer] zal gebruiken om het specifieke apparaat met een dupmelding te richten.
1. Het eerder gegenereerde pushtoken wordt doorgegeven aan Adobe Experience Platform en gesynchroniseerd met het Real-time klantprofiel. Dit gebeurt OOTB met een eenvoudig te integreren client-SDK
1. Pushberichten worden geschreven in [!DNL Adobe Journey Optimizer] , Pushberichten worden gemaakt op basis van een kanaalconfiguratie (d.w.z. een berichtvoorinstelling)
1. Pushberichten kunnen op het orkestcanvas in Journalen worden opgenomen
1. Na publicatie van de Reis, zijn de klantprofielen die op de voorwaarden van de Reis worden gebaseerd gekwalificeerd om dupberichten te ontvangen, duw overseinen ladingen bij deze stap worden gepersonaliseerd
1. Persoonlijke pushladingen worden doorgestuurd naar een interne service voor pushberichten
1. Deze interne service controleert vervolgens de referenties van de toepassing die aan het bericht is gekoppeld, en
1. Verstuurt het bericht naar Apple en Google messaging services voor de uiteindelijke levering
1. Feedback van berichtenservices wordt vermeld, fouten en successen worden geregistreerd voor rapportage in het rapport Journey Live &amp; Customer Journey Analytics
1. Pushmeldingen worden aan eindgebruikersapparaten geleverd
1. Interacties met pushmeldingen voor eindgebruikers worden als Experience Events verzonden vanuit de eindgebruikerclient via SDK-integratie

## Rollen van sleutelservices in pushberichten {#roles-of-key-services}

* **de dienstverleners van het pushbericht** zijn de diensten van het kerncomponentenWeb die berichten van verre servers aan mobiele apps leveren.

  [!DNL Adobe Journey Optimizer] ondersteunt zowel Android- als iOS-platforms en kan daarom worden geïntegreerd met:
   * [ het Overseinen van de Wolk van de Vuurbasis (FCM) ](https://firebase.google.com/docs/cloud-messaging) - om berichten naar Android mobiele app te verzenden
   * [ de Dienst van het Push Bericht van Apple (APNs) ](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html) - om berichten naar mobiele app van iOS te verzenden

* **Adobe Experience Platform Mobile SDK** die cliënt-zijintegratie APIs voor uw mobiles via Android en iOS compatibele SDKs verstrekt. De SDK biedt een [!DNL Adobe Journey Optimizer] -extensie die een aantal specifieke API&#39;s voor pushberichten toegankelijk maakt en gegevensstroom mogelijk maakt, zoals het registreren van het pushtoken of het verzenden van push-tracking-gebeurtenissen of andere aangepaste ervaringsgebeurtenissen naar Adobe Experience Platform. De SDK biedt ook diverse andere extensies die andere Adobe Experience Cloud en andere partnermogelijkheden van derden mogelijk maken.

  De integratie van SDK vereist ook opstelling van de [ diensten van de Inzameling van Gegevens van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=nl){target="_blank"} zoals:

   * Een gegevensstroom maken om het profiel te configureren en de gegevenssets met gebeurtenissen te ervaren op basis waarvan de gegevens in Adobe Experience Platform stromen
   * Mobiele eigenschap aan de clientzijde maken en extensies toevoegen. De SDK is nauw geïntegreerd met deze extensies voor een naadloze ervaring bij het verzamelen van gegevens.
   * De bundle-id en toepassingsgegevens van de mobiele app registreren

* **Adobe Experience Platform Real-time het Profiel van de Klant** handhaaft een holistische mening van elke individuele klant door gegevens van veelvoudige kanalen, met inbegrip van Web, mobiel, CRM, en derde te combineren. Het profiel staat u toe om uw klantengegevens in een verenigde mening te consolideren die een actionable, timestamped rekening van elke klanteninteractie aanbiedt. Het pushtoken voor een bepaalde gebruiker van de app wordt als recordgegevens opgeslagen ten opzichte van het profiel van de gebruiker, terwijl de interactie die de gebruiker met pushberichten onderneemt, als gebeurtenisgegevens uit de tijdreeks wordt bijgehouden. [ Leer meer over het Profiel van de Klant in real time van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target="_blank"}.

* **[!DNL Adobe Journey Optimizer]** : zodra uw mobiele app is geïntegreerd met de hierboven vermelde componenten en uw klantprofielen in Adobe Experience Platform, kunt u pushberichten ontwerpen en ordenen in [!DNL Adobe Journey Optimizer] om contact op te nemen met uw gebruikers.

## Werk met meer technische instellingen en praktische workflows {#push-technical-setup}

In de volgende afbeelding ziet u de verschillende stappen van begin tot eind die nodig zijn voor het configureren van de componenten die het skelet van de gegevensstroom van de push vormen. De actiepunten zijn gecategoriseerd gebaseerd op de rol die de configuratie en de component uitvoert die worden gevormd.

![](assets/user-flow.png)

**Verwante onderwerpen**

* [Pushkanaal configureren](push-configuration.md)
* [Pushmeldingenrapport](../reports/journey-global-report-cja-push.md)
* [Een pushmelding maken](create-push.md)
* [Een bericht toevoegen tijdens een rit](../building-journeys/journeys-message.md)
* [Een bericht toevoegen aan een campagne](../campaigns/create-campaign.md)