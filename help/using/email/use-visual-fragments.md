---
solution: Journey Optimizer
product: journey optimizer
title: Visuele fragmenten gebruiken
description: Leer hoe u visuele fragmenten kunt gebruiken bij het maken van e-mails in Journey Optimizer-campagnes en -reizen
feature: Email Design, Fragments
topic: Content Management
role: User
level: Beginner
exl-id: 25a00f74-ed08-479c-9a5d-4185b5f3c684
source-git-commit: 7a8a0c133318b0bfc33b0fdb294e5b9ef53de9a5
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 1%

---

# Visuele fragmenten toevoegen aan uw e-mails {#use-visual-fragments}

Een fragment is een herbruikbare component waarnaar in een of meer e-mails kan worden verwezen via Journey Optimizer-campagnes, -reizen of inhoudssjablonen. Met deze functionaliteit kunt u meerdere blokken met aangepaste inhoud vooraf samenstellen. Deze blokken kunnen door marketinggebruikers worden gebruikt om snel e-mailinhoud samen te stellen in een verbeterd ontwerpproces. [ leer hoe te om fragmenten ](../content-management/fragments.md) tot stand te brengen en te beheren.

➡️ [ Leer hoe te, auteur en gebruiks fragmenten in deze video ](../content-management/fragments.md#video-fragments) beheren

## Een fragment gebruiken {#use-fragment}

Voer de onderstaande stappen uit om een fragment te gebruiken in een e-mailbericht.

>[!NOTE]
>
>U kunt maximaal 30 fragmenten in een bepaalde levering toevoegen. Fragmenten kunnen maximaal 1 niveau worden genest.


1. Open om het even welke e-mail of malplaatjeinhoud gebruikend [ E-mail Designer ](get-started-email-design.md).

1. Selecteer het pictogram **[!UICONTROL Fragments]** van de linkerspoorstaaf.

   ![](assets/fragments-in-designer.png)

1. De lijst met alle visuele fragmenten die in de huidige sandbox zijn gemaakt, wordt weergegeven. Deze worden gesorteerd op aanmaakdatum: recent toegevoegde visuele fragmenten worden als eerste weergegeven in de lijst. U kunt:

   * Zoek naar een specifiek fragment door zijn etiket te beginnen typen.
   * Sorteer fragmenten in oplopende of aflopende volgorde.
   * De manier wijzigen waarop de fragmenten worden weergegeven (kaarten of lijstweergave).
   * Vernieuw de lijst.

   >[!NOTE]
   >
   >Als sommige fragmenten zijn gewijzigd of toegevoegd terwijl u de inhoud bewerkt, wordt de lijst bijgewerkt met de meest recente wijzigingen.

1. Sleep een fragment uit de lijst naar het gebied waar u het wilt invoegen.

   ![](assets/fragment-insert.png)

   >[!CAUTION]
   >
   >U kunt om het even welk **Ontwerp** toevoegen of **Levend** fragment aan uw inhoud. U kunt uw reis of campagne echter niet activeren als er een fragment met de status Concept in wordt gebruikt. Tijdens de reis- of campagnepublicatie wordt een fout weergegeven in ontwerpfragmenten die u moet goedkeuren om te kunnen publiceren.

1. Net als bij andere componenten kunt u het fragment in de inhoud verplaatsen.

1. Selecteer het fragment om het corresponderende venster rechts weer te geven. Daarna kunt u het fragment uit de inhoud verwijderen of dupliceren. U kunt deze handelingen ook rechtstreeks uitvoeren vanuit het contextmenu dat boven op het fragment wordt weergegeven.

   ![](assets/fragment-right-pane.png)

1. Via het tabblad **[!UICONTROL Settings]** kunt u:

   * Kies de apparaten waarop het fragment moet worden weergegeven.
   * Open het fragment op een nieuw tabblad om het zo nodig te bewerken. [Meer informatie](../content-management/fragments.md#edit-fragments)
   * Verken verwijzingen. [Meer informatie](../content-management/fragments.md#explore-references)

1. U kunt het fragment verder aanpassen met het tabblad **[!UICONTROL Styles]** .

1. Indien nodig, kunt u de overerving met het oorspronkelijke fragment verbreken. [Meer informatie](#break-inheritance)

1. Voeg zoveel fragmenten toe als u wilt en **[!UICONTROL Save]** uw wijzigingen.

## Gebruik impliciete variabelen {#implicit-variables-in-fragments}

De impliciete variabelen verbeteren de bestaande fragmentfunctionaliteit om de efficiëntie voor hergebruik van inhoud en het gebruik van scripts te verbeteren. Fragmenten kunnen invoervariabelen gebruiken en uitvoervariabelen maken die bruikbaar zijn in campagne- en reisinhoud.

Leer hoe te om impliciete variabelen in [ te gebruiken deze sectie ](../personalization/use-expression-fragments.md#implicit-variables).

## Bewerkbare velden aanpassen {#customize-fields}

Als bepaalde delen van het geselecteerde fragment bewerkbaar zijn gemaakt, kunt u de standaardwaarde ervan overschrijven nadat u het fragment aan de inhoud hebt toegevoegd. [ Leer hoe te om uw fragmenten klantgericht te maken ](../content-management/customizable-fragments.md)

Voer de volgende stappen uit om bewerkbare velden in een fragment aan te passen:

1. Voeg het fragment toe aan uw inhoud.

1. Selecteer het om de eigenschappen ruit op de rechterkant te openen.

   Alle editable gebieden in het fragment worden getoond in het **lusje van Montages**, onder de **sectie van het Fragment**.

1. Wanneer u in het rechterdeelvenster een bewerkbaar veld selecteert, wordt dit in het centrale voorvertoningsvenster groen gemarkeerd, zodat u gemakkelijk de locatie van het veld in de inhoud kunt identificeren.

   In het voorbeeld hieronder, kan de beeld **bron** en **alt tekst** worden uitgegeven, evenals &quot;klik hier&quot;knoop **URL**.

   ![](assets/fragment-editable.png)

## Overerving onderbreken {#break-inheritance}

Wanneer u een visueel fragment bewerkt, worden de wijzigingen gesynchroniseerd. Ze worden automatisch doorgegeven aan alle concepten of live reizen/campagnes en inhoudssjablonen die dat fragment bevatten.

Wanneer fragmenten aan een e-mail- of inhoudssjabloon worden toegevoegd, worden ze standaard gesynchroniseerd. U kunt de overerving echter wel verbreken van het oorspronkelijke fragment. In dat geval wordt de inhoud van het fragment naar het huidige ontwerp gekopieerd en worden de wijzigingen niet meer gesynchroniseerd.

Volg onderstaande stappen om overerving te onderbreken:

1. Selecteer het fragment.

1. Klik op het ontgrendelingspictogram op de contextafhankelijke werkbalk.

   ![](assets/fragment-break-inheritance.png)

1. Dat fragment wordt een zelfstandig element dat niet meer aan het oorspronkelijke fragment is gekoppeld. Bewerk de inhoud als elke andere inhoudscomponent in de inhoud. [Meer informatie](content-components.md)
