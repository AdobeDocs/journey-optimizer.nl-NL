---
solution: Journey Optimizer
product: journey optimizer
title: SMS-opt-out-beheer
description: Meer informatie over het beheren van opt-out met SMS-berichten
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# SMS-opt-out-beheer {#sms-opt-out}

In overeenstemming met de industriestandaarden en -voorschriften moeten alle SMS-marketingberichten een manier bevatten waarop de ontvangers hun abonnement gemakkelijk kunnen opzeggen. [Meer informatie over privacy- en opt-outbeheer](../privacy/opt-out.md)

Adobe Journey Optimizer verwerkt standaard standaardantwoordberichten in de Engelse taal, zoals STOP, UNSTOP en START voor berichten met de gratis en lange code, in overeenstemming met industriestandaarden voor native integratie, zoals Sinch en Twilio. Deze trefwoorden activeren doorgaans een automatisch standaardantwoord van uw externe provider (bijvoorbeeld Twilio, Sinch, enz.). U kunt dit rechtstreeks bij uw provider of via de documentatiesite bevestigen.

Er zijn geen stappen vereist om ervoor te zorgen dat de mogelijkheden voor SMS-opt-out in Adobe Journey Optimizer werken. De trefwoordreacties STOP, UNSTOP en START worden dan automatisch herkend.

Naast het stoppen van de verzending door Adobe Journey Optimizer op basis van de opt-out status (voor directe integratie met Twilio of Sinch), handhaven de meeste leveranciers van de gateway van SMS ook een lijst van gewezen personen ervoor zorgt dat geen SMS bericht zal worden geleverd aan een individu dat heeft gekozen om te weigeren. Als u een andere provider dan Sinch of Twilio gebruikt en een SMS verzendt via [aangepast kanaal](../building-journeys/using-custom-actions.md)moet u dit bevestigen met uw provider.

>[!IMPORTANT]
>
>Voor campagnes voor tekstberichten kunnen verschillende wettelijke nalevingsvereisten gelden, afhankelijk van de aard van uw campagne voor tekstberichten, de locatie vanwaar u uw tekstberichten verzendt en de locatie van uw ontvangers. <br>Hoewel Adobe Journey Optimizer de berichten over lange codes en gratis nummers zal afhandelen zoals hierboven beschreven, dient u uw juridische adviseur te raadplegen om ervoor te zorgen dat uw campagne voor tekstberichten voldoet aan alle toepasselijke wettelijke nalevingsvereisten.

## Korte codes {#short-codes}

Adobe Journey Optimizer verwerkt standaard geen opt-out-, opt-in- of Help-trefwoorden voor korte codenummers.

U moet ervoor zorgen dat uw korte code aan alle industrieregels en verordeningen voor opt-out behandeling voldoet.

## Alfanumerieke afzender-id {#alphanumeric}

Alfanumerieke identiteitskaart van de Afzender is slechts voor unidirectioneel overseinen, en kan binnenkomende berichten niet ontvangen. Als gevolg hiervan zijn de SMS STOP, START, HELP-trefwoorden van Adobe Journey Optimizer niet van toepassing op Alfa-verzender-id&#39;s. U moet andere instructies verstrekken, zoals het schrijven aan het team van de Steun, het roepen van een de telefoonlijn van de Steun, of het sms&#39;en van een ander telefoonaantal of code om gebruikers toe te staan om van berichten te kiezen die via Alphanumeric identiteitskaart van de Afzender worden verzonden.

## Video {#video-sms}

Raadpleeg de volgende video voor meer informatie over hoe ondersteuning voor geïntegreerde trefwoorden (START, STOP en UNSTOP) werkt voor SMS:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
