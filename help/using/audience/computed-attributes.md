---
solution: Journey Optimizer
product: journey optimizer
title: Werken met berekende kenmerken
description: Leer hoe u met berekende kenmerken werkt.
feature: Audiences, Profiles
role: User
level: Intermediate
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
source-git-commit: d87f33c80cc85b1d1a87150687f6d7c9a268a016
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Werken met berekende kenmerken {#computed-attributes}

Met berekende kenmerken worden afzonderlijke gedragsgebeurtenissen samengevat in berekende profielkenmerken die beschikbaar zijn op Adobe Experience Platform. Deze kenmerken zijn gebaseerd op de gegevenssets voor gebeurtenissen die zijn opgenomen in Adobe Experience Platform en fungeren als geaggregeerde gegevenspunten die zijn opgeslagen in klantprofielen.

Elk verwerkt kenmerk is een profielkenmerk dat u kunt gebruiken voor segmentatie, personalisatie en activering tijdens reizen en campagnes. Deze vereenvoudiging verbetert de mogelijkheid om uw klanten actuele en zinvolle persoonlijke ervaringen te bieden.


![](../rn/assets/do-not-localize/computed-attributes.gif)


>[!NOTE]
>
>Om tot gegevens verwerkte attributen toegang te hebben, verzeker u de aangewezen toestemmingen (**Mening Geschikt attributen** en **beheert Gedetailleerde attributen**).

## Berekende kenmerken maken {#manage}

Als u berekende kenmerken wilt maken, bladert u naar het tabblad **[!UICONTROL Computed attributes]** in het menu **[!UICONTROL Profiles]** links.

Vanuit dit scherm kunt u berekende kenmerken samenstellen door regels te maken die gebeurteniskenmerken, statistische functies en een opgegeven terugzoekperiode combineren. U kunt bijvoorbeeld de som van de aankopen berekenen die in de laatste drie maanden zijn gedaan, het meest recente object identificeren dat wordt weergegeven door een profiel dat de afgelopen week geen aankoop heeft gedaan, of de totale bonuspunten optellen die elk profiel heeft geaccumuleerd.

![](assets/computed-attributes.png)

Zodra uw regel klaar is, publiceer het gegevens verwerkte attribuut om het in andere stroomafwaartse diensten, met inbegrip van Journey Optimizer ter beschikking te stellen.

De gedetailleerde informatie bij het creëren van en het beheren van gegevens verwerkte attributen is beschikbaar in de [&#x200B; Berekende attributendocumentatie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html)

## Berekende kenmerken toevoegen aan de Adobe Experience Platform-gegevensbron {#source}

Aan hefboomwerking gegevens verwerkte attributen in Journey Optimizer, voeg hen aan de Journey Optimizer **Experience Platform** gegevensbron toe.

De Adobe Experience Platform-gegevensbron definieert de verbinding met het Adobe Real-Time Klantprofiel. Deze gegevensbron wint de gegevens van het Profiel en van de Ervaring van Gebeurtenissen van de Dienst van het Profiel van de Klant in real time terug.

Ga als volgt te werk om berekende kenmerken aan de gegevensbron toe te voegen:

1. Blader naar het linkermenu van **[!UICONTROL Configurations]** en klik op de kaart van **[!UICONTROL Data sources]** .

1. Selecteer de gegevensbron **[!UICONTROL Experience Platform]** .

   ![](assets/computed-attributes-add.png)

1. Voeg de **[!UICONTROL SystemComputedAttributes]** -veldgroep toe die alle gemaakte berekende kenmerken bevat.

   ![](assets/computed-attributes-fieldgroup.png)

De berekende kenmerken zijn nu beschikbaar voor gebruik in Journey Optimizer. [&#x200B; Leer hoe te om gegevens verwerkte attributen in Journey Optimizer te gebruiken &#x200B;](#use)

De gedetailleerde informatie bij het toevoegen van gebiedsgroepen aan de gegevensbron van Adobe Experience Platform is beschikbaar in [&#x200B; deze sectie &#x200B;](../datasource/adobe-experience-platform-data-source.md).

## Berekende kenmerken gebruiken in Journey Optimizer {#use}

>[!NOTE]
>
>Voordat u begint, moet u controleren of u uw berekende kenmerken aan de Adobe Experience Platform-gegevensbron hebt toegevoegd. [&#x200B; leer hoe in deze sectie &#x200B;](#source).

Computerkenmerken bieden veelzijdige mogelijkheden binnen Journey Optimizer. Gebruik deze voor verschillende doeleinden, zoals het personaliseren van de inhoud van berichten, het maken van nieuwe soorten publiek of het splitsen van reizen op basis van een specifiek berekend kenmerk. U kunt bijvoorbeeld het pad van een rit splitsen op basis van de totale aankopen van een profiel in de laatste drie weken door één berekend kenmerk toe te voegen aan een Condition-activiteit. U kunt een e-mailbericht ook personaliseren door het laatst bekeken item voor elk profiel weer te geven.

Aangezien de gegevens verwerkte attributen profielkenmerkgebieden zijn die op uw schema van de profielunie worden gecreeerd, toegang tot hen van de verpersoonlijkingsredacteur binnen de **gebiedsgroep 0&rbrace; SystemComputedAttributes &lbrace;.** Daarna voegt u berekende kenmerken toe aan uw expressies. Deze worden op dezelfde manier behandeld als andere profielkenmerken om de gewenste bewerkingen uit te voeren.

![](assets/computed-attributes-ajo.png)
