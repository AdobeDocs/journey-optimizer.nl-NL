---
solution: Journey Optimizer
product: journey optimizer
title: Referentie foutcodes
description: Meer informatie over algemene foutcodes in Adobe Journey Optimizer en hoe u deze kunt oplossen
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: fout, codes, problemen oplossen, reis, campagne, berichten
source-git-commit: 28a8f113d594f80ba7de22229e9a223b7f17ae8d
workflow-type: tm+mt
source-wordcount: '2394'
ht-degree: 0%

---


# Referentie foutcodes {#error-codes}

Adobe Journey Optimizer gebruikt gestandaardiseerde foutcodes om u te helpen problemen tijdens reizen, campagnes en berichtconfiguraties snel te identificeren en op te lossen. Door deze foutcodes te begrijpen, kunt u de tijd voor het oplossen van problemen aanzienlijk verkorten en optimale campagneprestaties behouden.

## Werken met foutcodestructuur {#error-code-structure}

Adobe Journey Optimizer-foutcodes volgen een consistent naamgevingspatroon waarmee u gemakkelijker het type component en uitgave kunt identificeren:

* **Prefix van de Dienst**: Wijst op welke dienst van Adobe Journey Optimizer de fout (b.v., CJMPTS voor de Dienst van het Push/Vervoer, CJMRT voor Runtime van de Reis, CJMMAS voor de Dienst van de Authoring van het Bericht, CJMCMP voor Campagne, CJMTL voor de Laag van het Vervoer, CJMRPS voor de Dienst van de Rapportering/van de Levering) productie produceerde
* **aantal van de Fout**: Unieke herkenningsteken voor de specifieke foutenvoorwaarde
* **de statuscode van HTTP**: Standaard HTTP- statuscode (b.v., 400, 403, 422, 500)

Voorbeeld: `CJMRT-030012-422` geeft een CJMRT-fout (Journey Runtime Error) aan met foutnummer 030012 en HTTP-status 422 (Unprocessable Entiteit).

## Waar kan ik foutcodes vinden? {#find-error-codes}

Foutcodes verschijnen op verschillende locaties in Adobe Journey Optimizer:

* Uitvoeringsverslagen en logboeken voor reizen
* Campagneactiveringsschermen
* Waarschuwingen voor validatie van berichten
* Systeemmeldingen en -waarschuwingen
* API-reacties (bij gebruik van REST API&#39;s)

Wanneer een fout voorkomt, neem nota van de volledige foutencode en om het even welke begeleidende verzoek identiteitskaart, aangezien deze voor het oplossen van problemen en steunescalatie essentieel zijn.

## Algemene foutcodes per service {#error-codes-by-service}

### CJMPTS: Push- en Transport Service-fouten {#cjmpts-errors}

Deze fouten komen tijdens de levering van het dupbericht en de verrichtingen van het berichtvervoer voor.

| Foutcode | Beschrijving | Hoofdoorzaak | Resolutie |
|------------|-------------|-----------|-----------|
| **CJMPTS-1410-500** | Interne serverfout bij verzenden van push/kanaal | Kanaalbackendout, verlopen geloofsbrieven, misconfiguration of leveranciershandeling | &#x200B;1. Opnieuw na vertraging <br/> 2. De leveranciersconfiguraties en quota van de controle <br/> 3. Verifieer dupgeloofsbrieven geldig <br/> 4 zijn. Test met een afwisselend kanaal <br/> 5. Als blijvend, contacteer de Steun van Adobe met verzoekidentiteitskaart <br/><br/>**Verwante documentatie**: [ Push configuratie ](../push/push-configuration.md) |
| **CJMPTS-1006-404** | Push/SMS mislukt met &quot;resource niet gevonden&quot; | De leverancier/het kanaal waarnaar wordt verwezen, bestaat niet, is verkeerd gespeld of is gedeprovisioned | &#x200B;1. Het overzicht en corrigeert leverancier/kanaalverwijzingen en IDs <br/> 2. De zandbak/organisatieconfiguratie van de controle <br/> 3. Verifieer kanaalconfiguraties actief <br/> 4 zijn. Creeer zo nodig kanaalconfiguratie opnieuw <br/><br/>**Verwante documentatie**: [ oppervlakken van het Kanaal ](../configuration/channel-surfaces.md) |
| **CJMPTS-1510-500** | Interne serverfout bij verzenden van pushkanaal | Uitval van back-end-push/transport; fout van provider of infrastructuur | &#x200B;1. De montages van de kanaallevering van de controle <br/> 2. Verifieer dupgeloofsbrieven geldig <br/>  zijn. Opnieuw verrichting <br/> 4. Als blijvend, contacteer de Steun van Adobe met verzoekidentiteitskaart <br/><br/>**Verwante documentatie**: [ Push configuratie ](../push/push-configuration.md) |
| **CJMPTS-1023-500** | Interne serverfout tijdens push-verzendproces (gateways van derden) | Tijdelijke fout in wolk of onbekende servicefout | &#x200B;1. Verifieer leverancier/kanaalconfiguratie <br/> 2. De status van de derdegateway van de controle <br/> 3. Opnieuw proberen na een paar notulen <br/> 4. De logboeken van het overzicht voor extra context <br/><br/>**Verwante documentatie**: [ duw berichten ](../push/create-push.md) |
| **CJMPTS-1310-500** | Interne fout van Render Service (voorvertoning of live verzending) | Downstreamsjabloonrenderer is mislukt, meestal vanwege JSON-/sjabloonsyntaxisproblemen | &#x200B;1. Valideer malplaatjesyntaxis en structuur <br/> 2. Controle alle verpersoonlijkingsvariabelen zijn geldig <br/> 3. Gebruik een testlading om de kwestie <br/> 4 te identificeren. Vereenvoudig malplaatjeingewikkeldheid indien nodig <br/><br/>**Verwante documentatie**: [ malplaatjes van het Bericht ](../content-management/content-templates.md), [ syntaxis van Personalization ](../personalization/personalization-syntax.md) |

### CJMRT: Fouten met betrekking tot reistijd en API {#cjmrt-errors}

Deze fouten treden op tijdens de uitvoering van de reis, gebeurtenisverwerking en API-bewerkingen.

| Foutcode | Beschrijving | Hoofdoorzaak | Resolutie |
|------------|-------------|-----------|-----------|
| **CJMRT-110001-500** | Maximum aantal uitvoeringen overschreden voor workflowstap (bijv. time-out voor IP-affiniteitsprovisioning) | Workflow/provisioning-taak is niet voltooid binnen toegestane pogingen/tijd, vaak als gevolg van vertragingen in de infrastructuur/service of tijdelijke back-endproblemen | &#x200B;1. Opnieuw na wat tijd <br/> 2. De Status van Adobe van de controle [ voor stroomonderbrekingen ](https://status.adobe.com/) 3. <br/> Escaleren aan de Steun van Adobe met werkschema/baan/org details <br/> 4. Verstrek logboeken en het netwerk vangen als beschikbaar <br/><br/>**Verwante documentatie**: [ het oplossen van problemen van de Reis ](troubleshooting.md) |
| **CJMRT-000071-400** | Onjuiste aanvraag tijdens reis-/testgebeurtenis of API-aanroep | Payload/parameters zijn onjuist geformuleerd of ontbreken; invoerverwijzingen verwijzen naar een niet-bestaande of niet-actieve bron | &#x200B;1. Herzie het verzoeklichaam voor foutendetails <br/> 2. Correcte verwijzing/parameter <br/> . Verwijder geavanceerde configuratie en probeer opnieuw <br/> 4. Voeg eigenschappen achter één voor één toe om de kwestie <br/><br/>**Verwante documentatie** te identificeren: [ het oplossen van problemen van de Reis ](troubleshooting.md), [ configuratie van Gebeurtenissen ](../event/about-events.md) |
| **CJMRT-000013-401** | Ongeoorloofde fout tijdens bewerking van berichtruntime/API-gebeurtenis | Verificatiefout: token is verlopen, machtigingen ontbreken of de integratie/gebruiker heeft omgevingstoegang verloren | &#x200B;1. Verifieer toestemmingen en rollen <br/> 2. Vernieuw authentificatietoken <br/> 3. Gebruik een bekende-geldige gebruiker/de dienstrekening <br/> 4. De taken van het productprofiel van het overzicht <br/><br/>**Verwante documentatie**: [ Toestemmingen ](../administration/permissions.md) |
| **CJMRT-080605-400** | Onjuiste aanvraag tijdens de uitvoering van de reis (bijvoorbeeld activering van knooppunt, handeling, enz.) | Configuratie verwijst naar een verwijderde/hernoemde of verouderde functie/sjabloon/kanaal | &#x200B;1. Valideer alle middelverwijzingen <br/> 2. De configuratie van de de reis van de controle en eigenschapvlaggen <br/> 3. Werk gebroken verwijzingen <br/> 4 bij. Herzie recente systeemupdates en migraties <br/><br/>**Verwante documentatie**: [ de verwezenlijking van de Reis ](journey-gs.md) |
| **CJMRT-030012-422** | Niet-verwerkbare entiteit - mislukte actie, ongeldige gebeurtenis of onjuiste lading | Ongeldige invoergegevens (bijvoorbeeld niet-bestaand publiek, gebeurtenis of kenmerk) | &#x200B;1. De structuur van de input/gebeurtenislading van de dubbel-controle <br/> 2. Verifieer de referenced voorwerpen (publiek, datasets) bestaan en zijn actief <br/> . Bevestig alle vereiste gebieden aanwezig zijn <br/> 4. Test met een bekende - goede nuttige lading <br/><br/>**Verwante documentatie**: [ het oplossen van problemen van de Reis ](troubleshooting.md), [ configuratie van Gebeurtenissen ](../event/about-events.md) |
| **CJMRT-130004-400** | Onjuist verzoek - misvormde input in reisknoop of kanaalconfig | Reislading of configuratieverwijzingen verwijderd/ongeldige bron | &#x200B;1. De configuratie van de de vervoerknoop van het overzicht <br/> 2. Verifieer alle referenced middelen (berichten, publiek, acties) bestaan <br/> 3. Repareer of werk gebroken verwijzingen <br/> 4 bij. Rebuild de configuratie van de reis indien nodig <br/><br/>**Verwante documentatie**: [ de verwezenlijking van de Reis ](journey-gs.md), [ de acties van de Douane ](../action/about-custom-action-configuration.md) |
| **CJMRT-000032-409** | Conflict - bron bestaat al | Poging om bron te maken met dubbele id of naam | &#x200B;1. Gebruik unieke IDs en namen voor alle middelen <br/> 2. Controle voor bestaande middelen met zelfde herkenningsteken <br/> 3. Schrap of noem het in conflict brengen voorwerpen <br/> 4 anders. Het overzicht noemend overeenkomsten <br/><br/>**Verwante documentatie**: [ versies van de Reis ](journey-gs.md#journey-versions) |
| **CJMRT-170016-400** | Beschadigd verzoek tijdens het configureren/voorvertonen van de verbinding | Vereiste afhankelijkheid of verbroken sjabloonkoppeling bij Payload ontbreekt | &#x200B;1. Bevestig alle vereiste middelen actief <br/>  zijn. Verzeker malplaatjes en inhoudsblokken worden gepubliceerd <br/> . Controle alle gebiedsdelen zijn behoorlijk verbonden <br/> 4. De resultaten van de de proefwijze van het overzicht <br/><br/>**Verwante documentatie**: [ Testende reizen ](testing-the-journey.md), [ de gebiedsdelen van de Reis ](journey-gs.md) |
| **CJMRT-080608-400** | Onjuist verzoek in domein/kanaal/delegatie | Vereiste DNS-records of e-mail/SMS-configuratie ontbreken | &#x200B;1. Volledige DNS configuratie voor e-maildomeinen <br/> 2. Verifieer subdomain delegatie volledig <br/> 3 is. De configuratietovenaars van de looppas opnieuw <br/> 4. Toestaan tijd voor DNS propagatie (tot 72 uren) <br/><br/>**Verwante documentatie**: [ oppervlakken van het Kanaal ](../configuration/channel-surfaces.md), [ Subdomain delegatie ](../configuration/delegate-subdomain.md) |
| **CJMRT-110100-500** | Interne fout bij laden | Fout in back-endgegevens/config of niet-ondersteunde configuratie | &#x200B;1. Opnieuw verrichting <br/> . Vereenvoudig configuratie als het gebruiken van geavanceerde eigenschappen <br/> 3. Escaleren aan de Steun van Adobe met verzoek identiteitskaart en nauwkeurige lading <br/> 4. Controle voor bekende kwesties in versienota&#39;s <br/><br/>**Verwante documentatie**: [ het oplossen van problemen van de Reis ](troubleshooting.md) |

### CJMMAS: fouten in de Message Authoring Service {#cjmmas-errors}

Deze fouten treden op wanneer u berichten, voorinstellingen en inhoud maakt, bewerkt of publiceert.

| Foutcode | Beschrijving | Hoofdoorzaak | Resolutie |
|------------|-------------|-----------|-----------|
| **CJMMAS-1732-500** | Bewijs is mislukt - Alle elementen worden niet gepubliceerd tijdens het verzenden van een proefdruk/test met AEM-middelen | Onlangs gepubliceerd element bevindt zich nog niet in AJO; ID van element komt niet overeen; gebruik van kruisrepo&#39;s; synchronisatiemarkering van AEM | &#x200B;1. Gebruik slechts gepubliceerde activa IDs van de correcte bewaarplaats/het milieu <br/> 2. Toestaan tijd voor synchronisatie tussen AEM en AJO <br/> 3. Opnieuw proberen met een bekend-goede activa <br/> 4. Verifieer activa het publiceren status in AEM <br/><br/>**Verwante documentatie**: [ integratie van Assets ](../integrations/assets.md) |
| **CJMMAS-1069-500** | Interne foutsjabloon opslaan of publiceren | Backend-uitzondering (infrastructuur/service bug of inhoudsprobleem); niet-ondersteunde opmaak/functie | &#x200B;1. Vereenvoudig of verminder de malplaatjeingewikkeldheid <br/> 2. Voeg inhoud in stijgende stappen opnieuw toe om de kwestie <br/>  te identificeren. Controleer de [ pagina van de Status van Adobe ](https://status.adobe.com/) <br/> 4. Verwijder niet gesteunde eigenschappen of prijsverhoging <br/><br/>**Verwante documentatie**: [ malplaatjes van de Inhoud ](../content-management/content-templates.md) |
| **CJMMAS-1149-400** | Onjuist verzoek bij opslaan van bericht, voorinstelling of variant | Vereiste velden ontbreken in bericht of slechte configuratie | &#x200B;1. Voltooi alle vereiste gebieden (duidelijk met asterisk) <br/> 2. Valideer bericht/vooraf ingestelde configuratie <br/> 3. De formaten en beperkingen van de het gebiedswaarde van de controle <br/> 4. De bevestigingsberichten van het overzicht in UI <br/><br/>**Verwante documentatie**: [ E-mailkanaal ](../email/get-started-email.md), [ oppervlakken van het Kanaal ](../configuration/channel-surfaces.md) |
| **CJMMAS-2073-422** | Niet-verwerkbare entiteit in bewerking van berichtvoorinstelling | Validatiefout, niet-ondersteund veld of onjuiste syntaxis | &#x200B;1. Corrigeer syntaxis/gebiedsfouten zoals vermeld <br/> 2. Ben met een bekende-goede configuratie <br/> 3 vergelijkbaar. De bevestiging van het bericht van het gebruik UI alvorens <br/> 4 te bewaren. De gebiedsvereisten van het overzicht in documentatie <br/><br/>**Verwante documentatie**: [ Voorinstellingen van het Bericht ](../configuration/channel-surfaces.md), [ e-mailmontages ](../email/email-settings.md) |
| **CJMMAS-1300-500** | Interne fout tijdens maken van bericht | Backend loopt vast vanwege een probleem met de infrastructuur, grote inhoud of downtime van services | &#x200B;1. Vereenvoudig malplaatje/inhoud (verminder grootte/ingewikkeldheid) <br/> 2. Opnieuw verrichting <br/> 3. Sparen het werk incrementeel <br/> 4. Als blijvend, escaleer aan de Steun van Adobe <br/><br/>**Verwante documentatie**: [ malplaatjes van de Inhoud ](../content-management/content-templates.md) |
| **CJMMAS-2001-200** | Status geslaagd, maar foutbanner: koppeling om te weigeren ontbreekt | Koppeling voor afmelden ontbreekt in e-mailvariant | &#x200B;1. Voeg opt-out/unsubscribe verbinding aan alle e-mailvarianten <br/> 2 toe. Verzeker verbinding in elke taalversie <br/> 3 aanwezig is. De hulp van de verpersoonlijking van het gebruik om opt-out verbinding <br/> 4 op te nemen. Test alle varianten alvorens <br/><br/>**Verwante documentatie** te publiceren: [ Opt-out beheer ](../privacy/opt-out.md), [ E-mailontwerp ](../email/content-from-scratch.md) |
| **CJMMAS-1603-403** | Verboden bij bijwerken/publiceren van sjabloon of voorinstelling | Gebruiker heeft geen vereiste machtiging/rol of is in de huidige staat geen handeling toegestaan | &#x200B;1. Controleer of de gebruiker de juiste machtigingen heeft (Berichtbeheer, Auteur, enz.)<br/> 2. De controle vooraf ingesteld/malplaatjestatus (ontwerp, gepubliceerd, gearchiveerd) <br/> . De toegang van het verzoek van beheerder indien nodig <br/> 4. De taken van het productprofiel van het overzicht <br/><br/>**Verwante documentatie**: [ Toestemmingen ](../administration/permissions.md), [ controle van de Toegang ](../administration/permissions-overview.md) |

### CJMCMP: Campagnefouten {#cjmcmp-errors}

Deze fouten komen tijdens campagneverwezenlijking, configuratie, en activering voor.

| Foutcode | Beschrijving | Hoofdoorzaak | Resolutie |
|------------|-------------|-----------|-----------|
| **CJMCMP-6003-400** | &quot;Er is ten minste één onjuiste campagne&quot; bij het publiceren/testen van reis/bericht in de testmodus | Knooppunt verwijst naar een ontbrekende, niet-gepubliceerde of ongeldige campagne; verouderde of gekloonde reis maakt geen inline | &#x200B;1. Open elke berichtknoop en verifieer configuratie <br/> 2. Verbind opnieuw of voeg berichtknopen <br/>  toe. Activeer testwijze om verwezenlijking van gealigneerde campagnes <br/> 4 te dwingen. Beweging aan de nieuwe reistovenaar als de kwestie vaak <br/><br/>**Verwante documentatie** is: [ de verwezenlijking van de Reis ](journey-gs.md), [ Testende reizen ](testing-the-journey.md) |
| **CJMCMP-2003-400** | UI-banner: &quot;Het experiment is onjuist&quot; in e-mail Designer | Stale of ontbrekende experiment/gegevensleverancier; mislukte experimenteeropschoning, schemawanverhouding of fout in gebruikersinterfacevalidatie | &#x200B;1. Verwijder ongebruikte proefdiervelden <br/> 2. Bevestig schema en gegevensleveranciersverbindingen <br/> 3. Herlaad UI en ontruim browser geheim voorgeheugen <br/> 4. Creeer knoop/e-mail als het probleem niet opgelost <br/><br/>**Verwante documentatie**: [ experimenten van de Inhoud ](../content-management/content-experiment.md) |
| **CJMCMP-3001-400** | Simulatie/voorvertoning &quot;onjuist filter voor vlaktekst&quot; | Knooppunt dat is gemaakt met een oudere structuur verzendt type=surfaceId, backend verwacht brandingPresetId | &#x200B;1. Schrap en ontspruit de beïnvloede knoop <br/> 2. Gebruik de nieuwe reisversie/malplaatje <br/> 3. De testwijze van het gebruik om configuratie <br/> 4 te ontruimen. Het bulk ontspant knopen als de kwestie wijdverspreid <br/><br/>**Verwante documentatie** is: [ oppervlakken van het Kanaal ](../configuration/channel-surfaces.md), [ simulatie van het Bericht ](../content-management/preview.md) |
| **CJMCMP-2050-400** | Onjuist verzoek bij activering of goedkeuring van campagne | Campagneverwijzingen ongeldig/ontbrekend beleid of segment | &#x200B;1. Controle alle configuraties van de campagneknoop <br/> 2. Verifieer beleid/segmentverbindingen huidig en geldig <br/>  zijn. Update met correcte configuratie <br/> 4. Hertest campagne vóór activering <br/><br/>**Verwante documentatie**: [ de verwezenlijking van de Campagne ](../campaigns/create-campaign.md), [ goedkeuring van de Campagne ](../test-approve/gs-approval.md) |

### CJMTL: fouten in transportlagen {#cjmtl-errors}

Deze fouten komen tijdens berichtvervoer en leveringsverrichtingen voor.

| Foutcode | Beschrijving | Hoofdoorzaak | Resolutie |
|------------|-------------|-----------|-----------|
| **CJMTL-010018-422** | &quot;Personalization niet toegestaan in domeinnaam&quot; bij het opslaan/verzenden van inhoud | Te strikte validatie heeft tijdelijk dynamische personalisatie van href-domein verbroken | &#x200B;1. De verbindingen van de factor als het gebruiken van domeinvariabelen <br/> . Verifieer de recentste versie van AJO in gebruik <br/>  is. Opnieuw verrichting <br/> 4. Het gebruik statische domeinen als de kwestie <br/><br/>**Verwante documentatie** voortduurt: [ de syntaxis van Personalization ](../personalization/personalization-syntax.md), [ E-mailontwerp ](../email/content-from-scratch.md) |
| **CJMTL-01001-422** | Onbewerkbare entiteit - Push/SMS/Email send mislukt, zegt &quot;invalid field&quot; | Payload of ontvanger/contactgegevens ontbreken of zijn ongeldig | &#x200B;1. Inspect logboeken voor specifieke gebiedsfouten <br/> . Profiel/contactinformatie van de moeilijke situatie <br/> . Valideer met testprofiel <br/> 4. Het ladingsformaat van de reactor zoals nodig <br/><br/>**Verwante documentatie**: [ het beheer van het Profiel ](../audience/get-started-profiles.md), [ de profielen van de Test ](../audience/creating-test-profiles.md) |

### CJMRPS: fouten in de rapportage- en leveringsservice {#cjmrps-errors}

Deze fouten komen tijdens het melden van configuratie en dataset leveringsverrichtingen voor.

| Foutcode | Beschrijving | Hoofdoorzaak | Resolutie |
|------------|-------------|-----------|-----------|
| **CJMRPS-1047-409** | &quot;Conflict. Dataset is al toegevoegd&quot; bij het toevoegen van de rapportgegevensset | Poging om een dataset toe te voegen die reeds provisioned is | &#x200B;1. De configuratie van de dataset van het overzicht in het melden van montages <br/> 2. Plaats datasets reeds aanwezig <br/> 3 niet opnieuw. De officiële migratiecontrolelijsten van het gebruik voor het melden van migratie <br/> 4. Verwijder dubbele datasetverwijzingen <br/><br/>**Verwante documentatie**: [ Meldend overzicht ](../reports/gs-reports.md), [ de rapporten van de Campagne ](../reports/campaign-global-report-cja.md), [ de rapporten van de Reis ](../reports/journey-global-report-cja.md) |

## Algemene benadering voor probleemoplossing {#troubleshooting-approach}

Volg deze systematische aanpak bij het tegenkomen van een foutcode:

1. **identificeer de fout**: Noteer de volledige foutencode, de status van HTTP, en om het even welk begeleidend bericht of verzoek identiteitskaart

2. **vind de dienst**: Gebruik de de dienstprefix (CJMPTS, CJMRT, CJMMAS, CJMCMP, CJMTL, CJMRPS) om te identificeren welke component wordt beïnvloed.

3. **Controle de statuscode**:
   * **400 (Onjuist Verzoek)**: De gegevens en de configuratie van de inputinput van het overzicht
   * **403 (Verboden)**: De toestemmingen van de controle en toegangsrechten
   * **409 (Conflict)**: Zoek dubbele of conflicterende middelen
   * **422 (Niet verwerkbare Entiteit)**: Valideer gegevens tegen schemavereisten
   * **500 (Interne Fout van de Server)**: Opnieuw en potentieel escaleer om te steunen

4. **recente veranderingen van het Overzicht**: Overweeg wat onlangs (reisupdates, nieuwe campagnes, configuratieveranderingen, enz.) werd gewijzigd.

5. **raadpleeg documentatie**: Gebruik de verbindingen die in deze gids worden verstrekt om tot gedetailleerde documentatie voor de beïnvloede eigenschap toegang te hebben.

6. **probeert opnieuw wanneer aangewezen**: Voor 500 reeksfouten, lost eenvoudig opnieuw na een paar notulen vaak voorbijgaande kwesties op.

7. **Escaleren wanneer nodig**: Als de fout na volgende resolutiestappen voortduurt, contacteer de Steun van Adobe met:
   * Volledige foutcode
   * Verzoek-id (indien beschikbaar)
   * Stappen om te reproduceren
   * Relevante configuratiedetails

## Tips en trucs om veelvoorkomende fouten te voorkomen {#best-practices}

### Voor de activering van de reis {#journey-best-practices}

* **bevestigt alle middelen**: Verzeker alle referenced publiek, gebeurtenissen, gegevensbronnen, en douaneacties behoorlijk worden gevormd
* **Test grondig**: De testwijze van het gebruik om kwesties te identificeren alvorens te publiceren ([ leer meer ](testing-the-journey.md))
* **bevestigt volumes**: Gebruik droge looppas om publieksbereik en taklogica te bevestigen alvorens te gaan leven ([ leer meer ](journey-dry-run.md))
* **de toestemmingen van de Controle**: Verifieer u noodzakelijke toegangsrechten voor alle componenten hebt
* **gebiedsdelen van het Overzicht**: Zorg ervoor alle verbonden berichten en inhoud worden gepubliceerd

### Berichten maken {#message-best-practices}

* **Volledige vereiste gebieden**: Vul altijd alle verplichte gebieden alvorens op te slaan
* **omvat opt-out verbindingen**: Voeg unsubscribe verbindingen aan alle e-mailvarianten toe ([ leer meer ](../privacy/opt-out.md))
* **bevestigt verpersoonlijking**: Test alle dynamische inhoud met steekproefprofielen ([ Leer meer ](../personalization/personalization-build-expressions.md))
* **Behoud malplaatjes handelbaar**: Vermijd te complexe malplaatjes die het teruggeven kwesties kunnen veroorzaken

### Voor campagnebeheer {#campaign-best-practices}

* **verifieer publieksgegevens**: Zorg doelpubliek behoorlijk wordt gevormd en bevolkt
* **de goedkeuringsstatus van de Controle**: Begrijp goedkeuringsvereisten alvorens te proberen te activeren ([ leer meer ](../test-approve/gs-approval.md))
* **de configuraties van de Monitor**: Regelmatig de oppervlakten van het overzichtskanaal en stelt voor geldigheid vooraf in
* **DNS van het Plan verandert**: Toestaan voldoende tijd voor DNS propagatie wanneer het bijwerken van domeinen

## Aanvullende bronnen {#additional-resources}

* [Reisproblemen oplossen](troubleshooting.md)
* [Problemen met uitvoering oplossen](troubleshooting-execution.md)
* [Problemen met binnenkomende activiteiten oplossen](troubleshooting-inbound.md)
* [Aangepaste acties oplossen](../action/troubleshoot-custom-action.md)
* [Veelgestelde vragen over reizen](journey-faq.md)
* [Afvoerkanalen en beperkingen](../start/guardrails.md)

## Ondersteuning {#getting-support}

Als u blijvende fouten tegenkomt die niet kunnen worden opgelost met behulp van deze handleiding:

1. **verzamel informatie**: Verzamel de foutencode, verzoek identiteitskaart, timestamps, en stappen om te reproduceren
2. **het systeemstatus van de Controle**: Bezoek [ Status van Adobe ](https://status.adobe.com/){target="_blank"} voor bekende de dienstkwesties
3. **documentatie van het Onderzoek**: Het overzicht [ Liga van de Ervaring van Adobe ](https://experienceleague.adobe.com/docs/journey-optimizer.html){target="_blank"} voor oplossingen
4. **gemeenschap van de Mogenschap**: De vragen van het post in de [ Gemeenschap van Adobe Journey Optimizer ](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}
5. **Steun van Adobe van het Contact**: leg een steunkaartje met alle relevante details voor

>[!NOTE]
>
>Deze foutcodeverwijzing wordt voortdurend bijgewerkt naarmate nieuwe codes worden geïdentificeerd en gedocumenteerd. Voor de huidigste informatie, controleer regelmatig de [ Communautaire blogs van Adobe Journey Optimizer ](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/bg-p/journey-optimizer-blogs){target="_blank"}.

**Verwante onderwerpen**

* [ demystifying Adobe Journey Optimizer Error Codes: Deel 1 ](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884){target="_blank"}
* [ demystifying Adobe Journey Optimizer Error Codes: Deel 2 ](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/bc-p/782661){target="_blank"}

