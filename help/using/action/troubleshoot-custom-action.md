---
solution: Journey Optimizer
product: journey optimizer
title: Aangepaste acties oplossen
description: Leer hoe u een aangepaste handeling kunt oplossen
badge: label="Beperkte beschikbaarheid"
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: handeling, extern, aangepast, reizen, API
source-git-commit: d7ef9cb8b74781d5c711bd2958070767735a3b24
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---


# Aangepaste acties oplossen {#troubleshoot-a-custom-action}

>[!AVAILABILITY]
>
>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.
>

U kunt uw aangepaste handelingen testen door API-aanroepen te verzenden vanuit de beheersectie van de gebruikersinterface van Journey Optimizer. Met deze functie kunt u uw aangepaste acties vóór of na het gebruik ervan tijdens een reis oplossen.

Als beheerder gebruikt u de **[!UICONTROL Send test request]** -functie om uw aangepaste actieconfiguraties te valideren door rechtstreeks vanuit Adobe Journey Optimizer echte API-aanroepen te maken. Deze eigenschap zorgt ervoor dat de verzoekstructuur, de kopballen, de authentificatie, en de lading correct geformatteerd alvorens in een reis worden gebruikt.

![](assets/send-test-request.png){width="70%" align="left"}

Met deze functie stroomlijnt u het test- en validatieproces en zorgt u ervoor dat aangepaste handelingen correct werken tijdens live reizen.

## Vereisten {#troubleshoot-custom-action-prereq}

Om het **[!UICONTROL Send test request]** vermogen te gebruiken, moet de Actie van de a **Douane** pre-gevormd met een URL, kopballen, en authentificatiemontages zijn.

De beheerders kunnen deze mogelijkheid alleen gebruiken als ze beschikken over de volgende machtigingen:

* Gebruikers moeten de machtiging **[!DNL Manage journeys events, data sources and actions]** hebben.
* Deze toestemming is inbegrepen in de *rol van de Beheerders van de Reis*.
* De machtiging **[!DNL View journeys events]** alleen is niet voldoende.

Leer meer over reistoestemmingen in [ deze sectie ](../administration/high-low-permissions.md#journey-capability).

## Hoe te om de Send eigenschap van het testverzoek te gebruiken {#troubleshoot-custom-action-use}

Voer de volgende stappen uit om een aangepaste handeling te testen:

1. Navigeer aan het **de configuratiescherm van Acties van de Douane**, en selecteer een douaneactie.
1. Klik op de knop **[!UICONTROL Send test request]** onder aan het actieconfiguratiescherm.

![ verzendt de knoop van het testverzoek in het paneel van de Configuratie van de Actie ](assets/test-request.png){width="70%" align="left"}

1. In het pop-upvenster kunt u aanvraagparameters opgeven:

   * Als de **methode van de douaneactie GET** is, wordt geen nuttige lading vereist.
   * Als de **methode van de douaneactie POST** is, moet u een nuttige lading JSON verstrekken.

     >[!NOTE]
     >
     >Adobe Journey Optimizer zal een fout veroorzaken als de structuur van dit JSON onjuist is, maar zal het niet doen als er een mismatch met een gegevenstype is. Er treedt bijvoorbeeld geen fout op als een parameter integer wordt gebruikt voor wat een tekenreeks moet zijn.

   * Als verificatie is gedefinieerd, wordt u gevraagd verificatiegegevens in te voeren.

1. Klik **verzenden** om het verzoek uit te voeren.
1. De reactie van de API, inclusief kopteksten en statuscodes, wordt weergegeven in de interface.

## Verificatieverwerking {#troubleshoot-custom-action-auth}

Wanneer een aangepaste handeling verificatie bevat, vereist Adobe Journey Optimizer dat de gebruiker voor elke testaanvraag verificatiegegevens invoert:

* **Basisauthentificatie:** de gebruiker moet het *wachtwoord* verstrekken.
* **API Zeer belangrijke Authentificatie:** de gebruiker moet de API sleutel *waarde* ingaan.
* **Authentificatie van de Douane:** de gebruiker moet de authentificatieparameters in het verzoek *bodyParam* leveren. Twee te voltooien secties worden toegevoegd in dit geval: **verzoek van de Authentificatie** en **de reactie van de Authentificatie**.

## Belangrijkste voordelen {#troubleshoot-custom-action-benefits}

Als Journey Optimizer-beheerder kunt u ook externe gereedschappen (bijvoorbeeld Postman) gebruiken om aangepaste handelingen te testen. De belangrijkste voordelen van de mogelijkheden voor probleemoplossing in producten in vergelijking met externe tests worden hieronder vermeld:

* Het testverzoek wordt uitgevoerd door **Reis van AJO**, betekenend:

   * De exacte aanvraagstructuur (inclusief Adobe Journey Optimizer-specifieke headers) wordt gebruikt.
   * De bron-IP en de kopballen passen die in levende reizen worden gebruikt.

* Het **[!UICONTROL Send test request]** vermogen kan voor het oplossen van problemen **levende reizen** worden gebruikt, aangezien de douaneactie reeds wordt opgesteld.

* Met deze testfunctie voor in-product producten hoeft u geen configuratiedetails handmatig tussen gereedschappen te kopiëren, waardoor het risico op fouten kleiner wordt.

## Problemen oplossen {#troubleshoot-custom-action-check}

Als de aanvraag mislukt, kunt u controleren:

* De verificatiereferenties die in de test zijn ingevoerd.
* De aanvraagmethode (GET versus POST) en de bijbehorende lading.
* Het API eindpunt en de kopballen die in de douaneactie worden bepaald.
* Gebruik de reactiegegevens om potentiële misconfiguraties te identificeren.

