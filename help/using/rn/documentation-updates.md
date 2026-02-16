---
solution: Journey Optimizer
product: journey optimizer
title: Documentatie-updates
description: Meer informatie over de meest recente documentatie-updates
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: b980a1be123328e60f4eb1fd28d11ec9525b5ce8
workflow-type: tm+mt
source-wordcount: '3330'
ht-degree: 6%

---

# Documentatie-updates {#latest-updates}

Deze pagina bevat een overzicht van alle meest recente wijzigingen in de documentatie van [!DNL Journey Optimizer] , naast de updates die betrekking hebben op de functies en verbeteringen van de maandelijkse release.

## Februari 2026 {#february-2026}

* De Externe pagina van de systeemintegratie is bijgewerkt met verbindingen met douanegegevensbronnen en douaneacties, en verduidelijkt dat de uitgangsvolmacht statische IP voor uitgaande vraag van **de acties van de Douane** aan uw externe systemen verstrekt. [Meer informatie](../configuration/external-systems.md)

* De documentatie bij de uitvoering Journey Dry is verduidelijkt: de kenmerken van de step-gebeurtenis `inDryRun` en `dryRunID` documenteren nu dat ze `true` / instantie-id retourneren in de modus Droog en `null` voor test- of live reizen. De richtlijnen voor het uitsluiten van Dry run step-gebeurtenissen bij het rapporteren van query&#39;s zijn dienovereenkomstig bijgewerkt. [Meer informatie](../building-journeys/journey-dry-run.md)

* **duw van het Web** is nu algemeen beschikbaar. De documentatie van het pushbericht is dienovereenkomstig geherstructureerd en bijgewerkt (begin, ontwerp, verzend, creeer). [Meer informatie](../push/get-started-push.md)

* De Web-push configuratiepagina is nu beschikbaar in de documentatie. [Meer informatie](../push/push-configuration-web.md)

* De documentatie over het gebruiken van fragmenten in Beslissing is bijgewerkt: de nota&#39;s zijn toegevoegd in de secties van Fragments en van Beslissing, en de Fragments in de pagina van besluitvormingsbeleid is bijgewerkt. [Meer informatie](../experience-decisioning/fragments-decision-policies.md)

* De documentatie van de sms-website-haak is bijgewerkt: de inhoud van de twilio-website is verwijderd. [Meer informatie](../sms/sms-webhook.md)

* De documentatie voor de migratie-API voor beslissingen is bijgewerkt. [Meer informatie](../experience-decisioning/decisioning-migration-api.md)

* De **activiteit van het Besluit van de Inhoud** is nu algemeen beschikbaar. De pagina Activiteit van het Besluit van de Inhoud is bijgewerkt met een sectie over Beslissingsgegevens beschikbaar in step gebeurtenissen. [Meer informatie](../building-journeys/content-decision.md)

* Koppelingen naar de API-documentatie voor loyaliteitsuitdagingen zijn toegevoegd aan de sectie Loyalty-uitdagingen (begin, maak uitdagingen, maak taken, maak de uitdagingen van de toegangloyaliteit). [Meer informatie](../loyalty-challenges/get-started.md)

* De ondersteunde kanaalgegevens in de documentatie van de wizard voor het maken van de campagne zijn gecorrigeerd. Aan de slag met kanalen en geordende campagnes op de pagina&#39;s met veelgestelde vragen zijn overeenkomstig bijgewerkt. [Meer informatie](../campaigns/get-started-with-campaigns.md)

* De toestemmingendocumentatie is verbeterd betreffende **Reis leidt** en **keurt** toestemmingen goed. [Meer informatie](../administration/ootb-permissions.md)

* De AEM (Adobe Experience Manager)-integratiedocumentatie is bijgewerkt met herziene naamgeving (AEM dynamic content en AEM fragments). [Meer informatie](../integrations/aem-fragments.md)

* Een nieuwe uitsluitingsreden is toegevoegd aan de uitsluitingslijst: **UnsubscribeLinkNotValid** (foutencode 050081). Deze uitsluiting wordt gegenereerd wanneer de lengte van het onderwerp List-Unsubscribe mailTo groter is dan de RFC-limiet van 998 tekens. [Meer informatie](../reports/exclusion-list.md)

* De documentatie van de functie formatDate helper is verbeterd met een opmerking dat de functie een datum-tijd veldtype (geen tekenreeks) vereist en met meerdere voorbeelden: een datum-tijd veld opmaken, een tekenreeks eerst omzetten in de datum, volledige datum met dagnaam, dynamische datum vanaf de systeemtijd en de dag-van-week-indeling, inclusief uitvoer in kleine letters. [Meer informatie](../personalization/functions/dates.md#format-date)

* De documentatie van e-mailberichten voor tekstversies is uitgebreid met uitgebreide instructies voor het gebruik van hoofdletters en kleine letters, waaronder beslissingscriteria voor het gebruik van gewone tekst in plaats van automatische synchronisatie, praktische voorbeelden met realistische scenario&#39;s en een sectie met veelgestelde vragen. [Meer informatie](../email/text-version-email.md#when-to-use)

* Er is een beperking toegevoegd aan de documentatie van de hulpmiddel Metagegevens van de Uitvoering om te verduidelijken dat de meta-gegevens niet voor profielen worden gevangen die van de actie worden uitgesloten. [Meer informatie](../personalization/functions/helpers.md#execution-metadata)

* De op code-gebaseerde documentatie van implementatiemonsters is bijgewerkt om het tokens gebied in propositionAction voor nauwkeurige het volgen en attributie in Beslissing te omvatten. [Meer informatie](../code-based/code-based-implementation-samples.md#client-side-how)

* Er is een opmerking toegevoegd aan de URL-tracking en de documentatie voor het opzeggen van lijsten om te verduidelijken dat de volgorde van URL-volgparameters die aan URL&#39;s zijn toegevoegd, willekeurig is en niet kan worden gecontroleerd. [Meer informatie](../email/url-tracking.md)

* De documentatie over Designer-thema&#39;s via e-mail is bijgewerkt met informatie over de ondersteuningsbeperkingen voor weblettertypen en het belang van fallback-lettertypen. [Meer informatie](../email/apply-email-themes.md#themes-guardrails)

## Januari 2026 {#january-2026}

* De documentatie van het gebruiksdashboard van de Vergunning is met bijgewerkte begeleiding over **toe te laten Profielen**, met inbegrip van definitiedetails en het oplossen van problemenbegeleiding verduidelijkt. [Meer informatie](../audience/license-usage.md#what-is-engageable-profile)

* Er is een opmerking toegevoegd aan de documentatie over thema&#39;s in e-mail voor Designer om de beperkingen van de ondersteuning van weblettertypen te verduidelijken. [Meer informatie](../email/apply-email-themes.md#themes-guardrails)

* Er is een nieuwe sectie toegevoegd aan de documentvalidatie van de ladingsgrootte van de transportlading, inclusief waarschuwings- en foutdrempels en richtlijnen voor het optimaliseren van reizen. [Meer informatie](../start/guardrails.md#journey-payload-size)

* De documentatie bij de beslissingsinstructies is bijgewerkt en bevat nu de groottebeperkingen voor besluitvormingsitems (1 kB voor items, inclusief kenmerken met maximaal 30 kenmerken). [Meer informatie](../experience-decisioning/decisioning-guardrails.md)

* Er is een notitie toegevoegd aan de documentatie over het maken van het beslissingsbeleid om gebruikers te laten weten dat wijzigingen na het maken van een beslissingsbeleid maximaal 15 minuten kunnen duren om zich over alle gegevensgebieden te verspreiden, en maximaal 30 minuten voor Canada. [Meer informatie](../experience-decisioning/create-decision-policy.md#review)

* Er is een notitie toegevoegd aan de fragmentdocumentatie om te waarschuwen dat wanneer zowel het knoplabel als de URL bewerkbaar worden gemaakt in een fragment, de volgende dataset de URL-waarde in plaats van de labelwaarde registreert. [Meer informatie](../content-management/customizable-fragments.md#visual)

* Er is nu een nieuwe pagina beschikbaar met een beschrijving van de voordelen van migratie van beslissingsbeheer naar besluitvorming, inclusief informatie over toekomstige API&#39;s voor migratiehulpmiddelen. [Meer informatie](../experience-decisioning/migrate-to-decisioning.md)

* Er is een hulplijn toegevoegd om te verduidelijken dat opzoekgegevenssets alleen beschikbaar zijn voor inbound edge-based activering in het gebied waar de sandbox van de gegevensset zich bevindt. [Meer informatie](../data/lookup-aep-data.md#guidelines)

* Er is een nieuwe sectie toegevoegd aan de configuratiedocumentatie van het geordende campagnekanaal waarin wordt uitgelegd hoe u contextafhankelijke kenmerken (zoals campagne-id, naam en details van handelingen) kunt gebruiken in URL-volgparameters voor analytische en rapportagedoeleinden. [Meer informatie](../orchestrated/channel-config.md#url-tracking)

* De documentatie voor het optimaliseren van inhoud is geherstructureerd voor meer duidelijkheid. De hoofdoptimalisatiepagina is opgedeeld in vier gerichte subpagina&#39;s: een pagina die aan de slag gaat, een pagina die speciaal is bedoeld voor doelframes, een pagina voor experimenten en een pagina voor het combineren van beide benaderingen. [Meer informatie](../content-management/gs-message-optimization.md)

* De opmerkingen bij Beperkte beschikbaarheid zijn verwijderd uit drie reiswaarschuwingen (Reis gepubliceerd, Reis voltooid en Aangepaste actiecapping geactiveerd), omdat deze functies nu algemeen beschikbaar zijn. [Meer informatie](../reports/alerts.md)

* De landingspagina voor testen, valideren en goedkeuren is uitgebreid met nieuwe secties, waaronder een overzicht van de testmogelijkheden, veelgestelde vragen, een beslissingsstructuur met navigatiekoppelingen en verbeterde terminologie met documentatiekoppelingen. [Meer informatie](../../rp_landing_pages/test-landing-page.md)

* Er is een nieuwe sectie toegevoegd aan de documentatie van de verpersoonlijkingssyntaxis om te verduidelijken hoe u gereserveerde trefwoorden in verpersoonlijkingsexpressies kunt gebruiken. Bepaalde PQL-trefwoorden zoals `next` , `last` en `this` moeten met backtiks worden beschermd wanneer ze als veldnamen in uw XDM-schema worden gebruikt. [Meer informatie](../personalization/personalization-syntax.md#reserved-keywords)

* [&#x200B; krijgt begonnen met campagnes &#x200B;](../campaigns/get-started-with-campaigns.md) en [&#x200B; leidt campagnes &#x200B;](../campaigns/manage-campaigns.md) pagina&#39;s zijn geherstructureerd met betere informatiearchitectuur, met inbegrip van een uitvoerig werkschema met type-specifieke gidsen, verbeterde vergelijkingen van het campagnetype, en geconsolideerde statuslijst.

* De landingspagina voor reizen is opnieuw ontworpen om het instappen te vergemakkelijken met een nieuwe werkstroom in zes stappen, verbeterde vergelijkingen van het type van reizen en verbeterde navigatie door de documentatie. [Meer informatie](../building-journeys/journey.md)

* Een gedetailleerde sectie is toegevoegd om gebruikers te helpen Base64-Gecodeerde OpenSSH privé sleutels voor authentificatie te produceren SFTP wanneer het vormen van dossier verpletterend voor Directe Post om verbindingsfouten te vermijden. [Meer informatie](../direct-mail/direct-mail-configuration.md#ssh-key-generation)

* Er is een notitie toegevoegd aan de documentatie van de subdomeindelegatie om gebruikers te informeren dat ze 24-48 uur voor DNS-propagatie moeten toestaan voordat ze een delegatie naar Adobe proberen. [Meer informatie](../configuration/delegate-subdomain.md#set-up-subdomain)

## December 2025 {#december-2025}

* Het uploadpubliek Aangepast voor beslissingsdocumentatie is bijgewerkt en bevat nu een vereiste API-markering voor het ophalen van verrijkingsgegevens. Wanneer u CSV-geüploade doelgroepen gebruikt bij het bepalen van de aanbieding, moet u `"xdm:enrichedAudience": true` in de payload van uw API-aanvraag opnemen om de verrijkingskenmerken op te halen in de reactie op het besluit van de aanbieding. [Meer informatie](../offers/custom-upload-decisioning.md#must-read)

* Er is een opmerking toegevoegd aan de documentatie over het verzenden van bewijzen om te verduidelijken dat de regels voor frequentiecortering van toepassing zijn op proefdrukken. De pagina bevat nu een sectie &#39;Moet lezen&#39; met belangrijke overwegingen met betrekking tot het gedrag van de frequentiekoppeling, de beperkingen van de spiegelpagina en de toegankelijkheidsregels voor elementen. [Meer informatie](../content-management/proofs.md)

* Er is een nieuwe beschikbaarheidstabel voor communicatiekanalen toegevoegd aan de pagina Aan de slag met kanalen, waarin wordt aangegeven welke kanalen door reizen en campagnes worden ondersteund (actiecampagnes, door de API geïnitieerde campagnes en geordende campagnes). [Meer informatie](../channels/gs-channels.md#channels)

* Er is een nieuwe, uitgebreide bestemmingspagina voor tracering gemaakt om gebruikers te helpen alle tracking- en bewakingsfuncties die in Journey Optimizer beschikbaar zijn, te detecteren en te gebruiken. [Meer informatie](../start/get-started-tracking.md)

* De pagina voor het beheer van e-mailweigeren is uitgebreid met gedetailleerde informatie over de workflow voor het afmelden van abonnementen, waarin de verwachte volgorde van gebeurtenissen voor het opzeggen van de bestemmingspagina wordt uitgelegd. [Meer informatie](../email/email-opt-out.md#send-message-unsubscribe-link)

* De documentatie van de abonnementenlijst is bijgewerkt om informatie over het stromen segmentgeschiktheidscriteria te omvatten. [Meer informatie](../landing-pages/subscription-list.md#define-subscription-list)

* Er is een nieuwe IP-handleiding voor warmteafgifte beschikbaar, die uitgebreide richtlijnen biedt voor de belangrijkste aspecten van de reputatie, voorbereiding vóór de vlucht, meetgegevens voor controle en beste praktijken voor de overgang van reputatie zonder nummer naar plaatsing in een postvak. [Meer informatie](../configuration/ip-warmup-deliverability-guide.md)

* Er is een waarschuwing toegevoegd aan de secties Landing en Email opt-out om te verduidelijken dat als u op een link Unsubscribe klikt, alleen de bestemmingspagina wordt geopend, maar gebruikers het formulier moeten verzenden om het opt-outproces te voltooien. [Meer informatie](../landing-pages/lp-use-cases.md#configure-opt-out)

* Er is nu een nieuwe bibliotheek met praktijkgevallen beschikbaar, waarin een verzameling praktijkgevallen wordt samengebracht, waaronder tactische patronen (suppressielogica, personalisatietechnieken, reisexit-strategieën) en complete scenario&#39;s voor marketing en technische workflows. [Meer informatie](../building-journeys/jo-use-cases.md)

* Er is nu een nieuw gebruiksgeval beschikbaar waarin wordt getoond hoe u een reis zodanig kunt configureren dat e-mailberichten alleen op weekdagen (maandag-vrijdag) worden verzonden. Er wordt nu automatisch een wachtrij voor weekendberichten weergegeven die op maandag op een bepaald tijdstip moeten worden verzonden. [Meer informatie](../building-journeys/weekday-email-uc.md)

* Er is nu een nieuwe pagina beschikbaar met uitleg over de beslissingsmogelijkheden van Journey Optimizer, waaronder de verschillen tussen het besluitvormingskader van de volgende generatie en de bestaande oplossing voor het beheer van besluiten, en hun belangrijkste voordelen voor het aanbieden van persoonlijke aanbiedingen langs verschillende kanalen. [Meer informatie](../experience-decisioning/gs-decision.md)

* Er is een nieuwe sectie toegevoegd aan de activeringsdocumentatie voor het publiek waarin wordt uitgelegd hoe u niet-ondersteunde publiekstypen (zoals Customer Journey Analytics-soorten publiek) in [!DNL Journey Optimizer] activeert door deze in een nieuwe segmentdefinitie in de portal Publiek te plaatsen. [Meer informatie](../audience/target-audiences.md#activation-non-supported)

* Een nieuwe sectie is toegevoegd aan de documentatie van de Activiteit van de Wacht verklarend hoe de profielen bij een Wacht activiteit in Gelezen reizen van het Publiek automatisch hun attributen van de Verenigde Dienst van het Profiel (UPS) verfrissen. Dit verduidelijkt dat de profielgegevens tijdens reisuitvoering na een wachttijdknoop kunnen veranderen, die onverwachte resultaten kan veroorzaken als u verenigbare momentopnamedata door de reis verwacht. [Meer informatie](../building-journeys/wait-activity.md#profile-refresh)

* Er is een waarschuwende opmerking toegevoegd aan de sectie Padexperimenten om gebruikers te waarschuwen de metagegevens van een padexperiment niet te bewerken nadat deze zijn gepubliceerd, omdat dit de berekening en rapportage van de experimentele resultaten zal verstoren. [Meer informatie](../building-journeys/optimize.md#experimentation)

* Er is een opmerking toegevoegd aan het gedeelte Een formuliervoorinstelling maken om de vereisten voor streamingverbindingen op te geven die moeten worden weergegeven in de keuzelijst. [Meer informatie](../landing-pages/lp-forms.md#create-form-preset)

* Een nieuwe pagina is nu beschikbaar in de sectie Beslissing over hoe te om gegevensinzameling voor het volgen van beelden, kliks, en douanegebeurtenissen te vormen. [Meer informatie](../experience-decisioning/data-collection/schema-requirement.md)

* De productie van Inhoud met AI hulpdocumentatie is gereorganiseerd voor betere duidelijkheid en bruikbaarheid. De vorige vijf kanaal-specifieke pagina&#39;s (E-mail, Duw, SMS, Web, en het Landing Pagina) zijn geconsolideerd in drie generatie-type pagina&#39;s: [&#x200B; produceer volledige inhoud &#x200B;](../content-management/generative-full-content.md), [&#x200B; produceert tekst &#x200B;](../content-management/generative-text.md), en [&#x200B; produceert beelden &#x200B;](../content-management/generative-image.md).

## November 2025 {#november-2025}

* Er is nu een nieuwe pagina met veelgestelde vragen over beslissingen beschikbaar, die onderwerpen omvat zoals plafondregels, AI-modelconfiguratie, verkeersvereisten en optimalisatiestrategieën. [Meer informatie](../experience-decisioning/decisioning-faq.md)

* De pagina Aan de slag met het ontwerpen van e-mailberichten is bijgewerkt om te verduidelijken hoe u de e-mailversie van Designer kunt openen. [Meer informatie](../email/get-started-email-design.md)

* Een het oplossen van problemensectie is toegevoegd aan de het verslagpagina van DMARC om DNS propagatielatentie te richten. [Meer informatie](../configuration/dmarc-record.md#troubleshooting)

* De pagina Werken met GenStudio for Performance Marketing is verbeterd met nieuwe secties, waaronder belangrijke functies, veelvoorkomende gebruiksgevallen, voorwaarden en veelgestelde vragen. [Meer informatie](../integrations/genstudio.md)

* Er is een hulplijn toegevoegd aan de pagina voor instructies en beperkingen voor het activeren van pseudoniem-profielen op inkomende kanalen: als u niet-geverifieerde bezoekers als doel opgeeft, wordt het totale aantal te gebruiken profielen verhoogd. Adobe raadt daarom aan een TTL (Time-To-Live) in te stellen voor het automatisch verwijderen van profielen om de bijbehorende kosten te beheren. [Meer informatie](../start/guardrails.md#profile-management-inbound)

* Twee leerprogramma&#39;s over het vormen van het Web SDK voor besluiten en op code-gebaseerde ervaringen worden nu van verwijzingen voorzien op de op code-gebaseerde pagina van de de steekproefsteekproeven van implementatiemethodes. [Meer informatie](../code-based/code-based-decisioning-implementations.md#tutorials)

* Er is een opmerking toegevoegd om aan te geven dat elementen en afbeeldingen maximaal 2 jaar (730 dagen) na de eerste publicatie toegankelijk blijven en na afloop opnieuw moeten worden gepubliceerd. [Meer informatie](../content-management/proofs.md)

* Er is nu een uitgebreide handleiding voor het vragen van inhoud naar AI Assistant beschikbaar. In deze handleiding leert u hoe u effectieve aanwijzingen voor het maken van marketinginhoud met een hoge conversie en uitlijning maakt. Leer beste praktijken voor het schrijven van marketing doelstellingen, het gebruiken van merkactiva, en het optimaliseren van inhoud voor verschillende kanalen. [Meer informatie](../content-management/ai-assistant-prompting-guide.md)

* Er is een opmerking toegevoegd aan de segmentdefinitiedocumentatie om te verduidelijken dat het kenmerk `frequencyMap` niet wordt ondersteund voor gebruik in segmentdefinities en niet kan worden gebruikt als onderdeel van segmenteringscriteria voor het publiek. Voor het op frequentie-gebaseerde richten, overweeg het gebruiken van de regels van de frequentiegaleiding onder bedrijfsregels. [Meer informatie](../audience/creating-a-segment-definition.md)
* Er is een nieuw voorbeeld toegevoegd aan de API-documentatie voor vraagantwoorden waarin wordt getoond hoe aangepaste handelingsantwoorden in native kanalen kunnen worden gebruikt. In het voorbeeld ziet u hoe u geneste arrays kunt doorlopen op basis van aangepaste handelingantwoorden met Handlebars-syntaxis in e-mail-, push- en SMS-berichten. [Meer informatie](../action/action-response.md#response-in-channels)

* Er is een nieuwe sectie toegevoegd aan de integratiedocumentatie van Campagne v7/v8 waarin wordt uitgelegd hoe u bestaande aangepaste acties kunt bijwerken wanneer het eindpunt in real time (RT) verandert. De sectie omvat geleidelijke instructies voor het bijwerken van het eindpunt URL, het testen van de verbinding, en het bevestigen van veranderingen alvorens te bewaren. [Meer informatie](../action/acc-action.md#update-action)

* Er zijn nieuwe beperkingen en tips en trucksecties toegevoegd aan de documentatie over visuele fragmenten om gebruikers te waarschuwen voor het niet-ondersteunde nesten van fragmenten die dynamische inhoud bevatten in andere ontgrendelde fragmenten met dynamische inhoud. De hulp omvat het oplossen van problemenstappen voor kwesties van de verenigbaarheidswijze en aanbevelingen voor behoorlijk ontwerp van de e-mailstructuur. [Meer informatie](../email/use-visual-fragments.md#fragment-dynamic-content)

* Er is een sectie voor het oplossen van problemen toegevoegd aan de documentatie voor live rapportering tijdens de reis om gebruikers te helpen problemen met ontbrekende rapportgegevens op te lossen. De sectie behandelt de synchronisatie van reisnamen met rapporteringsdatasets, gegevens verfrissen timing, toegangstoestemmingencontrole, en de vereisten van de reisstatus. [Meer informatie](../building-journeys/report-journey.md#troubleshooting-missing-data)

* Er zijn drie nieuwe items voor veelgestelde vragen toegevoegd aan de documentatie over de middelen, waarin wordt uitgelegd hoe de looptijd van middelen en het beheer van de levenscyclus verlopen. De onderwerpen die worden behandeld omvatten het tijd-aan-Levende (TTL) beleid voor de activa van AEM (730 dagen), hoe te om gebroken beelden wegens activa te oplossen die verlopen, en informatie over de aanstaande verbeteringen aan activa vervallogica. [Meer informatie](../integrations/assets.md#faq-assets)

* Er is een uitgebreide sectie over het oplossen van problemen toegevoegd aan de activiteitendocumentatie van het publiek Lezen om problemen met betrekking tot het aantal gebruikers aan te pakken die optreden tussen geschatte en feitelijke profielen die reizen. In de sectie wordt ingegaan op de timing en de verspreiding van gegevens, de validering en controle van gegevens, en op de beste praktijken, waaronder het gebruik van de optie &quot;Trigger na batchpublieksevaluatie&quot;. [Meer informatie](../building-journeys/read-audience.md#audience-count-mismatch)

* Een nota is toegevoegd aan de de gebeurtenisdocumentatie van de Kwalificatie van het Publiek om het stromen segmentatielatentie (tot 2 uren) te verduidelijken en adviseren toevoegend een activiteit van de Wacht of buffertijd voor tijd-gevoelige reizen. [Meer informatie](../building-journeys/audience-qualification-events.md#streamed-speed-segment-qualification)

* Er is een nieuwe sectie toegevoegd aan de e-mailhandleidingen waarin de limiet van 2 MB aan berichtinhoud voor het publiceren van reizen wordt beschreven. Deze sectie bevat tips en trucs om geschreven inhoud onder 1 MB te houden, zodat overheadkosten voor backendverwerking mogelijk zijn. [Meer informatie](../start/guardrails.md#message-content-size)

* Verbeterde documentatie voor de optie Incrementeel lezen in de activiteiten van het publiek lezen om afhankelijkheden voor momentopnamen en de terugkijkbeperking van 24 uur te verduidelijken, inclusief aanbevelingen om ontbrekende profielen te voorkomen. [Meer informatie](../building-journeys/read-audience.md)

* Er is een notitie toegevoegd aan de instructies voor het opzoeken van de gegevensset om op te geven dat opzoekopdrachten niet samen kunnen worden geketend. [Meer informatie](../data/lookup-aep-data.md#guidelines)

* WhatsApp- en LINE-kanalen zijn nu beschikbaar voor handelingscampagnes. [Meer informatie](../campaigns/campaign-content.md)

* Er is een uitgebreid nieuw hoofdstuk over de snelheid van de reisverwerking toegevoegd aan de documentatie over het beheer van de toegang, dat betrekking heeft op de toegangspercentages voor profielen, evenementen en publiekskwalificaties binnen reizen, de impact van wachtactiviteiten en de impact van activiteiten. [Meer informatie](../building-journeys/entry-management.md#journey-processing-rate)

* Bij het ontwerpen van e-mailberichten controleert het systeem nu op sleutelinstellingen en geeft waarschuwingen voor waarschuwingen en fouten weer. Informatie over e-mailwaarschuwingen en validatievereisten is toegevoegd aan de pagina met instructies. [Meer informatie](../email/create-email.md#check-email-alerts)

* De voorzichtige nota die dat de frequentie het begrenzen niet voor eerder gecreeerd aanbiedingen kan worden toegelaten of worden onbruikbaar gemaakt is verwijderd uit Add beperkingen aan een aanbiedingspagina. [Meer informatie](../offers/offer-library/add-constraints.md#capping)

* Documentatie over hoe te met de gebeurtenissen van de reisstap te werken is nu beschikbaar. [Meer informatie](../reports/journey-step-events-overview.md)

* Er is nu een nieuwe, uitgebreide gids beschikbaar over de criteria voor het in- en uitstappen van een reis, waarin de beste praktijken, voorbeelden uit de praktijk en praktische richtsnoeren worden behandeld voor het beheer van de reis die profielen in Adobe Journey Optimizer binnenkomen en verlaten. [Meer informatie](../building-journeys/entry-exit-criteria-guide.md)

* Er is nu een nieuwe pagina beschikbaar met uitleg over het doorlopen van contextuele gegevens in berichten. Deze gids behandelt hoe te om de syntaxis van Handlebars te gebruiken om dynamische lijsten van gebeurtenissen, de reacties van de douaneactie, datasetraadplegingen, en andere contextbronnen in uw verpersoonlijking te tonen. [Meer informatie](../personalization/iterate-contextual-data.md)

* De vraag voor het identificeren van verworpen gebeurtenissen in reizen is verbeterd om juiste filters voor de fouten van de segmentuitvoer, de teruggooi van de verzender, en staatsmachine te omvatten teruggooi. [Meer informatie](../reports/query-examples.md#common-queries)

* De inleidende zinnen zijn toegevoegd aan alle 37 vraagvoorbeelden in de documentatie van vraagvoorbeelden om betere context te verstrekken en te verklaren wat elke vraag doet alvorens de SQL code voor te stellen. Dit verbetert het begrip van de gebruiker en verstrekt duidelijkere begeleiding bij wanneer om elke vraag te gebruiken. [Meer informatie](../reports/query-examples.md)

## Oktober 2025 {#october-2025}

* U kunt afbeeldingen nu omzetten naar HTML-sjablonen met de afbeelding naar HTML-converter. [Meer informatie](../email/image-to-html.md)

* Informatie over de Adobe Journey Optimizer-releasecyclus is nu beschikbaar. [Meer informatie](releases.md)

* Er is nu een nieuwe pagina met veelgestelde vragen over reizen beschikbaar. [Meer informatie](../building-journeys/journey-faq.md)

* De functionaliteit voor aangepaste handelingen controleren is nu beschikbaar. [Meer informatie](../action/reporting.md)

* De modus voor hoge doorvoer voor door API geactiveerde campagnes is nu beschikbaar. [Meer informatie](../campaigns/api-triggered-high-throughput.md)

* Er is nu een verwijzing naar foutcodes voor reizen beschikbaar. [Meer informatie](../building-journeys/error-codes-reference.md)

* Journey Optimizer Experimentation Accelerator-documentatie is nu beschikbaar. [Meer informatie](../content-management/experiment-accelerator-gs.md)

* Een nieuwe sectie is toegevoegd aan **formatDate** hulpdocumentatie van de hulpfunctie. Deze sectie verduidelijkt de betekenis van zeer belangrijke patroonsymbolen zoals y, Y, M, d, en D. [&#x200B; las meer &#x200B;](../personalization/functions/dates.md#pattern-characters)

* Een PQL-voorbeeld is toegevoegd aan de sectie met rangschikkingsformules voor besluiten om te laten zien hoe aanbiedingen kunnen worden verhoogd op basis van de postcode en het jaarinkomen van een profiel. [Meer informatie](../experience-decisioning/ranking/ranking-formulas.md#ranking-formula-examples)

* Er is een beperking toegevoegd aan de sectie over de testmodus voor reizen om aan te geven dat de testmodus geen ondersteuning biedt voor de verrijking van aangepaste upload-publiekskenmerken. [Meer informatie](../building-journeys/testing-the-journey.md#important_notes)

* Een nieuwe sectie werd toegevoegd aan de [&#x200B; het beheersbegeleiding &amp; de beperkingen van het Besluit &#x200B;](../offers/decision-management-guardrails.md#configurations) en [&#x200B; Beslissende guardrails &amp; de beperkingen &#x200B;](../experience-decisioning/decisioning-guardrails.md#configurations) pagina&#39;s om het maximumaantal gesteunde configuraties (20.000) te specificeren, die aan het totale aantal het begrenzen regels beantwoorden die in uw zandbak bestaan.

* Een opmerking toegevoegd in het gedeelte Condition Activity van de reis om te documenteren dat de evaluatie van de voorwaarde zal mislukken voor profielen die meer dan twee apparaatidentiteiten bevatten. [Meer informatie](../building-journeys/condition-activity.md)

* Er is een nieuwe pagina toegevoegd waarin wordt beschreven hoe u het beleid voor toestemming kunt gebruiken om de voorkeuren van uw klanten te respecteren op basis van hun keuze en tegelijkertijd hun toestemming te respecteren. [Meer informatie](../action/preference-center.md)

* Er is een notitie toegevoegd aan de pagina Aan de slag met profielen en hulplijnen om op te geven dat bij het invoeren van gegevens e-mails hoofdlettergevoelig zijn. Dit houdt in dat dubbele profielen kunnen worden gemaakt en gebruikt wanneer de desbetreffende ontvanger als doel wordt ingesteld. [Meer informatie](../audience/get-started-profiles.md)

* Er is een nieuw `render` -kenmerk geïntroduceerd in de personalisatie-editor. Stel deze in op `false` in gevallen waarin u de inhoud van een expressiefragment wilt verbergen. [Meer informatie](../personalization/use-expression-fragments.md#use-expression-fragment)

* Er is een lijst met instructies toegevoegd aan de sectie waarin wordt beschreven hoe u fragmenten die zijn gekoppeld aan besluitvormingselementen, kunt gebruiken in het besluitvormingsbeleid. [Meer informatie](../experience-decisioning/use-decision-policy.md#fragments)

* Toegevoegde beste praktijken voor datasetraadplegingen: houd knevels om indexerende kwesties te vermijden, en begrijp hoe de partijschrappingen raadplegingsgegevens beïnvloeden. [Meer informatie](../data/lookup-aep-data.md#guidelines)

* Er is een beperking toegevoegd die aangeeft dat alleen het Unified Profile Service-publiek wordt ondersteund bij het gebruik van Read-publiekstrajecten met aanvullende id&#39;s. [Meer informatie](../building-journeys/supplemental-identifier.md#guardrails)

* Documentatie voor de Experimentation Accelerator is verplaatst naar een aparte collectie. [Meer informatie](https://experienceleague.adobe.com/nl/docs/experimentation-accelerator/using/overview)

## September 2025 {#september-2025}

* Er is een nieuwe sectie Binnenkomend kanaal toegevoegd aan de pagina Hulplijnen en beperkingen om alle beperkingen te verzamelen die van toepassing zijn op het web, In-app, op code gebaseerde ervaringen en inhoudskaartkanalen. Het omvat de piekvolumegrens van 5.000 binnenkomende verzoeken per seconde voor alle binnenkomende verzoeken, en het maximum van 500 actieve binnenkomende acties. [Meer informatie](../start/guardrails.md#inbound-guardrails)

* Er is een pagina Veelgestelde vragen gepubliceerd voor geordende campagnes. [Meer informatie](../orchestrated/orchestrated-campaigns-faq.md)

* Een het oplossen van problemensectie is toegevoegd aan de de gebeurtenisdocumentatie van de Stap van de Reis met definities, gemeenschappelijke oorzaken, en het oplossen van problemenstappen voor het frequentst verwerpen eventTypes. [Meer informatie](../reports/sharing-field-list.md#discarded-events)

* De documentatie over het gebruik van aanvullende id&#39;s tijdens reizen bevat nu een tabel waarin wordt aangegeven hoe profielen zich gedragen wanneer bij reizen afstapcriteria worden toegepast met behulp van aanvullende id&#39;s. [Meer informatie](../building-journeys/supplemental-identifier.md#exit-criteria)

* Er is een sectie voor probleemoplossing toegevoegd aan het verwijderen van onderdrukkende profielen tijdens gepauzeerde reizen. [Meer informatie](../building-journeys/journey-pause.md#discards-troubleshoot)

* De informatie is toegevoegd in de schemaoverzichtsdocumentatie om standaard en relationele schema&#39;s te onderscheiden die voor Geordende campagnes worden gebruikt. [Meer informatie](../data/gs-data.md)

* De informatie is toegevoegd in de Beslissing en de documentatie van het Beslissingsbeheer over de vereisten om [&#x200B; auto-optimalisering &#x200B;](../experience-decisioning/ranking/auto-optimization-model.md) en [&#x200B; met succes te trainen gepersonaliseerde optimalisering &#x200B;](../experience-decisioning/ranking/personalized-optimization-model.md) modellen.

* Verduidelijkt dat de Interactieve vraag van de Uitvoering van het Bericht REST API een 60 tweede onderbreking heeft, met interne pogingen om levering te verzekeren. [Meer informatie](../campaigns/trigger-campaigns.md)

* De pagina van de de puntinzamelingen van Beslissing werd bijgewerkt om het gedrag van **te verduidelijken BEVAT** exploitant wanneer het bepalen van regels. [Meer informatie](../experience-decisioning/collections.md)

* De Assign prioritaire scores pagina werd bijgewerkt met de specifieke stappen om een prioritaire score voor binnenkomende kanaalacties binnen de **Actie** activiteit te bepalen. [Meer informatie](../conflict-prioritization/priority-scores.md#priority-action)

<!--
## August 2025 {#august-2025}

* A new page listing the best practices for designing accessible email and landing page content with [!DNL Journey Optimizer] was added. [Read more](../email/accessible-content.md)

* The documentation for supplemental identifiers in journeys has been updated with the following clarifications:

    * After adding a supplemental identifier to a schema, a new event (for event-triggered journeys) or a new field group (for Read audience journeys) must be created. Existing entities do not refresh automatically and will not recognize the new identifier.

    * Supplemental identifiers are not validated against Data Usage Labeling & Enforcement (DULE) policies and are not considered during data governance checks in journeys.

        [Read more](../building-journeys/supplemental-identifier.md)

* The Optimization in campaigns page was updated to reflect the fact that optimization is now also available in journeys. [Read more](../content-management/gs-message-optimization.md)

* A link to the tutorial video describing how to leverage message optimization in a campaign was added. [Read more](../content-management/gs-message-optimization.md)

## July 2025 {#july-2025}

* The campaigns interface now features two separate tabs: **Action** and **API Triggered**. The documentation has been updated accordingly, with information for each campaign type organized into dedicated sections to improve clarity and usability. [Read more](../campaigns/get-started-with-campaigns.md)

* The [Get started with subdomain delegation](../configuration/about-subdomain-delegation.md) and [Delegate a subdomain](../configuration/delegate-subdomain.md) pages have been updated to better present the different delegation methods and the steps to set them up.

* A note has been added to the Fragments section, specifying that when tracking is enabled in a journey or a campaign, if links are present in a fragment and if this fragment is used in a message, these links are tracked such as all other links included in the message. [Learn more](../content-management/create-fragments.md#content)

* The guardrails and limitations applying to subdomain delegation in Journey Optimizer have been enriched and consolidated into one dedicated section. [Read more](../configuration/delegate-subdomain.md#guardrails)

* A note has been added to the Create fallback offers and Create decision pages to mention that fallback offers should contain all representations used within a decision. [Read more](../offers/offer-library/creating-fallback-offers.md)

* The guardrails applying to fragments have been enriched. [Read more](../start/guardrails.md#fragments-guardrails).

* A note has been added to specify that links added to messages expire after 25 months and links to mirror pages after 90 days. [Read more](../email/message-tracking.md)

<!--* The possible email error types that could happen upon sending email deliveries with are now listed in a dedicated section. [Read more](../configuration/email-error-types.md)-->

<!--
## June 2025 {#june-2025}

* Added a new section on how to add and use rich text such as line breaks, bold, italics etc., to customizable fragments by using HTML components. [Read more](../content-management/customizable-fragments.md#rich-text)

* The Decisioning part has been updated with a specific section dedicated to building AI models. [Read more](../experience-decisioning/ranking/ai-models.md)

* Added a recommendation about the usage of the `actionExecutionTime` field in the journeyStep events action. [Read more](../reports/sharing-execution-fields.md#actionexecutiontime-field)

* Added a note about the `messageID` which may not be unique for each individual delivery. [Read more](../data/datasets-query-examples.md)

* Added a recommendation about historical events management in data hygiene operations. [Read more](../privacy/data-hygiene.md#data-hygiene-recommendations)

* Added a guardrail about landing pages not being supported for migration between sandboxes. [Read more](../configuration/copy-objects-to-sandbox.md#global)

* Added a caution note about nested JSON objects not supported in custom authentication for custom actions. [Read more](../datasource/external-data-sources.md)

* Added a caution note about conditional content variant naming in the Email designer. [Read more](../personalization/create-conditions.md)

* Updated the "Undelegate a landing page subdomain" section. [Read more](../landing-pages/lp-subdomains.md#undelegate-subdomain)

* Clarified journey reentrance rules when using supplemental identifiers. [Read more](../building-journeys/supplemental-identifier.md#guardrails)

* Added a new note to clarify that you must use the expression editor in Advanced mode when selecting the supplemental identifier attribute during event configuration. [Learn more](../building-journeys/supplemental-identifier.md#add)

* Added clarification on how journey reentrance works with supplemental identifiers. [Learn more](../building-journeys/supplemental-identifier.md#guardrails)

## May 2025 {#may-2025}

* Adobe integrations available with Journey Optimizer are now listed in the "Connect your systems and environments" section. [Read more](../integrations/ajo-integrations.md)

* The content integrations are now grouped in the Content Management section. [Read more](../integrations/content-integrations.md)

* Architecture diagrams for Adobe Experience Platform and Journey Optimizer have been updated. [Read more](../start/get-started.md#architecture)

* Added a video about the personalization editor playground to help you learn how to write and test personalization code using sample data. [Read more](../personalization/personalize.md#video-perso)

* The maximum number of addresses in a seed list has been increased from 50 to 300. [Read more](../configuration/seed-lists.md#create-seed-list)

* A new step detailing how to wrap code when using decision policies in the code-based experience editor has been added to the Create decision policies page. [Read more](../experience-decisioning/create-decision.md#create-decision)

* A note has been added to the Code-based experiences documentation to specify that when you have multiple code-based experience actions running on the same surface, the campaign or journey's priority score determines what is delivered to the end-user if they qualify for more than one action. [Read more](../code-based/code-based-surface.md#surface-definition)

* A new page on troubleshooting inbound actions in journeys provides a step-by-step guide to identify and resolve issues independently before reaching out to support. [Read more](../building-journeys/troubleshooting-inbound.md)

* A new [page](../code-based/code-based-decisioning-implementations.md) has been added to describe how to add the following flags to your client implementation when using decisioning in code-based experiences:

    * Adding the `dryRun` flag to test decisioning in code-based experiences. [Read more](../code-based/code-based-decisioning-implementations.md#code-based-test-decisions)

    * Apply deduplication to decisioning requests in code-based experiences. [Read more](../code-based/code-based-decisioning-implementations.md#code-based-decisioning-deduplication)

## April 2025 {#apr-2025}

* The Configuration chapter is now split into three chapters: [Channel configuration](../configuration/get-started-configuration.md), [Journey configuration](../configuration/about-data-sources-events-actions.md), and [Connect your systems](../configuration/ajo-apis.md).
* Added a caution note about using experience events in journey expressions and conditions. [Read more](../building-journeys/expression/expressionadvanced.md#discovering-the-interface)
* Added a note on the Direct mail configuration page about temporary storage of the output file. [Read more](../direct-mail/direct-mail-configuration.md)
* Added a tip in the journey advanced expression editor section about the condition format guidelines. [Read more](../building-journeys/expression/expressionadvanced.md)
* Added a caution note in the `inAudience` function section about impacts and best practices when renaming an audience. [Read more](../building-journeys/functions/functioninaudience.md)
* Added a recommendation about the native keywords usage when using two-way SMS. [Read more](../sms/sms-opt-out.md)
* Updated the journey test page with a note about the need for including an identity namespace in the event used. [Read more](../building-journeys/testing-the-journey.md)
* Currently, you cannot undelegate subdomains through the [!UICONTROL Journey Optimizer] user interface - you must reach out to your Adobe representative. Steps to undelegate a subdomain are now detailed for [Emails](../configuration/delegate-subdomain.md#undelegate-subdomain), [SMS](../sms/sms-subdomains.md#undelegate-subdomain), [Web experiences](../web/web-delegated-subdomains.md#undelegate-subdomain), and [Landing pages](../landing-pages/lp-subdomains.md#undelegate-subdomain).<!--[Read more](../configuration/delegate-subdomain.md#undelegate-subdomain)-->
<!--
* Added clarification about the optional `maxHttpConnections` parameter in the journeys Capping API, including guidance on how to use it alongside throttling configurations for the same endpoint. [Read more](../configuration/throttling.md)
* In the Decisioning section, added guidance explaining that approved offer items cannot be deleted if they are used in a collection or a decision. Included steps to change their status to "Draft" using the **[!UICONTROL Undo approve]** option. [Read more](../experience-decisioning/items.md#manage)
* Information on sandboxes have been grouped together into a new "Sandboxes management" section. This new section provides information on how to use and assign sandboxes, and how to use package export and import capabilitie to copy objects such as journeys, content templates, or fragments, across multiple sandboxes. [Read more](../administration/sandboxes.md)

## March 2025 {#mar-2025}

* The page about Audience Qualification events has been updated with new recommendations. [Read more](../building-journeys/audience-qualification-events.md)
* Custom action troubleshooting capability is now available to all customers (GA). [Read more](../action/troubleshoot-custom-action.md)
* Data Hygiene is now Data Lifecycle in the product user interface. The documentation has been updated to reflect this change. [Read more](../privacy/data-hygiene.md)
* The missing Landing Page built-in permissions have been added to the documentation. [Read more](../administration/ootb-permissions.md)
* A note has been added about scheduling recurring campaigns. [Read more](../campaigns/create-campaign.md)
* The section about inserting links and enabling tracking in an email message has been updated and reorganized. [Read more](../email/message-tracking.md)
* The section about personalization capabilities into Adobe Journey Optimizer has been reorganized and improved. [Read more](../personalization/personalize.md)
* Decision management API to list personalized offers has been updated with a sample to perform pagination if multiple personalized offers are missing from the response. [Read more](../offers/api-reference/offers-api/personalized-offers/offers-list.md)
* A new page gathering all information regarding the List unsubscribe feature has been created for improved clarity. [Read more](../email/list-unsubscribe.md)
* The Frequency capping section has been updated with information on how the frequency capping counter is updated for the Decisioning and Batch Decisioning APIs, in addition to the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)

## February 2025 {#feb-2025}

* The Read Audience activity guardrails have been updated to specify that only one activity can be used in a journey and that it can target only one audience. [Read more](../building-journeys/read-audience.md)
* Journey guardrails when using Adobe Campaign activities have been updated. [Read more](../start/guardrails.md#ac-g)
* Steps to create your first journeys have been detailed, and links to documentation section have been added. [Read more](../building-journeys/journey-gs.md)
* A new page is now available to detail the journey dashboard and filtering user interface. [Read more](../building-journeys/journey-ui.md)
* Documentation for **[!UICONTROL Send-Time optimization]** and its related FAQ have been updated, improved and moved to a new dedicated page. [Read more](../building-journeys/send-time-optimization.md)
* New guardrails have been added for journey events. [Read more](../start/guardrails.md#events-g)
* The built-in channel actions page has been reorganized. [Read more](../building-journeys/journeys-message.md)
* Guardrails & limitations have been added in the Decisioning and Decision management sections.
    * [Decisioning guardrails & limitations](../experience-decisioning/decisioning-guardrails.md)
    * [Decision management guardrails & limitations](../offers/decision-management-guardrails.md)
* A new section on context data has been added in the Decision management documentation. It provides information on how to leverage context data in the decisioning engine, for example to design a decision rule that requires the current weather to be ≥80 degrees at the time the decision request is made. [Read more](../offers/context-data.md)

## January 2025 {#jan-2025}

* A new section on the **[!UICONTROL Execution address]** option in the email configuration has been added. The primary address is defined at the sandbox level, but the default setting can be overidden for a specific email configuration. [Read more](../email/email-settings.md#execution-address)

* The **Get started with deliverability** page has been updated with the possibility to create IP warmup workflows directly from the user interface. [Read more](../reports/deliverability.md#reputation)

* The **Header parameters** section has been updated to reflect the new labels and changes in the user interface. [Read more](../email/email-settings.md#email-header)

* The **Forward email** section has been updated to specify that all emails sent to the **From email** address are forwarded to the forward email address. If no forward email is specified, these emails are discarded. [Read more](../email/email-settings.md#email-settings)

* The maximum size of contextual attributes passed into an API-triggered campaign request has been updated to 200kb. [Read more](../campaigns/api-triggered-campaigns.md#contextual)

* A new section has been added to the **Manage fragments** page to describe how to add new attributes to a live fragment. The whole page has also been improved. [Read more](../content-management/manage-fragments.md#adding-new-attributes)

* A "Guardrails & limitations" section has been added to the conflict management & prioritizations tools documentation. [Read more](../conflict-prioritization/gs-conflict-prioritization.md)

* A new end-to-end use case has been added to present all the steps needed to use Decisioning in content experiments with the [!DNL Journey Optimizer] code-based experience channel. [Read more](../experience-decisioning/experience-decisioning-uc.md)

* The **Configure email settings** page has been divided into several sub-pages for improved readability, including new standalone pages dedicated to [List unsubscribe](../email/list-unsubscribe.md), [Header parameters](../email/header-parameters.md) and [URL tracking](../email/url-tracking.md).

## December 2024 {#nov-2024}

* A note has been added to help troubleshoot a potential error message when making an API call to enable datasets for personalization using Adobe Experience Platform data. [Read more](../personalization/aep-data-perso.md)

## October 2024 {#oct-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] October '24 release have been detailed in the documentation. [Read more](release-notes.md)
* All communication channels available in [!DNL Journey Optimizer] are now grouped in a dedicated section of the documentation. [Read more](../channels/gs-channels.md)
* The **Configure your code-based experience** page has been improved to make the process clearer, including the section explaining what a surface URI is. [Read more](../code-based/code-based-configuration.md)
* The **Create web channel configuration** page has been updated to clarify the steps when creating a pages matching rule, which also apply to Code-based experience configuration. [Read more](../web/web-configuration.md#web-page-matching-rule)
* A note about the upcoming time-to-live (TTL) guardrail for system-generated datasets has been added. [Read more](../data/get-started-datasets.md)
* A new section has been added to describe how to preview your code-based personalized experiences right on your browser or on your mobile devices, using the **Preview on device** option when simulating content in a journey or a campaign. [Read more](../code-based/test-code-based.md#preview-on-device)
* A new page has been added on how to leverage Custom upload audiences for decisioning. [Read more](../offers/custom-upload-decisioning.md)
* A new page has been added to introduce the decision capabilities available in Journey Optimizer. [Read more](../experience-decisioning/gs-decision.md)
* Guardrails and limitations have been added to the Decisioning documentation. [Read more](../experience-decisioning/gs-experience-decisioning.md#guardrails)

## September 2024 {#sept-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] Sept '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a section about journey retry management. [Read more](../building-journeys/read-audience.md#read-audience-retry)
* The FAQ about Capping/throttling rule for custom actions has been updated to mention the default capping rule. [Read more](../configuration/external-systems.md#faq)
* The Control access section has been updated with permissions related to AI Assistant Content Generator. [Read more](../administration/high-low-permissions.md#ai-orchestrated-campaign)
* A video about AI Assistant Content Generator for email generation has been added. [Read more](../content-management/generative-full-content.md#video)

<!--

## August 2024 {#aug-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] August '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Performance guardrails for Decision management have been updated to mention Decisioning APIs delivery throughputs with/without Edge Segmentation. [Read more](../start/guardrails.md#decision-management)
* Journey guardrails have been updated. [Read more](../start/guardrails.md#journeys-guardrails-journeys)


## July 2024 {#july-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] July '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A personalization use case has been added on how to personalize an email with information related health plans and prescriptions. [Read more](../personalization/perso-uc-plan-prescriptions.md)

## June 2024 {#june-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] June '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A note about the usage of merge policies in journeys has been added on [this page](../building-journeys/journey-properties.md#merge-policies).
* The page about how to configure a **Wait** activity in a journey has been reorganized and improved. [Read more](../building-journeys/wait-activity.md)
* A new page has been created to detail journey's properties. [Read more](../building-journeys/journey-properties.md)

## May 2024 {#may-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] May '24 release have been detailed in the documentation. [Read more](release-notes.md)
* The section on seed lists has been updated regarding recurring journeys. [Read more](../configuration/seed-lists.md#use-seed-list)
* The setion on external data sources has been updated. [Read more](../datasource/external-data-sources.md#custom-authentication-access-token)
* The global journey timeout of 30 days has been added to the Guardrail and limitation page. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* The section on the Adobe Campaign v7/v8 integration has been updated with information on provisionning. [Read more](../action/acc-action.md#access)
* The expression editor used to personalize content has been renamed in the documentation to "personalization editor" to clearly differenciate it from the [Journey expression editor](../building-journeys/expression/expressionadvanced.md). [Read more](../personalization/personalization-build-expressions.md)

## April 2024 {#april-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] April '24 release have been detailed in the documentation. [Read more](release-notes.md#apr-2024)
* Configuration steps for In-app messaging have been detailed. [Read more](../in-app/inapp-configuration.md)
* Documentation for [Offer decisioning APIs](../offers/api-reference/offer-delivery-api/decisioning-api.md) and [Batch decisioning APIs](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md) have been updated.
* Information has been added in the Decision management documentation regarding edge and hub regions management when using frequency capping with the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)
* Information has been added on identity creation with custom namespaces when working with API-triggered campaigns. [Read more](../campaigns/api-triggered-campaigns.md)
* Screeshots have been updated to reflect the improved Journey canvas.
* Naming constraints has been updated in the following page: [Configure a unitary event](../event/about-creating.md), [Configure a business event](../event/about-creating-business.md#gs-business-events), [Configure a custom action](../action/about-custom-action-configuration.md#configuration-steps), [External data sources](../datasource/external-data-sources.md)
* A note has been added on Send Time Optimization availability. [Read more](../building-journeys/send-time-optimization.md)
* A new technical use case has been added on how to create a custom action to send data to Experience Platform. [Read more](../building-journeys/custom-action-aep.md)

## March 2024 {#march-2024}
 
* A Frequently Asked Questions section has been added to address common questions regarding the use of audience composition and custom upload audiences in Journey Optimizer. [Read more](../audience/about-audiences.md#faq)
* All new features and improvements coming with [!DNL Journey Optimizer] March '24 release have been detailed in the documentation. [Read more](release-notes.md#mar-2024)
* The page on profile entrance management has been improved. [Read more](../building-journeys/entry-management.md)
* Troubleshooting information has been added to the Alerts page. [Read more](../reports/alerts.md#alert-profile-error-rate)
* Information on the Wait activity has been added to the page on journey reports. [Read more](../reports/sharing-overview.md)
* For Journeys in test mode, following shortcuts have been disabled:
    * T: Shortcut to toggle the test mode on or off.
    * E: Shortcut used to trigger an event in an event-based journey.
    * P: Shortcut to trigger an event in an audience-based journey for which the Single profile at a time option is turned on.
    * L: Shortcut designated to display the test logs.
* The Message frequency rules page has been updated with a new subsection on daily frequency cap, which is available on demand in addition to weekly or monthly capping.
* The Work with consent policies page has been improved and updated with useful links to the Experience Platform documentation. [Read more](../action/consent.md)
* A new section has been added to reflect the fact that you can display HTML email content templates as thumbnails with the Grid view mode (Limited Availability). [Read more](../content-management/content-templates.md#template-thumbnails)
* A new section has been added to the Deliverability page to explain what feedback loops are and how to leverage them. [Read more](../reports/deliverability.md#feedback-loops)
* A note has been added to the Create personalized offers section to specify that the size of an offer including all its representations cannot exceed 300KB. [Read more](../offers/offer-library/creating-personalized-offers.md#create-offer)

## February 2024 {#feb-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] February '24 release have been detailed in the documentation. [Read more](release-notes.md#feb-2024)
* The Journey Optimizer + Workfront integration has been added to the integrations page. [Read more](../integrations/ajo-integrations.md)
* Information has been added on how to personalize offers' representations based on context data. [Read more](../offers/offer-library/add-representations.md#context-data)
* The guardrails page has ben updated with a note on custom actions which support JSON format only when using request or response payloads. [Read more](../start/guardrails.md#custom-actions-g)
* Additional information has been added about the basic authentication type in external datasources. [Read more](../datasource/external-data-sources.md)
* A note has been added to clearly differenciate the [Journey expression editor](../building-journeys/expression/expressionadvanced.md) from the [personalization editor](../personalization/functions/functions.md).
* The list of functions available in the advanced expression editor has been updated. [Read more](../building-journeys/expression/functions.md)
* The page on the Split function has been updated. [Read more](../building-journeys/functions/functioninaudience.md)
* Information has been added regarding the impact of the opt-in or opt-out of push notifications on In-app messages. [Read more](../in-app/create-in-app.md)
* The Message frequency rules page has been updated to reflect the Duration options available in the user interface (weekly or monthly).
* The Edit a PTR record section has been updated to clarify the fact that PTR records cannot be created manually and that you need to edit PTR records to assign them new subdomains. [Read more](../configuration/ptr-records.md#edit-ptr-record)

## January 2024 {#jan-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] January '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A guardrail about the journey size has been added. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* Journey timeout management has been detailed [in the following section](../building-journeys/journey-properties.md#global_timeout).
* Journey Optimizer [documentation home](../../ajo-home.md) page has been redesigned.
* Recommendations about the Update Profiles activity have been added. [Read more](../building-journeys/update-profiles.md) 
* Information has been added regarding the behavior of timeouts on event activities in journeys. When no event is received during the specified timeout period, individuals will continue the journey if no timeout path is defined. [Read more](../building-journeys/general-events.md#events-specific-time)
* In-app channel configuration prerequisites have been updated with a note about the usage of a custom Dataset preference merge policy. [Read more](../in-app/inapp-configuration.md)
* More details have been added about how to manipulate collections in a custom action response. [Read more](../action/action-response.md#exp-syntax).
* A link to the [Schema Dictionary for Adobe Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=nl-NL) has been added to the home page.
* An outdated reference to the AJO Message resource has been removed from the list of resources available in the Audit Log. When an update is done on a message in a journey, a **Journey** log is created. [Read more](../privacy/audit-logs.md)
* Additional recommendations have been added about the usage of the **Read Audience** activity. [Read more](../building-journeys/read-audience.md#must-read)
* The Get started with Adobe Experience Platform audiences page has been improved with a list of audience generation methods. [Read more](../audience/about-audiences.md)
* Best practices have been added when choosing an endpoint to target using a custom action. [Read more](../action/about-custom-action-configuration.md)
* An note has been added to notify users that events cannot be fired from external systems using an API. [Read more](../building-journeys/testing-the-journey.md#important_notes)
* Information on the **currentActionField** function has been added to the list of [collection management functions](../building-journeys/expression/collection-management-functions.md). An expression sample leveraging the function has been added in the [Use API call reponses in custom actions](../action/action-response.md) page.
* Update custom authentication doc regarding cache duration. [Read more] (../datasource/external-data-sources.md)
* Support of `listObject` has been modified in multiple functions.
* Update the **duration** parameter in the `toString` function. [Read more](../building-journeys/functions/conversion-functions.md#toString)
* For some external data sources use-cases, usage of custom actions is recommended.
* Event field syntax has been updated. The following syntax is deprecated `@(my_event.myfield}` and replaced by `@event{my_event.myfield}`. [Read more](../building-journeys/expression/field-references.md)

+++ 2023

## November 2023 {#nov-2023}

* The guardrail that limits all custom actions has been changed from 150,000 calls over 30 seconds to 300,000 calls over one minute. In addition, the default capping no longer applies to each endpoint. It is now performed per host and per sandbox. For example, on a sandbox, if you have two endpoints with the same host (eg: `https://www.adobe.com/endpoint1` and `https://www.adobe.com/endpoint2`), the capping will apply for all endpoints under the adobe.com host. "endpoint1" and "endpoint2" will share the same capping configuration and having one endpoint reach the limit will have an impact on the other endpoint. [Read more](../action/about-custom-action-configuration.md)
* A new status for email campaigns has been added to the list of campaigns' statuses. [Read more](../campaigns/manage-campaigns.md#modify-an-action-campaign)
* The Get started with Adobe Experience Platform audiences section has been updated to reflect the audience evaluation methods available and how to select them. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* A new subsection has been added to specify which events should be avoided when building your audience if you are using the streaming segmentation evaluation method. [Read more](../audience/about-audiences.md#streaming-segmentation-events-guardrails)

## October 2023 {#oct-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] October '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added GIFs to illustrate some key capabilities, such as: [Content templates](../content-management/content-templates.md), [Fragments](../content-management/fragments.md), [Computed attributes](../audience/computed-attributes.md), [Direct mail](../direct-mail/get-started-direct-mail.md), [Tags](../start/search-filter-categorize.md#tags), [Decision management optimization models](../offers/ranking/personalized-optimization-model.md), [API-triggered campaigns](../campaigns/api-triggered-campaigns.md), and [Content experiment](../content-management/content-experiment.md).
* The Schema creation process has been updated to reflect latest updates in the user interface, coming with Adobe Experience Platform changes. [Read more](../audience/creating-test-profiles.md) 
* Decision management guardrails have been added to the Guardrails and limitations page. [Read more](../start/guardrails.md#decision-management)
* The Header parameters section has been updated to reflect how out-of-office notifications and challenge responses are handled (they are received on the **[!UICONTROL Error email]**). [Read more](../email/email-settings.md#email-header)
* A new section on how to preview and test your content has been created. [Read more](../content-management/preview-test.md)
* The Implement single-page applications page has been moved to the Adobe Experience Paltform Web SDK documentation. [Read more](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html?lang=nl-NL){target="_blank"}
* The Capping section has been updated to reflect the label changes relating to offer capping in the Decision management interface. [Read more](../offers/offer-library/add-constraints.md#capping)
* The Add dynamic content into emails has been updated with details on how to delete a variant. [Read more](../personalization/dynamic-content.md#emails)
* The example for capping & throttling configurations has been updated. [Read more](../configuration/external-systems.md)
* The limitation regarding scalar arrays has been removed from the external data source section. [Read more](../datasource/external-data-sources.md)
* The multi-channel journey use case has been updated. [Read more](../building-journeys/journeys-uc.md)
* The Journey Optimizer documentation set has been updated to reflect the new Experience Platform schema creation process. 

## September 2023 {#september-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] September '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added with scaling best practices and real-time stitching guidance. [Read more](../start/best-practices.md)
* A Frequently-Asked-Questions section has been added for Send-Time Optimization. [Read more](../building-journeys/journeys-message.md#faq-send-time)
* A note has been added for the audience qualification activity. It may take up to 10 minutes to be active and listen to profiles entering or exiting the audience. [Read more](../building-journeys/audience-qualification-events.md#batch-speed-segment-qualification)
* A list of limitations to be aware of when creating decision rules has been added to the Decision management documentation. [Read more](../offers/offer-library/creating-decision-rules.md)
* Links to access control documentation have been updated. [Read more](../administration/permissions.md)
* In-app channel prerequisites have been updated with Adobe Experience Platform Data Collection details. [Read more](../in-app/inapp-configuration.md)
* Some expressions presented in ranking formula examples have been updated to avoid validation errors. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* A warning has been added to the Define decision scopes section to specify that if AI model is used in an evaluation criteria group, all the evaluation criteria in that group must use the AI ranking method, with the same specific AI model. Moreover, only one evaluation criteria group can use AI model. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## August 2023 {#august-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] August '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The note about **authentication cache management** in journey has been updated to detail that the token is not shared between different journeys. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* The page about journey **entry management** has been updated to clarify behavior. [Read more](../building-journeys/entry-management.md)
* Offer decisioning **export datasets** are now enabled by default. The note about the previous behavior has been removed.  [Read more](../offers/export-catalog/get-started-export.md)
* Various **campaign report metrics** have been renamed, in both Live and Global reports. [Read more](../reports/campaign-live-report.md)
* A new section has been added on content experiment prerequisites for the web channel. [Read more](../web/web-prerequisites.md#experiment-prerequisites)
* A warning has been added on the **Work with content templates** page to indicate that currently tracking is not supported when testing email content templates. To test tracking, you must use the content template in an email and send a proof. [Read more](../content-management/content-templates.md#content-templates)
* Several warnings have been added in the **Create and publish landing pages** section to specify that you cannot access your landing page by simply copy-pasting into a web browser the URL defined when creating the page, even if published. Instead you can test it using the preview function. [Read more](../landing-pages/create-lp.md)
* A new section has been added on how to **manage consent** for the direct mail channel. [Read more](../direct-mail/test-send-direct-mail.md)

## July 2023 {#july-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] July '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The wait activity documentation page has been improved with additional information and best practices related to the global timeout and reentrance usage. [Read more](../building-journeys/wait-activity.md)
* The page on entry management has been improved. [Read more](../building-journeys/entry-management.md)
* Additional information has been added about the throttling rate in the Read audience activity documentation. [Read more](../building-journeys/read-audience.md)
* Additional information has been added about retries. [Read more](../start/guardrails.md#general-actions-g)
* The **Implement personalization consent** section has been updated to describe how to manually enforce personalization consent in campaigns: you can use the segment rule builder to create an audience containing opt-out profiles or add a split activity to a composition workflow. [Read more](../privacy/opt-out.md#opt-out-expression-editor)

## June 2023 {#june-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] June '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the discard rate ratio in the Journeys overview screen. [Read more](../building-journeys/journey-gs.md#journey-access)
* A note has been added with the steps to follow if you modify your schema with new enumeration values after creating an event [Read more](../event/about-creating.md)
* A recommendation has been added to use journeyVersionID instead of journeyVersionName when querying journeys. [Read more](../reports/sharing-common-fields.md#journeyversionid-field)
* Additional examples on the evaluation criteria order have been added to the **Create decisions** section to illustrate cases where multiple criteria and multiple decision scopes are used. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* Decision management documentation has been clarified with a note specifying that the use of Object Level Access Control is not available for dynamic collections. [Read more](../offers/offer-library/creating-collections.md)

## May 2023 {#may-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] May '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added to describe how to set up the subdomain that will be used to publish content coming from the Adobe Experience Manager Assets Essentials in your web experiences. [Read more](../web/web-delegated-subdomains.md)
* A new subsection has been added to explain how to add personalized tracking parameters to URLs in the Email Designer. [Read more](../email/message-tracking.md#url-tracking)
* A new section has been added to describe how to ensure that the choice of your customers who opt out from having their profile data used for personalization is honored. [Read more](../privacy/opt-out.md#opt-out-personalization)
* A note has been added about using special international characters in URLs included in email contents. [Read more](../email/message-tracking.md#insert-links)
* The permission needed to test and publish landing pages has been added. [Read more](../landing-pages/create-lp.md)
* A note has been added about the Adobe Experience Platform endpoints needed to have your custom events accounted for in Decision management frequency capping. [Read more](../offers/data-collection/schema-requirement.md#track-custom-events)

## April 2023 {#apr-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] April '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A note has been added to specify that built-in actions cannot be removed. [Read more](../start/guardrails.md#custom-actions-g)
* Information has been added on serviceEvents as well as a query example to check the details of a serviceEvent. [Read more](../reports/query-examples.md#common-queries) 
* A note has been added to specify that you cannot perform queries on time series. [Read more](../building-journeys/condition-activity.md)
* Adobe Experience Manager Assets Essentials and Adobe Stock have been added to the multi-solution integration page. [Read more](../integrations/ajo-integrations.md)
* The warning on multi-level email subdomains not being allowed has been removed as they are now supported. [Read more](../configuration/delegate-subdomain.md)
* A note has been added to specify that, if changes are made to an offer decision which is being used in a journey's message, you need to unpublish the journey and republish it. [Read more](../building-journeys/publish-journey.md)
* Explanation on how to make sure events are correctly accounted for in the capping counter has been clarified in the Decision management **Capping event** section. [Read more](../offers/offer-library/add-constraints.md#capping-event)
* A new section has been added to the **Change execution addresses** page. It specifies that it is possible to override the execution field set globally in the journey advanced parameters, but the email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. [Read more](../configuration/primary-email-addresses.md#override-execution-address-journey)
* The **URL tracking** section now provides the list and description of all contextual attributes that can be set for URL tracking in an email channel configuration. [Read more](../email/email-settings.md#url-tracking)

## March 2023 {#march-2023}

* The Journey Optimizer schema dictionary is now available. You will find the complete list of fields and attributes for each schema.  [Read more](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=nl-NL)
* All new features and improvements coming with [!DNL Journey Optimizer] March '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a step to enable Adobe Analytics events in your journeys. [Read more](../event/about-analytics.md)
* A new section has been created in the Decision management guide on how to collect offer decisioning feedback in Adobe Experience Platform, including which offers are displayed and how users interact with them. [Read more](../offers/data-collection/data-collection.md)
* A new subsection has been added to the **Create decision** section to explain the difference between evaluating criteria in a sequential order or at the same time. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* A guardrail has been added for read audience journeys with incremental read. You cannot create a new version, you need to duplicate the journey. [Read more](../start/guardrails.md#journey-versions-g)
* The use case on how to limit throughput put has been updated with information on throttling capabilities. [Read more](../building-journeys/limit-throughput.md)
* A note has been added to specify that scalar arrays are not supported in response payload definition. [Read more](../datasource/external-data-sources.md)
* The section on profile cap conditions has been updated. [Read more](../building-journeys/condition-activity.md#profile_cap)

## February 2023 {#feb-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the canvas toolbar. [Read more](../building-journeys/using-the-journey-designer.md#gs-journey-design)
* Information has been added to state that internal Adobe addresses are not allowed in URLs and APIs. [Read more](../start/guardrails.md)
* A note has been added in the API-triggered campaigns documentation to specify that contextual attributes passed into the request cannot exceed 50kb. [Read more](../campaigns/api-triggered-campaigns.md#contextual)
* Information was added on how opt-out information is stored in the **Consent Service Dataset** after recipients are unsubscribed through a landing page. [Read more](../landing-pages/lp-use-cases.md#configure-opt-out)

## January 2023 {#jan-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added on custom authentication endpoints in the capping documentation. [Read more](../configuration/external-systems.md)
* A new custom authentication example has been added in the external datasources section. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* A note has been added about Data Collection Core Service (DCCS) for event-triggered journeys. [Read more](../start/guardrails.md#events-g)
* A note on identity namespace retrieval has been added in the [Read audience](../building-journeys/read-audience.md), [Audience qualification](../building-journeys/audience-qualification-events.md) and [Event creation](../event/about-creating.md) sections.
* Accessibility features in [!DNL Journey Optimizer] are now grouped in a dedicated page. [Read more](../start/accessibility.md)
* The examples have been updated in the Operators section of the advanced expression editor documentation. [Read more](../building-journeys/expression/operators.md)
* A note has been added about the limitation on lookup with array of objects. [Read more](../event/experience-event-schema.md#relationships_limitations)
* Added a new page about data management in [!DNL Journey Optimizer]. [Read more](../data/gs-data.md)
* Added a table listing all codes that can be returned in the response when delivering offers using the Decisioning API. [Read more](../offers/api-reference/offer-delivery-api/decisioning-api.md)

+++

+++ 2022

## December 2022 {#december-2022}

* The Messages guide has been reorganized and split into dedicated guides for each channel:

    * [Email channel](../email/get-started-email.md)
    * [Push notification channel](../../rp_landing_pages/push-landing-page.md)
    * [SMS channel](../sms/get-started-sms.md)

* The Configuration guide has been reorganized for improved readability. [Read more](../configuration/get-started-configuration.md)

## November 2022 {#november-2022}

* Added a new page about Journey Optimizer integrations. [Read more](../integrations/ajo-integrations.md)
* Added a recommendation about the length of mirror pages URLs. [Read more](../email/message-tracking.md)
* A new subsection in the email settings configuration has been added on the reply to email address, including recommendations to ensure proper reply management. [Read more](../email/email-settings.md#send-to-suppressed-email-addresses)
* Added a section on how to modify the content of a message in a live journey. [Read more](../building-journeys/journeys-message.md#update-live-content)

## October 2022 {#october-2022}

* Added a journey use case on how to limit throughput using External Data Sources and Custom Actions. [Read more](../building-journeys/limit-throughput.md)
* The journey use case section has been reorganized into two categories: [Business use cases](../building-journeys/journeys-uc.md) and [Technical use cases](../building-journeys/collections.md).
* The **Entity Dataset** section has been updated with more details. [Read more](../data/datasets-query-examples.md#entity-dataset)
* The opt-out management and consent policies sections have been reorganized. [Read more](../privacy/opt-out.md)
* The section on advanced parameters in journey messages has been clarified and now specifies that email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. 
* Added a note to the **Configure landing page subdomains** section to specify that capital letters are not allowed in landing page subdomains. [Read more](../landing-pages/lp-subdomains.md)

## September 2022 {#september-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] September '22 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a best practice related to the use of wait activities in recurring read audience journeys. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added new step event query examples as well as information on the difference between id, instanceid and profileid. [Read more](../reports/query-examples.md).
* Updated the pages related to the [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly) and [toString](../building-journeys/functions/conversion-functions.md#toString) functions.
* Added details on the time condition parameters. [Read more](../building-journeys/condition-activity.md#time_condition)
* Added information on built-in datasets. [Read more](../data/get-started-datasets.md#access-datasets)
* The Global report and Live report sections have been improved and reorganized. [Read more](../reports/report-gs-cja.md)
* A list of every reporting metric available in Adobe Journey Optimizer has been added.
[Read more](../reports/report-gs-cja.md#email-and-sms-metrics)
* The BCC email section has been moved to the new Support for archiving page. [Read more](../configuration/archiving-support.md)

## August 2022 {#august-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] August '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The Frequency rules section has been updated to reflect the new in-line messaging flow.
* A video showing how to configure subscriptions and create landing pages is now referenced in the Get started with landing pages section. [Read more](../landing-pages/get-started-lp.md#video)
* A limitation has been added for journeys using Read Audience activities. [Read more](../building-journeys/read-audience.md)
* The expression editor operators page has been improved. [Read more](../building-journeys/expression/operators.md)
* A section on how to schedule a campaign has been added. [Read more](../campaigns/create-campaign.md)
* General syntax rules section for expression editor has been updated to take into account the new rule regarding the backslash symbol escaping in literal functions. The existing published messages are not impacted by this change. Only the new or draft messages must be updated. [Read more](../personalization/personalization-syntax.md#general-rules)

## July 2022 {#july-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] July '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Set up channel configurations** section has been clarified and updated with links to the page describing how to configure the SMS channel. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* In the journey properties, the **Profile Time zone** option is now disabled by default. [Read more](../building-journeys/timezone-management.md#timezone-from-profiles)
* In the **Wait** activity, the **Fixed date** option is no longer available. [Read more](../building-journeys/wait-activity.md)
* Added more information on the **Incremental read** option in the **Read audience** activity. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added recommendations on the **Profile cap** condition type. [Read more](../building-journeys/condition-activity.md#profile_cap)
* Added a limitation on business events. [Read more](../start/guardrails.md#events-g)

## June 2022 {#june-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] June '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new section about Privacy requests has been added to the documentation. [Read more](../privacy/requests.md)
* A new section about Audit logs on resources has been added to the documentation. [Read more](../privacy/audit-logs.md)
* A new section about how to add HTML or JSON content coming from Adobe Experience Cloud Asset library to an offer representation has been added to the documentation. [Read more](../offers/offer-library/add-representations.md#html-json)
* Added a new page on journey lifecyle. [Read more](../building-journeys/journey.md)
* Updated the Wait activity page. [Read more](../building-journeys/wait-activity.md)
* Added the list of Adobe Journey Optimizer datasets with query examples. [Read more](../data/datasets-query-examples.md)
* The Allowed list page has been moved to the Configuration section. [Read more](../configuration/allow-list.md)
* The Suppression list page has been updated to clarify some information, including the fact that all ASCII characters comprised between 32 and 126 are allowed in the reason for suppression field. [Read more](../configuration/manage-suppression-list.md)
* The link to guardrails and static limits for Decision management has been added. [Read more](../start/guardrails.md)
* Send-Time Optimization is now available for all customers. The beta mention has been removed. [Read more](../building-journeys/send-time-optimization.md)
* The Batch Decisioning API has been added to the list of available APIs to delivery personalized offers. [Read more](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## May 2022 {#may-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] May '22 release have been detailed in the documentation. [Read more](release-notes.md)
* New query examples related to [audience qualification](../reports/query-examples.md#segment-qualification-queries) and [events](../reports/query-examples.md#event-based-queries) have been added.
* The email design section now mentions new built-in templates available to start content with. Related screenshots have been updated. [Read more](../email/get-started-email-design.md)
* Links to key resources have been updated in Journey Optimizer documentation home page.
* Screenshots for landing page and subscription reporting have been updated. [Read more](../reports/live-report.md)
* A note has been added stating that the Delete method is not supported in custom actions. [Read more](../action/about-custom-action-configuration.md)
* Links to how-to videos have been updated.
* The [Email configuration](../configuration/about-subdomain-delegation.md), [Message presets](../configuration/channel-surfaces.md) and [Configure landing pages](../landing-pages/lp-subdomains.md) sections have been reorganized for improved readability.
* The URL tracking section has been updated and improved with examples. [Read more](../email/email-settings.md#url-tracking)
* A new subsection on setting up a forward email address has been added. Note that you cannot do it through the user interface. [Read more](../email/email-settings.md#email-settings)

## April 2022 {#april-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] April '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **reactions** event documentation page has been updated. [Read more](../building-journeys/reaction-events.md)
* Videos for Decision management capabilities have been updated to reflect Journey Optimizer user interface. [Read more](../offers/get-started/starting-offer-decisioning.md)
* The **Get Started with Datasets** section has been improved to detail how to access and create datasets. [Read more](../data/get-started-datasets.md)
* Links to help guides and product release notes have been added to the **Adobe Journey Optimizer Documentation** home page. [Read more](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=nl-NL)
* The **Create message presets** section now specifies that you cannot proceed with preset creation while the selected IP pool is under edition (**[!UICONTROL Processing]** status) and has never been associated with the selected subdomain. [Read more](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* The message presets **URL tracking** section has been updated to reflect minor changes in the user interface. [Read more](../configuration/channel-surfaces.md#url-tracking)

## March 2022 {#march-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] March '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page on getting started with AI models has been added to the **Offer decisioning** section, including a thorough description of the [auto-optimization model](../offers/ranking/auto-optimization-model.md), the algorithm it uses and more technical details. [Read more](../offers/ranking/ai-models.md)
* The test profile creation page has been moved to the  **Audience, profiles and identity** section. [Read more](../audience/creating-test-profiles.md)
* Added an example on how to add an expression as a default value in the expression editor. [Read more](../building-journeys/expression/field-references.md#default-value)
* The **Create personalized offers** section has been reorganized for improved readability. [Read more](../offers/offer-library/creating-personalized-offers.md)
* A new section has been added to describe the impacts that changing an offer's start and/or end dates may have on this offer's frequency capping. [Read more](../offers/offer-library/add-constraints.md#capping-change-date)
* The **Change the primary email addresses** section has been updated to reflect the user interface changes. [Read more](../configuration/primary-email-addresses.md)

## February 2022 {#feb-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The [replace](../building-journeys/functions/string-functions.md#replace) and [replaceAll](../building-journeys/functions/string-functions.md#replaceAll) function documentation pages have been updated with additional information and examples regarding the target parameter.
* Best practices have been added to the [Operators](../building-journeys/expression/operators.md#important-notes) page.

## January 2022 {#january-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Offer decisioning AI rankings** section has been updated with a more detailed description of the auto-optimization model. [Read more](../offers/ranking/auto-optimization-model.md)
* A new section on the schema requirements needed to be able to send in event types when using an AI model has been added. [Read more](../offers/data-collection/schema-requirement.md)
* The section related to [!DNL Journey Optimizer] personalization capabilities has been reorganized for better readability. [Read more](../personalization/personalize.md)
* The **Create message presets** section has been divided into several sections for improved clarity. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* The **Opt-out management** section has been clarified and slightly reorganized. [Read more](../privacy/opt-out.md#opt-out-decision-management)
* The **Insert links** section has been updated to reflect the recent user interface changes. [Read more](../email/message-tracking.md#insert-links)

+++

+++ 2021

## November 2021 {#november-2021}

* A full description of the **advanced expression editor** used in journeys is now available. [Read more](../building-journeys/expression/expressionadvanced.md)
* A new section about **CNAME subdomain delegation method** has been added. [Read more](../configuration/delegate-subdomain.md#cname-subdomain-setup)

## October 2021 {#october-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] Oct '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added **Date time function** list. [Read more](../personalization/functions/dates.md)
* New **Get Started sections per user persona**. Take your own path to get to your goals faster! [Read more](../start/quick-start.md)
* New **Edit a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New **Edit a PTR record** section. [Read more](../configuration/ptr-records.md#edit-ptr-record)
* New **Deactivate a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New limitations added to the **Decision Management API developer guide** on offer constraints not supported with the mobile [!DNL Experience Edge] workflows. [Read more](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* New **Create simulations** section. [Read more](../offers/offer-activities/simulation.md)
* Updated **Add decision scopes** section. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Updated **Define content for your representations** section, including a new [subsection](../offers/offer-library/creating-personalized-offers.md#custom-text) on how to define and personalize custom text. [Read more](../offers/offer-library/creating-personalized-offers.md#content)

## September 2021 {#september-2021}

* The following function pages have been updated: [sethours](../building-journeys/functions/date-functions.md#setHours), [getListItem](../building-journeys/functions/list-functions.md#getListItem), [inSegment](../building-journeys/functions/functioninaudience.md)

* The following functions have been added: [filter](../building-journeys/functions/list-functions.md#filter), [intersect](../building-journeys/functions/list-functions.md#intersect), [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly)

* The dateOnly date type has been added in the expression editor documentation. [Read more](../building-journeys/expression/data-types.md)

* Added details on custom action cache duration. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)

* Added information on custom action default ports. [Read more](../action/about-custom-action-configuration.md#url-configuration)

* Added information on multiple business event use cases. [Read more](../event/about-creating-business.md#multiple-business-events)

* Added commonly used examples to query Journey Step Events in Data Lake. [Read more](../reports/query-examples.md)

* Added a new **Limitations** page. [Read more](../start/guardrails.md)

* Improved the **Quick start** page with steps for different personas. [Read more](../start/quick-start.md)

* Now all the Decision management features described in the dedicated section also apply to the Adobe Experience Platform users leveraging the Offer Decisioning application. [Read more](../offers/get-started/starting-offer-decisioning.md)

* Added a subsection to clarify the differences between using audiences versus decision rules when applying a constraint to restrict the selection of offers for a given placement. [Read more](../offers/offer-activities/create-offer-activities.md#decision-list)

* Added specific ranking formula examples to illustrate some real-life use cases. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Added a subsection on how to edit IP pools. [Read more](../configuration/ip-pools.md#edit-ip-pool)

## August 2021 {#august-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] August '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Updated Decision management permissions. [Read more](../administration/ootb-product-profiles.md)
* Updated Email Designer screenshots with latest UI.
* Updated the configuration procedure for custom actions with dynamic URL paths and dynamic headers. [Read more](../action/about-custom-action-configuration.md#url-configuration)
* Added a section about accessibility features and shortcuts. [Read more](../start/user-interface.md#accessibility)
* Added a section about audience evaluation methods. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* Added notes to the Suppression list, Allowed list and Email global/live report sections to specify that profiles with Suppressed and Not allowed statuses are excluded from the Email report Sent metrics. [Read more](../reports/report-gs-cja.md)
* Added a new section to describe how to retrieve email addresses or domains that were excluded from a sending because they were not on the allowed list. [Read more](../configuration/allow-list.md#reporting)
* Updated the Enable the allow list section. [Learn more](../configuration/allow-list.md#enable-allow-list)
* Updated the Monitor message presets section with the possible preset creation failure reasons and details on such errors. [Read more](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Updated and renamed the Retry time period section to reflect the fact that you can now adjust the email retry setting in the message presets. [Read more](../configuration/retries.md#retry-duration)
* Updated the Delegate a subdomain section with more detailed information on the validation process performed by Adobe. [Read more](../configuration/delegate-subdomain.md#subdomain-validation)
* Added a section to describe how to manually add email addresses and domains to the suppression list. [Read more](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Updated the [Access the suppression list](../configuration/manage-suppression-list.md#access-suppression-list) section and [Retries](../configuration/retries.md) sections to reflect the new user interface.
* The new flow to add and configure representations when creating an offer has been documented. [Read more](../offers/offer-library/creating-personalized-offers.md#representations)

## July 2021 {#july-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] July '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added direct links to Experience Platform services documentation in [!DNL Journey Optimizer] home page and table of contents
* New landing pages for Experience Platform services available in [!DNL Journey Optimizer] 
* Added links to [!DNL Journey Optimizer] product description in the home page
* Added tutorial videos in multiple pages
* Optimized home page imagery
* Moved, improved and renamed 'Message tracking' section to 'Add links and track messages'. [Read more](../email/message-tracking.md)
* Added a subsection on mirror pages. [Read more](../email/message-tracking.md#mirror-page)
* Renamed 'offer activities' as 'decisions' and 'decisions' as 'decision scopes' in documentation and screens. [Read more](../offers/get-started/starting-offer-decisioning.md)
* New use case: [personalize a message with helper functions](../personalization/personalization-use-case-helper-functions.md)
* Updated the Read audience documentation to reflect materialized segment impacts. [Read more](../building-journeys/read-audience.md)
* Updated the Journey limitations. [Read more](../start/guardrails.md)
* Updated the Configure offers selection in decisions section. [Read more](../offers/offer-activities/configure-offer-selection.md)
* Added a warning to mention that event-based offers are not currently supported. [Read more](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Documented the Decision management new **[!UICONTROL Overview]** tab. [Read more](../offers/get-started/user-interface.md#overview)
* Added new sections to describe the actions available from the offer and decision lists: [Offer list](../offers/offer-library/creating-personalized-offers.md#offer-list) and [Decision list](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
-->
