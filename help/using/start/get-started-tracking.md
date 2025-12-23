---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met bijhouden in Journey Optimizer
description: Meer informatie over de mogelijkheden voor bijhouden en controleren in Journey Optimizer
feature: Monitoring
topic: Administration
role: User
level: Beginner
keywords: bijhouden, bewaken, analyseren, rapporteren, leverbaarbaarheid
source-git-commit: 4dfda2a13bfd01c7c556ae3e8eb31916592c569b
workflow-type: tm+mt
source-wordcount: '1916'
ht-degree: 3%

---

# Aan de slag met bijhouden in Journey Optimizer {#get-started-tracking}

Het volgen en de controle laten u toe om campagnedoeltreffendheid te meten, klantenervaringen te optimaliseren, en berichten te verzekeren bereiken hun voorgenomen ontvangers. Journey Optimizer biedt uitgebreide mogelijkheden voor het bijhouden van gegevens die de interactie van de klant, de leveringsprestaties en de systeemstatus vastleggen, zodat u uw gegevensgestuurde beslissingen kunt nemen zonder afbreuk te doen aan de privacy en de naleving van de regels.

De meeste tracking wordt automatisch geconfigureerd wanneer u berichten en reizen maakt. Voor geavanceerde scenario&#39;s, kunt u opstellings douanemetriek, URL parameters vormen, en met externe analyseplatforms integreren. Heb toegang tot uw het volgen gegevens door ingebouwde rapporten of voer het voor diepere analyse in Customer Journey Analytics uit.

>[!BEGINSHADEBOX]

Wat je kunt bijhouden in Journey Optimizer:

📧 **E-mailinteractie** - opent, klikt, en verbindingsprestaties

🌐 **het gedrag van het Web** - de meningen van de Pagina, klikken, en betrokkenheidspatronen

🛤️ **prestaties van de Reis** - de metriek van de Douane, stapgebeurtenissen, en omzettingswegen

📊 **gezondheid van de Leverbaarheid** - Stuiteren tarieven, spamklachten, en de reputatie van de afzender

⚙️ **de verrichtingen van het Systeem** - Alarm, fouten, en de prestaties van de douaneactie

>[!ENDSHADEBOX]

Om u te helpen begonnen worden, verkend deze essentiële volgende en controlerende onderwerpen:

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="../building-journeys/success-metrics.md">
    <img alt="Metrics" src="../assets/do-not-localize/success-metrics.jpeg">
    </a>
    <div>
    <a href="../building-journeys/success-metrics.md"><strong> vorm succesmetriek </strong></a>
    </div>
    <p>
    <em> Aangepaste KPIs van het Spoor die met uw bedrijfsdoelstellingen </em> wordt gericht
    <p>
  </td>
  <td>
    <a href="../reports/deliverability.md">
    <img alt="Strategie en definitie" src="../assets/do-not-localize/deliverability.jpeg">
    </a>
    <div>
    <a href="../reports/deliverability.md"><strong> de leverbaarheid van de Monitor </strong></a>
    </div>
    <p>
    <em> verzeker uw berichten klanteninboxes </em> bereiken
    <p>
  </td>
  <td>
    <a href="../reports/gs-reports.md">
    <img alt="Rapportage" src="../assets/do-not-localize/reporting.jpeg">
    </a>
    <div>
    <a href="../reports/gs-reports.md"><strong> onderzoek rapporterend </strong></a>
    </div>
    <p>
    <em> toegang levende en historische rapporten voor uw reizen en campagnes </em>
    <p>
  </td>
</tr>
</table>

## De klanteninteractie van het spoor over kanalen {#tracking-by-channel}

Journey Optimizer biedt kanaalspecifieke trackingsmogelijkheden. Hier is hoe te om het volgen voor elk kanaal te vormen en te gebruiken.

+++E-mailtracking

E-mailtracking wordt automatisch ingeschakeld wanneer u een e-mailbericht maakt. De sporen van Journey Optimizer opent, klikt, en unsubscribes door gebrek-geen extra configuratie nodig.

**vorm volgende opties:**

* **laat/maakt het volgen** toe - Controle het volgen op het berichtniveau wanneer het ontwerpen van uw e-mail. U kunt ervoor kiezen om opent, klikt of beide bij te houden. [Meer informatie](../email/message-tracking.md)

* **opstelling URL die parameters** volgen - vorm volgende parameters op het oppervlakteneniveau om campagne-herkenningstekens (utm_campagne, utm_source, enz.) aan alle e-mailverbindingen automatisch toe te voegen. Hierdoor wordt het bijhouden van eigenschappen mogelijk voor uw gehele digitale ecosysteem. [Meer informatie](../email/url-tracking.md)

* **de verbindingen van het Spoor in bewaarde fragmenten** - wanneer u sparen een fragment van inhoud die het volgen toegelaten heeft, blijven de verbindingen in dat fragment gevolgd wanneer u het in andere reizen of campagnes hergebruikt. [Meer informatie](../content-management/save-fragments.md)

* **voeg spiegelpagina het volgen** toe - laat de optie van de spiegelpagina toe om een Webversie van uw e-mail met het automatische volgen van toe wie het bekijkt. [Meer informatie](../email/message-tracking.md#mirror-page)

**prestaties van de Monitor:** metriek van de Mening in real time in campagne en reisrapporten met inbegrip van opent, klikt, en verbinding-vlakke prestaties. [ de rapporten van de Campagne ](../reports/campaign-global-report-cja-email.md) | [ de rapporten van de Reis ](../reports/journey-global-report-cja-email.md)

+++

+++Webtracking

Webtracering vereist expliciete configuratie om gebruikersinteracties met uw webwijzigingen te volgen.

**opstelling klikt het volgen:**

Wanneer u een webpagina ontwerpt, kunt u specifieke elementen (knoppen, afbeeldingen, koppelingen) selecteren die u wilt bijhouden. Hiermee schakelt u het bijhouden van klikken voor die elementen in zonder dat extra code vereist is. [Meer informatie](../web/monitor-web-experiences.md)

* **spoor om het even welk klikbaar element** - Uitgezochte knopen, beelden, verbindingen, of om het even welk interactief element in uw Webverpersoonlijking.
* **Automatische gegevensinzameling** - Zodra gevormd, vangt Journey Optimizer automatisch gebeurtenissen en associeert hen met profielen.
* **Monitor in real time** - de gebruikersinteractie van het spoor aangezien zij om verpersoonlijkingsdoeltreffendheid bevestigen.

**het volgen van de Mening gegevens:** de vertoningsmetriek van de Toegang, klik-door tarieven, en element-vlakke prestaties in rapporten. [ de rapporten van de Campagne ](../reports/campaign-global-report-cja-web.md) | [ de rapporten van de Reis ](../reports/journey-global-report-cja-web.md)

+++

+++Push notification tracking

Het volgen van de duw wordt automatisch toegelaten en vangt (geleverde) indrukken, klikt (ingetikt), en opent (app lanceerde). Om het volgen waarde te maximaliseren, vorm klikbare elementen in uw duw inhoud.

**vorm getraceerde elementen:**

* **de klikgedrag van het Lichaam** - plaats wat gebeurt wanneer de gebruikers het bericht tikken: open app, navigeer aan een deplink, of open een Web URL. Elke actie wordt automatisch bijgehouden. [Meer informatie](../push/design-push.md#on-click-behavior)

* **voeg actieknoppen** toe - omvat tot 3 knopen (Android) of veelvoudige knopen (iOS) met onafhankelijke het volgen voor elke knoopactie (open app, deplink, Web URL). [Meer informatie](../push/design-push.md#add-buttons-push)

* **laat het volgen** toe - verifieer het volgen wordt toegelaten in uw activiteit van de duwreis of campagne het volgen montages. [Meer informatie](../push/create-push.md#create)

>[!NOTE]
>
>Voor pushtracering is mobiele SDK-implementatie vereist. Zorg ervoor dat de Adobe Experience Platform Mobile SDK correct is geconfigureerd voor uw app. [Meer informatie](../push/push-configuration.md#integrate-mobile-app)

**analyseer overeenkomst:** klik-door tarieven van de Mening, knoopprestaties, en gevolgde verbindingsdetails in rapporten. [ de rapporten van de Campagne ](../reports/campaign-global-report-cja-push.md) | [ de rapporten van de Reis ](../reports/journey-global-report-cja-push.md)

+++

+++In-app berichten bijhouden

In-app berichten volgen automatisch weergaven en gebruikersinteracties. Configureer triggers en inhoud om de effectiviteit van bijhouden te maximaliseren.

**opstelling het volgen:**

* **bepaalt vertoningsregels** - plaats wanneer en waar binnen-app berichten gebruikend trekkers (app lancering, het schermlading), frequentieregels, en publieksvoorwaarden verschijnen. De juiste configuratie verzekert nauwkeurige het volgen van zowel teweeggebrachte als getoonde berichten.

* **voeg bijgehouden elementen** toe - omvat knopen, verbindingen, en interactieve elementen in uw berichtinhoud. Elke interactie wordt automatisch gevolgd met gedetailleerde labels.

* **optimaliseer vertoningstiming** - vorm dag-van-week en tijd-van-dag regels om de waarschijnlijkheid te maximaliseren dat de teweeggebrachte berichten eigenlijk aan gebruikers worden getoond.

[Leer hoe u in-app-berichten configureert](../in-app/create-in-app.md)

**wat wordt gevolgd:** Journey Optimizer vangt automatisch vertoningen, knoop klikt, ontslagen, teweeggebracht vs. getoonde metriek, en verbindingsprestaties. [ de rapporten van de Campagne ](../reports/campaign-global-report-cja-inapp.md) | [ de rapporten van de Reis ](../reports/journey-global-report-cja-inapp.md)

+++

+++SMS en MMS bijhouden

Voor het bijhouden van SMS is een minimale installatie vereist. Journey Optimizer zorgt ervoor dat koppelingen die u in berichten opneemt, automatisch worden ingekort en bijgehouden.

**hoe het werkt:**

* **Automatische verbinding het volgen** - voeg om het even welke URL aan uw inhoud van SMS toe gebruikend de hulpfunctie URL. Journey Optimizer verkort automatisch de verbinding en houdt kliks zonder extra configuratie bij. Als u URL-verkorting wilt gebruiken, moet u eerst een SMS-subdomein configureren. [Meer informatie](../sms/sms-subdomains.md)

* **Binnenkomende bericht het volgen** - de antwoorden van ontvangers worden automatisch gevangen, toestaand u om bidirectionele gesprekken en reactiepatronen te controleren. [Meer informatie](../sms/sms-opt-out.md#sms-native-keywords)

**metriek van de Mening:** de verbindingsgegevens van de Toegang klikken, binnenkomende berichtvolumes, en berichttype prestaties in rapporten. [ de rapporten van de Campagne ](../reports/campaign-global-report-cja-sms.md) | [ de rapporten van de Reis ](../reports/journey-global-report-cja-sms.md)

+++

+++Op code gebaseerde ervaring bijhouden

Voor op code gebaseerde ervaringen is implementatieinstelling vereist om trackinggegevens naar Adobe Experience Platform te verzenden.

**Eerste vereisten:**

Voordat tracking werkt, moet u uw implementatie configureren om interactiegebeurtenissen (weergaven, klikken) naar Adobe Experience Platform te verzenden. Hiervoor is het volgende vereist:

* Een gegevensstroom instellen die is geconfigureerd voor Adobe Experience Platform. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html)
* Het uitvoeren van gebeurtenisinzameling in uw code die Web SDK of Mobiele SDK gebruikt.
* Weergave- en interactiegebeurtenissen verzenden wanneer inhoud wordt weergegeven of geklikt.

[Meer informatie over implementatievereisten](../code-based/code-based-prerequisites.md#reporting-prerequisites)

**wat wordt gevolgd:** zodra uitgevoerd, spoorvertoningen, kliks, kliks-door tarieven, en element-vlakke prestaties over om het even welk digitaal aanraakpunt (websites, mobiele apps, apparaten IoT, enz.). [ de rapporten van de Campagne ](../reports/campaign-global-report-cja-code.md) | [ de rapporten van de Reis ](../reports/journey-global-report-cja-code.md)

+++

+++Tekstspatiëring van inhoudskaarten

Met inhoudskaarten worden gebruikersinteracties automatisch bijgehouden. Vorm inhoud en vertoningsregels om het volgen gedrag te controleren.

**hoe te om uit te voeren:**

* **Ontwerp volgde inhoud** - voeg knopen en verbindingen aan uw inhoudskaart toe. Elk interactief element wordt automatisch bijgehouden met labels en URL&#39;s.

* **vorm persistentie** - De kaarten van de inhoud blijven over toepassingszittingen, toestaand u om betrokkenheidspatronen op lange termijn te volgen. Stel de verloopregels in om te bepalen hoe lang kaarten traceerbaar blijven.

* **de vertoningsregels van de opstelling** - bepaal wanneer en waar de kaarten verschijnen om nauwkeurige het volgen van vertoningen vs. interactie te verzekeren.

[Leer hoe u inhoudskaarten kunt configureren](../content-card/create-content-card.md)

**Overeenkomst van de Monitor:** de vertoningen van het Spoor, klikken, kliks-door tarieven, en betrokkenheidspatronen over veelvoudige zittingen. [ de rapporten van de Campagne ](../reports/campaign-global-report-cja-content.md) | [ de rapporten van de Reis ](../reports/journey-global-report-cja-content.md)

+++

+++Bezig met bijhouden van bestemmingspagina

De bestemmingspagina&#39;s komen met ingebouwde het volgen die geen extra opstelling vereist. Journey Optimizer legt automatisch bezoeken, omzettingen en stuiterende koersen vast.

**wat automatisch wordt gevolgd:**

* **bezoeken** - Totaal en unieke bezoeken om bereik te meten
* **Conversies** - de Inzendingen van de vorm, abonnementbevestigingen, of andere bepaalde acties
* **Stuitpercentage** - Percentage bezoekers die zonder interactie vertrekken
* **trends van Prestaties** - tijd-reeksen gegevens die tonen hoe de metriek evolueren

[Leer hoe u bestemmingspagina&#39;s kunt configureren](../landing-pages/create-lp.md)

**prestaties van de Monitor:** de patronen van het Bezoek van het spoor, omzettingen, en stuittarieven in tijd om te begrijpen hoe de gebruikers met uw vormen in wisselwerking staan en gebieden voor verbetering identificeren. [ de rapporten van de Campagne ](../reports/lp-report-global-cja.md)

+++

## Volg uw reis- en campagneactiviteiten {#journey-campaign-tracking}

Buiten kanaal-niveau het volgen, vorm het volgen om algemene prestaties te meten en klantengedrag over uw marketing initiatieven te begrijpen.

* **bepaalt de metriek van het douanesucces** - vorm specifieke KPIs die met uw bedrijfsdoelstellingen (aankopen, tekenings-ups, vernieuwingen, enz.) voorbij standaardbetrokkenheidsmetriek wordt gericht. [Meer informatie](../building-journeys/success-metrics.md)

* **laat de gebeurtenissen van de reisstap** toe - activeer gedetailleerde het volgen van elke actieklanten nemen aangezien zij zich door reizen bewegen. Dit biedt granulaire zichtbaarheid in entry/exit-punten, padselectie en drop-down-locaties. [Meer informatie](../reports/journey-step-events-overview.md)

* **opstelling die** plant - vorm send-time optimalisering om prestaties over verschillende timingsstrategieën te volgen en optimale te identificeren verzendt vensters. [Meer informatie](../building-journeys/send-time-optimization.md)

* **vorm douaneacties controle** - opstelling het volgen voor integratie met externe systemen om API vraag, reactietijden, en foutenpatronen te controleren. [Meer informatie](../action/reporting.md)

* **Douane rapporteert &amp; gegevens** - bouw op maat gemaakte rapporten en de uitvoer volggegevens naar externe systemen voor diepere analyse. [Meer informatie](../reports/sharing-overview.md)

**Mening verenigde prestaties:** toegang uitvoerige rapporten voor zowel campagnes als reizen om prestaties over e-mail, duw, SMS, en andere kanalen te vergelijken, en te begrijpen welke combinaties drijven de beste resultaten. [ de rapporten van de Campagne ](../reports/campaign-global-report-cja.md) | [ de rapporten van de Reis ](../reports/journey-global-report-cja.md)

## Optimalisatie- en beslissingsprestaties bijhouden {#optimization-decisioning-tracking}

Journey Optimizer volgt automatisch optimalisatieexperimenten, doelgerichte strategieën en beslissingsprestaties. Configureer uw instellingen voor een correcte gegevensverzameling.

### Optimalisatie bijhouden instellen {#optimization-tracking}

* **Optimalisering in uw campagnes en reizen**

   * Definieer bij het maken van experimenten welke meetgegevens moeten worden bijgehouden (conversies, klikken, aangepaste gebeurtenissen). Journey Optimizer verzamelt automatisch prestatiegegevens voor elke behandeling. [Meer informatie](../campaigns/campaigns-message-optimization.md#experimentation)

   * Creeer het richten regels om verschillende inhoud aan verschillende publiekssegmenten te leveren. Journey Optimizer volgt automatisch de betrokkenheidswaarden voor elke doelgroep, zodat u de prestaties voor de verschillende segmenten kunt vergelijken. [Meer informatie](../campaigns/campaigns-message-optimization.md#targeting)

* **optimalisering van de weg van de Reis** - voeg **** activiteit aan uw reis toe optimaliseren en veelvoudige wegen vormen. Journey Optimizer houdt automatisch bij welke paden worden gebruikt en meet de prestaties. [Meer informatie](../building-journeys/optimize.md)

**analyseert resultaten:** de omrekeningskoersen van de Mening, statistische betekenis, en heft tussen behandelingen in experimentatierapporten op, of vergelijk betrokkenheidsmetriek over gerichte segmenten. [ het campagnerapport van de Experimentatiecampagne van de Experimentatie ](../reports/campaign-global-report-cja-experimentation.md) | [ het rapport van de reis van de Experimentatie ](../reports/journey-global-report-cja-experimentation.md) | [ Reis richtend rapport ](../reports/journey-global-report-cja.md#targeting)

### Prestaties van beslissingen bijhouden {#decisioning-tracking}

Wanneer het gebruiken van Beslissing om inhoud te personaliseren, volgt Journey Optimizer automatisch besluitvormingsgebeurtenissen, impressies, en klikt zonder extra vereiste configuratie.

* **Automatische gebeurtenis vangt** - Journey Optimizer vangt automatisch besluitvormingsgebeurtenissen vast wanneer een besluitpunt voor een profiel wordt geselecteerd.
* **het volgen van de Indruk** - voor e-mail, worden de indrukkingen automatisch gevolgd. Voor code-gebaseerde ervaringen, moet u de gebeurtenissen van de voorzetvertoning in uw code uitvoeren.
* **klik het volgen** - de klikken op besluitvormingspunten worden automatisch gevolgd in e-mail; op code-gebaseerde ervaringen vereisen het uitvoeren van klikgebeurtenissen.

**Vereisten voor op code-gebaseerde het volgen:** om besluitvorming in op code-gebaseerde ervaringen te volgen, zorg ervoor uw implementatie de gebeurtenissen van de vraaginteractie (vertoningen en klikken) naar Adobe Experience Platform verzendt gebruikend Web SDK of Mobiele SDK. [Meer informatie](../experience-decisioning/data-collection/schema-requirement.md)

**analyseert prestaties:** De besluitvorming KPIs van de Mening, vergelijkt besluitvormingspunten, analyseert selectiestrategieën, en controleert AI modelprestaties in rapporten. [Meer informatie](../experience-decisioning/cja-reporting.md)

## Gebruik van volggegevens beheren {#data-governance}

Het beleid van het beheer van gegevens staat u toe om te controleren hoe het volgen gegevens over uw organisatie kunnen worden gebruikt:

* **Van het Etiket gevoelige het volgen gegevens** - pas governance etiketten op gevolgde gedragsgegevens (b.v., klikt op gezondheidsinhoud, financiële productinteractie) toe om het als gevoelig of gereguleerd te merken.

* **Beperk gegevensgebruik** - creeer beleid dat geëtiketteerde het volgen gegevens in bepaalde kanalen verhinderen worden gebruikt, die naar derdesystemen worden uitgevoerd, of voor specifieke verpersoonlijkingsscenario&#39;s worden gebruikt.

* **Automatische handhaving** - Journey Optimizer controleert automatisch behoorlijk beleid wanneer u reizen en campagnes bouwt, die publicatie blokkeren als de bijgehouden gegevens in schending van bepaald beleid worden gebruikt.

Het beheer van gegevens zorgt voor naleving van regels zoals GDPR en CCPA, terwijl u het gedrag van klanten binnen goedgekeurde grenzen kunt volgen en analyseren. [Meer informatie](../action/action-privacy.md)

## Leverbaarheid en systeemstatus bewaken {#monitoring-capabilities}

Naast het volgen van betrokkenheid, vorm controle om ervoor te zorgen de berichten inboxes bereiken en de systemen presteren optimaal.

De controle van de leverbaarheid helpt ervoor zorgen uw berichten binnendozen van ontvangers bereiken en gezonde afzenderreputatie door zeer belangrijke indicatoren te volgen handhaven:

* **herzie de suppressielijst** regelmatig om te begrijpen waarom de adressen worden geblokkeerd en lijshygiëne handhaven. [Meer informatie](../reports/suppression-list.md)

* **analyseert leveringsfouten** om mislukkingen te diagnostiseren en correctieve actie te voeren. [Meer informatie](../configuration/email-error-types.md)

* **volg beste praktijken** voor DMARC, SPF, en DKIM om inbox plaatsing te maximaliseren. [Meer informatie](../reports/deliverability.md)

Stel proactieve bewaking in om meldingen in real time over kritieke gebeurtenissen en systeemproblemen te ontvangen, zodat u snel kunt reageren voordat deze van invloed zijn op de ervaringen van uw klanten:

* **vorm alarm** - de berichten van de opstelling in real time voor reisfouten, de mislukkingen van de douaneactie, en kritieke kwesties om snel aan problemen te antwoorden. [Meer informatie](../reports/alerts.md)

* **laat controlelogboeken** toe - activeer controleregistreren om alle acties op middelen voor naleving en het oplossen van problemen te volgen. [Meer informatie](../privacy/audit-logs.md)

* **de integraties van de Monitor** - de prestaties van de douaneactie van het spoor en externe systeemconnectiviteit om integratiekwesties vroegtijdig te identificeren. [Meer informatie](../action/reporting.md)

