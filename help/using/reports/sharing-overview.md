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
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 2%

---

# Trainingsrapporten maken {#design-jo-reports}

Naast [ rapporten in real time ](live-report.md) en ingebouwde [ rapporteringsmogelijkheden ](report-gs-cja.md), [!DNL Journey Optimizer] kunnen de gegevens van de vervoersprestaties automatisch verzenden naar Adobe Experience Platform zodat kan het met andere gegevens voor analysedoeleinden worden gecombineerd.

>[!NOTE]
>
>Deze functie wordt standaard geactiveerd bij alle gebeurtenissen voor stappen tijdens de reis. U kunt niet de schema&#39;s en datasets wijzigen of bijwerken die tijdens levering voor step gebeurtenissen zijn gecreeerd. Door gebrek, zijn deze schema&#39;s en datasets op read-only wijze.

U hebt bijvoorbeeld een reis ingesteld die meerdere e-mails verzendt. Met deze functie kunt u [!DNL Journey Optimizer] -gegevens combineren met gegevens over gebeurtenissen stroomafwaarts, zoals hoeveel conversies er hebben plaatsgevonden, hoeveel betrokkenheid er op de website heeft plaatsgevonden of hoeveel transacties er in de winkel hebben plaatsgevonden. De informatie over de reis kan worden gecombineerd met gegevens over Adobe Experience Platform, hetzij van andere digitale eigenschappen, hetzij van offline eigenschappen, voor een uitgebreider beeld van de prestaties.

[!DNL Journey Optimizer] leidt automatisch tot de noodzakelijke schema&#39;s en stromen in datasets aan Adobe Experience Platform voor elke stap een individu neemt in een reis. Een step-gebeurtenis komt overeen met een individuele gebeurtenis die zich tijdens een rit van het ene knooppunt naar het andere verplaatst. Bijvoorbeeld, in een reis die een gebeurtenis, een voorwaarde en een actie heeft, worden de drie stapgebeurtenissen verzonden naar Adobe Experience Platform.

Er zijn gevallen waarin meerdere gebeurtenissen voor hetzelfde knooppunt kunnen worden gemaakt. Bijvoorbeeld, in het geval van de Wacht activiteit:

* Er wordt een gebeurtenis gegenereerd wanneer het profiel de wachttijd ingaat (het kenmerk tripNodeProcesses is gelijk aan false).
* Er wordt een gebeurtenis gegenereerd wanneer het profiel dit verlaat (het kenmerk tripNodeProcess is gelijk aan true)

De lijst met XDM-velden die worden doorgegeven, is uitgebreid. Sommige bevatten door het systeem gegenereerde codes en andere hebben door mensen leesbare vriendelijke namen. Voorbeelden zijn het label van de reisactiviteit of de stapstatus: hoe vaak een actie met een time-out of een fout is beëindigd.

>[!CAUTION]
>
>Datasets kunnen niet worden ingeschakeld voor realtime profielservice. Controleer of de schakeloptie **[!UICONTROL Profile]** is uitgeschakeld.

[!DNL Journey Optimizer] verzendt gegevens op streamingwijze zoals deze zich voordoen. U kunt deze gegevens vragen met de Query-service. U kunt verbinding maken met Customer Journey Analytics of andere BI-gereedschappen om gegevens met betrekking tot deze stappen weer te geven.

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

[!DNL Journey Optimizer] stapgebeurtenissen kunnen aan andere datasets in [ Adobe Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html){target="_blank"}  worden verbonden.

De algemene workflow is:

* [!DNL Customer Journey Analytics] voert de gegevensset &quot;Journey Step Event&quot; in.
* Het **profileID** gebied in het bijbehorende schema van de Gebeurtenis van de Stap van de Reis voor Journey Orchestration&quot;wordt bepaald als gebied van de Identiteit. In [!DNL Customer Journey Analytics], kunt u deze dataset aan een andere dataset dan verbinden die de zelfde waarde zoals de op persoon gebaseerde herkenningsteken heeft.
* Om deze dataset in [!DNL Customer Journey Analytics], voor dwars-kanaalreisanalyse te gebruiken, verwijs naar [ documentatie van de Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html){target="_blank"} .

➡️ [ Werk met Customer Journey Analytics ](cja-ajo.md){target="_blank"}
