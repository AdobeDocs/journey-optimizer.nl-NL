---
solution: Journey Optimizer
product: journey optimizer
title: Definieer de door de API geactiveerde campagneeigenschappen
description: Leer hoe u de door de API geactiveerde campagne-eigenschappen definieert.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagnes, API-geactiveerd, REST, optimizer, berichten
exl-id: bda7e337-a246-4f01-b935-4a234d4c4baa
source-git-commit: d93b7ce225294257f49caee6ac08cfb575611a93
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Definieer de door de API geactiveerde campagneeigenschappen {#api-properties}

Ga als volgt te werk om een nieuwe API-actiecampagne te maken:

1. Blader naar het menu **[!UICONTROL Campaigns]** en selecteer de tab **[!UICONTROL API triggered]** .

1. Klik op de knop **[!UICONTROL Create campaign]** en selecteer het type campagne:

   * **[!UICONTROL API triggered - Marketing]** - Selecteer dit type API&#39;s die worden geactiveerd om gepersonaliseerde marketingberichten naar bepaalde doelgroepen te sturen.

   * **[!UICONTROL API triggered - Transactional]** - Transactiecampagnes zijn gericht op het verzenden van transactieberichten, d.w.z. berichten die worden verzonden na een actie uitgevoerd door een individu: verzoek om het opnieuw instellen van het wachtwoord, aankoop van winkelwagentje, enz.

     +++Modus Hoge doorvoer

     Voor transactie-API-getriggerde campagnes kunt u de modus **[!UICONTROL High Throughput]** inschakelen. Deze wijze wordt ontworpen voor grootschalig, in real time overseinen (tot 5000 transacties per seconde) en verstrekt hogere beschikbaarheid met lagere latentie. [ leer hoe te met de wijze van de Output van de Hoogtepunt werken ](../campaigns/api-triggered-high-throughput.md)

     >[!AVAILABILITY]
     >
     >De modus Hoge doorvoer is momenteel alleen beschikbaar voor het e-mailkanaal en in de regio VS.
     >
     >Dit vermogen is slechts beschikbaar voor organisaties die de het overseinen **toe:voegen-aan aanbieding van het overseinen van de de productietransactie van Adobe** hebben gekocht. Neem contact op met uw Adobe-vertegenwoordiger voor meer informatie.

     +++

   ![](assets/api-triggered-modal.png)

1. Voer op het tabblad **[!UICONTROL Properties]** een naam en beschrijving in voor uw campagne.

   ![](assets/create-campaign-properties.png)

1. Gebruik het **gebied van Markeringen** om Adobe Experience Platform Verenigde Markeringen aan uw campagne toe te wijzen. Op deze manier kunt u ze gemakkelijk classificeren en de zoekopdracht in de lijst met campagnes verbeteren. [ Leer hoe te met markeringen ](../start/search-filter-categorize.md#tags) te werken.

1. U kunt de toegang tot deze campagne beperken op toegangslabels wordt gebaseerd die. Blader naar de knop **[!UICONTROL Manage access]** boven aan deze pagina om een toegangsbeperking toe te voegen. Zorg ervoor dat u alleen labels selecteert waarvoor u gemachtigd bent. [ Leer meer over het Toegangsbeheer van het Niveau van Objecten ](../administration/object-based-access.md).

## Volgende stappen {#next}

Zodra uw campagneconfiguratie en inhoud klaar zijn, kunt u zijn actie vormen. [Meer informatie](api-triggered-campaign-action.md)
