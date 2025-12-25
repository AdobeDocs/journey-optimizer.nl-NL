---
solution: Journey Optimizer
product: Journey Optimizer
title: Testen en goedkeuren
description: Testen en goedkeuren
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: dd3d91266c0edea562f75ceb1f75974c7242ee1a
workflow-type: tm+mt
source-wordcount: '1296'
ht-degree: 0%

---

# Testen en goedkeuren{#section-overview}

Kwaliteitsborging is essentieel voor het bieden van uitzonderlijke klantervaringen. Adobe Journey Optimizer biedt uitgebreide test- en goedkeuringsmogelijkheden om u te helpen inhoud te valideren, de logica van de reis te controleren en ervoor te zorgen dat campagnes voldoen aan kwaliteitsnormen voordat ze bij uw publiek terechtkomen. Van het voorvertonen van persoonlijke berichten met testprofielen tot het simuleren van complexe reisstromen, deze hulpmiddelen u machtigen om kwesties vroegtijdig te identificeren en op te lossen, risico te verminderen, en merkintegriteit te handhaven. Of u nu het renderen van e-mail op verschillende apparaten, het valideren van meervoudige reizen of het vaststellen van formele goedkeuringswerkstromen test, in deze sectie worden de beste praktijken en stapsgewijze processen uitgelegd om vertrouwen in uw campagnes en reizen te wekken. Door grondig te testen en gestructureerde goedkeuringen uit te voeren, zult u fouten minimaliseren, leverbaarheid verbeteren, en naadloze ervaringen creëren die met uw klanten passen.

## Waarom het testen en goedkeuren belangrijk is

Testen en goedkeuringen dienen als essentiële kwaliteitspoorten die uw merkreputatie beschermen en het succes van de campagne garanderen. Dit is de reden waarom ze belangrijk zijn:

* **de fouten van de Vangst alvorens zij klanten** bereiken - identificeer gebroken verbindingen, onjuiste verpersoonlijking, teruggevende kwesties, en logische onvolkomenheden in een gecontroleerd milieu waar de moeilijke situaties snel en risico-vrij zijn.

* **verbeter leverability** - de spamscores van de Test, bevestigt e-mailauthentificatie, en controleert het teruggeven over e-mailcliënten om inbox plaatsing en betrokkenheidstarieven te maximaliseren.

* **verzeker merkconsistentie** - de inhoud van de voorproef met verschillende testprofielen om te verifiëren dat de verpersoonlijkingsvertoningen correct voor diverse klantensegmenten en handhaaft merknormen.

* **bevestigt complexe reizen** - Simuleer multi-step wegstromen om te bevestigen dat de trekkers correct branden, de voorwaarden evalueren behoorlijk, en de klanten ontvangen de juiste berichten op het juiste ogenblik.

* **Vestig verantwoordingsplicht** - voer formele goedkeuringswerkschema&#39;s uit die van de belanghebbende ondertekening vereisen, creërend duidelijke eigendom en verminderend onbevoegde of premature campagnelanceringen.

* **sparen tijd en middelen** - ontdek kwesties vroeg in de ontwikkelingscyclus wanneer de moeilijke situaties goedkoper en sneller zijn, verhinderend dure post-lanceringscorrecties of de escalaties van de klantendienst.

## Best practices testen

Volg de onderstaande aanbevolen procedures om de doeltreffendheid van uw testactiviteiten te maximaliseren:

1. **Test vroeg en vaak** - wacht niet tot een campagne volledig wordt gebouwd. Test inhoud, personalisatie en logica in toenemende mate tijdens uw ontwikkeling.

1. **Gebruik realistische testprofielen** - [&#x200B; creeer testprofielen &#x200B;](../using/audience/creating-test-profiles.md) die nauwkeurig uw doelpubliekssegmenten, met inbegrip van randgevallen en verschillende verpersoonlijkingsscenario&#39;s vertegenwoordigen.

1. **Test over apparaten en cliënten** - verifieer [&#x200B; e-mailteruggevende &#x200B;](../using/content-management/rendering.md) op populaire e-mailcliënten (Gmail, Vooruitzichten, de Post van Apple) en apparaten (Desktop, mobiel, tablet) om verenigbare vertoning te verzekeren.

1. **bevestigt volledig verpersoonlijking** - test met veelvoudige [&#x200B; testprofielen &#x200B;](../using/content-management/test-profiles.md) die verschillende attributenwaarden hebben om verpersoonlijkingstokens te bevestigen teruggeven correct en het werk van terugvalwaarden.

1. **Simuleer reiswegen** - voor complexe reizen met veelvoudige takken, gebruik [&#x200B; testwijze &#x200B;](../using/building-journeys/testing-the-journey.md) om verschillende ingangsvoorwaarden en profielattributen te testen om alle mogelijke wegen te bevestigen.

1. **de leverbaarheidsindicatoren van de Controle** - het spamscores van het Overzicht [&#x200B; &#x200B;](../using/content-management/spam-report.md), authentificatiestatus, en e-mailgezondheidsmetriek alvorens groot verzendt.

1. **de testresultaten van het Document** - houd verslagen van testresultaten, gevonden kwesties, en resoluties om toekomstige testprocessen te verbeteren en lessen met uw team te delen.

1. **verbind vroege belanghebbenden** - Deel voorproeven en testresultaten met belanghebbenden vóór [&#x200B; formele goedkeuring &#x200B;](../using/test-approve/gs-approval.md) om te verzamelen terugkoppel en richt verwachtingen.

## Aanbevolen testworkflow

Volg deze systematische aanpak om te zorgen voor grondige tests en probleemloze goedkeuringen:

### &#x200B;1. Ontwikkeling van inhoud en voorvertoning

Begin door uw inhoud te creëren en voorproefmogelijkheden te gebruiken om eerste ontwerp en verpersoonlijking te verifiëren:

* Ontwerp uw [&#x200B; e-mail &#x200B;](../using/email/create-email.md), [&#x200B; SMS &#x200B;](../using/sms/create-sms.md), [&#x200B; duw bericht &#x200B;](../using/push/create-push.md), of andere kanaalinhoud
* Gebruik de **[Simuleer inhoud](../using/content-management/preview-test.md)** eigenschap aan voorproef met testprofielen
* De tokens van de controle [&#x200B; van de 1&rbrace; verpersoonlijking &lbrace;, dynamische inhoud, en terugvalwaarden](../using/personalization/personalization-syntax.md)
* Verifieer [&#x200B; teruggevend &#x200B;](../using/content-management/rendering.md) over verschillende het schermgrootte en e-mailcliënten

### &#x200B;2. Technische validatie

Valideer technische aspecten die gevolgen hebben voor de leverbaarheid en functionaliteit:

* Voer [&#x200B; controles van de spamscore &#x200B;](../using/content-management/spam-report.md) in werking om potentiële leveringskwesties te identificeren
* Koppelingen testen om te controleren of ze niet worden verbroken en correct worden bijgehouden
* Bevestig [&#x200B; e-mailauthentificatie &#x200B;](../using/configuration/dmarc-record.md) (SPF, DKIM, DMARC) configuratie
* HTML-rendering controleren en controleren op problemen met CSS-compatibiliteit
* Test [&#x200B; ontvankelijk ontwerp &#x200B;](../using/email/content-from-scratch.md) op mobiele en Desktopapparaten

### &#x200B;3. Reistesten

Voor reizen valideert u de orkestlogica:

* Activeer **[wijze van de Test](../using/building-journeys/testing-the-journey.md)** om profielvooruitgang door de reis te simuleren
* Test verschillende [&#x200B; ingangsvoorwaarden &#x200B;](../using/building-journeys/entry-management.md) en publiekskwalificaties
* Verifieer [&#x200B; activiteiten &#x200B;](../using/building-journeys/wait-activity.md) wachten, [&#x200B; voorwaarden &#x200B;](../using/building-journeys/condition-activity.md), en vertakkend logisch werk correct
* Gebruik **[Droog looppas](../using/building-journeys/journey-dry-run.md)** voor complexe reizen om uitvoeringspaden te analyseren zonder berichten te verzenden
* Controle dat [&#x200B; gebeurtenissen &#x200B;](../using/event/about-events.md) correct teweegbrengen en [&#x200B; douaneacties &#x200B;](../using/action/about-custom-action-configuration.md) uitvoeren zoals verwacht

### &#x200B;4. Goedkeuringsaanvraag

Nadat het testen is voltooid en de problemen zijn opgelost:

* Verzend de campagne of de reis voor goedkeuring volgens het 0&rbrace; goedkeuringsbeleid van uw organisatie [&#128279;](../using/test-approve/approval-policies.md)
* Omvat testresultaten en documentatie met het [&#x200B; goedkeuringsverzoek &#x200B;](../using/test-approve/request-approval.md)
* Adres om het even welke terugkoppel of veranderingsverzoeken van [&#x200B; fiatteurs &#x200B;](../using/test-approve/review-approve-request.md)
* Breng de noodzakelijke herzieningen aan en test of de wijzigingen significant zijn

### &#x200B;5. Verificatie voorafgaand aan de lancering

Voordat u uw campagne of reis activeert:

* Voer een definitieve overzicht van alle montages, publiek, en [&#x200B; programma&#39;s &#x200B;](../using/building-journeys/journey-properties.md) uit
* Controleren of alle goedkeuringen zijn geïnstalleerd en gedocumenteerd
* Bevestig verzendt tijden en [&#x200B; tijdstreken &#x200B;](../using/building-journeys/timezone-management.md) correct zijn
* Laat [&#x200B; controle en alarm &#x200B;](../using/reports/alerts.md) toe om prestaties na lancering te volgen

### &#x200B;6. Monitor en herhaling

Ga na het opstarten door met de bewaking om eventuele problemen vroeg op te vangen:

* De opstelling [&#x200B; systeemalarm &#x200B;](../using/reports/alerts.md) voor reisfouten, hoge stuittarieven, of lage overeenkomst
* Herzie [&#x200B; levende rapporten &#x200B;](../using/building-journeys/report-journey.md) om prestaties tegen verwachtingen te volgen
* Ben bereid om [&#x200B; reizen te pauzeren of te wijzigen &#x200B;](../using/building-journeys/journey-pause.md) als de kritieke kwesties zich voordoen
* Geleerde documentlessen voor het verbeteren van toekomstige testprocessen

## Testen in actie: gebruik hoofdletters/kleine letters

Zie hoe testconcepten op real-world scenario&#39;s van toepassing zijn:

* **[verzend multi-kanaalberichten](../using/building-journeys/journeys-uc.md)** - Dit gebruiksgeval toont aan hoe te om een reis te testen die Gelezen Publiek, reactiegebeurtenissen, en e-mail/dupberichten combineert. Leer hoe te om de volledige stroom van publiek te bevestigen richtend aan berichtlevering, en test en het publiceren stappen in actie te zien.

* **[verzend een bericht naar abonnees](../using/building-journeys/message-to-subscribers-uc.md)** - ontdekt hoe te reizen te testen die de lijsten van het doelabonnement met dynamische e-mail het richten. Dit voorbeeld toont hoe te om verpersoonlijkingsuitdrukkingen te bevestigen en ervoor te zorgen bereiken de berichten de correcte abonnees.

* **[verzend tijd-gebonden berichten](../using/building-journeys/weekday-email-uc.md)** - begrijp hoe te reizen met op tijd-gebaseerde voorwaarden te testen om berichten te verzekeren worden verzonden op specifieke dagen. Zie hoe te om te bevestigen wachtende activiteiten en het plannen logica.

* **[Onderzoek meer gevallen van het reisgebruik](../using/building-journeys/jo-use-cases.md)** - toegang tot een uitvoerige inzameling van praktische voorbeelden die ervaringsgebeurtenissen, multi-kanaaloverseinen, en externe systeemintegratie behandelen.

## Inhoud testen en goedkeuren

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Inhoud voorvertonen, testen en valideren

Leer hoe u persoonlijke inhoud kunt voorvertonen, testen en valideren met testprofielen, e-mailrenderingtests, spamscore-evaluaties en meer.

[Voorvertoning weergeven en inhoud testen](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

Goedkeuringswerkstromen voor reizen en campagnes

Begrijp hoe u goedkeuringsprocedures instelt, beheert en uitvoert om kwaliteitscontrole voor reizen en campagnes te waarborgen.

[Meer informatie over goedkeuringswerkstromen](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Uw reis testen

Valideer uw reis voordat u deze publiceert door deze te testen met specifieke profielen om ervoor te zorgen dat gebeurtenissen, voorwaarden en acties naar behoren werken.

[Uw reis testen](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Reizen op reis

Voer een droge looppas uit om de uitvoeringspad van uw reis te simuleren en te bevestigen, die potentiële kwesties identificeren alvorens live te gaan.

[Meer informatie over Journey Dry run](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

Bewaking en probleemoplossing

Toegang tot uitgebreide bronnen voor probleemoplossing, systeemwaarschuwingen en foutcodes om problemen met de uitvoering en prestaties van de reis op te lossen.

[Bewaking en probleemoplossing weergeven](troubleshoot-journey-landing-page.md)
:::

::::

## Aanvullende bronnen

### Essentiële instructies voor het testen en valideren

* [&#x200B; Levend Rapport in Uw Reis &#x200B;](../using/building-journeys/report-journey.md) - de metriek van de reis van de monitor in real time om prestaties te volgen en kwesties tijdens uitvoering te identificeren. Toegang tot gedetailleerde uitsplitsingen van profielprogressie, gebeurtenistriggers en voltooiingssnelheden voor handelingen.

* [&#x200B; Creërend de Profielen van de Test &#x200B;](../using/audience/creating-test-profiles.md) - creeer en beheer testprofielen om echte klantenscenario&#39;s te simuleren en verpersoonlijking te bevestigen. Leer hoe u profielen markeert voor testen, kenmerkwaarden instelt en testprofielsegmenten ordent.

* [&#x200B; E-mailSpam Rapport &#x200B;](../using/content-management/spam-report.md) - controleer uw e-mailspamscore alvorens te verzenden om bevreesbaarheid en inbox plaatsing te verbeteren. Begrijp hoe de spamfilters uw inhoud evalueren en aanbevelingen voor verbetering krijgen.

* [&#x200B; Veelgestelde vragen van de Reis &#x200B;](../using/building-journeys/journey-faq.md) - vind antwoorden aan gemeenschappelijke vragen over reisverwezenlijking, het testen, de uitvoering, en het oplossen van problemen. Snelle referentie voor het oplossen van frequente problemen en het begrijpen van het reisgedrag.

### Verwante onderwerpen

* [&#x200B; het Beheer van de Inhoud &#x200B;](content-management-landing-page.md) - Leer hoe te, voorproef, en beheer inhoud gebruikend malplaatjes, fragmenten, en e-mail Designer. Aanbevolen werkwijzen voor het maken van basisinhoud voor consistente branding.

* [&#x200B; Rapportering &amp; Analytics &#x200B;](reporting-landing-page.md) - analyseer campagne en reisprestaties met uitvoerige rapporten, dashboards, en metriek. Maak gegevensgestuurde besluiten om klantenervaringen te optimaliseren.

* [&#x200B; Configuratie van de Reis &#x200B;](configure-journeys-landing-page.md) - vorm gegevensbronnen, gebeurtenissen, en douaneacties om verfijnde reisorchestratie toe te laten. De technische grondslagen leggen voor het creëren van reizen.

* [&#x200B; Beheer van de Campagne &#x200B;](../using/campaigns/get-started-with-campaigns.md) - onderzoek verschillende campagneretypes en leer hoe te, partij en in real time campagnes voor maximumeffect tot stand brengen te plannen en te optimaliseren.
