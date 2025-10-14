---
solution: Journey Optimizer
product: journey optimizer
title: Uw doeldimensie maken
description: Leer hoe te om een relationeel schema aan het klantenprofiel in kaart te brengen
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
version: Campaign Orchestration
source-git-commit: 0b92d0e806c47b0d87ba53b7c7f1d56ee4453abb
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---


# Een doeldimensie configureren {#configuration}

Met **[!UICONTROL Orchestrated Campaigns]**, kunt u gerichte mededelingen op entiteitniveau ontwerpen en leveren, leveraging Adobe Experience Platform relationele schemamogelijkheden. Experience Platform gebruikt schema&#39;s om de gegevensstructuur op een consistente en herbruikbare manier te beschrijven. Wanneer gegevens in Experience Platform worden opgenomen, worden ze gestructureerd volgens een XDM-schema.

Hoewel de segmentatie voor **[!UICONTROL Orchestrated Campaigns]** hoofdzakelijk op relationele schema&#39;s werkt, komt de daadwerkelijke berichtlevering altijd op het **niveau van het Profiel** voor.

Wanneer het vormen richt, bepaalt u twee zeer belangrijke aspecten:

* **gerichte Schema&#39;s**

  U geeft op welke relationele schema&#39;s geschikt zijn voor doelframes. Standaard wordt het schema met de naam `Recipient` gebruikt, maar u kunt alternatieven configureren, zoals `Visitors` , `Customers` .

  >[!IMPORTANT]
  >
  > Het doelschema moet een 1 :1 verhouding met het `Profile` schema hebben. U kunt `Purchases` bijvoorbeeld niet gebruiken als een doelschema, omdat dit doorgaans een een-op-een-relatie vertegenwoordigt.

* **Verbinding van het Profiel**

  Het systeem moet begrijpen hoe het doelschema aan het `Profile` schema in kaart brengt. Dit wordt bereikt door een gedeeld identiteitsgebied - dat zowel in het doelschema als het `Profile` schema bestaat en als identiteitsnaamruimte gevormd.

## Uw doeldimensie maken {#targeting-dimension}

Begin door campagneorchestratie op te zetten door een relationeel schema aan het klantenprofiel in kaart te brengen.

1. Open vanuit **[!UICONTROL Administration]** het menu **[!UICONTROL Configurations]** en selecteer **[!UICONTROL Campaign Target Dimension]** .

   ![](assets/target-dimension-1.png)

1. Klik op **[!UICONTROL Create]** om uw **[!UICONTROL Targeting dimension]** -bestand te maken.

1. Kies uw [&#x200B; eerder gevormd Schema &#x200B;](gs-schemas.md) &#x200B; van drop-down.

   Terwijl alle relationele schema&#39;s zichtbaar zijn, slechts zijn de schema&#39;s met een directe identiteitsverhouding aan het **Profiel** verkiesbaar voor selectie.

1. Selecteer **[!UICONTROL Identity value]** die de entiteit vertegenwoordigt u wilt richten.

   In dit voorbeeld is het klantprofiel gekoppeld aan meerdere abonnementen, die elk worden vertegenwoordigd door een uniek `crmID` in het `Recipient` -schema. Als u **[!UICONTROL Target Dimension]** instelt om het `Recipient` schema en de `crmID` identiteit te gebruiken, kunt u berichten verzenden op abonnementsniveau in plaats van naar het hoofdklantprofiel, zodat elk contract of elke regel een eigen gepersonaliseerd bericht ontvangt.

   [&#x200B; leer meer in de documentatie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/schema/composition#identity)

   ![](assets/target-dimension-2.png)

1. Klik op **[!UICONTROL Save]** om de installatie te voltooien. Een **[!UICONTROL Target dimension]** kan na het maken niet worden verwijderd of bewerkt.

Nadat u de **[!UICONTROL Target Dimension]** hebt geconfigureerd, gaat u verder met het maken en instellen van de **[!UICONTROL Channel Configuration]** en het definiëren van de bijbehorende **[!UICONTROL Execution Details]** .