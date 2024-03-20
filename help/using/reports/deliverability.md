---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met de prestaties
description: Richtlijnen voor leverbaarheid leren
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 0%

---

# Aan de slag met de prestaties {#manage-deliverability}

Leverbaarheid is een maatstaf voor het succes van uw leveringen die uw ontvangers in postvakken bereiken.

>[!NOTE]
>
>Voor klanten die een vergunning geven voor het Gezondheidsschild, gebruikt de Adobe de Veiligheid van de Laag van het Vervoer (TLS) 1.2 om de gegevensuitwisseling tussen gebruikerssystemen (ontvangers) en Journey Optimizer (afzender) te beveiligen. Als de ontvangende mailserver geen ondersteuning biedt voor TLS 1.2, kunnen klanten problemen ondervinden met de te leveren items, zoals het terugsturen van e-mailberichten naar de oorspronkelijke afzender.

**E-maillevering** verwijst naar de reeks eigenschappen die de capaciteit van een bericht bepalen om zijn bestemming, via een persoonlijk e-mailadres, binnen een korte tijd, en met de verwachte kwaliteit in termen van inhoud en formaat te bereiken. Deze kenmerken vallen in vier hoofdcategorieën: gegevenskwaliteit, bericht en inhoud, verzendende infrastructuur, en reputatie. Samen vormen ze de basis voor een succesvol e-mailprogramma.

De **leveringspercentage** is het aantal berichten die de inboxes van de ontvangers in vergelijking met het aantal berichten raakten die werden geleverd. Het hangt af van talrijke factoren, met name:

* Beperkte spamklachten
* Lage harde stuittarieven
* Kwaliteit van de beoogde adressen
* Berichtinhoud
* Afzender

Om de leverbaarheid van uw [!DNL Journey Optimizer] We raden u aan de beste praktijken in deze sectie te gebruiken. De problemen van de levering zijn over het algemeen verbonden met bescherming tegen spam die door de dienstverleners van Internet (ISPs) en de beheerders van de postserver wordt uitgevoerd.

Voor een diepgaander inzicht in wat de te leveren prestaties zijn en meer te leren over zeer belangrijke leverbaarheidsvoorwaarden, concepten, en benaderingen, verwijs naar [Handleiding voor beste praktijken bij de levering van Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=nl){target="_blank"}.

## Het klachtenpercentage verlagen {#reduce-complaint-rate}

ISPs heeft gewoonlijk een duidelijk middel om een ontvangen bericht als spam te melden. Hierdoor kunnen onbetrouwbare bronnen worden geïdentificeerd. Door opting-out verzoeken snel na te leven en daarom te tonen dat u een betrouwbare afzender bent, kunt u klachtentarieven verminderen. [Meer informatie over beheer van opt-out](../privacy/opt-out.md#opt-out-management)

Als algemene regel geldt dat u ontvangers die zich willen afmelden, niet in de weg wilt staan door van hen te verlangen dat ze bijvoorbeeld velden invullen zoals hun e-mailadres of naam. De landingspagina voor abonnementen mag slechts één validatieknop hebben.

Wees voorzichtig met het aanvragen van aanvullende bevestiging: een gebruiker kan twee e-mailadressen hebben die naar hetzelfde vak worden omgeleid (bijvoorbeeld: firstname.lastname@club.com en firstname.lastname@internet-club.com). Als het profiel alleen het eerste adres kan onthouden en het abonnement wil opzeggen via een bericht dat naar het andere wordt verzonden, wordt dit door het formulier geweigerd omdat de gecodeerde id en het ingevoerde e-mailadres niet overeenkomen.

## Overzichtsonderdrukkingslijsten {#suppression-lists}

[!DNL Journey Optimizer] beheert een onderdrukkingslijst die spamklachten, harde stuitingen, en zachte stuitingen verzamelt die consequent voorkomen.

Om uw leverbaarheid te beschermen, worden de ontvangers van wie adressen op de suppressielijst zijn uitgesloten door gebrek van alle toekomstige leveringen, omdat het verzenden naar deze contacten uw verzendende reputatie zou kunnen beschadigen.

[Meer informatie over de lijst met onderdrukking](suppression-list.md)

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

[Meer informatie over het ontwerpen van e-mailinhoud](../email/get-started-email-design.md)

## Uw reputatie als afzender vaststellen {#reputation}

Als u onlangs naar een andere e-maildienstverlener, IP adres, of e-maildomein of subdomain bent verplaatst, moet u uw reputatie als afzender vestigen. Anders, zouden uw leveringen kunnen worden geblokkeerd of aan de spamomslag van de brievenbus van ontvangers worden verplaatst.

Om uw IP op te warmen, kunt u geleidelijk het aantal van uw leveringen opvoeren. Meer informatie in deze [use case](../building-journeys/ramp-up-deliveries-uc.md).

## DMARC implementeren {#dmarc}

Om u te helpen het risico verlichten dat legitieme e-mails als spam of verworpen worden gemarkeerd, en leveringsproblemen te verhinderen, [!DNL Journey Optimizer] staat u aan opstellingsDMARC verslag voor alle subdomeinen toe die u aan Adobe delegeert.

De op domein-gebaseerde Authentificatie van het Bericht, het Melden, en de Conformiteit (DMARC) is een methode van de e-mailauthentificatie die domeineigenaars toestaat om hun domein tegen onbevoegd gebruik door kwaadwillige actoren te beschermen.

[Meer informatie over DMARC-record](../configuration/dmarc-record.md)

## Informatie over feedbackloops {#feedback-loops}

Een terugkoppel lijn (FBL) is de dienst die door sommige ISPs wordt aangeboden die de e-mailafzender toestaat om automatisch op de hoogte te worden gebracht wanneer de gebruiker die een e-mail ontvangt verkiest om het als spam (ook als &quot;klacht&quot;wordt bekend) te merken.

Nadat een eindgebruiker een klacht produceert die naar Adobe door ISP wordt teruggestuurd, wordt het e-mailadres automatisch toegevoegd aan [onderdrukkingslijst](../reports/suppression-list.md) en uitgesloten van toekomstige leveringen. Het verzenden van e-mails naar gebruikers die deze als spam hebben gemarkeerd, heeft een negatieve invloed op de reputatie van de afzender en kan problemen met de leverbaarheid veroorzaken. [Meer informatie over spamklachten](../reports/suppression-list.md#spam-complaints)

>[!IMPORTANT]
>
>Niet alle ISPs verstrekt traditionele FBL, zoals Gmail. Gmail biedt geen feedback op individueel niveau en kan niet worden gebruikt om spamklachten bij individuele ontvangers bij te houden, in plaats daarvan de nadruk te leggen op rapportage op geaggregeerd niveau binnen hun Google Postmaster Tools. [Meer informatie](https://support.google.com/a/answer/6254652?hl=en){target="_blank"}

Alle klanten van de Adobe worden automatisch ingeschreven in traditionele FBLs van volgende ISPs:

* 1&amp;1

* AOL

* BlueTie

* Comcast

* Fastmail

* Gandi

* Italia Online

* La Poste

* Liberty Global (Chello, UPC, Unity Media)

* Locaweb

* Mail.RU

* Microsoft

* OpenSRS

* Rackruimte

* SEZNM

* SFR

* SilverSky

* Swisscom

* Synacor

* Telecom Italia

* Telenet

* Telenor

* Telstra

* Terra

* UOL

* Virgin Media

* Yahoo

* Ziggo

De Adobe controleert deze FOL&#39;s regelmatig om ervoor te zorgen dat de recentste beschikbare FOL&#39;s worden toegevoegd.
