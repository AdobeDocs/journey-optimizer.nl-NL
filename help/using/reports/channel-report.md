---
solution: Journey Optimizer
product: journey optimizer
title: Rapporten op kanaalniveau
description: Leer hoe u gegevens uit de Channel-rapporten kunt gebruiken
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ead9359b-cdab-43ed-a469-d98b0ca19a17
source-git-commit: d26dbebaf36241d0e91c36c95f83ce6cf712ecee
workflow-type: tm+mt
source-wordcount: '3447'
ht-degree: 0%

---

# Kanaalrapporten {#channel-report}

>[!CONTEXTUALHELP]
>id="ajo_channel_level_report"
>title="Rapport op kanaalniveau"
>abstract="De rapporten van het Kanaal bieden een uitvoerig overzicht van verkeer en betrokkenheidsmetriek over alle kanalen. Uw rapporten zijn verdeeld in verschillende widgets die uw campagne en het succes en de fouten van reizen gedetailleerd beschrijven. Elk rapportdashboard kan worden gewijzigd door widgets te vergroten of te verkleinen of te verwijderen."

>[!IMPORTANT]
>
> Als u toegang wilt krijgen tot **Rapport** menu, moet u de **[!UICONTROL View Channel Reports]** toestemming. [Meer informatie](channel-report-gs.md#before-starting-manage-reports-prereq)

De rapporten van het Kanaal verstrekken gebruikers een uitvoerig overzicht van verkeer en betrokkenheidsmetriek op kanaal-niveau. De meetwaarden worden samengevoegd om geconsolideerde waarden voor acties te presenteren die afkomstig zijn van het gekozen kanaal en die zich uitstrekken over verschillende campagnes en reizen.

U kunt tot de rapporten van het Kanaal toegang hebben door aan **Rapporten** in het menu **Reisbeheer** sectie. Het is volledig aanpasbaar, kunt u uw gegevens filtreren afhankelijk van de datum van het Rapport of Actie. [Meer informatie](channel-report-gs.md)

De rapportpagina wordt getoond met de volgende lusjes:

* [Email](#email)
* [Pushmeldingen](#push)
* [Sms](#sms)
* [In-app](#inapp)
* [Web](#web)
* [Direct mail](#direct-mail)

➡️ [Deze functie in video detecteren](#channel-report-video)

## Email {#email}

In het menu E-mail van uw Channel-rapporten vindt u de belangrijkste gegevens met betrekking tot de e-mails die in uw campagnes en reizen zijn verzonden. De cijfers worden hieronder beschreven.

### E-mail - Totaal verzendende statistieken {#email-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics"
>title="E-mail - Totaal verzendende statistieken"
>abstract="De e-mail - het totaal verzenden van statistieken KPIs vat essentiële gegevens over uw e-mail zoals Gerichte of Geleverde berichten samen."

![](assets/channel_email_total_sending.png)

De **[!UICONTROL Email Total Sending Statistics]** widget biedt een uitgebreid overzicht van uw e-mailprestaties, waarin belangrijke prestatie-indicatoren (KPI&#39;s) worden weergegeven waarmee essentiële gegevens over uw e-mailberichten worden samengevat.

+++ Meer informatie over statistieken over totale verzendstatistieken per e-mail

* **[!UICONTROL Targeted]**: Totaal aantal verwerkte e-mails.

* **[!UICONTROL Sent]**: Totaal aantal verzendingen.

* **[!UICONTROL Delivered]**: Aantal verzonden e-mailberichten in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Delivery Rate]**: Percentage verzonden e-mailberichten.

* **[!UICONTROL Bounces]**: Totaal aantal gecumuleerde fouten en automatische retourverwerking in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounce Rate]**: Percentage van e-mails dat is teruggestuurd in vergelijking met verzonden e-mails.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden waardoor deze niet naar profielen kon worden verzonden.

* **[!UICONTROL Error Rate]**: Percentage fouten dat voorkwam waardoor het niet kon worden verzonden vergeleken met verzonden e-mails.

* **[!UICONTROL Excluded]**: Aantal profielen dat door Adobe Journey Optimizer is uitgesloten.

* **[!UICONTROL Exclude rate]**: Percentage profielen dat door Adobe Journey Optimizer is uitgesloten.

+++

### E-mail - Totaal aantal volgstatistieken {#email-total-tracking}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics"
>title="E-mail - Totaal aantal volgstatistieken"
>abstract="De KPI&#39;s voor statistieken over het bijhouden van gegevens via e-mail bieden gegevens over profielactiviteiten voor uw e-mails."

![](assets/channel_email_total_tracking.png)

De **[!UICONTROL Email Total Tracking statistics]** widget biedt een gedetailleerde momentopname van profielactiviteiten die aan uw e-mails zijn gekoppeld en die essentiële inzichten bieden in de betrokkenheid en de doeltreffendheid van e-mailberichten.

+++ Meer informatie over statistieken over het bijhouden van gegevens per e-mail

* **[!UICONTROL Opens]**: Het aantal keren dat het bericht is geopend.

* **[!UICONTROL Open Rate]**: Het totale aantal geopende e-mails in verhouding tot het aantal geleverde e-mails.

* **[!UICONTROL Clicks]**: Het aantal keren dat er op de inhoud is geklikt in een bericht.

* **[!UICONTROL Click rate]**: Percentage gebruikers dat interactie heeft gehad met de e-mail.

* **[!UICONTROL Spam complaints]**: Het aantal keren dat een bericht is gedeclareerd als spam of junk.

* **[!UICONTROL Spam complaint rate]**: Percentage berichten dat als spam of junk wordt gedeclareerd in verhouding tot het aantal verzonden e-mails.

* **[!UICONTROL Unsubscribes]**: Het aantal klikken op de abonnementkoppeling.

* **[!UICONTROL Unsubscribe rate]**: Percentage van abonnement vergeleken met het aantal verzonden e-mails.

+++

### E-mail - Statistieken verzenden in de loop der tijd {#email-sending-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics_overtime"
>title="E-mail - Statistieken verzenden in de loop der tijd"
>abstract="De e - mail - Verzendende statistieken in tijdgrafiek geven gegevens over verzonden e-mails weer, uitgesplitst op uur, dag, week, of maandbasis."

![](assets/channel_email_sending_statistics.png)

De **[!UICONTROL Email - Sending Statistics over time]** grafiek biedt een dynamische vertegenwoordiging aan, die een analyse van uw e-mailactiviteit toont. Deze grafische weergave biedt een uitgebreide uitsplitsing van verzonden e-mailberichten, waarmee u trends en patronen kunt waarnemen op een schaal van uur, dag, week of maand.

+++ Meer informatie over e-mail - Statistieken verzenden over tijdsmetingen

* **[!UICONTROL Sent]**: Totaal aantal verzendingen.

* **[!UICONTROL Delivered]**: Aantal verzonden e-mails in verhouding tot het totale aantal verzonden e-mails.

* **[!UICONTROL Bounces]**: Totaal aantal gecumuleerde fouten en automatische verwerking van de geretourneerde hoeveelheid ten opzichte van het totale aantal verzonden e-mails.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden waardoor deze niet naar profielen kon worden verzonden.

+++

### E-mail - Statistieken bijhouden in de loop der tijd {#email-tracking-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics_overtime"
>title="E-mail - Statistieken bijhouden in de loop der tijd"
>abstract="De E-mail - het Volgen statistieken over tijdsgrafiek verstrekt gegevens over profielactiviteit voor uw e-mail, die op een uur, dag, wekelijkse, of maandbasis wordt uitgesplitst."

![](assets/channel_email_tracking_overtime.png)

De **[!UICONTROL Email - Tracking statistics over time]** grafiek geeft een gedetailleerd overzicht van de profielactiviteiten met betrekking tot uw e-mails. Deze grafische weergave deelt de gegevens op uur-, dag-, week- of maandbasis op, en biedt waardevolle inzichten in hoe de betrokkenheid van de ontvanger zich ontwikkelt over verschillende tijdsintervallen.

+++ Meer informatie over e-mail - Statistieken bijhouden over tijdsmetingen

* **[!UICONTROL Opens]**: Het aantal keren dat het bericht is geopend.

* **[!UICONTROL Clicks]**: Het aantal keren dat er op de inhoud is geklikt in een bericht.

+++

### E-mail - rubrieken en redenen voor stuiteren {#bounce-categories}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_categories"
>title="Stuitcategorieën"
>abstract="De categorieën Bounce en de tabel geven gegevens over zowel tijdelijke als permanente fouten."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons"
>title="Stuitingsredenen"
>abstract="De grafieken en de tabel met Bounces Reasons bevatten de beschikbare gegevens met betrekking tot berichten die worden teruggestuurd."

![](assets/channel_email_bounce_categories.png)

De **[!UICONTROL Bounce categories]** en **[!UICONTROL Bounce reasons]** widgets kapselen de gegevens in die aan berichten met teruggang worden geassocieerd, die een uitvoerig overzicht van de diverse categorieën en specifieke redenen achter berichtgrenzen verstrekken

Voor meer informatie over grenzen raadpleegt u de [Onderdrukkingslijst](../reports/suppression-list.md) pagina.

+++ Meer informatie over de maatstaven van Bounce-rubrieken

* **[!UICONTROL Hard bounce]**: Het totale aantal permanente fouten, zoals een onjuist e-mailadres. Dit omvat een foutbericht waarin expliciet wordt aangegeven dat het adres ongeldig is, zoals Onbekende gebruiker.

* **[!UICONTROL Soft bounce]**: Het totale aantal tijdelijke fouten, zoals een volledig postvak.

* **[!UICONTROL Ignored]**: Het totale aantal tijdelijke berichten, zoals Buiten-kantoor, of een technische fout, bijvoorbeeld als het type afzender postmaster is.

+++

### Foutredenen {#error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_error_reasons"
>title="Foutredenen"
>abstract="Met de grafieken en de tabel met oorzaken van fouten kunt u de specifieke fouten identificeren die tijdens het verzendingsproces zijn opgetreden."

![](assets/channel_email_error.png)

De **[!UICONTROL Error Reasons]** Met grafieken en tabellen kunt u precies aangeven welke fouten tijdens het verzendproces zijn opgetreden. Zo krijgt u een duidelijk inzicht in de ondervonden problemen.

### Uitgesloten redenen {#excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_excluded_reasons"
>title="Uitgesloten redenen"
>abstract="In de grafieken en de tabel met uitgesloten redenen worden de verschillende factoren weergegeven die hebben geleid tot gebruikersprofielen die zijn uitgesloten van het doelpubliek en die het bericht niet ontvangen."

![](assets/channel_email_excluded.png)

De **[!UICONTROL Excluded reasons]** in grafieken en tabellen wordt een uitgebreid overzicht gegeven van de verschillende factoren die ertoe hebben geleid dat gebruikersprofielen van het beoogde publiek zijn uitgesloten, waardoor het bericht niet is ontvangen.

Zie [deze pagina](exclusion-list.md) voor de volledige lijst van uitsluitingsredenen.

### Verzonden en geleverd op domeinen {#sent-delivered-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_delivered_domains"
>title="Verzonden en geleverd op domeinen"
>abstract="De grafiek en tabel die worden verzonden en geleverd door domeinen geven een indeling op domeinniveau weer van elke belangrijke e-mail die gegevens verzendt."

![](assets/channel_email_sent_domains.png)

De  **[!UICONTROL Sent & delivered by domains]** tabel en grafiek geven een gedetailleerde uitsplitsing van e-mailleveringen op domeinniveau, zodat u uitgebreide inzichten kunt krijgen in de prestaties van uw e-mails.

+++ Meer informatie over Verzonden en geleverde waarden per domein

* **[!UICONTROL Sent]**: Totaal aantal verzendingen voor uw e-mail.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

+++

### Stuitingen en fouten per domein {#bounces-errors-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounces_errors_domains"
>title="Stuitingen en fouten per domein"
>abstract="De Bounces &amp; de fouten door domeingrafiek en de lijst vertegenwoordigen domein-vlakke uitsplitsing van specifieke fouten die tijdens het verzendende proces voorkwamen."

![](assets/channel_email_bounces_domain.png)

De  **[!UICONTROL Bounces & errors by domains]** de grafiek en de lijst verstrekken een domein-vlakke uitsplitsing van specifieke fouten die tijdens het verzendende proces worden ontmoet, die een gedetailleerde analyse van kwesties verstrekken die voorkwamen.

+++ Meer informatie over grenzen en fouten per domeinmetriek

* **[!UICONTROL Bounces]**: Totaal aan fouten gecumuleerd tijdens het verzendingsproces en automatische retourverwerking in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens het verzendproces waardoor het niet naar profielen kan worden verzonden.

+++

### Openen en klikken op domeinen {#open-clicks-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_open_clicks_domains"
>title="Openen en klikken op domeinen"
>abstract="De grafiek en tabel voor Openen en klikken op domeinen geven een overzicht van de betrokkenheid van uw bezoekers bij uw e-mail op domeinniveau."

![](assets/channel_email_open_domains.png)

De  **[!UICONTROL Open & clicks by domains]** in grafiek en tabel wordt een overzicht gegeven van de betrokkenheid van uw bezoekers op domeinniveau bij uw e-mail. Zo krijgt u waardevolle inzichten over de interactie tussen de verschillende domeinen en uw inhoud.

+++ Meer informatie over Openen en klikken op domeinmetriek

* **[!UICONTROL Opens]**: Aantal keer dat de e-mail is geopend.

* **[!UICONTROL Clicks]**: Aantal keer dat er op inhoud is geklikt in een e-mail.

+++

### Bounce reason by domain {#bounce-reasons-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons_domains"
>title="Bounce reason by domain"
>abstract="De redenen van de Stuiting door domein door domeingrafiek en lijst vertegenwoordigen domein-vlakke uitsplitsing van gegevens over zowel tijdelijke als permanente fouten."

![](assets/channel_email_bounce_domain.png)

De  **[!UICONTROL Bounce reasons by domain]** grafiek en tabel bieden een uitsplitsing op domeinniveau van gegevens met betrekking tot zowel tijdelijke als permanente fouten, die gedetailleerde inzichten verschaffen in de redenen achter aangekondigde berichten.

Voor meer informatie over grenzen raadpleegt u de [Onderdrukkingslijst](../reports/suppression-list.md) pagina.

## Pushmelding {#push}

Van uw rapporten van het Kanaal, **Pushmelding** bevat de belangrijkste informatie met betrekking tot pushmeldingen die in uw campagnes en reizen worden verzonden. Metrisch worden hieronder beschreven.

### Pushberichten - Totaal verzendende statistieken {#push-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics"
>title="Pushberichten - Totaal verzendende statistieken"
>abstract="De pushberichten - het totaal verzenden van statistieken KPIs vatten essentiële gegevens over uw dupberichten zoals Gericht of Geleverd samen."

![](assets/channel_push_total_sending.png)

De **[!UICONTROL Push notifications - Total sending statistics]** KPI&#39;s fungeren als een uitgebreide samenvatting waarin essentiële gegevens met betrekking tot uw pushberichten zijn opgenomen. Deze meetgegevens bevatten gedetailleerde inzichten in het doelpubliek en de werkelijke leveringsstatus, zodat u een goed doordachte weergave krijgt van de effectiviteit en het bereik van uw pushberichten.

+++ Meer informatie over pushberichten - statistische gegevens totaal verzenden

* **[!UICONTROL Targeted]**: Totaal aantal verwerkte pushberichten.

* **[!UICONTROL Sent]**: Totaal aantal verzonden pushmeldingen.

* **[!UICONTROL Delivered]**: Het aantal pushmeldingen dat is verzonden in verhouding tot het totale aantal verzonden pushmeldingen.

* **[!UICONTROL Delivery Rate]**: Percentage pushmeldingen verzonden.

* **[!UICONTROL Bounces]**: Totaal aantal gecumuleerde fouten en automatische retourverwerking in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounce Rate]**: Percentage pushmeldingen dat is teruggestuurd in vergelijking met verzonden pushmeldingen.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden waardoor deze niet naar profielen kon worden verzonden.

* **[!UICONTROL Error Rate]**: percentage fouten dat ervoor zorgde dat deze niet konden worden verzonden, vergeleken met verzonden pushberichten.

* **[!UICONTROL Excluded]**: Aantal profielen dat door Adobe Journey Optimizer is uitgesloten.

* **[!UICONTROL Exclude rate]**: Percentage profielen dat door Adobe Journey Optimizer is uitgesloten.

+++

### Pushmelding - Totaal aantal volgstatistieken {#push-total-tracking}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics"
>title="Pushmelding - Totaal aantal volgstatistieken"
>abstract="Het pushbericht - De statistische gegevens voor het bijhouden van gegevens bevatten gegevens over de profielactiviteit voor uw pushberichten."

De **[!UICONTROL Push notification - Total tracking statistics]** widget biedt een gedetailleerde momentopname van profielactiviteiten die aan uw pushmeldingen zijn gekoppeld, en biedt essentiële inzichten in de doeltreffendheid van betrokkenheid en pushmeldingen.

+++ Meer informatie over pushberichten - statistische gegevens over het bijhouden van gegevens

* **[!UICONTROL Opens]**: Het aantal keren dat een pushmelding is geopend.

* **[!UICONTROL Open Rate]**: Percentage geopende pushmeldingen.

* **[!UICONTROL Actions]**: Totaal aantal acties op de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

* **[!UICONTROL Action rate]**: Percentage acties op de geleverde pushmelding in vergelijking met verzonden pushberichten.

+++

### Pushmeldingen - Statistieken verzenden in de loop der tijd {#push-sending-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_overtime"
>title="Pushmeldingen - Statistieken verzenden in de loop der tijd"
>abstract="De grafiek van het Bericht van de Duw die statistieken over tijdsgrafiek verzendt geeft gegevens betreffende verzonden pushberichten, uitgesplitst op een uur, een dag, een wekelijkse, of maandbasis."

![](assets/channel_push_sending_statistics.png)

De **[!UICONTROL Push notifications - Sending statistics over time]** de grafiek biedt een dynamische vertegenwoordiging aan, die een analyse van uw activiteit van pushberichten toont. Deze grafische weergave biedt een uitgebreide uitsplitsing van verzonden pushberichten, waarmee u trends en patronen kunt waarnemen op een schaal van uur, dag, week of maand.

+++ Meer informatie over pushmeldingen - Statistieken over de tijd verzenden

* **[!UICONTROL Sent]**: Totaal aantal verzonden pushmeldingen.

* **[!UICONTROL Delivered]**: Het aantal pushmeldingen dat is verzonden in verhouding tot het totale aantal verzonden pushmeldingen.

* **[!UICONTROL Bounces]**: Totaal aantal gecumuleerde fouten en automatische retourverwerking in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden waardoor deze niet naar profielen kon worden verzonden.

+++

### Pushmeldingen - Statistieken bijhouden in de loop der tijd {#push-tracking-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_overtime"
>title="Pushmeldingen - Statistieken bijhouden in de loop der tijd"
>abstract="De pushberichten - Het bijhouden van statistieken in de tijdgrafiek geeft gegevens over de profielactiviteit voor uw pushberichten, uitgesplitst op een uur-, dag-, week- of maandbasis."

De **[!UICONTROL Push notifications - Tracking statistics over time]** grafiek verstrekt een gedetailleerd overzicht van profielactiviteit met betrekking tot uw dupberichten. Deze grafische weergave deelt de gegevens op uur-, dag-, week- of maandbasis op, en biedt waardevolle inzichten in hoe de betrokkenheid van de ontvanger zich ontwikkelt over verschillende tijdsintervallen.

+++ Meer informatie over pushmeldingen - Statistieken bijhouden over tijdwaarden

* **[!UICONTROL Opens]**: Het aantal keren dat uw pushmelding is geopend.

* **[!UICONTROL Actions]**: Totaal aantal acties op de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

+++

### Pushmeldingen - Uitgesloten redenen {#push-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_excluded_reasons"
>title="Uitgesloten redenen"
>abstract="In de grafieken en de tabel met uitgesloten redenen worden de verschillende factoren weergegeven die hebben geleid tot gebruikersprofielen die zijn uitgesloten van het doelpubliek en die het bericht niet ontvangen."

![](assets/channel_push_excluded.png)

De **[!UICONTROL Excluded reasons]** de grafiek en de lijst tonen de verschillende redenen die gebruikersprofielen, uitgesloten van de gerichte profielen, van het ontvangen van uw dupberichten verhinderden.

Zie [deze pagina](exclusion-list.md) voor de volledige lijst van uitsluitingsredenen.

### Pushmeldingen - Foutredenen {#push-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_error_reasons"
>title="Foutredenen"
>abstract="Met de grafieken en de tabel met oorzaken van fouten kunt u de specifieke fouten identificeren die tijdens het verzendingsproces zijn opgetreden."

![](assets/channel_push_error.png)

De **[!UICONTROL Error Reasons]** grafieken en tabel bieden u de mogelijkheid om de specifieke fouten te identificeren die zijn opgetreden tijdens het verzenden van uw pushberichten. Zo krijgt u gedetailleerde informatie over eventuele problemen die zich onderweg hebben voorgedaan.

### Pushmeldingen - Bijhouden per platform {#push-tracking-platform}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_platform"
>title="Statistieken bijhouden per platform"
>abstract="De statistieken van het Volgen door platformgrafiek en lijst verstrekken gegevens over profielactiviteit voor uw dupberichten afhankelijk van het operationele systeem van uw profiel."

De **[!UICONTROL Push notifications - Tracking by platform]** Grafieken en tabellen geven de activiteit van de ontvangers voor uw pushmelding weer, afhankelijk van het besturingssysteem van uw profiel.

### Pushmeldingen - Verzenden per platform {#push-sending-platform}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_platform"
>title="Statistieken verzenden per platform"
>abstract="De verzendende statistieken per platformgrafiek en tabel bevatten gegevens over verzonden pushberichten."

![](assets/channel_push_sending_platform.png)

De **[!UICONTROL Push notifications - Sending by platform]** een grafiek en tabellen geven een uitgebreide uitsplitsing van uw pushmeldingen met betrekking tot de operationele systemen van uw profielen. Deze grondige analyse biedt waardevolle inzichten in de doeltreffendheid van uw pushberichten op verschillende platforms.

## Sms {#sms}

Van uw **Kanaal** in het menu SMS worden de belangrijkste gegevens weergegeven met betrekking tot SMS die in uw campagnes en reizen is verzonden. De cijfers worden hieronder beschreven.

### SMS - Totaal aantal verzendende statistieken {#sms-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics"
>title="SMS - Totaal aantal verzendende statistieken"
>abstract="SMS - het totaal verzenden van statistieken KPIs vat essentiële gegevens over uw SMS berichten zoals Gericht of Geleverd samen."

![](assets/channel_sms_total_sending.png)

De **[!UICONTROL SMS - Total sending statistics]** KPIs dient als uitvoerige samenvatting, die essentiële gegevens met betrekking tot uw SMS omvat. Deze metriek omvat gedetailleerde inzichten in het gerichte publiek en de daadwerkelijke leveringsstatus, die een goed-afgeronde mening van de doeltreffendheid en het bereik van uw berichten van SMS verstrekken.

+++ Meer informatie over pushberichten - statistische gegevens totaal verzenden

* **[!UICONTROL Targeted]**: Aantal gebruikersprofielen dat als doelprofielen voor het kanaal van SMS kwalificeert.

* **[!UICONTROL Sent]**: Totaal aantal verzonden SMS-berichten.

* **[!UICONTROL Delivered]**: Aantal SMS-berichten dat is verzonden in verhouding tot het totale aantal verzonden SMS-berichten.

* **[!UICONTROL Delivery Rate]**: Percentage SMS-berichten verzonden.

* **[!UICONTROL Bounces]**: Totaal aantal gecumuleerde fouten en automatische retourverwerking in verhouding tot het totale aantal verzonden SMS-berichten.

* **[!UICONTROL Bounce Rate]**: Percentage van SMS-berichten dat wordt teruggestuurd in vergelijking met verzonden SMS-berichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden waardoor deze niet naar profielen kon worden verzonden.

* **[!UICONTROL Error Rate]**: percentage fouten dat voorkwam voorkómen dat het werd verzonden vergeleken met verzonden SMS-berichten.

* **[!UICONTROL Excluded]**: Aantal gebruikersprofielen dat is uitgesloten van de doelprofielen en dat het bericht niet heeft ontvangen.

* **[!UICONTROL Exclude rate]**: Percentage profielen dat door Adobe Journey Optimizer is uitgesloten.

+++

### SMS - Totaal aantal volgstatistieken {#sms-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics"
>title="SMS - Totaal aantal volgstatistieken"
>abstract="De statistieken voor het bijhouden van SMS - Totaal bieden gegevens over profielactiviteiten voor je SMS-berichten."

![](assets/channel_sms_tracking.png)

De **[!UICONTROL SMS - Total tracking statistics]** widget geeft een gedetailleerd overzicht van belangrijke informatie over de betrokkenheid van uw bezoekers bij uw URL&#39;s en biedt inzichten in de effectiviteit van uw SMS-berichten:

* **[!UICONTROL Clicks]**: Het aantal keren dat er op de inhoud is geklikt in het SMS-bericht.

### SMS - Statistieken over een tijdsverloop verzenden {#sms-sending-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics_overtime"
>title="SMS - Statistieken over een tijdsverloop verzenden"
>abstract="De sms - Verzendstatistieken in tijdgrafiek geven gegevens weer betreffende verzonden sms - berichten, uitgesplitst op uur, dag, week, of maandbasis."

![](assets/channel_sms_sending_overtime.png)

De **[!UICONTROL SMS - Sending statistics over time]** de grafiek biedt een uitvoerige mening van verzonden SMS berichten, die gegevens verstrekken die op een uur, dag, wekelijkse, of maandbasis worden uitgesplitst. Deze grafische vertegenwoordiging staat u toe om tendensen in uw het overseinenactiviteit van SMS over verschillende tijdintervallen te volgen en te analyseren.

+++ Meer informatie over SMS - Statistieken verzenden over tijdsmetingen

* **[!UICONTROL Sent]**: Totaal aantal verzonden SMS-berichten.

* **[!UICONTROL Bounces]**: Totaal aantal gecumuleerde fouten en automatische retourverwerking in verhouding tot het totale aantal verzonden SMS-berichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden waardoor deze niet naar profielen kon worden verzonden.

+++

### SMS - Statistieken bijhouden in de loop der tijd {#sms-tracking-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics_overtime"
>title="SMS - Statistieken bijhouden in de loop der tijd"
>abstract="De sms - het Volgen statistieken over tijdsgrafiek verstrekt gegevens over profielactiviteit voor uw sms- berichten, die op een uur, dag, wekelijkse, of maandbasis worden uitgesplitst."

![](assets/channel_sms_tracking_overtime.png)

De **[!UICONTROL SMS - Tracking statistics over time]** de grafiek verstrekt gegevens over profielactiviteit met betrekking tot uw berichten van SMS, die een gedetailleerde uitsplitsing op een uur, dag, wekelijkse, of maandbasis aanbieden. Met deze grafische weergave kunt u patronen in de betrokkenheid van gebruikers analyseren en begrijpen in verschillende tijdsintervallen.

* **[!UICONTROL Clicks]**: Het aantal keren dat er op de inhoud is geklikt in het SMS-bericht.

### Uitgesloten redenen {#sms-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_excluded_reasons"
>title="Uitgesloten redenen"
>abstract="In de grafieken en de tabel met uitgesloten redenen worden de verschillende factoren weergegeven die hebben geleid tot gebruikersprofielen die zijn uitgesloten van het doelpubliek en die het bericht niet ontvangen."

![](assets/channel_sms_excluded.png)

De **[!UICONTROL Excludes Reasons]** in grafieken en tabellen worden visueel de verschillende factoren weergegeven die hebben geleid tot de uitsluiting van gebruikersprofielen van het beoogde publiek, zodat gebruikers uw SMS-berichten niet kunnen ontvangen.

Zie [deze pagina](exclusion-list.md) voor de volledige lijst van uitsluitingsredenen.

### Stuitingsredenen {#sms-bounce-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_bounce_reasons"
>title="Stuitingsredenen"
>abstract="De grafieken en de tabel met Bounces Reasons bevatten de beschikbare gegevens met betrekking tot berichten die worden teruggestuurd."

![](assets/channel_sms_bounce_reasons.png)

De **[!UICONTROL Bounces Reasons]** grafieken en tabellen bieden een uitgebreid overzicht van de gegevens met betrekking tot verzonden SMS-berichten en bieden waardevolle inzichten in de specifieke redenen achter sms-berichten.

### Foutredenen {#sms-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_error_reasons"
>title="Foutredenen"
>abstract="Met de grafieken en de tabel met oorzaken van fouten kunt u de specifieke fouten identificeren die tijdens het verzendingsproces zijn opgetreden."

De **[!UICONTROL Error Reasons]** Met grafieken en tabellen kunt u de specifieke fouten identificeren die zijn opgetreden tijdens het verzenden van uw SMS-berichten. Zo kunt u een grondige analyse van alle ondervonden problemen maken.

## Direct mail {#direct-mail}

Van uw **Kanaal** de **Directe post** bevat de belangrijkste informatie met betrekking tot de direct-mailberichten die in uw **Campagnes** en **Reizen**. De methodes worden hieronder gedetailleerd.

### Directe post - Totale verzendende statistieken {#direct-mail-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_sending_statistics"
>title="Directe post - Totale verzendende statistieken"
>abstract="Direct post - het Totaal verzenden van statistieken KPIs vat essentiële gegevens over uw direct-mailberichten zoals Gericht of Geleverd samen."

![](assets/channel_direct_sending.png)

De **[!UICONTROL Direct mail - Total sending statistics]** widget biedt een uitgebreid overzicht van de prestaties van uw direct-mailberichten, die zeer belangrijke prestatiesindicatoren (KPIs) tonen die essentiële gegevens over uw direct-mailberichten samenvatten.

+++ Meer informatie over Direct mail - cijfers over totale verzendstatistieken

* **[!UICONTROL Targeted]**: Aantal gebruikersprofielen dat als doelprofielen voor uw direct-mailberichten wordt gekwalificeerd.

* **[!UICONTROL Sent]**: Totaal aantal verzendingen.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden waardoor deze niet naar profielen kon worden verzonden.

* **[!UICONTROL Error Rate]**: percentage fouten dat ervoor zorgde dat deze niet konden worden verzonden, vergeleken met verzonden pushberichten.

* **[!UICONTROL Excluded]**: Aantal gebruikersprofielen dat is uitgesloten van de doelprofielen en dat het bericht niet heeft ontvangen.

* **[!UICONTROL Exclude rate]**: Percentage profielen dat door Adobe Journey Optimizer is uitgesloten.

+++

### Uitgesloten redenen {#direct-mail-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_excluded_reasons"
>title="Uitgesloten redenen"
>abstract="In de grafieken en de tabel met uitgesloten redenen worden de verschillende factoren weergegeven die hebben geleid tot gebruikersprofielen die zijn uitgesloten van het doelpubliek en die het bericht niet ontvangen."

![](assets/channel_direct_excluded.png)

De **[!UICONTROL Direct Mail - Excluded reasons]** in grafieken en tabellen worden visueel de verschillende factoren geïllustreerd die ertoe hebben geleid dat gebruikersprofielen zijn uitgesloten van het doelpubliek, zodat deze geen directe-mailberichten kunnen ontvangen.

Zie [deze pagina](exclusion-list.md) voor de volledige lijst van uitsluitingsredenen.

### Foutredenen {#direct-mail-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_error_reasons"
>title="Foutredenen"
>abstract="Met de grafieken en de tabel met oorzaken van fouten kunt u de specifieke fouten identificeren die tijdens het verzendingsproces zijn opgetreden."

![](assets/channel_direct_error.png)

De **[!UICONTROL Direct Mail - Error reasons]** voorzien in de middelen om specifieke fouten te identificeren die tijdens het verzendingsproces van uw direct-mailberichten voorkwamen, die voor een gedetailleerde analyse van om het even welke ondervonden kwesties toestaan.

## In-app {#in-app}

Uit uw Channel-rapporten vindt u in het menu In-app de belangrijkste informatie over berichten in de app die in uw campagnes en reizen worden verzonden. De cijfers worden hieronder beschreven.

### Totale betrokkenheid in de app {#inapp-total-engagement}

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement"
>title="In-app - totale betrokkenheid"
>abstract="De in-app - totale betrokkenheid-KPI&#39;s bieden uitgebreide informatie over de betrokkenheid van uw bezoekers bij uw in-app-berichten, waaronder metriek zoals Impressies en Interacties."

![](assets/channel_inapp_engagement.png)

De **[!UICONTROL In-app total engagement]** KPI&#39;s bieden uitgebreide inzichten in de betrokkenheid van uw bezoekers bij uw In-app-berichten, die belangrijke meetgegevens bevatten, zoals **Impressies** en **Interacties**.

+++ Meer informatie over de totale betrokkenheidswaarden in de app

* **[!UICONTROL Impressions]**: Het totale aantal in-app berichten dat aan alle gebruikers wordt geleverd.

* **[!UICONTROL Interactions]**: Totaal aantal contracten met uw In-app-bericht. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken, ontslag of andere interactie.

+++

### Overuren van betrokkenheid binnen de app {#inapp-engagement-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement_overtime"
>title="In-app - Betrokkenheid bij overuren"
>abstract="In de overloopgrafiek in de app - De overloopgrafiek van de betrokkenheid houdt in-app beelden en interacties bij, die uurs, dagelijks, wekelijks, en maandonderbrekingen verstrekken."

![](assets/channel_inapp_engagement_overtime.png)

De **[!UICONTROL In-app engagement overtime]** in de grafiek wordt de ontwikkeling van uw In-app-indrukkingen en -interacties voor de desbetreffende periode weergegeven door elke indruk, afwijzing of interactie te volgen.

+++ Meer informatie over metrische gegevens over in-app betrokkenheid bij overwerk

* **[!UICONTROL Impressions]**: Het totale aantal in-app berichten dat aan alle gebruikers wordt geleverd.

* **[!UICONTROL Interactions]**: Totaal aantal contracten met uw In-app-bericht. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken, ontslag of andere interactie.

+++

## Web {#web}

Van uw **Kanaal** rapporten, detailleert het menu van het Web de belangrijkste informatie met betrekking tot Web-pagina&#39;s inbegrepen in uw **Campagnes** en **Reizen**. De cijfers worden hieronder beschreven.

### Web - totale betrokkenheid {#web-engagement-total}

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement"
>title="Web - totale betrokkenheid"
>abstract="De Web - Totale betrokkenheid KPIs verstrekken uitvoerige informatie over de betrokkenheid van uw bezoekers bij uw Web-pagina&#39;s, met inbegrip van metriek zoals Impressies en Interacties."

![](assets/channel_web_engagement.png)

De **[!UICONTROL Web total engagement]** KPI&#39;s bieden uitgebreide inzichten in de betrokkenheid van uw bezoekers bij uw webpagina&#39;s, die belangrijke metriek omvatten, zoals impressies en interacties.

+++ Meer informatie over de totale betrokkenheid op het web

* **[!UICONTROL Impressions]**: Het totale aantal webervaringen dat aan alle gebruikers wordt geleverd.

* **[!UICONTROL Interactions]**: Het totale aantal contracten met uw webpagina. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken of andere interacties.

+++

### Web - Totale betrokkenheid overuren {#web-engagement-total-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement_overtime"
>title="Web - Totale betrokkenheid overuren"
>abstract="De Web - de grafiek van de Betrokkenheid overwerk volgt uw Web-pagina&#39;s indrukken en interactie, die uurs, dagelijks, wekelijks, en maanduitsplitsingen verstrekken."

![](assets/channel_web_engagement_overtime.png)

De **[!UICONTROL Web engagement overtime]** de grafiek controleert **Impressies** en **Interacties** van uw webpagina&#39;s, met gedetailleerde uitsplitsingen per uur, dag, week en maand.

+++ Meer informatie over de metriek van overwerk bij webbetrokkenheid

* **[!UICONTROL Impressions]**: Het totale aantal webervaringen dat aan alle gebruikers wordt geleverd.

* **[!UICONTROL Interactions]**: Het totale aantal contracten met uw webpagina. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken of andere interacties.

+++

## Kanaalrapport (video) {#channel-report-video}

Leer hoe u rapporten op kanaalniveau in deze video kunt openen, navigeren en exporteren

>[!VIDEO](https://video.tv.adobe.com/v/3424537?quality=12)
