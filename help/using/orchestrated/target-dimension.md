---
solution: Journey Optimizer
product: journey optimizer
title: Uw doeldimensie maken
description: Leer hoe te om een relationeel schema aan het klantenprofiel in kaart te brengen
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
version: Campaign Orchestration
source-git-commit: f842142a985481004192c88af2973787912c85b3
workflow-type: tm+mt
source-wordcount: '413'
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
  > De geordende Campagnes staan het richten op om het even welk schema toe dat een directe of verwante verhouding aan het **schema van het Profiel** heeft. Terwijl zijn gebruik hoofdzakelijk op 1 :1 verhoudingen voorgenomen is, steunt het ook 1 :N verhoudingen, zoals de Ontvangers van de Rekening `>`, zolang de relatieweg behoorlijk in het gegevensmodel wordt gemodelleerd. Dit laat het richten toe op basis van op rekeningsniveau gegevens terwijl nog het oplossen van de correcte profielidentiteit voor berichtlevering.

* **Verbinding van het Profiel**

  Het systeem moet begrijpen hoe het doelschema aan het `Profile` schema in kaart brengt. Dit wordt bereikt door een gedeeld identiteitsgebied - dat zowel in het doelschema als het `Profile` schema bestaat en als identiteitsnaamruimte gevormd.

➡️ [&#x200B; Leer meer over relationele schema&#39;s in de documentatie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/schema/relational#how-relational-schemas-differ-from-standard-xdm-schemas)

## Uw doeldimensie maken {#targeting-dimension}

Begin door campagneorchestratie op te zetten door een relationeel schema aan het klantenprofiel in kaart te brengen.

1. Open vanuit **[!UICONTROL Administration]** het menu **[!UICONTROL Configurations]** en selecteer **[!UICONTROL Campaign Target Dimension]** .

   ![](assets/target-dimension-1.png)

1. Klik op **[!UICONTROL Create]** om uw **[!UICONTROL Targeting dimension]** -bestand te maken.

1. Kies uw [&#x200B; eerder gevormd Schema &#x200B;](gs-schemas.md) &#x200B; van drop-down.

   Terwijl alle relationele schema&#39;s worden getoond, slechts zijn die met een direct identiteitsverband met **Profiel** verkiesbaar voor selectie. U kunt geen andere schema&#39;s kiezen, bijvoorbeeld aankopen, en een schema selecteren dat rechtstreeks aan een profiel is gekoppeld.

1. Selecteer **[!UICONTROL Identity value]** die de entiteit vertegenwoordigt u wilt richten.

   In dit voorbeeld is het klantprofiel gekoppeld aan meerdere abonnementen, die elk worden vertegenwoordigd door een uniek `crmID` in het `Recipient` -schema. Als u **[!UICONTROL Target Dimension]** instelt om het `Recipient` schema en de `crmID` identiteit te gebruiken, kunt u berichten verzenden op abonnementsniveau in plaats van naar het hoofdklantprofiel, zodat elk contract of elke regel een eigen gepersonaliseerd bericht ontvangt.

   [&#x200B; leer meer in de documentatie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/schema/composition#identity)

   ![](assets/target-dimension-2.png)

1. Klik op **[!UICONTROL Save]** om de installatie te voltooien. Een **[!UICONTROL Target dimension]** kan na het maken niet worden verwijderd of bewerkt.

Nadat u de **[!UICONTROL Target Dimension]** hebt geconfigureerd, gaat u verder met het maken en instellen van de **[!UICONTROL Channel Configuration]** en het definiëren van de bijbehorende **[!UICONTROL Execution Details]** .