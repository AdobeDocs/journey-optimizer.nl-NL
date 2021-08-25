---
title: Live-melding via e-mail
description: Leer hoe u gegevens uit het live e-mailrapport kunt gebruiken
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: c54e4443c0a8b6c2e427fa007adf5d800b2ba3b5
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Live-melding via e-mail {#email-live-report}

De e-mail **[!UICONTROL Live report]** richt slechts een specifieke e-maillevering.

Selecteer **[!UICONTROL Live view]** op het tabblad **[!UICONTROL Executions]** van het menu **[!UICONTROL Messages]** en selecteer **[!UICONTROL Live report]** in het geavanceerde menu van de geselecteerde levering.

![](../assets/live_report.png)

Het e-mailbericht **[!UICONTROL Live report]** is verdeeld in verschillende widgets waarin het succes en de fouten van uw levering worden beschreven. Elke widget kan indien nodig worden vergroot of verkleind en verwijderd. Voor meer informatie hierover raadpleegt u deze [sectie](live-report.md#modify-dashboard).

![](../assets/live_report_5.png)

**[!UICONTROL Email performance]** en  **[!UICONTROL Email summary]** widgets geeft de belangrijkste informatie met betrekking tot uw bericht met een grafiek en KPIs:

* **[!UICONTROL Sent]**: Het totale aantal verzendt voor de levering.

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounces]**: Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

* **[!UICONTROL Opens]**: Aantal keren dat een bericht in een levering werd geopend.

* **[!UICONTROL Clicks]**: Het aantal keren dat op een inhoud is geklikt in een levering.

De grafiek **[!UICONTROL Sending Statistics]** geeft het succes van uw levering weer:

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounces]**: Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

![](../assets/live_report_6.png)

Met de grafiek en tabel **[!UICONTROL Error Reasons]** kunt u zien welke fout is opgetreden tijdens de levering.

De widgets **[!UICONTROL Bounce Reasons]** en **[!UICONTROL Bounce categories]** bevatten de beschikbare gegevens met betrekking tot berichten die worden teruggestuurd, zoals:

* **[!UICONTROL Hard bounce]**: Het totale aantal permanente fouten, zoals een onjuist e-mailadres. Dit omvat een foutbericht waarin expliciet wordt aangegeven dat het adres ongeldig is, zoals Onbekende gebruiker.

* **[!UICONTROL Soft bounce]**: Het totale aantal tijdelijke fouten, zoals een volledig postvak.

* **[!UICONTROL Ignored]**: Het totale aantal tijdelijke gegevens, zoals Buiten-kantoor, of een technische fout, bijvoorbeeld als het type afzender postmaster is.

>[!NOTE]
>
>De profielen met **[!UICONTROL Suppressed]** of **[!UICONTROL Not allowed]** status worden uitgesloten tijdens het verzenden van berichten. Daarom, terwijl **Reis rapporteert** deze profielen zal tonen als die door de reis ([Leessegment](../building-journeys/read-segment.md) en [Bericht](../building-journeys/journeys-message.md) activiteiten) zijn bewogen, **E-mailrapporten** zullen niet hen in **[!UICONTROL Sent]** metriek omvatten aangezien zij voorafgaand aan e-mail verzenden worden gefilterd.
>
>Meer informatie vindt u in de [Onderdrukkingslijst](../suppression-list.md) en [Lijst van gewenste personen](../allow-list.md). Om de reden voor alle uitsluitingsgevallen te weten te komen, kunt u [de Dienst van de Vraag van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html) gebruiken.
