---
title: Aan de slag met de pushconfiguratie
description: De gegevensstroom van pushmeldingen en componenten begrijpen
hide: true
hidefromtoc: true
source-git-commit: a2eee802f82552e56ced00f93e5e4c8a7b3feb7a
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 0%

---

# Aan de slag met de pushconfiguratie {#get-started-push}

![](assets/do-not-localize/badge.png)

Met pushberichten kunt u snel berichten, aanbiedingen of andere informatie doorgeven aan gebruikers van uw mobiele app. Doorgaans moet de eindgebruiker zich aanmelden om pushberichten te ontvangen; de opt-in gebeurt gewoonlijk tijdens het installatieproces en de eindgebruikers krijgen een manier om meldingen te beheren als zij later van mening veranderen. Een belangrijk voordeel van pushberichten in mobiel computergebruik is dat de technologie geen specifieke toepassingen op een mobiel apparaat nodig heeft om een bericht te ontvangen. Hierdoor kan een smartphone meldingen ontvangen en weergeven, zelfs wanneer het scherm van het apparaat is vergrendeld en de mobiele app op de achtergrond of gesloten is.

**[!DNL Adobe Journey Optimizer]**  kunt u tijdgevoelige, relevante en gepersonaliseerde pushberichten op grote schaal verzenden. Een segment van klantprofielen kan worden gebruikt voor het ontvangen van uitgebreide pushberichten op hun iOS- en Android-mobiele apparaten. Deze segmenten kunnen worden gemaakt op basis van eerdere of live gebruikerservaringsgebeurtenissen, gebruikersrecordgegevens of een combinatie van gebruikersinteracties en gegevens. Zodra een reis levend is, kunt u gedetailleerde rapporten bekijken over hoeveel berichten werden verzonden, om welke reden ontbroken en ook duwend volginformatie zoals hoeveel gebruikers op hen klikte.

Dit document zal u door een basis duw- berichten gegevensstroom van begin tot eind gebruikend [!DNL Journey Optimizer] en een diagram van de gebruikersstroom lopen om uit te leggen hoe elke rol zijn verantwoordelijkheden vervult en samenwerkt om de stroom van dupgegevens samen te brengen.


## Betrokken onderdelen en services

* **Cloud Messaging** Providers zijn services van derden waarmee we berichten van externe servers naar mobiele apps kunnen verzenden.

   [!DNL Adobe Journey Optimizer]  ondersteunt zowel Android- als iOS-platforms en werkt met twee services voor primaire cloudberichten:
   * Firebase Cloud Messaging (FCM) - berichten verzenden naar mobiele Android-app
   * Apple Push Notification Service (APNs) - voor het verzenden van meldingen naar mobiele app voor iOS

* **Mobile App geïntegreerd met Adobe Mobile** SDK, waarmee u uw mobiele apps kunt integreren met Adobe Experience Cloud Solutions. De mobiele SDK bestaat uit diverse Experience Cloud oplossing-uitbreidingen om eigenschappen te verstrekken specifiek voor de dienst zij vertegenwoordigen. Deze extensies maken verschillende API&#39;s beschikbaar om gegevensstroom in te schakelen, zoals het registreren van het pushtoken of het verzenden van push-gebeurtenissen of andere aangepaste ervaringsgebeurtenissen naar Adobe Experience Platform.

* **Adobe Launch**  (of gegevensverzameling) is de volgende generatie mogelijkheden voor beheer van mobiele SDK waarmee gegevens van de Mobile SDK naar  [!DNL Adobe Experience Platform]kunnen worden verzonden. Het biedt mogelijkheden om extensies te registreren, regels en gegevenselementen te maken om gegevens van uw mobiele app naar de Adobe Experience Cloud-oplossingen te verzenden. Met betrekking tot de stroom van de gegevens van dupmeldingen, zijn de primaire configuraties die in de Lancering van Adobe worden vereist:

   * Creërend een gegevensstroom om het profiel en de datasets van de ervaringsgebeurtenis te vormen waartegen de gegevens in ervaringsplatform stromen.
   * Een client-side mobiele eigenschap maken en extensies toevoegen. Mobile SDK is nauw geïntegreerd met deze extensies voor een naadloze ervaring bij het verzamelen van gegevens.
   * Registreer de bundle-id en de toepassingsreferenties van de mobiele app om de hygiëne van de app op het moment van de publicatie van de pushmelding op unieke wijze te identificeren en valideren.

* **Klantprofiel in realtime is de** component in Adobe Experience Platform die u in staat stelt een holistische weergave van elke individuele klant te bekijken door gegevens van meerdere kanalen te combineren, waaronder web, mobiel, CRM en derden. Het profiel staat u toe om uw klantengegevens in een verenigde mening te consolideren die een actionable, timestamped rekening van elke klanteninteractie aanbiedt. Statische gegevens die de gebruiker van de mobiele app identificeren, zoals een pushtoken, worden opgeslagen volgens het profiel van de gebruiker als recordgegevens, terwijl de interactie die de gebruiker met pushberichten maakt, wordt bijgehouden als gebeurtenisgegevens uit de tijdreeks.

* **[!DNL Adobe Journey Optimizer]** : zodra uw mobiele app-integratie met bovengenoemde componenten is geïnstalleerd en uw klantprofielen beschikbaar zijn als realtime-klantprofielen, kunt u profiteren van de krachtige mogelijkheden voor publiekssegmentatie  [!DNL Adobe Journey Optimizer]  om ervoor te zorgen dat elke persoon de beste ervaring heeft.


## Gegevensstroom duwen

Dit diagram toont een basisstroom van de gegevens van het drukkingsoverseinen en geeft een blik bij de diverse producten en de componenten van Adobe betrokken bij de stroom.

![](assets/push-flow.png)


1. De klant ontwikkelt een mobiele app op Android of iOS die hij of zij aan zijn of haar gebruikers zou vrijgeven. Om gebruik te kunnen maken van de pushmogelijkheden die worden geboden door push-providers, d.w.z. APNS van Apple en FCM van Google, registreert de mobiele app zichzelf en maakt deze de mogelijkheid tot pushberichten mogelijk.
1. De pushproviders genereren een pushtoken en sturen dit naar de mobiele app. Een pushtoken is een id die afzenders gebruiken om specifieke apparaten met een pushmelding als doel in te stellen.
1. De mobiele app is geïntegreerd met de Adobe Mobile SDK, die verschillende extensies en API&#39;s beschikbaar maakt. De uitbreiding van het Overseinen stelt API bloot om het pushtoken in Adobe Experience Platform tegen het profiel van de klant te registreren.
1. Zodra de mobiele app klaar is, wordt deze samen met de referenties geconfigureerd in **[!DNL Journey Launch]** `>` **App Configurations**.
De markeerder ontwerpt nu een pushmelding in **[!DNL Adone Journey Optimizer]** `>` **Berichten** tegen de geregistreerde mobiele app.
1. De markeerder organiseert een klantenreis die de stroom van gebeurtenissen en acties bepaalt. Als u een pushmelding wilt verzenden in een stadium van de rit, voegt de markeerteken een actie van het type &#39;Bericht&#39; toe en koppelt u deze aan het bericht dat in de vorige stap is geschreven.
1. Wanneer een klantprofiel in aanmerking komt om de pushmelding te ontvangen om welke reden dan ook, bijvoorbeeld bij het activeren van een gebeurtenis of bij het kwalificeren van een segment, wordt het bericht gepersonaliseerd ten opzichte van het profiel, indien van toepassing.
1. Het persoonlijke pushbericht wordt verzonden voor verdere verwerking naar de pushservice.
1. De pushservice valideert de referenties van de app die aan het bericht is gekoppeld.
1. Het bericht wordt naar de pushproviders verzonden voor levering aan de mobiele app op basis van het specifieke pushtoken en de gegevens.
1. De pushproviders sturen een feedback waarin wordt gesuggereerd of het bericht correct aan de provider is bezorgd. Als dat niet het geval is, maakt het desbetreffende foutbericht deel uit van de feedback. Deze feedback wordt naar de Adobe-rapportage gestuurd, zodat de klant deze kan bekijken op zijn reis [Live](reports/live-report.md) en [Global Reports](reports/global-report.md).
1. Ondertussen leveren de pushproviders asynchroon de geslaagde pushmelding aan de mobiele app.
1. Wanneer de klant met de melding communiceert, kunnen de indrukken zoals click/open vervolgens worden bijgehouden als **Experience Events**. De uitbreiding van het Overseinen stelt APIs bloot om volgende gebeurtenissen naar Adobe Experience Platform tegen het profiel van de klant te verzenden.

## Gebruikersstroom duwen

Dit diagram toont de diverse stappen betrokken bij het vormen van de componenten die het skelet van de stroom van duwgegevens vormen. De actiepunten zijn gecategoriseerd gebaseerd op de rol die de configuratie en de component uitvoert die worden gevormd. Zoals u kunt zien, moet u ervoor zorgen dat er configuraties en integratie zijn in de mobiele app **[!DNL Adobe Launch]** en **[!DNL Adobe Experience Platform]** voordat u pushmeldingen verzendt.**[!DNL Adobe Journey Optimizer]**

![](assets/user-flow.png)

Gedetailleerde stappen voor het configureren van het pushkanaal en het inschakelen van pushmeldingen in [!DNL Journey Optimizer] zijn beschikbaar op [deze pagina](push-configuration.md).