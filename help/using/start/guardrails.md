---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer-instructies en beperkingen
description: Meer informatie over Journey Optimizer guardrails
feature: Journeys
topic: Content Management
role: User
level: Intermediate
mini-toc-levels: 1
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 74723337f97c8196b506ccc1ace11077710494ea
workflow-type: tm+mt
source-wordcount: '2915'
ht-degree: 0%

---

# Afvoerkanalen en beperkingen {#limitations}

Hieronder vindt u aanvullende instructies en beperkingen wanneer u [!DNL Adobe Journey Optimizer] gebruikt.

De rechten, de productbeperkingen en de prestatiesbegeleiding worden vermeld in [ Adobe Journey Optimizer pagina van de productbeschrijving ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.


>[!CAUTION]
>
>* [ Grafieken voor gegevens en segmentatie van het Profiel van de Klant in real time ](https://experienceleague.adobe.com/en/docs/experience-platform/profile/guardrails){target="_blank"} zijn ook op Adobe Journey Optimizer van toepassing.
>
>* Zie ook [ Grafieken voor de Ingestie van Gegevens in het Profiel van de Klant in real time ](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/guardrails){target="_blank"}


## Ondersteunde browsers {#browsers}

De Adobe [!DNL Journey Optimizer] -interface is ontworpen om optimaal te werken in de nieuwste versie van Google Chrome. Mogelijk kunt u problemen ondervinden bij het gebruik van bepaalde functies in oudere versies of andere browsers.

## Gegevenssethandleidingen {#datasets-guardrails}

Vanaf Februari 2025, wordt een tijd-aan-levende (TTL) guardrail opgesteld uit aan systeem-geproduceerde datasets van Journey Optimizer in **nieuwe zandbakken en nieuwe organisaties** als volgt:

* 90 dagen voor gegevens in de profielopslag,
* 13 maanden voor gegevens in het data Lake.

Deze verandering zal uit aan **bestaande klantenzandbakken** in een verdere fase worden opgerold. [ leer meer over datasets tijd-aan-Levende (TTL) guardrails ](../data/datasets-ttl.md)

## Kanaalhulplijnen {#channel-guardrails}

>[!NOTE]
>
>In zeldzame gevallen kunnen tijdelijke onderbrekingen in een bepaalde regio ertoe leiden dat geldige profielen van reizen worden uitgesloten, of dat poststukken ten onrechte als tussenruimten worden gemarkeerd. Zodra de diensten worden hersteld, hercontroleer reislogboeken, verifieer de gebieden van het toestemmingsprofiel, en herpubliceer de reis indien nodig. In het geval van een ISP stroomonderbreking, leer hoe te om profielen uit de suppressielijst in [ te verwijderen deze sectie ](../configuration/manage-suppression-list.md#remove-from-suppression-list).
>

### E-mailhandleidingen {#message-guardrails}

<!--The following guardrails apply to the [email channel](../../rp_landing_pages/email-landing-page.md):-->

De volgende gidsen zijn op het [ e-mailkanaal ](../email/get-started-email.md) van toepassing:

* U kunt niet hetzelfde verzendende domein gebruiken om e-mailberichten te verzenden vanuit [!DNL Adobe Journey Optimizer] en vanuit een ander product, zoals [!DNL Adobe Campaign] of [!DNL Adobe Marketo Engage] .

Bij het ontwerpen van e-mailberichten controleert het systeem op de belangrijkste instellingen en geeft het waarschuwingen weer voor waarschuwingen (aanbevelingen en aanbevolen procedures) en fouten (problemen die het testen of activeren verhinderen). Leer meer over e-mailalarm en bevestigingsvereisten in [ deze sectie ](../email/create-email.md#check-email-alerts).

### SMS-handleidingen {#sms-guardrails}

De volgende guardrails zijn op het [ kanaal van SMS ](../sms/get-started-sms.md) van toepassing:

* Mediabestanden voor MMS kunnen via een ondersteunde URL worden opgenomen. Controleer of het mediabestand afzonderlijk is geüpload.
* Berichtfeedback synchroniseren is momenteel niet beschikbaar voor MMS.
* Het beheer van de toestemming werkt op het kanaalniveau van SMS voor MMS.

### Binnenkomende kanaalhulplijnen {#inbound-guardrails}

* Journey Optimizer ondersteunt een piekvolume van 5.000 binnenkomende verzoeken per seconde. Deze graadlijn is op alle binnenkomende verzoeken van toepassing, die uit om het even welke Journey Optimizer gesteunde binnenkomende kanalen ([ Web ](../web/get-started-web.md), [ In-app ](../in-app/get-started-in-app.md), [ code-gebaseerde ervaringen ](../code-based/get-started-code-based.md), [ inhoudskaarten ](../../rp_landing_pages/content-card-landing-page.md)) kunnen voortkomen.

  Binnenkomende Journey Optimizer-kanalen zijn gericht op nieuwe profielen die mogelijk nog niet eerder zijn ingeschakeld op andere kanalen. Hierdoor wordt het totale aantal aanspreekbare profielen verhoogd. Dit kan kosten met zich meebrengen als het contractuele aantal aanschafbare profielen dat u hebt aangeschaft, wordt overschreden.

  De metriek van de vergunning voor elk pakket is vermeld op de [ pagina van de Beschrijving van het Product van Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

* Journey Optimizer biedt op elk gewenst moment ondersteuning voor maximaal 500 actieve acties. Deze binnenkomende acties ([ Web ](../web/get-started-web.md), [ In-app ](../in-app/get-started-in-app.md), [ op code-gebaseerde ervaringen ](../code-based/get-started-code-based.md), [ inhoudskaarten ](../../rp_landing_pages/content-card-landing-page.md)) worden geteld als zij deel van een levende campagne uitmaken of als zij een knoop zijn die in een levende reis wordt gebruikt. Wanneer u dit aantal bereikt, moet u oudere campagnes of reizen deactiveren die binnenkomende acties gebruiken alvorens nieuwe te kunnen lanceren.

* Om [ code-gebaseerde ervaring ](../code-based/get-started-code-based.md) acties in [!DNL Journey Optimizer] te gebruiken en de lading van de codeinhoud te leveren die door uw toepassingen kan worden gebruikt, volg de eerste vereisten die op [ worden gedetailleerd deze pagina ](../code-based/code-based-prerequisites.md).

### Handleidingen voor Transactieberichten {#transactional-message-guardrails}

Journey Optimizer ondersteunt een piekvolume van 500 transactieberichten per seconde in campagnes.

## Handleidingen voor landingspagina&#39;s {#lp-guardrails}

De volgende gidsen zijn op de [ landende pagina&#39;s ](../landing-pages/get-started-lp.md) van toepassing:

* Slechts één **component van de Vorm** kan in één enkele primaire pagina worden gebruikt.
* De **component van de Vorm** kan niet in subpages worden gebruikt.
* U kunt geen preheader toevoegen aan een openingspagina.
* U kunt niet de **Code uw eigen** optie selecteren wanneer het ontwerpen van een het landen primaire pagina.

## Subdomeinen guardraals {#subdomain-guardrails}

De guardrails en de beperkingen die op subdomain delegatie in Journey Optimizer van toepassing zijn worden gedetailleerd op [ deze pagina ](../configuration/delegate-subdomain.md#guardrails).

## Fragmenten, ardraals {#fragments-guardrails}

De volgende gidsen zijn op de [ fragmenten ](../content-management/fragments.md) van toepassing:

* Om, fragmenten tot stand te brengen uit te geven, te archiveren en te publiceren hebt u de **[!DNL Manage library items]** nodig en **[publiceer de toestemmingen van het Fragment]** inbegrepen in het **[!DNL Content Library Manager]** productprofiel. [Meer informatie](../administration/ootb-product-profiles.md#content-library-manager)
* Visuele fragmenten zijn alleen beschikbaar voor het e-mailkanaal.
* Expressiefragmenten zijn niet beschikbaar voor het kanaal in de app.
* Visuele fragmenten mogen niet groter zijn dan 100 kB. Expressiefragmenten mogen niet groter zijn dan 200 kB.
* Om een fragment in een reis of een campagne te gebruiken, moet het in **Levende** status zijn.
* [ Contextafhankelijke attributen ](../personalization/personalization-build-expressions.md) worden niet gesteund binnen fragmenten.
* Visuele fragmenten zijn niet kruiscompatibel tussen de modi Thema&#39;s gebruiken en Handmatige stijlen. Als u een fragment wilt kunnen gebruiken in inhoud waarop u een thema wilt toepassen, moet dit fragment worden gemaakt in de modus Thema&#39;s gebruiken. [ leer meer over thema&#39;s ](../email/apply-email-themes.md)
* Wanneer het volgen in een reis of een campagne wordt toegelaten, als u verbindingen aan een fragment toevoegt en als dit fragment in een bericht wordt gebruikt, worden deze verbindingen gevolgd zoals alle andere verbindingen inbegrepen in het bericht. [ leer meer op verbindingen en het volgen ](../email/message-tracking.md)

## Garanties voor publiek en profiel {#audience}

* U kunt maximaal 10 publiekscomposities in een bepaalde sandbox publiceren. Als u deze drempel hebt bereikt, moet u een samenstelling schrappen om ruimte vrij te maken en nieuwe te publiceren.

  Leer meer over publiekssamenstellingen op [ deze pagina ](../audience/get-started-audience-orchestration.md).

* Bij het invoeren van gegevens zijn e-mails hoofdlettergevoelig. Dit betekent dat er dubbele profielen kunnen worden gemaakt (bijvoorbeeld één profiel voor John.Greene@luma.com, een ander profiel voor john.greene@luma.com) en gebruikt wanneer u zich richt op de overeenkomstige ontvanger tijdens uw [!DNL Journey Optimizer] -reizen en -campagnes.

## Garanties voor besluitvorming en besluitvorming {#decisioning-guardrails}

In de afdelingen Beslissingen en Beslissingsbeheer worden de volgende informatie gegeven over de beperkingen en beperkingen waarmee rekening moet worden gehouden bij het werken met besluiten of het nemen van besluiten:

* [Afbakening en beperkingen](../experience-decisioning/decisioning-guardrails.md)
* [Beheersbeheerinstructies en beperkingen](../offers/decision-management-guardrails.md)

## Reisgeleiders {#journeys-guardrails}

### Algemene reisgeleiders {#journeys-guardrails-journeys}

* Het aantal activiteiten op een reis is beperkt tot 50. Het aantal activiteiten wordt weergegeven in de linkerbovensectie van het reiscanvas. Dit zal helpen in leesbaarheid, QA en het oplossen van problemen.
* Standaard is het aantal ritten in één keer tijdens de uitvoering tijdens het vervoer per dag beperkt tot 100.  Het huidige aantal reizen wordt weergegeven boven het canvas van de reis.
* Tijdens het publiceren van reizen worden de schaal en de stabiliteit automatisch aangepast om een maximale doorvoer en stabiliteit te garanderen. Aangezien u dichtbij de mijlpaal van 100 levende reizen in één keer, zult u een bericht over deze verwezenlijking zien verschijnen in UI. Als u deze melding ziet en uw reizen moet verlengen tot meer dan 100 rechtstreekse reizen tegelijk, maak dan een ticket voor de klantenservice en wij helpen u uw doelstellingen te bereiken.
* Wanneer u een publiekskwalificatie gebruikt op een reis, kan het tot 10 minuten duren voordat de activiteit van de publiekskwalificatie actief is en naar profielen luistert die het publiek binnenkomen of verlaten.
* Een reisinstantie voor een profiel heeft een maximumgrootte van 1 MB. Alle gegevens die als onderdeel van de uitvoering van de reis worden verzameld, worden opgeslagen in die reisinstantie. Daarom gegevens van een binnenkomende gebeurtenis, profielgegevens die zijn opgehaald uit Adobe Experience Platform, aangepaste reacties op acties, enzovoort. worden opgeslagen in die reisinstantie en beïnvloeden de reisgrootte. Wanneer een reis met een evenement begint, wordt het aanbevolen de maximale omvang van die lading (bv. minder dan 800 kB) te beperken om te voorkomen dat die limiet na een paar activiteiten wordt bereikt, in de uitvoering van de reis. Wanneer deze limiet is bereikt, heeft het profiel een foutstatus en wordt het van de reis uitgesloten.
* Naast de time-out die wordt gebruikt bij reisactiviteiten, is er ook een wereldwijde reistime-out die niet in de interface wordt weergegeven en niet kan worden gewijzigd. Deze wereldwijde time-out houdt de voortgang van individuen op de reis 91 dagen na hun binnenkomst tegen. [Meer informatie](../building-journeys/journey-properties.md#global_timeout)

### Algemene acties {#general-actions-g}

De volgende gidsen zijn op de [ Acties ](../building-journeys/about-journey-activities.md) in uw reizen van toepassing:

* In het geval van een fout worden drie pogingen systematisch opnieuw uitgevoerd. U kunt het aantal pogingen niet aanpassen volgens het ontvangen foutbericht. Retries wordt uitgevoerd voor alle HTTP-fouten, behalve voor HTTP 401, 403 en 404.
* De ingebouwde **gebeurtenis van de Reactie** staat u toe om op uit-van-de-doos acties te reageren. Leer meer op [ deze pagina ](../building-journeys/reaction-events.md). Als u op een bericht wilt reageren dat via een douaneactie wordt verzonden, moet u een specifieke gebeurtenis vormen.
* U kunt geen twee acties parallel plaatsen, u moet hen één na andere toevoegen.
* Een profiel kan niet veelvoudige tijden in de zelfde reis, tezelfdertijd, voor alle actieve [ versies van de reis ](../building-journeys/publish-journey.md#create-a-new-version-of-a-journey-journey-create-new-version) zijn. Als de terugkeer wordt toegelaten, kan een profiel een reis opnieuw ingaan, maar kan het niet doen tot hij dat vorige geval van de reis volledig verliet. [Meer informatie](../building-journeys/end-journey.md)

### Journeyversies {#journey-versions-g}

De volgende gidsen zijn op de [ versies van de Reis ](../start/user-interface.md) van toepassing:

* Een reis die begint met een gebeurtenisactiviteit in v1 kan niet met iets anders beginnen dan een gebeurtenis in verdere versies. U kunt geen reis met de gebeurtenis van de Kwalificatie van het a **publiek beginnen**.
* Een reis die met a **activiteit begint van de Kwalificatie van het Publiek** in v1 moet altijd met de Kwalificatie van het Publiek **in verdere versies beginnen.**
* Het publiek en namespace die in **de Kwalificatie van het Publiek** (eerste knoop) worden gekozen kunnen niet in nieuwe versies worden veranderd.
* De regel van de terugkeer moet het zelfde in alle reisversies zijn.
* Een reis die met a **begint Gelezen Publiek** kan niet met een andere gebeurtenis in volgende versies beginnen.
* U kunt geen nieuwe versie maken van een leestoegang met incrementeel lezen. U moet de reis dupliceren.

### Aangepaste acties {#custom-actions-g}

De volgende gidsen zijn op de [ Acties van de Douane ](../action/action.md) in uw reizen van toepassing:

* Voor alle aangepaste handelingen, per host en per sandbox wordt een limiet van 300.000 aanroepen per minuut gedefinieerd. Verwijs naar [ deze pagina ](../action/about-custom-action-configuration.md). Deze grens is geplaatst gebaseerd op klantengebruik, om externe eindpunten te beschermen die door douaneacties worden gericht. Indien nodig, kunt u deze het plaatsen met voeten treden door een grotere het maximum van het maximum of het vertragen grens door onze Capping/het Draaien APIs te bepalen. Zie [deze pagina](../configuration/external-systems.md).
* De URL van de aangepaste handeling ondersteunt geen dynamische parameters.
* POST-, PUT- en GET-callmethoden worden ondersteund
* De naam van de queryparameter of -header mag niet beginnen met &quot;.&quot; of &quot;$&quot;
* IP-adressen zijn niet toegestaan
* Interne Adobe-adressen (`.adobe.*`) zijn niet toegestaan in URL&#39;s en API&#39;s.
* Ingebouwde aangepaste handelingen kunnen niet worden verwijderd.
* Aangepaste acties bieden alleen ondersteuning voor de JSON-indeling als u een aanvraag- of antwoordlading gebruikt. Zie [deze pagina](../action/about-custom-action-configuration.md#custom-actions-limitations).
* Wanneer het kiezen van een eindpunt om het gebruiken van een douaneactie te richten, ben zeker dat:

   * Dit eindpunt kan de productie van de reis steunen, gebruikend configuraties van [ het Throttling API ](../configuration/throttling.md) of [ Capping API ](../configuration/capping.md) om het te beperken. Wees voorzichtig dat een snelheidsbegrenzingsconfiguratie niet lager kan zijn dan 200 TPS. Om het even welk gericht eindpunt moet minstens 200 TPS steunen.
   * Dit eindpunt moet een reactietijd hebben zo laag mogelijk. Afhankelijk van uw verwachte productie, zou het hebben van een hoge reactietijd de daadwerkelijke productie kunnen beïnvloeden.

### Gebeurtenissen {#events-g}

De volgende gidsen zijn op de [ Gebeurtenissen ](../event/about-events.md) in uw reizen van toepassing:

* Journey Optimizer ondersteunt een piekvolume van 5.000 inkomende reisgebeurtenissen per seconde, over alle sandboxen. Leer meer over deze beperking [ op deze pagina ](../event/about-events.md#event-thoughput).
* Het kan tot 5 minuten duren voordat de eerste actie tijdens de reis wordt uitgevoerd.
* Voor door het systeem gegenereerde gebeurtenissen moeten streaminggegevens die worden gebruikt om een klantentraject te starten, eerst binnen Journey Optimizer worden geconfigureerd om een unieke orchestratie-id te verkrijgen. Deze orkest-id moet worden toegevoegd aan de streaminglading die naar Adobe Experience Platform komt. Deze beperking geldt niet voor op regels gebaseerde gebeurtenissen.
* Zakelijke evenementen kunnen niet worden gebruikt in combinatie met monitaire evenementen of kwalificatieactiviteiten voor het publiek.
* Eenheidstrajecten (te beginnen met een evenement of een kwalificatie van het publiek) bevatten een begeleidend element dat voorkomt dat ritten bij dezelfde gebeurtenis meerdere keren ten onrechte worden gestart. De ingang van het profiel wordt tijdelijk geblokkeerd door gebrek gedurende 5 minuten. Bijvoorbeeld, als een gebeurtenis een reis bij 12 :01 voor een specifiek profiel teweegbrengt en een andere bij 12 :03 aankomt (of het de zelfde gebeurtenis of verschillende is die de zelfde reis teweegbrengen) die reis niet opnieuw voor dit profiel zal beginnen.
* Journey Optimizer vereist dat gebeurtenissen worden gestreamd naar Data Collection Core Service (DCCS) om een reis te kunnen activeren. Gebeurtenissen die worden ingevoerd in batch of gebeurtenissen uit interne Journey Optimizer-gegevenssets (Berichtfeedback, E-mailtracking, enz.) kunnen niet worden gebruikt om een reis te activeren. Voor gebruiksgevallen waar u gestreamde gebeurtenissen niet kunt krijgen, moet u een publiek bouwen dat op die gebeurtenissen wordt gebaseerd en in plaats daarvan de **Gelezen activiteit van het Publiek** gebruiken. De kwalificatie van het publiek kan technisch worden gebruikt, maar wordt niet geadviseerd omdat het stroomafwaartse uitdagingen kan veroorzaken die op de gebruikte acties worden gebaseerd.

### Gegevensbronnen {#data-sources-g}

De volgende gidsen zijn op de [ Bronnen van Gegevens ](../datasource/about-data-sources.md) in uw reizen van toepassing:

* De externe gegevensbronnen kunnen binnen een klantenreis worden gebruikt om externe gegevens in echt op te zoeken - tijd. Deze bronnen moeten bruikbaar zijn via REST API, JSON ondersteunen en het volume van aanvragen kunnen verwerken.
* Interne Adobe-adressen (`.adobe.*`) zijn niet toegestaan in URL&#39;s en API&#39;s.

>[!NOTE]
>
>Aangezien de reacties nu worden gesteund, zou u douaneacties in plaats van gegevensbronnen voor externe gegevensbronnen moeten gebruiken-gevallen.

### Reizen en profiel maken {#journeys-limitation-profile-creation}

Er is een vertraging verbonden aan het maken/bijwerken van een op API gebaseerd profiel in Adobe Experience Platform. Het doel van het Niveau van de Dienst (SLT) in termen van latentie is &lt; 1 min van opname aan Verenigd Profiel voor 95th percentiel van verzoeken, bij een volume van 20K Verzoeken per seconde (RPS).

Als een reis gelijktijdig aan een profielverwezenlijking wordt teweeggebracht en onmiddellijk controleert/informatie van de Dienst van het Profiel terugwint, zou het niet behoorlijk kunnen werken.

U kunt uit één van deze twee oplossingen kiezen:

* Voeg een wachttijdactiviteit toe na de eerste gebeurtenis om Adobe Experience Platform de tijd te geven die nodig is om de opname naar de profielservice uit te voeren.

* Stel een reis in die niet onmiddellijk gebruikmaakt van het profiel. Als de reis bijvoorbeeld is ontworpen om het aanmaken van een account te bevestigen, kan de ervaringsgebeurtenis informatie bevatten die nodig is om het eerste bevestigingsbericht te verzenden (voornaam, achternaam, e-mailadres, enz.).


### Aanvullende id&#39;s {#supplemental}

Specifieke garanties gelden voor het gebruik van aanvullende identificatiemiddelen op reizen. Zij zijn vermeld in [ deze pagina ](../building-journeys/supplemental-identifier.md#guardrails).

### Expression-editor {#expression-editor}

De volgende gidsen zijn op de [ redacteur van de reisuitdrukking ](../building-journeys/expression/expressionadvanced.md) van toepassing:

* U kunt gebeurtenisveldgroepen niet gebruiken voor reizen die beginnen met een leespubliek, een kwalificatie Audience of een activiteit voor een zakelijke gebeurtenis. U moet een nieuw publiek maken en de voorwaarde `inaudience` gebruiken tijdens de rit.
* `timeSeriesEvents` -kenmerken kunnen niet worden gebruikt in de expressie-editor. Maak een nieuwe veldgroep op basis van een `XDM ExperienceEvent` -schema voor toegang tot Experience Events op profielniveau.

### Reisactiviteiten {#activities}

#### Kwalificatieactiviteit van het publiek {#audience-qualif-g}

De volgende richtlijn is op de [ de reisactiviteit van de Kwalificatie van het publiek 0} van toepassing:](../building-journeys/audience-qualification-events.md)

* De kwalificatie-activiteit Publiek kan niet worden gebruikt met Adobe Campaign-activiteiten.
* Aanvullende id&#39;s worden niet ondersteund voor de kwalificatie Publiek.

Leer meer over de tarieven van de reisverwerking en productielimieten in [ deze sectie ](../building-journeys/entry-management.md#journey-processing-rate).

#### Campagne {#ac-g}

De volgende instructies zijn van toepassing op de activiteiten **[!UICONTROL Campaign v7/v8]** en **[!UICONTROL Campaign Standard]** :

* Adobe Campaign-activiteiten kunnen niet worden gebruikt met een Read-publiek of met een Audience-kwalificatieactiviteit.
* Campagne-activiteiten kunnen niet worden gebruikt met andere kanaalactiviteiten: kaart, ervaring op basis van code, e-mail, push, SMS, In-app berichten, Web.

#### Activiteiten in de app {#in-app-activity-limitations}

De volgende instructies zijn van toepassing op de handeling **[!UICONTROL In-app message]** . Leer meer over in-app berichten op [ deze pagina ](../in-app/create-in-app.md).

* Deze functie is momenteel niet beschikbaar voor klanten in de gezondheidszorg.

* Personalization kan alleen profielkenmerken bevatten.

* De activiteiten in de app kunnen niet worden gebruikt met Adobe Campaign-activiteiten.

* De weergave in de app is gekoppeld aan de duur van de rit. Dit houdt in dat wanneer de reis voor een profiel afloopt, alle in-app-berichten binnen die reis niet meer worden weergegeven voor dat profiel.  Het is daarom niet mogelijk om een bericht in de app rechtstreeks te stoppen van een reisactiviteit. In plaats daarvan moet u de hele reis beëindigen om te voorkomen dat de berichten in de app naar het profiel worden weergegeven.

* In de testmodus is de weergave in de app afhankelijk van de levensduur van de rit. Als u wilt voorkomen dat de reis te vroeg eindigt tijdens het testen, past u de **[!UICONTROL Wait time]** -waarde voor uw **[!UICONTROL Wait]** -activiteiten aan.

* **[!UICONTROL Reaction]** -activiteiten kunnen niet worden gebruikt om te reageren op een geopende of geklikte In-app.

* Er kan een activeringsvertraging optreden tussen het moment dat een gebruikersprofiel een in-app-activiteit op het canvas bereikt en het moment waarop het bericht in de app wordt weergegeven.

* De inhoud van berichten in de app is beperkt tot 2 MB. Het opnemen van grote afbeeldingen kan het publicatieproces belemmeren.

#### Snelheid {#jump-g}

Specifieke instructies zijn van toepassing op de **[!UICONTROL Jump]** -activiteit. Zij zijn vermeld op [ deze pagina ](../building-journeys/jump.md#jump-limitations).

#### Lees de publieksactiviteit {#read-segment-g}

De volgende gidsen zijn op [ Gelezen de reisactiviteit van het publiek ](../building-journeys/read-audience.md) van toepassing:

* Gestroomlijnde doelgroepen zijn altijd up-to-date, maar batchdoelgroepen worden niet berekend tijdens het ophalen. Ze worden alleen elke dag geëvalueerd op het tijdstip van de dagelijkse batchevaluatie.
* Voor reizen die a **gebruiken Gelezen de activiteit van het publiek**, is er een maximumaantal reizen dat precies tezelfdertijd kan beginnen. De pogingen zullen door het systeem worden uitgevoerd maar gelieve te vermijden hebbend meer dan vijf reizen (met **Gelezen Publiek**, gepland of die &quot;zo spoedig mogelijk&quot;beginnen) op het nauwkeurige zelfde ogenblik door hen over tijd, bijvoorbeeld 5 tot 10 minuten uit elkaar te spreiden. Leer meer over de tarieven van de reisverwerking in [ deze sectie ](../building-journeys/entry-management.md#journey-processing-rate).
* De **Gelezen activiteit van het publiek** kan niet met de activiteiten van Adobe Campaign worden gebruikt.
* De **Gelezen activiteit van het Publiek** kan slechts als eerste activiteit in een reis, van na een bedrijfsgebeurtenisactiviteit worden gebruikt.
* Een reis kan slechts één **Gelezen activiteit van het Publiek** hebben.
* Zie ook aanbevelingen over hoe te om **te gebruiken las de activiteit van het publiek** op [ deze pagina ](../building-journeys/read-audience.md).
* De pogingen worden toegepast door gebrek op publiek-getriggerde reizen (die met a **Gelezen Publiek** of a **BedrijfsGebeurtenis** beginnen) terwijl het terugwinnen van de uitvoerbaan. Als er een fout optreedt tijdens het maken van de exporttaak, worden de pogingen om de 10mn opnieuw uitgevoerd, tot maximaal 1 uur. Daarna zullen we het als een mislukking beschouwen. Deze soorten reizen kunnen daarom tot 1 uur na de geplande tijd worden uitgevoerd.
* Voor ritten die gebruikmaken van aanvullende id&#39;s, is de leessnelheid van de activiteit van het leespubliek voor elke reisinstantie beperkt tot maximaal 500 profielen per seconde.

Zie ook [ deze pagina ](../building-journeys/read-audience.md#must-read).

#### Profielactiviteit bijwerken {#update-profile-g}

Specifieke instructies zijn van toepassing op de **[!UICONTROL Update profile]** -activiteit. Zij zijn vermeld op [ deze pagina ](../building-journeys/update-profiles.md).

## Garanties voor campagneorganisatie {#orchestration-guardrails}

De gidsen en de beperkingen om in mening te houden wanneer het werken met de Orchestratie van de Campagne zijn gedetailleerd in deze sectie: [ Grails &amp; beperkingen ](../orchestrated/guardrails.md).
