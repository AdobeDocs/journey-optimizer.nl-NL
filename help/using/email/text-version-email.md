---
solution: Journey Optimizer
product: journey optimizer
title: De tekstversie van een e-mailbericht maken
description: Leer hoe u de tekstversie van een e-mailbericht maakt
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: text, email, version, plain, editor
exl-id: 4bb36810-65fb-4a9b-9bea-e56ed2c1eea3
source-git-commit: 30241f4504ad82bf8ef9f6b58d3bb9482f572dae
workflow-type: tm+mt
source-wordcount: '1031'
ht-degree: 0%

---

# De tekstversie van een e-mailbericht maken {#text-version-email}

U wordt aangeraden een tekstversie van de berichttekst te maken die wordt gebruikt wanneer HTML-inhoud niet kan worden weergegeven.

Standaard maakt de Designer-e-mail een **[!UICONTROL Plain text]** -versie van uw e-mail, inclusief personalisatievelden. Deze versie wordt automatisch gegenereerd en gesynchroniseerd met de HTML-versie van uw inhoud.

Als u liever een andere inhoud gebruikt voor de versie zonder opmaak, voert u de onderstaande stappen uit:

1. Selecteer het pictogram **[!UICONTROL Plain text]** in uw e-mail.

   ![](assets/text_version_3.png)

1. Schakel synchronisatie uit met de schakeloptie **[!UICONTROL Sync with HTML]** . Klik op het vinkje om uw keuze te bevestigen.

   ![](assets/text_version_2.png)

1. Vervolgens kunt u de versie zonder tekst naar wens bewerken.

>[!CAUTION]
>
> * Als synchronisatie is uitgeschakeld, worden wijzigingen die in de weergave **[!UICONTROL Plain text]** zijn aangebracht, niet weerspiegeld in de weergave HTML.
>
>* Als u de optie **[!UICONTROL Sync with HTML]** weer inschakelt nadat u de normale tekstinhoud hebt bijgewerkt, gaan de wijzigingen verloren en worden deze vervangen door tekstinhoud die uit de HTML-versie is gegenereerd.

## Wanneer moet u aangepaste standaardtekstversies gebruiken? {#when-to-use}

Als u precies begrijpt wanneer u een aangepaste versie voor normale tekst maakt in plaats van automatische synchronisatie, bent u verzekerd van een optimale e-maillevering en leesbaarheid.

### Gebruik aangepaste normale tekst (sync uitschakelen) wanneer:

* **Complexe lay-outs van HTML** - Uw e-mail van HTML omvat meerkolomlay-outs, lijsten, of complexe CSS die niet goed aan gewone teksten vertalen.
* **Visuele-zware inhoud** - Uw e-mail baseert zich zwaar op beelden, en u wilt beschrijvende tekstalternatieven voor beeld-gehandicapte cliënten verstrekken.
* **Verschillende overseinenstructuur** - u wilt een vereenvoudigde of gereorganiseerde berichtstructuur verstrekken die voor gewone tekstlezers wordt geoptimaliseerd.
* **de vereisten van de Toegankelijkheid** - u specifieke duidelijke tekst het formatteren nodig om aan toegankelijkheidsnormen te voldoen.
* **Verouderde e-mailcliënten** - Uw publiek omvat gebruikers op oudere e-mailcliënten (b.v., Vooruitzichten 2003, tekst-slechts mobiele cliënten) die speciaal geformatteerde inhoud vereisen.
* **ASCII het formatteren** - u specifiek duidelijk-tekst het formatteren zoals kunst ASCII, lijsten, of specifieke lijnonderbrekingen wilt omvatten.

### Automatische synchronisatie gebruiken (standaard) wanneer:

* **Eenvoudig ontwerp van HTML** - Uw e-mail van HTML heeft een eenvoudige, lineaire structuur die goed aan gewone teksten vertaalt.
* **Consistente inhoud** - u wilt nauwkeurige consistentie tussen HTML en gewone tekstversies handhaven.
* **de Frequente updates** - u werkt regelmatig e-mailinhoud bij en wilt handduplicatie vermijden.
* **Personalization werkt goed** - Uw verpersoonlijkingsgebieden functioneren behoorlijk in beide formaten.
* **beperkingen van de Tijd** - u moet e-mails zonder extra duidelijke tekstaanpassing snel lanceren.

## Praktische voorbeelden {#practical-examples}

In de volgende voorbeelden worden realistische scenario&#39;s getoond om u te helpen bij het kiezen of u aangepaste normale tekst of automatische synchronisatie wilt gebruiken. In elk voorbeeld worden de context, de aanbevolen aanpak en de motivering van het besluit uitgelegd.

+++Voorbeeld 1: nieuwsbrief met complexe lay-out op de markt brengen

**Scenario:** Meerdere-kolombulletin met beelden, gestileerde knopen, en kleur-gecodeerde secties.

![](assets/text_version_ex1.png)

**Aanbeveling:** Gebruik douane gewone teksten (maak synchronisatie onbruikbaar).

**waarom de douane gewone tekst:** de versie van HTML gebruikt een driekolomnetlay-out met bannerbeelden, gestileerde knopen, en kleur-gecodeerde secties. Deze visuele elementen vertalen niet goed naar normale tekst via automatische synchronisatie, wat leidt tot onoverzichtelijke, moeilijk leesbare inhoud. Met een aangepaste versie voor normale tekst kunt u de inhoud herstructureren in een lineaire, eenvoudig te scannen indeling met duidelijke sectiekoppen en correct opgemaakte koppelingen.

**Voorbeeld van de Onbewerkte tekst van de Douane:**

```
================================================
YOUR BRAND - MONTHLY NEWSLETTER
December 2025
================================================

🌟 FEATURED ARTICLE
"10 Ways to Optimize Your Customer Journeys"
Read more: https://example.com/articles/optimize-journeys

📢 UPCOMING WEBINAR
"Mastering Email Personalization"
December 15, 2025 at 2:00 PM EST
Register: https://example.com/webinar/register

📦 NEW PRODUCTS
- Winter Collection: https://example.com/winter
- Holiday Gift Guide: https://example.com/gifts

================================================
Website: https://example.com
Unsubscribe: https://example.com/unsubscribe
================================================
```

+++

+++Voorbeeld 2: bevestiging van de transactieorder

**Scenario:** de bevestiging van de orde met gestructureerde gegevens (orderaantal, punten, prijzen, verschepende details).

![](assets/text_version_ex2.png)

**Aanbeveling:** gebruik auto-synchronisatie.

**waarom de auto-synchronisatiewerken:** de bevestigingen van de Orde hebben een eenvoudige, lineaire structuur die van nature van HTML aan gewone teksten vertaalt. De informatiestromen logisch (orde details → punten → totalen → verzending), en verpersoonlijkingsgebieden zoals orderaantallen en klantennamen werken identiek in beide formaten. De gestructureerde, tabelgegevens worden naadloos geconverteerd zonder dat handmatige aanpassingen nodig zijn, zodat u tijd bespaart terwijl u helderheid behoudt.

+++

+++Voorbeeld 3: Uitnodiging voor gebeurtenis met rich media

**Scenario:** de uitnodiging van de gebeurtenis met achtergrondbeelden, ingebedde video&#39;s, en interactieve elementen.

![](assets/text_version_ex3.png)

**Aanbeveling:** Gebruik douane gewone teksten (maak synchronisatie onbruikbaar).

**waarom douane gewone tekst:** de versie van HTML baseert zich op visuele effect-achtergrond beelden, video sluit, en interactieve knopen RSVP in. Automatische synchronisatie verwijdert deze elementen uit elkaar, waardoor een verwarrende tekstversie overblijft van verbroken verwijzingen. Met een aangepaste versie voor normale tekst kunt u duidelijke gebeurtenisdetails, sprekersinformatie en directe registratiekoppelingen opgeven in een goed georganiseerde indeling die zonder visuele elementen werkt.

**Voorbeeld van de Onbewerkte tekst van de Douane:**

```
YOU'RE INVITED!
Annual Customer Summit 2025

📅 When: March 15-17, 2025
📍 Where: San Francisco Convention Center
         123 Market Street, San Francisco, CA

KEYNOTE SPEAKERS
- Jane Smith, CEO TechCorp: "The Future of Digital Marketing"
- John Doe, Chief Innovation Officer: "AI and Customer Experience"

REGISTER NOW: https://example.com/summit/register
Early bird discount ends February 1st

Full agenda: https://example.com/summit/agenda
Questions: events@example.com | 1-800-555-0123
```

+++

## Vaak voorkomende gebruiksscenario&#39;s {#common-use-cases}

In de volgende gebruiksgevallen ziet u situaties waarin het nuttig is een aangepaste versie voor normale tekst te maken (synchroniseren uitschakelen). Elk voorbeeld toont de uitdaging die door de versie van HTML wordt gesteld en hoe een oplossing van de douanekleurtekst het richt.

+++Kwestie 1 gebruiken: e-mails over productcatalogus

**Uitdaging:** HTML toont net van producten met beelden, prijzen, en koopknopen

**Onbewerkte tekstoplossing:** creeer een gestructureerde lijst met duidelijke productnamen, prijzen, en directe verbindingen

```
FEATURED PRODUCTS
=================

1. Premium Leather Wallet
   Price: $89.99
   View product: https://example.com/product/wallet
   
2. Designer Sunglasses
   Price: $129.99
   View product: https://example.com/product/sunglasses
```

+++

+++Hoofdlettergebruik 2: welkome e-mailreeks

**Uitdaging:** Gemarkeerde welkome-mail met bedrijfembleem en gestileerde het formatteren

**Onbewerkte tekstoplossing:** de kunst van ASCII van het Gebruik of tekst het formatteren om visuele hiërarchie tot stand te brengen

```
***************************************************
*                                                 *
*     WELCOME TO [BRAND NAME]                    *
*     We're thrilled to have you!                *
*                                                 *
***************************************************
```

+++

+++Kwestie 3 gebruiken: verzoek om een enquête of feedback

**Uitdaging:** HTML omvat gestileerde knopen en vormelementen

**Onbewerkte tekstoplossing:** verstrek duidelijke tekstverbindingen met instructies

```
We'd love your feedback!
------------------------

Please take 2 minutes to complete our survey:
https://example.com/survey/customer-feedback

Your input helps us improve our service.
```

+++

## Veelgestelde vragen {#faq}

**zal mijn verpersoonlijkingsgebieden in gewone teksten werken?**\
Ja, verpersoonlijkingsvelden zoals `{{profile.firstName}}` werken op dezelfde manier in zowel HTML- als normale tekstversies.

**hoe ik mijn gewone tekstversie test?**
* Schakel over naar de weergave **[!UICONTROL Plain text]** in de Designer-e-mail. [&#x200B; leer hoe &#x200B;](#text-version-email)
* Verzend teste-mailberichten naar e-mailclients met alleen tekst, zoals oude versies van Pine of mobiele e-mailapps met een standaardversie.

**wat gebeurt als ik vergeet om een gewone tekstversie tot stand te brengen?**\
Het systeem genereert automatisch een normale tekstversie van uw HTML, die mogelijk niet optimaal is opgemaakt, maar die zorgt voor levering aan alleen-tekst clients.

**kan ik verschillende verpersoonlijking in HTML versus gewone teksten gebruiken?**\
Ja, wanneer u synchronisatie uitschakelt, kunt u elke versie afzonderlijk aanpassen, inclusief verschillende verpersoonlijkingsvelden of -inhoud.

**Welke e-mailcliënten steunen slechts gewone teksten?**\
Zeer weinig moderne clients zijn alleen-tekst, maar in sommige beleidsregels voor e-mail, toegankelijkheidsfuncties en oudere mobiele apparaten kan onbewerkte tekst worden weergegeven. Het is ook een fallback wanneer HTML rendering mislukt.

**hoe vaak zou ik mijn gewone tekstversie moeten bijwerken?**\
Werk het bij wanneer u belangrijke wijzigingen aanbrengt in uw HTML-inhoud. Kleine HTML-tweaks hebben mogelijk geen onbewerkte tekstupdates nodig als het kernbericht hetzelfde blijft.

**kan ik verbindingen in duidelijke tekste-mails omvatten?**\
Ja! Als u volledige URL&#39;s (bijvoorbeeld https://example.com/page) opneemt, kunnen de meeste e-mailclients automatisch op deze URL&#39;s klikken.

**zou ik beelden in gewone teksten moeten omvatten?**\
Nee, gewone tekst ondersteunt geen afbeeldingen. Beschrijf in plaats daarvan wat de afbeelding weergeeft of geef een koppeling op om de afbeelding online weer te geven.
