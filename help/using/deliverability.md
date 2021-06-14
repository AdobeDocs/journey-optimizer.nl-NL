---
title: Uitvoering van controleberichten
description: Meer informatie over richtlijnen voor bewaking en levering
feature: Leverbaarheid
topic: Contentmanagement
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Te leveren {#manage-deliverability} beheren

![](assets/do-not-localize/badge.png)

Leverbaarheid is een maatstaf voor het succes van uw leveringen die uw ontvangers in postvakken bereiken.

**De e-** mailleverbaarheid verwijst naar de reeks eigenschappen die de capaciteit van een bericht bepalen om zijn bestemming, via een persoonlijk e-mailadres, binnen een korte tijd, en met de verwachte kwaliteit in termen van inhoud en formaat te bereiken. Deze kenmerken vallen in vier hoofdcategorieën: gegevenskwaliteit, bericht en inhoud, verzendende infrastructuur, en reputatie. Samen vormen ze de basis voor een succesvol e-mailprogramma.

Het **leverbaarheidstarief** is het aantal berichten die de brievenbussen van de ontvangers vergeleken bij het aantal berichten raakten die werden geleverd. Het hangt af van talrijke factoren, met name:

* Beperkte spamklachten
* Lage harde stuittarieven
* Kwaliteit van de beoogde adressen
* Berichtinhoud
* Afzender

Om de leverbaarheid van uw [!DNL Journey Optimizer] ervaringen te optimaliseren, adviseren wij het gebruiken van de beste praktijken die in deze sectie worden vermeld. De problemen van de levering zijn over het algemeen verbonden met bescherming tegen spam die door de dienstverleners van Internet (ISPs) en de beheerders van de postserver wordt uitgevoerd.

## Reduceer het klachtenpercentage {#reduce-complaint-rate}

ISPs heeft gewoonlijk een duidelijk middel om een ontvangen bericht als spam te melden. Hierdoor kunnen onbetrouwbare bronnen worden geïdentificeerd. Door opting-out verzoeken snel na te leven en daarom te tonen dat u een betrouwbare afzender bent, kunt u klachtentarieven verminderen. [Meer weten over opt-outbeheer](consent.md#opt-out-management)?

Als algemene regel geldt dat u ontvangers die zich willen afmelden, niet in de weg wilt staan door van hen te verlangen dat ze bijvoorbeeld velden invullen zoals hun e-mailadres of naam. De landingspagina voor abonnementen mag slechts één validatieknop hebben.

Extra zorg betalen wanneer om extra bevestiging wordt gevraagd: een gebruiker kan twee e-mailadressen naar hetzelfde vak hebben omgeleid (bijvoorbeeld: firstname.lastname@club.com en firstname.lastname@internet-club.com). Als het profiel alleen het eerste adres kan onthouden en het abonnement wil opzeggen via een bericht dat naar het andere wordt verzonden, wordt dit door het formulier geweigerd omdat de gecodeerde id en het ingevoerde e-mailadres niet overeenkomen.

## Leveringsonderdrukkingslijsten {#suppression-lists}

[!DNL Journey Optimizer] beheert een onderdrukkingslijst die spamklachten, harde stuit, en zachte stuitingen verzamelt die consequent voorkomen.

Om uw leverbaarheid te beschermen, worden de ontvangers waarvan adressen op de suppressielijst zijn uitgesloten door gebrek van alle toekomstige leveringen, omdat het verzenden naar deze contacten uw verzendende reputatie zou kunnen beschadigen.

[Meer informatie over de lijst](suppression-list.md) met onderdrukking vindt u.

## Monitoringtools gebruiken {#monitoring-tools}

Gebruik de functies die worden aangeboden door [!DNL Journey Optimizer] om de prestaties te controleren.

Met het tabblad **[!UICONTROL Executions]** van de berichtenlijst kunt u controleren hoe uw leveringen in real-time worden uitgevoerd. Dit tabblad geeft onder andere het volgende weer:
* Het aantal berichten dat met succes wordt uitgevoerd, verzonden en geleverd.
* Het aantal berichten dat is geopend en het aantal berichten/verbindingen dat is geklikt.

[Meer weten over het controleren van de uitvoering](message-monitoring.md) van berichten?

## Berichtinhoud {#adapt-message-content} aanpassen

In mindere mate kan de inhoud van bepaalde berichten worden gedetecteerd als spam.

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

Volg onderstaande principes bij het ontwerpen van de inhoud van uw bericht om de afleverbaarheid te verbeteren en ervoor te zorgen dat de e-mails bij de ontvangers terechtkomen:

* **Naam en adres** van de afzender: Het adres moet de afzender uitdrukkelijk identificeren. Het domein moet eigendom zijn van en geregistreerd zijn bij de afzender. Het domeinregister mag niet worden geprivatiseerd.

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **Koppeling en bestemmingspagina** afmelden: De afmeldingslink is essentieel. Het formulier moet zichtbaar en geldig zijn en moet functioneel zijn.

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[Meer informatie over het ontwerpen van e-mailinhoud](design-emails.md).
