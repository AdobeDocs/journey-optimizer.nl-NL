---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer-instructies en beperkingen
description: Meer informatie over Journey Optimizer guardrails
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: a2e4a6c15ea9e6a96544eaa8f58dc0cd55854bbe
workflow-type: tm+mt
source-wordcount: '2464'
ht-degree: 0%

---

# Afvoerkanalen en beperkingen {#limitations}

Hieronder vindt u aanvullende instructies en beperkingen wanneer u [!DNL Adobe Journey Optimizer] gebruikt.

De rechten, de productbeperkingen en de prestatiesbegeleiding worden vermeld in [ Adobe Journey Optimizer pagina van de productbeschrijving ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

U moet zich ook bewust zijn van [ Gidsen voor de gegevens van het Profiel van de Klant in real time ](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html){target="_blank"} alvorens te beginnen.

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

De volgende gidsen zijn op het [ e-mailkanaal ](../email/get-started-email.md) van toepassing:

* U kunt geen bijlagen aan een e-mailbericht toevoegen met [!DNL Journey Optimizer] .
* U kunt niet hetzelfde verzendende domein gebruiken om berichten van [!DNL Adobe Journey Optimizer] en van een ander product, zoals [!DNL Adobe Campaign] of [!DNL Adobe Marketo Engage] , te verzenden.

### SMS-handleidingen {#sms-guardrails}

De volgende guardrails zijn op het [ kanaal van SMS ](../sms/get-started-sms.md) van toepassing:

* Mediabestanden voor MMS kunnen via een ondersteunde URL worden opgenomen. Controleer of het mediabestand afzonderlijk is geüpload.
* Berichtfeedback synchroniseren is momenteel niet beschikbaar voor MMS.
* Het beheer van de toestemming werkt op het kanaalniveau van SMS voor MMS.

### Webkanaalhulplijnen {#web-guardrails}

[!DNL Journey Optimizer] [ Webcampagnes ](../web/get-started-web.md) richten nieuwe profielen die niet eerder op andere kanalen zijn betrokken. Hierdoor wordt het totale aantal aanspreekbare profielen verhoogd. Dit kan kosten met zich meebrengen als het contractuele aantal aanschafbare profielen dat u hebt aangeschaft, wordt overschreden.

De metriek van de vergunning voor elk pakket is vermeld op de [ pagina van de Beschrijving van het Product van Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

### Kanaalhulplijnen op basis van code {#code-based-guardrails}

Om code-gebaseerde ervaringsacties in [!DNL Journey Optimizer] te gebruiken en de lading van de codeinhoud te leveren die door uw toepassingen kan worden gebruikt, volg de eerste vereisten die op [ worden gedetailleerd deze pagina ](../code-based/code-based-prerequisites.md).

## Handleidingen voor landingspagina&#39;s {#lp-guardrails}

De volgende gidsen zijn op de [ landende pagina&#39;s ](../landing-pages/get-started-lp.md) van toepassing:

* Slechts één **component van de Vorm** kan in één enkele primaire pagina worden gebruikt.
* De **component van de Vorm** kan niet in subpages worden gebruikt.
* U kunt geen preheader toevoegen aan een openingspagina.
* U kunt niet de **Code uw eigen** optie selecteren wanneer het ontwerpen van een het landen primaire pagina.

## Subdomeinen guardraals {#subdomain-guardrails}

In [!DNL Journey Optimizer] kunt u standaard maximaal 10 subdomeinen delegeren (voor zowel e-mail- als webkanalen).

Afhankelijk van uw licentiecontract kunt u echter maximaal 100 subdomeinen delegeren. Neem contact op met uw Adobe-contactpersoon voor meer informatie over het aantal subdomeinen waarop u recht hebt.

Leer meer over domeindelegatie op [ deze pagina ](../configuration/delegate-subdomain.md).

## Fragmenten, ardraals {#fragments-guardrails}

De volgende gidsen zijn op de [ fragmenten ](../content-management/fragments.md) van toepassing:

* Visuele fragmenten zijn alleen beschikbaar voor het e-mailkanaal.
* Expressiefragmenten zijn niet beschikbaar voor het kanaal in de app.

## Audiëntenguardrails {#audience}

U kunt maximaal 10 publiekscomposities in een bepaalde sandbox publiceren. Als u deze drempel hebt bereikt, moet u een samenstelling schrappen om ruimte vrij te maken en nieuwe te publiceren.

Leer meer over publiekssamenstellingen op [ deze pagina ](../audience/get-started-audience-orchestration.md).

## Garanties voor besluitvorming en besluitvorming {#decisioning-guardrails}

In de afdelingen Beslissingen en Beslissingsbeheer worden de volgende informatie gegeven over de beperkingen en beperkingen waarmee rekening moet worden gehouden bij het werken met besluiten of het nemen van besluiten:

* [Afbakening en beperkingen](../experience-decisioning/decisioning-guardrails.md)
* [Beheersbeheerinstructies en beperkingen](../offers/decision-management-guardrails.md)


## Reisgeleiders {#journeys-guardrails}

### Algemene reisgeleiders {#journeys-guardrails-journeys}

* Het aantal activiteiten op een reis is beperkt tot 50. Het aantal activiteiten wordt weergegeven in de linkerbovensectie van het reiscanvas. Dit zal helpen in leesbaarheid, QA en het oplossen van problemen.
* Tijdens het publiceren van reizen worden de schaal en de stabiliteit automatisch aangepast om een maximale doorvoer en stabiliteit te garanderen. Aangezien u dichtbij de mijlpaal van 100 levende reizen in één keer, zult u een bericht over deze verwezenlijking zien verschijnen in UI. Als u deze melding ziet en uw reizen moet verlengen tot meer dan 100 rechtstreekse reizen tegelijk, maak dan een ticket voor de klantenservice en wij helpen u uw doelstellingen te bereiken.
  <!-- DOCAC-10977 * As you publish journeys, we automatically scale and adjust to ensure maximum throughput and stability. As you near the milestone of 500 live journeys at one time, you will see a notification appear in the UI on this achievement. If you see this notification and have a need to extend your journeys beyond 500 live journeys at a time, please create a ticket for customer care and we will help you reach your goals.-->
* Wanneer u een publiekskwalificatie gebruikt op een reis, kan het tot 10 minuten duren voordat de activiteit van de publiekskwalificatie actief is en naar profielen luistert die het publiek binnenkomen of verlaten.
* Een reisinstantie voor een profiel heeft een maximumgrootte van 1 MB. Alle gegevens die als onderdeel van de uitvoering van de reis worden verzameld, worden opgeslagen in die reisinstantie. Daarom gegevens van een binnenkomende gebeurtenis, profielgegevens die zijn opgehaald uit Adobe Experience Platform, aangepaste reacties op acties, enzovoort. worden opgeslagen in die reisinstantie en beïnvloeden de reisgrootte. Wanneer een reis met een evenement begint, wordt het aanbevolen de maximale omvang van die lading (bv. minder dan 800 kB) te beperken om te voorkomen dat die limiet na een paar activiteiten wordt bereikt, in de uitvoering van de reis. Wanneer deze limiet is bereikt, heeft het profiel een foutstatus en wordt het van de reis uitgesloten.
* Naast de time-out die wordt gebruikt bij reisactiviteiten, is er ook een wereldwijde reistime-out die niet in de interface wordt weergegeven en niet kan worden gewijzigd. Deze wereldwijde time-out houdt de voortgang van individuen op de reis 91 dagen na hun binnenkomst tegen. [Meer informatie](../building-journeys/journey-properties.md#global_timeout)

### Algemene acties {#general-actions-g}

De volgende gidsen zijn op de [ Acties ](../building-journeys/about-journey-activities.md) in uw reizen van toepassing:

* In het geval van een fout worden drie pogingen systematisch opnieuw uitgevoerd. U kunt het aantal pogingen niet aanpassen volgens het ontvangen foutbericht. Retries wordt uitgevoerd voor alle HTTP-fouten, behalve voor HTTP 401, 403 en 404.
* De ingebouwde **gebeurtenis van de Reactie** staat u toe om op uit-van-de-doos acties te reageren. Leer meer op [ deze pagina ](../building-journeys/reaction-events.md). Als u op een bericht wilt reageren dat via een douaneactie wordt verzonden, moet u een specifieke gebeurtenis vormen.
* U kunt geen twee acties parallel plaatsen, u moet hen één na andere toevoegen.
* Een profiel kan niet veelvoudige tijden in de zelfde reis, tezelfdertijd, voor alle actieve [ versies van de reis ](../building-journeys/publishing-the-journey.md#create-a-new-version-of-a-journey-journey-create-new-version) zijn. Als de terugkeer wordt toegelaten, kan een profiel een reis opnieuw ingaan, maar kan het niet doen tot hij dat vorige geval van de reis volledig verliet. [Meer informatie](../building-journeys/end-journey.md)

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

* Voor alle aangepaste handelingen, per host en per sandbox wordt een limiet van 300.000 aanroepen per minuut gedefinieerd. Verwijs naar [ deze pagina ](../action/about-custom-action-configuration.md). Deze grens is geplaatst gebaseerd op klantengebruik, om externe eindpunten te beschermen die door douaneacties worden gericht. U moet hiermee rekening houden bij reizen voor uw publiek door een juiste leessnelheid te definiëren (5000 profielen/s wanneer aangepaste handelingen worden gebruikt). Indien nodig, kunt u deze het plaatsen met voeten treden door een grotere het maximum van het maximum of het vertragen grens door onze Capping/het Draaien APIs te bepalen. Zie [deze pagina](../configuration/external-systems.md).
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

* Journey Optimizer ondersteunt een piekvolume van 5.000 inkomende reisevenementen per seconde.
* Het kan tot 5 minuten duren voordat de eerste actie tijdens de reis wordt uitgevoerd.
* Voor door het systeem gegenereerde gebeurtenissen moeten streaminggegevens die worden gebruikt om een klantentraject te starten, eerst binnen Journey Optimizer worden geconfigureerd om een unieke orchestratie-id te verkrijgen. Deze orkest-id moet worden toegevoegd aan de streaminglading die naar Adobe Experience Platform komt. Deze beperking geldt niet voor op regels gebaseerde gebeurtenissen.
* Zakelijke evenementen kunnen niet worden gebruikt in combinatie met monitaire evenementen of kwalificatieactiviteiten voor het publiek.
* Eenheidstrajecten (te beginnen met een evenement of een kwalificatie van het publiek) bevatten een begeleidend element dat voorkomt dat ritten bij dezelfde gebeurtenis meerdere keren ten onrechte worden gestart. De ingang van het profiel wordt tijdelijk geblokkeerd door gebrek gedurende 5 minuten. Als bijvoorbeeld een evenement om 12.01 uur een reis voor een bepaald profiel start en een ander om 12.03 uur aankomt (ongeacht of het dezelfde gebeurtenis is of een andere gebeurtenis die dezelfde reis veroorzaakt), zal die reis niet opnieuw beginnen voor dit profiel.
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

### Profiel bijwerken {#update-profile-g}

Specifieke instructies zijn van toepassing op de **[!UICONTROL Update profile]** -activiteit. Zij zijn vermeld op [ deze pagina ](../building-journeys/update-profiles.md).

### Doelgroep lezen {#read-segment-g}

De volgende gidsen zijn op [ Gelezen de reisactiviteit van het publiek ](../building-journeys/read-audience.md) van toepassing:

* Gestroomlijnde doelgroepen zijn altijd up-to-date, maar batchdoelgroepen worden niet berekend tijdens het ophalen. Ze worden alleen elke dag geëvalueerd op het tijdstip van de dagelijkse batchevaluatie.
* Voor reizen die a **gebruiken Gelezen de activiteit van het publiek**, is er een maximumaantal reizen dat precies tezelfdertijd kan beginnen. De pogingen zullen door het systeem worden uitgevoerd maar gelieve te vermijden hebbend meer dan vijf reizen (met **Gelezen Publiek**, gepland of die &quot;zo spoedig mogelijk&quot;beginnen) op het nauwkeurige zelfde ogenblik door hen over tijd, bijvoorbeeld 5 tot 10 minuten uit elkaar te spreiden.
* De **Gelezen activiteit van het publiek** kan niet met de activiteiten van Adobe Campaign worden gebruikt.
* De **Gelezen activiteit van het Publiek** kan slechts als eerste activiteit in een reis, van na een bedrijfsgebeurtenisactiviteit worden gebruikt.
* Een reis kan slechts één **Gelezen activiteit van het Publiek** hebben.
* Zie ook aanbevelingen over hoe te om **te gebruiken las de activiteit van het publiek** op [ deze pagina ](../building-journeys/read-audience.md).
* De pogingen worden toegepast door gebrek op publiek-getriggerde reizen (die met a **Gelezen Publiek** of a **BedrijfsGebeurtenis** beginnen) terwijl het terugwinnen van de uitvoerbaan. Als er een fout optreedt tijdens het maken van de exporttaak, worden de pogingen om de 10mn opnieuw uitgevoerd, tot maximaal 1 uur. Daarna zullen we het als een mislukking beschouwen. Deze soorten reizen kunnen daarom tot 1 uur na de geplande tijd worden uitgevoerd.

### Poortkwalificatie {#audience-qualif-g}

De volgende richtlijn is op de ](../building-journeys/audience-qualification-events.md) de reisactiviteit van de Kwalificatie van het publiek 0} van toepassing:[

* De kwalificatie-activiteit Publiek kan niet worden gebruikt met Adobe Campaign-activiteiten.

### Expression-editor {#expression-editor}

De volgende richtlijn is op de [ redacteur van de reisuitdrukking ](../building-journeys/expression/expressionadvanced.md) van toepassing:

* U kunt gebeurtenisveldgroepen niet gebruiken voor reizen die beginnen met een leespubliek, een kwalificatie Audience of een activiteit voor een zakelijke gebeurtenis. U moet een nieuw publiek creëren en een onpublieksvoorwaarde in de reis gebruiken.

### Activiteiten in de app {#in-app-activity-limitations}

De volgende instructies zijn van toepassing op de handeling **[!UICONTROL In-app message]** . Leer meer over in-app berichten op [ deze pagina ](../in-app/create-in-app.md).

* Deze functie is momenteel niet beschikbaar voor klanten in de gezondheidszorg.

* Personalization kan alleen profielkenmerken bevatten.

* De activiteiten in de app kunnen niet worden gebruikt met Adobe Campaign-activiteiten.

* De weergave in de app is gekoppeld aan de duur van de rit. Dit houdt in dat wanneer de reis voor een profiel afloopt, alle in-app-berichten binnen die reis niet meer worden weergegeven voor dat profiel.  Het is daarom niet mogelijk om een bericht in de app rechtstreeks te stoppen van een reisactiviteit. In plaats daarvan moet u de hele reis beëindigen om te voorkomen dat de berichten in de app naar het profiel worden weergegeven.

* In de testmodus is de weergave in de app afhankelijk van de levensduur van de rit. Als u wilt voorkomen dat de reis te vroeg eindigt tijdens het testen, past u de **[!UICONTROL Wait time]** -waarde voor uw **[!UICONTROL Wait]** -activiteiten aan.

* **[!UICONTROL Reaction]** -activiteiten kunnen niet worden gebruikt om te reageren op een geopende of geklikte In-app.

* Er kan een activeringsvertraging optreden tussen het moment dat een gebruikersprofiel een in-app-activiteit op het canvas bereikt en het moment waarop het bericht in de app wordt weergegeven.

* De inhoud van berichten in de app is beperkt tot 2 MB. Het opnemen van grote afbeeldingen kan het publicatieproces belemmeren.

### Snelheid {#jump-g}

Specifieke instructies zijn van toepassing op de **[!UICONTROL Jump]** -activiteit. Zij zijn vermeld op [ deze pagina ](../building-journeys/jump.md#jump-limitations).

### Campagne {#ac-g}

De volgende instructies zijn van toepassing op de activiteiten **[!UICONTROL Campaign v7/v8]** en **[!UICONTROL Campaign Standard]** :

* Adobe Campaign-activiteiten kunnen niet worden gebruikt met een Read-publiek of met een Audience-kwalificatieactiviteit.
* Campagne-activiteiten kunnen niet worden gebruikt met andere kanaalactiviteiten: kaart, ervaring op basis van code, e-mail, push, SMS, In-app berichten, Web.
