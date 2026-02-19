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
source-git-commit: dfa33cb17c75d1d58b8893bbc190f003e5c3258e
workflow-type: tm+mt
source-wordcount: '5505'
ht-degree: 7%

---

# Documentatie-updates {#latest-updates}

Deze pagina bevat een overzicht van alle meest recente wijzigingen in de documentatie van [!DNL Journey Optimizer] , naast de updates die betrekking hebben op de functies en verbeteringen van de maandelijkse release.

## Februari 2026 {#february-2026}

* De pagina met beslissingsitems is bijgewerkt met informatie over het uitlijnen van het pushkanaal en de gebeurtenis Custom. [Meer informatie](../experience-decisioning/items.md#capping)

* De **de gebeurtenisraadpleging van de Ervaring in reizen** documentatie is bijgewerkt met de afgekeuringschronologie: beginnend 1 April, 2026, organisaties die geen eigenschappen van de ervaringsgebeurtenis in reisuitdrukkingen in de laatste 90 dagen hebben gebruikt zullen geen toegang meer tot dit vermogen hebben. De FAQ concentreert zich nu op de ouderdomschronologie en wie wordt beïnvloed, en de pagina van het de gebeurtenisschema van de Ervaring is gericht met een directe verbinding aan alternatieve benaderingen. [Meer informatie](../building-journeys/exp-event-lookup.md)

* De **Beslissende** documentatie is bijgewerkt voor **datasetraadpleging** met de gegevens van Adobe Experience Platform: de gesteunde kanaalbegeleiding verklaart nu dat de datasetraadpleging voor alle kanalen werkt waar het Beslissen (code-based ervaring, E-mail, Duw, SMS, en de activiteit van het Besluit van de Inhoud in reizen) beschikbaar is. De beperkte Beschikbaarheid en openbare bètanota&#39;s zijn verwijderd uit de besluitvormingsregels, rangschikkingsformules, en beslissingspunten pagina&#39;s. [Meer informatie](../experience-decisioning/aep-data-exd.md)

* De Externe pagina van de systeemintegratie is bijgewerkt met verbindingen met douanegegevensbronnen en douaneacties, en verduidelijkt dat de uitgangsvolmacht statische IP voor uitgaande vraag van **de acties van de Douane** aan uw externe systemen verstrekt. [Meer informatie](../configuration/external-systems.md)

* De documentatie bij de uitvoering Journey Dry is verduidelijkt: de kenmerken van de step-gebeurtenis `inDryRun` en `dryRunID` documenteren nu dat ze `true` / instantie-id retourneren in de modus Droog en `null` voor test- of live reizen. De richtlijnen voor het uitsluiten van Dry run step-gebeurtenissen bij het rapporteren van query&#39;s zijn dienovereenkomstig bijgewerkt. [Meer informatie](../building-journeys/journey-dry-run.md)

* **duw van het Web** is nu algemeen beschikbaar. De documentatie van het pushbericht is dienovereenkomstig geherstructureerd en bijgewerkt (begin, ontwerp, verzend, creeer). [Meer informatie](../push/get-started-push.md)

* De Web-push configuratiepagina is nu beschikbaar in de documentatie. [Meer informatie](../push/push-configuration-web.md)

* De documentatie over het gebruiken van fragmenten in Beslissing is bijgewerkt: de nota&#39;s zijn toegevoegd in de secties van Fragments en van Beslissing, en de Fragments in de pagina van besluitvormingsbeleid is bijgewerkt. [Meer informatie](../experience-decisioning/fragments-decision-policies.md)

* De documentatie van de sms-website-haak is bijgewerkt: de inhoud van de twilio-website is verwijderd. [Meer informatie](../sms/sms-webhook.md)

* **zet beelden in inhoudsmalplaatjes** documentatie om is verbeterd met uitgebreide gidsen en aanbevelingen, gemeenschappelijke gebruiksgevallen, en duidelijkere begeleiding voor het omzetten van beeldontwerpen in editable HTML inhoudsmalplaatjes. Er wordt ook vermeld dat u nu een thema kunt gebruiken als input voor de conversie. [Meer informatie](../content-management/image-to-html.md)

* De documentatie voor de migratie-API voor beslissingen is bijgewerkt. [Meer informatie](../experience-decisioning/decisioning-migration-api.md)

* De **activiteit van het Besluit van de Inhoud** is nu algemeen beschikbaar. De pagina Activiteit van het Besluit van de Inhoud is bijgewerkt met een sectie over Beslissingsgegevens beschikbaar in step gebeurtenissen. [Meer informatie](../building-journeys/content-decision.md)

* Koppelingen naar de API-documentatie voor loyaliteitsuitdagingen zijn toegevoegd aan de sectie Loyalty-uitdagingen (begin, maak uitdagingen, maak taken, maak de uitdagingen van de toegangloyaliteit). [Meer informatie](../loyalty-challenges/get-started.md)

* De ondersteunde kanaalgegevens in de documentatie van de wizard voor het maken van de campagne zijn gecorrigeerd. Aan de slag met kanalen en geordende campagnes op de pagina&#39;s met veelgestelde vragen zijn overeenkomstig bijgewerkt. [Meer informatie](../campaigns/get-started-with-campaigns.md)

* De toestemmingendocumentatie is verbeterd betreffende **Reis leidt** en **keurt** toestemmingen goed. [Meer informatie](../administration/ootb-permissions.md)

* De AEM (Adobe Experience Manager)-integratiedocumentatie is bijgewerkt met herziene naamgeving (AEM dynamic content en AEM fragments). [Meer informatie](../integrations/aem-fragments.md)

* Een nieuwe uitsluitingsreden is toegevoegd aan de uitsluitingslijst: **UnsubscribeLinkNotValid** (foutencode 050081). Deze uitsluiting wordt gegenereerd wanneer de lengte van het onderwerp List-Unsubscribe mailTo groter is dan de RFC-limiet van 998 tekens. [Meer informatie](../reports/exclusion-list.md)

* De documentatie van de functie formatDate helper is verbeterd met een opmerking dat de functie een datum-tijd veldtype (geen tekenreeks) vereist en met meerdere voorbeelden: een datum-tijd veld opmaken, een tekenreeks eerst omzetten in de datum, volledige datum met dagnaam, dynamische datum vanaf de systeemtijd en de dag-van-week-indeling, inclusief uitvoer in kleine letters. [Meer informatie](../personalization/functions/dates.md#format-date)

* De documentatie van e-mailberichten voor tekstversies is uitgebreid met uitgebreide instructies voor het gebruik van hoofdletters en kleine letters, waaronder beslissingscriteria voor het gebruik van gewone tekst in plaats van automatische synchronisatie, praktische voorbeelden met realistische scenario&#39;s en een sectie met veelgestelde vragen. [Meer informatie](../email/text-version-email.md#when-to-use)

* De documentatie over Designer-thema&#39;s via e-mail is bijgewerkt met informatie over de ondersteuningsbeperkingen voor weblettertypen en het belang van fallback-lettertypen. [Meer informatie](../email/apply-email-themes.md#themes-guardrails)

* Er is een beperking toegevoegd aan de documentatie van de hulpmiddel Metagegevens van de Uitvoering om te verduidelijken dat de meta-gegevens niet voor profielen worden gevangen die van de actie worden uitgesloten. [Meer informatie](../personalization/functions/helpers.md#execution-metadata)

* De op code-gebaseerde documentatie van implementatiemonsters is bijgewerkt om het tokens gebied in propositionAction voor nauwkeurige het volgen en attributie in Beslissing te omvatten. [Meer informatie](../code-based/code-based-implementation-samples.md#client-side-how)

* Er is een opmerking toegevoegd aan de URL-tracking en de documentatie voor het opzeggen van lijsten om te verduidelijken dat de volgorde van URL-volgparameters die aan URL&#39;s zijn toegevoegd, willekeurig is en niet kan worden gecontroleerd. [Meer informatie](../email/url-tracking.md)

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

* U kunt afbeeldingen nu omzetten naar HTML-sjablonen met de afbeelding naar HTML-converter. [Meer informatie](../content-management/image-to-html.md)

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

## Augustus 2025 {#august-2025}

* Er is een nieuwe pagina toegevoegd met de aanbevolen procedures voor het ontwerpen van toegankelijke e-mail en het plaatsen van pagina-inhoud met [!DNL Journey Optimizer] . [Meer informatie](../email/accessible-content.md)

* De documentatie voor aanvullende identificatiemiddelen voor reizen is met de volgende verduidelijkingen bijgewerkt:

   * Nadat u een aanvullende id aan een schema hebt toegevoegd, moet er een nieuwe gebeurtenis (voor door gebeurtenissen geïnitieerde reizen) of een nieuwe veldgroep (voor publiekstrajecten Lezen) worden gemaakt. Bestaande entiteiten worden niet automatisch vernieuwd en herkennen de nieuwe id niet.

   * Aanvullende id&#39;s worden niet gevalideerd op basis van het beleid voor etikettering en handhaving van gegevensgebruik (DULE) en worden niet meegenomen tijdens controles van gegevensbeheer op reizen.

[Meer informatie](../building-journeys/supplemental-identifier.md)

* De pagina Optimalisatie in campagnes werd bijgewerkt om aan te geven dat optimalisatie nu ook beschikbaar is voor reizen. [Meer informatie](../content-management/gs-message-optimization.md)

* Er is een koppeling toegevoegd naar de zelfstudie-video waarin wordt beschreven hoe berichten in een campagne kunnen worden geoptimaliseerd. [Meer informatie](../content-management/gs-message-optimization.md)

## Juli 2025 {#july-2025}

* De campagneinterface kenmerkt nu twee afzonderlijke lusjes: **Actie** en **API teweeggebracht**. De documentatie is dienovereenkomstig bijgewerkt, met informatie voor elk campagneretype dat in specifieke secties wordt georganiseerd om duidelijkheid en bruikbaarheid te verbeteren. [Meer informatie](../campaigns/get-started-with-campaigns.md)

* [&#x200B; wordt begonnen met subdomain delegatie &#x200B;](../configuration/about-subdomain-delegation.md) en [&#x200B; delegeer een subdomain &#x200B;](../configuration/delegate-subdomain.md) pagina&#39;s zijn bijgewerkt om de verschillende delegatiemethodes en de stappen beter voor te stellen om hen op te zetten.

* Er is een notitie toegevoegd aan de sectie Fragments, waarin wordt aangegeven dat wanneer het bijhouden is ingeschakeld in een reis of een campagne, als er koppelingen aanwezig zijn in een fragment en als dit fragment wordt gebruikt in een bericht, deze koppelingen worden bijgehouden, zoals alle andere koppelingen in het bericht. [Meer informatie](../content-management/create-fragments.md#content)

* De instructies en beperkingen die van toepassing zijn op subdomeindelegatie in Journey Optimizer zijn verrijkt en geconsolideerd in één specifieke sectie. [Meer informatie](../configuration/delegate-subdomain.md#guardrails)

* Er is een notitie toegevoegd aan de keuzelijsten voor het maken van fallback en het maken van beslissingspagina&#39;s om aan te geven dat fallback-aanbiedingen alle voorstellingen moeten bevatten die in een beslissing worden gebruikt. [Meer informatie](../offers/offer-library/creating-fallback-offers.md)

* De voor fragmenten geldende hulplijnen zijn verrijkt. [Meer informatie](../start/guardrails.md#fragments-guardrails).

* Er is een opmerking toegevoegd om op te geven dat koppelingen die aan berichten zijn toegevoegd, na 25 maanden verlopen en koppelingen naar spiegel-pagina&#39;s na 90 dagen. [Meer informatie](../email/message-tracking.md)

<!--* The possible email error types that could happen upon sending email deliveries with are now listed in a dedicated section. [Read more](../configuration/email-error-types.md)-->

## Juni 2025 {#june-2025}

* Er is een nieuwe sectie toegevoegd over het toevoegen en gebruiken van RTF-tekst (regeleinden, vet, cursief, enz.) aan aanpasbare fragmenten met HTML-componenten. [Meer informatie](../content-management/customizable-fragments.md#rich-text)

* Het beslissingsonderdeel is bijgewerkt met een specifieke sectie die is gewijd aan het samenstellen van AI-modellen. [Meer informatie](../experience-decisioning/ranking/ai-models.md)

* Er is een aanbeveling toegevoegd over het gebruik van het veld `actionExecutionTime` in de handeling voor de gebeurtenis tripStep. [Meer informatie](../reports/sharing-execution-fields.md#actionexecutiontime-field)

* Er is een notitie toegevoegd over de `messageID` die mogelijk niet uniek is voor elke afzonderlijke levering. [Meer informatie](../data/datasets-query-examples.md)

* Er is een aanbeveling toegevoegd over het beheer van historische gebeurtenissen in gegevenshygiënische activiteiten. [Meer informatie](../privacy/data-hygiene.md#data-hygiene-recommendations)

* Er is een hulplijn toegevoegd over het plaatsen van pagina&#39;s die niet worden ondersteund voor migratie tussen sandboxen. [Meer informatie](../configuration/copy-objects-to-sandbox.md#global)

* Er is een waarschuwing toegevoegd over geneste JSON-objecten die niet worden ondersteund in aangepaste verificatie voor aangepaste handelingen. [Meer informatie](../datasource/external-data-sources.md)

* Er is een waarschuwing toegevoegd over de naamgeving van voorwaardelijke inhoudvarianten in de e-mailontwerper. [Meer informatie](../personalization/create-conditions.md)

* De sectie &quot;Undelegate a landing page subdomain&quot; is bijgewerkt. [Meer informatie](../landing-pages/lp-subdomains.md#undelegate-subdomain)

* Verduidelijkt de regels van de reisterugkeer wanneer het gebruiken van extra herkenningstekens. [Meer informatie](../building-journeys/supplemental-identifier.md#guardrails)

* Er is een nieuwe notitie toegevoegd om te verduidelijken dat u de expressie-editor in de modus Geavanceerd moet gebruiken wanneer u het extra kenmerk Id selecteert tijdens de gebeurtenisconfiguratie. [Meer informatie](../building-journeys/supplemental-identifier.md#add)

* Opheldering toegevoegd over de manier waarop de aansluiting van de reis werkt met aanvullende identificatiecodes. [Meer informatie](../building-journeys/supplemental-identifier.md#guardrails)

## Mei 2025 {#may-2025}

* Adobe-integratie die beschikbaar is met Journey Optimizer wordt nu vermeld in de sectie &quot;Connect your systems and environment&quot;. [Meer informatie](../integrations/ajo-integrations.md)

* De integratie van de inhoud wordt nu gegroepeerd in de sectie Inhoudsbeheer. [Meer informatie](../integrations/content-integrations.md)

* Architectuurdiagrammen voor Adobe Experience Platform en Journey Optimizer zijn bijgewerkt. [Meer informatie](../start/get-started.md#architecture)

* Er is een video toegevoegd over de afspeellocatie van de verpersoonlijkingseditor om u te helpen bij het schrijven en testen van verpersoonlijkingscode met behulp van voorbeeldgegevens. [Meer informatie](../personalization/personalize.md#video-perso)

* Het maximumaantal adressen in een zaadlijst is verhoogd van 50 tot 300. [Meer informatie](../configuration/seed-lists.md#create-seed-list)

* Een nieuwe stap die detailleert hoe te om code te verpakken wanneer het gebruiken van besluitvormingsbeleid in de op code-gebaseerde ervaringsredacteur is toegevoegd aan de Create pagina van besluitvormingsbeleid. [Meer informatie](../experience-decisioning/create-decision.md#create-decision)

* Een nota is toegevoegd aan de op code-gebaseerde ervaringsdocumentatie om te specificeren dat wanneer u veelvoudige code-gebaseerde ervaringsacties hebt die op de zelfde oppervlakte lopen, de campagne of de prioritaire score van de reis bepaalt wat aan de eindgebruiker wordt geleverd als zij voor meer dan één actie kwalificeren. [Meer informatie](../code-based/code-based-surface.md#surface-definition)

* Een nieuwe pagina over het oplossen van problemen binnenkomende acties in reizen verstrekt een geleidelijke gids om kwesties onafhankelijk te identificeren en op te lossen alvorens uit te gaan om te steunen. [Meer informatie](../building-journeys/troubleshooting-inbound.md)

* Een nieuwe [&#x200B; pagina &#x200B;](../code-based/code-based-decisioning-implementations.md) is toegevoegd om te beschrijven hoe te om de volgende vlaggen aan uw cliëntimplementatie toe te voegen wanneer het gebruiken van besluit in op code-gebaseerde ervaringen:

   * De markering `dryRun` toevoegen om de besluitvorming in op code gebaseerde ervaringen te testen. [Meer informatie](../code-based/code-based-decisioning-implementations.md#code-based-test-decisions)

   * Pas deduplicatie toe op besluitvormingsverzoeken in op code-gebaseerde ervaringen. [Meer informatie](../code-based/code-based-decisioning-implementations.md#code-based-decisioning-deduplication)

## April 2025 {#apr-2025}

* Het hoofdstuk van de Configuratie is nu gesplitst in drie hoofdstukken: [&#x200B; de configuratie van het Kanaal &#x200B;](../configuration/get-started-configuration.md), [&#x200B; configuratie van de Reis &#x200B;](../configuration/about-data-sources-events-actions.md), en [&#x200B; verbindt uw systemen &#x200B;](../configuration/ajo-apis.md).
* Er is een waarschuwende opmerking toegevoegd over het gebruik van ervaringsgebeurtenissen in reisexpressies en -omstandigheden. [Meer informatie](../building-journeys/expression/expressionadvanced.md#discovering-the-interface)
* Er is een opmerking toegevoegd op de pagina voor Direct-mailconfiguratie over tijdelijke opslag van het uitvoerbestand. [Meer informatie](../direct-mail/direct-mail-configuration.md)
* Er is een tip toegevoegd in de sectie met de editor voor geavanceerde expressies voor de reis over de richtlijnen voor de indeling van voorwaarden. [Meer informatie](../building-journeys/expression/expressionadvanced.md)
* In de functiesectie `inAudience` is een waarschuwing toegevoegd over de effecten en aanbevolen procedures bij het wijzigen van de naam van een publiek. [Meer informatie](../building-journeys/functions/functioninaudience.md)
* Een aanbeveling toegevoegd over het gebruik van native trefwoorden bij het gebruik van 2-wegs-SMS. [Meer informatie](../sms/sms-opt-out.md)
* De testpagina voor de reis is bijgewerkt met een opmerking over de noodzaak om een naamruimte voor identiteit op te nemen in de gebruikte gebeurtenis. [Meer informatie](../building-journeys/testing-the-journey.md)
* U kunt subdomeinen momenteel niet dedelegeren via de gebruikersinterface van [!UICONTROL Journey Optimizer] . Dit moet u doorgeven aan uw Adobe-vertegenwoordiger. De stappen om een subdomain niet langer te delegeren zijn nu gedetailleerd voor [&#x200B; E-mail &#x200B;](../configuration/delegate-subdomain.md#undelegate-subdomain), [&#x200B; SMS &#x200B;](../sms/sms-subdomains.md#undelegate-subdomain), [&#x200B; de ervaringen van het Web &#x200B;](../web/web-delegated-subdomains.md#undelegate-subdomain), en [&#x200B; het Bestaan pagina&#39;s &#x200B;](../landing-pages/lp-subdomains.md#undelegate-subdomain).<!--[Read more](../configuration/delegate-subdomain.md#undelegate-subdomain)-->
* Meer informatie over de optionele parameter `maxHttpConnections` in de API voor afdekritten, inclusief instructies voor het gebruik van deze parameter naast configuraties voor het vertragen van hetzelfde eindpunt. [Meer informatie](../configuration/throttling.md)
* In de sectie Beslissing kunnen toegevoegde richtlijnen waarin wordt uitgelegd dat goedgekeurde aanbiedingspunten niet kunnen worden verwijderd als zij in een verzameling of een beslissing worden gebruikt. Opgenomen stappen om de status te wijzigen in Concept met de optie **[!UICONTROL Undo approve]** . [Meer informatie](../experience-decisioning/items.md#manage)
* Informatie over sandboxen is gegroepeerd in een nieuwe sectie voor &quot;Sandboxbeheer&quot;. Deze nieuwe sectie biedt informatie over het gebruik en toewijzen van sandboxen en over het gebruik van de functie voor exporteren en importeren van pakketten om objecten zoals reizen, inhoudssjablonen of fragmenten over meerdere sandboxen te kopiëren. [Meer informatie](../administration/sandboxes.md)

## Maart 2025 {#mar-2025}

* De pagina over de gebeurtenissen van de Kwalificatie van het Publiek is bijgewerkt met nieuwe aanbevelingen. [Meer informatie](../building-journeys/audience-qualification-events.md)
* Aangepaste oplossingen voor acties zijn nu beschikbaar voor alle klanten (GA). [Meer informatie](../action/troubleshoot-custom-action.md)
* Gegevenshygiëne is nu de levenscyclus van gegevens in de gebruikersinterface van het product. De documentatie is bijgewerkt met deze wijziging. [Meer informatie](../privacy/data-hygiene.md)
* De ontbrekende ingebouwde bevoegdheden voor de bestemmingspagina zijn toegevoegd aan de documentatie. [Meer informatie](../administration/ootb-permissions.md)
* Er is een opmerking toegevoegd over het plannen van terugkerende campagnes. [Meer informatie](../campaigns/create-campaign.md)
* De sectie over het invoegen van koppelingen en het inschakelen van tracering in een e-mailbericht is bijgewerkt en opnieuw ingedeeld. [Meer informatie](../email/message-tracking.md)
* Het gedeelte over personalisatiemogelijkheden in Adobe Journey Optimizer is gereorganiseerd en verbeterd. [Meer informatie](../personalization/personalize.md)
* De Beslissingsbeheer-API voor het weergeven van gepersonaliseerde aanbiedingen is bijgewerkt met een voorbeeld om paginering uit te voeren als er in de reactie meerdere gepersonaliseerde aanbiedingen ontbreken. [Meer informatie](../offers/api-reference/offers-api/personalized-offers/offers-list.md)
* Voor meer duidelijkheid is er een nieuwe pagina gemaakt met alle informatie over de functie voor afmelden bij lijst. [Meer informatie](../email/list-unsubscribe.md)
* De sectie Frequency Capping is bijgewerkt met informatie over hoe de teller voor het afluisteren van frequenties wordt bijgewerkt voor de API&#39;s voor het bepalen van beslissingen en het bepalen van batch, in aanvulling op de Edge-API voor besluitvorming. [Meer informatie](../offers/offer-library/add-constraints.md#frequency-capping)

## Februari 2025 {#feb-2025}

* De activiteitenhandleidingen voor het lezen van doelgroepen zijn bijgewerkt om aan te geven dat slechts één activiteit kan worden gebruikt in een reis en dat deze slechts voor één doelgroep kan worden gebruikt. [Meer informatie](../building-journeys/read-audience.md)
* Reisinstructies bij het gebruik van Adobe Campaign-activiteiten zijn bijgewerkt. [Meer informatie](../start/guardrails.md#ac-g)
* De stappen voor het maken van uw eerste ritten zijn in detail beschreven en er zijn koppelingen naar de sectie documentatie toegevoegd. [Meer informatie](../building-journeys/journey-gs.md)
* Er is nu een nieuwe pagina beschikbaar waarin het dashboard voor de reis en de gebruikersinterface worden gefilterd. [Meer informatie](../building-journeys/journey-ui.md)
* De documentatie voor **[!UICONTROL Send-Time optimization]** en de bijbehorende veelgestelde vragen zijn bijgewerkt, verbeterd en naar een nieuwe, speciale pagina verplaatst. [Meer informatie](../building-journeys/send-time-optimization.md)
* Er zijn nieuwe instructies toegevoegd voor reisevenementen. [Meer informatie](../start/guardrails.md#events-g)
* De ingebouwde pagina met kanaalacties is opnieuw ingedeeld. [Meer informatie](../building-journeys/journeys-message.md)
* In de afdelingen Beslissingen en Beslissingsbeheer zijn instructies en beperkingen toegevoegd.
   * [Afbakening en beperkingen](../experience-decisioning/decisioning-guardrails.md)
   * [Beheersbeheerinstructies en beperkingen](../offers/decision-management-guardrails.md)
* Er is een nieuw hoofdstuk over contextgegevens toegevoegd aan de documentatie over het beheer van besluiten. Het verstrekt informatie over hoe te om contextgegevens in de beslissingsmotor te hefboomwerking, bijvoorbeeld om een beslissingsregel te ontwerpen die het huidige weer om 80 graden op het tijdstip vereist het beslissingsverzoek wordt gemaakt. [Meer informatie](../offers/context-data.md)

## Januari 2025 {#jan-2025}

* Er is een nieuwe sectie over de optie **[!UICONTROL Execution address]** in de e-mailconfiguratie toegevoegd. Het primaire adres wordt gedefinieerd op sandboxniveau, maar de standaardinstelling kan worden oververborgen voor een specifieke e-mailconfiguratie. [Meer informatie](../email/email-settings.md#execution-address)

* **wordt begonnen met leverability** pagina is bijgewerkt met de mogelijkheid om IP warmteopwerkschema&#39;s van het gebruikersinterface direct tot stand te brengen. [Meer informatie](../reports/deliverability.md#reputation)

* De **sectie van de Parameters van de Kopbal** is bijgewerkt om op de nieuwe etiketten en de veranderingen in het gebruikersinterface te wijzen. [Meer informatie](../email/email-settings.md#email-header)

* De **voorwaartse e-mail** sectie is bijgewerkt om te specificeren dat alle e-mails die naar **van e-mail** adres worden verzonden door:sturen aan het voorwaartse e-mailadres. Als er geen e-mailbericht naar voren is opgegeven, worden deze e-mails verwijderd. [Meer informatie](../email/email-settings.md#email-settings)

* De maximumgrootte van contextafhankelijke kenmerken die worden doorgegeven aan een door de API geactiveerd campagneverzoek is bijgewerkt naar 200 kb. [Meer informatie](../campaigns/api-triggered-campaigns.md#contextual)

* Een nieuwe sectie is toegevoegd aan **Manage fragments** pagina om te beschrijven hoe te om nieuwe attributen aan een levend fragment toe te voegen. De hele pagina is ook verbeterd. [Meer informatie](../content-management/manage-fragments.md#adding-new-attributes)

* Er is een sectie ‘Hulplijnen en beperkingen’ toegevoegd aan de documentatie met betrekking tot conflictenbeheer en -prioriteiten. [Meer informatie](../conflict-prioritization/gs-conflict-prioritization.md)

* Er is een nieuw gebruiksgeval van begin tot eind toegevoegd om alle stappen voor te stellen die nodig zijn om het Beslissen in inhoudexperimenten met het [!DNL Journey Optimizer] op code-gebaseerde ervaringskanaal te gebruiken. [Meer informatie](../experience-decisioning/experience-decisioning-uc.md)

* **vormt e-mailmontages** pagina is verdeeld in verscheidene subpagina&#39;s voor betere leesbaarheid, met inbegrip van nieuwe standalone pagina&#39;s gewijd aan [&#x200B; Lijst unsubscribe &#x200B;](../email/list-unsubscribe.md), [&#x200B; parameters van de Kopbal &#x200B;](../email/header-parameters.md) en [&#x200B; URL het volgen &#x200B;](../email/url-tracking.md).

## December 2024 {#nov-2024}

* Er is een notitie toegevoegd om een mogelijk foutbericht op te lossen wanneer u een API-aanroep maakt om gegevenssets voor personalisatie met Adobe Experience Platform-gegevens in te schakelen. [Meer informatie](../personalization/aep-data-perso.md)

## Oktober 2024 {#oct-2024}

* Alle nieuwe functies en verbeteringen die worden geïntroduceerd in de release van [!DNL Journey Optimizer] oktober 24 zijn beschreven in de documentatie. [Meer informatie](release-notes.md)
* Alle communicatiekanalen die beschikbaar zijn in [!DNL Journey Optimizer] worden nu gegroepeerd in een specifieke sectie van de documentatie. [Meer informatie](../channels/gs-channels.md)
* **vorm uw code-gebaseerde ervaring** pagina is verbeterd om het proces helderder te maken, met inbegrip van de sectie die verklaart wat een oppervlakte URI is. [Meer informatie](../code-based/code-based-configuration.md)
* **creeer de configuratie van het Webkanaal** pagina is bijgewerkt om de stappen te verduidelijken wanneer het creëren van een pagina passende regel, die ook op code-gebaseerde ervaringsconfiguratie van toepassing is. [Meer informatie](../web/web-configuration.md#web-page-matching-rule)
* Er is een notitie toegevoegd over de aanstaande time-to-live (TTL) guardrail voor door het systeem gegenereerde gegevenssets. [Meer informatie](../data/get-started-datasets.md)
* Een nieuwe sectie is toegevoegd om te beschrijven hoe te om uw code-gebaseerde gepersonaliseerde ervaringen op uw browser of op uw mobiele apparaten voor te vertonen, gebruikend de **Voorproef op apparaat** optie wanneer het simuleren van inhoud in een reis of een campagne. [Meer informatie](../code-based/test-code-based.md#preview-on-device)
* Er is een nieuwe pagina toegevoegd over het gebruik van Aangepast uploadpubliek voor besluitvorming. [Meer informatie](../offers/custom-upload-decisioning.md)
* Er is een nieuwe pagina toegevoegd om de beslissingsmogelijkheden van Journey Optimizer te introduceren. [Meer informatie](../experience-decisioning/gs-decision.md)
* Er zijn instructies en beperkingen toegevoegd aan de beslissingsdocumentatie. [Meer informatie](../experience-decisioning/gs-experience-decisioning.md#guardrails)

## September 2024 {#sept-2024}

* Alle nieuwe functies en verbeteringen die worden geïntroduceerd in de release [!DNL Journey Optimizer] Sept &#39;24 zijn beschreven in de documentatie. [Meer informatie](release-notes.md)
* Er is een gedeelte toegevoegd over het beheer van de reistijd. [Meer informatie](../building-journeys/read-audience.md#read-audience-retry)
* Veelgestelde vragen over het Afbakenen/vertragen van regel voor douaneacties zijn bijgewerkt om de standaard het afschilderen regel te vermelden. [Meer informatie](../configuration/external-systems.md#faq)
* Het gedeelte Toegang tot besturingselement is bijgewerkt met machtigingen voor de AI Assistant Content Generator. [Meer informatie](../administration/high-low-permissions.md#ai-orchestrated-campaign)
* Er is een video toegevoegd over de AI Assistant Content Generator voor het genereren van e-mail. [Meer informatie](../content-management/generative-full-content.md#video)

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
* Support of `<listObject>` has been modified in multiple functions.
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
