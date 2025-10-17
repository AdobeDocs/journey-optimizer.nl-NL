---
solution: Journey Optimizer
product: journey optimizer
title: Overzicht van het delen van journeystappen
description: Overzicht van het delen van journeystappen
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: 29d6b881-35a3-4c62-9e7d-d0aeb206ea77
source-git-commit: efae7f7d366690af71430bb9eb62523d1881c50e
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 2%

---

# Trainingsrapporten maken {#design-jo-reports}

Naast [&#x200B; rapporten in real time &#x200B;](live-report.md) en ingebouwde [&#x200B; rapporteringsmogelijkheden &#x200B;](report-gs-cja.md), [!DNL Journey Optimizer] kunnen de gegevens van de vervoersprestaties automatisch verzenden naar Adobe Experience Platform zodat kan het met andere gegevens voor analysedoeleinden worden gecombineerd.

>[!NOTE]
>
>Deze functie wordt standaard geactiveerd bij alle gebeurtenissen voor stappen tijdens de reis. U kunt niet de schema&#39;s en datasets wijzigen of bijwerken die tijdens levering voor step gebeurtenissen zijn gecreeerd. Door gebrek, zijn deze schema&#39;s en datasets op read-only wijze.

U hebt bijvoorbeeld een reis ingesteld die meerdere e-mails verzendt. Met deze functie kunt u [!DNL Journey Optimizer] -gegevens combineren met gegevens over gebeurtenissen stroomafwaarts, zoals hoeveel conversies er hebben plaatsgevonden, hoeveel betrokkenheid er op de website heeft plaatsgevonden of hoeveel transacties er in de winkel hebben plaatsgevonden. De informatie over de reis kan worden gecombineerd met gegevens over Adobe Experience Platform, hetzij van andere digitale eigenschappen, hetzij van offline eigenschappen, voor een uitgebreider beeld van de prestaties.

[!DNL Journey Optimizer] leidt automatisch tot de noodzakelijke schema&#39;s en stromen in datasets aan Adobe Experience Platform voor elke stap een individu neemt in een reis. Een step-gebeurtenis komt overeen met een individuele gebeurtenis die zich tijdens een rit van het ene knooppunt naar het andere verplaatst. Bijvoorbeeld, in een reis die een gebeurtenis, een voorwaarde en een actie heeft, worden de drie stapgebeurtenissen verzonden naar Adobe Experience Platform.

>[!NOTE]
>
>Naast profiel-vlakke stapgebeurtenissen, produceert het systeem ook interne gebeurtenissen voor **Gelezen de activiteiten van het publiek**. Deze gebeurtenissen, `segmentExportJob` gebeurtenissen genoemd, registreren de levenscyclus van de Read knoop van de Publiek (zoals de schepping van de uitvoerbaan, het een rij vormen, voltooiing, en fouten) en worden geproduceerd per Gelezen activiteit van de Publiek, niet per individueel profiel. Hierdoor hebben deze gebeurtenissen mogelijk geen bijbehorende profiel-id (UPMID). Deze interne gebeurtenissen zijn nuttig voor controle en het oplossen van problemen Gelezen de prestaties van het Publiek en kunnen worden gevraagd gebruikend de gebieden die in de [&#x200B; worden gedocumenteerd serviceEvents sectie &#x200B;](../reports/sharing-field-list.md#servicevents-field). Voor vraagvoorbeelden op hoe te met segmentExportJob gebeurtenissen te werken, zie [&#x200B; Vragen met betrekking tot het Gelezen publiek &#x200B;](../reports/query-examples.md#read-segment-queries).

Er zijn gevallen waarin meerdere gebeurtenissen voor hetzelfde knooppunt kunnen worden gemaakt. Bijvoorbeeld, in het geval van de Wacht activiteit:

* Er wordt een gebeurtenis gegenereerd wanneer het profiel de wachttijd ingaat (het kenmerk tripNodeProcesses is gelijk aan false).
* Er wordt een gebeurtenis gegenereerd wanneer het profiel dit verlaat (het kenmerk tripNodeProcess is gelijk aan true)

De lijst met XDM-velden die worden doorgegeven, is uitgebreid. Sommige bevatten door het systeem gegenereerde codes en andere hebben door mensen leesbare vriendelijke namen. Voorbeelden zijn het label van de reisactiviteit of de stapstatus: hoe vaak een actie met een time-out of een fout is beëindigd.

>[!CAUTION]
>
>Datasets kunnen niet worden ingeschakeld voor realtime profielservice. Controleer of de schakeloptie **[!UICONTROL Profile]** is uitgeschakeld.

[!DNL Journey Optimizer] verzendt gegevens zoals deze zich voordoen, in het streamen. U kunt deze gegevens vragen met de Query-service. U kunt verbinding maken met Customer Journey Analytics of andere BI-gereedschappen om gegevens met betrekking tot deze stappen weer te geven.

De volgende schema&#39;s worden gemaakt:

* Gebeurtenisschema voor stap van de reis voor [!DNL Journey Orchestration] - gebeurtenis van de stap van de reis die aan een Meta-gegevens van de Reis wordt gebonden.
* Reisschema met reisvelden voor [!DNL Journey Orchestration] - Reismetagegevens voor het beschrijven van reizen.

![](assets/sharing1.png)

![](assets/sharing2.png)

De volgende datasets worden overgegaan:

* Gebeurtenissen reisstap
* Journeys

![](assets/sharing3.png)

De lijsten van XDM gebieden die tot Adobe Experience Platform worden overgegaan zijn hier gedetailleerd:

* [Lijst met gebeurtenisvelden voor stappen](../reports/sharing-field-list.md)
* [Gebeurtenisvelden voor oudere stappen](../reports/sharing-legacy-fields.md)

## Integratie met Customer Journey Analytics {#integration-cja}

[!DNL Journey Optimizer] stapgebeurtenissen kunnen aan andere datasets in [&#x200B; Adobe Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=nl-NL){target="_blank"} worden verbonden.

De algemene workflow is:

* [!DNL Customer Journey Analytics] voert de gegevensset &quot;Journey Step Event&quot; in.
* Het **profileID** gebied in het bijbehorende &quot;schema van de Gebeurtenis van de Stap van de Reis voor Journey Orchestration&quot;wordt bepaald als gebied van de Identiteit. In [!DNL Customer Journey Analytics], kunt u deze dataset aan een andere dataset dan verbinden die de zelfde waarde zoals de op persoon gebaseerde herkenningsteken heeft.
* Om deze dataset in [!DNL Customer Journey Analytics], voor dwars-kanaalreisanalyse te gebruiken, verwijs naar [&#x200B; documentatie van Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html?lang=nl-NL){target="_blank"}.

➡️ [&#x200B; Werk met Customer Journey Analytics &#x200B;](cja-ajo.md){target="_blank"}
