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
source-git-commit: c2f2dde40385f56ea86be15a5857fa9e5e2e2fed
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Werken met [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] integratie met [!DNL Customer Journey Analytics] biedt een holistische weergave van al uw reizen met geautomatiseerde rapportdistributie en aangepaste visualisaties van de gegevens.

![](assets/cja.png)

Na het maken van uw reis in [!DNL Journey Optimizer]kunt u uw klantgegevens importeren naar [!DNL Customer Journey Analytics] om rapporten te beginnen en het effect van elke interactie te begrijpen een klant met uw reizen heeft.

➡️ [Customer Journey Analytics detecteren](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html){target="_blank"}

>[!NOTE]
>
>Naast deze integratie kunt u ook de inhoud van Adobe Journey Optimizer-gegevenssets exporteren naar opslaglocaties in de cloud en deze informatie gebruiken voor rapportage- of analysedoeleinden. [Leer hoe u gegevenssets exporteert naar opslaglocaties in de cloud](../data/export-datasets.md)
>
>Merk op dat de de uitvoereigenschap van datasets momenteel in bèta en beschikbaar aan alle gebruikers van Adobe Journey Optimizer is. Werk samen met uw Adobe als u nog geen toegang hebt tot Doelen.

Voor gebruik [!DNL Customer Journey Analytics] voor uw reizen, moet u deze integratie eerst vormen:

1. [Verbinding maken](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html) in [!DNL Customer Journey Analytics] met de **[!UICONTROL Dataset]** je wilt naar Adobe Experience Platform sturen.

   Het volgende [!DNL Journey Optimizer] kan worden geconfigureerd:
   * [Reisstapgebeurtenis](../data/datasets-query-examples.md#journey-step-event): Hiermee kunt u zien wie uw reizen binnenkomt en hoe ver ze komen.
   * [Gegevensbestanden voor feedback/reeksspatiëring](../data/datasets-query-examples.md#message-feedback-event-dataset): hiermee kunt u leveringsinformatie weergeven over de berichten die via [!DNL Journey Optimizer].
   * [Gegevensbestanden voor entiteiten en reizen](../data/datasets-query-examples.md#entity-dataset): hiermee kunt u zoeken in familienamen en deze gebruiken in uw rapportage.

1. [Een gegevensweergave maken](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) om de afmetingen en metriek te vormen u voor uw rapport wilt gebruiken.

   U kunt Journey Optimizer-specifieke metriek maken om de gegevens van uw reizen beter weer te geven. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)

Gebruiken [!DNL Journey Optimizer] with [!DNL Customer Journey Analytics] kan leiden tot enige discrepantie in de rapportage van gegevens die wordt veroorzaakt door:

* **Beide [!DNL Journey Optimizer] en [!DNL Customer Journey Analytics] synchroniseer gegevens van Azure Data Lake Storage (ADLS) voor rapportage.**

  De verwerkingstijd voor binnenkomende gegevens kan enigszins verschillen tussen producten. Daarom komen gegevens mogelijk niet overeen bij het weergeven van rapporten van een bepaalde datum tot en met de huidige dag. Om discrepantie te verminderen, gebruik datumwaaiers exclusief de huidige dag.

* **In [!DNL Journey Optimizer] rapporten, Verzonden metrisch omvat ook metrisch opnieuw proberen.**

  **[!UICONTROL Retries]** wordt niet opgenomen in **[!UICONTROL Sent]** metrisch in [!DNL Customer Journey Analytics]. Dit leidt tot [!DNL Customer Journey Analytics] **[!UICONTROL Sent]** maatstaven voor het weergeven van lagere waarden dan [!DNL Journey Optimizer]. Gegevens voor opnieuw proberen worden echter geconverteerd naar de **[!UICONTROL Messages successfully sent]** of **[!UICONTROL Bounces]** metrisch.
Om discrepantie te verminderen, waaier van de gebruiksdatum van een week geleden of zelfs later.

* **De rapporten worden gediend van een verschillende gegevensbron.**

  Dit kan leiden tot verschillen in gegevens tussen de 1-2% van de producten.
