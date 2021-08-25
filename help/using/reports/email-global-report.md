---
title: Globaal e-mailrapport
description: Leer hoe u gegevens uit het algemene e-mailrapport kunt gebruiken
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 9408a93deecfb12f28a0a87c19fa0074c66844a9
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# E-mailglobaal rapport {#email-global-report}

De e-mail **[!UICONTROL Global report]** richt slechts een specifieke e-maillevering.

Selecteer **[!UICONTROL Global view]** op het tabblad **[!UICONTROL Executions]** van het menu **[!UICONTROL Messages]** en selecteer **[!UICONTROL Global report]** in het geavanceerde menu van de geselecteerde levering.

![](../assets/global_report_3.png)

Het e-mailbericht **[!UICONTROL Global report]** is verdeeld in verschillende widgets waarin het succes en de fouten van uw levering worden beschreven. Elke widget kan indien nodig worden vergroot of verkleind en verwijderd. Voor meer informatie hierover raadpleegt u deze [sectie](global-report.md#modify-dashboard).

![](../assets/global_report_4.png)

**[!UICONTROL Email performance]** detailleert de belangrijkste informatie met betrekking tot uw bericht met KPIs:

* **[!UICONTROL Sent]**: Het totale aantal verzendt voor de levering.

* **[!UICONTROL Delivery Rate]**: Percentage berichten verzonden.

* **[!UICONTROL Bounce Rate]**: Percentage van e-mails dat is teruggestuurd in vergelijking met verzonden e-mails.

* **[!UICONTROL Error Rate]**: Percentage fouten die optraden tijdens een levering waardoor deze niet kon worden verzonden, vergeleken met verzonden e-mailberichten.

* **[!UICONTROL Open Rate]**: Percentage geopende berichten.

* **[!UICONTROL Click Rate]**: Percentage van klikken in een levering.

* **[!UICONTROL Spam Complaint Rate]**: Percentage e-mails dat door ontvangers als spam werd gemarkeerd in vergelijking met de geleverde berichten. Voor meer informatie over klachten, verwijs naar [De gids van de Beste praktijken van de Levering ](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}.

* **[!UICONTROL Unsubscribe Rate]**: Percentage van unieke afboekingen in verhouding tot het aantal geleverde berichten. Deze indicator baseert zich niet op het aantal kliks op de unsubscription verbinding maar is gebaseerd op het aantal unsubscriptions die door ontvangers in werking worden gesteld. Meer informatie over abonnementen vindt u op deze [pagina](../consent.md).

**[!UICONTROL Email - Tracking statistics]** bevat de beschikbare gegevens voor ontvankelijke activiteit voor uw levering:

* **[!UICONTROL Opens]**: Aantal keren dat de levering is geopend in een levering.

* **[!UICONTROL Unique Opens]**: Percentage geopende leveringen.

* **[!UICONTROL Open Rate]**: Het totale aantal geopende e-mails in verhouding tot het aantal geleverde e-mails.

* **[!UICONTROL Clicks]**: Aantal keer dat er op een inhoud in een e-mail is geklikt.

* **[!UICONTROL Unique Clicks]**:Aantal ontvangers die op een inhoud in een e-mail hebben geklikt.

* **[!UICONTROL Click through rate]**: Percentage gebruikers dat met de reis interactie heeft gehad.

De grafiek **[!UICONTROL Sending Statistics]** geeft het succes van uw levering weer:

* **[!UICONTROL Delivered]**: Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Bounces]**: Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.

* **[!UICONTROL Errors]**: Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.

![](../assets/global_report_5.png)

De widgets **[!UICONTROL Bounce Reasons]** en **[!UICONTROL Bounce categories]** bevatten de beschikbare gegevens met betrekking tot berichten die worden teruggestuurd, zoals:

* **[!UICONTROL Hard bounce]**: Het totale aantal permanente fouten, zoals een onjuist e-mailadres. Dit omvat een foutbericht waarin expliciet wordt aangegeven dat het adres ongeldig is, zoals Onbekende gebruiker.

* **[!UICONTROL Soft bounce]**: Het totale aantal tijdelijke fouten, zoals een volledig postvak.

* **[!UICONTROL Ignored]**: Het totale aantal tijdelijke berichten, zoals buiten het kantoor, of een technische fout, bijvoorbeeld als het type afzender postmaster is.

Voor meer informatie over grenzen, verwijs naar [de pagina van de Onderdrukking ](../suppression-list.md).

Met de grafiek en tabel **[!UICONTROL Error Reasons]** kunt u zien welke fout is opgetreden tijdens de levering.

![](../assets/global_report_6.png)

De **[!UICONTROL Email - Top recipient domain]** grafiek en lijstdetails die domeinen het meest door ontvangers worden gebruikt om e-mail te openen.

De **[!UICONTROL Email - Top Url]** grafiek en lijstdetails die URLs van uw levering het meest bezocht zijn.

**[!UICONTROL Open vs Click]** identificeert de interactie van uw ontvangers met de levering:

* **[!UICONTROL Unique Clicks]**:Aantal ontvangers die op een inhoud in een e-mail hebben geklikt.

* **[!UICONTROL Unique Opens]**: Aantal ontvangers dat de levering heeft geopend.

>[!NOTE]
>
>De profielen met **[!UICONTROL Suppressed]** of **[!UICONTROL Not allowed]** status worden uitgesloten tijdens het verzenden van berichten. Daarom, terwijl **Reis rapporteert** deze profielen zal tonen als die door de reis ([Leessegment](../building-journeys/read-segment.md) en [Bericht](../building-journeys/journeys-message.md) activiteiten) zijn bewogen, **E-mailrapporten** zullen niet hen in **[!UICONTROL Sent]** metriek omvatten aangezien zij voorafgaand aan e-mail verzenden worden gefilterd.
>
>Meer informatie vindt u in de [Onderdrukkingslijst](../suppression-list.md) en [Lijst van gewenste personen](../allow-list.md). Om de reden voor alle uitsluitingsgevallen te weten te komen, kunt u [Adobe Experience Platform de Dienst van de Vraag ](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html) {target= &quot;_blank&quot;} gebruiken.