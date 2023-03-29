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
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '1707'
ht-degree: 0%

---

# Globaal verslag campagne voeren {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="Globaal verslag campagne voeren"
>abstract="Met het algemene rapport Campagne kunt u het effect van uw campagnes over een bepaalde tijdsperiode meten. Uw rapport is verdeeld in verschillende widgets waarin het succes en de fouten van uw campagne worden beschreven. Elk rapportdashboard kan worden gewijzigd door widgets te vergroten of te verkleinen of te verwijderen."

Het algemene rapport van de campagne kan direct van uw Campagne met het **[!UICONTROL View report]** knop.

![](assets/campaign_report_global_5.png)

De campagne **[!UICONTROL Global report]** Deze pagina wordt weergegeven met de volgende tabbladen:

* [Campaign](#campaign-global)
* [Email](#email-global)
* [In-app](#inapp-global)
* [Push](#push-global)
* [Sms](#sms-global)

De campagne **[!UICONTROL Global report]** is verdeeld in verschillende widgets waarin het succes en de fouten van uw campagne worden beschreven. Elke widget kan indien nodig worden vergroot of verkleind en verwijderd. Raadpleeg voor meer informatie hierover [sectie](../reports/global-report.md#modify-dashboard).

Voor een gedetailleerde lijst van elke metrisch beschikbaar in Adobe Journey Optimizer, verwijs naar [deze pagina](global-report.md#list-of-components-global.md)

## Tabblad Campagne {#campaign-global}

### Levering {#delivery-global}

![](assets/campaign_report_global_1.png)

De **[!UICONTROL Campaign's Statistics]** widget geeft de belangrijkste informatie met betrekking tot uw campagne:

* **[!UICONTROL Entered profiles]**: Aantal profielen dat de reis is begonnen.

* **[!UICONTROL Actions delivered]**: Het totale aantal unieke tijden dat een actie in de reis is uitgevoerd.

* **[!UICONTROL Actions failed in %]**: Het totale aantal unieke tijden dat een actie tijdens de reis is mislukt in verhouding tot het totale aantal unieke tijden dat een actie is uitgevoerd.

## Tabblad E-mail {#email-global}

![](assets/campaign_report_global_2.png)

Van uw campagne **[!UICONTROL Global report]** de **[!UICONTROL Email]** bevat de belangrijkste gegevens met betrekking tot de e-mailleveringen die in uw campagne zijn verzonden.

+++ Meer informatie over de verschillende maatstaven en widgets die beschikbaar zijn voor het e-mailrapport.

De **[!UICONTROL Email Sending Statistics]** grafiek geeft het succes van uw levering aan:

* **[!UICONTROL Targeted]**: Het totale aantal berichten dat tijdens de leveringsanalyse wordt verwerkt.

* **[!UICONTROL Sent]**: Het totale aantal verzendt voor de levering.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Delivery Rate]**: Percentage berichten verzonden.

* **[!UICONTROL Bounces]**: Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.

* **[!UICONTROL Bounce Rate]**: Percentage van e-mails dat is teruggestuurd in vergelijking met verzonden e-mails.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

* **[!UICONTROL Error Rate]**: Percentage fouten die optraden tijdens een levering waardoor deze niet kon worden verzonden, vergeleken met verzonden e-mailberichten.

* **[!UICONTROL Retries]**: Aantal e-mails in de wachtrij voor nieuwe pogingen.

* **[!UICONTROL Excluded]**: Aantal profielen dat door Adobe Journey Optimizer is uitgesloten.

De **[!UICONTROL Email - Tracking statistics]** widget bevat de beschikbare gegevens voor de activiteit van de ontvanger voor uw levering:

* **[!UICONTROL Opens]**: Aantal keren dat de levering is geopend in een levering.

* **[!UICONTROL Unique Opens]**: Percentage geopende leveringen.

* **[!UICONTROL Open Rate]**: Het totale aantal geopende e-mails in verhouding tot het aantal geleverde e-mails.

* **[!UICONTROL Clicks]**: Aantal keer dat er op een inhoud in een e-mail is geklikt.

* **[!UICONTROL Unique Clicks]**:Aantal ontvangers die op een inhoud in een e-mail hebben geklikt.

* **[!UICONTROL Unique Click Rate]**: Percentage gebruikers dat interactie had met de levering.

* **[!UICONTROL Unsubscriptions]**: Aantal klikken op de verbinding van het unsubscription.

* **[!UICONTROL Spam complaints]**: Aantal keren dat een bericht als spam of junk werd verklaard.

De **[!UICONTROL Sending Statistics]** De grafiek bevat de gegevens die beschikbaar zijn voor verzonden e-mailberichten, zoals:

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounces]**: Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.

* **[!UICONTROL Retries]**: Aantal e-mails in de wachtrij voor nieuwe pogingen.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

De **[!UICONTROL Bounce Reasons]** en **[!UICONTROL Bounce categories]** widgets bevatten de beschikbare gegevens met betrekking tot berichten die worden teruggestuurd, zoals:

* **[!UICONTROL Hard bounce]**: Het totale aantal permanente fouten, zoals een onjuist e-mailadres. Dit omvat een foutbericht waarin expliciet wordt aangegeven dat het adres ongeldig is, zoals Onbekende gebruiker.

* **[!UICONTROL Soft bounce]**: Het totale aantal tijdelijke fouten, zoals een volledig postvak.

* **[!UICONTROL Ignored]**: Het totale aantal tijdelijke gegevens, zoals Buiten-kantoor, of een technische fout, bijvoorbeeld als het type afzender postmaster is.

Voor meer informatie over grenzen raadpleegt u de [Onderdrukkingslijst](../reports/suppression-list.md) pagina.

De **[!UICONTROL Error Reasons]** de grafiek en de lijst laten u zien welke fout tijdens uw levering voorkwam.

De **[!UICONTROL Excluded reasons]** de grafiek en de lijst tonen de verschillende redenen die gebruikersprofielen, uitgesloten van de gerichte profielen, van het ontvangen van het bericht verhinderden.

De **[!UICONTROL Email - Top Url]** grafiek en lijstdetails die URLs van uw levering het meest bezocht zijn.

De **[!UICONTROL Email - Top recipient domain]** grafiek en lijstdetails welke domeinen het meest door ontvangers worden gebruikt om e-mail te openen.

>[!NOTE]
>
>De **[!UICONTROL Optimized vs non optimized]** en **[!UICONTROL Send time optimization]**  widgets zijn alleen beschikbaar als de optie Send-Time Optimization is geactiveerd voor uw levering. Voor meer informatie over Send-Time Optimization, verwijs naar [deze pagina](../building-journeys/journeys-message.md#send-time-optimization).

De **[!UICONTROL Optimized vs non optimized]** de grafiek geeft de belangrijkste informatie met betrekking tot uw bericht of zij of niet worden geoptimaliseerd:

* **[!UICONTROL Sent]**: Het totale aantal verzendt voor de levering.
* **[!UICONTROL Opens]**: Aantal keren dat de levering is geopend in een levering.
* **[!UICONTROL Clicks]**: Aantal keer dat er op een inhoud in een e-mail is geklikt.

De **[!UICONTROL Send time optimization]** Geeft details over het succes van uw levering afhankelijk van de verzendende methode: geoptimaliseerd of normaal.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.
* **[!UICONTROL Bounces]**: Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.
+++

## Tabblad In-app {#inapp-global}

>[!IMPORTANT]
>
>De functie In-app is momenteel beschikbaar als een bètaversie om alleen gebruikers te selecteren. Neem contact op met de klantenservice van Adobe om deel te nemen aan het bètaprogramma.

Van uw campagne **[!UICONTROL Global report]** de **[!UICONTROL In-app]** bevat de belangrijkste informatie met betrekking tot de in-app-leveringen die in uw campagne zijn verzonden.

![](assets/campaign_report_global_6.png)

+++ Meer informatie over de verschillende maatstaven en widgets die beschikbaar zijn voor het rapport in de app.

De **[!UICONTROL In-app performance]** KPI&#39;s geven een gedetailleerde beschrijving van de belangrijkste informatie over de betrokkenheid van uw bezoekers bij uw In-app-berichten, zoals:

* **[!UICONTROL Unique impressions]**: aantal unieke gebruikers aan wie het In-app-bericht is bezorgd.

* **[!UICONTROL Impressions]**: totaal aantal in-app berichten dat aan alle gebruikers wordt geleverd.

* **[!UICONTROL Click rate]**: percentage gebruikers dat interactie had met de knoppen in het In-app-bericht vergeleken met gebruikers die het bericht hebben gezien.

* **[!UICONTROL Dismiss rate]**: percentage in-app berichten dat ontvangers hebben genegeerd.

De **[!UICONTROL In-app summary]** in de grafiek wordt de ontwikkeling van uw In-app-afbeeldingen voor de desbetreffende periode weergegeven.

De **[!UICONTROL Clicks by button]** de grafiek en de lijst bevatten de beschikbare gegevens voor ontvangend gedrag per knoop:

* **[!UICONTROL Clicks]**: het totale aantal ontvangers dat interactie heeft gehad met de knoppen die in het bericht in de app zijn opgenomen.

* **[!UICONTROL Click rate]**: percentage gebruikers dat interactie had met de knoppen in het In-app-bericht vergeleken met gebruikers die het bericht hebben gezien.
+++

## Tabblad Pushmelding {#push-global}

Van uw campagne **[!UICONTROL Global report]** de **[!UICONTROL Push notification]** bevat de belangrijkste informatie met betrekking tot de pushberichten die in uw campagne worden verzonden.

![](assets/campaign_report_global_3.png)

+++Leer meer op de verschillende metriek en widgets beschikbaar voor het Push- rapport.

De **[!UICONTROL Push notification - Sending statistics]** de tabel bevat de belangrijkste informatie met betrekking tot uw pushberichten met grafiek en PKI&#39;s:

* **[!UICONTROL Targeted]**: Het totale aantal berichten dat tijdens de leveringsanalyse wordt verwerkt.

* **[!UICONTROL Sent]**: Het totale aantal verzendt voor de levering.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Delivery Rate]**: Percentage berichten verzonden.

* **[!UICONTROL Bounces]**: Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.

* **[!UICONTROL Bounce Rate]**: Percentage pushmeldingen dat is teruggestuurd in vergelijking met verzonden pushberichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

* **[!UICONTROL Error Rate]**: Percentage fouten die optraden tijdens een levering waardoor deze niet kon worden verzonden, vergeleken met verzonden pushberichten.

* **[!UICONTROL Excluded]**: Aantal profielen dat door Adobe Journey Optimizer is uitgesloten.

De **[!UICONTROL Push - Tracking statistics]** bevat de beschikbare gegevens voor ontvankelijke activiteit voor uw levering:

* **[!UICONTROL Opens]**: Aantal keren dat een bericht in een levering werd geopend.

* **[!UICONTROL Open Rate]**: Percentage geopende pushmeldingen.

* **[!UICONTROL Actions]**: Het totale aantal acties op de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

* **[!UICONTROL Engagements]**: Het totale aantal keren dat wordt geopend en de acties voor deze pushmelding, bijvoorbeeld als het profiel de pushmelding heeft geopend of als op een knop is geklikt.

* **[!UICONTROL Engagement Rate]**: Percentage van het aantal keren dat wordt geopend en handelingen voor deze pushmelding, bijvoorbeeld als het profiel de pushmelding heeft geopend of als op een knop is geklikt.

De **[!UICONTROL Push notification summary]** De grafiek bevat de gegevens die beschikbaar zijn voor verzonden pushberichten, zoals:

* **[!UICONTROL Opens]**: Aantal keren dat een bericht in een levering werd geopend.

* **[!UICONTROL Actions]**: Het totale aantal acties op de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

* **[!UICONTROL Bounces]**: Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

>[!NOTE]
>
>De **[!UICONTROL Optimized vs non optimized]** en **[!UICONTROL Send time optimization]**  widgets zijn alleen beschikbaar als de optie Send-Time Optimization is geactiveerd voor uw levering. Voor meer informatie over Send-Time Optimization, verwijs naar [deze pagina](../building-journeys/journeys-message.md#send-time-optimization).

De **[!UICONTROL Optimized vs non optimized]** de grafiek geeft de belangrijkste informatie met betrekking tot uw bericht of zij of niet worden geoptimaliseerd:

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.
* **[!UICONTROL Opens]**: Aantal keren dat de levering is geopend in een levering.
* **[!UICONTROL Actions]**: Het totale aantal acties op de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

De **[!UICONTROL Send time optimization]** Geeft details over het succes van uw levering afhankelijk van de verzendende methode: geoptimaliseerd of normaal.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.
* **[!UICONTROL Bounces]**: Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.

De **[!UICONTROL Error Reasons]** de grafiek en de lijst laten u zien welke fout tijdens uw levering voorkwam.

De **[!UICONTROL Excluded reasons]** de grafiek en de lijst tonen de verschillende redenen die gebruikersprofielen, uitgesloten van de gerichte profielen, van het ontvangen van het bericht verhinderden.

De **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** en **[!UICONTROL Breakdown by platform]** grafieken en tabellen geven het succes van uw pushmelding weer, afhankelijk van het besturingssysteem van de ontvanger.
+++

## Tabblad SMS {#sms-global}

Van uw campagne **[!UICONTROL Global report]** de **[!UICONTROL SMS]** bevat de belangrijkste informatie met betrekking tot de SMS-leveringen die in uw campagne zijn verzonden.

![](assets/campaign_report_global_4.png)

+++Meer informatie over de verschillende maatstaven en widgets die beschikbaar zijn voor het SMS-rapport.

De **[!UICONTROL SMS - Sending statistics]** de tabel geeft het succes van uw levering aan :

* **[!UICONTROL Targeted]**: Aantal gebruikersprofielen dat als doelprofielen voor deze levering in aanmerking komt.

* **[!UICONTROL Excluded]**: Aantal gebruikersprofielen dat is uitgesloten van de doelprofielen en dat het bericht niet heeft ontvangen.

* **[!UICONTROL Sent]**: Het totale aantal verzendt voor de levering.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounces]**: Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

De **[!UICONTROL SMS Performance by date]** widget geeft de belangrijkste informatie met betrekking tot uw bericht met een grafiek:

* **[!UICONTROL Sent]**: Het totale aantal verzendt voor de levering.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounces]**: Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

De **[!UICONTROL Exclude Reasons]**, **[!UICONTROL Bounces Reasons]** en **[!UICONTROL Error Reasons]** in grafieken en tabellen kunt u zien welke fout en uitsluitingen tijdens de levering zijn opgetreden.

De **[!UICONTROL SMS - Clicks by links]** en **[!UICONTROL SMS - Tracking statistics]** widgets bevatten gedetailleerde informatie over de belangrijkste informatie met betrekking tot de betrokkenheid van uw bezoekers bij uw URL&#39;s.

+++

## Aanvullende bronnen

* [Aan de slag met campagnes](../campaigns/get-started-with-campaigns.md)
* [Een campagne maken](../campaigns/create-campaign.md)
* [API-gestuurde campagnes maken](../campaigns/api-triggered-campaigns.md)
* [Een campagne wijzigen of stoppen](../campaigns/modify-stop-campaign.md)
* [Campagne live-rapport](campaign-live-report.md)
