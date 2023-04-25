---
title: Werken met evenementen voor Beslissingsbeheer
description: Leer hoe u Beslissingsbeheerrapporten maakt in Adobe Experience Platform.
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: a6a892ec20dfeb6879bef2f4c2eb4a0f8f54885f
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 48%

---

# Aan de slag met besluitvormingsgebeurtenissen {#monitor-offer-events}

Telkens wanneer het Beslissingsbeheer een besluit neemt voor een bepaald profiel, wordt informatie over deze gebeurtenissen automatisch naar Adobe Experience Platform verzonden.

Hierdoor kunt u meer inzicht krijgen in uw beslissingen, bijvoorbeeld om te weten welk aanbod aan een bepaald profiel is gepresenteerd. U kunt deze gegevens exporteren om ze te analyseren in uw eigen rapportagesysteem, of Adobe Experience Platform gebruiken [Query-service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=nl) in combinatie met andere instrumenten voor versterkte analyse en rapportage.

## Belangrijke informatie beschikbaar in gegevensreeksen {#key-information}

Elke gebeurtenis die wordt verzonden wanneer een besluit wordt genomen, bevat vier belangrijke gegevenspunten die u voor analyse en rapportagedoeleinden kunt gebruiken:

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: naam en ID van de alternatieve aanbieding als er geen persoonlijke aanbieding is geselecteerd;
* **[!UICONTROL Placement]**: naam, id en kanaal van de plaatsing die voor de aanbieding wordt gebruikt;
* **[!UICONTROL Selections]**: naam en id van de voor het profiel geselecteerde aanbieding;
* **[!UICONTROL Activity]**: Naam en ID van de beslissing.

Daarnaast kunt u ook de **[!UICONTROL identityMap]** en **[!UICONTROL Timestamp]**-velden gebruiken om informatie op te halen over het profiel en het tijdstip waarop de aanbieding is geleverd.

Raadpleeg voor meer informatie over alle XDM-velden die bij elke beslissing worden verzonden, [deze sectie](xdm-fields.md).

## Gegevensbestanden voor toegang {#access-datasets}

De datasets met gebeurtenissen in verband met het beheer van besluiten zijn toegankelijk vanuit Adobe Experience Platform **[!UICONTROL Datasets]** -menu. Eén dataset wordt automatisch gemaakt bij het invullen van elk van uw instanties.

![](../assets/events-datasets-list.png)

Deze gegevensbestanden zijn gebaseerd op de **[!UICONTROL ODE DecisionEvents]** schema, dat alle XDM gebieden bevat die worden vereist om informatie van Beslissingsbeheer naar Adobe Experience Platform te verzenden.

>[!NOTE]
>
>Merk op dat de datasets van ODE DecisionEvents **niet-profieldatasets** zijn, wat betekent dat ze niet in Experience Platform kunnen worden opgenomen voor gebruik door het realtimeklantprofiel.
