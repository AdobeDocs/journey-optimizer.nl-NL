---
solution: Journey Optimizer
product: journey optimizer
title: Campagne Global-rapport
description: Leer hoe u gegevens uit het rapport Campagne Global kunt gebruiken
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: d26dbebaf36241d0e91c36c95f83ce6cf712ecee
workflow-type: tm+mt
source-wordcount: '4293'
ht-degree: 0%

---

# Globaal verslag campagne voeren {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="Globaal verslag campagne voeren"
>abstract="Met het algemene rapport Campagne kunt u het effect van uw campagnes over een bepaalde tijdsperiode meten. Uw rapport is verdeeld in verschillende widgets waarin het succes en de fouten van uw campagne worden beschreven. Elk rapportdashboard kan worden gewijzigd door widgets te vergroten of te verkleinen of te verwijderen."

Algemene rapporten, toegankelijk via de **Alle tijd** weergegeven, gebeurtenissen die ten minste twee uur geleden hebben plaatsgevonden en gebeurtenissen gedurende een geselecteerde tijdsperiode bedekken. In vergelijking hiermee richten Live-rapporten zich op gebeurtenissen die zich in de afgelopen 24 uur hebben voorgedaan, met een minimale tijdsinterval van twee minuten vanaf het plaatsvinden van de gebeurtenis.

Het algemene rapport van de campagne kan direct van uw Campagne met worden betreden **[!UICONTROL View report]** knop.

![](assets/campaign_report_global_5.png)

De campagne **[!UICONTROL Global report]** Deze pagina wordt weergegeven met de volgende tabbladen:

* [Campaign](#campaign-global)
* [Email](#email-global)
* [In-app](#inapp-global)
* [Push](#push-global)
* [Sms](#sms-global)
* [Web](#web-tab)
* [Direct mail](#direct-mail-global)

De campagne **[!UICONTROL Global report]** is verdeeld in verschillende widgets waarin het succes en de fouten van uw campagne worden beschreven. Elke widget kan indien nodig worden vergroot of verkleind en verwijderd. Raadpleeg voor meer informatie hierover [sectie](../reports/global-report.md#modify-dashboard).

Voor een gedetailleerde lijst van elke metrisch beschikbaar in Adobe Journey Optimizer, verwijs naar [deze pagina](global-report.md#list-of-components-global.md)

## Tabblad Campagne {#campaign-global}

### Levering {#delivery-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_delivery_global"
>title="Statistieken van de campagne"
>abstract="De widget Statistieken van de campagne bevat de belangrijkste informatie met betrekking tot uw campagne, zoals de ingevoerde profielen en acties."

![](assets/campaign_report_global_1.png)

De **[!UICONTROL Campaign's Statistics]** KPI&#39;s fungeren als een uitgebreid dashboard met een gedetailleerde uitsplitsing van de belangrijkste maatstaven voor uw campagne. Dit omvat essentiële informatie zoals het aantal profielen en de geleverde acties, die een grondig inzicht in de prestaties en de betrokkenheid van uw campagne verstrekken.

+++ Meer informatie over statistische gegevens van campagne

* **[!UICONTROL Audience]**: Aantal doelprofielen.

* **[!UICONTROL Actions delivered]**: Het totale aantal unieke tijden dat een handeling is uitgevoerd.

* **[!UICONTROL Actions failed in %]**: Percentage unieke tijden dat een actie is mislukt in verhouding tot het totale aantal unieke tijden dat een actie is uitgevoerd.

+++

<!--
### Objectives report {#objectives-global}

![](assets/performance_report.gif)

The **[!UICONTROL Objectives]** tab allows you to better fine-tune your deliveries' reports by targeting one specific metric.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of built-in **[!UICONTROL Objectives]** is available but you can add your own by adding new **[!UICONTROL Dataset]**. For the detailed procedure, refer to this [section](../campaigns/reporting-configuration.md).

After selecting the Objectives you want to target on, the two **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets will provide a detailed summary of your delivery performance. 

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your main objective with another metric.
-->

### Experimentatierapport {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Metrisch met succes"
>abstract="De totale waarde van de metrische waarde van het Succes, eerder geselecteerd toen het creëren van uw Experimenten, gedeeld door het aantal profielen."

![](assets/experimentation_report_3.png)

De **[!UICONTROL Experimentation]** tab geeft belangrijke inzichten in de prestaties van elke variant en geeft de meest succesvolle variant aan.

Het kan enige tijd duren om de beste uitvoerder te definiëren. Dit pictogram geeft dit weer. ![](assets/experimentation_report_1.png).

+++Leer meer over de verschillende metriek en widgets beschikbaar voor het rapport van de Experimentatie.

De **[!UICONTROL Experiment result]** widget geeft de prestaties van elke variant weer. U kunt uw basislijn wijzigen door een van de behandelingen te kiezen in het menu **[!UICONTROL Baseline]** de vervolgkeuzelijst. De beste behandeling wordt weergegeven met een sterpictogram.

Raadpleeg voor een diepgaande analyse van deze resultaten en de manier waarop u deze kunt interpreteren de volgende bronnen: [deze pagina](../campaigns/get-started-experiment.md#interpret-results).

De tabel bevat de volgende cijfers:

* **[!UICONTROL Lift over baseline]**: Meting van de procentuele verbetering van de conversiesnelheid van een bepaalde behandeling ten opzichte van de uitgangswaarde.

* **[!UICONTROL Confidence]**: Bewijs dat een bepaalde behandeling gelijk is aan de basisbehandeling. [Meer informatie](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Unique outbound clicks]**: Totaal aantal klikken over uitgaande kanalen.

* **[!UICONTROL Profiles]**: Aantal profielen waarop deze behandeling is gericht.

* **[!UICONTROL Unique outbound clicks/profiles]**: De totale waarde van de metrische waarde voor succes die eerder is geselecteerd bij het maken van uw experimenten, gedeeld door het aantal profielen.

De **[!UICONTROL Confidence interval]** in grafiek wordt de onzekerheid over de verbetering gemeten . Het geeft het procentuele verschil in prestaties weer tussen de basislijn en de best presterende behandeling. [Meer informatie](../campaigns/experiment-calculations.md#confidence-intervals).

![](assets/experimentation_report_4.png)

De laatste widget bevat gegevens die betrekking hebben op de **[!UICONTROL Success metric]** u eerder voor uw Behandelingen hebt geselecteerd. U kunt een andere doelmetrische waarde selecteren in het menu **[!UICONTROL Metric]** vervolgkeuzelijst voor het bijhouden van alternatieve gegevens.

>[!CAUTION]
>
>Wanneer u werkt met gefilterde meetgegevens voor experimenteren, moet u er rekening mee houden dat als u de optie Metrisch in het keuzemenu op de vergelijkingspagina voor experimenteren wijzigt, de filterwaarde niet behouden blijft. Als u bijvoorbeeld van &quot;Kliks&quot; overschakelt op &quot;Unieke klikken&quot;, gaat het toegepaste filter verloren, waardoor de vergelijking onjuist of ongeldig wordt.

+++

## Tabblad E-mail {#email-global}

### E-mail - Statistieken verzenden {#sending-statistics-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_statistics"
>title="E-mail - Statistieken verzenden"
>abstract="De tabel E-mail - Statistieken verzenden bevat een overzicht van de belangrijkste gegevens over uw e-mail, zoals Gericht of bezorgd."

![](assets/campaign_email_sending.png)

De **[!UICONTROL Email Sending Statistics]** de lijst verstrekt een uitvoerige samenvatting van essentiële gegevens betreffende uw e-mailcampagnes. Het bevat belangrijke metriek, zoals de grootte van het beoogde publiek en het aantal e-mails dat succesvol is geleverd. Het biedt waardevolle inzichten in de effectiviteit en het bereik van uw e-mails.

+++ Meer informatie over statistieken over verzendstatistieken per e-mail

* **[!UICONTROL Targeted]**: Het totale aantal e-mailberichten dat tijdens het verzendproces is verwerkt.

* **[!UICONTROL Sent]**: Totaal aantal verzendingen voor uw e-mail.

* **[!UICONTROL Delivered]**: Aantal verzonden e-mailberichten in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Delivery Rate]**: Percentage verzonden e-mailberichten.

* **[!UICONTROL Bounces]**: Totaal aan fouten gecumuleerd tijdens het verzendingsproces en automatische retourverwerking in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounce Rate]**: Percentage van e-mails dat is teruggestuurd in vergelijking met verzonden e-mails.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens het verzendproces waardoor het niet naar profielen kan worden verzonden.

* **[!UICONTROL Error Rate]**: Percentage fouten dat is opgetreden tijdens het verzendproces waardoor het niet kan worden verzonden, vergeleken met verzonden e-mailberichten.

* **[!UICONTROL Retries]**: Aantal e-mails in de wachtrij voor nieuwe pogingen.

* **[!UICONTROL Excluded]**: Aantal profielen dat door Adobe Journey Optimizer is uitgesloten.

+++

### E-mail - Trackingstatistieken {#tracking-statistics-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_tracking_statistics"
>title="E-mail - Trackingstatistieken"
>abstract="De tabel E-mail - Statistische gegevens bijhouden bevat gegevens over profielactiviteiten voor uw e-mail."

![](assets/campaign_email_tracking.png)

De **[!UICONTROL Email - Tracking statistics]** tabel bevat een gedetailleerd overzicht van de profielactiviteiten die betrekking hebben op uw e-mailcampagnes. Dit omvat cijfers over het openen, klikken en andere relevante betrokkenheidsindicatoren, die een uitgebreid overzicht bieden van hoe profielen met uw e-mailinhoud communiceren.

+++ Meer informatie over e-mail - statistieken bijhouden

* **[!UICONTROL Opens]**: Aantal keer dat de e-mail is geopend.

* **[!UICONTROL Unique Opens]**: Percentage geopende e-mails.

* **[!UICONTROL Open Rate]**: Het totale aantal geopende e-mails in verhouding tot het aantal geleverde e-mails.

* **[!UICONTROL Clicks]**: Het aantal keren dat er op de inhoud in uw e-mails is geklikt.

* **[!UICONTROL Unique Clicks]**: Aantal profielen dat op de inhoud van een e-mail heeft geklikt.

* **[!UICONTROL Unique Click Rate]**: Percentage gebruikers dat interactie heeft gehad met uw e-mails.

* **[!UICONTROL Unsubscriptions]**: Het aantal klikken op de koppeling voor het opzeggen van abonnementen.

* **[!UICONTROL Spam complaints]**: Het aantal keren dat een bericht is gedeclareerd als spam of junk.

+++

### E-mail - Prestaties verzenden {#sending-performance-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_performance"
>title="E-mail - Prestaties verzenden"
>abstract="De grafiek van de e-mail - Verzendende prestaties biedt uitvoerige gegevens betreffende verzonden E-mail, die inzicht in zeer belangrijke metriek zoals geleverde en staren, toestaat voor een gedetailleerde analyse van het proces van de e-maillevering."

![](assets/campaign_email_sending_performance.png)

De **[!UICONTROL Email - Sending Performance]** in grafiek vindt u een uitgebreide weergave van gegevens over verzonden e-mailberichten met inzichten in belangrijke meetgegevens zoals geleverde gegevens en stuitingen. Dit maakt een gedetailleerde analyse van het verzendingsproces van e-mail mogelijk en biedt waardevolle informatie over de efficiëntie en prestaties van uw e-mailcampagnes.

+++ Meer informatie over e-mail - Prestatiegegevens verzenden

* **[!UICONTROL Delivered]**: Aantal verzonden e-mails in verhouding tot het totale aantal verzonden e-mails.

* **[!UICONTROL Bounces]**: Totaal aantal fouten gecumuleerd tijdens het verzendproces en automatische retourverwerking in verhouding tot het totale aantal verzonden e-mails.

* **[!UICONTROL Retries]**: Aantal e-mails in de wachtrij voor nieuwe pogingen.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens het verzendproces waardoor het niet naar profielen kan worden verzonden.

+++

### E-mail - Oproepredenen en -rubrieken {#bounces-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_categories"
>title="E-mail - Bounce-categorieën"
>abstract="De categorieën E-mail - Stuiteren grafieken en tabel bieden gegevens over zowel tijdelijke als permanente fouten."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_reasons"
>title="E-mail - Bounges redenen"
>abstract="De grafieken en tabel met redenen voor e-mail - Bounces bevatten de beschikbare gegevens met betrekking tot teruggestuurde berichten."

![](assets/campaign_email_bounces.png)

De **[!UICONTROL Email - Bounce Reasons]** en **[!UICONTROL Email - Bounce categories]** widgets compileren de beschikbare gegevens met betrekking tot teruggestuurde berichten , zodat ze gedetailleerde informatie kunnen krijgen over de specifieke redenen en categorieën achter e - mailberichten .

Voor meer informatie over grenzen raadpleegt u de [Onderdrukkingslijst](../reports/suppression-list.md) pagina.

+++ Meer informatie over e-mail - cijfers voor rubrieken voor sprongen

* **[!UICONTROL Hard bounce]**: Het totale aantal permanente fouten, zoals een onjuist e-mailadres. Dit omvat een foutbericht waarin expliciet wordt aangegeven dat het adres ongeldig is, zoals Onbekende gebruiker.

* **[!UICONTROL Soft bounce]**: Het totale aantal tijdelijke fouten, zoals een volledig postvak.

* **[!UICONTROL Ignored]**: Het totale aantal tijdelijke berichten, zoals Buiten-kantoor, of een technische fout, bijvoorbeeld als het type afzender postmaster is.

+++


### E-mail - Foutredenen {#errors-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_error_reasons"
>title="E-mail - Foutredenen"
>abstract="Met de grafieken en de tabel met redenen voor e-mail - Fout kunt u de specifieke fouten identificeren die tijdens het verzendingsproces zijn opgetreden."

![](assets/campaign_email_error_reasons.png)

De **[!UICONTROL Error Reasons]** grafieken en tabellen bieden zichtbaarheid in de specifieke fouten die tijdens het verzendingsproces zijn opgetreden, zodat u waardevolle informatie kunt krijgen over de aard en het optreden van fouten.

U kunt ervoor kiezen om te schakelen van een tabel, staafdiagram of donut.

### E-mail - Uitgesloten redenen {#excluded-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_excluded_reasons"
>title="E-mail - Uitgesloten redenen"
>abstract="In de grafieken en de tabel met uitgesloten redenen worden de verschillende factoren weergegeven die hebben geleid tot gebruikersprofielen die zijn uitgesloten van het doelpubliek en die het bericht niet ontvangen."

![](assets/campaign_email_excluded.png)

De **[!UICONTROL Excluded reasons]** in grafieken en tabellen wordt een uitgebreid overzicht gegeven van de verschillende factoren die ertoe hebben geleid dat gebruikersprofielen van het beoogde publiek zijn uitgesloten, waardoor het bericht niet is ontvangen.

Zie [deze pagina](exclusion-list.md) voor de volledige lijst van uitsluitingsredenen.

### Verzonden en geleverd op domeinen {#sent-domains}

![](assets/campaign_email_sent_domains.png)

De  **[!UICONTROL Sent & delivered by domains]** tabel en grafiek geven een gedetailleerde uitsplitsing van e-mails op domeinniveau, zodat u uitgebreide inzichten kunt krijgen in de prestaties van uw e-mails.

+++ Meer informatie over Verzonden en geleverde waarden per domein

* **[!UICONTROL Sent]**: Totaal aantal verzendingen voor uw e-mail.

* **[!UICONTROL Delivered]**: Aantal verzonden e-mails in verhouding tot het totale aantal verzonden e-mails.

+++

### Stuitingen en fouten per domein {#bounces-domains}

![](assets/campaign_email_bounce_domains.png)

De  **[!UICONTROL Bounces & errors by domains]** de grafiek en de lijst verstrekken een domein-vlakke uitsplitsing van specifieke fouten die tijdens het verzendende proces worden ontmoet, die een gedetailleerde analyse van kwesties verstrekken die voorkwamen.

+++ Meer informatie over grenzen en fouten per domeinmetriek

* **[!UICONTROL Bounces]**: Totaal aantal fouten gecumuleerd tijdens het verzendproces en automatische retourverwerking in verhouding tot het totale aantal verzonden e-mails.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens het verzenden waardoor uw e-mailbericht niet naar profielen kan worden verzonden.

+++

### Openen en klikken op domeinen {#opens-domains}

![](assets/campaign_email_open_domains.png)

De  **[!UICONTROL Open & clicks by domains]** in grafiek en tabel wordt een overzicht gegeven van de betrokkenheid van uw profielen op domeinniveau bij uw e-mail. Zo krijgt u waardevolle inzichten over de interactie tussen de verschillende domeinen en uw inhoud.

+++ Meer informatie over Openen en klikken op domeinmetriek

* **[!UICONTROL Opens]**: Aantal keer dat de e-mail is geopend.

* **[!UICONTROL Clicks]**: Aantal keer dat er op een inhoud in een e-mail is geklikt.

+++

### Bounce reason by domain {#bounce-reasons-domains}

![](assets/campaign_email_bounce_reasons_domains.png)

De  **[!UICONTROL Bounce reasons by domain]** grafiek en tabel bieden een uitsplitsing op domeinniveau van gegevens met betrekking tot zowel tijdelijke als permanente fouten, die gedetailleerde inzichten verschaffen in de redenen achter aangekondigde berichten.

+++ Meer informatie over Bounce-redenen per domein

* **[!UICONTROL Opens]**: Aantal keer dat de e-mail is geopend.

* **[!UICONTROL Clicks]**: Aantal keer dat er op een inhoud in een e-mail is geklikt.

+++

### E-mail - bovenste URL {#top-url-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_top_url"
>title="E-mail - bovenste URL"
>abstract="De grafiek en tabel E-mail - URL bovenaan bieden een uitgebreid overzicht van de URL&#39;s in uw e-mail die het hoogste bezoekersverkeer ontvangen, zodat u de populairste koppelingen kunt identificeren."

![](assets/campaign_email_topurl.png)

De **[!UICONTROL Email - Top Url]** de grafiek en de lijst verstrekken een uitvoerig overzicht van URLs binnen uw e-mail die het hoogste bezoekersverkeer aantrekken. Hierdoor kunt u de populairste koppelingen identificeren en er prioriteiten aan stellen, zodat u meer inzicht krijgt in de betrokkenheid bij profielen met specifieke inhoud in uw e-mails.

### E-mail - Beste ontvangende domein {#top-recipient-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_best_recipient"
>title="E-mail - Beste ontvangende domein"
>abstract="De grafiek en tabel met het domein E-mail - Beste ontvangers bieden een gedetailleerde uitsplitsing van de domeinen die ontvangers het vaakst gebruiken om e-mail te openen, en bieden waardevolle inzichten in het gedrag van ontvangers."

![](assets/campaign_email_best_recipient.png)

>[!CAUTION]
>
> De **[!UICONTROL Email - Best recipient domain]** de widget heeft een nauwkeurigheid van 99 , 95 % .

De **[!UICONTROL Email - Best recipient domain]** de grafiek en de lijst verstrekken een gedetailleerde uitsplitsing van de domeinen die profielen het vaakst gebruiken om uw e-mails te openen. Dit biedt waardevolle inzichten in profielgedrag, waardoor u beter inzicht krijgt in voorkeursplatforms.

+++ Meer informatie over e-mail - Beste maatgegevens voor ontvangende domein

* **[!UICONTROL Delivered]**: Aantal verzonden e-mails in verhouding tot het totale aantal verzonden e-mails.

* **[!UICONTROL Delivery Rate]**: Percentage verzonden e-mailberichten.

* **[!UICONTROL Bounces + Errors Rate]**: Percentage van e-mails dat is teruggestuurd in vergelijking met verzonden e-mails.

+++

### E-mail - Optimalisatie {#optimized-email}

![](assets/campaign_email_optimized.png)

>[!NOTE]
>
>De **[!UICONTROL Optimized vs non optimized]** en **[!UICONTROL Send time optimization]**  widgets zijn alleen beschikbaar als de optie Send-Time Optimization is geactiveerd voor uw e-mail. Voor meer informatie over Send-Time Optimization, verwijs naar [deze pagina](../building-journeys/journeys-message.md#send-time-optimization).

De **[!UICONTROL Optimized vs non optimized]** en **[!UICONTROL Send time optimization]** widgets bevatten de belangrijkste informatie ten opzichte van uw bericht, ongeacht of deze zijn geoptimaliseerd of niet.

+++ Meer informatie over optimalisatiegegevens voor verzendtijd

* **[!UICONTROL Sent]**: Totaal aantal verzendingen.

* **[!UICONTROL Opens]**: Het aantal keren dat het bericht is geopend.

* **[!UICONTROL Clicks]**: Aantal keer dat er op inhoud is geklikt in een e-mail.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounces]**: Totaal aan fouten gecumuleerd tijdens het verzendingsproces en automatische retourverwerking in verhouding tot het totale aantal verzonden berichten.

+++

### E-mail - voorstellen {#email-offers}

![](assets/campaign_email_offers.png)

De **[!UICONTROL Offers statistics]**, **[!UICONTROL Offers statistics over time]** en **[!UICONTROL Offers detailed statistic]** widgets meten het succes en de invloed van uw aanbieding op uw doelgroep.

+++ Meer informatie over e-mail - Metriek van aanbiedingen

* **[!UICONTROL Offer sent]**: Totaal aantal verzendingen voor de aanbieding.

* **[!UICONTROL Offer impression]**: Het aantal keren dat het voorstel in je e-mails is geopend.

* **[!UICONTROL Offer clicks]**: Het aantal keren dat er op een voorstel is geklikt in je e-mailberichten.

* **[!UICONTROL Placement name]**: Naam van uw plaatsing die wordt gebruikt om uw voorstel weer te geven. Raadpleeg deze voor meer informatie over plaatsing [page](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Offer name]**: Naam van de aanbieding die in de levering is toegevoegd. Raadpleeg deze voor meer informatie over plaatsing [page](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offer sent]**: Totaal aantal verzendingen voor de aanbieding.

* **[!UICONTROL Offer impression rate]**: Percentage geopende aanbiedingen in verhouding tot het aantal verzonden aanbiedingen.

+++

## Tabblad In-app {#inapp-global}

Van uw campagne **[!UICONTROL Global report]** de **[!UICONTROL In-app]** bevat de belangrijkste informatie met betrekking tot de berichten in de app die in uw campagne worden verzonden.

### Prestaties in de app {#in-app-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_performance"
>title="Prestaties in de app"
>abstract="De prestatie-KPI&#39;s in de app bieden essentiële inzichten in de betrokkenheid van uw bezoekers bij In-app-berichten."

![](assets/campaign_inapp_performance.png)

De **[!UICONTROL In-app performance]** KPI&#39;s bieden essentiële inzichten in de betrokkenheid van uw bezoekers bij In-app-berichten en bieden essentiële gegevens om de effectiviteit en impact van uw In-app-campagnes te beoordelen.

+++ Meer informatie over prestatiemetriek in de app

* **[!UICONTROL Unique impressions]**: aantal unieke gebruikers aan wie het In-app-bericht is bezorgd.

* **[!UICONTROL Impressions]**: totaal aantal in-app berichten dat aan alle gebruikers is bezorgd.

* **[!UICONTROL Interactions]**: totaal aantal contracten met uw In-app-bericht. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken, ontslag of andere interactie.

+++

### Interacties per type {#interactions-type}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_interactions"
>title="Interacties per type"
>abstract="De interacties per type grafieken en de lijstdetails hoe de gebruikers met uw in-app bericht in wisselwerking stonden door om het even welke klik te volgen, te ontslaan, of interactie."

![](assets/campaign_inapp_interactions.png)

De **[!UICONTROL Interactions by type]** grafieken en tabellen geven een gedetailleerd overzicht van de interactie tussen profielen en uw bericht in de app, en bevatten informatie over het volgen van acties zoals klikken, ontslag of andere vormen van betrokkenheid.

### Overzicht in de app {#in-app-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_summary"
>title="Overzicht in de app"
>abstract="De overzichtsgrafiek in de app illustreert de voortgang van uw impressies en interacties in de app gedurende de opgegeven periode."

![](assets/campaign_inapp_summary.png)

De **[!UICONTROL In-app summary]** De grafiek illustreert de voortgang van uw in-app-afdrukken en interacties gedurende de opgegeven periode en geeft een uitgebreid overzicht van de prestaties van uw In-app-berichten.

+++ Meer informatie over overzichtsgegevens in de app

* **[!UICONTROL Unique impressions]**: aantal unieke gebruikers aan wie het In-app-bericht is bezorgd.

* **[!UICONTROL Impressions]**: totaal aantal in-app berichten dat aan alle gebruikers is bezorgd.

* **[!UICONTROL Interactions]**: totaal aantal contracten met uw In-app-bericht. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken, ontslag of andere interactie.

+++

## Tabblad Pushmelding {#push-global}

Van uw campagne **[!UICONTROL Global report]** de **[!UICONTROL Push notification]** bevat de belangrijkste informatie met betrekking tot de pushmeldingen die in uw campagne worden verzonden.

### Pushmelding - Statistieken verzenden {#push-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_statistics"
>title="Pushmelding - Statistieken verzenden"
>abstract="De lijst van het Verzenden van de Statistieken van het Bericht van de Duw vat essentiële gegevens over uw dupberichten zoals Gerichte of Geleide berichten samen."

![](assets/campaign_push_sending.png)

De **[!UICONTROL Push notification - Sending statistics]** de tabel bevat een beknopt overzicht van de essentiële gegevens over uw pushberichten, inclusief de belangrijkste meetgegevens zoals het aantal gerichte berichten en het aantal succesvol afgeleverde berichten.

+++ Meer informatie over pushmeldingen - Statistische gegevens verzenden

* **[!UICONTROL Execution time]**: Begintijd van elke uitvoering van uw terugkerende pushmelding. Als u slechts één of meerdere terugkerende pushmeldingen wilt activeren, selecteert u deze in het menu **[!UICONTROL Execution time]** vervolgkeuzelijst.

* **[!UICONTROL Targeted]**: Het totale aantal pushmeldingen dat tijdens de analyse is verwerkt.

* **[!UICONTROL Sent]**: Totaal aantal verzendingen voor de pushmelding.

* **[!UICONTROL Delivered]**: Het aantal pushmeldingen dat is verzonden in verhouding tot het totale aantal verzonden pushmeldingen.

* **[!UICONTROL Delivery Rate]**: Percentage pushmeldingen verzonden.

* **[!UICONTROL Bounces]**: Totaal aantal fouten gecumuleerd tijdens het verzendproces en automatische retourverwerking in verhouding tot het totale aantal pushmeldingen.

* **[!UICONTROL Bounce Rate]**: Percentage pushmeldingen dat is teruggestuurd in vergelijking met verzonden pushmeldingen.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden waardoor deze niet naar profielen kon worden verzonden.

* **[!UICONTROL Error Rate]**: percentage fouten dat is opgetreden tijdens het voorkomen dat deze werden verzonden, vergeleken met verzonden pushberichten.

* **[!UICONTROL Excluded]**: Aantal profielen dat door Adobe Journey Optimizer is uitgesloten.

+++

### Pushmeldingen - Statistieken bijhouden {#push-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_tracking_statistics"
>title="Pushmeldingen - Statistieken bijhouden"
>abstract="De statistieken van het Spoor van de Duw verstrekken gegevens over profielactiviteit voor uw dupmelding."

![](assets/campaign_push_tracking.png)

De **[!UICONTROL Push notification- Tracking statistics]** widget biedt een gedetailleerde momentopname van profielactiviteiten die aan uw pushmeldingen zijn gekoppeld, en biedt essentiële inzichten in de doeltreffendheid van betrokkenheid en pushmeldingen.

+++ Meer informatie over pushmeldingen - statistieken bijhouden

* **[!UICONTROL Execution time]**: Begintijd van elke uitvoering van uw terugkerende pushmelding. Als u slechts één of meerdere terugkerende pushmeldingen wilt activeren, selecteert u deze in het menu **[!UICONTROL Execution time]** vervolgkeuzelijst.

* **[!UICONTROL Opens]**: Het aantal keren dat uw pushmelding is geopend.

* **[!UICONTROL Actions]**: Totaal aantal acties op de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

+++

### Pushmelding - Samenvatting verzenden {#push-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_summary"
>title="Pushmelding - Samenvatting verzenden"
>abstract="In de grafiek Samenvatting van pushberichten wordt aangegeven welke gegevens beschikbaar zijn voor verzonden pushberichten."

![](assets/campaign_push_sending_summary.png)

De **[!UICONTROL Push notification - Sending summary]** de grafiek biedt een dynamische vertegenwoordiging aan, die een analyse van uw activiteit van pushberichten toont. Deze grafische weergave biedt een uitgebreide uitsplitsing van verzonden pushberichten.

+++ Meer informatie over pushmeldingen - Samenvattingscijfers verzenden

* **[!UICONTROL Opens]**: Het aantal keren dat uw pushmelding is geopend.

* **[!UICONTROL Actions]**: Totaal aantal acties op de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

* **[!UICONTROL Bounces]**: Totaal aantal gecumuleerde fouten en automatische retourverwerking in verhouding tot het totale aantal verzonden pushberichten.

* **[!UICONTROL Delivered]**: Het aantal pushmeldingen dat is verzonden in verhouding tot het totale aantal verzonden pushmeldingen.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden waardoor deze niet naar profielen kon worden verzonden.

+++

### Pushmelding - Optimalisatie {#push-optimized}

>[!NOTE]
>
>De **[!UICONTROL Optimized vs non optimized]** en **[!UICONTROL Send time optimization]**  widgets zijn alleen beschikbaar als de optie Send-Time Optimization is geactiveerd voor uw pushmelding. Voor meer informatie over Send-Time Optimization, verwijs naar [deze pagina](../building-journeys/journeys-message.md#send-time-optimization).

De **[!UICONTROL Optimized vs non optimized]** en **[!UICONTROL Send time optimization]** widgets bevatten de belangrijkste informatie ten opzichte van uw bericht, ongeacht of deze zijn geoptimaliseerd of niet.

+++ Meer informatie over pushmeldingen - Metrische gegevens voor tijdoptimalisatie verzenden

* **[!UICONTROL Delivered]**: Het aantal pushmeldingen dat is verzonden in verhouding tot het totale aantal verzonden pushmeldingen.

* **[!UICONTROL Opens]**: Het aantal keren dat uw pushmelding is geopend.

* **[!UICONTROL Actions]**: Totaal aantal acties op de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

* **[!UICONTROL Bounces]**: Totaal aantal fouten gecumuleerd tijdens het verzendproces en automatische retourverwerking in verhouding tot het totale aantal verzonden pushmeldingen.

+++

### Pushmelding - Foutredenen {#error-reasons-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_error_reasons"
>title="Pushmelding - Foutredenen"
>abstract="Met de grafieken en de tabel met oorzaken van fouten kunt u de specifieke fouten identificeren die tijdens het verzendingsproces zijn opgetreden."

![](assets/campaign_push_error_reasons.png)

De **[!UICONTROL Error Reasons]** tabel en grafieken bieden u de mogelijkheid om de specifieke fouten te identificeren die zijn opgetreden tijdens het verzenden van uw pushberichten. Zo krijgt u gedetailleerde informatie over eventuele problemen die zich onderweg hebben voorgedaan.

### Pushmelding - Uitgesloten redenen {#excluded-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_excluded_reasons"
>title="Pushmelding - Uitgesloten redenen"
>abstract="In de grafieken en de tabel met uitgesloten redenen worden de verschillende factoren weergegeven die hebben geleid tot gebruikersprofielen die zijn uitgesloten van het doelpubliek en die het bericht niet ontvangen."

![](assets/campaign_push_excluded.png)

De **[!UICONTROL Excluded reasons]** in grafieken en tabellen worden de verschillende redenen weergegeven waarom gebruikersprofielen, die zijn uitgesloten van de doelprofielen, uw pushberichten niet hebben ontvangen.

Zie [deze pagina](exclusion-list.md) voor de volledige lijst van uitsluitingsredenen.

### Pushmelding - Onderverdeling per platform {#breakdown-platform-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_breakdown_platform"
>title="Pushmelding - Onderverdeling per platform"
>abstract="De grafieken en tabel van de indeling naar platform geven een overzicht van het succes van uw pushberichten op basis van het besturingssysteem van het profiel."

![](assets/campaign_push_breakdown.png)

De **[!UICONTROL Push notification - Breakdown by platform]** de grafiek en de lijst verstrekken een gedetailleerde analyse van het succes van uw pushberichten, die inzichten aanbieden die op het werkende systeem van uw profiel worden gebaseerd. Deze ineenstorting verbetert uw inzicht in hoe goed uw pushberichten op verschillende platforms presteren.

+++ Meer informatie over pushmeldingen - Uitsplitsing op basis van afmetingen van het platform

* **[!UICONTROL Targeted]**: Het totale aantal pushmeldingen dat tijdens de analyse is verwerkt.

* **[!UICONTROL Delivered]**: Het aantal pushmeldingen dat is verzonden in verhouding tot het totale aantal verzonden pushmeldingen.

* **[!UICONTROL Opens]**: Het aantal keren dat uw pushmelding is geopend.

* **[!UICONTROL Actions]**: Totaal aantal acties op de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

* **[!UICONTROL Bounces]**: Totaal aantal gecumuleerde fouten en automatische retourverwerking in verhouding tot het totale aantal verzonden pushberichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden waardoor deze niet naar profielen kon worden verzonden.

* **[!UICONTROL Excluded]**: Aantal profielen dat door Adobe Journey Optimizer is uitgesloten.

+++

## Tabblad SMS {#sms-global}

Van uw campagne **[!UICONTROL Global report]** de **[!UICONTROL SMS]** bevat de belangrijkste informatie met betrekking tot de SMS-berichten die in uw campagne worden verzonden.

### SMS - Statistieken verzenden {#sms-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_sending_statistics"
>title="SMS - Statistieken verzenden"
>abstract="De SMS die Statistieken verzendt vat essentiële gegevens over uw SMS- berichten zoals Gerichte of Geleide berichten samen."

![](assets/campaign_sms_sending.png)

De **[!UICONTROL SMS - Sending statistics]** de lijst verstrekt een beknopte samenvatting van essentiële gegevens met betrekking tot uw berichten van SMS, die zeer belangrijke metriek zoals het aantal gerichte berichten en het aantal met succes geleverde berichten omvatten.

+++ Meer informatie over SMS - Statistische gegevens verzenden

* **[!UICONTROL Execution time]**: Begintijd voor elke uitvoering van uw terugkerende SMS-bericht. Als u slechts één of meerdere terugkerende SMS-berichten wilt aanwijzen, selecteert u deze in het menu **[!UICONTROL Execution time]** vervolgkeuzelijst.

* **[!UICONTROL Targeted]**: Aantal gebruikersprofielen dat als doelprofielen wordt gekwalificeerd.

* **[!UICONTROL Excluded]**: Aantal gebruikersprofielen dat is uitgesloten van de doelprofielen en dat het bericht niet heeft ontvangen.

* **[!UICONTROL Sent]**: Het totale aantal verzendingen voor uw SMS-berichten.

* **[!UICONTROL Bounces]**: Totaal aantal fouten gecumuleerd tijdens het verzendingsproces en automatische retourverwerking in verhouding tot het totale aantal verzonden SMS-berichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden waardoor deze niet naar profielen kon worden verzonden.

+++

### SMS - Trackingstatistieken {#sms-tracking-statistics}

![](assets/campaign_sms_tracking.png)

De **[!UICONTROL SMS - Tracking statistics]** widget geeft een gedetailleerd overzicht van belangrijke informatie over de betrokkenheid van uw bezoekers bij uw URL&#39;s en biedt inzichten in de effectiviteit van uw SMS-berichten.

+++ Meer informatie over SMS - statistieken bijhouden

* **[!UICONTROL Execution time]**: Begintijd voor elke uitvoering van uw terugkerende SMS. Als u slechts één of meerdere terugkerende SMS-berichten wilt gebruiken, selecteert u deze in het menu **[!UICONTROL Execution time]** vervolgkeuzelijst.

* **[!UICONTROL Clicks]**: Het aantal keren dat er op de inhoud is geklikt in een SMS-bericht.

+++

### SMS - Prestaties op datum {#sms-perfomance-date}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_performance"
>title="SMS - Prestaties op datum"
>abstract="De widget SMS-prestaties op datum biedt via een grafische weergave belangrijke informatie over uw berichten."

![](assets/campaign_sms_performance.png)

De **[!UICONTROL SMS Performance by date]** widget biedt een gedetailleerd overzicht van belangrijke informatie met betrekking tot uw berichten , die door een grafiek wordt voorgesteld , die inzicht geeft in de prestatietrends over specifieke tijdsperiodes.

+++ Meer informatie over SMS - Prestaties op basis van datum

* **[!UICONTROL Sent]**: Het totale aantal verzendingen voor uw SMS-berichten.

* **[!UICONTROL Bounces]**: Totaal aantal fouten gecumuleerd tijdens het verzendingsproces en automatische retourverwerking in verhouding tot het totale aantal verzonden SMS-berichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden waardoor deze niet naar profielen kon worden verzonden.

+++

### SMS - Redenen voor fouten {#sms-error}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_error_reasons"
>title="SMS - Redenen voor fouten"
>abstract="Met SMS - Foutgrafieken en -tabel kunt u de specifieke fouten identificeren die tijdens het verzendingsproces zijn opgetreden."

![](assets/campaign_sms_error_reasons.png)

De **[!UICONTROL Error Reasons]** Met grafieken en tabellen kunt u de specifieke fouten identificeren die zijn opgetreden tijdens het verzenden van uw SMS-berichten. Zo kunt u een grondige analyse van alle ondervonden problemen maken.

### SMS - Uitgesloten redenen {#sms-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_excluded_reasons"
>title="SMS - Uitgesloten redenen"
>abstract="In de grafieken en de tabel met uitgesloten redenen worden de verschillende factoren weergegeven die hebben geleid tot gebruikersprofielen die zijn uitgesloten van het doelpubliek en die het bericht niet ontvangen."

![](assets/campaign_sms_excluded.png)

De **[!UICONTROL Excludes Reasons]** in grafieken en tabellen worden visueel de verschillende factoren weergegeven die hebben geleid tot de uitsluiting van gebruikersprofielen van het beoogde publiek, zodat gebruikers uw SMS-berichten niet kunnen ontvangen.

Zie [deze pagina](exclusion-list.md) voor de volledige lijst van uitsluitingsredenen.

### SMS - Bounges redenen {#sms-bounces-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_bounces_reasons"
>title="SMS - Bounges redenen"
>abstract="De grafieken en de tabel met Bounces Reasons bevatten de beschikbare gegevens met betrekking tot berichten die worden teruggestuurd."

De **[!UICONTROL Bounces Reasons]** grafieken en tabellen bieden een uitgebreid overzicht van de gegevens met betrekking tot verzonden SMS-berichten en bieden waardevolle inzichten in de specifieke redenen achter sms-berichten.

### SMS - Klikken op koppelingen {#sms-clicks-links}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_clicks_links"
>title="SMS - Klikken op koppelingen"
>abstract="SMS - De widget klikt op koppelingen biedt essentiële inzichten in de betrokkenheid van uw bezoekers bij de URL&#39;s in uw berichten"

![](assets/campaign_sms_clicks.png)

De **[!UICONTROL SMS - Clicks by links]** widget biedt essentiële inzichten in de betrokkenheid van uw bezoekers bij de URL&#39;s die in uw berichten zijn opgenomen en biedt waardevolle informatie over welke koppelingen de meeste interactie aantrekken.

## Tabblad Web {#web-tab}

Van uw campagne **[!UICONTROL Global report]** de **[!UICONTROL Web]** van het lusje details de belangrijkste informatie met betrekking tot uw Web-pagina&#39;s.

### Webprestaties {#web-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_performance"
>title="Webprestaties"
>abstract="De KPI&#39;s voor webprestaties bieden uitgebreide informatie over de betrokkenheid van uw bezoekers bij uw webervaringen."

![](assets/campaign_web_performance.png)

De **[!UICONTROL Web performance]** KPI&#39;s bieden uitgebreide inzichten in de betrokkenheid van uw bezoekers bij uw webpagina&#39;s, die belangrijke metriek omvatten, zoals impressies en interacties.

+++ Meer informatie over prestatietriek op het web

* **[!UICONTROL Unique impressions]**: aantal unieke gebruikers aan wie de webervaring is geleverd.

* **[!UICONTROL Impressions]**: totaal aantal webervaringen dat aan alle gebruikers wordt geleverd.

* **[!UICONTROL Interaction rate]**: percentage van de afspraken met uw webpagina. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken of andere interacties.

+++

### Weboverzicht {#web-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_summary"
>title="Weboverzicht"
>abstract="De webinvattingsgrafiek illustreert de voortgang van uw webervaringen, inclusief indrukken, unieke indrukken en interacties, gedurende de opgegeven periode."

![](assets/campaign_web_summary.png)

De **[!UICONTROL Web summary]** in de grafiek wordt de evolutie van uw webervaringen (indrukken, unieke indrukken en interacties) voor de desbetreffende periode weergegeven.

+++ Meer informatie over overzichtsmetriek op internet

* **[!UICONTROL Unique impressions]**: aantal unieke gebruikers aan wie de webervaring is geleverd.

* **[!UICONTROL Impressions]**: totaal aantal webervaringen dat aan alle gebruikers wordt geleverd.

* **[!UICONTROL Interaction]**: totaal aantal contracten met uw webpagina. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken of andere interacties.

+++

### Interacties per element {#web-interactions}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_interactions"
>title="Interacties per element"
>abstract="De tabel Interacties per element biedt belangrijke informatie over de betrokkenheid van uw bezoekers bij verschillende elementen op uw webpagina&#39;s."

![](assets/campaign_web_interactions.png)

De **[!UICONTROL Interactions by element]** de tabel bevat uitgebreide informatie over de betrokkenheid van uw bezoekers bij de verschillende elementen op uw webpagina&#39;s en biedt waardevolle inzichten in gebruikersinteracties en voorkeuren.

+++ Meer informatie over interacties op basis van elementmeetgegevens

* **[!UICONTROL Interaction]**: totaal aantal contracten met uw webpagina. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken of andere interacties.

* **[!UICONTROL Interaction rate]**: percentage van de afspraken met uw webpagina. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken of andere interacties.

+++

## Tabblad Direct mail {#direct-mail-global}

Van uw campagne **[!UICONTROL Global report]** de **[!UICONTROL Direct mail]** bevat de belangrijkste gegevens met betrekking tot uw Direct-mailberichten.

### Directe post - Verzendstatistieken {#direct-mail-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_sending_statistics"
>title="Directe post - Verzendstatistieken"
>abstract="De Direct mail die Statistieken verzendt vat essentiële gegevens over uw Directe Berichten zoals Gerichte of Geleverde berichten samen."

![](assets/campaign_direct_sending.png)

De **[!UICONTROL Direct Mail - Sending statistics]** De lijst verstrekt een beknopte samenvatting van essentiële gegevens met betrekking tot uw Directe Berichten, die zeer belangrijke metriek zoals het aantal gerichte berichten en het aantal met succes geleverde berichten omvatten.

+++ Meer informatie over Direct Mail - Statistische gegevens verzenden

* **[!UICONTROL Execution time]**: Begintijd van elke uitvoering van uw terugkerende Direct-mail. Als u slechts één of meerdere terugkerende Direct-mail als doel wilt instellen, selecteert u deze in het menu **[!UICONTROL Execution time]** vervolgkeuzelijst.

* **[!UICONTROL Targeted]**: Aantal gebruikersprofielen dat als doelprofielen voor uw direct-mailberichten in aanmerking komt.

* **[!UICONTROL Sent]**: Het totale aantal verstuurt voor uw direct-mailberichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens het verzendproces waardoor het niet naar profielen kan worden verzonden.

* **[!UICONTROL Excluded]**: Aantal gebruikersprofielen dat is uitgesloten van de doelprofielen en dat uw e-mailberichten niet heeft ontvangen.

+++

### Directe post - de redenen van de Fout {#direct-mail-error}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_error_reasons"
>title="Directe post - de redenen van de Fout"
>abstract="Met de grafieken en de tabel Directe e-mail - Foutredenen kunt u de specifieke fouten identificeren die tijdens het verzendingsproces zijn opgetreden."

![](assets/direct-mail-report_1.png)

De **[!UICONTROL Direct Mail - Error reasons]** grafieken en tabel bieden de middelen om specifieke fouten te identificeren die zijn opgetreden tijdens het verzenden van uw e-mailberichten, zodat een gedetailleerde analyse van eventuele problemen kan worden uitgevoerd.

### Direct mail - Uitgesloten redenen {#direct-mail-excluded}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_excluded_reasons"
>title="Direct mail - Uitgesloten redenen"
>abstract="De grafiek en de tabel met uitgesloten redenen voor Direct Mail illustreren de verschillende factoren die tot gebruikersprofielen hebben geleid, die van het beoogde publiek zijn uitgesloten en die het bericht niet ontvangen."

![](assets/campaign_direct_excluded.png)

De **[!UICONTROL Direct Mail - Excluded reasons]** in grafieken en tabellen worden visueel de verschillende factoren geïllustreerd die ertoe hebben geleid dat gebruikersprofielen zijn uitgesloten van het doelpubliek, zodat deze geen directe-mailberichten kunnen ontvangen.

Zie [deze pagina](exclusion-list.md) voor de volledige lijst van uitsluitingsredenen.

## Aanvullende bronnen

* [Aan de slag met campagnes](../campaigns/get-started-with-campaigns.md)
* [Een campagne maken](../campaigns/create-campaign.md)
* [API-gestuurde campagnes maken](../campaigns/api-triggered-campaigns.md)
* [Een campagne wijzigen of stoppen](../campaigns/modify-stop-campaign.md)
* [Campagne live-rapport](campaign-live-report.md)
