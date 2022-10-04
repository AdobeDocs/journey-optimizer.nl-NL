---
title: Werken met het compositicanvas
description: Leer hoe u met het compositicanvas werkt
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: f439e4387139b3136c46d25ecb43f304e29b0f17
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---

# Werken met het compositicanvas {#composition-canvas}

Het compositicanvas is een visueel canvas waarmee u composities kunt maken door publiek en activiteiten te benutten (splitsen, uitsluiten...).

De stappen om een samenstelling in het samenstellingscanvas te vormen zijn als volgt:

1. [Uw beginpubliek(en) definiëren](#starting-audience)
1. [Voeg een of meerdere activiteiten toe](#action-activities)
1. [De resultaten opslaan in een nieuw publiek](#save)

## Selecteer het beginpubliek {#starting-audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="Typen samenvoegen"
>abstract="Geef op hoe de profielen van het geselecteerde publiek moeten worden samengevoegd."

De eerste stap om een samenstelling tot stand te brengen moet één of veelvoudige bestaande publiek als basis van uw samenstelling selecteren.

Selecteer **[!UICONTROL Audience]** activiteit en klik vervolgens op **[!UICONTROL Add audience]** Selecteer vervolgens een of meer soorten publiek.

In dit voorbeeld willen we ons richten op alle profielen die tot het goud- en zilverpubliek behoren.

![](assets/audiences-starting-audience.png)

Als u meerdere soorten publiek selecteert, geeft u op hoe de profielen van deze soorten publiek moeten worden samengevoegd:

* **[!UICONTROL Union]**: alle profielen van het geselecteerde publiek omvatten,
* **[!UICONTROL Intersection]**: profielen opnemen die alle geselecteerde doelgroepen gemeen hebben;
* **[!UICONTROL Exclude overlap]**: bevatten profielen die alleen bij een van de doelgroepen horen. Profielen die bij meer dan één publiek horen, worden niet opgenomen.

## Activiteiten toevoegen {#action-activities}

Voeg activiteiten toe nadat u het beginpubliek hebt geselecteerd om de selectie te verfijnen.

Om dit te doen, klik + knoop op de samenstellingsweg dan selecteren de gewenste activiteit. De juiste ruit opent, toestaand u om de activiteit te vormen.

![](assets/audiences-select-activity.png)

>[!NOTE]
>
>U kunt maximaal **[!UICONTROL Audience]** en **[!UICONTROL Exclude]** activiteiten die nodig zijn in uw compositie. Er kan echter geen aanvullende activiteit worden toegevoegd na **[!UICONTROL Rank]** en **[!UICONTROL Split]** activiteiten.

U kunt een activiteit uit het canvas op elk ogenblik verwijderen door de schrappingsknoop in de juiste ruit te klikken. Alle activiteiten die na deze activiteit worden toegevoegd, worden ook van het canvas verwijderd.

Beschikbare activiteiten zijn:

* [Publiek](#audience): aanvullende profielen opnemen die tot een of meer bestaande doelgroepen behoren;
* [Uitsluiten](#exclude): profielen uitsluiten die tot een bestaand publiek behoren of profielen uitsluiten die op specifieke kenmerken zijn gebaseerd;
* [Rang](#rank): rangschikt profielen die op een specifiek attribuut worden gebaseerd, specificeer het aantal profielen om te houden en hen in uw samenstelling te omvatten;
* [Splitsen](#split): verdeel uw samenstelling in veelvoudige wegen die op willekeurige percentages of op attributen worden gebaseerd.

### Poortactiviteit {#audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="Poortactiviteit"
>abstract="Met de activiteit van het publiek kunt u in uw compositie aanvullende profielen opnemen die tot een bestaand publiek behoren."

De **[!UICONTROL Audience]** Met activiteiten kunt u in uw compositie aanvullende profielen opnemen die tot een bestaand publiek behoren.

De configuratie van deze activiteit is identiek aan het begin [Poortactiviteit](#starting-audience).

### Exclusief activiteit {#exclude}

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="Type uitsluiten"
>abstract="Met het publiekstype Niet opnemen kunt u profielen uitsluiten die tot een bestaand publiek behoren. Met de optie Uitsluiten met behulp van het kenmerktype kunt u profielen uitsluiten op basis van een specifiek kenmerk."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="Exclusief activiteit"
>abstract="Met de activiteit Uitsluiten kunt u profielen uitsluiten van uw compositie door een bestaand publiek te selecteren of een regel te gebruiken."

De **[!UICONTROL Exclude]** Met activiteit kunt u profielen uitsluiten van uw compositie. Er zijn twee soorten uitsluitingen beschikbaar:

* **[!UICONTROL Exclude Audience]**: Profielen uitsluiten die bij een bestaand publiek horen.

   Klik op de knop **[!UICONTROL Add audience]** selecteert u vervolgens het publiek dat u wilt uitsluiten.

   ![](assets/audiences-exclude-audience.png)

* **[!UICONTROL Exclude using attribute]**: Profielen uitsluiten die zijn gebaseerd op een specifiek kenmerk.

   Selecteer het kenmerk dat u wilt opzoeken en geef de waarde op die u wilt uitsluiten. In dit voorbeeld sluiten we compositieprofielen uit waarvan het adres in Japan ligt.

   ![](assets/audiences-exclude-attribute.png)

### Leesactiviteit {#rank}

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="Beoordelingsactiviteit"
>abstract="De activiteit van de Rang staat u toe om profielen te rangschikken die op een specifiek attribuut worden gebaseerd en hen te omvatten in uw samenstelling. Neem bijvoorbeeld de 50 profielen op met de grootste hoeveelheid loyaliteitspunten."

De **[!UICONTROL Rank]** De activiteit staat u toe om profielen te rangschikken die op een specifiek attribuut worden gebaseerd en hen te omvatten in uw samenstelling. U kunt bijvoorbeeld de 50 profielen met de grootste hoeveelheid loyaliteitspunten opnemen.

1. Selecteer het kenmerk dat u wilt opzoeken en geef een rangschikking op (oplopend of aflopend).

   >[OPMERKING]
   >
   >U kunt kenmerken selecteren met de volgende gegevenstypen: integer, numbers, short <!--(other?)-->

1. Schakelen tussen **[!UICONTROL Add profile limit]** en geeft u een maximumaantal profielen op dat u in de compositie wilt opnemen.

   ![](assets/audiences-rank.png)

### Gesplitste activiteit {#split}

>[!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Controlegroep"
>abstract="Gebruik controlegroepen om een gedeelte van de profielen te isoleren. Hierdoor kunt u de impact van een marketingactiviteit meten en een vergelijking maken met het gedrag van de rest van de bevolking."

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="Gesplitste activiteit"
>abstract="Met de activiteit Splitsen kunt u de compositie opsplitsen in meerdere paden. Wanneer u de compositie publiceert, wordt voor elk pad één publiek opgeslagen in Adobe Experience Platform."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="Tekst splitsen"
>abstract="Met het gesplitste percentage kunt u profielen op willekeurige wijze splitsen in meerdere paden. Met het splitsingstype Kenmerk kunt u profielen splitsen op basis van een specifiek kenmerk."

De **[!UICONTROL Split]** Met activiteit kunt u de compositie opsplitsen in meerdere paden.

Deze bewerking voegt automatisch een **[!UICONTROL Save]** activiteit aan het einde van elk pad. Wanneer u de compositie publiceert, wordt voor elk pad één publiek opgeslagen in Adobe Experience Platform.

Er zijn twee soorten splitsingsbewerkingen beschikbaar:

* **[!UICONTROL Percent split]**: willekeurig gesplitste profielen in twee of meer paden. U kunt de profielen bijvoorbeeld opsplitsen in twee afzonderlijke paden van elk 45% en een extra pad toevoegen voor een controlegroep.

   ![](assets/audiences-split-percentage.png)

* **[!UICONTROL Attribute split]**: gesplitste profielen op basis van een specifiek kenmerk. In dit voorbeeld splitsen we profielen op basis van voorkeuren voor kamertype.

   ![](assets/audiences-split.png)

   >[!NOTE]
   >
   >De **[!UICONTROL Other profiles]** kunt u een extra pad maken met de resterende profielen die niet overeenkomen met een van de voorwaarden die in de andere paden zijn opgegeven.

## Uw publiek opslaan {#save}

Configureer het resulterende publiek dat in Adobe Experience Platform wordt opgeslagen.

Selecteer hiervoor de optie **[!UICONTROL Save audience]** aan het einde van elk pad geeft u vervolgens de naam op van het nieuwe publiek dat u wilt maken.

![](assets/audiences-publish.png)

Zodra uw samenstelling klaar is, kunt u het publiceren. [Leer hoe u composities maakt](create-compositions.md)

Meer informatie:

* [Aan de slag met publiekscompositie](get-started-audience-orchestration.md)
* [Samenstellingswerkstromen maken](create-compositions.md)
* [Toegang tot en beheer van het publiek](access-audiences.md)
