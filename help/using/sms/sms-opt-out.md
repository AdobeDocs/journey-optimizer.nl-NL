---
solution: Journey Optimizer
product: journey optimizer
title: SMS-opt-out-beheer
description: Meer informatie over het beheren van opt-out met SMS-berichten
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 676e2d6788c8110b76a38e857a62ba9c1be5842c
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# SMS-opt-out-beheer {#sms-opt-out}

In overeenstemming met de industriestandaarden en -voorschriften moeten alle SMS-marketingberichten een manier bevatten waarop de ontvangers hun abonnement gemakkelijk kunnen opzeggen. [Meer informatie over privacy- en opt-outbeheer](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Communicatie van tekstberichten kan afhankelijk van zijn aard, de plaats van waar u tekstberichten verzendt, en de plaats van uw ontvangers onderworpen zijn aan diverse wettelijke nalevingsvereisten. Terwijl Adobe Journey Optimizer de berichten over lange codes en gratis nummers afhandelt zoals hieronder beschreven, raadpleegt u uw juridische adviseur om ervoor te zorgen dat uw communicatie over tekstberichten voldoet aan alle toepasselijke wettelijke nalevingsvereisten.

## Oorspronkelijke binnenkomende trefwoorden{#sms-native-keywords}

Adobe Journey Optimizer verwerkt standaard standaardantwoordberichten in de Engelse taal, zoals STOP, UNSTOP en START voor berichten met de gratis en lange code, in overeenstemming met industriestandaarden voor native integratie, zoals Sinch en Twilio.

Deze trefwoorden activeren doorgaans een automatische standaardreactie van uw externe provider (zoals Twilio of Sinch). U kunt dit rechtstreeks bij uw provider of via de documentatiesite bevestigen.

Er zijn geen stappen vereist om ervoor te zorgen dat de mogelijkheden voor SMS-uitschakelmogelijkheden in Adobe Journey Optimizer werken als de trefwoordreacties STOP, UNSTOP en START automatisch worden herkend. De status van de optie om profielen te weigeren wordt in real time bijgewerkt in Adobe Journey Optimizer.


## Lijsten van gewezen personen{#sms-blocklists}

Naast het tegenhouden van Adobe Journey Optimizer verzendt op basis van de opt-out status (voor directe integratie met Twilio of Sinch), handhaven de meeste de gatewayleveranciers van SMS ook een lijst van gewezen personen die u verzekert dat een bericht van SMS niet aan een individu wordt geleverd die heeft verkozen om uit te kiezen. Als u een andere provider dan Sinch of Twilio gebruikt en een SMS-bericht verzendt via [aangepast kanaal](../building-journeys/using-custom-actions.md)moet u dit bevestigen met uw provider.


## Korte codes {#short-codes}

Adobe Journey Optimizer verwerkt standaard geen opt-out-, opt-in- of Help-trefwoorden voor korte codenummers. U moet ervoor zorgen dat uw korte code aan alle industrieregels en verordeningen voor opt-out behandeling voldoet.

## Alfanumerieke afzender-id {#alphanumeric}

Alfanumerieke identiteitskaart van de Afzender is slechts voor unidirectioneel overseinen, en kan binnenkomende berichten niet ontvangen. Als gevolg hiervan zijn de SMS STOP, START, HELP-trefwoorden van Adobe Journey Optimizer niet van toepassing op Alfa-verzender-id&#39;s. U moet andere instructies verstrekken, zoals het schrijven aan het team van de Steun, het roepen van een de telefoonlijn van de Steun, of het sms&#39;en van een ander telefoonaantal of code om gebruikers toe te staan om van berichten te kiezen die via Alphanumeric identiteitskaart van de Afzender worden verzonden.

## Video {#video-sms}

Raadpleeg de volgende video voor meer informatie over hoe ondersteuning voor geïntegreerde trefwoorden (START, STOP en UNSTOP) werkt voor SMS:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
