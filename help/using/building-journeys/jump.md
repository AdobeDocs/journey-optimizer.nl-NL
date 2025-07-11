---
solution: Journey Optimizer
product: journey optimizer
title: Van de ene journey naar de andere gaan
description: Van de ene journey naar de andere gaan
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: springen, activiteit, reis, splitsen, splitsen
exl-id: 46d8950b-8b02-4160-89b4-1c492533c0e2
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 2%

---

# Van de ene reis naar de andere gaan {#jump}

>[!CONTEXTUALHELP]
>id="ajo_journey_jump"
>title="Snelheid"
>abstract="Met de actie Snelheid kunt u individuen van de ene reis naar de andere duwen. Met deze functie kunt u het ontwerp van zeer complexe reizen vereenvoudigen en reizen maken op basis van gemeenschappelijke en herbruikbare reispatronen."

Met de actieactiviteit **[!UICONTROL Jump]** kunt u personen van de ene reis naar de andere verplaatsen. Met deze functie kunt u:

* vereenvoudigen het ontwerp van zeer complexe reizen door deze in verschillende te splitsen
* ritten bouwen op basis van gemeenschappelijke en herbruikbare reispatronen

Voeg in de oorspronkelijke rit een **[!UICONTROL Jump]** activiteit toe en selecteer een doelreis. Wanneer het individu de **[!UICONTROL Jump]** stap ingaat, wordt een interne gebeurtenis verzonden naar de eerste gebeurtenis van de doelreis. Als de **[!UICONTROL Jump]** actie slaagt, blijft het individu in de reis voortgaan. Het gedrag is vergelijkbaar met andere acties.

Tijdens de doelrit maakt de eerste gebeurtenis die intern door de **[!UICONTROL Jump]** -activiteit wordt geactiveerd, de individuele flow in de reis.

## Levenscyclus {#jump-lifecycle}

Veronderstel u a **[!UICONTROL Jump]** activiteit in reis A aan reis B. Reis A is de **oorsprongstransport**, en reis B is de **doelreis** toegevoegd.

Hier volgen de verschillende stappen van het uitvoeringsproces:

**Reis A** wordt teweeggebracht van een externe gebeurtenis:

1. Reis A ontvangt een externe gebeurtenis met betrekking tot een individu.
1. De persoon bereikt de **[!UICONTROL Jump]** -stap.
1. Het individu wordt geduwd op reis B en gaat naar de volgende stappen in reis A, na de **[!UICONTROL Jump]** stap.

Bij reis B wordt de eerste gebeurtenis intern geactiveerd via de **[!UICONTROL Jump]** -activiteit van reis A:

1. Reis B ontvangt een intern evenement van reis A.
1. Het individu begint te stromen in reis B.

>[!NOTE]
>
>Reis B kan ook worden geactiveerd via een externe gebeurtenis.

## Best practices en beperkingen {#jump-limitations}

### Authoring {#jump-limitations-authoring}

* De **[!UICONTROL Jump]** -activiteit is alleen beschikbaar voor reizen die een naamruimte gebruiken.
* U kunt alleen naar een reis springen die dezelfde naamruimte gebruikt als de oorspronkelijke reis.
* U kunt niet aan een reis springen die met een **gebeurtenis van de Kwalificatie van het publiek 0&rbrace; &lbrace;of** Gelezen Publiek **begint.**
* U kunt geen a **[!UICONTROL Jump]** activiteit en a **2&rbrace; gebeurtenis van de Kwalificatie van het Publiek of** Gelezen Publiek **in de zelfde reis hebben.**
* U kunt zoveel **[!UICONTROL Jump]** activiteiten opnemen als u nodig hebt voor een reis. Na een **[!UICONTROL Jump]** kunt u alle benodigde activiteiten toevoegen.
* U kunt zo veel sprongniveaus hebben zoals nodig. Zo springt een A naar reis B, die naar reis C gaat, enzovoort.
* De doeltocht kan ook zoveel **[!UICONTROL Jump]** activiteiten omvatten als nodig is.
* Luspatronen worden niet ondersteund. Er is geen manier om twee of meer reizen aan elkaar te koppelen, wat een oneindige lus zou creëren. Het scherm van de **[!UICONTROL Jump]** activiteitenconfiguratie verhindert u dit te doen.

### Execution {#jump-limitations-exec}

* Wanneer de **[!UICONTROL Jump]** activiteit wordt uitgevoerd, wordt de recentste versie van de doelreis teweeggebracht.
* Een uniek individu kan slechts één keer op dezelfde reis aanwezig zijn. Als het individu dat van de oorspronkelijke reis werd verdreven, zich al in de doelreis bevindt, zal het individu de doelreis niet betreden. Er wordt geen fout gerapporteerd over de **[!UICONTROL Jump]** -activiteit omdat dit normaal gedrag is.

## De sprongactiviteit configureren {#jump-configure}

1. Ontwerp uw **originele reis**.

   ![](assets/jump1.png)

1. Voeg bij elke stap van de rit een **[!UICONTROL Jump]** activiteit toe vanuit de categorie **[!UICONTROL ACTIONS]** . Voeg een label en beschrijving toe.

   ![](assets/jump2.png)

1. Klik binnen het **reis van het Doel** gebied.
In de lijst worden alle reisversies weergegeven die concept, live of in de testmodus zijn. De reizen die een verschillende namespace gebruiken of die met een **gebeurtenis van de Kwalificatie van het publiek 0&rbrace; beginnen zijn niet beschikbaar.** Doeltrajecten die een luspatroon zouden maken, worden ook uitgefilterd.

   ![](assets/jump3.png)

   >[!NOTE]
   >
   >U kunt het **Open doelreis** pictogram, op de rechterkant klikken, om de doelreis in een nieuw lusje te openen.

1. Selecteer de doelreis waarnaar u wilt springen.
Het **Eerste gebeurtenis** gebied wordt voorgevuld met de naam van de eerste gebeurtenis van de doelreis. Als uw doelreis meerdere gebeurtenissen bevat, is **[!UICONTROL Jump]** alleen toegestaan voor de eerste gebeurtenis.

   ![](assets/jump4.png)

1. De **parameters van de Actie** sectie toont alle gebieden van de doelgebeurtenis. Elk veld toewijzen met velden uit de gebeurtenis of gegevensbron, net als met andere typen acties. Deze informatie wordt tijdens runtime doorgegeven aan de doelroute.
1. Voeg de volgende activiteiten toe om uw oorspronkelijke reis te voltooien.

   ![](assets/jump5.png)


   >[!NOTE]
   >
   >De identiteit van het individu wordt automatisch toegewezen. Deze informatie is niet zichtbaar in de interface.

Uw **[!UICONTROL Jump]** activiteit wordt gevormd. Zodra uw reis live is of in de testmodus, worden personen die de **[!UICONTROL Jump]** -stap bereiken, naar de doeltocht verplaatst.

Wanneer een **[!UICONTROL Jump]** activiteit in een reis wordt gevormd, wordt een **[!UICONTROL Jump]** ingangspictogram automatisch toegevoegd aan het begin van de doelreis. Dit helpt u identificeren dat de reis extern maar ook intern van een **[!UICONTROL Jump]** activiteit kan worden teweeggebracht.

![](assets/jump7.png)

## Problemen oplossen {#jump-troubleshoot}

Er treden fouten op als:

* De doelreis bestaat niet meer
* De doelreis is een concept, gesloten of gestopt
* De eerste gebeurtenis van de doelreis is veranderd, en de afbeelding is gebroken

![](assets/jump6.png)
