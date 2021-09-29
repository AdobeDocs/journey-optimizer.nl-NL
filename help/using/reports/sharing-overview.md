---
title: Overzicht van het delen van journeystappen
description: Overzicht van het delen van journeystappen
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 07d25f8e-0065-4410-9895-ffa15d6447bb
source-git-commit: 7e4b5342fc57029517ae4d6a6c1e8e03e0dc0c3b
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 6%

---

# Trainingsrapporten maken{#design-jo-reports}

Naast [real-time rapporten](live-report.md) en ingebouwde [global reporting mogelijkheden](global-report.md), kan [!DNL Journey Optimizer] automatisch gegevens over de reisprestaties naar Adobe Experience Platform verzenden, zodat deze met andere gegevens voor analysedoeleinden kunnen worden gecombineerd.

>[!NOTE]
>
>Deze functie wordt standaard geactiveerd bij alle gebeurtenissen voor stappen tijdens de reis. Voor trapsgewijze gebeurtenissen voor het reisprofiel wordt de activering op verzoek uitgevoerd. U kunt niet de schema&#39;s en datasets wijzigen of bijwerken die tijdens levering voor step gebeurtenissen zijn gecreeerd. Door gebrek, zijn deze schema&#39;s en datasets op read-only wijze.

U hebt bijvoorbeeld een reis ingesteld die meerdere e-mails verzendt. Met deze functie kunt u [!DNL Journey Optimizer]-gegevens combineren met gegevens over gebeurtenissen in de downstream, zoals hoeveel conversies er hebben plaatsgevonden, hoeveel betrokkenheid er op de website heeft plaatsgevonden of hoeveel transacties er in de winkel hebben plaatsgevonden. De informatie over de reis kan worden gecombineerd met gegevens over Adobe Experience Platform, hetzij van andere digitale eigenschappen, hetzij van offline eigenschappen, voor een uitgebreider beeld van de prestaties.

[!DNL Journey Optimizer] leidt automatisch tot de noodzakelijke schema&#39;s en stromen in datasets aan Adobe Experience Platform voor elke stap een individu in een reis neemt. Een step-gebeurtenis komt overeen met een individuele gebeurtenis die zich tijdens een rit van het ene knooppunt naar het andere verplaatst. Bijvoorbeeld, in een reis die een gebeurtenis, een voorwaarde en een actie heeft, worden de drie stapgebeurtenissen verzonden naar Adobe Experience Platform.

De lijst met XDM-velden die worden doorgegeven, is uitgebreid. Sommige bevatten door het systeem gegenereerde codes en andere hebben door mensen leesbare vriendelijke namen. Voorbeelden zijn het etiket van de reisactiviteit of de stapstatus: hoe vaak een time-out of een fout is opgetreden.

>[!CAUTION]
>
>Datasets kunnen niet worden ingeschakeld voor realtime profielservice. Controleer of de schakeloptie **[!UICONTROL Profile]** is uitgeschakeld.

De reizen verzenden gegevens aangezien het voorkomt, op een het stromen manier. U kunt deze gegevens vragen met de Query-service. U kunt verbinding maken met Customer Journey Analytics of andere BI-gereedschappen om gegevens met betrekking tot deze stappen weer te geven.

De volgende schema&#39;s worden gemaakt:

* Gebeurtenissenschema voor trede-stapprofiel voor [!DNL Journey Orchestration] - Ervaar gebeurtenissen voor stappen die in een reis samen met een identiteitskaartje zijn uitgevoerd en die moeten worden gebruikt voor toewijzing aan een individuele deelnemer aan de reis.
* Gebeurtenisschema voor stap van de reis voor [!DNL Journey Orchestration] - gebeurtenis van de stap van de reis die aan een Meta-gegevens van de Reis wordt gebonden.
* Reisschema met reisvelden voor [!DNL Journey Orchestration] - Reismetagegevens om reizen te beschrijven.

![](../assets/sharing1.png)

![](../assets/sharing2.png)

De volgende datasets worden overgegaan:

* Gebeurtenisschema voor stapsgewijze reis voor [!DNL Journey Orchestration]
* Gebeurtenissen reisstap
* Journeys

![](../assets/sharing3.png)

De lijsten van XDM gebieden die tot Adobe Experience Platform worden overgegaan zijn hier gedetailleerd:

* [Gemeenschappelijke velden van journeySteps-gebeurtenissen](../reports/sharing-common-fields.md)
* [Velden voor het uitvoeren van acties van journeyStep-gebeurtenissen](../reports/sharing-execution-fields.md)
* [Velden voor het ophalen van gegevens van journeyStep-gebeurtenissen](../reports/sharing-fetch-fields.md)
* [Identiteitsvelden van journeyStep-gebeurtenissen](../reports/sharing-identity-fields.md)
* [journeyvelden](../reports/sharing-journey-fields.md)

Voor meer informatie over step gebeurtenissen die aan Adobe Experience Platform rapporteren, bekijk deze [zelfstudie video](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/reporting-step-events-to-adobe-experience-platform.html){target=&quot;_blank&quot;}.
