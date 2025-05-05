---
title: Beleid voor beslissingen maken
description: Leer hoe u beleidsbeslissingen maakt
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '1729'
ht-degree: 0%

---

# Beslissingsbeleid maken {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="Wat is een beslissing?"
>abstract="Het beslissingsbeleid bevat alle selectielogica waarmee de beslissingsengine de beste inhoud kan kiezen. Het besluitvormingsbeleid is specifiek voor de campagne. Hun doel is de beste aanbiedingen voor elk profiel te selecteren terwijl het campagneontwerp u toestaat om erop te wijzen hoe de geselecteerde besluitvormingspunten zouden moeten worden voorgesteld, met inbegrip van welke puntattributen om in het bericht worden omvat."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Informatie over beslissen"

Beslissingsbeleid zijn containers voor uw aanbiedingen die de beslissingsengine gebruiken om de beste inhoud te kiezen die u kunt leveren, afhankelijk van het publiek.

<!--Decision policies contain all of the selection logic for the decisioning engine to pick the best content. Decision policies are campaign specific. -->Hun doel is de beste aanbiedingen voor elk profiel te selecteren, terwijl het campagne/reis auteursrecht u toestaat om te wijzen op hoe de geselecteerde besluitvormingspunten, met inbegrip van welke puntattributen in het bericht moeten worden omvat.

>[!NOTE]
>
>In het [!DNL Journey Optimizer] gebruikersinterface, wordt het besluitvormingsbeleid geëtiketteerd als besluiten <!--but they are decision policies. TBC if this note is needed-->.

De belangrijkste stappen om besluitvormingsbeleid in uw op code-gebaseerde campagnes te gebruiken zijn als volgt:

1. [Voeg een besluitvormingsbeleid aan een op code-gebaseerde ervaring toe](#add-decision)
1. [Het beslissingsbeleid gebruiken](#use-decision-policy)
1. [Aangepaste Customer Journey Analytics-rapporteringsdashboards maken](cja-reporting.md)

## Voeg een besluitvormingsbeleid aan een op code-gebaseerde ervaring toe {#add-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="Het aantal items definiëren dat moet worden geretourneerd"
>abstract="Selecteer het aantal beslissingsitems dat u wilt retourneren. Als u bijvoorbeeld 2 selecteert, worden de beste twee in aanmerking komende aanbiedingen voor de huidige configuratie weergegeven."

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="Een fallback selecteren"
>abstract="Een reservepunt toont aan de gebruiker wanneer geen van de selectiestrategieën die voor dat besluitvormingsbeleid worden bepaald worden gekwalificeerd."

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="Wat is een strategie?"
>abstract="De volgorde van de selectiestrategie bepaalt welke strategie eerst wordt geëvalueerd. Er is ten minste één strategie nodig. Beslissingsonderdelen in gecombineerde strategieën worden samen geëvalueerd."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Strategieën maken"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Evaluatievolgorde"

Als u uw bezoekers de beste dynamische aanbieding en ervaring wilt laten zien op uw website of mobiele app, voegt u een beslissingsbeleid toe aan een op code gebaseerde campagne of reis. Volg de onderstaande stappen om dit te doen.

### Het beslissingsbeleid maken {#add}

1. Maak een campagne en selecteer de handeling **[!UICONTROL Code-base experience]** . [Meer informatie](../code-based/create-code-based.md)

1. Van de [ coderedacteur ](../code-based/create-code-based.md#edit-code), selecteer **[!UICONTROL Decision policy]** en klik **[!UICONTROL Add decision policy]**.

   ![](assets/decision-code-based-create.png)

1. Maak standaard een nieuw beleid.

   >[!NOTE]
   >
   >U kunt ook een bestaand beleid selecteren.

1. Vul de details voor uw besluitvormingsbeleid in: voeg een naam toe en selecteer een catalogus.

   >[!NOTE]
   >
   >Momenteel is alleen de standaardcatalogus **[!UICONTROL Offers]** beschikbaar.

1. Selecteer het aantal objecten dat je wilt retourneren. Als u bijvoorbeeld 2 selecteert, worden de beste twee in aanmerking komende aanbiedingen voor de huidige configuratie weergegeven. Klik op **[!UICONTROL Next]**.

   ![](assets/decision-code-based-details.png)

### Items selecteren en selectiestrategieën {#select}

In de sectie **[!UICONTROL Strategy sequence]** kunt u de beslissingsitems en de selectiestrategieën selecteren die u met het beslissingsbeleid wilt presenteren.

1. Klik op de knop **[!UICONTROL Add]**.

1. Kies het type object dat u in het beleid wilt opnemen:

   * **[!UICONTROL Selection strategy]**: voeg een of meerdere selectiestrategieën toe. Beslissingsstrategieën maken gebruik van collecties die verband houden met toelatingsbeperkingen en rangordemethoden om te bepalen welke items moeten worden getoond. U kunt een bestaande selectiestrategie selecteren of een nieuwe selectiestrategie maken met de knop **[!UICONTROL Create selection strategy]** . [ Leer hoe te om selectiestrategieën ](selection-strategies.md) tot stand te brengen

   * **[!UICONTROL Decision item]**: voeg enkele beslissingsitems toe die u wilt presenteren zonder dat u een selectiestrategie hoeft te doorlopen. U kunt slechts één beslissingsitem tegelijk selecteren. Alle voorwaarden die voor het onderdeel zijn ingesteld, zijn van toepassing.

   ![](assets/decision-code-based-strategy-sequence.png)

   >[!NOTE]
   >
   >Een beslissingsbeleid ondersteunt maximaal 10 selectiestrategieën en besluitvormingselementen samen. [ leer meer over het Beslissen van gidsen &amp; beperkingen ](gs-experience-decisioning.md#guardrails)

1. Wanneer het toevoegen van verscheidene besluitvormingspunten en/of strategieën, zullen zij in een specifieke orde worden geëvalueerd. Het eerste object dat aan de reeks is toegevoegd, wordt eerst geëvalueerd, enzovoort.

   Als u de standaardvolgorde wilt wijzigen, kunt u de objecten en/of groepen slepen en neerzetten om ze naar wens opnieuw te rangschikken. [Meer informatie](#evaluation-order)

### De evaluatievolgorde in een beslissingsbeleid beheren {#evaluation-order}

Nadat u besluitvormingspunten en selectiestrategieën aan uw beleid hebt toegevoegd, kunt u hun volgorde rangschikken om hun evaluatievolgorde te bepalen en kunt u selectiestrategieën combineren om deze samen te evalueren.

De **opeenvolgende orde** waarin de punten en de strategieën zullen worden geëvalueerd wordt vermeld met aantallen links van elk voorwerp of groep voorwerpen. Als u de positie van een selectiestrategie (of een groep strategieën) binnen de reeks wilt verplaatsen, sleept u deze naar een andere positie.

>[!NOTE]
>
>Alleen selectiestrategieën kunnen binnen een reeks worden gesleept en neergezet. Als u de positie van een beslissingsitem wilt wijzigen, moet u het item verwijderen en opnieuw toevoegen met de knop **[!UICONTROL Add]** nadat u de andere items hebt toegevoegd die u eerder wilt evalueren.

![](assets/decision-code-based-strategy-groups.png)

U kunt **&#x200B;**&#x200B;veelvoudige selectiestrategieën in groepen ook combineren zodat worden zij samen en niet afzonderlijk geëvalueerd. Klik hiertoe op de knop **`+`** onder een selectiestrategie om deze te combineren met een andere. U kunt een selectiestrategie ook naar een andere slepen om de twee strategieën in een groep te groeperen.

>[!NOTE]
>
>Beslissingsonderdelen kunnen niet worden gegroepeerd met andere onderdelen of selectiestrategieën.

Meerdere strategieën en de groepering daarvan bepalen de prioriteit van de strategieën en de rangorde van de in aanmerking komende aanbiedingen. De eerste strategie heeft de hoogste prioriteit en de strategieën in dezelfde groep hebben dezelfde prioriteit.

U hebt bijvoorbeeld twee verzamelingen, één in strategie A en één in strategie B. Het verzoek is om terugzending van twee besluitvormingselementen. Laten we zeggen dat er twee in aanmerking komende aanbiedingen zijn van strategie A en drie in aanmerking komende aanbiedingen van strategie B.

* Als de twee strategie **niet wordt gecombineerd** of in opeenvolgende orde (1 en 2), zullen de hoogste twee in aanmerking komende aanbiedingen van de eerste strategie in de eerste rij zijn teruggekeerd. Als er niet twee in aanmerking komende aanbiedingen voor de eerste strategie zijn, zal de beslissingsmotor op één na de volgende strategie volgen om te vinden hoeveel aanbiedingen nog nodig zijn, en zal uiteindelijk een terugslag teruggeven indien nodig.

  ![](assets/decision-code-based-consecutive-strategies.png)

* Als de twee inzamelingen **tezelfdertijd** worden geëvalueerd, aangezien er twee in aanmerking komende aanbiedingen van strategie A en drie in aanmerking komende aanbiedingen van strategie B zijn, zullen de vijf aanbiedingen allen worden stapel samen gebaseerd op de waarde die door de respectieve rangschikkingsmethodes wordt bepaald. Er wordt om twee aanbiedingen verzocht, zodat de twee belangrijkste in aanmerking komende aanbiedingen van deze vijf aanbiedingen worden teruggegeven.

  ![](assets/decision-code-based-combined-strategies.png)

+++ **Voorbeeld met veelvoudige strategieën**

Laten we nu een voorbeeld bekijken waarbij meerdere strategieën verdeeld zijn in verschillende groepen.

U hebt drie strategieën gedefinieerd. Strategie 1 en Strategie 2 zijn in groep 1 samengevoegd en strategie 3 is onafhankelijk (groep 2).

De in aanmerking komende aanbiedingen voor elke strategie en hun prioriteit (gebruikt bij de beoordeling van de rangorde) zijn als volgt:

* Groep 1:
   * Strategie 1 - (Aanbieding 1, Aanbieding 2, Aanbieding 3) - Prioriteit 1
   * Strategie 2 - (Aanbieding 3, Aanbieding 4, Aanbieding 5) - Prioriteit 1

* Groep 2:
   * Strategie 3 - (aanbod 5, aanbod 6) - Prioriteit 0

De belangrijkste prioritaire strategische aanbiedingen worden eerst geëvalueerd en aan de gerangschikte biedingenlijst toegevoegd.

**Herhaling 1:**

Aanbiedingen voor strategie 1 en strategie 2 worden samen geëvalueerd (Aanbieding 1, Aanbieding 2, Aanbieding 3, Aanbieding 4, Aanbieding 5). Laten we zeggen dat het resultaat:

Aanbieding 1 - 10
Voorstel 2 - 20
Aanbieding 3 - 30 van strategie 1, 45 van strategie 2. Het hoogste van beide wordt in overweging genomen, dus er wordt rekening gehouden met 45.
Voorstel 4 - 40
Voorstel 5 - 50

De gerangschikte voorstellen zijn nu als volgt: Voorstel 5, voorstel 3, voorstel 4, voorstel 2, voorstel 1.

**Herhaling 2:**

Aanbiedingen voor strategie 3 worden geëvalueerd (voorstel 5, voorstel 6). Laten we zeggen dat het resultaat:

* Voorstel 5 - Wordt niet geëvalueerd omdat dit al in het bovenstaande resultaat voorkomt.
* Voorstel 6 - 60

De gerangschikte voorstellen zijn nu als volgt: Voorstel 5, voorstel 3, voorstel 4, voorstel 2, voorstel 1, voorstel 6.

+++

### Extra voorstellen toevoegen {#fallback}

Nadat u de keuze hebt gemaakt voor de keuze van de onderdelen en/of de selectiestrategieën, kunt u back-upaanbiedingen toevoegen die worden weergegeven aan gebruikers als geen van de bovenstaande items of selectiestrategieën gekwalificeerd zijn.

![](assets/decision-code-based-strategy-fallback.png)

U kunt elk item in de lijst selecteren, waarin alle beslissingsitems worden weergegeven die in de huidige sandbox zijn gemaakt. Als geen selectiestrategie wordt gekwalificeerd, wordt fallback getoond aan de gebruiker ongeacht de data en de geschiktheidsbeperking die op het geselecteerde punt <!--nor frequency capping when available - TO CLARIFY--> wordt toegepast.

>[!NOTE]
>
>Een fallback is optioneel. Als er geen fallback is geselecteerd en geen strategie is gekwalificeerd, wordt er niets weergegeven door [!DNL Journey Optimizer] . U kunt het aantal objecten optellen dat het besluitvormingsbeleid aanvraagt. Dit garandeert dat een bepaald aantal items wordt geretourneerd als dat nodig is voor het gebruik.

Wanneer uw beslissingsbeleid klaar is, slaat u het op en klikt u op **[!UICONTROL Create]** . Nu het besluitvormingsbeleid wordt gecreeerd, kunt u de besluitvormingsattributen binnen uw code-gebaseerde ervaringsinhoud gebruiken. [Meer informatie](#use-decision-policy)

![](assets/decision-code-based-decision-added.png)

## Het beslissingsbeleid in de code-editor gebruiken {#use-decision-policy}

Zodra gecreeerd, kan het besluitvormingsbeleid in de [ verpersoonlijkingsredacteur ](../code-based/create-code-based.md#edit-code) worden gebruikt. Volg de onderstaande stappen om dit te doen.

>[!NOTE]
>
>De op code-gebaseerde ervaring gebruikt de [!DNL Journey Optimizer] verpersoonlijkingsredacteur met al zijn verpersoonlijking en auteursmogelijkheden. [Meer informatie](../personalization/personalization-build-expressions.md)

1. Klik op de knop **[!UICONTROL Insert policy]**. De code die overeenkomt met het beslissingsbeleid wordt toegevoegd.

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >Deze opeenvolging zal het aantal tijden worden herhaald u het besluitvormingsbeleid wilt zijn teruggekeerd. Bijvoorbeeld, als u verkoos om terug 2 punten terug te keren wanneer [ creërend het besluit ](#add-decision), zal de zelfde opeenvolging tweemaal worden herhaald.

1. Nu kunt u alle beslissingskenmerken toevoegen die u in die code wilt. De beschikbare kenmerken worden opgeslagen in het schema van de catalogus van **[!UICONTROL Offers]** . De attributen van de douane worden opgeslagen in **`_<imsOrg`>** omslag en standaardattributen in de **`_experience`** omslag. [ Leer meer over het schema van de catalogus van Aanbiedingen ](catalogs.md)

   ![](assets/decision-code-based-decision-attributes.png)

   >[!NOTE]
   >
   >Voor het volgen van het Punt van het besluitvormingsbeleid, moet de `trackingToken` attributen als volgt voor de inhoud van het besluitvormingsbeleid worden toegevoegd:
   >`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

1. Klik op elke map om deze uit te vouwen. Plaats de cursor van de muis op de gewenste locatie en klik op het pictogram + naast het kenmerk dat u wilt toevoegen. U kunt zoveel kenmerken aan de code toevoegen als u wilt.

   ![](assets/decision-code-based-add-decision-attributes.png)

1. U kunt ook alle andere kenmerken toevoegen die beschikbaar zijn in de verpersoonlijkingseditor, zoals profielkenmerken.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Klik op **[!UICONTROL Save and close]** om uw wijzigingen te bevestigen.

## Uw op code gebaseerde ervaring testen en publiceren {#test-and-publish}

Voer de onderstaande stappen uit om uw op code gebaseerde ervaring te voltooien en uw wijzigingen live te zetten.

1. Bekijk en publiceer uw op code gebaseerde ervaringscampagne of reis. [ leer hoe ](../code-based/publish-code-based.md)

   Zodra uw ontwikkelaar een API- of SDK-aanroep maakt om inhoud op te halen voor het oppervlak dat is gedefinieerd in uw kanaalconfiguratie, worden de wijzigingen toegepast op uw webpagina of app.

1. Momenteel kunt u geen inhoud van het gebruikersinterface in a [ code-gebaseerde ervaring ](../code-based/create-code-based.md) campagne of reis simuleren gebruikend besluiten.

   Als tijdelijke oplossing kunt u de besluitvorming testen nadat u uw campagne hebt gepubliceerd door de markering `dryRun` toe te voegen aan het XDM-gebeurtenisblok `data` in uw clientimplementatie:

   ```
   {
       "data": {
           "__adobe": {
               "ajo": {
                   "dryRun": true
               }
           }
       }
   }
   ```

1. Om te zien hoe uw besluiten presteren, kunt u douane [ Customer Journey Analytics nu creëren rapporterend dashboards ](cja-reporting.md).


