---
solution: Journey Optimizer
product: journey optimizer
title: Campagne live-rapport
description: Leer hoe u gegevens uit het live rapport over campagne kunt gebruiken
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: adcfff1cb8bb2ae98d41e4071f56a137e52ee56a
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 0%

---

# Campagne live-rapport {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="Campagne live-rapport"
>abstract="Met het live rapport Campagne kunt u de impact en prestaties van uw campagnes in real-time alleen in de afgelopen 24 uur meten en visualiseren. Uw rapport is verdeeld in verschillende widgets waarin het succes en de fouten van uw campagne worden beschreven. Elk rapportdashboard kan worden gewijzigd door widgets te vergroten of te verkleinen of te verwijderen."

Live rapporten, die toegankelijk zijn vanaf het tabblad Laatste 24 uur, geven gebeurtenissen weer die in de afgelopen 24 uur hebben plaatsgevonden, met een minimale tijdsinterval van twee minuten vanaf de gebeurtenis. Globale rapporten richten zich daarentegen op gebeurtenissen die zich minstens twee uur geleden hebben voorgedaan en bestrijken gebeurtenissen gedurende een geselecteerde tijdsperiode.

U kunt het live campagnerapport rechtstreeks vanuit uw campagne openen via de **[!UICONTROL Live view]** knop.

De campagne **[!UICONTROL Live report]** Deze pagina wordt weergegeven met de volgende tabbladen:

* [Campaign](#campaign-live)
* [Email](#email-live)
* [In-app](#inapp-live)
* [Push](#push-live)
* [Sms](#sms-live)
* [Web](#web-tab)
* [Direct mail](#direct-mail-tab)

De campagne **[!UICONTROL Live report]** is verdeeld in verschillende widgets waarin het succes en de fouten van uw campagne worden beschreven. Elke widget kan indien nodig worden vergroot of verkleind en verwijderd. Raadpleeg voor meer informatie hierover [sectie](../reports/live-report.md#modify-dashboard).

Voor een gedetailleerde lijst van elke metrisch beschikbaar in Adobe Journey Optimizer, verwijs naar [deze pagina](live-report.md#list-of-components-live).

## Tabblad Campagne {#campaign-live}

### Levering {#delivery-live}

De **[!UICONTROL Campaign Statistics]** widget geeft de belangrijkste informatie met betrekking tot uw campagne:

* **[!UICONTROL Entered profiles]**: Aantal profielen dat de reis is gestart.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## Tabblad E-mail {#email-live}

Van uw campagne **[!UICONTROL Live report]** de **[!UICONTROL Email]** bevat de belangrijkste informatie met betrekking tot de e-mailleveringen die in uw campagne zijn verzonden.

![](assets/campaign_report_live_1.png)

+++ Meer informatie over de verschillende maatstaven en widgets die beschikbaar zijn voor het e-mailrapport.

De **[!UICONTROL Email Sending Statistics]** widget geeft details over de belangrijkste informatie met betrekking tot uw bericht:

* **[!UICONTROL Delivered]**: Aantal verzonden berichten.

* **[!UICONTROL Bounces]**: Totaal aantal fouten gecumuleerd tijdens levering en automatische terugzendverwerking.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

De **[!UICONTROL Sending metrics by Email]** tabel en **[!UICONTROL Email Summary]** grafiek geeft het succes van uw levering aan:

* **[!UICONTROL Sent]**: Totaal aantal verzendingen voor de levering.

* **[!UICONTROL Delivered]**: Aantal verzonden berichten.

* **[!UICONTROL Bounces]**: Totaal aantal fouten gecumuleerd tijdens levering en automatische terugzendverwerking.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

* **[!UICONTROL Opens]**: Aantal keren dat een bericht is geopend in een levering.

* **[!UICONTROL Clicks]**: Het aantal keren dat op een inhoud is geklikt in een levering.

* **[!UICONTROL Unsubscribe]**: Het aantal klikken op de koppeling voor het opzeggen van abonnementen.

* **[!UICONTROL Spam complaints]**: Het aantal keren dat een bericht is gedeclareerd als spam of junk.

De **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** en **[!UICONTROL Hard and bounce - by Email]** widgets bevatten de beschikbare gegevens met betrekking tot berichten die worden teruggestuurd, zoals:

* **[!UICONTROL Hard bounce]**: Het totale aantal permanente fouten, zoals een onjuist e-mailadres. Dit omvat een foutbericht waarin expliciet wordt aangegeven dat het adres ongeldig is, zoals Onbekende gebruiker.

* **[!UICONTROL Soft bounce]**: Het totale aantal tijdelijke fouten, zoals een volledig postvak.

* **[!UICONTROL Ignored]**: Het totale aantal tijdelijke berichten, zoals Buiten-kantoor, of een technische fout, bijvoorbeeld als het type afzender postmaster is.

De **[!UICONTROL Error Reasons]** en **[!UICONTROL Exclude Reasons]** in grafieken en tabellen kunt u zien welke fout en uitsluitingen tijdens de levering zijn opgetreden.

De **[!UICONTROL Email - Top recipient domain]** grafiek en lijstdetails welke domeinen het meest door ontvangers worden gebruikt om e-mail te openen.
+++

## Tabblad In-app {#inapp-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_performance"
>title="Prestaties in de app"
>abstract="De prestatie-KPI&#39;s in de app bieden essentiële inzichten in de betrokkenheid van uw bezoekers bij In-app-berichten in de afgelopen 24 uur."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_interactions"
>title="Interacties per type"
>abstract="De interacties per type grafieken en de lijstdetails hoe de gebruikers met uw in-app bericht in wisselwerking stonden door om het even welke klik te volgen, te ontslaan, of interactie van de laatste 24 uren."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_summary"
>title="Overzicht in de app"
>abstract="De overzichtsgrafiek in de app illustreert de voortgang van uw impressies en interacties in de app in de afgelopen 24 uur."

Van uw campagne **[!UICONTROL Live report]** de **[!UICONTROL In-app]** bevat de belangrijkste informatie met betrekking tot de in-app-leveringen die in uw campagne zijn verzonden.

+++ Meer informatie over de verschillende maatstaven en widgets die beschikbaar zijn voor het rapport in de app.

De **[!UICONTROL In-app performance]** KPI&#39;s geven een gedetailleerde beschrijving van de belangrijkste informatie over de betrokkenheid van uw bezoekers bij uw In-app-berichten, zoals:

* **[!UICONTROL Impressions]**: totaal aantal in-app berichten dat aan alle gebruikers is bezorgd.

* **[!UICONTROL Interactions]**: totaal aantal contracten met uw In-app-bericht. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken, ontslag of andere interactie.

De **[!UICONTROL In-app summary]** in de grafiek wordt de ontwikkeling van uw In-app-afbeeldingen en -interacties voor de desbetreffende periode weergegeven.

De **[!UICONTROL Interactions by type]** grafieken en tabellen geven aan hoe gebruikers met uw bericht in de app hebben gewerkt door een klik, sluiting of interactie bij te houden.

+++

## Tabblad Pushmelding {#push-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_performance"
>title="Pushmelding - Prestaties verzenden"
>abstract="De grafiek van de Prestaties bij verzenden van pushberichten geeft een overzicht van de belangrijkste gegevens over uw pushberichten, zoals Fouten of Geleverde berichten van de afgelopen 24 uur."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_statistics"
>title="Pushmeldingen - Statistieken"
>abstract="De lijst van de Statistieken van de Duw verstrekt gegevens over ontvankelijke activiteit voor uw levering van de laatste 24 uren."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_summary"
>title="Pushmelding - Samenvatting verzenden"
>abstract="In de grafiek Samenvatting van pushmeldingen worden de gegevens weergegeven die beschikbaar zijn voor verzonden pushberichten van de laatste 24 uur."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_excluded_reasons"
>title="Pushmelding - Uitgesloten redenen"
>abstract="De grafieken en tabel met uitgesloten redenen illustreren de verschillende factoren die hebben geleid tot gebruikersprofielen die zijn uitgesloten van het doelpubliek en die het bericht in de afgelopen 24 uur niet hebben ontvangen."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_error_reasons"
>title="Pushmelding - Foutredenen"
>abstract="Met de grafieken en de tabel met oorzaken van fouten kunt u de specifieke fouten identificeren die zich de laatste 24 uur tijdens de levering hebben voorgedaan."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_breakdown_platform"
>title="Pushmelding - Onderverdeling per platform"
>abstract="De grafieken en tabel in de indeling Uitsplitsing naar platform geven een overzicht van het succes van uw pushberichten in de afgelopen 24 uur, afhankelijk van het besturingssysteem van de ontvanger."

Van uw campagne **[!UICONTROL Live report]** de **[!UICONTROL Push notification]** bevat de belangrijkste informatie met betrekking tot de pushberichten die in uw campagne worden verzonden.

![](assets/campaign_report_live_2.png)

+++Leer meer op de verschillende metriek en widgets beschikbaar voor het Push- rapport.

**[!UICONTROL Push notification sending performance]**, **[!UICONTROL Push notification summary]** en **[!UICONTROL Push notification - Statistics]** widgets geeft details over de belangrijkste informatie met betrekking tot uw bericht:

* **[!UICONTROL Sent]**: Totaal aantal verzendingen voor de levering.

* **[!UICONTROL Delivered]**: Aantal verzonden berichten.

* **[!UICONTROL Bounces]**: Totaal aantal fouten gecumuleerd tijdens levering en automatische terugzendverwerking.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

* **[!UICONTROL Opens]**: Aantal keren dat een bericht is geopend in een levering.

* **[!UICONTROL Actions]**: Totaal aantal acties op de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

* **[!UICONTROL Engagements]**: Het totale aantal keren dat wordt geopend en de acties voor deze pushmelding, bijvoorbeeld als het profiel de pushmelding heeft geopend of als op een knop is geklikt.

De **[!UICONTROL Error Reasons]** en **[!UICONTROL Exclude Reasons]** in grafieken en tabellen kunt u zien welke fout en uitsluitingen tijdens de levering zijn opgetreden.

De **[!UICONTROL Sending statistics - Failed]** met widget kunt u zien hoeveel fouten en golven er zijn opgetreden.

De **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** en **[!UICONTROL Breakdown by platform]** in grafieken en tabellen wordt aangegeven hoe succesvol uw pushmelding is, afhankelijk van het besturingssysteem.
+++

## Tabblad SMS {#sms-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_statistics"
>title="SMS - Statistieken"
>abstract="De SMS die Statistieken verzendt vat essentiële gegevens over uw SMS berichten zoals Gerichte of Geleide berichten van de laatste 24 uren samen."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_performance"
>title="SMS - Prestaties op datum"
>abstract="De widget Prestaties per datum van SMS biedt via een grafische weergave belangrijke informatie van de laatste 24 uur over uw berichten."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_error_reasons"
>title="SMS - Redenen voor fouten"
>abstract="Met SMS - Foutgrafieken en -tabel kunt u de specifieke fouten identificeren die zich de laatste 24 uur tijdens de levering hebben voorgedaan."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_excluded_reasons"
>title="SMS - Uitgesloten redenen"
>abstract="De grafieken en tabel met uitgesloten redenen illustreren de verschillende factoren die hebben geleid tot gebruikersprofielen die zijn uitgesloten van het doelpubliek en die het bericht in de afgelopen 24 uur niet hebben ontvangen."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_bounces_reasons"
>title="SMS - Bounges redenen"
>abstract="De grafieken en de tabel met Bounces Reasons bevatten de gegevens die beschikbaar zijn in de laatste 24 uur met betrekking tot berichten die worden teruggestuurd."

Van uw campagne **[!UICONTROL Live report]** de **[!UICONTROL SMS]** bevat de belangrijkste informatie met betrekking tot de SMS-leveringen die in uw campagne zijn verzonden.

![](assets/campaign_report_live_3.png)

+++Meer informatie over de verschillende maatstaven en widgets die beschikbaar zijn voor het SMS-rapport.

De **[!UICONTROL SMS - Statistics]** de tabel geeft het succes van uw levering aan :

* **[!UICONTROL Targeted]**: Aantal gebruikersprofielen dat als doelprofielen voor deze levering in aanmerking komt.

* **[!UICONTROL Excluded]**: Aantal gebruikersprofielen dat is uitgesloten van de doelprofielen en dat het bericht niet heeft ontvangen.

* **[!UICONTROL Sent]**: Totaal aantal verzendingen voor de levering.

* **[!UICONTROL Bounces]**: Totaal aantal fouten gecumuleerd tijdens levering en automatische terugzendverwerking.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

* **[!UICONTROL Clicks]**: Totaal aantal URL-bezoeken.

De **[!UICONTROL SMS Performance by date]** widget geeft de belangrijkste informatie met betrekking tot uw bericht met een grafiek:

* **[!UICONTROL Sent]**: Totaal aantal verzendingen voor de levering.

* **[!UICONTROL Bounces]**: Totaal aantal fouten gecumuleerd tijdens levering en automatische terugzendverwerking.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

De **[!UICONTROL Exclude Reasons]**, **[!UICONTROL Bounces Reasons]** en **[!UICONTROL Error Reasons]** in grafieken en tabellen kunt u zien welke fout en uitsluitingen tijdens de levering zijn opgetreden.
+++

## Tabblad Web {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_performance"
>title="Webprestaties"
>abstract="De Web Performance KPIs verstrekt uitvoerige informatie over de betrokkenheid van uw bezoekers met uw Webervaringen van de laatste 24 uren."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_summary"
>title="Weboverzicht"
>abstract="De webinvattingsgrafiek illustreert de voortgang van uw webervaringen, inclusief indrukken, unieke indrukken en interacties, vanaf de laatste 24 uur."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_interactions"
>title="Interacties per element"
>abstract="De tabel Interacties per element bevat belangrijke informatie over de betrokkenheid van uw bezoekers bij verschillende elementen op uw webpagina&#39;s in de afgelopen 24 uur."

Van uw campagne **[!UICONTROL Live report]** de **[!UICONTROL Web]** van het lusje details de belangrijkste informatie met betrekking tot uw Web-pagina&#39;s.

+++Leer meer op de verschillende metriek en widgets beschikbaar voor het rapport van het Web.

De **[!UICONTROL Web performance]** KPI&#39;s geven een gedetailleerde beschrijving van de belangrijkste informatie over de betrokkenheid van uw bezoekers bij uw webervaringen, zoals:

* **[!UICONTROL Impressions]**: totaal aantal webervaringen dat aan alle gebruikers wordt geleverd.

* **[!UICONTROL Interactions]**: totaal aantal contracten met uw webpagina. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken of andere interacties.

De **[!UICONTROL Web summary]** in de grafiek wordt de evolutie van uw webervaringen (indrukken, unieke indrukken en interacties) gedurende de laatste 24 uur getoond.

De **[!UICONTROL Interactions by element]** de tabel bevat de belangrijkste informatie over de betrokkenheid van uw bezoekers bij de verschillende elementen op uw webpagina&#39;s.
+++

## Tabblad Direct mail {#direct-mail-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_sending_statistics"
>title="Directe post - Verzendstatistieken"
>abstract="De Direct mail die Lijst van de Statistieken verzendt vat essentiële gegevens van de laatste 24 uur over uw Directe Berichten zoals Gerichte of Geleverde berichten samen."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_error_reasons"
>title="Directe post - de redenen van de Fout"
>abstract="Met de grafieken en de tabel Direct Mail - Error Redons kunt u de specifieke fouten identificeren die zich de afgelopen 24 uur hebben voorgedaan."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_excluded_reasons"
>title="Direct mail - Uitgesloten redenen"
>abstract="De grafiek en tabel met uitgesloten redenen voor Direct Mail illustreren de verschillende factoren die hebben geleid tot gebruikersprofielen die zijn uitgesloten van het doelpubliek en die het bericht in de afgelopen 24 uur niet hebben ontvangen."

Van uw campagne **[!UICONTROL Live report]** de **[!UICONTROL Direct mail]** bevat de belangrijkste informatie met betrekking tot uw Direct-mailleveringen.

![](assets/direct-mail-report_2.png)

+++ Meer informatie over de verschillende maatstaven en widgets die beschikbaar zijn voor het Direct-mailrapport.

De **[!UICONTROL Direct Mail - Sending statistics]** de tabel geeft het succes van uw levering aan :

* **[!UICONTROL Targeted]**: Aantal gebruikersprofielen dat als doelprofielen voor deze levering in aanmerking komt.

* **[!UICONTROL Sent]**: Totaal aantal verzendingen voor de levering.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

* **[!UICONTROL Excluded]**: Aantal gebruikersprofielen dat niet is opgenomen in de doelprofielen en dat de levering niet heeft ontvangen.

De **[!UICONTROL Direct Mail - Excluded reasons]** en **[!UICONTROL Direct Mail - Error reasons]** in grafieken en tabellen kunt u zien welke fout en uitsluitingen tijdens de levering zijn opgetreden.
+++

## Aanvullende bronnen

* [Aan de slag met campagnes](../campaigns/get-started-with-campaigns.md)
* [Een campagne maken](../campaigns/create-campaign.md)
* [API-gestuurde campagnes maken](../campaigns/api-triggered-campaigns.md)
* [Een campagne wijzigen of stoppen](../campaigns/modify-stop-campaign.md)
* [Globaal verslag campagne voeren](campaign-global-report.md)
