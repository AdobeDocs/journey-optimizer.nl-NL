---
solution: Journey Optimizer
product: journey optimizer
title: Een aangepaste handeling testen
description: Leer hoe u een aangepaste handeling kunt oplossen
badge: label="Beperkte beschikbaarheid"
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: handeling, extern, aangepast, reizen, API
source-git-commit: 5ce76bd61a61e1ed5e896f8da224fc20fba74b53
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 1%

---


# Aangepaste acties oplossen {#troubleshoot-a-custom-action}

>[!AVAILABILITY]
>
>Deze mogelijkheid is alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.
>

## Overzicht

De **verzendt 1} eigenschap van het Verzoek van de Test {staat beheerders toe om hun configuraties van de douaneactie te bevestigen door echte API vraag van Adobe Journey Optimizer (AJO) direct te maken.** Deze eigenschap zorgt ervoor dat de verzoekstructuur, de kopballen, de authentificatie, en de lading correct geformatteerd alvorens in een reis worden gebruikt.

![](assets/send-test-request.png){width="70%" align="left"}

## Vereisten

- **Vereiste Toegang van de Beheerder:**
   - De gebruikers moeten **&quot;hebben de reisgebeurtenissen, gegevensbronnen, en acties&quot;beheren** toestemming.
   - Deze toestemming is inbegrepen in de *rol van de Beheerders van de Reis*.
   - De **&quot;gebeurtenis van de ritten van de Mening...&quot;** toestemming alleen is niet voldoende.
- A **de Actie van de Douane** moet met een URL, kopballen, en authentificatiemontages worden pre-gevormd.

## De functie Testaanvraag verzenden gebruiken

1. Navigeer aan het **de configuratiescherm van Acties van de Douane**.
1. Klik op de **&quot;Send Test Request&quot;** knoop.
1. Er wordt een pop-upvenster weergegeven waarin u aanvraagparameters kunt opgeven:
   - Als de **methode van de douaneactie GET** is, wordt geen nuttige lading vereist.
   - Als de **methode van de douaneactie POST** is, moet u een nuttige lading JSON verstrekken.

     >[!NOTE]
     >
     >AJO zal een fout veroorzaken als de structuur van dit JSON onjuist is maar zal het niet doen als er een wanverhouding met een gegevenstype is. Er treedt bijvoorbeeld geen fout op als een parameter integer wordt gebruikt voor wat een tekenreeks moet zijn.

   - Als verificatie is gedefinieerd, wordt u gevraagd verificatiegegevens in te voeren.

1. Klik **verzenden** om het verzoek uit te voeren.
1. De reactie van de API, inclusief kopteksten en statuscodes, wordt weergegeven in de interface.

## Verificatieverwerking

Wanneer een aangepaste handeling verificatie bevat, vereist AJO dat de gebruiker voor elke testaanvraag verificatiegegevens invoert:

- **Basisauthentificatie:** de gebruiker moet het *wachtwoord* verstrekken.
- **API Zeer belangrijke Authentificatie:** de gebruiker moet de API sleutel *waarde* ingaan.
- **Authentificatie van de Douane:** de gebruiker moet de authentificatieparameters in het verzoek *bodyParam* leveren. Twee te voltooien secties worden toegevoegd in dit geval: **verzoek van de Authentificatie** en **de reactie van de Authentificatie**.

## Belangrijkste verschillen met externe testgereedschappen (bijvoorbeeld Postman)

- Het testverzoek wordt uitgevoerd door **Reis van AJO**, betekenend:
   - De exacte aanvraagstructuur (inclusief AJO-specifieke headers) wordt gebruikt.
   - De bron-IP en de kopballen passen die in levende reizen worden gebruikt.
- Kan voor het oplossen van problemen **levende reizen** worden gebruikt waar de douaneactie reeds wordt opgesteld.
- Elimineert de behoefte om configuratiedetails tussen hulpmiddelen manueel te kopiëren, die het risico van fouten verminderen.

## Problemen oplossen

- Als de aanvraag mislukt, controleert u of:
   - De verificatiereferenties die in de test zijn ingevoerd.
   - De aanvraagmethode (GET versus POST) en de bijbehorende lading.
   - Het API eindpunt en de kopballen die in de douaneactie worden bepaald.
- Gebruik de reactiegegevens om potentiële misconfiguraties te identificeren.

Met deze functie stroomlijnt u het test- en validatieproces en zorgt u ervoor dat aangepaste handelingen correct werken tijdens live AJO-reizen.

