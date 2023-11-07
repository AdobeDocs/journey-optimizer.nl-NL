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
source-git-commit: 82b8c9032d6c377cb76acce4d5cc45afb0ddd6ba
workflow-type: tm+mt
source-wordcount: '2124'
ht-degree: 0%

---

# Journaal algemeen rapport {#journey-global-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_global_report"
>title="Journaal algemeen rapport"
>abstract="Met het algemene rapport Journey kunt u de impact van uw reizen over een bepaalde tijdsperiode meten. Uw rapport is verdeeld in verschillende widgets die het succes en de fouten van uw reis gedetailleerd beschrijven. Elk rapportdashboard kan worden gewijzigd door widgets te vergroten of te verkleinen of te verwijderen."

Globale rapporten, toegankelijk vanaf het tabblad Alle tijd, geven gebeurtenissen weer die zich ten minste twee uur geleden hebben voorgedaan en bestrijken gebeurtenissen gedurende een geselecteerde tijdsperiode. In vergelijking hiermee richten Live-rapporten zich op gebeurtenissen die zich in de afgelopen 24 uur hebben voorgedaan, met een minimale tijdsinterval van twee minuten vanaf het plaatsvinden van de gebeurtenis.

Het algemene rapport van de reis kan direct van uw reis met het **[!UICONTROL View report]** knop.

![](assets/report_journey.png)

De reis **[!UICONTROL Global report]** Deze pagina wordt weergegeven met de volgende tabbladen:

* [Reis](#journey-global)
* [Email](#email-global)
* [Push](#push-global)
* [Sms](#sms-global)
* [In-app](#in-app-global)

De reis **[!UICONTROL Global report]** is verdeeld in verschillende widgets waarin het succes en de fouten van uw reis worden beschreven. Elke widget kan indien nodig worden vergroot of verkleind en verwijderd. Raadpleeg voor meer informatie hierover [sectie](global-report.md#modify-dashboard).

Voor een gedetailleerde lijst van elke metrisch beschikbaar in Adobe Journey Optimizer, verwijs naar [deze pagina](global-report.md#list-of-components-global).

## Tabblad Reis {#journey-global}

Vanaf uw reis **[!UICONTROL Global report]** de **[!UICONTROL Journey]** geeft u een duidelijk overzicht van de belangrijkste volgende gegevens over uw reis.

![](assets/journey_global_1.png)

+++Leer meer op de verschillende metriek en widgets beschikbaar voor het rapport van de Reis.

De **[!UICONTROL Journey Performance]** Met widget kunt u het pad van uw doelprofielen stap voor stap bekijken.

De **[!UICONTROL Journey Statistics]** widget geeft de volgende KPI&#39;s weer:

* **[!UICONTROL Entered profiles]**: Totaal aantal personen dat de inreisgebeurtenis van de reis heeft bereikt.

* **[!UICONTROL Exited profiles]**: Totaal aantal personen dat de reis heeft verlaten.

* **[!UICONTROL Failed individual journey]**: Totaal aantal individuele reizen die niet succesvol zijn uitgevoerd.

De **[!UICONTROL Events received by event]**, **[!UICONTROL Events by origin]** en **[!UICONTROL Top events]** met widgets kunt u zien welke van uw **[!UICONTROL Events]** is uitgevoerd via grafieken en tabellen.

**[!UICONTROL Action Performance]**, **[!UICONTROL Action Error Reasons]** en **[!UICONTROL Top Actions]** widgets vertegenwoordigen de meest geslaagde actie en fouten die zijn opgetreden bij het **[!UICONTROL Actions]** werden geactiveerd.

De **[!UICONTROL Top Actions]** tabel bevat de gegevens die beschikbaar zijn voor **[!UICONTROL Actions]**, zoals:

* **[!UICONTROL Actions successfully executed]**: Totaal aantal **[!UICONTROL Actions]** succesvol uitgevoerd voor een reis.

* **[!UICONTROL Error in action]**: Totaal aantal fouten voor **[!UICONTROL Actions]**.

De **[!UICONTROL Consent policies]** in tabel en grafiek wordt het aantal profielen weergegeven dat is uitgesloten van elk beleid in uw aangepaste acties.
Voor meer informatie over aangepaste handelingen raadpleegt u [de gedetailleerde documentatie](../action/about-custom-action-configuration.md).

Houd er rekening mee dat u de dashboards opnieuw moet instellen als deze widgets alleen in uw journalistiek worden weergegeven. Klik hiervoor op **[!UICONTROL Modify]** dan **[!UICONTROL Reset]** boven aan uw rapport.
+++

## Tabblad E-mail {#email-global}

Vanaf uw reis **[!UICONTROL Global report]** de **[!UICONTROL Email]** bevat de belangrijkste informatie met betrekking tot de e-mailleveringen die tijdens uw reis worden verzonden.

![](assets/journey_global_2.png)

+++ Meer informatie over de verschillende maatstaven en widgets die beschikbaar zijn voor het e-mailrapport.

De **[!UICONTROL Email Sending Statistics]** grafiek geeft het succes van uw levering aan:

* **[!UICONTROL Execution time]**: Begintijd van elke uitvoering van uw terugkerende e-mail tijdens uw reis. Als u slechts één of meerdere terugkerende e-mails wilt aanwijzen, selecteert u deze in het menu **[!UICONTROL Execution time]** vervolgkeuzelijst.

* **[!UICONTROL Targeted]**: Het aantal profielen dat is bedoeld voor acties zoals het verzenden van e-mail of sms.

* **[!UICONTROL Sent]**: Totaal aantal verzendingen voor de levering.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Delivery Rate]**: Percentage berichten dat succesvol is verzonden.

* **[!UICONTROL Bounces]**: Totaal aan fouten gecumuleerd tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounce Rate]**: Percentage van e-mails dat is teruggestuurd in vergelijking met verzonden e-mails.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

* **[!UICONTROL Error Rate]**: Percentage fouten die optraden tijdens een levering waardoor deze niet kon worden verzonden, vergeleken met verzonden e-mailberichten.

De **[!UICONTROL Email - Tracking statistics]** bevat de beschikbare gegevens voor ontvankelijke activiteit voor uw levering:

* **[!UICONTROL Execution time]**: Begintijd van elke uitvoering van uw terugkerende e-mail tijdens uw reis. Als u slechts één of meerdere terugkerende e-mails wilt aanwijzen, selecteert u deze in het menu **[!UICONTROL Execution time]** vervolgkeuzelijst.

* **[!UICONTROL Opens]**: Aantal keren dat de levering is geopend in een levering.

* **[!UICONTROL Unique Opens]**: Percentage geopende leveringen.

* **[!UICONTROL Unique Open Rate]**: Het totale aantal geopende e-mails in verhouding tot het aantal geleverde e-mails.

* **[!UICONTROL Clicks]**: Aantal keer dat er op inhoud is geklikt in een e-mail.

* **[!UICONTROL Unique Clicks]**:Aantal ontvangers die op een inhoud in een e-mail hebben geklikt.

* **[!UICONTROL Click through rate]**: Percentage gebruikers die met de reis communiceerden.

* **[!UICONTROL Unsubscribe]**: Het aantal klikken op de koppeling voor het opzeggen van abonnementen.

* **[!UICONTROL Spam complaints]**: Het aantal keren dat een bericht is gedeclareerd als spam of junk.

De **[!UICONTROL Sending Statistics]** De grafiek bevat de gegevens die beschikbaar zijn voor verzonden e-mailberichten, zoals:

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounces]**: Totaal aan fouten gecumuleerd tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

De **[!UICONTROL Bounce Reasons]** en **[!UICONTROL Bounce categories]** widgets bevatten de beschikbare gegevens met betrekking tot berichten die worden teruggestuurd, zoals:

* **[!UICONTROL Hard bounce]**: Het totale aantal permanente fouten, zoals een onjuist e-mailadres. Dit omvat een foutbericht waarin expliciet wordt aangegeven dat het adres ongeldig is, zoals Onbekende gebruiker.

* **[!UICONTROL Soft bounce]**: Het totale aantal tijdelijke fouten, zoals een volledig postvak.

* **[!UICONTROL Ignored]**: Het totale aantal tijdelijke berichten, zoals Buiten-kantoor, of een technische fout, bijvoorbeeld als het type afzender postmaster is.

Voor meer informatie over grenzen raadpleegt u de [Onderdrukkingslijst](../reports/suppression-list.md) pagina.

De **[!UICONTROL Error Reasons]** de grafiek en de lijst laten u zien welke fout tijdens uw levering voorkwam.

De **[!UICONTROL Excluded reasons]** de grafiek en de lijst tonen de verschillende redenen die gebruikersprofielen, uitgesloten van de gerichte profielen, van het ontvangen van het bericht verhinderden.

De **[!UICONTROL Email - Top Url]** grafiek en lijstdetails die URLs van uw levering het meest bezocht zijn.

De **[!UICONTROL Email - Top recipient domain]** grafiek en lijstdetails welke domeinen het meest door ontvangers worden gebruikt om e-mail te openen.

>[!NOTE]
>
>De **[!UICONTROL Optimized vs non optimized]** en **[!UICONTROL Send time optimization]**  widgets zijn alleen beschikbaar als de optie Send-Time Optimization is geactiveerd voor uw levering. Voor meer informatie over Send-Time Optimization, verwijs naar [deze pagina](../building-journeys/journeys-message.md#send-time-optimization).

De **[!UICONTROL Optimized vs non optimized]** de grafiek geeft de belangrijkste informatie met betrekking tot uw bericht of zij of niet worden geoptimaliseerd:

* **[!UICONTROL Sent]**: Totaal aantal verzendingen voor de levering.
* **[!UICONTROL Opens]**: Aantal keren dat de levering is geopend in een levering.
* **[!UICONTROL Clicks]**: Aantal keer dat er op inhoud is geklikt in een e-mail.

De **[!UICONTROL Send time optimization]** bepaalt het succes van uw levering afhankelijk van de verzendende methode: geoptimaliseerd of normaal.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.
* **[!UICONTROL Bounces]**: Totaal aan fouten gecumuleerd tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten.

>[!NOTE]
>
>De widgets en cijfers voor aanbiedingen zijn alleen beschikbaar als een beslissing in een e-mail is ingevoegd. Raadpleeg voor meer informatie over het beheer van de beslissingen het volgende [page](../offers/get-started/starting-offer-decisioning.md).

De **[!UICONTROL Offers statistic]** en **[!UICONTROL Offers statistics]** in de loop der tijd meten de widgets het succes van uw aanbieding en de impact op uw doelgroep. Het detailleert de belangrijkste informatie met betrekking tot uw bericht met KPIs:

* **[!UICONTROL Offer sent]**: Totaal aantal verzendingen voor de aanbieding.

* **[!UICONTROL Offer impression]**: Het aantal keren dat de aanbieding is geopend in een levering.

* **[!UICONTROL Offer clicks]**: Aantal keren dat op een voorstel is geklikt in een levering.

De **[!UICONTROL Offers detailed statistic]** de tabel bevat de beschikbare gegevens voor de activiteit van de ontvanger met uw voorstel:

* **[!UICONTROL Placement name]**: Naam van uw plaatsing die wordt gebruikt om uw voorstel weer te geven. Raadpleeg deze voor meer informatie over plaatsing [page](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Offer name]**: Naam van de aanbieding die in de levering is toegevoegd. Raadpleeg deze voor meer informatie over plaatsing [page](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offer sent]**: Totaal aantal verzendingen voor de aanbieding.

* **[!UICONTROL Offer impression rate]**: Percentage geopende aanbiedingen in verhouding tot het aantal verzonden aanbiedingen.

* **[!UICONTROL Offer click rate]**: Percentage gebruikers dat interactie heeft gehad met het aanbod.
+++

## Tabblad Pushmelding {#push-global}

Vanaf uw reis **[!UICONTROL Global report]** de **[!UICONTROL Push notification]** bevat de belangrijkste informatie met betrekking tot de pushberichten die tijdens uw reis worden verzonden.

![](assets/journey_global_3.png)

+++Leer meer op de verschillende metriek en widgets beschikbaar voor het Push- rapport.

De **[!UICONTROL Push notification - Sending statistics]** de tabel bevat de belangrijkste informatie met betrekking tot uw pushberichten met grafiek en PKI&#39;s:

* **[!UICONTROL Execution time]**: Begintijd van elke uitvoering van uw terugkerende pushmelding tijdens uw reis. Als u slechts één of meerdere terugkerende pushmeldingen wilt activeren, selecteert u deze in het menu **[!UICONTROL Execution time]** vervolgkeuzelijst.

* **[!UICONTROL Targeted]**: Het aantal profielen dat is bedoeld voor acties zoals het verzenden van e-mail of sms.

* **[!UICONTROL Sent]**: Totaal aantal verzendingen voor de levering.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Delivery Rate]**: Percentage berichten dat succesvol is verzonden.

* **[!UICONTROL Bounces]**: Totaal aan fouten gecumuleerd tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounce Rate]**: Percentage pushmeldingen dat is teruggestuurd in vergelijking met verzonden pushmeldingen.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

* **[!UICONTROL Error Rate]**: Percentage fouten die optraden tijdens een levering waardoor deze niet kon worden verzonden, vergeleken met verzonden pushberichten.

De **[!UICONTROL Push - Tracking statistics]** bevat de beschikbare gegevens voor ontvankelijke activiteit voor uw levering:

* **[!UICONTROL Execution time]**: Begintijd van elke uitvoering van uw terugkerende pushmelding tijdens uw reis. Als u slechts één of meerdere terugkerende pushmeldingen wilt activeren, selecteert u deze in het menu **[!UICONTROL Execution time]** vervolgkeuzelijst.

* **[!UICONTROL Opens]**: Aantal keren dat een bericht is geopend in een levering.

* **[!UICONTROL Open Rate]**: Percentage geopende pushmeldingen.

* **[!UICONTROL Actions]**: Totaal aantal acties op de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

* **[!UICONTROL Engagements]**: Het totale aantal keren dat wordt geopend en de acties voor deze pushmelding, bijvoorbeeld als het profiel de pushmelding heeft geopend of als op een knop is geklikt.

* **[!UICONTROL Engagement Rate]**: Percentage van de knoppen en handelingen voor deze pushmelding, bijvoorbeeld als het profiel de pushmelding heeft geopend of als op een knop is geklikt.

De **[!UICONTROL Push notification summary]** De grafiek bevat de gegevens die beschikbaar zijn voor verzonden pushberichten, zoals:

* **[!UICONTROL Opens]**: Aantal keren dat een bericht is geopend in een levering.

* **[!UICONTROL Actions]**: Totaal aantal acties op de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

* **[!UICONTROL Bounces]**: Totaal aan fouten gecumuleerd tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

>[!NOTE]
>
>De **[!UICONTROL Optimized vs non optimized]** en **[!UICONTROL Send time optimization]**  widgets zijn alleen beschikbaar als de optie Send-Time Optimization is geactiveerd voor uw levering. Voor meer informatie over Send-Time Optimization, verwijs naar [deze pagina](../building-journeys/journeys-message.md#send-time-optimization).

De **[!UICONTROL Optimized vs non optimized]** de grafiek geeft de belangrijkste informatie met betrekking tot uw bericht of zij of niet worden geoptimaliseerd:

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.
* **[!UICONTROL Opens]**: Aantal keren dat de levering is geopend in een levering.
* **[!UICONTROL Actions]**: Totaal aantal acties op de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.

De **[!UICONTROL Send time optimization]** bepaalt het succes van uw levering afhankelijk van de verzendende methode: geoptimaliseerd of normaal.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.
* **[!UICONTROL Bounces]**: Totaal aan fouten gecumuleerd tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten.

De **[!UICONTROL Error Reasons]** de grafiek en de lijst laten u zien welke fout tijdens uw levering voorkwam.

De **[!UICONTROL Excluded reasons]** de grafiek en de lijst tonen de verschillende redenen die gebruikersprofielen, uitgesloten van de gerichte profielen, van het ontvangen van het bericht verhinderden.

De **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** en **[!UICONTROL Breakdown by platform]** grafieken en tabellen geven het succes van uw pushmelding weer, afhankelijk van het besturingssysteem van de ontvanger.

Het SMS **[!UICONTROL Global report]** is verdeeld in verschillende widgets waarin het succes en de fouten van uw levering worden beschreven. Elke widget kan indien nodig worden vergroot of verkleind en verwijderd. Zie voor meer informatie hierover [sectie](global-report.md#modify-dashboard).
+++

## Tabblad SMS {#sms-global}

![](assets/journey_global_4.png)

+++Meer informatie over de verschillende maatstaven en widgets die beschikbaar zijn voor het SMS-rapport.

De **[!UICONTROL SMS - Sending statistics]** de tabel geeft het succes van uw levering aan :

* **[!UICONTROL Execution time]**: Begintijd voor elke uitvoering van uw terugkerende SMS-bericht tijdens uw reis. Als u slechts één of meerdere terugkerende SMS-berichten wilt aanwijzen, selecteert u deze in het menu **[!UICONTROL Execution time]** vervolgkeuzelijst.

* **[!UICONTROL Targeted]**: Aantal gebruikersprofielen dat als doelprofielen voor deze levering in aanmerking komt.

* **[!UICONTROL Excluded]**: Aantal gebruikersprofielen dat is uitgesloten van de doelprofielen en dat het bericht niet heeft ontvangen.

* **[!UICONTROL Sent]**: Totaal aantal verzendingen voor de levering.

* **[!UICONTROL Bounces]**: Totaal aan fouten gecumuleerd tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

De **[!UICONTROL SMS summary]** widget geeft de belangrijkste informatie met betrekking tot uw bericht met een grafiek:

* **[!UICONTROL Sent]**: Totaal aantal verzendingen voor de levering.

* **[!UICONTROL Bounces]**: Totaal aan fouten gecumuleerd tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

De **[!UICONTROL Exclude Reasons]** in grafieken en tabellen kunt u zien welke fout en uitsluitingen tijdens de levering zijn opgetreden.

De **[!UICONTROL SMS - Clicks by links]** en **[!UICONTROL SMS - Tracking statistics]** widgets bevatten gedetailleerde informatie over de belangrijkste informatie met betrekking tot de betrokkenheid van uw bezoekers bij uw URL&#39;s.

+++

## Tabblad In-app {#in-app-global}

Van je reis **[!UICONTROL Global report]** de **[!UICONTROL In-app]** bevat de belangrijkste informatie met betrekking tot de in-app-leveringen die tijdens uw reizen worden verzonden.

![](assets/in-app-journey-report.png)

+++ Meer informatie over de verschillende maatstaven en widgets die beschikbaar zijn voor het rapport in de app.

De **[!UICONTROL In-app performance]** KPI&#39;s geven een gedetailleerde beschrijving van de belangrijkste informatie over de betrokkenheid van uw bezoekers bij uw In-app-berichten, zoals:

* **[!UICONTROL Unique impressions]**: aantal unieke gebruikers aan wie het In-app-bericht is weergegeven.

* **[!UICONTROL Impressions]**: totaal aantal in-app-berichten dat aan alle gebruikers wordt weergegeven.

  >[!NOTE]
  >
  >Om ervoor te zorgen dat een indruk wordt geteld, moet de gebruiker aan twee criteria voldoen:
  >* Kwalificatie binnen de In-app ervaring, die door de specifieke In-app activiteit tijdens hun reis wordt bereikt.
  >* Voldoen aan de voorwaarden die zijn opgegeven in de triggerregels.
  > 
  >Als gevolg van het tweede criterium kunnen er aanzienlijke verschillen zijn tussen het aantal doelprofielen en het aantal unieke indrukkingen.

* **[!UICONTROL Interaction]**: aantal contracten met uw In-app-bericht. Dit omvat alle handelingen die de gebruikers hebben uitgevoerd, zoals klikken, ontslag of andere interactie.

De **[!UICONTROL In-app summary]** in de grafiek wordt de ontwikkeling van uw In-app-afbeeldingen en -interacties voor de desbetreffende periode weergegeven.

De **[!UICONTROL Interactions by type]** grafieken en tabellen geven aan hoe gebruikers met uw bericht in de app hebben gewerkt door een klik, sluiting of interactie bij te houden.
+++
