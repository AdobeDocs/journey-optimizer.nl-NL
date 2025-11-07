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
source-git-commit: 6023f1004c74cedc7567fd142be767b12d85ba6d
workflow-type: tm+mt
source-wordcount: '1138'
ht-degree: 0%

---

# Aan de slag met de prestaties {#manage-deliverability}

Leverbaarheid is een maatstaf voor het succes van uw leveringen die uw ontvangers in postvakken bereiken.

>[!NOTE]
>
>Voor klanten die een vergunning geven voor het Gezondheidsschild, gebruikt Adobe Transport Layer Security (TLS) 1.2 om de gegevensuitwisseling tussen gebruikerssystemen (ontvangers) en Journey Optimizer (afzender) te beveiligen. Als de ontvangende mailserver geen ondersteuning biedt voor TLS 1.2, kunnen klanten problemen ondervinden met de te leveren items, zoals het terugsturen van e-mailberichten naar de oorspronkelijke afzender.

**E-mailleverbaarheid** verwijst naar de reeks kenmerken die de capaciteit van een bericht bepalen om zijn bestemming, via een persoonlijk e-mailadres, binnen een korte tijd, en met de verwachte kwaliteit in termen van inhoud en formaat te bereiken. Deze kenmerken vallen in vier hoofdcategorieën: gegevenskwaliteit, bericht en inhoud, verzendende infrastructuur, en reputatie. Samen vormen ze de basis voor een succesvol e-mailprogramma.

Het **leverbaarheidstarief** is het aantal berichten die de inboxes van ontvangers vergeleken met het aantal berichten raken die werden geleverd. Het hangt af van talrijke factoren, met name:

* Beperkte spamklachten
* Lage harde stuittarieven
* Kwaliteit van de beoogde adressen
* Berichtinhoud
* Afzender

Om de leverbaarheid van uw [!DNL Journey Optimizer] -ervaringen te optimaliseren, raden we u aan de best practices in deze sectie te gebruiken. De problemen van de levering zijn over het algemeen verbonden met bescherming tegen spam die door de dienstverleners van Internet (ISPs) en de beheerders van de postserver wordt uitgevoerd.

Voor een diepere duik op wat de leverbaarheid is en meer op zeer belangrijke leveringsvoorwaarden, concepten, en benaderingen te leren, verwijs naar de [&#x200B; Gids van de Beste praktijken van de Levering van Adobe &#x200B;](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=nl){target="_blank"}.

## Het klachtenpercentage verlagen {#reduce-complaint-rate}

ISPs heeft gewoonlijk een duidelijk middel om een ontvangen bericht als spam te melden. Hierdoor kunnen onbetrouwbare bronnen worden geïdentificeerd. Door opting-out verzoeken snel na te leven en daarom te tonen dat u een betrouwbare afzender bent, kunt u klachtentarieven verminderen. [&#x200B; leer meer over opt-out beheer &#x200B;](../privacy/opt-out.md#opt-out-management)

Als algemene regel geldt dat u ontvangers die zich willen afmelden, niet in de weg wilt staan door van hen te verlangen dat ze bijvoorbeeld velden invullen zoals hun e-mailadres of naam. De landingspagina voor abonnementen mag slechts één validatieknop hebben.

Wees voorzichtig met het aanvragen van aanvullende bevestiging: een gebruiker kan twee e-mailadressen hebben die naar hetzelfde vak worden omgeleid (bijvoorbeeld: firstname.lastname@club.com en firstname.lastname@internet-club.com). Als het profiel alleen het eerste adres kan onthouden en het abonnement wil opzeggen via een bericht dat naar het andere wordt verzonden, wordt dit door het formulier geweigerd omdat de gecodeerde id en het ingevoerde e-mailadres niet overeenkomen.

## Overzichtsonderdrukkingslijsten {#suppression-lists}

[!DNL Journey Optimizer] beheert een suppressielijst die spamklachten, harde stuit en zachte stuitingen verzamelt die consistent voorkomen.

Om uw leverbaarheid te beschermen, worden de ontvangers van wie adressen op de suppressielijst zijn uitgesloten door gebrek van alle toekomstige leveringen, omdat het verzenden naar deze contacten uw verzendende reputatie zou kunnen beschadigen.

[Meer informatie over de lijst met onderdrukking](suppression-list.md)

## Gereedschappen voor bewaking gebruiken {#monitoring-tools}

Gebruik de rapportfuncties die [!DNL Journey Optimizer] aanbiedt om de prestaties te controleren.

Met de campagne- en reisrapporten kunt u controleren hoe uw leveringen presteren aan de hand van een reeks realtime-indicatoren. Ze geven onder andere het volgende weer:

* Het aantal berichten dat met succes wordt uitgevoerd, verzonden en geleverd.
* Het aantal berichten dat is geopend en het aantal berichten/verbindingen dat is geklikt.

Leer meer over [&#x200B; levend rapport &#x200B;](../reports/live-report.md) en [&#x200B; al tijdrapport &#x200B;](../reports/report-gs-cja.md)

## Berichtinhoud aanpassen {#adapt-message-content}

In mindere mate kan de inhoud van bepaalde berichten worden gedetecteerd als spam.

Volg onderstaande principes bij het ontwerpen van de inhoud van uw bericht om de afleverbaarheid te verbeteren en ervoor te zorgen dat de e-mails bij de ontvangers terechtkomen:

* **de naam en het adres van de afzender**: Het adres moet de afzender uitdrukkelijk identificeren. Het domein moet eigendom zijn van en geregistreerd zijn bij de afzender. Het domeinregister mag niet worden geprivatiseerd.

* **Unsubscribe verbinding en het landen pagina**: De unsubscribe verbinding is essentieel. Het formulier moet zichtbaar en geldig zijn en moet functioneel zijn.

[Meer informatie over het ontwerpen van e-mailinhoud](../email/get-started-email-design.md)

## Uw reputatie als afzender vaststellen {#reputation}

Als u onlangs naar een andere e-maildienstverlener, IP adres, of e-maildomein of subdomain bent verplaatst, moet u uw reputatie als afzender vestigen. Anders, zouden uw leveringen kunnen worden geblokkeerd of aan de spamomslag van de brievenbus van ontvangers worden verplaatst.

Wanneer het verzenden van e-mail op een gloednieuw IP adres, kunt u IP warmteopwerkschema&#39;s nu gemakkelijk rechtstreeks van het gebruikersinterface uitvoeren.

Adobe Journey Optimizer biedt een gestandaardiseerde en efficiënte manier om uw IP adressen op te warmen die de beste praktijken voor optimale leverbaarheid volgen.

[Meer informatie over IP-opwarmingsplannen](../configuration/ip-warmup-gs.md)

<!--To warm up your IP, you can gradually ramp up the number of your deliveries. Learn more in this [use case](../building-journeys/ramp-up-deliveries-uc.md).-->

## DMARC implementeren {#dmarc}

Met [!DNL Journey Optimizer] kunt u DMARC-records instellen voor alle subdomeinen die u aan Adobe delegeert, zodat u het risico kunt beperken dat legitieme e-mailberichten worden gemarkeerd als spam of afgewezen en dat leveringsproblemen worden voorkomen.

De op domein-gebaseerde Authentificatie van het Bericht, het Melden, en de Conformiteit (DMARC) is een methode van de e-mailauthentificatie die domeineigenaars toestaat om hun domein tegen onbevoegd gebruik door kwaadwillige actoren te beschermen.

[Meer informatie over DMARC-records](../configuration/dmarc-record.md)

## Informatie over feedbackloops {#feedback-loops}

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="Sommige subdomeinen zijn mogelijk niet beschikbaar"
>abstract="Bepaalde subdomeinen zijn momenteel niet beschikbaar voor selectie vanwege de registratie van de feedbacklus die in behandeling is. Dit proces kan tot 10 werkdagen duren. Na voltooiing kunt u kiezen uit alle beschikbare subdomeinen."
>additional-url="https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation" text="Aan de slag met subdomeindelegatie"

Een terugkoppel lijn (FBL) is de dienst die door sommige ISPs wordt aangeboden die de e-mailafzender toestaat om automatisch op de hoogte te worden gebracht wanneer de gebruiker die een e-mail ontvangt verkiest om het als spam (ook als &quot;klacht&quot;wordt bekend) te merken.

Nadat een eindgebruiker een klacht produceert die terug naar Adobe door ISP wordt verzonden, wordt het e-mailadres automatisch toegevoegd aan de [&#x200B; suppressielijst &#x200B;](../reports/suppression-list.md) en uitgesloten van toekomstige leveringen. Het verzenden van e-mails naar gebruikers die deze als spam hebben gemarkeerd, heeft een negatieve invloed op de reputatie van de afzender en kan problemen met de leverbaarheid veroorzaken. [&#x200B; Leer meer over spamklachten &#x200B;](../reports/suppression-list.md#spam-complaints)

>[!IMPORTANT]
>
>Niet alle ISPs verstrekt traditionele FBL, zoals Gmail. Gmail biedt geen feedback op individueel niveau en kan niet worden gebruikt om spamklachten bij individuele ontvangers bij te houden, in plaats daarvan de nadruk te leggen op rapportage op geaggregeerd niveau binnen hun Google Postmaster Tools. [Meer informatie](https://support.google.com/a/answer/6254652?hl=en){target="_blank"}

Alle klanten van Adobe worden automatisch ingeschreven in traditionele FBLs van volgende ISPs:

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

Adobe controleert deze FOL&#39;s regelmatig om ervoor te zorgen dat de recentste beschikbare FOL&#39;s worden toegevoegd.

## SMTP-relais gebruiken {#smtp-relay}

[!DNL Journey Optimizer] gebruikt MTA&#39;s (Mail Transfer Agents) en IP&#39;s die eigendom zijn van Adobe om uw e-mails aan internetserviceproviders (ISP&#39;s) te verzenden. In sommige gevallen wilt u echter wellicht de uiteindelijke e-mailleveringen doorsturen via uw eigen MTA&#39;s en IP&#39;s, of wilt u definitieve validaties uitvoeren op de e-mails voordat u deze naar uw ontvangers verzendt.

In dit geval, kunt u verkiezen om uw e-mails te hebben die aan servers SMTP door uw organisatie worden gehost in plaats van rechtstreeks van Journey Optimizer naar ISPs worden verzonden.

>[!AVAILABILITY]
>
>De SMTP relaiscapaciteit is beschikbaar op bestelling - contacteer uw vertegenwoordiger van Adobe.
