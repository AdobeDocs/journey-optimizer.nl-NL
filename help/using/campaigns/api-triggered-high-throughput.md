---
solution: Journey Optimizer
product: journey optimizer
title: De modus Hoge doorvoer activeren voor door API geïnitieerde campagnes
description: Leer hoe u de modus Hoge doorvoer activeert voor door API geactiveerde campagnes.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagnes, API-geactiveerd, REST, optimizer, berichten
source-git-commit: 5a6abcd48495a66496495e62c6027c2fd0fdd4c4
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---


# De modus Hoge doorvoer activeren voor door API geïnitieerde campagnes {#high-throughput}

De hoge wijze van de Productie wordt ontworpen voor organisaties die **zeer groot, transactioneel overseinen in real time** (tot 5000 transacties per seconde) nodig hebben. In tegenstelling tot reguliere API-campagnes werken campagnes met hoge doorvoer onafhankelijk van Adobe-profielen en vereisen deze een ander configuratiemodel.

Op deze pagina wordt uitgelegd hoe campagnes met hoge doorvoer verschillen van standaard API-getriggerde campagnes, instellingsvereisten en wanneer elke modus moet worden gekozen.

## Afbeeldingen en beperkingen

* **Toegang** - Beschikbaar slechts in het gebied van de V.S. voor organisaties die met de Hoge het overseinentoe:voegen-op van de Transactie van de Productie vergunning hebben gekregen.

* **Kanalen**: Momenteel beschikbaar slechts voor e-mail.

* **Personalization**:

   * Al verpersoonlijking moet in de API nuttige lading als **contextafhankelijke gegevens** worden omvat. [&#x200B; Leer hoe te om inhoud te personaliseren gebruikend contextuele gegevens &#x200B;](../campaigns/api-triggered-campaign-action.md#contextual)
   * Aanpassing op basis van profielen wordt niet ondersteund. Als profielvariabelen worden gebruikt, treden validatiefouten op.

* **Gepersonaliseerde kanaalconfiguraties** - de configuraties van het Kanaal die [&#x200B; op profiel-gebaseerde verpersoonlijking &#x200B;](../email/surface-personalization.md) gebruiken kunnen niet met hoge productiecampagnes worden gebruikt. U kunt alleen oppervlakken gebruiken zonder profielpersonalisatie.

* **API eindpunt** - de Hoge campagnes van de Output gebruiken een verschillend eindpunt dan standaardAPI getriggerde campagnes. Voor details, zie [&#x200B; een API teweeggebrachte campagne &#x200B;](../campaigns/trigger-campaigns.md#trigger) uitvoeren.

* **de exclusiviteit van de Campagne** - de Hoge productie campagnes gebruiken geen Profielen van Adobe. Berichten worden geleverd ongeacht of er een profiel bestaat.

  Bovendien kan een campagne niet voor zowel profiel-toegelaten als niet-profiel gebruiksgevallen worden gebruikt. Als u beide nodig hebt, maakt u twee aparte campagnes en zorgt u ervoor dat het aanroepende systeem besluit welke campagne op basis van de context moet worden gestart.

## Kiezen tussen standaard- en hoge-doorvoercampagnes

Gebruik deze tabel om te bepalen welk type API-activering van het campagneretype in uw gebruiksscenario past:

| Functie/vereiste | Standaard API-activering | Campagne met hoge doorvoer |
|------------------------|---------------------------------|---------------------------|
| **Beschikbaarheid** | Opgenomen in basisaanbieding | Vereist een add-on voor transactionele berichten met hoge doorvoer. |
| **Output** | Maximaal 500 transacties per seconde | Maximaal 5000 transacties per seconde |
| **Kanalen** | E-mail, SMS, Push | Email |
| **Personalization** | Profiel + contextafhankelijk in de API-lading | Contextueel alleen in de API-payload |
| **Profiel &amp; stitching** | Bestaat of wordt gemaakt met gebeurtenissen die aan profiel zijn gekoppeld | Geen profiel |
| **Volume van het Bericht** | Standaardmachtiging en berichtpakketten | Afzonderlijke gelaagde berichtvolumes |
| **Infrastructuur** | Standard | Verbeterd |
| **Uptime** | 99,9% | 99,99% |
| **Controle API van de Gezondheid** | Ja | Ja |

Met andere woorden:

* Kies **Standaard API getriggerde** campagnes als:
   * U hebt geen hoge doorvoerinstelling.
   * Uw doorvoer is &lt;500 TPS.
   * U hebt personalisatie op basis van Adobe-profielen nodig.
   * U wilt campagnegegevens aan profielen voor toekomstige richten vastmaken.
   * U wilt een ander kanaal gebruiken dan E-mail.

* Kies **Hoge productie** campagnes als:
   * U hebt doorvoer > 500 TPS nodig.
   * U hebt geen profielstitching nodig.
   * U kunt alle personalisatie in de API-lading doorgeven.
   * U wilt het e-mailkanaal gebruiken.

## Richtlijnen instellen

Volg de volgende richtlijnen om campagnes met hoge doorvoer correct te configureren:

1. Creeer een nieuwe IP pool. [&#x200B; Leer hoe te om IP tot stand te brengen pools &#x200B;](../configuration/ip-pools.md)
1. Maak een nieuwe kanaalconfiguratie. [&#x200B; leer hoe te de configuraties van het opstellingskanaal &#x200B;](../configuration/channel-surfaces.md)
1. Neem contact op met de klantenservice van Adobe om te vragen dat het geactiveerde oppervlak wordt toegewezen aan de functie voor hoge doorvoer. Geef de kanaalconfiguratie en IP-groepsgegevens op, samen met uw organisatie-id.

>[!IMPORTANT]
>
>De IP pool en kanaalconfiguraties die voor hoog-productie transactionele berichten worden aangewezen moeten uitsluitend voor dat doel worden gebruikt, en niet met standaard transactioneel overseinen worden gebruikt gebruikend API teweeggebrachte campagnes of reizen.
