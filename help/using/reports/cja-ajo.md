---
solution: Journey Optimizer
product: journey optimizer
title: Werken met Customer Journey Analytics
description: Aan de slag met Customer Journey Analytics
feature: Reporting, Integrations
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 9ceccdf1daca1745cc0610a97660b92524f732d2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# [!DNL Customer Journey Analytics] handmatig configureren {#cja-ajo}

[!DNL Journey Optimizer] integratie met [!DNL Customer Journey Analytics] biedt een holistische weergave van al uw reizen met geautomatiseerde rapportdistributie en aangepaste visualisaties van de gegevens.

In de volgende sectie wordt beschreven hoe u door Journey Optimizer gegenereerde gegevens handmatig kunt gebruiken voor een diepgaande analyse in Customer Journey Analytics. Deze integratie kan automatisch worden ingesteld. [Meer informatie](report-gs-cja.md)

![](assets/cja.png)

Nadat u uw reis in [!DNL Journey Optimizer] hebt gemaakt, kunt u uw klantgegevens importeren naar [!DNL Customer Journey Analytics] om rapporten te starten en inzicht te krijgen in de impact van elke interactie die een klant onderhoudt met uw reizen.

➡️ [ ontdekt Customer Journey Analytics ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/integrations/ajo#manually-configure-a-data-view-to-be-used-with-journey-optimizer){target="_blank"}

>[!NOTE]
>
>Naast deze integratie kunt u ook de inhoud van Adobe Journey Optimizer-gegevenssets exporteren naar opslaglocaties in de cloud en deze informatie gebruiken voor rapportage- of analysedoeleinden. [ Leer hoe te om datasets naar de plaatsen van de wolkenopslag uit te voeren ](../data/export-datasets.md)
>

Voordat u [!DNL Customer Journey Analytics] gebruikt voor uw reizen, moet u deze integratie eerst configureren:

1. [ creeer een verbinding ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html){target="_blank"} in [!DNL Customer Journey Analytics] met **[!UICONTROL Dataset]** u naar Adobe Experience Platform wilt verzenden.

   De volgende [!DNL Journey Optimizer] kan worden geconfigureerd:
   * [ Gebeurtenis van de Stap van de Reis ](../data/datasets-query-examples.md#journey-step-event): staat u toe om te bekijken wie uw reizen ingaat en hoe ver zij krijgen.
   * [ de Terugkoppeling/het Volgen datasets van het Bericht ](../data/datasets-query-examples.md#message-feedback-event-dataset): staat u toe om leveringsinformatie over uw berichten te bekijken die door [!DNL Journey Optimizer] worden verzonden.
   * [ de datasets van de Entiteit en van de Reis ](../data/datasets-query-examples.md#entity-dataset): staat u toe om vriendschappelijke namen te zoeken en hen in uw rapportering te gebruiken.

1. [ creeer een gegevensmening ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html){target="_blank"} om de afmetingen en metriek te vormen u voor uw rapport wilt gebruiken.

   U kunt Journey Optimizer-specifieke metriek maken om de gegevens van uw reizen beter weer te geven. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics){target="_blank"}

>[!NOTE]
>
>Als de veelvoudige verbindingen voor uw zandbak bestaan, bevestig dat de [ gegevensmening ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html){target="_blank"} verwijzingen de [ verbinding ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html){target="_blank"} flagged **[!UICONTROL Use in CJA]**. Anders, kan [**analyseren in CJA** knoop ](report-cja-manage.md#analyze) in [!DNL Journey Optimizer] worden onbruikbaar gemaakt.

Het gebruik van [!DNL Journey Optimizer] met [!DNL Customer Journey Analytics] kan leiden tot enige discrepantie bij het rapporteren van gegevens die worden veroorzaakt door:

* **zowel [!DNL Journey Optimizer] als [!DNL Customer Journey Analytics] synchronisatiegegevens van de Opslag van het meer van Gegevens van Azure (ADLS) voor het melden.**

  De verwerkingstijd voor binnenkomende gegevens kan enigszins verschillen tussen producten. Daarom komen gegevens mogelijk niet overeen bij het weergeven van rapporten van een bepaalde datum tot en met de huidige dag. Om discrepantie te verminderen, gebruik datumwaaiers exclusief de huidige dag.

* **in [!DNL Journey Optimizer] rapporten, Verzonden metrisch omvat ook opnieuw metrisch.**

  **[!UICONTROL Retries]** wordt niet opgenomen in **[!UICONTROL Sent]** metrisch in [!DNL Customer Journey Analytics] . Hierdoor geven [!DNL Customer Journey Analytics] **[!UICONTROL Sent]** -meetwaarden weer die lager zijn dan [!DNL Journey Optimizer] . Gegevens voor opnieuw proberen worden echter geconverteerd naar de metrische waarde **[!UICONTROL Messages successfully sent]** of **[!UICONTROL Bounces]** .
Om discrepantie te verminderen, waaier van de gebruiksdatum van een week geleden of zelfs later.

* **de Rapporten worden gediend van een verschillende gegevensbron.**

  Dit kan leiden tot verschillen in gegevens tussen de 1-2% van de producten.
