---
solution: Journey Optimizer
product: journey optimizer
title: Uitschakelen van beheer voor tekstberichten
description: Meer informatie over het beheren van opt-out met SMS/MMS-berichten
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: be758a577dbff2ae400d0642f9e898b423353f90
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Uitschakelen van beheer voor tekstberichten {#sms-opt-out}

In overeenstemming met de industriestandaarden en -voorschriften moeten alle SMS-marketingberichten een manier bevatten waarop de ontvangers hun abonnement gemakkelijk kunnen opzeggen. [Meer informatie over privacy- en opt-outbeheer](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Communicatie van tekstberichten kan afhankelijk van zijn aard, de plaats van waar u uw tekstberichten verzendt, en de plaats van uw ontvangers onderworpen zijn aan diverse wettelijke nalevingsvereisten. Terwijl Adobe Journey Optimizer de berichten over Korte codes, Lange codes en Gratis nummers afhandelt zoals hieronder beschreven, raadpleegt u uw juridische adviseur om ervoor te zorgen dat uw communicatie met tekstberichten voldoet aan alle toepasselijke wettelijke nalevingsvereisten.
>

## Oorspronkelijke binnenkomende trefwoorden {#sms-native-keywords}

>[!NOTE]
>
> Alleen Sinch en Infobip ondersteunen native trefwoorden bij gebruik met Journey Optimizer.

Adobe Journey Optimizer verwerkt standaard de volgende standaardantwoordberichten in de Engelse taal voor korte codes, gratis berichten en berichten met lange code:

* **Uitschakelen**: STOP, QUIT, CANCEL, END, UNABSCRIBE, NO.
* **Inschakelen**: ABONNEMENT, JA, ONSTOP, START, DOORGAAN, HERVATTEN, BEGINNEN.
* **Help**: HELP.

Deze trefwoorden activeren doorgaans een automatische standaardreactie van uw externe provider. U kunt dit rechtstreeks bij uw provider of via de documentatiesite bevestigen.

Wanneer het gebruiken van Infobip, zorg ervoor dat de het Door:sturen actie aan de configuratie van de Trek wordt geplaatst.

Er zijn geen stappen vereist om ervoor te zorgen dat de mogelijkheden voor SMS-opt-out in Adobe Journey Optimizer werken als de trefwoordreacties STOP, UNSTOP, START, QUIT, CANCEL, END en UNSUBSCRIBE automatisch worden herkend. De status van de optie om profielen te weigeren wordt in real time bijgewerkt in Adobe Journey Optimizer.


## Lijsten van gewezen personen {#sms-blocklists}

Naast het tegenhouden van Adobe Journey Optimizer verzendt op basis van de opt-out status (voor directe integratie met Twilio, Infobip, of Sinch), handhaven de meeste gatewayproviders van SMS ook een lijst van gewezen personen die u ervoor zorgt dat geen SMS-bericht wordt geleverd aan een individu dat ervoor heeft gekozen om te weigeren. Als u een andere provider dan Sinch of Twilio gebruikt en een SMS-bericht verzendt via [aangepast kanaal](../building-journeys/using-custom-actions.md)moet u dit bevestigen met uw provider.


## Korte codes {#short-codes}

Standaard worden opt-in- of Help-trefwoorden voor korte codenummers niet door Adobe Journey Optimizer afgehandeld. Om naleving van de industrieregels en regels voor opt-out behandeling te verzekeren, is het essentieel om te verifiëren dat uw korte code aan alle richtlijnen voldoet.

Journey Optimizer biedt echter wel ondersteuning voor wereldwijde opt-outs op basis van binnenkomende trefwoorden met verschillende verzender-id&#39;s.

## Alfanumerieke afzender-id {#alphanumeric}

Alfanumerieke identiteitskaart van de Afzender is slechts voor unidirectioneel overseinen, en kan binnenkomende berichten niet ontvangen. Dientengevolge, START van het SMS van Adobe Journey Optimizer, de sleutelwoorden van HELP zijn niet van toepassing voor de Afzender IDs van de Alpha. U moet andere instructies verstrekken, zoals het schrijven aan het team van de Steun, het roepen van een de telefoonlijn van de Steun, of het sms&#39;en van een ander telefoonaantal of code om gebruikers toe te staan om van berichten te kiezen die via Alphanumeric identiteitskaart van de Afzender worden verzonden.

## Video {#video-sms}

* In de onderstaande video ziet u hoe native ondersteuning voor inkomende trefwoorden (START, STOP en UNSTOP) werkt voor SMS.

+++ Zie video

  >[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)

+++

* In de onderstaande video leert u hoe u dubbele aanmelding voor SMS kunt configureren.

+++ Zie video

  >[!VIDEO](https://video.tv.adobe.com/v/3427129/?learn=on)

+++
