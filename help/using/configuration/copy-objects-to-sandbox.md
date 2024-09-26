---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer-objecten kopiëren tussen sandboxen
description: Leer hoe u reizen, inhoudssjablonen en fragmenten tussen sandboxen kopieert.
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: zandbak, reis, exemplaar, milieu
source-git-commit: 62b5cfd480414c898ab6f123de8c6b9f99667b7d
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---


# Journey Optimizer-objecten kopiëren naar een andere sandbox {#copy-to-sandbox}

Met sandboxgereedschappen kunt u objecten zoals reizen, inhoudssjablonen of fragmenten over meerdere sandboxen heen kopiëren door het exporteren en importeren van pakketten te benutten. Een pakket kan uit één object of uit meerdere objecten bestaan. Alle objecten die in een pakket zijn opgenomen, moeten afkomstig zijn uit dezelfde sandbox.

Op deze pagina wordt het gebruik-hoofdlettergebruik voor Sandbox-gereedschappen in de context van Journey Optimizer beschreven. Voor meer informatie over de eigenschap zelf, verwijs naar de [ documentatie van het Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html).

>[!NOTE]
>
>Deze eigenschap vereist de volgende toestemmingen van het **beleid Sandbox** vermogen: beheer zandbakken (of zandbakken van de Mening) en beheer pakketten. [Meer informatie](../administration/ootb-permissions.md)

Het kopieerproces wordt uitgevoerd via een pakketexport en importeren tussen de bron- en doelsandboxen. Hier volgen de algemene stappen voor het kopiëren van een reis van de ene naar de andere sandbox:

1. Voeg het object dat u wilt exporteren als een pakket toe aan de bronsandbox.
1. Exporteer het pakket naar de doelsandbox.

Bovendien kunt u hefboomwerking Journey Optimizer **de REST API van de Dienst van het Exemplaar van Objecten** gebruiken om zandbakken&#39; voorwerpen te beheren. [ Leer hoe te om met de REST API van de Dienst van het Exemplaar van Objecten te werken ](https://developer.adobe.com/journey-optimizer-apis/references/sandbox/)

## Geëxporteerde objecten en aanbevolen werkwijzen {#objects}

Journey Optimizer staat het exporteren van reizen, inhoudssjablonen en fragmenten naar een andere sandbox toe. In de volgende secties vindt u informatie en tips en trucs voor elk type object.

### Algemene beste praktijken {#global}

* Wanneer u een object kopieert, worden afhankelijkheden (zoals geneste fragmenten, reisdoelgroepen of handelingen) correct bijgewerkt in het bovenliggende object, zodat de doelsandbox correct wordt toegewezen.

* Als een geëxporteerd object profielpersonalisatie bevat, controleert u of het juiste schema in de doelsandbox aanwezig is om problemen met de personalisatie te voorkomen.

### Journeys {#journeys}

* Bij het exporteren van een reis kopieert Journey Optimizer naast de reis zelf ook het grootste deel van de objecten waarvan de reis afhankelijk is: publiek, schema&#39;s, evenementen en acties. Voor meer details op gekopieerde voorwerpen, verwijs naar deze [ sectie ](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html#abobe-journey-optimizer-objects).

* We garanderen niet dat alle gekoppelde elementen naar de doelsandbox worden gekopieerd. Wij adviseren ten zeerste dat u een grondige controle uitvoert, bijvoorbeeld alvorens een reis te publiceren. Zo kunt u elk mogelijk ontbrekend object identificeren.

* De gekopieerde objecten in de doelsandbox zijn uniek en er bestaat geen risico dat bestaande elementen worden overschreven. Zowel de reis als alle berichten binnen de reis worden in de ontwerpmodus overgenomen. Hierdoor kunt u een grondige validatie uitvoeren voordat deze wordt gepubliceerd in de doelsandbox.

* Het kopieerproces kopieert alleen de metagegevens over de reis en de objecten in die reis. Er worden geen profiel- of gegevenssetgegevens gekopieerd als onderdeel van dit proces.

### Contentsjablonen {#content-templates}

* Bij het exporteren van een inhoudssjabloon worden ook alle geneste fragmenten gekopieerd.

* Het exporteren van inhoudssjablonen kan soms leiden tot fragmentduplicatie. Als twee sjablonen bijvoorbeeld hetzelfde fragment delen en in afzonderlijke pakketten worden gekopieerd, moeten beide sjablonen hetzelfde fragment opnieuw gebruiken in de doelsandbox. Als u dubbel werk wilt voorkomen, selecteert u de optie &quot;Bestaande gebruiken&quot; tijdens het importproces. [ leer hoe te om een pakket ](#import) in te voeren

* Om dubbel werk verder te vermijden, wordt aanbevolen inhoudssjablonen in één pakket te exporteren. Dit zorgt ervoor dat het systeem deduplicatie efficiënt beheert.

### Fragmenten {#fragments}

* Fragmenten kunnen met uitvoering meerdere statussen hebben, zoals Live, Concept en Live. Wanneer u een fragment exporteert, wordt de laatste conceptstatus ervan naar de doelsandbox gekopieerd.

* Bij het exporteren van een fragment worden ook alle geneste fragmenten gekopieerd.

## Objecten toevoegen als pakket{#export}

Als u objecten naar een andere sandbox wilt kopiëren, moet u ze eerst als een pakket in de bronsandbox toevoegen. Voer de volgende stappen uit:

1. Navigeer naar de inventaris waar het eerste object dat u wilt kopiëren, is opgeslagen, zoals de lijst met ritten. Klik het **Meer acties** pictogram (de drie punten naast de objecten naam) en klik **toevoegen aan pakket**.

   ![](assets/journey-sandbox1.png)

1. In **voeg aan pakket** venster toe, kies als u het voorwerp aan een bestaand pakket wilt toevoegen of een nieuw pakket creëren:

   ![](assets/journey-sandbox2.png)

   * **Bestaand pakket**: selecteer het pakket van het drop-down menu.
   * **creeer een nieuw pakket**: type de pakketnaam. U kunt ook een beschrijving toevoegen.

1. Herhaal deze stappen om alle objecten toe te voegen die u met het pakket wilt exporteren.

>[!NOTE]
>
>Voor reizen die worden uitgevoerd, kopieert Journey Optimizer naast de reis zelf ook het grootste deel van de objecten waarvan de reis afhankelijk is: publiek, schema&#39;s, evenementen en acties. Voor meer detailreizen die uitvoeren, verwijs naar [ deze sectie ](../building-journeys/copy-to-sandbox.md).

## Het te exporteren pakket Publish {#publish}

Als uw pakket klaar is om te worden geëxporteerd, voert u de volgende stappen uit om het te publiceren:

1. Navigeer aan **[!UICONTROL Administration]** > **[!UICONTROL Sandboxes]** menu, selecteer de **Pakketten** tabel.

1. Open het pakket u wilt uitvoeren, de voorwerpen selecteren u wilt uitvoeren en **Publish** klikken.

   In dit voorbeeld willen wij een reis, een inhoudsmalplaatje en een fragment uitvoeren.

   ![](assets/journey-sandbox4.png)

1. De status van de publicatie van het pakket volgen via het tabblad **[!UICONTROL Jobs]** . Selecteer een taak in de lijst en klik op de knop **[!UICONTROL View import details]** voor meer informatie over een taak.

   ![](assets/journey-sandbox9.png)

## Het pakket importeren in de doelsandbox {#import}

Nadat het pakket is gepubliceerd, moet u het importeren in de doelsandbox. Voer de volgende stappen uit:

1. Navigeer naar het menu **[!UICONTROL Sandboxes]** en selecteer de tab **[!UICONTROL Browse]** .

1. Zoek naar de zandbak waar u het pakket wilt invoeren, dan klik + pictogram naast zijn naam.

   ![](assets/journey-sandbox5.png)

   >[!NOTE]
   >
   >Alleen sandboxen binnen uw organisatie zijn beschikbaar.

1. Op het **zandbak van het Doel** gebied, controleer dat de correcte doelzandbakken wordt geselecteerd en selecteer het pakket om van de **[!UICONTROL Package name]** drop-down lijst in te voeren. Klik **daarna**.

   ![](assets/journey-sandbox6.png)

1. Controleer de pakketobjecten en afhankelijkheden. Dit is de lijst met objecten die aan het pakket zijn toegevoegd, samen met andere objectritten zijn afhankelijk van bijvoorbeeld soorten publiek, schema&#39;s, gebeurtenissen of handelingen.

   Voor elk object kunt u een nieuw object maken of een bestaand object in de doelsandbox gebruiken. Zo voorkomt u bijvoorbeeld fragmentduplicatie die kan optreden bij het importeren van inhoudssjablonen met behulp van algemene fragmenten.

   ![](assets/journey-sandbox7.png)

1. Klik de **Afwerking** knoop, in de hoger-juiste hoek beginnen het pakket aan de doelzandbak te kopiëren. Het kopiëren is afhankelijk van de complexiteit van de objecten en het aantal objecten dat moet worden gekopieerd.

1. Klik op de importtaak om het kopieerresultaat te bekijken:

   * Klik de **Geïmporteerde voorwerpen van de Mening** knoop om elk individueel gekopieerd voorwerp te tonen.
   * Klik de **de invoerdetails van de Mening** knoop om de invoerresultaten voor elk voorwerp te controleren.

   ![](assets/journey-sandbox8.png)

1. Open de doelsandbox en voer een grondige controle uit van alle gekopieerde objecten.
