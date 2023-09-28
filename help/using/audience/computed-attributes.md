---
solution: Journey Optimizer
product: journey optimizer
title: Werken met berekende kenmerken
description: Leer hoe u met berekende kenmerken werkt.
feature: Profiles
role: User
level: Beginner
source-git-commit: d2619b3b3871073b35faf04adba71dbb1ddd29a1
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---


# Werken met berekende kenmerken {#computed-attributes}

Met berekende kenmerken kunt u afzonderlijke gedragsgebeurtenissen samenvatten in berekende profielkenmerken die beschikbaar zijn op Adobe Experience Platform. Deze berekende kenmerken zijn gebaseerd op de gegevenssets van de Experience Event die zijn opgenomen in Adobe Experience Platform en fungeren als geaggregeerde gegevenspunten die zijn opgeslagen in de profielen van de klant.

Elk verwerkt kenmerk is een profielkenmerk dat u kunt gebruiken voor segmentatie, personalisatie en activering tijdens reizen en campagnes. Deze vereenvoudiging verbetert de mogelijkheid om uw klanten actuele en zinvolle persoonlijke ervaringen te bieden.

>[!NOTE]
>
>Als u toegang wilt krijgen tot berekende kenmerken, moet u beschikken over de juiste machtigingen (**Berekende kenmerken weergeven** en **Berekende kenmerken beheren**).

## Berekende kenmerken maken {#manage}

Als u berekende kenmerken wilt maken, navigeert u naar de **[!UICONTROL Computed attributes]** in de **[!UICONTROL Profiles]** aan de linkerzijde.

Van dit scherm, kunt u gegevens verwerkte attributen construeren door regels te bouwen die gebeurtenisattributen, samengevoegde functies, naast een gespecificeerde raadplegingsperiode combineren. U kunt bijvoorbeeld de som van de aankopen berekenen die in de laatste drie maanden zijn gedaan, het meest recente object identificeren dat wordt weergegeven door een profiel met wie in de afgelopen week geen aankoop is gedaan, of de totale bonuspunten optellen die elk profiel heeft geaccumuleerd.

![](assets/computed-attributes.png)

Zodra uw regel klaar is, publiceer het gegevens verwerkte attribuut om het in andere stroomafwaartse diensten, met inbegrip van Journey Optimizer ter beschikking te stellen.

Gedetailleerde informatie over het maken en beheren van berekende kenmerken vindt u in de [Documentatie over berekende kenmerken](https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html)

## Berekende kenmerken toevoegen aan de Adobe Experience Platform-gegevensbron {#source}

Als u de berekende kenmerken in Journey Optimizer wilt gebruiken, moet u deze eerst toevoegen aan Journey Optimizer **Experience Platform** gegevensbron.

De gegevensbron van Adobe Experience Platform bepaalt de verbinding aan Adobe Real-time het Profiel van de Klant. Deze gegevensbron is ontworpen om profielgegevens op te halen en de gegevens van de Ervaring van Gebeurtenissen van de Dienst van het Profiel van de Klant in real time.

Ga als volgt te werk om berekende kenmerken aan de gegevensbron toe te voegen:

1. Ga naar de **[!UICONTROL Configurations]** klik op het linkerzijmenu en vervolgens op het **[!UICONTROL Data sources]** kaart.

1. Selecteer de **[!UICONTROL Experience Platform]** gegevensbron.

   ![](assets/computed-attributes-add.png)

1. Voeg de **[!UICONTROL SystemComputedAttributes]** veldgroep met alle gemaakte berekende kenmerken.

   ![](assets/computed-attributes-fieldgroup.png)

De berekende kenmerken zijn nu beschikbaar voor gebruik in Journey Optimizer. [Meer informatie over het gebruik van berekende kenmerken in Journey Optimizer](#use)

Gedetailleerde informatie over het toevoegen van veldgroepen aan de Adobe Experience Platform-gegevensbron is beschikbaar in [deze sectie](../datasource/adobe-experience-platform-data-source.md).

## Berekende kenmerken gebruiken in Journey Optimizer {#use}

>[!NOTE]
>
>Voordat u begint, moet u controleren of u de berekende kenmerken hebt toegevoegd aan de Adobe Experience Platform-gegevensbron. [Meer informatie in deze sectie](#source).

Berekende kenmerken bieden een veelzijdige set mogelijkheden binnen de functie Reisoptimalisatie. U kunt ze voor verschillende doeleinden gebruiken, zoals het personaliseren van berichtinhoud, het maken van nieuwe soorten publiek of het splitsen van reizen op basis van een specifiek berekend kenmerk. U kunt bijvoorbeeld het pad van een rit splitsen op basis van de totale aankopen van een profiel in de laatste drie weken door één berekend kenmerk toe te voegen aan een Condition-activiteit. U kunt een e-mailbericht ook personaliseren door het laatst bekeken item voor elk profiel weer te geven.

Aangezien berekende kenmerken profielkenmerkvelden zijn die in het schema van de profielunie zijn gemaakt, kunt u ze openen via de Expressieeditor in het dialoogvenster **SystemComputedAttributes** veldgroep. Daarna kunt u het berekende kenmerk aan uw expressies toevoegen en deze als elk ander profielkenmerk behandelen om de gewenste bewerkingen uit te voeren.

![](assets/computed-attributes-ajo.png)
