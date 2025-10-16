---
title: Prioritaire scores toewijzen aan reizen en campagnes
description: Leer hoe u prioriteitsscores kunt toewijzen aan reizen en campagnes.
role: User
level: Beginner
exl-id: f33ca0a8-ed33-4964-a85c-8705a4ff728e
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 1%

---

# Prioriteitsscores toewijzen {#priority}

Met Journey Optimizer kunt u een prioriteitsscore toewijzen aan een reis, een campagne of een actie voor een binnenkomend kanaal binnen de **[!UICONTROL Action]** -activiteit.

Prioriteit is essentieel om prioriteit te geven aan een reis, campagne of actie wanneer er een opgelegde beperking is (zoals een frequentiegrens).

In situaties waar een klant voor vele reizen, campagnes, of mededelingen kwalificeert en u selectief wilt zijn wat zij zouden moeten ingaan en ontvangen, zou u dit gebied moeten gebruiken.

## Prioritaire scores toewijzen aan reizen en campagnes {#priority-journey-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Prioriteit"
>abstract="Wijs een prioriteitsscore toe aan de campagne. Prioriteit is essentieel om prioriteit te geven aan een campagne wanneer er een opgelegde beperking is, zoals een frequentiegrens.</br> ga een numerieke waarde (van 0-100) in. Let op: hoe hoger het getal, hoe hoger de prioriteit. Voor situaties waarin twee campagnes dezelfde prioriteitsscore hebben, wordt de campagne weergegeven die als eerste werd geactiveerd."

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Prioriteit"
>abstract="Wijs een prioritaire score toe aan de reis. Prioriteit is essentieel om prioriteit te geven aan een reis wanneer er een opgelegde beperking is, zoals een frequentiegrens.</br> ga een numerieke waarde (van 0-100) in. Let op: hoe hoger het getal, hoe hoger de prioriteit. Voor situaties waarin twee ritten dezelfde prioriteitsscore hebben, wordt de reis die als eerste werd ingezet, getoond."

➡️ [Ontdek deze functie in video](#video)

Het toewijzen van een prioritaire score is essentieel voor binnenkomende communicatie zoals Web, Mobiel, &amp; in-App. Als u meerdere campagnes hebt met dezelfde kanaalconfiguratie (bijvoorbeeld een banner boven op uw webpagina), kan dit problematisch zijn omdat slechts inhoud van één campagne gemakkelijk kan worden weergegeven. Bij de prioriteitsscore voegt u uw voorkeur in waarvoor de campagne moet worden weergegeven wanneer de ontvanger in aanmerking komt voor meer dan één campagne.

>[!NOTE]
>
>In campagnes is de prioriteitsscore alleen beschikbaar voor het web, in-app en op code gebaseerde inkomende kanalen.

Als u een prioriteitsscore wilt toewijzen aan een reis of campagne, voert u een numerieke waarde (van 0 tot 100) in het veld **[!UICONTROL Priority score]** in in de eigenschappen van de reis of campagne. Hoe hoger het getal, hoe hoger de prioriteit.

Als u deze campagne zou ontwerpen en ervoor wilde zorgen dat deze inhoud van de campagne wordt getoond, zou u het een score van 100 geven.

![](assets/priority-score.png)

>[!IMPORTANT]
>
>Als twee reizen of campagnes dezelfde prioriteitsscore hebben, heeft het systeem geen mechanisme voor het afbreken van de verbinding. Ervoor zorgen dat prioriteitsscores uniek zijn om conflicten te voorkomen.

## Prioriteitsscores toewijzen aan binnenkomende kanaalhandelingen {#priority-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_priority"
>title="Prioriteit"
>abstract="Wijs een prioritaire score aan de reisactie toe. Prioriteit is essentieel om een binnenkomende actie voorrang te geven wanneer er veelvoudige reisacties of campagnes gebruikend de zelfde kanaalconfiguratie zijn.</br> ga een numerieke waarde (van 0-100) in. Let op: hoe hoger het getal, hoe hoger de prioriteit. Standaard wordt de prioriteitsscore voor de actie overgenomen van de algemene prioriteitsscore voor de reis."

Journey Optimizer staat u ook toe om een prioritaire score aan binnenkomende kanaalacties binnen de [&#x200B; Actie &#x200B;](../building-journeys/journey-action.md) activiteit toe te wijzen.

Dit staat u toe om aan een binnenkomende actie voorrang te geven wanneer er veelvoudige reisacties of campagnes gebruikend de zelfde kanaalconfiguratie zijn.

>[!NOTE]
>
>In de **[!UICONTROL Action]** -activiteit is de prioriteitsscore alleen beschikbaar voor het web, in-app en op code gebaseerde binnenkomende kanalen.

In de sectie **[!UICONTROL Conflict management]** is de optie **[!UICONTROL Use journey priority]** standaard geselecteerd. Dit houdt in dat de prioriteitsscore voor de actie wordt overgenomen van de algemene prioriteitsscore voor de reis.

Als u een prioriteitsscore wilt toewijzen aan de binnenkomende acties die zijn gedefinieerd in de **[!UICONTROL Action]** -activiteit, schakelt u de optie **[!UICONTROL Use journey priority]** uit en voert u een numerieke waarde (van 0 tot 100) in het **[!UICONTROL Priority]** -veld in. Hoe hoger het getal, hoe hoger de prioriteit.

![](assets/action-journey-priority-score.png){width=70%}

## Hoe kan ik-video {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435529?quality=12)
