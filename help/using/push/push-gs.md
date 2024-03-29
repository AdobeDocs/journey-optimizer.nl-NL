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
source-git-commit: 03c714833930511fa734662b637d2416728073c2
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 3%

---

# Gegevensstroom van pushmeldingen en componenten {#get-started-push}

Met deze pagina kunt u belangrijke services en workflows instellen en begrijpen die bij pushmeldingen zijn betrokken in [!DNL Journey Optimizer].


>[!AVAILABILITY]
>
>De nieuwe **Snelle start-workflow voor mobiel instapinstapsysteem** is nu beschikbaar. Met deze nieuwe productfunctie kunt u de Mobile SDK snel configureren om gegevens van mobiele gebeurtenissen te verzamelen en te valideren en om mobiele pushberichten te verzenden. Dit vermogen is toegankelijk via de homepage van de Inzameling van Gegevens als openbare bèta. [Meer informatie](mobile-onboarding-wf.md)
>

Meer informatie over het maken van pushmeldingen op [deze pagina](create-push.md).

Stappen voor het configureren van het pushkanaal [!DNL Adobe Journey Optimizer] worden gedetailleerd op [deze pagina](push-configuration.md).

De volgende afbeelding toont de systemen en services die bij de bijbehorende gegevensstromen betrokken zijn en geeft aan hoe pushberichten vanuit een end-to-end servicestandpunt worden geleverd.

![](assets/push-flow.png)

1. Registratie van uw merkloze mobiele app (Android of iOS) met APN&#39;s voor Apple en Google FCM-pushberichten
1. De diensten van het overseinen produceren een duptoken, dat, een herkenningsteken is dat [!DNL Adobe Journey Optimizer] wordt gebruikt om het specifieke apparaat met een pushmelding als doel in te stellen.
1. Het eerder gegenereerde pushtoken wordt doorgegeven aan Adobe Experience Platform en gesynchroniseerd met het Real-time klantprofiel. Dit gebeurt OOTB met een eenvoudig te integreren client-SDK
1. Push-berichten worden in [!DNL Adobe Journey Optimizer], worden pushberichten gemaakt op basis van een kanaaloppervlak (d.w.z. een voorinstelling voor berichten)
1. Pushberichten kunnen op het orkestcanvas in Journalen worden opgenomen
1. Na publicatie van de Reis, zijn de klantprofielen die op de voorwaarden van de Reis worden gebaseerd gekwalificeerd om dupberichten te ontvangen, duw overseinen ladingen bij deze stap worden gepersonaliseerd
1. Persoonlijke pushladingen worden doorgestuurd naar een interne service voor pushberichten
1. Deze interne service controleert vervolgens de referenties van de toepassing die aan het bericht is gekoppeld, en
1. Verstuurt het bericht naar Apple en Google messaging services voor de uiteindelijke levering
1. Feedback van berichtenservices wordt vermeld, fouten en successen worden geregistreerd voor rapportage in Live en Global-rapporten van Journey
1. Pushmeldingen worden aan eindgebruikersapparaten geleverd
1. Pushmeldingsinteracties voor eindgebruikers worden als Experience Events verzonden vanuit de eindgebruikerclient via SDK-integratie

## Rollen van sleutelservices in pushberichten {#roles-of-key-services}

* **Serviceproviders voor pushmeldingen** zijn de belangrijkste onderdelen van webservices die meldingen leveren van externe servers naar mobiele apps.

  [!DNL Adobe Journey Optimizer]  ondersteunt zowel Android- als iOS-platforms en sluit deze daarom aan bij het volgende:
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging) - om meldingen te verzenden naar de mobiele app Android
   * [APN&#39;s (Apple Push Notification Service)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html) - om berichten te verzenden naar de mobiele app van iOS

* **Adobe Experience Platform Mobile SDK** die integratie-API&#39;s aan de clientzijde voor uw mobiele apparaten biedt via met Android en iOS compatibele SDK&#39;s. De SDK biedt een [!DNL Adobe Journey Optimizer] een extensie die een aantal specifieke API&#39;s voor pushberichten toegankelijk maakt en gegevensstroom mogelijk maakt, zoals het registreren van het pushtoken of het verzenden van push-tracking-gebeurtenissen of andere aangepaste ervaringsgebeurtenissen naar Adobe Experience Platform. De SDK biedt ook een groot aantal andere extensies die andere Adobe Experience Cloud en andere partnermogelijkheden van derden mogelijk maken.

  SDK-integratie vereist ook instellen van Adobe Experience Platform [Gegevensverzameling](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=nl){target="_blank"} diensten zoals:

   * Een gegevensstroom maken om het profiel te configureren en de gegevenssets met gebeurtenissen te ervaren op basis waarvan de gegevens in Adobe Experience Platform stromen
   * Mobiele eigenschap aan de clientzijde maken en extensies toevoegen. De SDK is nauw geïntegreerd met deze extensies voor een naadloze ervaring bij het verzamelen van gegevens.
   * De bundle-id en toepassingsgegevens van de mobiele app registreren

* **Adobe Experience Platform Real-time klantprofiel**  onderhoudt een holistische mening van elke individuele klant door gegevens van veelvoudige kanalen, met inbegrip van Web, mobiel, CRM, en derde te combineren. Het profiel staat u toe om uw klantengegevens in een verenigde mening te consolideren die een actionable, timestamped rekening van elke klanteninteractie aanbiedt. Het pushtoken voor een bepaalde gebruiker van de app wordt als recordgegevens opgeslagen ten opzichte van het profiel van de gebruiker, terwijl de interactie die de gebruiker met pushberichten onderneemt, als gebeurtenisgegevens uit de tijdreeks wordt bijgehouden. [Meer informatie over Adobe Experience Platform Real-time klantprofiel](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target="_blank"}.

* **[!DNL Adobe Journey Optimizer]** : zodra uw mobiele app is geïntegreerd met de hierboven vermelde componenten en uw klantprofielen in Adobe Experience Platform, kunt u pushberichten ontwerpen en ordenen in [!DNL Adobe Journey Optimizer] om contact op te nemen met uw gebruikers.

## Werk met meer technische instellingen en praktische workflows {#push-technical-setup}

In de volgende afbeelding ziet u de verschillende stappen van begin tot eind die nodig zijn voor het configureren van de componenten die het skelet van de gegevensstroom van de push vormen. De actiepunten zijn gecategoriseerd gebaseerd op de rol die de configuratie en de component uitvoert die worden gevormd.

![](assets/user-flow.png)

**Verwante onderwerpen**

* [Pushkanaal configureren](push-configuration.md)
* [Pushmeldingenrapport](../reports/journey-global-report.md#push-global)
* [Een pushmelding maken](create-push.md)
* [Een bericht toevoegen in een journey](../building-journeys/journeys-message.md)
* [Een bericht toevoegen aan een campagne](../campaigns/create-campaign.md)