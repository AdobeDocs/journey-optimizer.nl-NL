---
title: Aan de slag met de prestaties
description: Richtlijnen voor leverbaarheid leren
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: ad1aadd8b10b05d96ee0de5988d82728aca57d5e
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 0%

---

# Aan de slag met de prestaties {#manage-deliverability}

Leverbaarheid is een maatstaf voor het succes van uw leveringen die uw ontvangers in postvakken bereiken.

**E-maillevering** verwijst naar de reeks eigenschappen die de capaciteit van een bericht bepalen om zijn bestemming, via een persoonlijk e-mailadres, binnen een korte tijd, en met de verwachte kwaliteit in termen van inhoud en formaat te bereiken. Deze kenmerken vallen in vier hoofdcategorieën: gegevenskwaliteit, bericht en inhoud, verzendende infrastructuur, en reputatie. Samen vormen ze de basis voor een succesvol e-mailprogramma.

De **leveringspercentage** is het aantal berichten die de inboxes van de ontvangers in vergelijking met het aantal berichten raakten die werden geleverd. Het hangt af van talrijke factoren, met name:

* Beperkte spamklachten
* Lage harde stuittarieven
* Kwaliteit van de beoogde adressen
* Berichtinhoud
* Afzender

Om de leverbaarheid van uw [!DNL Journey Optimizer] We raden u aan de beste praktijken in deze sectie te gebruiken. De problemen van de levering zijn over het algemeen verbonden met bescherming tegen spam die door de dienstverleners van Internet (ISPs) en de beheerders van de postserver wordt uitgevoerd.

Voor een diepgaander inzicht in wat de te leveren prestaties zijn en meer te leren over zeer belangrijke leverbaarheidsvoorwaarden, concepten, en benaderingen, verwijs naar [Adobe Handleiding voor beste praktijken voor aflevering](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=nl){target=&quot;_blank&quot;}.

## Het klachtenpercentage verlagen {#reduce-complaint-rate}

ISPs heeft gewoonlijk een duidelijk middel om een ontvangen bericht als spam te melden. Hierdoor kunnen onbetrouwbare bronnen worden geïdentificeerd. Door opting-out verzoeken snel na te leven en daarom te tonen dat u een betrouwbare afzender bent, kunt u klachtentarieven verminderen. [Meer informatie over beheer van opt-out](../messages/consent.md#opt-out-management).

Als algemene regel geldt dat u ontvangers die zich willen afmelden, niet in de weg wilt staan door van hen te verlangen dat ze bijvoorbeeld velden invullen zoals hun e-mailadres of naam. De landingspagina voor abonnementen mag slechts één validatieknop hebben.

Extra zorg betalen wanneer om extra bevestiging wordt gevraagd: een gebruiker kan twee e-mailadressen naar hetzelfde vak hebben omgeleid (bijvoorbeeld: firstname.lastname@club.com en firstname.lastname@internet-club.com). Als het profiel alleen het eerste adres kan onthouden en het abonnement wil opzeggen via een bericht dat naar het andere wordt verzonden, wordt dit door het formulier geweigerd omdat de gecodeerde id en het ingevoerde e-mailadres niet overeenkomen.

## Overzichtsonderdrukkingslijsten {#suppression-lists}

[!DNL Journey Optimizer] beheert een onderdrukkingslijst die spamklachten, harde stuit, en zachte stuitingen verzamelt die consequent voorkomen.

Om uw leverbaarheid te beschermen, worden de ontvangers waarvan adressen op de suppressielijst zijn uitgesloten door gebrek van alle toekomstige leveringen, omdat het verzenden naar deze contacten uw verzendende reputatie zou kunnen beschadigen.

[Meer informatie over de lijst met onderdrukking](suppression-list.md).

## Gereedschappen voor bewaking gebruiken {#monitoring-tools}

De functies van [!DNL Journey Optimizer] om de prestaties te controleren.

De **[!UICONTROL Executions]** kunt u met behulp van een set realtime-indicatoren controleren hoe uw leveringen presteren. Dit tabblad geeft onder andere het volgende weer:
* Het aantal berichten dat met succes wordt uitgevoerd, verzonden en geleverd.
* Het aantal berichten dat is geopend en het aantal berichten/verbindingen dat is geklikt.

## Berichtinhoud aanpassen {#adapt-message-content}

In mindere mate kan de inhoud van bepaalde berichten worden gedetecteerd als spam.

Volg onderstaande principes bij het ontwerpen van de inhoud van uw bericht om de afleverbaarheid te verbeteren en ervoor te zorgen dat de e-mails bij de ontvangers terechtkomen:

* **Naam en adres van de afzender**: Het adres moet de afzender uitdrukkelijk identificeren. Het domein moet eigendom zijn van en geregistreerd zijn bij de afzender. Het domeinregister mag niet worden geprivatiseerd.

* **Koppeling en bestemmingspagina opzeggen**: De afmeldingslink is essentieel. Het formulier moet zichtbaar en geldig zijn en moet functioneel zijn.

[Meer informatie over het ontwerpen van e-mailinhoud](../design/design-emails.md).

## Uw reputatie als afzender vaststellen

Als u onlangs naar een andere e-maildienstverlener, IP adres, of e-maildomein of subdomain bent verplaatst, moet u uw reputatie als afzender vestigen. Anders, zouden uw leveringen kunnen worden geblokkeerd of aan de spamomslag van de brievenbus van ontvangers worden verplaatst.

Om uw IP op te warmen, kunt u geleidelijk het aantal van uw leveringen opvoeren. Zie dit [use case](../building-journeys/ramp-up-deliveries-uc.md).
