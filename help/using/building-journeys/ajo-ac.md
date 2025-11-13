---
solution: Journey Optimizer
product: journey optimizer
title: Een bericht verzenden met Campagne v7/v8
description: Leer hoe u een bericht verzendt met Campagne v7/v8
feature: Journeys, Integrations, Custom Actions, Use Cases
topic: Administration
role: Admin, Developer, User
level: Intermediate, Experienced
keywords: reis, boodschap, campagne, integratie
exl-id: b07feb98-b2ae-476c-8fcb-873b308176f0
version: Journey Orchestration
source-git-commit: 7822e9662d03e6c6b2d5bc5ecb9ca85dc32f0942
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Een bericht verzenden met Campagne v7/v8 {#campaign-v7-v8-use-case}

In deze handige case worden alle stappen beschreven die vereist zijn om een e-mail te verzenden via de integratie met Adobe Campaign v7 en Adobe Campaign v8.

>[!NOTE]
>
>Als u deze integratie wilt gebruiken, hebt u Campaign v7/v8 build 9125 of hoger nodig.

Maak eerst een transactionele e-mailsjabloon in Campagne. Maak vervolgens in Journey Optimizer de gebeurtenis, handeling en ontwerp de reis.

Raadpleeg de volgende pagina&#39;s voor meer informatie over de integratie van campagnes:

* [Campagne maken](../action/acc-action.md)
* [ Gebruikend de actie in een reis ](../building-journeys/using-adobe-campaign-v7-v8.md).

**Adobe Campaign**

Voor deze integratie moet uw Campagne-instantie zijn ingericht. De eigenschap van het Overseinen van de Transactie moet worden gevormd.

1. Meld u aan bij de besturingsinstantie Campagne.

1. Onder **Beleid** > **Platform** > **Opsommingen**, selecteer het **type van Gebeurtenis** (eventType) opsomming. Maak een nieuw gebeurtenistype (&quot;reis-gebeurtenis&quot;, in ons voorbeeld). Gebruik de interne naam van het gebeurtenistype wanneer u het JSON-bestand later schrijft.

   ![ vorm een gebeurtenis in Adobe Journey Optimizer met schema en gebiedsselectie ](assets/accintegration-uc-1.png)

1. Maak de verbinding met de instantie los en maak opnieuw verbinding zodat het ontwerp van kracht wordt.

1. Onder **Centrum van het Bericht** > **Transactionele berichtmalplaatjes**, creeer een nieuw e-mailmalplaatje dat op het eerder gecreeerde gebeurtenistype wordt gebaseerd.

   ![ de configuratie die van de Gebeurtenis namespace en montages van het profielherkenningsteken toont ](assets/accintegration-uc-2.png)

1. Ontwerp uw sjabloon. In dit voorbeeld wordt personalisatie toegepast op de voornaam en het ordernummer van het profiel. De voornaam staat in de Adobe Experience Platform-gegevensbron en het ordernummer is een veld van de Journey Optimizer-gebeurtenis. Zorg ervoor dat u de juiste veldnamen gebruikt in Campagne.

   ![ de voorproef van de nuttige lading van de Gebeurtenis die JSON structuur met profiel en gebeurtenisgegevens toont ](assets/accintegration-uc-3.png)

1. Publiceer uw transactiesjabloon.

   ![ het exemplaarknoop van de Gebeurtenis om nuttige identiteitskaart voor API integratie te kopiëren ](assets/accintegration-uc-4.png)

1. Schrijf de JSON-lading die overeenkomt met de sjabloon.

```
{
     "channel": "email",
     "eventType": "journey-event",
     "email": "Email address",
     "ctx": {
          "firstName": "First name", "purchaseOrderNumber": "Purchase order number"
     }
}
```

* Voor het kanaal moet u &quot;email&quot; typen.
* Voor eventType gebruikt u de interne naam van het gebeurtenistype dat u eerder hebt gemaakt.
* Het e-mailadres is een variabele, dus u kunt elk label typen.
* Onder ctx, zijn de verpersoonlijkingsgebieden ook variabelen.

**Journey Optimizer**

1. Maak een gebeurtenis. Neem het veld &quot;purchaseOrderNumber&quot; op.

   ![ het scherm van de actieconfiguratie van de Douane voor de integratie van Adobe Campaign Classic ](assets/accintegration-uc-5.png)

1. Maak een actie in Journey Optimizer die overeenkomt met uw campagnemplate. In het **type van Actie** drop-down, uitgezochte **Adobe Campaign Classic**.

   ![ het type van Actie selectie die de optie van Adobe Campaign Classic toont ](assets/accintegration-uc-6.png)

1. Klik het **gebied van de Lading** en kleef JSON vroeger gecreeerd.

   ![ drop-down van de de rekeningsselectie van de campagne voor actiesintegratie ](assets/accintegration-uc-7.png)

1. Voor het e-mailadres en de twee verpersoonlijkingsgebieden, veranderings **Constante** aan **Variabele**.

   ![ de ladlastconfiguratie van de Actie met gebiedstoewijzing voor de integratie van de Campagne ](assets/accintegration-uc-8.png)

1. Maak nu een nieuwe reis en begin met de gebeurtenis die eerder is gemaakt.

   ![ het canvas van de Reis met gebeurtenis en gevormde actie van de Campagne ](assets/accintegration-uc-9.png)

1. Voeg de handeling toe en wijs elk veld toe aan het juiste veld in Journey Optimizer.

   ![ de parameterafbeelding van de Actie met uitdrukkingsredacteur voor dynamische waarden ](assets/accintegration-uc-10.png)

1. Test je reis.

   ![ Volledige reisstroom met gebeurtenistrekker en de uitvoering van de actie van de Campagne ](assets/accintegration-uc-11.png)

1. U kunt nu uw reis publiceren.
