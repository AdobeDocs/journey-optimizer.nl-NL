---
title: Aan de slag met de pushconfiguratie
description: De gegevensstroom van pushmeldingen en componenten begrijpen
feature: Applicatie-instellingen
topic: Beheer
role: Administrator
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 0%

---

# Aan de slag met de pushconfiguratie {#get-started-push}

Met pushberichten bereikt u op elk gewenst moment gebruikers van uw mobiele app, vooral wanneer ze uw app niet actief gebruiken. Met pushberichten kunt u verschillende gebruiksgevallen bereiken, zoals het aanbieden van updates over uw service, het vragen van een gebruiker om actie te ondernemen, de gebruiker te waarschuwen voor een nieuwe deal, enz. Apparaatplatforms moeten zich aanmelden voordat eindgebruikers uw meldingen kunnen ontvangen of bekijken. Gebruikers kunnen zich al aanmelden nadat de app voor de eerste keer na de installatie is gestart of in een volgende sessie of workflow, al naar gelang wat van toepassing is. [!DNL Journey Optimizer] ondersteunt pushmeldingen en helpt u zeer relevante meldingen te verzenden met toonaangevende doorvoersnelheden. Pushmeldingen kunnen personalisatie en Reiscontext omvatten om gegevensinzichten van uw merk met Adobe Experience Cloud te benutten.

Deze pagina helpt u bij het instellen en begrijpen van belangrijke services en workflows die betrokken zijn bij pushberichten in [!DNL Journey Optimizer].

De stappen voor het configureren van het pushkanaal in [!DNL Adobe Journey Optimizer] worden beschreven in [deze pagina](push-configuration.md).

## Pushberichten en Adobe Journey Optimizer

De volgende afbeelding toont de systemen en services die bij de bijbehorende gegevensstromen betrokken zijn en geeft aan hoe pushberichten vanuit een end-to-end servicestandpunt worden geleverd.

![](assets/push-flow.png)

1. Registratie van uw merk mobiele app (Android of iOS) met APN&#39;s van Apple en Google FCM-pushberichten
1. De diensten van het overseinen produceren een duptoken, dat, een herkenningsteken is dat Adobe Journey Optimizer zal gebruiken om het specifieke apparaat met een dupmelding te richten.
1. Het eerder gegenereerde pushtoken wordt doorgegeven aan Adobe Experience Platform en gesynchroniseerd met het Real-time klantprofiel. Dit gebeurt OOTB met een eenvoudig te integreren client-SDK
1. Pushberichten zijn ontworpen in Adobe Journey Optimizer, pushberichten worden gemaakt op basis van een berichtvoorinstelling
1. Pushberichten kunnen op het orkestcanvas in Journalen worden opgenomen
1. Na publicatie van de Reis, zijn de klantprofielen die op de voorwaarden van de Reis worden gebaseerd gekwalificeerd om dupberichten te ontvangen, duw overseinen ladingen bij deze stap worden gepersonaliseerd
1. Persoonlijke pushladingen worden doorgestuurd naar een interne service voor pushberichten
1. Deze interne service controleert vervolgens de referenties van de toepassing die aan het bericht is gekoppeld, en
1. Verstuurt het bericht naar Apple &amp; Google Messing Services voor de uiteindelijke aflevering
1. Feedback van berichtenservices wordt vermeld, fouten en successen worden geregistreerd voor rapportage in Live en Global-rapporten van Journey
1. Pushmeldingen worden aan eindgebruikersapparaten geleverd
1. Pushmeldingsinteracties voor eindgebruikers worden als Experience Events verzonden vanuit de eindgebruikerclient via SDK-integratie

## Rollen van de Zeer belangrijke Diensten in de Berichten van de Duw

* **Push Notification service-** providers zijn de belangrijkste onderdelen van webservices die berichten van externe servers naar mobiele apps leveren.

   [!DNL Adobe Journey Optimizer]  ondersteunt zowel Android- als iOS-platforms en kan daarom worden geïntegreerd met:
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging)  - om meldingen naar de mobiele Android-app te verzenden
   * [APN&#39;s (Apple Push Notification Service)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html)  - voor het verzenden van meldingen naar mobiele app voor iOS

* **Adobe Experience Platform Mobile** SDK biedt integratie-API&#39;s aan de clientzijde voor uw mobiele apparaten via met Android en iOS compatibele SDK&#39;s. De SDK biedt een Adobe Journey Optimizer-extensie die een aantal specifieke API&#39;s voor pushberichten toegankelijk maakt en gegevensstroom mogelijk maakt, zoals het registreren van het pushtoken of het verzenden van push-tracking-gebeurtenissen of andere aangepaste ervaringsgebeurtenissen naar Adobe Experience Platform. De SDK biedt ook een groot aantal andere extensies die andere Adobe Experience Cloud en andere partnermogelijkheden van derden mogelijk maken.

   SDK-integratie vereist ook de installatie van Adobe Experience Platform [Data Collection](https://experienceleague.adobe.com/docs/launch/using/home.html)-services, zoals:

   * Een gegevensstroom maken om het profiel te configureren en de gegevenssets met gebeurtenissen te ervaren op basis waarvan de gegevens in Adobe Experience Platform stromen
   * Mobiele eigenschap aan de clientzijde maken en extensies toevoegen. De SDK is nauw geïntegreerd met deze extensies voor een naadloze ervaring bij het verzamelen van gegevens.
   * De bundle-id en toepassingsgegevens van de mobiele app registreren

* **Adobe Experience Platform Real-time Customer**  Profileming behoudt een holistische weergave van elke individuele klant door gegevens van meerdere kanalen te combineren, waaronder web, mobiel, CRM en derden. Het profiel staat u toe om uw klantengegevens in een verenigde mening te consolideren die een actionable, timestamped rekening van elke klanteninteractie aanbiedt. Het pushtoken voor een bepaalde gebruiker van de app wordt als recordgegevens opgeslagen ten opzichte van het profiel van de gebruiker, terwijl de interactie die de gebruiker met pushberichten onderneemt, als gebeurtenisgegevens uit de tijdreeks wordt bijgehouden. [Meer informatie over Adobe Experience Platform Real-time klantprofiel](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)

* **[!DNL Adobe Journey Optimizer]** : als uw mobiele app is geïntegreerd met de hierboven vermelde componenten en uw klantprofielen in Adobe Experience Platform, kunt u pushberichten in Adobe Journey Optimizer ontwerpen en ordenen om contact op te nemen met uw gebruikers.

## Push Technical Setup and Practice Workflows

In de volgende afbeelding ziet u de verschillende stappen van begin tot eind die nodig zijn voor het configureren van de componenten die het skelet van de gegevensstroom van de push vormen. De actiepunten zijn gecategoriseerd gebaseerd op de rol die de configuratie en de component uitvoert die worden gevormd.

![](assets/user-flow.png)
