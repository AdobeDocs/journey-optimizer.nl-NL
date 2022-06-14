---
title: Globaal e-mailrapport
description: Leer hoe u gegevens uit het algemene e-mailrapport kunt gebruiken
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 2bead395-082a-4fea-ad10-b2b2c5f484e9
source-git-commit: 0ca491315e214e3c12bec11a93da1a2b98b493b6
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# E-mailglobaal rapport {#email-global-report}

De e-mail **[!UICONTROL Global report]** is alleen bedoeld voor een specifieke e-maillevering.

Van de **[!UICONTROL Executions]** tabblad van het dialoogvenster **[!UICONTROL Messages]** menu, selecteert u **[!UICONTROL Global view]** Selecteer vervolgens in het geavanceerde menu van de geselecteerde levering **[!UICONTROL Global report]**.

![](assets/global_report_3.png)

De e-mail **[!UICONTROL Global report]** is verdeeld in verschillende widgets waarin het succes en de fouten van uw levering worden beschreven. Elke widget kan indien nodig worden vergroot of verkleind en verwijderd. Zie voor meer informatie hierover [sectie](global-report.md#modify-dashboard).

![](assets/global_report_4.png)

**[!UICONTROL Email performance]** detailleert de belangrijkste informatie met betrekking tot uw bericht met KPIs:

* **[!UICONTROL Sent]**: Het totale aantal verzendt voor de levering.

* **[!UICONTROL Delivery Rate]**: Percentage berichten verzonden.

* **[!UICONTROL Bounce Rate]**: Percentage van e-mails dat is teruggestuurd in vergelijking met verzonden e-mails.

* **[!UICONTROL Error Rate]**: Percentage fouten die optraden tijdens een levering waardoor deze niet kon worden verzonden, vergeleken met verzonden e-mailberichten.

* **[!UICONTROL Open Rate]**: Percentage geopende berichten.

* **[!UICONTROL Click Rate]**: Percentage van klikken in een levering.

* **[!UICONTROL Spam Complaint Rate]**: Percentage e-mails dat door ontvangers als spam werd gemarkeerd in vergelijking met de geleverde berichten. Voor meer informatie over klachten raadpleegt u de [Handleiding voor best practices voor levering](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}.

* **[!UICONTROL Unsubscribe Rate]**: Percentage van unieke afboekingen in verhouding tot het aantal geleverde berichten. Deze indicator baseert zich niet op het aantal kliks op de unsubscription verbinding maar is gebaseerd op het aantal unsubscriptions die door ontvangers in werking worden gesteld. Meer informatie over abonnementen vindt u in deze [page](../messages/consent.md).

De **[!UICONTROL Email - Tracking statistics]** bevat de beschikbare gegevens voor ontvankelijke activiteit voor uw levering:

* **[!UICONTROL Opens]**: Aantal keren dat de levering is geopend in een levering.

* **[!UICONTROL Unique Opens]**: Percentage geopende leveringen.

* **[!UICONTROL Open Rate]**: Het totale aantal geopende e-mails in verhouding tot het aantal geleverde e-mails.

* **[!UICONTROL Clicks]**: Aantal keer dat er op een inhoud in een e-mail is geklikt.

* **[!UICONTROL Unique Clicks]**:Aantal ontvangers die op een inhoud in een e-mail hebben geklikt.

* **[!UICONTROL Click through rate]**: Percentage gebruikers dat met de reis interactie heeft gehad.

De **[!UICONTROL Sending Statistics]** grafiek geeft het succes van uw levering aan:

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounces]**: Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

![](assets/global_report_5.png)

De **[!UICONTROL Bounce Reasons]** en **[!UICONTROL Bounce categories]** widgets bevatten de beschikbare gegevens met betrekking tot berichten die worden teruggestuurd, zoals:

* **[!UICONTROL Hard bounce]**: Het totale aantal permanente fouten, zoals een onjuist e-mailadres. Dit omvat een foutbericht waarin expliciet wordt aangegeven dat het adres ongeldig is, zoals Onbekende gebruiker.

* **[!UICONTROL Soft bounce]**: Het totale aantal tijdelijke fouten, zoals een volledig postvak.

* **[!UICONTROL Ignored]**: Het totale aantal tijdelijke berichten, zoals buiten het kantoor, of een technische fout, bijvoorbeeld als het type afzender postmaster is.

Voor meer informatie over grenzen raadpleegt u de [Onderdrukkingslijst](../reports/suppression-list.md) pagina.

De **[!UICONTROL Error Reasons]** en **[!UICONTROL Exclude Reasons]** in grafieken en tabellen kunt u zien welke fout en uitsluitingen tijdens de levering zijn opgetreden.

![](assets/global_report_6.png)

De **[!UICONTROL Email - Top recipient domain]** grafiek en lijstdetails welke domeinen het meest door ontvangers worden gebruikt om e-mail te openen.

De **[!UICONTROL Email - Top Url]** grafiek en lijstdetails die URLs van uw levering het meest bezocht zijn.

De **[!UICONTROL Open vs Click]** identificeert de interactie van uw ontvangers met de levering:

* **[!UICONTROL Unique Clicks]**:Aantal ontvangers die op een inhoud in een e-mail hebben geklikt.

* **[!UICONTROL Unique Opens]**: Aantal ontvangers dat de levering heeft geopend.

![](assets/global_report_20.png)

>[!NOTE]
>
>De widgets en cijfers voor aanbiedingen zijn alleen beschikbaar als een beslissing in een e-mail is ingevoegd. Raadpleeg voor meer informatie over het beheer van de besluiten [page](../offers/get-started/starting-offer-decisioning.md).

De **[!UICONTROL Offers statistic]** en **[!UICONTROL Offers statistics]** in de loop der tijd meten de widgets het succes van uw aanbieding en de impact op uw doelgroep. Het detailleert de belangrijkste informatie met betrekking tot uw bericht met KPIs:

* **[!UICONTROL Offer sent]**: Het totale aantal verzendingen voor de aanbieding.

* **[!UICONTROL Offer impression]**: Aantal keren dat het voorstel is geopend in een levering.

* **[!UICONTROL Offer clicks]**: Aantal keren dat op een voorstel is geklikt in een levering.

De **[!UICONTROL Offers detailed statistic]** de tabel bevat de beschikbare gegevens voor de activiteit van de ontvanger met uw voorstel:

* **[!UICONTROL Placement name]**: Naam van de plaatsing die u hebt gebruikt om uw voorstel weer te geven. Raadpleeg deze voor meer informatie over plaatsing [page](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Offer name]**: Naam van de aanbieding die in de levering is toegevoegd. Raadpleeg deze voor meer informatie over plaatsing [page](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offer sent]**: Het totale aantal verzendingen voor de aanbieding.

* **[!UICONTROL Offer impression rate]**: Percentage geopende aanbiedingen in verhouding tot het aantal verzonden aanbiedingen.

* **[!UICONTROL Offer click rate]**: Percentage gebruikers dat interactie had met het aanbod.

>[!NOTE]
>
>De profielen met **[!UICONTROL Suppressed]** of **[!UICONTROL Not allowed]** status worden uitgesloten tijdens het verzenden van berichten. Daarom moet **Reisrapporten** geeft aan dat deze profielen door de reis zijn gegaan ([Segment lezen](../building-journeys/read-segment.md) en [Bericht](../building-journeys/journeys-message.md) de **E-mailrapporten** worden niet opgenomen in de **[!UICONTROL Sent]** Metrische gegevens worden uitgefilterd voordat e-mail wordt verzonden.
>
>Meer informatie over de [Onderdrukkingslijst](suppression-list.md) en [Lijst van gewenste personen](../configuration/allow-list.md). Als u de reden voor alle uitsluitingsgevallen wilt achterhalen, kunt u de opdracht [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.
