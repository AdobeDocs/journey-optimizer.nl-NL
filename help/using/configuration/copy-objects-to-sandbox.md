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
exl-id: 356d56a5-9a90-4eba-9875-c7ba96967da9
source-git-commit: 0ad4c6a9024ea91d502ca2a733117f58c63ca50b
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 0%

---

# Objecten exporteren naar een andere sandbox {#copy-to-sandbox}

U kunt objecten zoals reizen, aangepaste handelingen, inhoudssjablonen of fragmenten over meerdere sandboxen kopiëren met behulp van de opties voor exporteren en importeren van pakketten. Een pakket kan uit één object of uit meerdere objecten bestaan. Alle objecten die in een pakket zijn opgenomen, moeten afkomstig zijn uit dezelfde sandbox.

Op deze pagina wordt het gebruik-hoofdlettergebruik voor Sandbox-gereedschappen in de context van Journey Optimizer beschreven. Voor meer informatie over de eigenschap zelf, verwijs naar de [ documentatie van Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html).

>[!NOTE]
>
>Deze eigenschap vereist de volgende toestemmingen van het **beleid Sandbox** vermogen: beheer zandbakken (of zandbakken van de Mening) en beheer pakketten. [Meer informatie](../administration/ootb-permissions.md)

Het kopieerproces wordt uitgevoerd via een pakketexport en importeren tussen de bron- en doelsandboxen. Hier volgen de algemene stappen voor het kopiëren van een reis van de ene naar de andere sandbox:

1. Voeg het object dat u wilt exporteren als een pakket toe aan de bronsandbox.
1. Exporteer het pakket naar de doelsandbox.

## Geëxporteerde objecten en aanbevolen werkwijzen {#objects}

Journey Optimizer staat het exporteren van reizen, aangepaste handelingen, inhoudssjablonen en fragmenten naar een andere sandbox toe. In de volgende secties vindt u informatie en tips en trucs voor elk type object.

### Algemene beste praktijken {#global}

* Wanneer u een object kopieert, worden afhankelijkheden (zoals geneste fragmenten, reisdoelgroepen of handelingen) correct bijgewerkt in het bovenliggende object, zodat de doelsandbox correct wordt toegewezen.

* Als een geëxporteerd object profielpersonalisatie bevat, controleert u of het juiste schema in de doelsandbox aanwezig is om problemen met de personalisatie te voorkomen.

### Journeys {#journeys}

* Bij het exporteren van een reis kopieert Journey Optimizer naast de reis zelf ook het grootste deel van de objecten waarvan de reis afhankelijk is: publiek, aangepaste acties, schema&#39;s, evenementen en acties. Voor meer details op gekopieerde voorwerpen, verwijs naar deze [ sectie ](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html#abobe-journey-optimizer-objects).

* We garanderen niet dat alle gekoppelde elementen naar de doelsandbox worden gekopieerd. Wij adviseren ten zeerste dat u een grondige controle uitvoert, bijvoorbeeld alvorens een reis te publiceren. Zo kunt u elk mogelijk ontbrekend object identificeren.

* De gekopieerde objecten in de doelsandbox zijn uniek en er bestaat geen risico dat bestaande elementen worden overschreven. Zowel de reis als alle berichten binnen de reis worden in de ontwerpmodus overgenomen. Hierdoor kunt u een grondige validatie uitvoeren voordat deze wordt gepubliceerd in de doelsandbox.

* Het kopieerproces kopieert alleen de metagegevens over de reis en de objecten in die reis. Er worden geen profiel- of gegevenssetgegevens gekopieerd als onderdeel van dit proces.

### Aangepaste acties {#custom-actions}

* Wanneer het uitvoeren van douaneacties, worden de configuratie URL en de parameters van de lading gekopieerd over. Om veiligheidsredenen worden de verificatieparameters echter niet gekopieerd en vervangen door &quot;GEHEIM INSERT HIER&quot;. De waarden van de de verzoekkopbal en van de vraagparam van de constante worden van het verzoek ook vervangen door &quot;INSERT SECRET HERE&quot;.

  Dit zijn onder andere de aangepaste handelingen voor speciale doeleinden ([!DNL Adobe Campaign Standard] , [!DNL Campaign Classic] , [!DNL Marketo Engage] ).

* Als u tijdens het importeren de optie &#39;Bestaande gebruiken&#39; selecteert voor een aangepaste handeling, moet de aangepaste actie die u selecteert, gelijk zijn aan de aangepaste bronactie (dus dezelfde configuratie, parameters, enzovoort) wanneer u een reis naar een andere sandbox kopieert. Anders bevat de nieuwe reiskopie fouten die niet op het canvas kunnen worden opgelost.

### Campagnes {#campaigns}

Campagnes worden samen met alle punten gekopieerd met betrekking tot het profiel, het publiek, het schema, de gealigneerde berichten, en afhankelijke voorwerpen. Nochtans, worden de volgende punten **niet** gekopieerd:

* Meertalige varianten en taalinstellingen
* Bedrijfsvoorschriften,
* Tags,
* Labels voor gegevensgebruik en etiketten voor handhaving (DULE).

Zorg er bij het kopiëren van campagnes voor dat het hieronder vermelde object in de doelsandbox wordt gevalideerd om verkeerde configuraties te voorkomen:

* **configuraties van het Kanaal**: De configuraties van het kanaal worden gekopieerd samen met campagnes. Nadat de campagnes worden gekopieerd, moeten de kanaalconfiguraties manueel in de doelzandbak worden geselecteerd.
* **de varianten en montages van de Experimentatie van de Experimentatie**: De experimentele varianten en de montages zijn inbegrepen in het proces van het campagneexemplaar. Valideer deze instellingen in de doelsandbox na het importeren.
* **Verenigde beslissing**: Het beleid van het besluit en de besluitvormingspunten worden gesteund voor de uitvoer en de invoer. Zorg ervoor dat aan beslissingen gerelateerde afhankelijkheden correct worden toegewezen in de doelsandbox.

### Contentsjablonen {#content-templates}

* Bij het exporteren van een inhoudssjabloon worden ook alle geneste fragmenten gekopieerd.

* Het exporteren van inhoudssjablonen kan soms leiden tot fragmentduplicatie. Als twee sjablonen bijvoorbeeld hetzelfde fragment delen en in afzonderlijke pakketten worden gekopieerd, moeten beide sjablonen hetzelfde fragment opnieuw gebruiken in de doelsandbox. Als u dubbel werk wilt voorkomen, selecteert u de optie &quot;Bestaande gebruiken&quot; tijdens het importproces. [ leer hoe te om een pakket ](#import) in te voeren

* Om dubbel werk verder te vermijden, wordt aanbevolen inhoudssjablonen in één pakket te exporteren. Dit zorgt ervoor dat het systeem deduplicatie efficiënt beheert.

### Beslissing {#decisioning}

* De objecten hieronder moeten aanwezig zijn in de doelsandbox voordat u beslissingsobjecten kopieert:

   * Profielkenmerken die worden gebruikt voor Decisioning-objecten
   * De veldgroep aangepaste aanbiedingskenmerken,
   * De schema&#39;s van gegevensstromen die voor de Attributen van de Context over Regels, het Rangschikken of het Kappen worden gebruikt.

* Sandbox-kopie voor rangschikkingsformules met AI-modellen wordt momenteel niet ondersteund.

* Wanneer het kopiëren van Beslissende entiteiten, zorg ervoor u besluitvormingspunten **vóór** om het even welk ander voorwerp kopieert. Als u bijvoorbeeld eerst een verzameling kopieert en de nieuwe sandbox geen aanbiedingen bevat, blijft die nieuwe verzameling leeg.

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

## Het te exporteren pakket publiceren {#publish}

Als uw pakket klaar is om te worden geëxporteerd, voert u de volgende stappen uit om het te publiceren:

1. Navigeer aan **[!UICONTROL Administration]** > **[!UICONTROL Sandboxes]** menu, selecteer de **Pakketten** tabel.

1. Open het pakket u wilt uitvoeren, de voorwerpen selecteren u wilt uitvoeren en **publiceren** klikken.

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
