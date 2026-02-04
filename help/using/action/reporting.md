---
solution: Journey Optimizer
product: journey optimizer
title: Aangepaste acties controleren
description: Leer hoe u gegevens uit het reisrapport kunt gebruiken
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 97464b7afa07199792bd4311d0477b5bcb140d8e
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Aangepaste acties controleren {#reporting}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_custom_actions_monitor"
>title="Aangepaste acties controleren"
>abstract="Met de rapportpagina van **[!UICONTROL Custom action]** kunt u de prestaties en betrouwbaarheid van API-aanroepen bijhouden die uw reizen naar systemen van derden maken."

Met de rapportpagina van **[!UICONTROL Custom action]** kunt u de betrouwbaarheid en prestaties controleren van API-aanroepen die tijdens uw reizen naar systemen van derden zijn gemaakt. Deze rapporten helpen u snel integratiekwesties, latentieknelpunten, of het vertragen/het begrenzen identificeren die levering kunnen beïnvloeden.

De pagina met de rapportage van de aangepaste actie werkt net als andere All-time rapporten in Journey Optimizer. Voor details op dashboardfunctionaliteit, verwijs naar [&#x200B; deze documentatie &#x200B;](../reports/report-cja-manage.md).

Als u de **[!UICONTROL Custom action]** -rapportpagina wilt openen, klikt u op ![](assets/do-not-localize/Smock_Monitoring_18_N.svg) vanaf de **[!UICONTROL Actions]** -startpagina.

![](assets/monitor-1.png)

➡️ [&#x200B; Leer meer over de configuratie van de Acties van de Douane &#x200B;](../action/about-custom-action-configuration.md)

Naast de **[!UICONTROL Custom action]** rapportpagina kunt u **[!DNL Adobe Experience Platform Query Service]** gebruiken om query&#39;s te maken voor het rapporteren van maatstaven voor aangepaste handelingsprestaties. De voorbeelden van de vraag zijn beschikbaar in [&#x200B; deze sectie &#x200B;](../reports/query-examples.md).

## KPI&#39;s {#kpis}

![](assets/monitor-2.png)

De **[!UICONTROL Custom action]** Belangrijkste Indicatoren van Prestaties (KPIs) dienen als gecentraliseerd dashboard, dat een geconsolideerde mening van de operationele gezondheid en de betrouwbaarheid van uw vraag van de douaneactie verstrekt. Met deze maatstaven kunt u de prestaties evalueren, knelpunten identificeren en zorgen voor stabiele integratie met externe systemen.

+++ Meer informatie over KPI&#39;s voor aangepaste handelingen

* **[!UICONTROL Successful calls]**: Het totale aantal HTTP-aanroepen dat een geldige reactie zonder fout heeft geretourneerd.

* **[!UICONTROL 4xx/5xx errors]**: Aantal mislukte aanroepen als gevolg van client-side (4xx) of server-side (5xx) fouten, die configuratiekwesties of eindpuntfouten benadrukken.

* **[!UICONTROL Timeouts]**: Aantal aanroepen dat is mislukt omdat ze de maximale responstijd overschrijden. Dit helpt problemen met de latentie of prestaties van het oppervlak met externe eindpunten.

* **[!UICONTROL Capped calls]**: Het aantal aanroepen dat is geblokkeerd vanwege plafondbeperkingen, zodat downstreamsystemen niet worden overbelast.

* **[!UICONTROL Average RPS]**: aantal aanvragen per seconde dat door de aangepaste handeling over het geselecteerde tijdbereik wordt verwerkt.

* **[!UICONTROL Average latency]**: gemiddelde reactietijd van begin tot eind (in milliseconden) voor alle vraag van HTTP, met inbegrip van succesvolle vraag, fouten, en onderbrekingen.

* **[!UICONTROL Average successful latency]**: gemiddelde reactietijd van begin tot eind (in milliseconden) voor succesvolle vraag slechts, exclusief ontbroken verzoeken en onderbrekingen.

* **[!UICONTROL Average queue time]**: Gemiddelde tijd (in milliseconden) vraag besteed het wachten in de uitvoeringsrij alvorens wordt verzonden. Dit is slechts op vertraagde eindpunten van toepassing, waar Journey Optimizer omhoog vraag een rij vormt wanneer de productielimiet wordt bereikt.

+++

## Oproepen in de tijd {#calls}

![](assets/monitor-3.png)

De **[!UICONTROL Calls over time]** grafiek toont de HTTP vraagKPI trend over de tijdspanne die voor het rapport wordt geselecteerd. De korreligheid van de tijdreeks is afhankelijk van het geselecteerde tijdbereik. Bijvoorbeeld:

* Voor een 7 dagrapport, zal elk gegevenspunt KPIs voor één dag tonen.
* Als u een tijdbereik van 1 dag selecteert, worden de KPI&#39;s per uur weergegeven in de grafiek.
* Als u een tijdbereik van 1 uur selecteert, worden in de grafiek de PKI&#39;s per minuut weergegeven.

➡️[&#x200B; zie de sectie KPIs voor een beschrijving van de metriek van de vraag van HTTP &#x200B;](#kpis)

## Latentie in de tijd {#latency-overtime}

![](assets/monitor-6.png)

In de grafiek van **[!UICONTROL Latency over time]** wordt de trend van latentiemetriek gedurende de geselecteerde tijdsperiode weergegeven. In deze tijdreeksweergave kunt u prestatiepatronen volgen, pieklatentieperiodes identificeren en de invloed van optimalisaties of systeemwijzigingen in de loop van de tijd controleren.

➡️[&#x200B; zie de sectie KPIs voor een beschrijving van de metriek van de Latentie &#x200B;](#kpis)


## Uitsplitsing naar oproep {#breakdown}

![](assets/monitor-4.png)

De **[!UICONTROL Calls breakdown]** lijst verstrekt een hiërarchische verdeling van de metriek van de vraag van HTTP, van de algemene metriek per eindpunt op het hoogste niveau aan de metriek per Actie van de Douane die elk eindpunt tot de reizen gebruikt die op hen op het bodemniveau baseren.

➡️[&#x200B; zie de sectie KPIs voor een beschrijving van de metriek van de vraag van HTTP &#x200B;](#kpis)

## Latentie-uitsplitsing {#latency-breakdown}

![](assets/monitor-5.png)

De tabel **[!UICONTROL Latency breakdown]** bevat een gedetailleerde uitsplitsing van de latentiemetriek in uw aangepaste handelingen. Deze weergave helpt u te identificeren welke specifieke eindpunten of acties prestatieproblemen ondervinden, zodat u knelpunten met betrekking tot wachttijden kunt opsporen en aanpakken.

➡️[&#x200B; zie de sectie KPIs voor een beschrijving van de metriek van de Latentie &#x200B;](#kpis)

## Hoe kan ik-video {#video}

In de onderstaande video ziet u hoe u de betrouwbaarheid en prestaties kunt controleren van API-aanroepen die tijdens uw reizen naar systemen van derden zijn gemaakt.

+++Zie video

>[!VIDEO](https://video.tv.adobe.com/v/3479547?captions=dut&quality=12&learn=on)

+++
