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
source-git-commit: 63a849b50ff7f02da07e6fd74d00f3d9360ad012
workflow-type: tm+mt
source-wordcount: '4602'
ht-degree: 13%

---

# Documentatie-updates {#latest-updates}

Deze pagina bevat alle laatste updates in [!DNL Journey Optimizer] documentatie.

## Februari 2024 (#feb-2024)

* Er is informatie toegevoegd over hoe u de representaties van aanbiedingen kunt aanpassen op basis van contextgegevens. [Meer informatie](../offers/offer-library/add-representations.md#context-data)

## Januari 2024 {#jan-2024}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 24 januari is gedetailleerd weergegeven in de documentatie. [Meer informatie](release-notes.md)
* Er is een begeleiding toegevoegd over de grootte van de reis. [Meer informatie](../start/guardrails.md#journeys-guardrails-journeys)
* Tijdlijnbeheer is gedetailleerd [in het volgende gedeelte](../building-journeys/journey-gs.md#global_timeout).
* Journey Optimizer [documentatiehuis](../../ajo-home.md) pagina is opnieuw ontworpen.
* Recommendations over de activiteit Profielen bijwerken is toegevoegd. [Meer informatie](../building-journeys/update-profiles.md)
* Er is informatie toegevoegd over het gedrag van onderbrekingen in de activiteiten van gebeurtenissen tijdens reizen. Wanneer geen gebeurtenis tijdens de gespecificeerde onderbrekingsperiode wordt ontvangen, zullen de individuen de reis voortzetten als geen onderbrekingspad wordt bepaald. [Meer informatie](../building-journeys/general-events.md#events-specific-time)
* De vereisten van de in-app kanaalconfiguratie zijn bijgewerkt met een nota over het gebruik van een de voorkeur van de Dataset van de douane samenvoegbeleid. [Meer informatie](../in-app/inapp-configuration.md)
* Er zijn meer details toegevoegd over het manipuleren van verzamelingen in een aangepaste handelingsreactie. [Meer informatie](../action/action-response.md#exp-syntax).
* Een koppeling naar de [Schema-woordenboek voor Adobe Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html) is toegevoegd aan de startpagina.
* Een verouderde verwijzing naar het middel van het Bericht AJO is verwijderd uit de lijst van middelen beschikbaar in het Logboek van de Controle. Wanneer een update op een bericht in een reis wordt gedaan, **Reis** log wordt gemaakt. [Meer informatie](../privacy/audit-logs.md)
* Er zijn aanvullende aanbevelingen toegevoegd over het gebruik van de **Publiek lezen** activiteit. [Meer informatie](../building-journeys/read-audience.md#must-read)
* De pagina Aan de slag met Adobe Experience Platform-soorten publiek is verbeterd met een lijst met methoden voor het genereren van doelgroepen. [Meer informatie](../audience/about-audiences.md)
* De beste praktijken zijn toegevoegd wanneer het kiezen van een eindpunt aan doel gebruikend een douaneactie. [Meer informatie](../action/about-custom-action-configuration.md)
* Er is een opmerking toegevoegd om gebruikers te laten weten dat gebeurtenissen niet kunnen worden gestart vanaf externe systemen met een API. [Meer informatie](../building-journeys/testing-the-journey.md#important-notes)
* Informatie over de **currentActionField** functie is toegevoegd aan de lijst met [beheerfuncties voor verzamelingen](../building-journeys/expression/collection-management-functions.md). Er is een expressiemonster toegevoegd waarin de functie wordt gebruikt [API-aanroepreacties gebruiken in aangepaste handelingen](../action/action-response.md) pagina.
* Werk het aangepaste verificatiedocument bij met betrekking tot de duur van de cache. [Meer informatie] ../datasource/external-data-sources.md)
* Steun voor `<listObject>` is gewijzigd in meerdere functies.
* Werk de **duur** in de `toString` functie. [Meer informatie](../building-journeys/functions/functiontostring.md)
* Voor sommige externe gegevensbronnen wordt het gebruik van aangepaste handelingen aanbevolen.
* Syntaxis van gebeurtenisveld is bijgewerkt. De volgende syntaxis is vervangen `@(my_event.myfield}` en vervangen door `@event{my_event.myfield}`. [Meer informatie](../building-journeys/expression/field-references.md)
* Het Global-rapport en de Live-rapporthulplijnen zijn gereorganiseerd. [Meer informatie](../reports/campaign-global-report.md)


## November 2023 {#nov-2023}

* De guardrail die alle douaneacties beperkt is veranderd van 150.000 vraag over 30 seconden aan 300.000 vraag over één minuut. Bovendien is het gebrek het maximum niet meer op elk eindpunt van toepassing. Het wordt nu uitgevoerd per host en per sandbox. Op een sandbox bijvoorbeeld als u twee eindpunten met dezelfde host hebt (bijvoorbeeld: `https://www.adobe.com/endpoint1` en `https://www.adobe.com/endpoint2`), wordt de aftopping toegepast op alle eindpunten onder de host adobe.com. De &quot;eindpunt1&quot;en &quot;eindpunt2&quot;zullen de zelfde het begrenzen configuratie delen en het hebben van één eindpunt bereikt de grens zal een effect op het andere eindpunt hebben. [Meer informatie](../action/about-custom-action-configuration.md)
* Er is een nieuwe status voor e-mailcampagnes toegevoegd aan de lijst met statussen van campagnes. [Meer informatie](../campaigns/modify-stop-campaign.md#campaign-statuses-and-alerts-statuses)
* De sectie Aan de slag met het publiek van Adobe Experience Platform is bijgewerkt met informatie over de beschikbare methoden voor publieksevaluatie en de manier waarop u deze kunt selecteren. [Meer informatie](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* Er is een nieuwe subsectie toegevoegd om op te geven welke gebeurtenissen moeten worden vermeden wanneer u een publiek maakt als u de evaluatiemethode voor streamingsegmentatie gebruikt. [Meer informatie](../audience/about-audiences.md#streaming-segmentation-events-guardrails)

## Oktober 2023 {#oct-2023}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 23 oktober is gedetailleerd weergegeven in de documentatie. [Meer informatie](release-notes.md)
* Toegevoegde GIFFEN ter illustratie van enkele belangrijke mogelijkheden, zoals: [Inhoudssjablonen](../content-management/content-templates.md), [Fragmenten](../content-management/fragments.md), [Berekende kenmerken](../audience/computed-attributes.md), [Directe post](../direct-mail/get-started-direct-mail.md), [Tags](../start/search-filter-categorize.md#tags), [Optimalisatiemodellen voor het beheer van beslissingen](../offers/ranking/personalized-optimization-model.md), [API-gestuurde campagnes](../campaigns/api-triggered-campaigns.md), en [Inhoudsexperiment](../campaigns/content-experiment.md).
* Het proces voor het maken van schema&#39;s is bijgewerkt met de meest recente updates in de gebruikersinterface die worden geleverd bij Adobe Experience Platform-wijzigingen. [Meer informatie](../audience/creating-test-profiles.md)
* De pagina met instructies voor beslissingsbeheer is toegevoegd aan de pagina met instructies en beperkingen. [Meer informatie](../start/guardrails.md#decision-management)
* De sectie van de Parameters van de Kopbal is bijgewerkt om erop te wijzen hoe de uit-van-bureauberichten en uitdagingsreacties worden behandeld (zij worden ontvangen op **[!UICONTROL Error email]**). [Meer informatie](../email/email-settings.md#email-header)
* Er is een nieuwe sectie gemaakt voor het voorvertonen en testen van uw inhoud. [Meer informatie](../content-management/preview-test.md)
* De implementeer single-page toepassingenpagina is verplaatst naar de documentatie van het Web SDK van het Palet van de Ervaring van de Adobe. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html){target="_blank"}
* De sectie van het Afschilderen is bijgewerkt om op de etiketveranderingen met betrekking tot aanbieding het maximum in de interface van het besluitvormingsbeheer te wijzen. [Meer informatie](../offers/offer-library/add-constraints.md#capping)
* De functie Dynamische inhoud toevoegen aan e-mailberichten is bijgewerkt met informatie over het verwijderen van een variant. [Meer informatie](../personalization/dynamic-content.md#emails)
* Het voorbeeld voor configuraties met begrenzing en vertraging is bijgewerkt. [Meer informatie](../configuration/external-systems.md)
* De beperking met betrekking tot scalaire arrays is verwijderd uit de externe gegevensbronsectie. [Meer informatie](../datasource/external-data-sources.md)
* De meerkanaals reisgebruikscase is bijgewerkt. [Meer informatie](../building-journeys/journeys-uc.md)
* De Journey Optimizer documentatieset is bijgewerkt om het nieuwe proces van het creëren van het schema van het Experience Platform te weerspiegelen.

## September 2023 {#september-2023}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van september &#39;23 is gedetailleerd weergegeven in de documentatie. [Meer informatie](release-notes.md)
* Er is een nieuwe pagina toegevoegd met de aanbevolen tips voor het schalen en stitching in real time. [Meer informatie](../start/best-practices.md)

  <!--  * The maximum wait duration has been changed from 30 to 29 days. [Read more](../building-journeys/wait-management.md) -->

* Een veelgestelde-Vragen sectie is toegevoegd voor Optimalisering Send-Time. [Meer informatie](../building-journeys/journeys-message.md#faq-send-time)
* Er is een opmerking toegevoegd voor de kwalificatieactiviteit van het publiek. Het kan 10 minuten duren om actief te zijn en te luisteren naar profielen die het publiek binnenkomen of verlaten. [Meer informatie](../building-journeys/audience-qualification-events.md#important-notes-segment-qualification)
* Er is een lijst toegevoegd aan de documentatie van het besluitvormingsbeheer met beperkingen die u bekend moeten maken bij het opstellen van beslissingsregels. [Meer informatie](../offers/offer-library/creating-decision-rules.md)
* De koppelingen naar de documentatie van toegangsbeheer zijn bijgewerkt. [Meer informatie](../administration/permissions.md)
* In-app kanaalvereisten zijn bijgewerkt met Adobe Experience Platform-gegevens over gegevensverzameling. [Meer informatie](../in-app/inapp-configuration.md)
* Sommige expressies die worden weergegeven in voorbeelden van ranking-formules zijn bijgewerkt om validatiefouten te voorkomen. [Meer informatie](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* Er is een waarschuwing toegevoegd aan de sectie Bepaal beslissingsbereik om te specificeren dat als AI-model wordt gebruikt in een groep evaluatiecriteria, alle evaluatiecriteria in die groep de AI-rangordemethode moeten gebruiken, met hetzelfde specifieke AI-model. Bovendien kan slechts één groep met evaluatiecriteria het AI-model gebruiken. [Meer informatie](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## Augustus 2023 {#august-2023}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van augustus &#39;23 is gedetailleerd weergegeven in de documentatie. [Meer informatie](release-notes.md)
* De opmerking over **beheer van verificatiecache** op reis is bijgewerkt om duidelijk te maken dat het token niet wordt gedeeld tussen verschillende reizen . [Meer informatie](../datasource/external-data-sources.md#custom-authentication-mode)
* De pagina over de reis **toegangsbeheer** is bijgewerkt om het gedrag te verduidelijken. [Meer informatie](../building-journeys/entry-management.md)
* Offer decisioning **exportgegevenssets** zijn nu standaard ingeschakeld. De opmerking over het vorige gedrag is verwijderd.  [Meer informatie](../offers/export-catalog/get-started-export.md)
* Diversen **campagnerapportcijfers** zijn hernoemd, zowel in Live als in Global-rapporten. [Meer informatie](../reports/campaign-global-report.md)
* Er is een nieuwe sectie toegevoegd over de voorwaarden voor het testen van inhoud voor het webkanaal. [Meer informatie](../web/web-prerequisites.md#experiment-prerequisites)
* Er is een waarschuwing toegevoegd op de **Werken met inhoudssjablonen** pagina om aan te geven dat huidige tracering niet wordt ondersteund bij het testen van sjablonen voor e-mailinhoud. Voor het testen van het bijhouden moet u de inhoudssjabloon in een e-mail gebruiken en een proefdruk verzenden. [Meer informatie](../content-management/content-templates.md#test-template)
* Er zijn verschillende waarschuwingen toegevoegd aan de **bestemmingspagina&#39;s maken en publiceren** om aan te geven dat u de landingspagina niet kunt openen door de bij het maken van de pagina gedefinieerde URL gewoon te kopiëren en in een webbrowser te plakken, zelfs als deze is gepubliceerd. In plaats daarvan kunt u het testen met behulp van de voorvertoningsfunctie. [Meer informatie](../landing-pages/create-lp.md)
* Er is een nieuwe sectie toegevoegd over hoe u **toestemming beheren** voor het directe-mailkanaal. [Meer informatie](../direct-mail/test-send-direct-mail.md)

## Juli 2023 {#july-2023}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 23 juli is in detail beschreven in de documentatie. [Meer informatie](release-notes.md)
* De pagina met documentatie over wachtactiviteiten is verbeterd met aanvullende informatie en aanbevolen procedures met betrekking tot de algemene time-out en het herbetreden van bestanden. [Meer informatie](../building-journeys/wait-activity.md)
* De pagina over toegangsbeheer is verbeterd. [Meer informatie](../building-journeys/entry-management.md)
* Er is aanvullende informatie toegevoegd over de vertragingsfactor in de documentatie over de activiteit van het publiek lezen. [Meer informatie](../building-journeys/read-audience.md)
* Er is aanvullende informatie toegevoegd over nieuwe pogingen. [Meer informatie](../start/guardrails.md#general-actions-g)
* De **Persoonlijkheidsgoedkeuring implementeren** de sectie is bijgewerkt om te beschrijven hoe te om verpersoonlijkingstoestemming in campagnes manueel af te dwingen: u kunt de bouwer van de segmentregel gebruiken om een publiek tot stand te brengen die opt-out profielen of een gespleten activiteit aan een samenstellingswerkschema bevatten. [Meer informatie](../privacy/opt-out.md#opt-out-expression-editor)

## Juni 2023 {#june-2023}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 23 juni is in detail beschreven in de documentatie. [Meer informatie](release-notes.md)
* Er is informatie toegevoegd over de verhouding voor de diskette-snelheid in het scherm Journalen-overzicht. [Meer informatie](../building-journeys/journey-gs.md#journey-access)
* Er is een notitie toegevoegd met de volgende stappen als u het schema wijzigt met nieuwe opsomwaarden nadat u een gebeurtenis hebt gemaakt [Meer informatie](../event/about-creating.md)
* Er is een aanbeveling toegevoegd voor het gebruik van tripVersionID in plaats van tripVersionName bij het opvragen van reizen. [Meer informatie](../reports/sharing-common-fields.md#journeyversionid-field)
* Er zijn aanvullende voorbeelden toegevoegd aan de **Besluiten maken** aan te geven in welke gevallen meerdere criteria en verschillende besluitvormingsgebieden worden gebruikt. [Meer informatie](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* De documentatie van het Beslissingsbeheer is verduidelijkt met een nota die specificeert dat het gebruik van de Controle van de Toegang van het Niveau van Objecten niet beschikbaar voor dynamische inzamelingen is. [Meer informatie](../offers/offer-library/creating-collections.md)

## Mei 2023 {#may-2023}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van mei &#39;23 is gedetailleerd weergegeven in de documentatie. [Meer informatie](release-notes.md)
* Er is een nieuwe pagina toegevoegd waarin wordt beschreven hoe u het subdomein instelt dat wordt gebruikt om inhoud die afkomstig is van de Adobe Experience Manager Assets Essentials, te publiceren in uw webervaringen. [Meer informatie](../web/web-delegated-subdomains.md)
* Er is een nieuwe subsectie toegevoegd waarin wordt uitgelegd hoe u aangepaste volgparameters kunt toevoegen aan URL&#39;s in de e-mailontwerper. [Meer informatie](../email/message-tracking.md#url-tracking)
* Er is een nieuwe sectie toegevoegd waarin wordt beschreven hoe u ervoor kunt zorgen dat de keuze van uw klanten die ervoor kiezen hun profielgegevens niet te laten gebruiken voor personalisatie, wordt gerespecteerd. [Meer informatie](../privacy/opt-out.md#opt-out-personalization)
* Er is een opmerking toegevoegd over het gebruik van speciale internationale tekens in URL&#39;s die in e-mailinhoud zijn opgenomen. [Meer informatie](../email/message-tracking.md#insert-links)
* De benodigde machtigingen voor het testen en publiceren van bestemmingspagina&#39;s zijn toegevoegd. [Meer informatie](../landing-pages/create-lp.md)
* Er is een opmerking toegevoegd over de Adobe Experience Platform-eindpunten die nodig zijn om uw aangepaste gebeurtenissen mee te laten tellen in de limiet voor de frequentie van het beheer van beslissingen. [Meer informatie](../offers/data-collection/schema-requirement.md#track-custom-events)

## April 2023 {#apr-2023}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 23 april is in detail beschreven in de documentatie. [Meer informatie](release-notes.md)
* Er is een opmerking toegevoegd om op te geven dat ingebouwde handelingen niet kunnen worden verwijderd. [Meer informatie](../start/guardrails.md#custom-actions-g)
* De informatie is toegevoegd op serviceEvents evenals een vraagvoorbeeld om de details van een serviceEvent te controleren. [Meer informatie](../reports/query-examples.md#common-queries)
* Er is een opmerking toegevoegd om aan te geven dat u geen query&#39;s kunt uitvoeren op tijdreeksen. [Meer informatie](../building-journeys/condition-activity.md)
* Adobe Experience Manager Assets Essentials en Adobe Stock zijn toegevoegd aan de integratiepagina voor meerdere oplossingen. [Meer informatie](../start/ajo-integrations.md)
* De waarschuwing dat e-mailsubdomeinen op meerdere niveaus niet zijn toegestaan, is verwijderd omdat deze nu worden ondersteund. [Meer informatie](../configuration/delegate-subdomain.md)
* Er is een notitie toegevoegd om aan te geven dat als er wijzigingen worden aangebracht in een besluit over een aanbod dat wordt gebruikt in een reisbericht, u de reis ongedaan moet maken en opnieuw moet publiceren. [Meer informatie](../building-journeys/publishing-the-journey.md)
* In het besluitvormingsbeheer is verduidelijkt hoe u ervoor moet zorgen dat gebeurtenissen correct in de afluisterteller worden verwerkt **gebeurtenis Capping** sectie. [Meer informatie](../offers/offer-library/add-constraints.md#capping-event)
* Er is een nieuwe sectie toegevoegd aan de **Uitvoeringadressen wijzigen** pagina. Het specificeert dat het mogelijk is om het uitvoeringsgebied met voeten te treden globaal in de reis geavanceerde parameters wordt geplaatst, maar de e-mailadresopheffing zou slechts voor specifieke gebruiksgevallen moeten worden gebruikt. Meestal wordt de waarde gedefinieerd als het primaire adres in de **Uitvoervelden** Dat is de methode die moet worden gebruikt. [Meer informatie](../configuration/primary-email-addresses.md#journey-parameters)
* De **URL-tracking** biedt nu de lijst en beschrijving van alle contextafhankelijke kenmerken die kunnen worden ingesteld voor URL-tracking in een oppervlak van een e-mailkanaal. [Meer informatie](../email/email-settings.md#url-tracking)

## Maart 2023 {#march-2023}

* Het Journey Optimizer-schemawoordenboek is nu beschikbaar. U zult de volledige lijst van gebieden en attributen voor elk schema vinden.  [Meer informatie](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html)
* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 23 maart is in detail beschreven in de documentatie. [Meer informatie](release-notes.md)
* Voeg een stap toe om Adobe Analytics-gebeurtenissen tijdens uw reizen mogelijk te maken. [Meer informatie](../event/about-analytics.md)
* In de gids voor het beheer van besluiten is een nieuw gedeelte opgenomen over de wijze waarop feedback van offer decisioning in Adobe Experience Platform kan worden verzameld, met inbegrip van de aanbiedingen die worden weergegeven en de wijze waarop gebruikers met hen communiceren. [Meer informatie](../offers/data-collection/data-collection.md)
* Er is een nieuwe subsectie toegevoegd aan de **Beslissing maken** een toelichting bij het verschil tussen de beoordeling van de criteria in een opeenvolgende volgorde of tegelijkertijd. [Meer informatie](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* Er is een hulplijn toegevoegd voor het lezen van lezersritten met incrementeel lezen. U kunt geen nieuwe versie maken, u moet de reis dupliceren. [Meer informatie](../start/guardrails.md#journey-versions-g)
* Het gebruiksgeval op hoe te om productie te beperken is bijgewerkt met informatie over het vertragen mogelijkheden. [Meer informatie](../building-journeys/limit-throughput.md)
* Er is een opmerking toegevoegd om op te geven dat scalaire arrays niet worden ondersteund in de definitie van de responslading. [Meer informatie](../datasource/external-data-sources.md)
* De sectie over de condities van het profieluiteinde is bijgewerkt. [Meer informatie](../building-journeys/condition-activity.md#profile_cap)

## Februari 2023 {#feb-2023}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] Release Feb &#39;23 is gedetailleerd in de documentatie. [Meer informatie](release-notes.md)
* Er is informatie toegevoegd over de canvaswerkbalk. [Meer informatie](../building-journeys/using-the-journey-designer.md#gs-journey-design)
* Er is informatie toegevoegd om aan te geven dat interne adressen van Adoben niet zijn toegestaan in URL&#39;s en API&#39;s. [Meer informatie](../start/guardrails.md)
* Er is een opmerking toegevoegd aan de API-getriggerde campagnedocumentatie om op te geven dat contextafhankelijke kenmerken die aan de aanvraag worden doorgegeven, niet groter mogen zijn dan 50 kB. [Meer informatie](../campaigns/api-triggered-campaigns.md#contextual)
* Er is informatie toegevoegd over de wijze waarop gegevens over opt-out worden opgeslagen in het dialoogvenster **Dataset voor goedgekeurde service** nadat de ontvangers zijn afgemeld via een bestemmingspagina. [Meer informatie](../landing-pages/lp-use-cases.md#configure-opt-out)

## Januari 2023 {#jan-2023}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 23 januari is gedetailleerd weergegeven in de documentatie. [Meer informatie](release-notes.md)
* De informatie is toegevoegd op de eindpunten van de douaneauthentificatie in de het maximum documentatie. [Meer informatie](../configuration/external-systems.md)
* Een nieuw voorbeeld van de douaneauthentificatie is toegevoegd in de externe datasources sectie. [Meer informatie](../datasource/external-data-sources.md#custom-authentication-mode)
* Er is een opmerking toegevoegd over Data Collection Core Service (DCCS) voor door gebeurtenissen geïnitieerde reizen. [Meer informatie](../start/guardrails.md#events-g)
* Er is een opmerking toegevoegd over het ophalen van naamruimten in het dialoogvenster [Lees publiek](../building-journeys/read-audience.md), [kwalificatie publiek](../building-journeys/audience-qualification-events.md) en [Gebeurtenis maken](../event/about-creating.md) secties.
* Toegankelijkheidsfuncties in [!DNL Journey Optimizer] worden nu gegroepeerd in een specifieke pagina. [Meer informatie](../start/accessibility.md)
* De voorbeelden zijn bijgewerkt in de sectie Operatoren van de documentatie van de geavanceerde expressie-editor. [Meer informatie](../building-journeys/expression/operators.md)
* Er is een opmerking toegevoegd over de beperking bij het opzoeken met een array van objecten. [Meer informatie](../event/experience-event-schema.md#relationships_limitations)
* Een nieuwe pagina over gegevensbeheer toegevoegd in [!DNL Journey Optimizer]. [Meer informatie](../data/gs-data.md)
* Er is een tabel toegevoegd met alle codes die in de reactie kunnen worden geretourneerd wanneer aanbiedingen worden geleverd met de API voor besluitvorming. [Meer informatie](../offers/api-reference/offer-delivery-api/decisioning-api.md)

+++ 2022

## December 2022 {#december-2022}

* De gids van Berichten is gereorganiseerd en verdeeld in specifieke gidsen voor elk kanaal:

   * [Email channel](../email/get-started-email.md)
   * [Push-meldingskanaal](../push/get-started-push.md)
   * [SMS-kanaal](../sms/get-started-sms.md)

* De configuratiegids is gereorganiseerd voor betere leesbaarheid. [Meer informatie](../configuration/get-started-configuration.md)

## November 2022 {#november-2022}

* Er is een nieuwe pagina toegevoegd over Journey Optimizer-integratie. [Meer informatie](../start/ajo-integrations.md)
* Er is een aanbeveling toegevoegd over de lengte van URL&#39;s van spiegelpagina&#39;s. [Meer informatie](../email/message-tracking.md)
* Er is een nieuwe subsectie in de configuratie van de e-mailinstellingen toegevoegd aan het antwoord op het e-mailadres, inclusief aanbevelingen voor een correct antwoordbeheer. [Meer informatie](../email/email-settings.md#reply-to-email)
* Er is een sectie toegevoegd over het wijzigen van de inhoud van een bericht tijdens een live reis. [Meer informatie](../building-journeys/journeys-message.md#update-live-content)

## Oktober 2022 {#october-2022}

* Toegevoegd een geval van het reisgebruik op hoe te om productie te beperken gebruikend Externe Gegevensbronnen en de Acties van de Douane. [Meer informatie](../building-journeys/limit-throughput.md)
* De gevallenge van het reisgebruik is gereorganiseerd in twee categorieën: [Kwesties voor zakelijk gebruik](../building-journeys/journeys-uc.md) en [Kwesties van technisch gebruik](../building-journeys/collections.md).
* De **Entiteitsgegevens** is bijgewerkt met meer details. [Meer informatie](../data/datasets-query-examples.md#entity-dataset)
* De onderdelen &quot;opt-out&quot;-beheer en toestemmingsbeleid zijn gereorganiseerd. [Meer informatie](../privacy/opt-out.md)
* De sectie over geavanceerde parameters in reisberichten is verduidelijkt en specificeert nu dat de e-mailadresopheffing slechts voor specifieke gebruiksgevallen zou moeten worden gebruikt. Meestal wordt de waarde gedefinieerd als het primaire adres in de **Uitvoervelden** Dat is de methode die moet worden gebruikt.
* Een notitie toegevoegd aan de **Subdomeinen van bestemmingspagina configureren** -sectie om aan te geven dat hoofdletters niet zijn toegestaan in subdomeinen van de landingspagina. [Meer informatie](../landing-pages/lp-subdomains.md)

## September 2022 {#september-2022}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van september &#39;22 is gedetailleerd weergegeven in de documentatie. [Meer informatie](release-notes.md)
* Er is een aanbevolen werkwijze toegevoegd met betrekking tot het gebruik van wachtactiviteiten bij terugkerende publiekstrajecten. [Meer informatie](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Voorbeelden van query&#39;s voor nieuwe stapgebeurtenissen en informatie over het verschil tussen id, instanceid en profileid zijn toegevoegd. [Meer informatie](../reports/query-examples.md).
* De pagina&#39;s die betrekking hebben op de [toDateOnly](../building-journeys/functions/functiontodateonly.md) en [toString](../building-journeys/functions/functiontostring.md) functies.
* Meer informatie over de parameters voor de tijdvoorwaarde. [Meer informatie](../building-journeys/condition-activity.md#time_condition)
* Toegevoegde informatie over ingebouwde datasets. [Meer informatie](../data/get-started-datasets.md#access-datasets)
* De secties Global Report en Live zijn verbeterd en gereorganiseerd. [Meer informatie](../reports/global-report.md)
* Er is een lijst toegevoegd met alle in Adobe Journey Optimizer beschikbare rapporteringsmetrische gegevens.
  [Meer informatie](../reports/global-report.md#email-and-sms-metrics)
* Het e-mailgedeelte BCC is verplaatst naar de nieuwe pagina Ondersteuning voor archivering. [Meer informatie](../configuration/archiving-support.md)

## Augustus 2022 {#august-2022}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 22 augustus is gedetailleerd weergegeven in de documentatie. [Meer informatie](release-notes.md)
* De sectie van de Regels van de Frequentie is bijgewerkt om op de nieuwe in-lijn overseinenstroom te wijzen. [Meer informatie](../configuration/frequency-rules.md#apply-frequency-rule)
* Er wordt nu verwezen naar een video waarin wordt getoond hoe u abonnementen kunt configureren en bestemmingspagina&#39;s kunt maken in de sectie Aan de slag met bestemmingspagina&#39;s. [Meer informatie](../landing-pages/get-started-lp.md#video)
* Er is een beperking toegevoegd voor ritten die gebruikmaken van de activiteiten van het leespubliek. [Meer informatie](../building-journeys/read-audience.md)
* De pagina met operators van expressies is verbeterd. [Meer informatie](../building-journeys/expression/operators.md)
* Er is een sectie toegevoegd over het plannen van een campagne. [Meer informatie](../campaigns/create-campaign.md)
* De sectie van de algemene syntaxisregels voor uitdrukkingsredacteur is bijgewerkt om rekening te houden met de nieuwe regel betreffende backslash symbool ontsnapend in letterlijke functies. Deze wijziging heeft geen invloed op de bestaande gepubliceerde berichten. Alleen de nieuwe berichten of conceptberichten moeten worden bijgewerkt. [Meer informatie](../personalization/personalization-syntax.md#general-rules)

## Juli 2022 {#july-2022}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 22 juli is in detail beschreven in de documentatie. [Meer informatie](release-notes.md)
* De **Kanaaloppervlakken instellen** Deze sectie is verduidelijkt en bijgewerkt met koppelingen naar de pagina die beschrijft hoe u het SMS-kanaal kunt configureren. [Meer informatie](../configuration/channel-surfaces.md#create-channel-surface)
* In de reiseigenschappen **Tijdzone profiel** Deze optie is nu standaard uitgeschakeld. [Meer informatie](../building-journeys/timezone-management.md#timezone-from-profiles)
* In de **Wachten** de **Vaste datum** is niet meer beschikbaar. [Meer informatie](../building-journeys/wait-activity.md)
* Meer informatie over de **Incrementeel lezen** in de **Lees publiek** activiteit. [Meer informatie](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Toegevoegde aanbevelingen voor de **Profiel uiteinde** voorwaardetype. [Meer informatie](../building-journeys/condition-activity.md#profile_cap)
* Een beperking toegevoegd op bedrijfsgebeurtenissen. [Meer informatie](../start/guardrails.md#events-g)

## Juni 2022 {#june-2022}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 22 juni is gedetailleerd weergegeven in de documentatie. [Meer informatie](release-notes.md)
* Er is een nieuwe sectie over privacyverzoeken toegevoegd aan de documentatie. [Meer informatie](../privacy/requests.md)
* Een nieuwe sectie over de logboeken van de Controle op middelen is toegevoegd aan de documentatie. [Meer informatie](../privacy/audit-logs.md)
* Er is een nieuw gedeelte toegevoegd aan de documentatie over het toevoegen van HTML- of JSON-inhoud uit de Adobe Experience Cloud Asset Library aan een aanbiedingsweergave. [Meer informatie](../offers/offer-library/add-representations.md#html-json)
* Er is een nieuwe pagina toegevoegd over de levensstijl van de reis. [Meer informatie](../building-journeys/journey.md#journey-versions)
* De pagina Wachttijd activiteit is bijgewerkt. [Meer informatie](../building-journeys/wait-activity.md)
* De lijst met Adobe Journey Optimizer-gegevenssets met queryvoorbeelden toegevoegd. [Meer informatie](../data/datasets-query-examples.md)
* De pagina van de Lijst van gewenste personen is verplaatst naar de sectie van de Configuratie. [Meer informatie](../configuration/allow-list.md)
* De pagina van de Lijst van de Onderdrukking is bijgewerkt om sommige informatie te verduidelijken, met inbegrip van het feit dat alle karakters van ASCII tussen 32 en 126 in de reden voor onderdrukking worden toegestaan. [Meer informatie](../configuration/manage-suppression-list.md)
* Er is een verband toegevoegd met garanties en statische limieten voor het beheer van besluiten. [Meer informatie](../start/guardrails.md)
* Send-Time Optimization is nu beschikbaar voor alle klanten. De bètavermelding is verwijderd. [Meer informatie](../building-journeys/journeys-message.md#send-time-optimization)
* De API voor het bepalen van de batch is toegevoegd aan de lijst met beschikbare API&#39;s voor het aanbieden van gepersonaliseerde aanbiedingen. [Meer informatie](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## Mei 2022 {#may-2022}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van mei &#39;22 is gedetailleerd weergegeven in de documentatie. [Meer informatie](release-notes.md)
* Nieuwe queryvoorbeelden met betrekking tot [doelgroep](../reports/query-examples.md#segment-qualification-queries) en [gebeurtenissen](../reports/query-examples.md#event-based-queries) zijn toegevoegd.
* In de sectie E-mailontwerp staan nu nieuwe ingebouwde sjablonen waarmee inhoud kan worden gestart. Gerelateerde screenshots zijn bijgewerkt. [Meer informatie](../email/get-started-email-design.md)
* Koppelingen naar belangrijke bronnen zijn bijgewerkt in de homepage van Journey Optimizer-documentatie.
* Screenshots voor de openingspagina en abonnementrapportage zijn bijgewerkt. [Meer informatie](../reports/live-report.md)
* Er is een opmerking toegevoegd waarin staat dat de methode Verwijderen niet wordt ondersteund in aangepaste handelingen. [Meer informatie](../action/about-custom-action-configuration.md)
* De koppelingen naar Hoe kan ik-video&#39;s zijn bijgewerkt.
* De [E-mailconfiguratie](../configuration/about-subdomain-delegation.md), [Voorinstellingen voor berichten](../configuration/channel-surfaces.md) en [Landingspagina&#39;s configureren](../landing-pages/lp-subdomains.md) secties zijn gereorganiseerd voor betere leesbaarheid.
* De sectie URL-tracering is bijgewerkt en verbeterd met voorbeelden. [Meer informatie](../email/email-settings.md#url-tracking)
* Er is een nieuwe subsectie toegevoegd over het instellen van een e-mailadres voor verzending. U kunt dit niet doen via de gebruikersinterface. [Meer informatie](../email/email-settings.md#forward-email)

## April 2022 {#april-2022}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 22 april is in detail beschreven in de documentatie. [Meer informatie](release-notes.md)
* De **reacties** de pagina met gebeurtenisdocumentatie is bijgewerkt. [Meer informatie](../building-journeys/reaction-events.md)
* Video&#39;s voor beslissingsbeheermogelijkheden zijn bijgewerkt met Journey Optimizer-gebruikersinterface. [Meer informatie](../offers/get-started/starting-offer-decisioning.md)
* De **Aan de slag met gegevenssets** de sectie is verbeterd aan detail hoe te om tot datasets toegang te hebben en te creëren. [Meer informatie](../data/get-started-datasets.md)
* Er zijn koppelingen toegevoegd naar hulplijnen en opmerkingen bij de release van het product **Adobe Journey Optimizer-documentatie** homepage. [Meer informatie](https://experienceleague.adobe.com/docs/journey-optimizer.html)
* De **Voorinstellingen voor berichten maken** in deze sectie wordt nu aangegeven dat u niet kunt doorgaan met het maken van een voorinstelling terwijl de geselecteerde IP-pool zich in de editie bevindt (**[!UICONTROL Processing]** status) en is nooit gekoppeld aan het geselecteerde subdomein. [Meer informatie](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* Voorinstellingen voor berichten **URL-tracking** is bijgewerkt om kleine wijzigingen in de gebruikersinterface te weerspiegelen. [Meer informatie](../configuration/channel-surfaces.md#url-tracking)

## Maart 2022 {#march-2022}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 22 maart is gedetailleerd weergegeven in de documentatie. [Meer informatie](release-notes.md)
* Er is een nieuwe pagina toegevoegd aan de **Offer decisioning** , met een grondige beschrijving van de [model voor automatische optimalisatie](../offers/ranking/auto-optimization-model.md), het gebruikte algoritme en meer technische details. [Meer informatie](../offers/ranking/ai-models.md)
* De pagina voor het maken van het testprofiel is verplaatst naar de  **Publiek, profielen en identiteit** sectie. [Meer informatie](../audience/creating-test-profiles.md)
* Er is een voorbeeld toegevoegd over het toevoegen van een expressie als standaardwaarde in de expressie-editor. [Meer informatie](../building-journeys/expression/field-references.md#default-value)
* De **Aangepaste aanbiedingen maken** deze sectie is gereorganiseerd voor een betere leesbaarheid. [Meer informatie](../offers/offer-library/creating-personalized-offers.md)
* Er is een nieuw gedeelte toegevoegd waarin wordt beschreven welke gevolgen het wijzigen van de begin- en/of einddatum van een aanbieding kan hebben voor de maximale frequentie van deze aanbieding. [Meer informatie](../offers/offer-library/add-constraints.md#capping-change-date)
* De **Het primaire e-mailadres wijzigen** is bijgewerkt om de wijzigingen in de gebruikersinterface te weerspiegelen. [Meer informatie](../configuration/primary-email-addresses.md)

## Februari 2022 {#feb-2022}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] Release Feb &#39;22 is gedetailleerd in de documentatie. [Meer informatie](release-notes.md)
* De functiedocumentatiepagina&#39;s [replace](../building-journeys/functions/functionreplace.md#example_2) en [replaceAll](../building-journeys/functions/functionreplaceall.md#example) zijn bijgewerkt met aanvullende informatie en voorbeelden met betrekking tot de doelparameter.
* Er zijn best practices toegevoegd aan de pagina [Operators](../building-journeys/expression/operators.md#important-notes).

## Januari 2022 {#january-2022}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 22 januari is gedetailleerd weergegeven in de documentatie. [Meer informatie](release-notes.md)
* De **AI-classificaties van offer decisioning** is bijgewerkt met een meer gedetailleerde beschrijving van het model voor automatische optimalisatie. [Meer informatie](../offers/ranking/auto-optimization-model.md)
* Er is een nieuwe sectie toegevoegd over de schemavereisten die nodig zijn om gebeurtenistypen te kunnen verzenden bij het gebruik van een AI-model. [Meer informatie](../offers/data-collection/schema-requirement.md)
* Het gedeelte over [!DNL Journey Optimizer] personaliseringsmogelijkheden zijn gereorganiseerd voor een betere leesbaarheid . [Meer informatie](../personalization/personalize.md)
* De **Voorinstellingen voor berichten maken** voor meer duidelijkheid is dit gedeelte in verschillende secties onderverdeeld . [Meer informatie](../configuration/channel-surfaces.md#create-channel-surface)
* De **Uitschakelen, beheer** dit gedeelte is verduidelijkt en enigszins gereorganiseerd . [Meer informatie](../privacy/opt-out.md#opt-out-management)
* De **Koppelingen invoegen** is bijgewerkt met de recente wijzigingen in de gebruikersinterface. [Meer informatie](../email/message-tracking.md#insert-links)

+++

+++ 2021

## November 2021 {#november-2021}

* Een volledige beschrijving van de **geavanceerde expressie-editor** gebruikt voor reizen is nu beschikbaar . [Meer informatie](../building-journeys/expression/expressionadvanced.md)
* Een nieuwe sectie over **Methode voor subdomeindelegatie van CNAME** is toegevoegd. [Meer informatie](../configuration/delegate-subdomain.md#cname-subdomain-delegation)

## Oktober 2021 {#october-2021}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] Release okt &#39;21 is gedetailleerd in de documentatie. [Meer informatie](release-notes.md)
* Toegevoegd **Date time, functie** lijst. [Meer informatie](../personalization/functions/dates.md)
* Nieuw **Aan de slag-secties per gebruiker**. Volg uw eigen weg om sneller aan uw doelstellingen te komen! [Meer informatie](../start/quick-start.md)
* Nieuw **Een berichtvoorinstelling bewerken** sectie. [Meer informatie](../configuration/channel-surfaces.md#edit-channel-surface)
* Nieuw **Een PTR-record bewerken** sectie. [Meer informatie](../configuration/ptr-records.md#edit-ptr-record)
* Nieuw **Een berichtvoorinstelling uitschakelen** sectie. [Meer informatie](../configuration/channel-surfaces.md#edit-channel-surface#deactivate-a-surface)
* Nieuwe beperkingen toegevoegd aan de **Handleiding voor ontwikkelaars van API voor beheer van beslissingen** op-aanbieding-beperkingen die niet worden ondersteund door het mobiele [!DNL Experience Edge] workflows. [Meer informatie](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* Nieuw **Simulaties maken** sectie. [Meer informatie](../offers/offer-activities/simulation.md)
* Bijgewerkt **Beslissingsbereik toevoegen** sectie. [Meer informatie](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Bijgewerkt **Inhoud definiëren voor uw weergaven** , met inbegrip van een nieuwe [onderafdeling](../offers/offer-library/creating-personalized-offers.md#custom-text) over het definiëren en aanpassen van aangepaste tekst. [Meer informatie](../offers/offer-library/creating-personalized-offers.md#content)

## September 2021 {#september-2021}

* De volgende functiepagina&#39;s zijn bijgewerkt: [sethours](../building-journeys/functions/functionsethours.md), [getListItem](../building-journeys/functions/functiongetlistitem.md), [inSegment](../building-journeys/functions/functioninsegment.md)

* De volgende functies zijn toegevoegd: [filter](../building-journeys/functions/functionfilter.md), [intersect](../building-journeys/functions/functionintersect.md), [toDateOnly](../building-journeys/functions/functiontodateonly.md)

* Het datumtype dateOnly is toegevoegd in de documentatie van de expressie-editor. [Meer informatie](../building-journeys/expression/data-types.md)

* Er zijn details toegevoegd over de duur van de cache voor aangepaste acties. [Meer informatie](../datasource/external-data-sources.md#custom-authentication-mode)

* Informatie toegevoegd over standaardpoorten voor aangepaste acties. [Meer informatie](../action/about-custom-action-configuration.md#url-configuration)

* Informatie toegevoegd over meerdere gevallen waarin zakelijke gebeurtenissen worden gebruikt. [Meer informatie](../event/about-creating-business.md#multiple-business-events)

* Veelgebruikte voorbeelden toegevoegd voor het opvragen van Journey Step Events in Data Lake. [Meer informatie](../reports/query-examples.md)

* Een nieuwe **Beperkingen** pagina. [Meer informatie](../start/guardrails.md)

* Verbeterde **Snel starten** pagina met stappen voor verschillende personen. [Meer informatie](../start/quick-start.md)

* Nu zijn alle functies voor Beslissingsbeheer die in de desbetreffende sectie worden beschreven ook van toepassing op Adobe Experience Platform-gebruikers die gebruikmaken van de toepassingsservice van de Offer decisioning. [Meer informatie](../offers/get-started/starting-offer-decisioning.md)

* Een subsectie toegevoegd om de verschillen tussen het gebruik van regels voor publiek en beslissing bij het toepassen van een beperking om de selectie van aanbiedingen voor een bepaalde plaatsing te beperken, te verduidelijken. [Meer informatie](../offers/offer-activities/create-offer-activities.md#segments-vs-decision-rules)

* Voorbeelden van specifieke rangschikkingsformules zijn toegevoegd ter illustratie van een aantal praktijkvoorbeelden. [Meer informatie](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Een subsectie toegevoegd over het bewerken van IP-pools. [Meer informatie](../configuration/ip-pools.md#edit-ip-pool)

## Augustus 2021 {#august-2021}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 21 augustus is gedetailleerd weergegeven in de documentatie. [Meer informatie](release-notes.md)
* Bijgewerkte beslissingsbevoegdheden. [Meer informatie](../administration/ootb-product-profiles.md)
* Bijgewerkte screenshots van e-mailontwerpers met de nieuwste gebruikersinterface.
* De configuratieprocedure voor aangepaste handelingen met dynamische URL-paden en dynamische koppen is bijgewerkt. [Meer informatie](../action/about-custom-action-configuration.md#url-configuration)
* Een sectie over toegankelijkheidsfuncties en sneltoetsen toegevoegd. [Meer informatie](../start/user-interface.md#accessibility)
* Een sectie toegevoegd over de evaluatiemethoden voor het publiek. [Meer informatie](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* Toegevoegde notities bij de lijst Onderdrukking, de secties Lijst van gewenste personen en E-mail global/live om aan te geven dat profielen met de status Onderdrukt en Niet toegestaan zijn uitgesloten van het e-mailrapport Metriek verzonden. [Meer informatie](../reports/global-report.md)
* Er is een nieuwe sectie toegevoegd waarin wordt beschreven hoe e-mailadressen of domeinen kunnen worden opgehaald die zijn uitgesloten van een verzendende server omdat deze zich niet op de lijst van gewenste personen bevonden. [Meer informatie](../configuration/allow-list.md#reporting)
* De sectie lijst van gewenste personen inschakelen is bijgewerkt. [Meer informatie](../configuration/allow-list.md#enable-allow-list)
* De sectie met voorinstellingen voor monitorberichten is bijgewerkt met de mogelijke oorzaken van een eventuele fout bij het maken van de voorinstelling en details over dergelijke fouten. [Meer informatie](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* De sectie Tijdsperiode voor opnieuw proberen is bijgewerkt en de naam is gewijzigd om aan te geven dat u de instelling voor het opnieuw proberen van e-mail nu kunt aanpassen in de voorinstellingen voor berichten. [Meer informatie](../configuration/retries.md#retry-duration)
* Er is een nieuwe sectie toegevoegd waarin wordt beschreven hoe u met één klik een koppeling om te weigeren kunt invoegen in e-mailinhoud. [Meer informatie](../privacy/opt-out.md#one-click-opt-out-link)
* De subdomeinsectie Delegeren is bijgewerkt met meer gedetailleerde informatie over het validatieproces dat door de Adobe wordt uitgevoerd. [Meer informatie](../configuration/delegate-subdomain.md#subdomain-validation)
* Er is een sectie toegevoegd waarin wordt beschreven hoe u handmatig e-mailadressen en domeinen aan de suppressielijst kunt toevoegen. [Meer informatie](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* De [De lijst met onderdrukking openen](../configuration/manage-suppression-list.md#access-suppression-list) en [Opnieuw](../configuration/retries.md) secties om de nieuwe gebruikersinterface te weerspiegelen.
* De nieuwe flow om weergaven toe te voegen en te configureren wanneer u een aanbod maakt, is gedocumenteerd. [Meer informatie](../offers/offer-library/creating-personalized-offers.md#representations)

## Juli 2021 {#july-2021}

* Alle nieuwe functies en verbeteringen die worden geleverd bij [!DNL Journey Optimizer] De release van 21 juli is gedetailleerd weergegeven in de documentatie. [Meer informatie](release-notes.md)
* Extra directe verbindingen aan de documentatie van de diensten van het Experience Platform in [!DNL Journey Optimizer] homepage en inhoudsopgave
* Nieuwe bestemmingspagina&#39;s voor de diensten van het Experience Platform beschikbaar in [!DNL Journey Optimizer]
* Koppelingen toegevoegd aan [!DNL Journey Optimizer] productbeschrijving op de homepage
* Videozelfstudie toegevoegd op meerdere pagina&#39;s
* Geoptimaliseerde homepage-images
* Verplaatst, verbeterd en de naam van de sectie &#39;Bericht bijhouden&#39; is gewijzigd in &#39;Koppelingen toevoegen en berichten bijhouden&#39;. [Meer informatie](../email/message-tracking.md)
* Een subsectie toegevoegd op spiegelpagina&#39;s. [Meer informatie](../email/message-tracking.md#mirror-page)
* In documentatie en schermen hernoemd tot &#39;aanbiedingsactiviteiten&#39; als &#39;besluiten&#39; en &#39;besluiten&#39; als &#39;besluiten&#39;. [Meer informatie](../offers/get-started/starting-offer-decisioning.md)
* Nieuwe gebruikscase: [personaliseren een bericht met hulpfuncties](../personalization/personalization-use-case-helper-functions.md)
* Bijgewerkt de Lees publieksdocumentatie om de concretiseerde segmentgevolgen te weerspiegelen. [Meer informatie](../building-journeys/read-audience.md)
* De beperkingen voor de reis zijn bijgewerkt. [Meer informatie](../start/guardrails.md)
* Bijgewerkt Configure aanbiedingen selectie in beslissingssectie. [Meer informatie](../offers/offer-activities/configure-offer-selection.md)
* Er is een waarschuwing toegevoegd om aan te geven dat op gebeurtenissen gebaseerde aanbiedingen momenteel niet worden ondersteund. [Meer informatie](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Documenteerde het nieuwe Besluit Management **[!UICONTROL Overview]** tab. [Meer informatie](../offers/get-started/user-interface.md#overview)
* Nieuwe secties toegevoegd om de acties te beschrijven die beschikbaar zijn op de lijsten met aanbiedingen en besluiten: [Aanbiedingslijst](../offers/offer-library/creating-personalized-offers.md#offer-list) en [Beslissingslijst](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
