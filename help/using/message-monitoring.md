---
title: Uitvoering van monitorberichten
description: Meer informatie over richtlijnen voor bewaking
feature: Bewaking
topic: Contentmanagement
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Bewaking van berichten {#monitor-message-execution}

![](assets/do-not-localize/badge.png)

[!DNL Journey Optimizer] biedt mogelijkheden om de berichten te controleren die momenteel worden gepubliceerd en geactiveerd om ervoor te zorgen dat uw berichten correct worden uitgevoerd, verzonden en afgeleverd. U kunt zien hoe uw berichten over reizen <!--and APIs--> in real time van de **[!UICONTROL Executions]** lijst uitvoeren.

U opent deze lijst door op de startpagina **[!DNL Journey Optimizer]** **[!UICONTROL Messages]** te selecteren en op het tabblad **[!UICONTROL Executions]** te klikken.

Dit tabblad bevat twee weergaven: **[!UICONTROL Live view]** en **[!UICONTROL Global view]**.

* Het tabblad **[!UICONTROL Live view]** biedt een **real-time overzicht van alle uitgevoerde berichten** die worden geactiveerd door een of meer [ritten](building-journeys/journey.md) **alleen gedurende de laatste 24 uur**.

   ![](assets/message-execution-tab-live.png)

   Deze lijst wordt elke 60 seconden automatisch vernieuwd. Als geen uitvoering in de laatste 24 uren voor een specifiek bericht voorkwam, zullen alle kolommen ongeldige waarden (0) voor dat bericht tonen.

* Het tabblad **[!UICONTROL Global view]** biedt een **overzicht van alle uitgevoerde berichten** die worden geactiveerd door een of meer [ritten](building-journeys/journey.md) **sinds de begindatum van het bericht**.

   ![](assets/message-execution-tab-global.png)

   Deze lijst wordt elke negentig minuten automatisch vernieuwd. De gegevens worden geaggregeerd in de tijd sinds de begindatum van elk bericht.

Als een bericht wordt gepubliceerd maar nog niet door een reis teweeggebracht, het niet vermeld in om het even welke lusjes. Alleen de volgende elementen worden weergegeven:
* Berichten die zijn geactiveerd, maar nog niet zijn gestart (in behandeling).
* Berichten die zijn geactiveerd en die momenteel worden uitgevoerd (bezig).

<!--For multichannel messages, one row per channel is displayed for each message. STILL VALID? looks like NOT-->

>[!NOTE]
>
>Als een bericht in verscheidene reizen is gebruikt, wordt één rij per reis getoond voor elke uitvoering.

<!--![](assets/message-execution-multichannel.png)-->

<!--If a message has been used in several journeys, the **[!UICONTROL Source]** column displays **[!UICONTROL Multiple]**.-->

Standaard worden de berichten vanaf de meest recente uitvoeringsdatum weergegeven. Klik op het pictogram **[!UICONTROL Filters]** om de berichten te doorzoeken op basis van het kanaal, de begindatum en/of de einddatum.

![](assets/message-execution-tab-filters.png)

Met de tweede kolom <!--**[!UICONTROL Quick action]**-->kunt u het corresponderende [message](create-message.md) openen en het [Live Report](reports/live-report.md) openen als u zich in **[!UICONTROL Live view]** bevindt, of het [Global Report](reports/global-report.md) als u zich in **[!UICONTROL Global view]** bevindt.

![](assets/message-execution-open-live-report.png)

Voor elke berichtuitvoering wordt een aantal indicatoren weergegeven:

* **[!UICONTROL Message label]**: De titel van het bericht die u bij het  [creëren van het bericht](create-message.md) bepaalde. De automatisch gegenereerde uitvoerings-id wordt tussen haakjes weergegeven.

   <!--**[!UICONTROL Execution ID]**: Automatically generated identifier.
  **[!UICONTROL Source]**: Name of the journey leveraging that message.-->

* **[!UICONTROL Journey - Version - Action]**: Naam van de reis die het bericht, versie van de reis, en etiket van de actie leveraging het bericht in de reis leveraging.

* **[!UICONTROL Status]**: Status van uitvoering van bericht.  <!--List all the possible statuses? For now only Live status? The user cannot stop or cancel the execution. TBC by Fred-->

* **[!UICONTROL Start date]**: Datum en tijdstip waarop het bericht is uitgevoerd vanaf de reis.

   <!--Targeted: Number of targeted profiles for each message execution. To come?-->

* **[!UICONTROL Excluded]**: Aantal profielen dat vanwege uitsluitingsregels van het oorspronkelijke doel is uitgesloten.

* **[!UICONTROL Sent]**: Aantal verzonden berichten.

* **[!UICONTROL Delivered]**: Aantal berichten met succes geleverd in de brievenbus van de ontvanger (e-mail) of apparaat (duw) zonder een stuitende of een andere leveringsfout te produceren.

* **[!UICONTROL Bounces]**: Aantal berichten dat niet kan worden geleverd wegens een leveringsmislukking. [Meer weten over grenzen](suppression-list.md)?

* **[!UICONTROL Opens]**: Aantal berichten dat is geopend.

* **[!UICONTROL Clicks]**: Aantal klikken op koppelingen in een e-mailbericht.

   >[!NOTE]
   >
   >Klik bestaat niet voor pushberichten: wanneer een gebruiker op een pushmelding klikt, wordt de app geopend die alleen als een open app kan worden beschouwd.

* **[!UICONTROL Errors]**: Aantal berichten dat niet kan worden verzonden wegens een technische fout.

* **[!UICONTROL Spam complaints]**: Aantal berichten die als spam door ontvangers werden gemerkt. [Meer weten over klachten](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability)?

Als u op elke hyperlink klikt, wordt de bijbehorende overzichtsweergave van het bericht geopend. [Meer weten over berichten](create-message.md)?
