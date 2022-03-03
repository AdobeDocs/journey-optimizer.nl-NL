---
title: Live-melding via e-mail
description: Leer hoe u gegevens uit het live e-mailrapport kunt gebruiken
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 1ddfbf1a-3cd5-446a-b0fb-76b81b88c1b4
source-git-commit: fad7eb9feea0d8c21494b4a7c1608369e725023e
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# Live-melding via e-mail {#email-live-report}

De e-mail **[!UICONTROL Live report]** is alleen bedoeld voor een specifieke e-maillevering.

Van de **[!UICONTROL Executions]** tabblad van het dialoogvenster **[!UICONTROL Messages]** menu, selecteert u **[!UICONTROL Live view]** Selecteer vervolgens in het geavanceerde menu van de geselecteerde levering **[!UICONTROL Live report]**.

![](assets/live_report.png)

De e-mail **[!UICONTROL Live report]** is verdeeld in verschillende widgets waarin het succes en de fouten van uw levering worden beschreven. Elke widget kan indien nodig worden vergroot of verkleind en verwijderd. Zie voor meer informatie hierover [sectie](live-report.md#modify-dashboard).

![](assets/live_report_5.png)

**[!UICONTROL Email performance]** en **[!UICONTROL Email summary]** widgets detailleert de belangrijkste informatie met betrekking tot uw bericht met een grafiek en KPIs:

* **[!UICONTROL Targeted]**: Aantal gebruikersprofielen dat als doelprofielen voor deze levering in aanmerking komt.

* **[!UICONTROL Sent]**: Het totale aantal verzendt voor de levering.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Opens]**: Aantal keren dat een bericht in een levering werd geopend.

* **[!UICONTROL Clicks]**: Het aantal keren dat op een inhoud is geklikt in een levering.

* **[!UICONTROL Bounces]**: Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

* **[!UICONTROL Spam complaints]**: Aantal berichten geclassificeerd als spam.

* **[!UICONTROL Unsubscriptions]**: Aantal klikken op de verbinding van het unsubscription.

* **[!UICONTROL Excluded]**: Aantal gebruikersprofielen dat is uitgesloten van de doelprofielen en dat het bericht niet heeft ontvangen.

De **[!UICONTROL Sending Statistics]** widget geeft aan hoe succesvol uw levering is:

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounces]**: Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

![](assets/live_report_6.png)

De **[!UICONTROL Error Reasons]** de grafiek en de lijst laten u zien welke fout tijdens uw levering voorkwam.

De **[!UICONTROL Bounce Reasons]** en **[!UICONTROL Bounce categories]** widgets bevatten de beschikbare gegevens met betrekking tot berichten die worden teruggestuurd, zoals:

* **[!UICONTROL Hard bounce]**: Het totale aantal permanente fouten, zoals een onjuist e-mailadres. Dit omvat een foutbericht waarin expliciet wordt aangegeven dat het adres ongeldig is, zoals Onbekende gebruiker.

* **[!UICONTROL Soft bounce]**: Het totale aantal tijdelijke fouten, zoals een volledig postvak.

* **[!UICONTROL Ignored]**: Het totale aantal tijdelijke gegevens, zoals Buiten-kantoor, of een technische fout, bijvoorbeeld als het type afzender postmaster is.

<!--
![](assets/live_report_8.png)

>[!NOTE]
>
>The Offers widgets and metrics are only available if a decision was inserted in an email. For more information on Decision Management, refer to this [page](../offers/get-started/starting-offer-decisioning.md).

The **[!UICONTROL Offers statistic]** and **[!UICONTROL Offers statistics]** over time widgets measure your offer's success and impact on your targeted audience. It detail the main information relative to your message with KPIs:

* **[!UICONTROL Offer sent]**: Total number of sends for the offer.

* **[!UICONTROL Offer impression]**: Number of times the offer was opened in a delivery.

* **[!UICONTROL Offer clicks]**: Number of times an offer was clicked on in a delivery.
-->
>[!NOTE]
>
>De profielen met **[!UICONTROL Suppressed]** of **[!UICONTROL Not allowed]** status worden uitgesloten tijdens het verzenden van berichten. Daarom moet **Reisrapporten** geeft aan dat deze profielen door de reis zijn gegaan ([Segment lezen](../building-journeys/read-segment.md) en [Bericht](../building-journeys/journeys-message.md) de **E-mailrapporten** worden niet opgenomen in de **[!UICONTROL Sent]** Metrische gegevens worden uitgefilterd voordat e-mail wordt verzonden.
>
>Meer informatie over de [Onderdrukkingslijst](../messages/suppression-list.md) en [Lijst van gewenste personen](../messages/allow-list.md). Als u de reden voor alle uitsluitingsgevallen wilt achterhalen, kunt u de opdracht [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.
