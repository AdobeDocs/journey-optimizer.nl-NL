---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer-artikelen voor probleemoplossing
description: Journey Optimizer-artikelen voor probleemoplossing
feature: Get Started
role: User
level: Intermediate
exl-id: f8acb987-5c6e-4545-93b9-fdfc0d74db57
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '2748'
ht-degree: 0%

---

# Problemen met artikelen oplossen {#ajo-troubleshooting}

Hieronder volgt een lijst met artikelen voor het oplossen van problemen voor Adobe Journey Optimizer. Elke het oplossen van problemensectie verstrekt antwoorden aan vaak gestelde vragen en oplossingen aan problemen.

Zie ook de [ Veelgestelde vragen van Adobe Experience Platform en de documentatie van het Oplossen van problemen ](https://experienceleague.adobe.com/en/docs/experience-platform/landing/troubleshooting){target="_blank"}.

## Email channel {#ajo-troubleshooting-email}

+++ Hoe kan ik voorkomen dat er in Adobe Journey Optimizer problemen met e-mailopmaak optreden met thema&#39;s?

In Adobe Journey Optimizer (AJO) kan het wijzigen van de standaard CSS-blokken in de e-mailkoptekst leiden tot onverwachte opmaakproblemen, vooral na het verwijderen van inhoudsfragmenten. Deze problemen zijn merkbaarder op mobiele apparaten en kunnen leiden tot layoutverschuivingen of opmaakinconsistenties. Om dit te voorkomen, gebruikt u de functie Thema&#39;s om aangepaste CSS veilig toe te passen zonder door het systeem gegenereerde CSS-stijlen te wijzigen.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"} om te leren hoe te om deze kwestie op te lossen.

Leer meer over e-mail het formatteren [ op deze pagina ](../email/get-started-email-design.md).

+++


+++ Waarom werken fragmenten met bewerkbare velden niet?

In Adobe Journey Optimizer worden fragmenten met bewerkbare velden mogelijk niet correct geladen of onverwacht gedupliceerd wanneer ze aan sjablonen worden toegevoegd. Het probleem heeft doorgaans invloed op specifieke fragmenten in verschillende omgevingen.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"} om te leren hoe te om deze kwestie op te lossen.

Leer meer over klantgerichte fragmenten [ op deze pagina ](../content-management/customizable-fragments.md).

+++

+++ Waarom worden HTML-fragmenten niet correct weergegeven in e-mails?

De fragmenten van HTML kunnen er niet in slagen behoorlijk in e-mails terug te geven, die vaak als **fragment IDs** eerder dan daadwerkelijke inhoud verschijnen. In tegenstelling tot visuele fragmenten, vereisen de fragmenten van HTML zorgvuldige configuratie. Om dit op te lossen, volg beste praktijken voor het gebruiken van zowel **visuele als de uitdrukkingsfragmenten van HTML** in uw e-mailcampagnes.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-25441){target="_blank"} om te leren hoe te om deze kwestie op te lossen.

Leer meer over de fragmenten van HTML [ op deze pagina ](../content-management/fragments.md).

+++

+++ Waarom verdwijnen e-mailsjablonen en inhoud van ongepubliceerde reizen?

Wanneer u e-mailsjablonen bewerkt in een niet-gepubliceerde reis, kunnen de inhoud en sjablonen van bepaalde e-mails onverwachts verdwijnen. Dit kan tot nieuwe werk en vertragingen leiden. Om het risico van deze kwestie te verminderen, vermijd gelijktijdige uitgeeft, beperk het aantal open lusjes, en sla regelmatig veranderingen op.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} om te leren hoe te om deze kwestie op te lossen.

Leer meer over malplaatjes [ op deze pagina ](../email/use-email-templates.md).

+++

+++ Waarom wordt het veld E-mailvoorheader niet weergegeven in de modus &#39;Uw eigen code&#39;? 

In **&quot;Code uw eigen&quot;** wijze onder de **uitgeef E-mailHoofdtekst** eigenschap, verschijnt het gebied van de Preheaderinput niet. Om preheader tekst te omvatten, moeten de gebruikers **manueel preheader** binnen hun inhoud van douaneHTML coderen.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26174){target="_blank"} om te leren hoe te om deze kwestie op te lossen.

Leer meer over E-mail preheader configuratie [ op deze pagina ](../email/header-parameters.md).

+++

+++ Waarom is er een discrepantie in koppelingsgedrag wanneer het gebruiken van een component van HTML in e-mailmalplaatjes?  

Wanneer het toevoegen van een **component van HTML** aan een e-mailmalplaatje, kunnen de verbindingen zich verschillend afhankelijk van de **e-mailcliënt** gedragen, **het bekijken wijze**, of **apparaat/browser**. Bijvoorbeeld, kunnen de ankerverbindingen verschillend in **Vooruitzichten zij aan zij mening** in vergelijking met het volledig-schermmening functioneren. Houd rekening met deze variaties wanneer u e-mailsjablonen ontwerpt en test op meerdere clients en apparaten.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26221){target="_blank"} om te leren hoe te om deze kwestie op te lossen.

Zie ook het ontwerp beste praktijken van e-mail [ op deze pagina ](../email/get-started-email-design.md).

+++


+++ Hoe te om ontbrekende verbindingen van het e-mailvolgen in rapportering te verhinderen?

Het bijhouden van koppelingen ontbreekt in Adobe Journey Optimizer wanneer e-mailURL&#39;s dynamische variabelen gebruiken en niet beginnen met http, of wanneer logische instructies in het URL-veld worden geplaatst. U lost dit probleem op door ervoor te zorgen dat alle URL&#39;s beginnen met http, geen logica te gebruiken in het URL-veld en complexe personalisatielogica te verplaatsen naar de HTML-inhoud of vooraf verwerkte kenmerken.


Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"} om te leren hoe te om deze kwestie op te lossen.

Leer meer over e-mail het volgen [ op deze pagina ](../email/message-tracking.md).

+++

+++ Hoe los ik een fout van de Uitwisseling van de Post wanneer het opzetten van API-teweeggebrachte transactie-e-mailcampagnes op? 

Als u een fout van de Uitwisseling van de Post (MX) terwijl het creëren van een kanaalconfiguratie voor een API-teweeggebrachte transactie e-mailcampagne in Adobe Journey Optimizer ontmoet, kan het aan **DNS misconfiguraties** of **het beleidsbeperkingen van DMARC** toe te schrijven zijn. Om dit op te lossen, zorg ervoor dat uw DNS correct wordt gevormd en verifieer dat uw domein met **op domein-gebaseerde Authentificatie van het Bericht, het Melden, en Conformance (DMARC)** vereisten voldoet.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26200){target="_blank"} om te leren hoe te om deze kwestie op te lossen.

Leer meer over e-mailDMARC beleid [ op deze pagina ](../configuration/dmarc-record-update.md).

Zie ook [ API-teweeggebrachte campagnedocumentatie ](../campaigns/api-triggered-campaigns.md).
+++

## Push-kanaal {#ajo-troubleshooting-push}

+++ Kan een profiel meerdere pushtokens hebben in Adobe Journey Optimizer?

Bij het implementeren van pushberichten in Journey Optimizer kan één profiel meerdere pushtokens hebben die zijn gekoppeld aan verschillende apparaten. Tijdens een pushmeldingscampagne is Journey Optimizer ontworpen om deze tokens te beheren en ervoor te zorgen dat het doelprofiel op alle gekoppelde apparaten kan worden bereikt.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} om meer over het beheer van het duptoken te leren.

Leer meer over dupconfiguratie [ op deze pagina ](../push/push-configuration.md).

+++

+++ Waarom leidt het klikken op een duwbericht me niet aan gevormd Web URL om?  

Als de pushberichten niet worden omgeleid naar de bedoelde web-URL, kan dit worden veroorzaakt door een onjuiste configuratie voor klikken op handeling of door uitgeschakelde instellingen voor pushmeldingen. Zorg ervoor dat de **klikactie** voor het duw bericht correct wordt geplaatst en dat **automatische vertoning en het volgen** van duw berichten worden toegelaten om deze kwestie op te lossen.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26226){target="_blank"} om meer over deze kwestie te leren.

Leer meer over dupconfiguratie [ op deze pagina ](../push/push-configuration.md).

+++


## SMS-kanaal {#ajo-troubleshooting-sms}

+++ Waarom wordt mijn transactie-SMS niet geleverd, ook al is de toestemming ingesteld op `marketing.sms.value=y` ?

Als een ontvanger **STOP** aan SMS antwoordt, worden alle toekomstige berichten van dat korte aantal geblokkeerd — met inbegrip van transactionele berichten. Om ononderbroken levering van transactieSMS te waarborgen, vorm en verzend hen door a **afzonderlijk kort aantal** dat de ontvangers niet eerder hebben gekozen uit.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26258){target="_blank"} om meer over deze kwestie te leren.

Leer meer over de opt-outconfiguratie van SMS [ op deze pagina ](../sms/sms-opt-out.md).

+++

## Kanaal in app

+++ Waarom kan ik niet rapporteren over het kanaal in de app in Customer Journey Analytics?

De moeilijkheden die op het **in-app kanaal** in Adobe Customer Journey Analytics melden komen vaak uit misconfigured **gegevensmeningen**, **datasets**, of **schemaupdates** voort. Controleer of deze configuraties correct zijn toegepast om het probleem op te lossen.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26206){target="_blank"} om meer over deze kwestie te leren.

Leer meer hoe te om de analysegegevens van Journey Optimizer in Customer Journey Analytics [ op deze pagina ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/integrations/ajo#automatically-configure-journey-optimizer-integration){target="_blank"} te integreren.

Zie ook de [ Journey Optimizer All-time documentatie van rapporten ](../reports/report-gs-cja.md)

+++


## Data management {#ajo-troubleshooting-data-management}

+++ Hoe zijn de tijd-aan-Levende (TTL) montages van toepassing op de datasets van het Profiel en van het Leer van Gegevens wanneer u een nieuwe zandbak creeert?

Organisaties die nieuwe sandboxen in Adobe Journey Optimizer leveren, hebben vragen opgeworpen over hoe de instellingen voor tijd tot leven (TTL) van toepassing zijn op de datasets van het Profiel en Gegevensmeer. Dit artikel verduidelijkt dat de montages van TTL geen bestaande zandbakken beïnvloeden en automatisch toegepast slechts op nieuw provisioned degenen.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} om te leren hoe te om TTL te behandelen.

Leer meer over dataset tijd-aan-levende [ op deze pagina ](../data/datasets-ttl.md).

+++


## Profielen en beheer van het publiek {#ajo-troubleshooting-audiences}

+++ Hoe kan ik verschillen in aantal gebruikers oplossen?

Het aantal verwerkte ingangen in de **Gelezen eigenschap van het Publiek** van Adobe Journey Optimizer kan lager zijn dan de verwachte publiekstelling. Dit probleem doet zich vaak voor als gevolg van onjuiste naamruimteconfiguraties, waardoor profielen van reizen worden uitgesloten. De resolutie omvat het controleren en corrigeren van naamruimteconfiguraties, het controleren van relevante documentatie en het aanpassen van prioriteiten om ervoor te zorgen dat bewerkingen in Adobe Journey Optimizer soepeler verlopen.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} om te leren hoe te om deze kwestie op te lossen.

Zie ook [ dit artikel over verouderde publieksaantallen ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26166){target="_blank"}.

Leer meer over de **Gelezen activiteit van het publiek** in reizen [ op deze pagina ](../building-journeys/read-audience.md).

+++

+++ Waarom mislukken profielupdates?

In Adobe Journey Optimizer, kunnen bepaalde gebiedswaarden niet correct na het lopen door een **activiteit van het Profiel van de Update** in een reis bijwerken. In sommige gevallen kunnen bijgewerkte velden verdwijnen of terugkeren naar de vorige status. Om dit te richten, controleren voor conflicterende regels of voorwaarden, herzie toestemmingsmontages, gebruik een unieke dataset voor de **activiteit van het Profiel van de Update**, en verzeker geen ander insluitingsproces aan het zelfde profiel tezelfdertijd schrijft.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"} om stappen te leren om deze kwestie op te lossen.

Leer meer over de **activiteit van het Profiel van de Update** in reizen [ op deze pagina ](../building-journeys/update-profiles.md).

Zie ook de [ documentatie van Adobe Experience Platform over Inname van Gegevens ](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/tutorials/ingest-batch-data#dataset-activity){target="_blank"}.

+++

+++ Waarom komt er een verschil in aantal profielen bij een reis in vergelijking met het betrokken publiek?

De discrepantie kan gebeuren wanneer de reis een het profielmomentopname van een vorige dag gebruikt als de momentopname van de huidige dag niet beschikbaar op het tijdstip van reisuitvoering is.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26253){target="_blank"} om stappen te leren om deze kwestie op te lossen.

Leer meer in [ dit communautaire post van Journey Optimizer ](https://experienceleaguecommunities.adobe.com/t5/real-time-customer-data-platform/profile-snapshot-and-segment-qualification-troubleshooting/ba-p/698998){target="_blank"}.

Zie ook de [ documentatie van de Programma&#39;s API van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/api/schedules){target="_blank"} om te controleren wanneer uw dagelijkse baan gepland is.

+++


+++ Hoe kan ik problemen met de doelgroep oplossen?

De de bevolkingsproblemen van het publiek kunnen voorkomen wanneer de componenten of de middelen, vaak toe te schrijven aan recht, levering, of toestemmingsmisconfiguraties ontbreken. Als u deze problemen wilt verhelpen, begint u met het controleren van rechten, het garanderen van correcte provisioning en het controleren van machtigingen. Als het probleem aanhoudt, escaleer de zaak en coördineer met steunteams voor een volledige resolutie.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26333){target="_blank"} om stappen te leren om deze kwestie op te lossen.

Leer meer over de **activiteit van het Profiel van de Update** in reizen [ op deze pagina ](../building-journeys/update-profiles.md).

Zie ook de [ documentatie van het Profiel van Adobe Real-Time CDP ](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide#profile-detail){target="_blank"}.

+++

+++ Waarom is het aantal Engageable Profiles in een korte periode aanzienlijk gestegen? 

**toe te laten Profielen** metrisch wijst op het aantal unieke profielen die door reizen of campagnes in de afgelopen 12 maanden worden betrokken. Een plotselinge toename kan het gevolg zijn van doelgericht grote doelgroepen of wijzigingen in gegevenssets. Om dit te beheren, herzie de **profiel tellende logica**, onderzoeken reizen gericht op grote publiek, **filterpubliek** op het vervoerniveau, verminderen de **adresseerbare publieksgrootte**, en controleren **datasetveranderingen**.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26161){target="_blank"} om stappen te leren om deze kwestie op te lossen.

De het vergunningsgebruik en in dienst komende profielen van uw organisatie controleren gebruikend het [ dashboard van het Gebruik van de Vergunning ](../audience/license-usage.md)

Zie ook het [ overzicht van de Dienst van de Vraag van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/query/home){target="_blank"}.

+++

+++ Waarom worden e-mails naar personen buiten het beoogde publiek verzonden op basis van datumfuncties?

E-mails kunnen worden verzonden naar ontvangers die **niet aan de gespecificeerde publiekscriteria** voldoen. Bijvoorbeeld, kunnen de leden met terugkoopdata **vóór 4 Juli, 2025** e-mails ontvangen die slechts voor die na die datum worden bestemd. Dit gedrag kan uit **misconfigured publiekssegmentatie** of **onverwachte veranderingen in de logica van de profielkwalificatie** voortvloeien.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26173){target="_blank"} om stappen te leren om deze kwestie op te lossen.

Leer meer over datumfuncties [ op deze pagina ](../building-journeys/functions/date-functions.md).

+++

+++ Hoe kan ik problemen met publieksselectie en Chrome-fouten oplossen bij het opslaan van reizen?

Het toevoegen van publiek aan reisvoorwaarden kan soms **toepassingsneerstortingen** veroorzaken of een **Onverwachte fout van de Waaier** in Chrome tonen, met inbegrip van fouten wanneer het bewaren van reizen. Deze kwesties zijn vaak verwant met **de diensten van het Chroom**. Om hen op te lossen, a **browser update** toepassen of een aangewezen **tijdelijke oplossing** gebruiken.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26145){target="_blank"} om stappen te leren om deze kwestie op te lossen.

+++

## Journeys {#ajo-troubleshooting-journeys}

Raadpleeg de volgende secties over het oplossen van problemen voor Reizen:

* [ los fouten vóór het testen van uw reis ](../building-journeys/troubleshooting.md) problemen op
* [ los binnenkomende acties in reizen ](../building-journeys/troubleshooting-inbound.md) problemen op
* [ los uw levende reisuitvoering ](../building-journeys/troubleshooting-execution.md) problemen op
* [Aangepaste acties oplossen](../action/troubleshoot-custom-action.md)


+++ Waarom gaan expressies verloren bij het maken van een nieuwe reisversie?  

Wanneer het creëren van een nieuwe versie van een reis, **uitdrukkingen in specifieke stappen** kunnen worden verloren, veroorzakend fouten en vereist handterugkeer. Om dit op te lossen, **dupliceer de reis**, test voor reproduceerbaarheid, **vermijden browser herlaadt**, en gebruik het **bijgewerkte canvas** voor oudere reizen.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26152){target="_blank"} om stappen te leren om deze kwestie op te lossen.

Leer hoe te om een reis [ op deze pagina ](../building-journeys/journey-ui.md#duplicate-a-journey) te dupliceren.

+++

+++ Waarom worden profielen voortijdig afgesloten? 

Profielen kunnen een reis onverwacht verlaten zonder door een aangewezen knoop over te gaan wanneer de **voorwaarde die status** van verzonden berichten controleert misconfigured is. Om dit op te lossen, herzie de **voorwaardenlogica**, voer **alternatieve logica** uit, of raadpleeg met uw **implementatieteam**.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26127){target="_blank"} om stappen te leren om deze kwestie op te lossen.

Zie ook [ het ontwerprichtlijnen van de Reis ](../building-journeys/using-the-journey-designer.md).

+++


+++ Waarom worden profielen onverwachts afgezet?

De profielen kunnen een reis onverwacht verlaten wanneer **gebeurtenis het begrenzen** voorkomt, veroorzakend sommige profielen om worden verworpen als het aantal verwerkte gebeurtenissen systeemcapaciteit overschrijdt. Om profieluitgang te verminderen, begrijp de **systeemgrenzen**, controleer voor **gebeurtenisspikes**, en optimaliseer **gegevensstroom** om het overschrijden van drempels te verhinderen.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26018){target="_blank"} om stappen te leren om deze kwestie op te lossen.

Zie ook [ reisbegeleiding ](../start/guardrails.md#decisioning-guardrails).

+++


+++ Waarom leidt mijn gebeurtenis niet tot de geplande reis?  

De gebeurtenissen kunnen er niet in slagen om een reis teweeg te brengen zelfs als alle criteria worden voldaan aan wanneer zij **door vraagdiensten** eerder dan wordt gestroomd aan de **Dienst van de Kern van de Inzameling van Gegevens (DCCS)** worden gecreeerd. Om dit op te lossen, herzie de gebeurtenisconfiguratie, zorg ervoor gebeurtenissen **direct aan DCCS** worden gestroomd, en verifieer functionaliteit gebruikend **testwijze**.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"} om stappen te leren om deze kwestie op te lossen.

Leer meer over gebeurtenissen [ op deze pagina ](../event/about-events.md).

Zie ook {de guardrails van de Gebeurtenis van 0}. [](../start/guardrails.md#events-g)

+++


+++ Hoe los ik problemen op die aanleiding geven tot reizen nadat het publiek in Adobe Journey Optimizer is veranderd? 

Als een reis na wijzigingen aan zijn bijbehorend publiek, zoals veranderingen in het fusiebeleid ophoudt teweegbrengend, kunt u onderbroken stromen ervaren. Om dit op te lossen, **dupliceer en publiceer de reis** met de bijgewerkte publieksmontages om trekkerfunctie correct te verzekeren.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"} om stappen te leren om deze kwestie op te lossen.

Leer hoe te om een reis [ op deze pagina ](../building-journeys/journey-ui.md#duplicate-a-journey) te dupliceren.

+++

+++ Waarom een douaneactie die een externe derde eindpunttijd roepen uit?

De fouten van de onderbreking kunnen voorkomen wanneer a **douaneactie** een extern derdeeindpunt roept. Om dit op te lossen, verifieer dat het **eindpunt toegankelijk** is, controleer **serverlogboeken**, ervoor zorgen er **geen het blokkeren van Adobe** is, update eindpuntconfiguraties zoals nodig, en **test na updates**. Ook, houd rekening met **API specificaties van de vraagonderbreking**.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26156){target="_blank"} om stappen te leren om deze kwestie op te lossen.

Leer meer over Reis het Draaien API [ op deze pagina ](../configuration/throttling.md).

Zie ook de [ Integratie met externe systeemdocumentatie ](../configuration/external-systems.md).

+++

+++ Welke stappen zou u moeten nemen als u een fout 403 met het bericht **invalid_access** of **Geen toegang tot dit gegevenId=XX verleende** wanneer het publiceren van een publiek van een pijl?

Als u deze fout wilt verhelpen, vraagt u de beheerder om te controleren of uw gebruikersprofiel toegang heeft tot de vereiste gegevensweergaven voor het publiceren van publiek. Probeer vervolgens het publiek opnieuw te publiceren.

Verwijs naar [ de toestemmingendocumentatie ](../administration/permissions.md){target="_blank"} om stappen te leren om deze kwestie op te lossen.

+++

## Regels {#ajo-troubleshooting-rules}

+++ Waarom werkt de vervolgkeuzelijst voor uitlijnen niet?

De kwesties met **Capping regels dropdown** komen vaak voor wanneer de regelreeksen **misconfigured** of **ontoegankelijk** zijn. Zorg ervoor dat alle regelreeksen correct worden gevormd en beschikbaar zijn om het probleem op te lossen.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26204){target="_blank"} om meer te leren.

Leer hoe te om het begrenzen van regels [ in deze sectie ](../conflict-prioritization/rule-sets.md) toe te passen.

+++

## Beslissing {#ajo-troubleshooting-decisioning}

+++ Hoe los ik problemen op bij het maken van aanbiedingsverzamelingen?

De moeilijkheden die tot aanbiedingsinzamelingen leiden komen vaak voor wanneer **catalogi niet provisioned** voor uw organisatie zijn. Om dit op te lossen, verifieer dat alle vereiste catalogi correct provisioned zijn alvorens te proberen om aanbiedingsinzamelingen tot stand te brengen.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"} om stappen te leren om deze kwestie op te lossen.

Leer meer over aanbiedingsinzamelingen [ op deze pagina ](../offers/offer-library/creating-collections.md).

+++

+++ Waarom heb ik geen toegang tot Offer Decisioning?  

Wanneer het integreren van Adobe Target in een toepassing die Adobe Journey Optimizer gebruikt, kan de **Offer Decisioning** optie ontoegankelijk binnen de configuratie zijn DataStream. Dit komt typisch toe te schrijven aan **toestemmingsmontages** of **leveringsbeperkingen**. Om de kwestie op te lossen, verifieer gebruikerstoestemmingen en controleer de noodzakelijke levering op zijn plaats is.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26175){target="_blank"} om stappen te leren om deze kwestie op te lossen.

Leer meer over vereiste toestemmingen voor Offer Decisioning [ op deze pagina ](../offers/get-started/starting-offer-decisioning.md#granting-acess-to-decision-management).

+++



## Meertalig {#ajo-troubleshooting-multilingual}

+++ Hoe los je dit probleem op `Message validation error (CJMMAS - 1069-500)`?

In Adobe Journey Optimizer voorkomt een Message Validation Error (CJMMAS - 1069-500) die gekoppeld is aan de meertalige functie dat reizen niet in de testmodus worden ingesteld of worden gepubliceerd.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"} om stappen te leren om deze kwestie op te lossen.

Leer meer over meertalige inhoud [ op deze pagina ](../content-management/multilingual-gs.md).

+++


## Configuratie {#ajo-troubleshooting-config}

+++ Hoe kan ik TLS v1.3 inschakelen voor aangepaste handelingen?  

Om **gegevensintegriteit en veiligheid** te handhaven wanneer het verbinden met derdesystemen, zorg ervoor dat de Veiligheid van de Laag van het Vervoer (**TLS**) v1.3 voor uw douaneacties wordt toegelaten. Dit helpt mededelingen beschermen en verhindert potentiële veiligheidskwetsbaarheid.


Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"} om meer te leren.

Leer meer over meertalige inhoud [ op deze pagina ](../action/about-custom-action-configuration.md).

+++

+++ Waarom kan ik geen dashboard direct van een vraag in Adobe Journey Optimizer tot stand brengen? 

In Adobe Journey Optimizer kunnen dashboards niet rechtstreeks van query&#39;s worden gemaakt. Om dashboards te bouwen, gebruik de beschikbare **functies van de dashboardverwezenlijking** binnen Adobe Experience Platform, die u toestaan om vraaggegevens effectief te visualiseren en te analyseren.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"} om meer te leren.

+++

## API&#39;s {#ajo-troubleshooting-apis}

+++ Hoe los ik toegangskwesties met de Dienst API van de Vraag op?  

De fouten van de toegang wanneer het gebruiken van de **Dienst API van de Vraag** via Postman of gelijkaardige hulpmiddelen worden gewoonlijk veroorzaakt door **ontoereikende toestemmingen**. Om dit op te lossen, verifieert u gebruikerstoestemmingen, controleert API geloofsbrieven, en verstrekt gedetailleerde informatie om indien nodig te steunen.

Verwijs naar [ dit het oplossen van problemenartikel ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26196){target="_blank"} om meer te leren.

Zie ook [ leiden API geloofsdocumentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions#manage-api-credentials-for-role){target="_blank"}.

+++
