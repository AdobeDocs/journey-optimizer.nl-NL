---
title: Werken met Customer Journey Analytics
description: Aan de slag met Customer Journey Analytics
feature: Reporting
topic: Content Management
role: User
level: Beginner
source-git-commit: bf4857f63b44d557304ef05e490fe6659f0ad888
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# Werken met [!DNL Customer Journey Analytics] {#cja-ajo}

![](assets/cja.png)

Na het maken van uw reis in [!DNL Journey Optimizer]kunt u uw klantgegevens importeren naar [!DNL Customer Journey Analytics] om rapporten te beginnen en het effect van elke interactie te begrijpen een klant met uw reizen heeft.

➡️ [Discover Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html){target=&quot;_blank&quot;}

Voor gebruik [!DNL Customer Journey Analytics] voor uw reizen, moet u deze integratie eerst vormen:

1. [Verbinding maken](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html) in [!DNL Customer Journey Analytics] met de **[!UICONTROL Dataset]** u wilt naar het Platform verzenden.

1. [Een gegevensweergave maken](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) om de afmetingen en metriek te vormen u voor uw rapport wilt gebruiken.

   U kunt Journey Optimizer-specifieke metriek maken om de gegevens van uw reizen beter weer te geven. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)


Gebruiken [!DNL Journey Optimizer] with [!DNL Customer Journey Analytics] kan leiden tot enige discrepantie in de rapportage van gegevens die wordt veroorzaakt door:

* **Beide [!DNL Journey Optimizer] en [!DNL Customer Journey Analytics] synchroniseer gegevens van Azure Data Lake Storage (ADLS) voor rapportage.**

   De verwerkingstijd voor binnenkomende gegevens kan enigszins verschillen tussen producten. Daarom komen gegevens mogelijk niet overeen bij het weergeven van rapporten van een bepaalde datum tot en met de huidige dag. Om discrepantie te verminderen, gebruik datumwaaiers exclusief de huidige dag.

* **In [!DNL Journey Optimizer] rapporten, Verzonden metrisch omvat ook metrisch opnieuw proberen.**

   **[!UICONTROL Retries]** wordt niet opgenomen in **[!UICONTROL Sent]** metrisch in [!DNL Customer Journey Analytics]. Dit leidt tot [!DNL Customer Journey Analytics] **[!UICONTROL Sent]** maatstaven voor het weergeven van lagere waarden dan [!DNL Journey Optimizer]. Gegevens voor opnieuw proberen worden echter geconverteerd naar de **[!UICONTROL Messages successfully sent]** of **[!UICONTROL Bounces]** metrisch.
Om discrepantie te verminderen, waaier van de gebruiksdatum van een week geleden of zelfs later.

* **De rapporten worden gediend van een verschillende gegevensbron.**

   Dit kan leiden tot verschillen tussen de gegevens van 1-2% tussen de producten.
