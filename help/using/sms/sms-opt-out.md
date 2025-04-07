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
source-git-commit: 478706e893354d59be5d2010da84546aa4385d99
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Uitschakelen van beheer voor tekstberichten {#sms-opt-out}

In overeenstemming met de industriestandaarden en -voorschriften moeten alle SMS-marketingberichten een manier bevatten waarop de ontvangers hun abonnement gemakkelijk kunnen opzeggen. [ Leer meer op privacy &amp; opt-out beheer ](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Communicatie van tekstberichten kan afhankelijk van zijn aard, de plaats van waar u uw tekstberichten verzendt, en de plaats van uw ontvangers onderworpen zijn aan diverse wettelijke nalevingsvereisten. Terwijl Adobe Journey Optimizer de berichten over Korte codes, Lange codes en Gratis nummers afhandelt zoals hieronder beschreven, raadpleegt u uw juridische adviseur om ervoor te zorgen dat uw communicatie met tekstberichten voldoet aan alle toepasselijke wettelijke nalevingsvereisten.
>

## Oorspronkelijke binnenkomende trefwoorden {#sms-native-keywords}

>[!NOTE]
>
> Alleen Sinch en Infobip ondersteunen native trefwoorden bij gebruik met Journey Optimizer.

Adobe Journey Optimizer verwerkt standaard de volgende standaardantwoordberichten in de Engelse taal voor korte codes, gratis berichten en berichten met lange code:

* **Opt-uit**: STOP, SLUIT, ANNULEREN, EINDE, ONABONNEMENT, GEEN.
* **Opt-binnen**: ABONNEMENT, JA, ONOPLOSSEN, BEGINNEN, DOORGAAN, HERVATTEN, BEGINNEN.
* **Hulp**: HELP.

Deze trefwoorden activeren doorgaans een automatische standaardreactie van uw externe provider. U kunt dit rechtstreeks bij uw provider of via de documentatiesite bevestigen.

Wanneer het gebruiken van Infobip, zorg ervoor dat de het Door:sturen actie aan de configuratie van de Trek wordt geplaatst.

Er zijn geen stappen vereist om ervoor te zorgen dat de mogelijkheden voor SMS-opt-out in Adobe Journey Optimizer werken als de trefwoordreacties STOP, UNSTOP, START, QUIT, CANCEL, END en UNSUBSCRIBE automatisch worden herkend. De status van de optie om profielen te weigeren wordt in real time bijgewerkt in Adobe Journey Optimizer.

Merk op dat als een klant STOP aan een tekstbericht antwoordt, de leverancier al verder SMS van die specifieke afzenderidentiteitskaart (korte code of lang aantal), met inbegrip van transactionele berichten blokkeert. Om ononderbroken levering van transactieSMS te verzekeren, gebruik een afzonderlijke afzender identiteitskaart die niet eerder uit is gekozen.

## Lijsten van gewezen personen {#sms-blocklists}

Naast het tegenhouden van Adobe Journey Optimizer verzendt op basis van de opt-out status (voor directe integratie met Twilio, Infobip, of Sinch), handhaven de meeste gatewayproviders van SMS ook een lijst van gewezen personen die u ervoor zorgt dat geen SMS-bericht wordt geleverd aan een individu dat ervoor heeft gekozen om te weigeren. Als u een leverancier buiten Sinch of Twilio gebruikt, en een SMS via [ douanekanaal ](../building-journeys/using-custom-actions.md) verzendt, moet u dit met uw leverancier bevestigen.


## Korte codes {#short-codes}

Standaard worden opt-in- of Help-trefwoorden voor korte codenummers niet door Adobe Journey Optimizer afgehandeld. Om naleving van de industrieregels en regels voor opt-out behandeling te verzekeren, is het essentieel om te verifiëren dat uw korte code aan alle richtlijnen voldoet.

Journey Optimizer biedt echter wel ondersteuning voor wereldwijde opt-outs op basis van binnenkomende trefwoorden met verschillende verzender-id&#39;s.

## Alfanumerieke afzender-id {#alphanumeric}

Alfanumerieke identiteitskaart van de Afzender is slechts voor unidirectioneel overseinen, en kan binnenkomende berichten niet ontvangen. Als gevolg hiervan zijn Adobe Journey Optimizer Sender ID&#39;s niet van toepassing op SMS STOP, START en HELP. U moet andere instructies verstrekken, zoals het schrijven aan het team van de Steun, het roepen van een de telefoonlijn van de Steun, of het sms&#39;en van een ander telefoonaantal of code om gebruikers toe te staan om van berichten te kiezen die via Alphanumeric identiteitskaart van de Afzender worden verzonden.

## Video {#video-sms}

* In de onderstaande video leert u hoe u dubbele aanmelding voor SMS kunt configureren.

+++ Zie video

  >[!VIDEO](https://video.tv.adobe.com/v/3427129/?learn=on)

+++
