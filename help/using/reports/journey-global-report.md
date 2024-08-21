---
solution: Journey Optimizer
product: journey optimizer
title: Journaal algemeen rapport
description: Meer informatie over het gebruik van gegevens uit het global report van de reis
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: 428e08ca712724cb0b3453681bee1c7e86ce49dc
workflow-type: tm+mt
source-wordcount: '4150'
ht-degree: 0%

---

# Journaal algemeen rapport {#journey-global-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_global_report"
>title="Journaal algemeen rapport"
>abstract="Met het algemene rapport Journey kunt u de impact van uw reizen over een bepaalde tijdsperiode meten. Uw rapport is verdeeld in verschillende widgets die het succes en de fouten van uw reis gedetailleerd beschrijven. Elk rapportdashboard kan worden gewijzigd door widgets te vergroten of te verkleinen of te verwijderen."

>[!AVAILABILITY]
>
>De huidige ervaring met rapportage wordt vanaf de release van oktober opgeheven. Na deze datum wordt de nieuwe ervaring met rapportage de norm. We raden u aan bekend te maken met de nieuwe functies en functies om een soepele overgang te garanderen. [ worden begonnen met Journey Optimizer nieuwe het Melden interface.](report-gs-cja.md)

Globale rapporten, toegankelijk vanaf het tabblad Alle tijd, geven gebeurtenissen weer die zich ten minste twee uur geleden hebben voorgedaan en bestrijken gebeurtenissen gedurende een geselecteerde tijdsperiode. In vergelijking hiermee richten Live-rapporten zich op gebeurtenissen die zich in de afgelopen 24 uur hebben voorgedaan, met een minimale tijdsinterval van twee minuten vanaf het plaatsvinden van de gebeurtenis.

U hebt rechtstreeks via de knop **[!UICONTROL View report]** toegang tot het algemene rapport over de reis.

![](assets/report_journey.png)

De pagina &quot;trip **[!UICONTROL Global report]**&quot; wordt weergegeven met de volgende tabbladen:

* [Reis](#journey-global)
* [Email](#email-global)
* [Push](#push-global)
* [Sms](#sms-global)
* [In-app](#in-app-global)

De reis **[!UICONTROL Global report]** is verdeeld in verschillende widgets die het succes en de fouten van uw reis gedetailleerd beschrijven. Elke widget kan indien nodig worden vergroot of verkleind en verwijderd. Voor meer informatie over dit, verwijs naar deze [ sectie ](global-report.md#modify-dashboard).

Voor een gedetailleerde lijst van elke metrisch beschikbaar in Adobe Journey Optimizer, verwijs naar [ deze pagina ](global-report.md#list-of-components-global).

## Tabblad Reis {#journey-global}

Vanaf uw reis **[!UICONTROL Global report]** geeft het tabblad **[!UICONTROL Journey]** u een duidelijke weergave van de belangrijkste gegevens over uw reis.

### Reisprestaties {#journey-perfomance}

>[!CONTEXTUALHELP]
>id="ajo_journey_performance"
>title="Reisprestaties"
>abstract="Met de widget voor reisprestaties kunt u visueel het pad volgen van uw doelprofielen terwijl deze uw reis doorlopen."

![](assets/journey_performance.png)

Met de widget **[!UICONTROL Journey Performance]** kunt u visueel het traject volgen van uw doelprofielen terwijl u door de reis navigeert.

Let op: het aantal profielen voor een knooppunt wordt alleen bijgewerkt nadat het profiel het knooppunt heeft voltooid, niet wanneer het knooppunt wordt ingevoerd. Bijvoorbeeld, wacht een profiel op a **** knoop slechts wanneer de gespecificeerde datum wordt bereikt en het profiel de knoop heeft verlaten.

### Reisstatistieken {#journey-statistics}

>[!CONTEXTUALHELP]
>id="ajo_journey_statistics"
>title="Reisstatistieken"
>abstract="De belangrijkste indicatoren van de Prestaties van de Statistieken van de Reis (KPIs) dienen als uitvoerig dashboard, dat een diepgaande analyse van essentiële metriek met betrekking tot uw reis verstrekt."

![](assets/journey_statistics.png)

De **[!UICONTROL Journey Statistics]** Belangrijkste Indicatoren van Prestaties (KPIs) functioneren als een allesomvattend dashboard, dat een analyse van essentiële metriek verbonden aan uw reis levert. Dit omvat details zoals het aantal binnengekomen profielen en gevallen van mislukte individuele reizen, die een uitvoerig inzicht in de doeltreffendheid van uw reis en niveau van betrokkenheid aanbieden.

+++ Meer informatie over statistieken voor reisstatistieken

* **[!UICONTROL Entered profiles]**: Het totale aantal personen dat de gebeurtenis entry van de reis heeft bereikt.

* **[!UICONTROL Exited profiles]**: Het totale aantal personen dat de reis heeft verlaten.

* **[!UICONTROL Failed individual journey]**: Het totale aantal individuele reizen dat niet succesvol is uitgevoerd.

+++

### Prestaties van handelingen {#action-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_performance"
>title="Prestaties van handelingen"
>abstract="De widget Prestaties van acties illustreert de meest succesvolle acties die hebben plaatsgevonden toen uw acties werden geïnitieerd."

![](assets/journey_action_performance.png)

De widget **[!UICONTROL Action Performance]** vertegenwoordigt de meest succesvolle acties die zijn uitgevoerd toen de **[!UICONTROL actions]** werd geactiveerd.

### Bovenste acties {#top-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_top_actions"
>title="Bovenste acties"
>abstract="De tabel met de belangrijkste acties consolideert essentiële informatie over uw acties en geeft beknopte opmerkingen over zowel de frequentie als de doeltreffendheid van elke actie."

![](assets/journey_top_actions.png)

In de tabel **[!UICONTROL Top Actions]** worden de belangrijkste gegevens van uw **[!UICONTROL Actions]** gecompileerd. Het biedt beknopte inzichten in de frequentie en de prestaties van elke actie.

+++ Meer informatie over maatstaven voor acties bovenaan

* **[!UICONTROL Actions successfully executed]**: Het totale aantal **[!UICONTROL Actions]** dat is uitgevoerd voor een rit.

* **[!UICONTROL Error in action]**: het totale aantal fouten dat is opgetreden voor **[!UICONTROL Actions]** .

+++

### Foutredenen voor handelingen {#action-error}

>[!CONTEXTUALHELP]
>id="ajo_journey_actions_error_reasons"
>title="Foutredenen voor handelingen"
>abstract="De tabel met oorzaken van fouten in Handelingen en de grafiek geven een uitgebreid overzicht van de fouten die tijdens de uitvoering van de handelingen zijn aangetroffen. Zo krijgt u een uitgebreid overzicht van de problemen die zich kunnen hebben voorgedaan."

![](assets/journey_action_error.png)

De tabel en grafiek van **[!UICONTROL Action Error Reasons]** bieden een uitgebreid overzicht van de fouten die zijn opgetreden tijdens de uitvoering van uw **[!UICONTROL Actions]** .

### Gebeurtenissen naar oorsprong {#events-origin}

>[!CONTEXTUALHELP]
>id="ajo_journey_events_origin"
>title="Gebeurtenissen naar oorsprong"
>abstract="In de tabel Gebeurtenissen op oorsprong en de grafieken ziet u hoe uw gebeurtenissen met succes worden ontvangen. Met deze visuele voorstellingen kunt u nauwkeurig bepalen welke gebeurtenissen daadwerkelijk zijn ontvangen. Zo hebt u waardevolle inzichten in de prestaties en de impact van elke gebeurtenis op uw reis."

![](assets/journey_events_origin.png)

De **[!UICONTROL Events by origin]** -tabel en -grafieken bieden een gedetailleerd perspectief op de geslaagde ontvangst van de **[!UICONTROL events]** -tabel. Via deze visuele voorstellingen kunt u precies zien welke van uw **[!UICONTROL events]** effectief zijn ontvangen. Zo hebt u waardevolle inzichten in de prestaties en de impact van afzonderlijke gebeurtenissen op uw reis.

### Gebeurtenissen ontvangen per gebeurtenis {#events-received}

>[!CONTEXTUALHELP]
>id="ajo_journey_events_received"
>title="Gebeurtenissen ontvangen per gebeurtenis"
>abstract="De gebeurtenissen die door de grafiek van de Gebeurtenis worden ontvangen staan u toe om de specifieke gebeurtenissen binnen uw reis te identificeren en te analyseren die effectief werd uitgevoerd, leverend waardevolle inzichten in de prestaties en succespercentages van individuele gebeurtenissen."

![](assets/journey_event_received.png)

Met de grafiek van **[!UICONTROL Events received by event]** kunt u bepalen en analyseren welke specifieke **[!UICONTROL event]** tijdens uw reis effectief is uitgevoerd. Zo hebt u waardevolle inzichten in de prestaties en succespercentages van afzonderlijke gebeurtenissen.

### Frequente gebeurtenissen {#top-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_top_events"
>title="Frequente gebeurtenissen"
>abstract="De tabel Top Events consolideert essentiële gegevens over uw gebeurtenissen en geeft beknopte observaties over zowel de frequentie als de prestaties van elke afzonderlijke gebeurtenis."

![](assets/journey_top_events.png)

In de tabel **[!UICONTROL Top events]** worden de belangrijkste gegevens van uw **[!UICONTROL Events]** gecompileerd. Het biedt beknopte inzichten in de frequentie en prestaties van elke **[!UICONTROL Event]** .

### Toestemmingsbeleid {#consent-policies}

>[!CONTEXTUALHELP]
>id="ajo_journey_consent_policies"
>title="Toestemmingsbeleid"
>abstract="De lijst en de grafiek van het Beleid van de Toestemming tonen de hoeveelheid profielen die van elk beleid binnen uw douaneacties worden uitgesloten. Deze presentatie biedt een duidelijk inzicht in de invloed van elk toestemmingsbeleid op profieluitsluitingen."

![](assets/journey_consent.png)

In de tabel en grafiek van **[!UICONTROL Consent policies]** ziet u het aantal profielen dat is uitgesloten van elk beleid in uw aangepaste acties. Dit geeft een duidelijk inzicht in de gevolgen van elk toestemmingsbeleid voor profieluitsluitingen.

Voor meer informatie over douaneacties, verwijs naar [ de gedetailleerde documentatie ](../action/about-custom-action-configuration.md).

Houd er rekening mee dat u de dashboards opnieuw moet instellen als deze widgets alleen in uw journalistiek worden weergegeven. Klik hiertoe op **[!UICONTROL Modify]** en vervolgens op **[!UICONTROL Reset]** boven aan uw rapport.

## Tabblad E-mail {#email-global}

Vanaf uw reis **[!UICONTROL Global report]** geeft het tabblad **[!UICONTROL Email]** de belangrijkste informatie weer met betrekking tot de e-mails die tijdens uw reis worden verzonden.

### E-mail - Statistieken verzenden {#email-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sending_statistics"
>title="E-mail - Statistieken verzenden"
>abstract="De tabel E-mail - Statistieken verzenden bevat een overzicht van de belangrijkste gegevens over uw e-mail, zoals Gericht of bezorgd."

![](assets/journey_email_statistics.png)

De tabel **[!UICONTROL Email Sending Statistics]** bevat een uitgebreide samenvatting van essentiële gegevens over e-mails tijdens uw reizen. Het bevat belangrijke metriek zoals de grootte van het beoogde publiek en het aantal e-mails dat succesvol is afgeleverd. Het biedt waardevolle inzichten in de effectiviteit en het bereik van uw e-mails en reizen.

+++ Meer informatie over statistieken over verzendstatistieken per e-mail

* **[!UICONTROL Execution time]**: Begintijd van elke uitvoering van de reis in het geval van terugkerende reizen. Als u slechts één of meerdere herhalingen als doel wilt instellen, selecteert u deze in de vervolgkeuzelijst **[!UICONTROL Execution time]** .

* **[!UICONTROL Targeted]**: Het aantal profielen waarvoor een actie wordt uitgevoerd, zoals het verzenden van e-mail of sms.

* **[!UICONTROL Sent]**: Het totale aantal e-mails dat is verzonden voor de reis.

* **[!UICONTROL Delivered]**: Aantal verzonden e-mailberichten in verhouding tot het totale aantal verzonden e-mails.

* **[!UICONTROL Delivery Rate]**: percentage e-mailberichten is verzonden.

* **[!UICONTROL Bounces]**: het totaal aan fouten dat tijdens het verzendproces is gecumuleerd en de automatische retourverwerking in verhouding tot het totale aantal verzonden e-mails.

* **[!UICONTROL Bounce Rate]**: percentage e-mailberichten dat is teruggestuurd in vergelijking met verzonden e-mails.

* **[!UICONTROL Errors]**: het totale aantal fouten dat is opgetreden tijdens het verzendproces waardoor het niet naar profielen kan worden verzonden.

* **[!UICONTROL Error Rate]**: percentage fouten dat is opgetreden tijdens het verzendproces waardoor het niet kan worden verzonden, vergeleken met verzonden e-mailberichten.

* **[!UICONTROL Retries]**: Aantal e-mails in de wachtrij voor nieuwe pogingen.

* **[!UICONTROL Excluded]**: aantal profielen dat door Adobe Journey Optimizer is uitgesloten.

+++

### E-mail - Trackingstatistieken {#email-tracking}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_tracking_statistics"
>title="E-mail - Trackingstatistieken"
>abstract="De tabel E-mail - Statistische gegevens bijhouden bevat gegevens over profielactiviteiten voor uw e-mail."

![](assets/journey_email_tracking.png)

De tabel **[!UICONTROL Email - Tracking statistics]** bevat een gedetailleerd overzicht van de profielactiviteiten met betrekking tot e-mails die u onderweg hebt. Dit omvat cijfers over het openen, klikken en andere relevante betrokkenheidsindicatoren, die een uitgebreid overzicht bieden van hoe profielen met uw e-mailinhoud communiceren.

+++ Meer informatie over e-mail - statistieken over bijhouden

* **[!UICONTROL Execution time]**: Begintijd voor elke uitvoering van uw terugkerende e-mail op uw reis. Als u slechts één of meerdere terugkerende e-mails wilt aanwijzen, selecteert u deze in de vervolgkeuzelijst **[!UICONTROL Execution time]** .

* **[!UICONTROL Opens]**: Het aantal keren dat uw e-mails zijn geopend tijdens een rit.

* **[!UICONTROL Unique Opens]**: percentage geopende e-mailberichten.

* **[!UICONTROL Unique Open Rate]**: Het totale aantal geopende e-mails in verhouding tot het aantal geleverde e-mails.

* **[!UICONTROL Clicks]**: Het aantal keer dat er op de inhoud in uw e-mails is geklikt.

* **[!UICONTROL Unique Clicks]**:Aantal ontvangers die op een inhoud in uw e-mails hebben geklikt.

* **[!UICONTROL Click through rate]**: percentage gebruikers dat interactie had met de reis.

* **[!UICONTROL Unsubscriptions]**: Het aantal klikken op de koppeling voor het opzeggen van abonnementen.

* **[!UICONTROL Spam complaints]**: Het aantal keren dat uw e-mails zijn gedeclareerd als spam of junk.

+++

### E-mail - Prestaties verzenden {#email-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sending_performance"
>title="E-mail - Prestaties verzenden"
>abstract="De grafiek van de e-mail - Verzendende prestaties biedt uitvoerige gegevens betreffende verzonden E-mail, die inzicht in zeer belangrijke metriek zoals geleverde en staren, toestaat voor een gedetailleerde analyse van het proces van de e-maillevering."

![](assets/journey_email_performance.png)

De grafiek van **[!UICONTROL Email - Sending performance]** biedt een uitgebreide weergave van gegevens die betrekking hebben op verzonden e-mails tijdens uw reis en biedt inzicht in belangrijke metriek zoals geleverde gegevens en stuitingen. Dit maakt een gedetailleerde analyse van het verzendingsproces van e-mail mogelijk en biedt waardevolle informatie over de efficiëntie en prestaties van uw reizen.

+++ Meer informatie over e-mail - Prestatiegegevens verzenden

* **[!UICONTROL Delivered]**: Aantal verzonden e-mailberichten in verhouding tot het totale aantal verzonden e-mails.

* **[!UICONTROL Bounces]**: het totaal aan fouten dat tijdens het verzendproces is gecumuleerd en de automatische retourverwerking in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Retries]**: Aantal e-mails in de wachtrij voor nieuwe pogingen.

* **[!UICONTROL Errors]**: het totale aantal fouten dat is opgetreden tijdens het verzendingsproces waardoor het niet naar profielen kan worden verzonden.

+++

### E-mail - rubrieken en redenen voor stuiteren {#email-bounce-categories}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces"
>title="E-mail - rubrieken en redenen voor stuiteren"
>abstract="De e-mail - de categorieën en de motiegidwidgets verzamelen de gegevens betreffende valse berichten, die diepgaand inzicht in de specifieke redenen en de categorieën aanbieden die tot e-mailstuitingen bijdragen"

![](assets/journey_email_bounce_categories.png)

De widgets **[!UICONTROL Bounce Reasons]** en **[!UICONTROL Bounce categories]** compileren de beschikbare gegevens met betrekking tot verzonden berichten, die gedetailleerde inzichten verstrekken in de specifieke redenen en categorieën achter e-mailgrenzen.

Voor meer informatie over grenzen, verwijs naar de [ lijst van de Onderdrukking ](../reports/suppression-list.md) pagina.

+++ Meer informatie over e-mail - cijfers voor rubrieken voor sprongen

* **[!UICONTROL Hard bounce]**: Het totale aantal permanente fouten, zoals een onjuist e-mailadres. Dit omvat een foutbericht waarin expliciet wordt aangegeven dat het adres ongeldig is, zoals Onbekende gebruiker.

* **[!UICONTROL Soft bounce]**: Het totale aantal tijdelijke fouten, zoals een volledig Postvak IN.

* **[!UICONTROL Ignored]**: Het totale aantal tijdelijke bestanden, zoals Buiten-kantoor, of een technische fout, bijvoorbeeld als het type afzender postmaster is.

+++

### E-mail - Foutredenen {#email-errors}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_error_reasons"
>title="E-mail - Foutredenen"
>abstract="Met de grafieken en de tabel met redenen voor e-mail - Fout kunt u de specifieke fouten identificeren die tijdens het verzendingsproces zijn opgetreden."

![](assets/journey_email_error.png)

De **[!UICONTROL Error Reasons]** -grafieken en -tabel bieden zichtbaarheid in de specifieke fouten die tijdens het verzendingsproces zijn opgetreden en bieden waardevolle informatie over de aard en het optreden van fouten.

### E-mail - Uitgesloten redenen {#email-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_excluded_reasons"
>title="E-mail - Uitgesloten redenen"
>abstract="In de grafieken en de tabel met uitgesloten redenen worden de verschillende factoren weergegeven die hebben geleid tot gebruikersprofielen die zijn uitgesloten van het doelpubliek en die het bericht niet ontvangen."

![](assets/journey_email_excluded.png)

De grafieken en tabel van **[!UICONTROL Excluded reasons]** bevatten een uitgebreide weergave van de verschillende factoren die ertoe hebben geleid dat gebruikersprofielen zijn uitgesloten van het doelpubliek, waardoor het bericht niet is ontvangen.

Verwijs naar [ deze pagina ](exclusion-list.md) voor de uitvoerige lijst van uitsluitingsredenen.

### Verzonden en geleverd op domeinen {#sent-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sent_delivered_domains"
>title="Verzonden en geleverd op domeinen"
>abstract="De tabel Verzonden en geleverd door domeinen en de grafiek geven een uitsplitsing van e-mails per domein, waarin diepgaande inzichten in de algemene prestaties van uw e-mailcommunicatie worden getoond."

![](assets/journey_email_sent_domains.png)

De tabel en grafiek van **[!UICONTROL Sent & delivered by domains]** bevatten een gedetailleerde uitsplitsing van e-mails op domeinniveau, met uitgebreide inzichten in de prestaties van uw e-mails.

+++ Meer informatie over Verzonden en geleverde waarden per domein

* **[!UICONTROL Sent]**: Het totale aantal verzendingen voor uw e-mails.

* **[!UICONTROL Delivered]**: Aantal verzonden e-mailberichten in verhouding tot het totale aantal verzonden e-mails.

+++

### Openen en klikken op domeinen {#open-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_open_clicks_domains"
>title="Openen en klikken op domeinen"
>abstract="De grafiek en tabel Openen en klikken op domeinen bieden een gedetailleerde uitsplitsing op domeinniveau en bieden een uitgebreide weergave van hoe uw publiek met uw e-mailberichten werkt."

![](assets/journey_email_open_domains.png)

In de grafiek en tabel van **[!UICONTROL Open & clicks by domains]** ziet u een uitsplitsing op domeinniveau van de betrokkenheid van uw profielen bij uw e-mail. Zo krijgt u waardevolle inzichten in de manier waarop verschillende domeinen met uw inhoud werken.

+++ Meer informatie over Openen en klikken op domeinmetriek

* **[!UICONTROL Opens]**: Het aantal keren dat de e-mail is geopend.

* **[!UICONTROL Clicks]**: Het aantal keer dat er op inhoud is geklikt in een e-mail.

+++

### Stuitingen en fouten per domein {#bounces-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces_errors_domains"
>title="Stuitingen en fouten per domein"
>abstract="De grafiek en de lijst van Bounces &amp; van Fouten door Domains verstrekken een korrelige uitsplitsing op domeinniveau, die inzicht in specifieke fouten aanbieden die tijdens het e-mailverzendingsproces worden ontmoet."

![](assets/journey_email_bounce_domains.png)

De grafiek en de tabel van **[!UICONTROL Bounces & errors by domains]** bevatten een specificatie op domeinniveau van specifieke fouten die tijdens het verzendingsproces zijn aangetroffen. Hierin wordt een gedetailleerde analyse gegeven van de problemen die zich hebben voorgedaan.

+++ Meer informatie over grenzen en fouten per domeinmetriek

* **[!UICONTROL Bounces]**: het totaal aan fouten dat tijdens het verzendproces is gecumuleerd en de automatische retourverwerking in verhouding tot het totale aantal verzonden e-mails.

* **[!UICONTROL Errors]**: het totale aantal fouten dat is opgetreden tijdens het verzendproces waardoor het niet naar profielen kan worden verzonden.

+++

### Bounce reason by domain {#bounce-reasons-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces_reasons_domains"
>title="Bounces redenen per domein"
>abstract="De stuitredenen per domeingrafiek en tabel geven een indeling op domeinniveau met uitgebreide inzichten in zowel tijdelijke als permanente fouten. Deze gedetailleerde analyse geeft u waardevolle informatie over de specifieke redenen achter de berichten die worden aangekondigd."

![](assets/journey_email_bounce_reasons_domain.png)

De grafiek en de tabel van **[!UICONTROL Bounce reasons by domain]** bevatten een uitsplitsing op domeinniveau van gegevens die betrekking hebben op zowel tijdelijke als permanente fouten. Zo krijgt u gedetailleerde inzichten van de redenen die ten grondslag liggen aan aangekondigde berichten.

### E-mail - bovenste URL {#email-top}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_top_url"
>title="E-mail - bovenste URL"
>abstract="De grafiek en tabel E-mail - URL bovenaan bieden een uitgebreid overzicht van de URL&#39;s in uw e-mail die het hoogste bezoekersverkeer ontvangen, zodat u de populairste koppelingen kunt identificeren."

![](assets/journey_email_top.png)

De grafiek en tabel van **[!UICONTROL Email - Top Url]** bieden een uitgebreid overzicht van de URL&#39;s in uw e-mail die het hoogste bezoekersverkeer aantrekken. Hierdoor kunt u de populairste koppelingen identificeren en er prioriteiten aan stellen, zodat u meer inzicht krijgt in de betrokkenheid bij profielen met specifieke inhoud in uw e-mails.

### E-mail - Optimalisatie {#email-sto}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_optimization"
>title="E-mail - Optimalisatie"
>abstract="De optimalisatie voor de verzendtijd en de geoptimaliseerde en niet-geoptimaliseerde widgets bieden gedetailleerde informatie over uw berichten en geven aan of deze zijn geoptimaliseerd of niet."

![](assets/journey_email_sto.png)

>[!NOTE]
>
>De widgets **[!UICONTROL Send time optimization]** en **[!UICONTROL Optimized vs non optimized]** zijn alleen beschikbaar als de optie Send-Time Optimization is geactiveerd voor de levering. Voor meer informatie over Send-Time Optimalisering, verwijs naar [ deze pagina ](../building-journeys/journeys-message.md#send-time-optimization).

De widgets **[!UICONTROL Send time optimization]** en **[!UICONTROL Optimized vs non optimized]** geven een gedetailleerd overzicht van het succes van uw e-mails, afhankelijk van de verzendmethode: geoptimaliseerd of normaal.

+++ Meer informatie over optimalisatie van de verzendtijd en geoptimaliseerde versus niet-geoptimaliseerde meetgegevens

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.
* **[!UICONTROL Bounces]**: het totaal aan fouten dat tijdens het verzendproces is gecumuleerd en de automatische retourverwerking in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Sent]**: Het totale aantal e-mails dat is verzonden voor de reis.

* **[!UICONTROL Opens]**: Het aantal keren dat uw e-mails zijn geopend tijdens de reis.

* **[!UICONTROL Clicks]**: Het aantal keer dat er op de inhoud in uw e-mails is geklikt.

+++

### E-mail - voorstellen {#email-offers}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_offers"
>title="E-mail - voorstellen"
>abstract="De statistische en gedetailleerde statistische widgets van de Aanbiedingen verstrekken uitvoerige inzichten in de prestaties van uw aanbiedingen, die een gedetailleerde analyse van hun effect in tijd aanbieden en gedetailleerde statistieken voor een meer diepgaand begrip presenteren."

>[!NOTE]
>
>De widgets en cijfers voor aanbiedingen zijn alleen beschikbaar als een beslissing in een e-mail is ingevoegd. Voor meer informatie over het Beheer van het Besluit, verwijs naar deze [ pagina ](../offers/get-started/starting-offer-decisioning.md).

Met de widgets **[!UICONTROL Offers statistic]** en **[!UICONTROL Offers detailed statistic]** in de tijd kunt u meten wat het succes van uw aanbieding is en wat de invloed ervan is op uw doelgroep. Het detailleert de belangrijkste informatie met betrekking tot uw bericht met KPIs.

+++ Meer informatie over e-mail - Metriek van aanbiedingen

* **[!UICONTROL Offer sent]**: Het totale aantal verzendingen voor de aanbieding.

* **[!UICONTROL Offer impression]**: Het aantal keren dat het voorstel in uw e-mail is geopend.

* **[!UICONTROL Offer clicks]**: Het aantal keren dat er op een voorstel is geklikt in uw e-mails.

* **[!UICONTROL Placement name]**: naam van de plaatsing die u hebt gebruikt om uw voorstel weer te geven. Voor meer informatie over plaatsing, verwijs naar deze [ pagina ](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Offer name]**: naam van de aanbieding die in uw e-mails is toegevoegd. Voor meer informatie over plaatsing, verwijs naar deze [ pagina ](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offer sent]**: Het totale aantal verzendingen voor de aanbieding.

* **[!UICONTROL Offer impression rate]**: percentage geopende voorstellen in verhouding tot het aantal verzonden voorstellen.

* **[!UICONTROL Offer click rate]**: percentage gebruikers dat interactie heeft gehad met de aanbieding.

+++

## Tabblad Pushmelding {#push-global}

Vanaf uw reis **[!UICONTROL Global report]** bevat het tabblad **[!UICONTROL Push notification]** de belangrijkste informatie met betrekking tot de pushberichten die tijdens uw reis worden verzonden.

### Pushmelding - Statistieken verzenden {#push-sending-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_sending_statistics"
>title="Pushmelding - Statistieken verzenden"
>abstract="De lijst van het Verzenden van de Statistieken van het Bericht van de Duw vat essentiële gegevens over uw dupberichten zoals Gerichte of Geleide berichten samen."

![](assets/journey_push_sending.png)

De tabel **[!UICONTROL Push notification - Sending statistics]** bevat een beknopte samenvatting van de belangrijkste gegevens die betrekking hebben op uw pushberichten, waaronder belangrijke gegevens zoals het aantal gerichte berichten en het aantal succesvol afgeleverde berichten.

+++ Meer informatie over pushmeldingen - Statistische gegevens verzenden

* **[!UICONTROL Execution time]**: Begintijd van elke uitvoering van de reis in het geval van terugkerende reizen. Als u slechts één of meerdere herhalingen als doel wilt instellen, selecteert u deze in de vervolgkeuzelijst **[!UICONTROL Execution time]** .

* **[!UICONTROL Targeted]**: Het aantal profielen waarvoor een actie wordt uitgevoerd, zoals het verzenden van e-mail of sms.

* **[!UICONTROL Sent]**: Het totale aantal verzonden pushberichten.

* **[!UICONTROL Delivered]**: Het aantal pushmeldingen dat is verzonden, in verhouding tot het totale aantal verzonden pushmeldingen.

* **[!UICONTROL Delivery Rate]**: percentage pushberichten dat is verzonden.

* **[!UICONTROL Bounces]**: het totaal aan fouten dat tijdens het verzendproces is gecumuleerd en de automatische retourverwerking in verhouding tot het totale aantal verzonden pushberichten.

* **[!UICONTROL Bounce Rate]**: percentage pushmeldingen dat is teruggestuurd in vergelijking met verzonden pushberichten.

* **[!UICONTROL Errors]**: het totale aantal fouten dat is opgetreden tijdens het verzendproces waardoor het niet naar profielen kan worden verzonden.

* **[!UICONTROL Error Rate]**: percentage fouten dat is opgetreden tijdens het verzendproces waardoor het niet kan worden verzonden, vergeleken met verzonden pushberichten.

* **[!UICONTROL Excluded]**: aantal profielen dat door Adobe Journey Optimizer is uitgesloten.

+++

### Pushmeldingen - Statistieken bijhouden {#push-tracking-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_tracking_statistics"
>title="Pushmeldingen - Statistieken bijhouden"
>abstract="De statistieken van het Spoor van de Duw verstrekken gegevens over profielactiviteit voor uw dupmelding."

De **[!UICONTROL Push - Tracking statistics]** -widget biedt een gedetailleerde momentopname van profielactiviteiten die aan uw pushberichten zijn gekoppeld, en biedt essentiële inzichten in de doeltreffendheid van betrokkenheid en pushberichten.

+++ Meer informatie over pushmeldingen - statistieken bijhouden

* **[!UICONTROL Execution time]**: Begintijd van elke uitvoering van de reis in het geval van terugkerende reizen. Als u slechts één of meerdere herhalingen als doel wilt instellen, selecteert u deze in de vervolgkeuzelijst **[!UICONTROL Execution time]** .

* **[!UICONTROL Opens]**: Het aantal keren dat uw pushberichten tijdens de rit zijn geopend.

* **[!UICONTROL Actions]**: Totaal aantal acties voor de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

+++

### Pushmelding - Samenvatting verzenden {#push-summary}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_sending_summary"
>title="Pushmelding - Samenvatting verzenden"
>abstract="In de grafiek Samenvatting van pushberichten wordt aangegeven welke gegevens beschikbaar zijn voor verzonden pushberichten."

![](assets/journey_push_summary.png)

De grafiek van **[!UICONTROL Push notification - Sending summary]** biedt een dynamische vertegenwoordiging, die een analyse van uw activiteit van pushberichten toont. Deze grafische weergave biedt een uitgebreide uitsplitsing van verzonden pushberichten.

+++ Meer informatie over pushmeldingen - Samenvattingscijfers verzenden

* **[!UICONTROL Opens]**: Het aantal keren dat uw pushberichten tijdens de rit zijn geopend.

* **[!UICONTROL Actions]**: Totaal aantal acties voor de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

* **[!UICONTROL Bounces]**: het totaal aan fouten dat tijdens het verzendproces is gecumuleerd en de automatische retourverwerking in verhouding tot het totale aantal verzonden pushberichten.

* **[!UICONTROL Delivered]**: Het aantal pushmeldingen dat is verzonden, in verhouding tot het totale aantal verzonden pushmeldingen.

* **[!UICONTROL Errors]**: het totale aantal fouten dat is opgetreden tijdens het verzendproces waardoor het niet naar profielen kan worden verzonden.

+++

### Pushmelding - Foutredenen {#push-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_error_reasons"
>title="Pushmelding - Foutredenen"
>abstract="Met de grafieken en de tabel met oorzaken van fouten kunt u de specifieke fouten identificeren die tijdens het verzendingsproces zijn opgetreden"

![](assets/journey_push_error.png)

De **[!UICONTROL Error Reasons]** -tabel en -grafieken bieden u de mogelijkheid om de specifieke fouten te identificeren die zijn opgetreden tijdens het verzenden van uw pushberichten. Zo krijgt u gedetailleerde informatie over eventuele problemen die onderweg zijn opgetreden.

### Pushmelding - Uitgesloten redenen {#push-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_excluded_reasons"
>title="Pushmelding - Uitgesloten redenen"
>abstract="In de grafieken en tabel met uitgesloten redenen worden de verschillende factoren weergegeven die hebben verhinderd dat gebruikersprofielen, die zijn uitgesloten van het doelpubliek, het bericht ontvingen."

![](assets/journey_push_excluded.png)

In de grafieken en tabel van **[!UICONTROL Excluded reasons]** ziet u de verschillende redenen waarom gebruikersprofielen, die zijn uitgesloten van de doelprofielen, uw pushberichten niet hebben ontvangen.

Verwijs naar [ deze pagina ](exclusion-list.md) voor de uitvoerige lijst van uitsluitingsredenen.

### Pushmelding - Onderverdeling per platform {#push-breakdown}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_breakdown_platform"
>title="Pushmelding - Onderverdeling per platform"
>abstract="De pushmelding - Uitsplitsing naar platformgrafieken en tabel geeft een overzicht van het succes van uw pushberichten op basis van het besturingssysteem van het profiel."

![](assets/journey_push_breakdown.png)

De grafiek en tabel van **[!UICONTROL Breakdown by platform]** bieden een gedetailleerde analyse van het succes van uw pushberichten en bieden inzichten op basis van het besturingssysteem van uw profiel. Deze ineenstorting verbetert uw inzicht in hoe goed uw pushberichten op verschillende platforms presteren.

### Pushmelding - Optimalisatie {#push-sto}

>[!NOTE]
>
>De widgets **[!UICONTROL Optimized vs non optimized]** en **[!UICONTROL Send time optimization]** zijn alleen beschikbaar als de optie Send-Time Optimization is geactiveerd voor de levering. Voor meer informatie over Send-Time Optimalisering, verwijs naar [ deze pagina ](../building-journeys/journeys-message.md#send-time-optimization).

In de widgets **[!UICONTROL Optimized vs non optimized]** en **[!UICONTROL Send time optimization]** worden de belangrijkste gegevens met betrekking tot uw bericht gedetailleerd, ongeacht of ze zijn geoptimaliseerd of niet.

+++ Meer informatie over pushmeldingen - Optimalisatiegegevens

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Opens]**: Het aantal keren dat uw pushberichten tijdens de rit zijn geopend.

* **[!UICONTROL Actions]**: Totaal aantal acties voor de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounces]**: het totaal aan fouten dat tijdens het verzendproces is gecumuleerd en de automatische retourverwerking in verhouding tot het totale aantal verzonden berichten.

+++

## Tabblad SMS {#sms-global}

### SMS - Statistieken verzenden {#sms-sending-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_sending_statistics"
>title="SMS - Statistieken verzenden"
>abstract="De sms - Verzendende lijst van Statistieken vat essentiële gegevens over uw SMS berichten zoals Gerichte of Geleide berichten samen."

![](assets/journey_sms_sending.png)

De tabel **[!UICONTROL SMS - Sending statistics]** bevat een beknopte samenvatting van essentiële gegevens over uw SMS-berichten, die belangrijke gegevens bevat, zoals het aantal gerichte berichten en het aantal berichten dat met succes is verzonden.

+++ Meer informatie over SMS - Statistische gegevens verzenden

* **[!UICONTROL Execution time]**: Begintijd van elke uitvoering van de reis in het geval van terugkerende reizen. Als u slechts één of meerdere herhalingen als doel wilt instellen, selecteert u deze in de vervolgkeuzelijst **[!UICONTROL Execution time]** .

* **[!UICONTROL Targeted]**: Aantal gebruikersprofielen dat in aanmerking komt als doelprofielen voor uw SMS-berichten.

* **[!UICONTROL Excluded]**: Aantal gebruikersprofielen dat is uitgesloten van de doelprofielen en dat uw SMS-berichten niet heeft ontvangen.

* **[!UICONTROL Sent]**: Het totale aantal SMS-berichten dat voor de reis is verzonden.

* **[!UICONTROL Bounces]**: het totaal aan fouten dat tijdens het verzendproces is gecumuleerd en de automatische retourverwerking in verhouding tot het totale aantal verzonden SMS-berichten.

* **[!UICONTROL Errors]**: het totale aantal fouten dat is opgetreden tijdens het verzendproces waardoor het niet naar profielen kan worden verzonden.

+++

### SMS - Trackingstatistieken {#sms-tracking-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_tracking_statistics"
>title="SMS - Trackingstatistieken"
>abstract="De widget statistieken voor sms - bijhouden biedt een uitgebreid overzicht van essentiële informatie over de interactie van uw bezoekers met uw URL."

![](assets/journey_sms_tracking.png)

De **[!UICONTROL SMS - Tracking statistics]** -widget biedt een gedetailleerd overzicht van belangrijke informatie over de betrokkenheid van uw bezoekers bij uw URL&#39;s en biedt inzichten in de effectiviteit van uw SMS-berichten.

* **[!UICONTROL Execution time]**: Begintijd voor elke uitvoering van uw terugkerende SMS. Als u slechts één of meerdere terugkerende SMS-berichten als doel wilt instellen, selecteert u deze in de vervolgkeuzelijst **[!UICONTROL Execution time]** .

* **[!UICONTROL Clicks]**: Het aantal keer dat er op de inhoud in uw SMS-berichten is geklikt.

### SMS - Prestaties op datum {#sms-performance-date}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_perfomance_date"
>title="SMS - Prestaties op datum"
>abstract="De widget SMS - Prestaties op datum biedt via een grafische weergave belangrijke informatie over uw berichten."

![](assets/journey_sms_performance.png)

De **[!UICONTROL SMS - Performance by date]** -widget biedt een gedetailleerd overzicht van belangrijke informatie met betrekking tot uw berichten, weergegeven in een grafiek, die inzicht biedt in de prestatietrends gedurende specifieke tijdsperioden.

+++ Meer informatie over SMS - Prestaties op basis van datum

* **[!UICONTROL Sent]**: Totaal aantal SMS-berichten dat voor de reis is verzonden

* **[!UICONTROL Bounces]**: het totaal aan fouten dat tijdens het verzendproces is gecumuleerd en de automatische retourverwerking in verhouding tot het totale aantal verzonden SMS-berichten.

* **[!UICONTROL Errors]**: het totale aantal fouten dat is opgetreden tijdens het verzendproces waardoor het niet naar profielen kan worden verzonden.

+++

### SMS - Bounges redenen {#sms-bounce}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_bounces_reasons"
>title="SMS - Bounges redenen"
>abstract="De grafieken en de tabel met Bounces Reasons bevatten de beschikbare gegevens met betrekking tot berichten die worden teruggestuurd."

![](assets/journey_sms_bounce_reasons.png)

De **[!UICONTROL Bounces Reasons]** -grafieken en -tabel bieden een uitgebreid overzicht van gegevens met betrekking tot verzonden SMS-berichten, waarmee u waardevolle inzichten krijgt over de specifieke redenen achter sms-berichten.

### SMS - Redenen voor fouten {#sms-error}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_error_reasons"
>title="SMS - Redenen voor fouten"
>abstract="Met SMS - Foutgrafieken en -tabel kunt u de specifieke fouten identificeren die tijdens het verzendingsproces zijn opgetreden."

![](assets/journey_sms_error.png)

Met de grafieken en de tabel van **[!UICONTROL Error Reasons]** kunt u de specifieke fouten identificeren die zijn opgetreden tijdens het verzenden van uw SMS-berichten. Zo kunt u een grondige analyse maken van alle ondervonden problemen.

### SMS - Uitgesloten redenen {#sms-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_excluded_reasons"
>title="SMS - Uitgesloten redenen"
>abstract="In de grafieken en de tabel met uitgesloten redenen worden de verschillende factoren weergegeven die hebben geleid tot gebruikersprofielen die zijn uitgesloten van het doelpubliek en die het bericht niet ontvangen."

![](assets/journey_sms_excluded.png)

In de grafieken en tabel van **[!UICONTROL Excluded Reasons]** worden visueel de verschillende factoren weergegeven die ertoe hebben geleid dat gebruikersprofielen zijn uitgesloten van het doelpubliek, zodat gebruikers uw SMS-berichten niet kunnen ontvangen.

Verwijs naar [ deze pagina ](exclusion-list.md) voor de uitvoerige lijst van uitsluitingsredenen.

### SMS - Klikken op koppelingen {#sms-clicks}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_clicks"
>title="SMS - Klikken op koppelingen"
>abstract="SMS - De widget klikt op koppelingen biedt essentiële inzichten in de betrokkenheid van uw bezoekers bij de URL&#39;s in uw berichten."

![](assets/journey_sms_clicks.png)

De **[!UICONTROL SMS - Clicks by links]** -widget biedt essentiële inzichten in de betrokkenheid van uw bezoekers bij de URL&#39;s die in uw berichten zijn opgenomen en biedt waardevolle informatie over welke koppelingen de meeste interactie aantrekken.

## Tabblad In-app {#in-app-global}

Vanaf uw reis **[!UICONTROL Global report]** bevat het tabblad **[!UICONTROL In-app]** de belangrijkste informatie met betrekking tot de in-app-berichten die tijdens uw reizen worden verzonden.

### Prestaties in de app {#inapp-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_performance"
>title="Prestaties in de app"
>abstract="De prestatie-KPI&#39;s in de app bieden essentiële inzichten in de betrokkenheid van uw bezoekers bij In-app-berichten."

![](assets/journey_inapp_performance.png)

De KPI&#39;s van **[!UICONTROL In-app performance]** bieden essentiële inzichten in de betrokkenheid van uw profielen bij In-app-berichten. Deze bieden essentiële meetgegevens om de effectiviteit en impact van de in-app-berichten die tijdens uw reis worden geleverd, te beoordelen.

+++ Meer informatie over In-app - Prestaties op basis van datum

* **[!UICONTROL Unique impressions]**: aantal unieke gebruikers aan wie het In-app-bericht is weergegeven.

* **[!UICONTROL Impressions]**: het totale aantal In-app-berichten dat aan alle gebruikers wordt weergegeven.

  >[!NOTE]
  >
  >Om ervoor te zorgen dat een indruk wordt geteld, moet de gebruiker aan twee criteria voldoen:
  >* Kwalificatie binnen de In-app ervaring, die door de specifieke In-app activiteit tijdens hun reis wordt bereikt.
  >* Voldoen aan de voorwaarden die zijn opgegeven in de triggerregels.
  > 
  >Als gevolg van het tweede criterium kunnen er aanzienlijke verschillen zijn tussen het aantal doelprofielen en het aantal unieke indrukkingen.

* **[!UICONTROL Interaction]**: aantal contracten met uw In-app-bericht. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken, ontslag of andere interactie.
+++

### Overzicht in de app {#inapp-summary}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_summary"
>title="Overzicht in de app"
>abstract="De overzichtsgrafiek in de app illustreert de voortgang van uw impressies en interacties in de app gedurende de opgegeven periode."

![](assets/journey_inapp_summary.png)

De grafiek van **[!UICONTROL In-app summary]** illustreert de vooruitgang van uw in-app beelden en interactie over de gespecificeerde periode, die een uitvoerig overzicht van uw in-app berichtprestaties verstrekken.

### Interacties per type {#interactions-type}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_interactions"
>title="Interacties per type"
>abstract="De interacties per type grafieken en de lijstdetails hoe de gebruikers met uw in-app bericht in wisselwerking stonden door om het even welke klik te volgen, te ontslaan, of interactie."

![](assets/journey_inapp_interactions.png)

In de grafieken en tabel van **[!UICONTROL Interactions by type]** vindt u een gedetailleerd overzicht van de interactie tussen profielen en uw bericht in de app. Zo kunt u acties zoals klikken, ontslag of andere vormen van betrokkenheid volgen.
