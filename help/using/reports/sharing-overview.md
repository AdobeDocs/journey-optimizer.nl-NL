---
title: Overzicht van het delen van journeystappen
description: Overzicht van het delen van journeystappen
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 07d25f8e-0065-4410-9895-ffa15d6447bb
source-git-commit: 1fa91a841d4f941f2c5bd1efd4a06ac8a9938bc7
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 3%

---

# Trainingsrapporten maken {#design-jo-reports}

Naast [real-time rapporten](live-report.md) en ingebouwde [algemene rapportagemogelijkheden](global-report.md), [!DNL Journey Optimizer] kunnen automatisch gegevens over de reisprestaties naar Adobe Experience Platform sturen, zodat deze voor analysedoeleinden met andere gegevens kunnen worden gecombineerd.

>[!NOTE]
>
>Deze functie wordt standaard geactiveerd bij alle gebeurtenissen voor stappen tijdens de reis. U kunt niet de schema&#39;s en datasets wijzigen of bijwerken die tijdens levering voor step gebeurtenissen zijn gecreeerd. Door gebrek, zijn deze schema&#39;s en datasets op read-only wijze.

U hebt bijvoorbeeld een reis ingesteld die meerdere e-mails verzendt. Dankzij deze functie kunt u [!DNL Journey Optimizer] gegevens met downstreamgebeurtenisgegevens zoals hoeveel conversies hebben plaatsgevonden, hoeveel betrokkenheid op de website heeft plaatsgevonden of hoeveel transacties in de winkel hebben plaatsgevonden. De informatie over de reis kan worden gecombineerd met gegevens over Adobe Experience Platform, hetzij van andere digitale eigenschappen, hetzij van offline eigenschappen, voor een uitgebreider beeld van de prestaties.

[!DNL Journey Optimizer] leidt automatisch tot de noodzakelijke schema&#39;s en stromen in datasets aan Adobe Experience Platform voor elke stap een individu in een reis neemt. Een step-gebeurtenis komt overeen met een individuele gebeurtenis die zich tijdens een rit van het ene knooppunt naar het andere verplaatst. Bijvoorbeeld, in een reis die een gebeurtenis, een voorwaarde en een actie heeft, worden de drie stapgebeurtenissen verzonden naar Adobe Experience Platform.

De lijst met XDM-velden die worden doorgegeven, is uitgebreid. Sommige bevatten door het systeem gegenereerde codes en andere hebben door mensen leesbare vriendelijke namen. Voorbeelden zijn het etiket van de reisactiviteit of de stapstatus: hoe vaak een time-out of een fout is opgetreden.

>[!CAUTION]
>
>Datasets kunnen niet worden ingeschakeld voor realtime profielservice. Controleer of de **[!UICONTROL Profile]** schakeloptie is uitgeschakeld.

[!DNL Journey Optimizer] verzendt gegevens aangezien het voorkomt, op een het stromen manier. U kunt deze gegevens vragen met de Query-service. U kunt verbinding maken met Customer Journey Analytics of andere BI-gereedschappen om gegevens met betrekking tot deze stappen weer te geven.

De volgende schema&#39;s worden gemaakt:

* Dagstapgebeurtenisschema voor [!DNL Journey Orchestration] - Reisstapgebeurtenis die is gekoppeld aan een Reismetagegevens.
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

[!DNL Journey Optimizer] step-gebeurtenissen kunnen worden gekoppeld aan andere datasets in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html){target=&quot;_blank&quot;}.

De algemene workflow is:

* [!DNL Customer Journey Analytics] Neemt de dataset &quot;Journey Step Event&quot; op.
* De **profileID** veld in het bijbehorende &quot;Dagboekstapschema voor Journey Orchestration&quot; wordt gedefinieerd als een identiteitsveld. In [!DNL Customer Journey Analytics], kunt u deze dataset aan een andere dataset dan verbinden die de zelfde waarde zoals persoon gebaseerde herkenningsteken heeft.
* Deze gegevensset gebruiken in [!DNL Customer Journey Analytics], voor de analyse van de kanaalreis, zie [Customer Journey Analytics-documentatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html){target=&quot;_blank&quot;}.

