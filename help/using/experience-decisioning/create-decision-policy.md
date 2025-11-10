---
title: Beleid voor beslissingen maken
description: Leer hoe u beleidsbeslissingen maakt
feature: Decisioning
topic: Integrations
role: User
level: Experienced
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '1667'
ht-degree: 0%

---


# Beslissingsbeleid maken {#create-decision}

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
>additional-url="https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Strategieën maken"

Om de beste dynamische aanbieding en ervaring aan uw klanten voor te stellen, voeg een besluitvormingsbeleid aan uw inhoud in een campagne of reis dan vormen de punten om terug te keren en de selectiestrategie aan gebruik. Hiervoor voert u de volgende stappen uit:

1. [&#x200B; voeg een besluitvormingsbeleid &#x200B;](#add) toe - van de redacteur van Personalization of E-mail Designer.
1. [&#x200B; vorm het besluitvormingsbeleid &#x200B;](#configurre) - voeg een naam toe en specificeer het aantal punten om terug te keren.
1. [&#x200B; opstelling een strategieopeenvolging &#x200B;](#strategy) - selecteer de punten met het besluitvormingsbeleid terug te keren.
1. [&#x200B; Uitgezochte reserveaanbiedingen &#x200B;](#fallback) (facultatief) - selecteer punten om te tonen als geen punten of selectiestrategieën worden gekwalificeerd.
1. [&#x200B; Overzicht en sparen &#x200B;](#review) de selectiestrategie

>[!AVAILABILITY]
>
>Voor nu, zijn het besluitvormingsbeleid beschikbaar aan alle klanten voor het **op code-gebaseerde kanaal van de Ervaring**. Zij zijn beschikbaar voor het **E-mail** kanaal als Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

## Een beslissingsbeleid toevoegen {#add}

1. Open een reis of een campagne, selecteer de actie van het a [&#x200B; kanaal &#x200B;](../building-journeys/journeys-message.md) en geef de inhoud van uw bericht uit.

1. Schakel de optie **[!UICONTROL Enable decisioning]** in voor e-mailberichten.

   ![](assets/decision-policy-enable.png)

   >[!IMPORTANT]
   >
   >Als u beslissingen toestaat, wordt bestaande e-mailinhoud gewist. Als u uw e-mail al hebt ontworpen, moet u uw inhoud vooraf opslaan als een sjabloon.
   >
   >Merk op dat om het even welk die besluitvormingsbeleid binnen e-mail wordt gevormd niet in het malplaatje zal worden bewaard. Als u het malplaatje op een andere e-mail toepast, moet u het beleid opnieuw vormen.

1. Open de **verpersoonlijkingsredacteur** om het besluitvormingsbeleid tot stand te brengen. Voor e-mail, kunt u een specifiek menu in de **E-mail ontwerper** ook gebruiken om een besluitvormingsbeleid tot stand te brengen. Vouw de onderstaande secties uit om de twee methoden te verkennen.

   +++Een beslissingsbeleid maken vanuit de Personalization-editor

   1. Open de personalisatie-editor en selecteer **[!UICONTROL Decision policy]** .
   1. Klik op de knop **[!UICONTROL Add decision policy]** om een nieuw beleid te maken.

      ![](assets/decision-code-based-create.png)

   +++

   +++Een beslissingsbeleid maken via de e-mailserver-Designer

   Selecteer een component in uw e-mailinhoud, klik op het pictogram **[!UICONTROL Decisioning]** op de werkbalk of in het deelvenster Eigenschappen en selecteer vervolgens **[!UICONTROL Add new policy]** .

   Met **[!UICONTROL Reuse decision output]** kunt u een beslissingsbeleid opnieuw gebruiken dat al in deze e-mail is gemaakt.

   ![](assets/decision-policy-email-designer.png)

   +++

## Het beslissingsbeleid configureren {#configure}

Nadat u een nieuw besluitvormingsbeleid in uw inhoud hebt toegevoegd, opent het scherm van de configuratiescherm van het beslissingsbeleid.

1. Geef een naam op voor het beslissingsbeleid en selecteer een catalogus (die momenteel is beperkt tot de standaardcatalogus **[!UICONTROL Offers]** ).

1. Selecteer het aantal items dat u wilt retourneren. Als u bijvoorbeeld 2 selecteert, worden de beste twee in aanmerking komende aanbiedingen voor de huidige configuratie weergegeven.

   ![](assets/decision-code-based-details.png)

   Voor het e-mailkanaal is het veld **[!UICONTROL Number of items]** standaard ingesteld op 1 en kan dit alleen worden gewijzigd als het beslissingsbeleid wordt toegevoegd vanuit een component **[!UICONTROL Repeat Grid]** . Vouw de onderstaande sectie uit voor meer informatie:

   +++Meerdere beslissingsitems in e-mails retourneren met een component **[!UICONTROL Repeat Grid]**

   1. Sleep een component **[!UICONTROL Repeat Grid]** in de e-mail en configureer deze naar wens in het deelvenster **[!UICONTROL Settings]** .

      ![](assets/decision-policy-repeat.png)

   1. Klik op het pictogram **[!UICONTROL Decisioning]** op de canvaswerkbalk of open het deelvenster **[!UICONTROL Decisioning]** en selecteer **[!UICONTROL Add decision policy]** .

   1. Geef het aantal items op dat in het veld **[!UICONTROL Number of items]** moet worden geretourneerd en configureer vervolgens het beslissingsbeleid zoals hieronder beschreven. Het maximumaantal items dat u kunt selecteren, wordt beperkt door het aantal tegels dat is gedefinieerd in de component **[!UICONTROL Repeat grid]** .

   ![](assets/decision-policy-repeat-number.png)

   +++

1. Klik op **[!UICONTROL Next]**.

## Een strategiereeks instellen {#strategy}

In de sectie **[!UICONTROL Strategy sequence]** kunt u de beslissingsitems selecteren en selectiestrategieën instellen die in het besluitvormingsbeleid worden weergegeven.

1. Klik op **[!UICONTROL Add]** en kies het type object dat u in het beleid wilt opnemen:

   ![](assets/decision-code-based-strategy-sequence.png)

   * **[!UICONTROL Selection strategy]** - Beslissingsstrategieën maken gebruik van collecties die verband houden met geschiktheidsbeperkingen en rangordemethoden om te bepalen welke items moeten worden weergegeven. U kunt een of meerdere bestaande selectiestappen selecteren of een nieuwe strategie maken met de knop **[!UICONTROL Create selection strategy]** . [&#x200B; Leer hoe te om selectiestrategieën &#x200B;](selection-strategies.md) tot stand te brengen

   * **[!UICONTROL Decision item]** - Selecteer enkele-beslissingsitems zonder een selectiestrategie te moeten doorlopen. U kunt slechts één beslissingsitem tegelijk selecteren. Alle voorwaarden die voor het onderdeel zijn ingesteld, zijn van toepassing.

   >[!NOTE]
   >
   >Een beslissingsbeleid ondersteunt maximaal 10 selectiestrategieën en besluitvormingselementen samen. [&#x200B; leer meer over het Beslissen van gidsen &amp; beperkingen &#x200B;](gs-experience-decisioning.md#guardrails)

1. Wanneer het toevoegen van verscheidene besluitvormingspunten en/of strategieën, zullen zij in een specifieke orde worden geëvalueerd. Het eerste object dat aan de reeks is toegevoegd, wordt eerst geëvalueerd, enzovoort. Als u de standaardvolgorde wilt wijzigen, sleept u de objecten en/of de groepen en zet u deze neer om ze naar wens opnieuw te rangschikken. Vouw de onderstaande sectie uit voor meer informatie.

   +++De evaluatievolgorde in een beslissingsbeleid beheren

   Nadat u besluitvormingspunten en selectiestrategieën aan uw beleid hebt toegevoegd, kunt u hun volgorde rangschikken om hun evaluatievolgorde te bepalen en kunt u selectiestrategieën combineren om deze samen te evalueren.

   De **opeenvolgende orde** waarin de punten en de strategieën zullen worden geëvalueerd wordt vermeld met aantallen links van elk voorwerp of groep voorwerpen. Als u de positie van een selectiestrategie (of een groep strategieën) binnen de reeks wilt verplaatsen, sleept u deze naar een andere positie.

   ![](assets/decision-code-based-strategy-groups.png)

   >[!NOTE]
   >
   >Alleen selectiestrategieën kunnen binnen een reeks worden gesleept en neergezet. Als u de positie van een beslissingsitem wilt wijzigen, moet u het item verwijderen en opnieuw toevoegen met de knop **[!UICONTROL Add]** nadat u de andere items hebt toegevoegd die u eerder wilt evalueren.

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

   **Voorbeeld met veelvoudige strategieën**

   Laten we nu een voorbeeld bekijken waarbij meerdere strategieën verdeeld zijn in verschillende groepen. U hebt drie strategieën gedefinieerd. Strategie 1 en Strategie 2 zijn in groep 1 samengevoegd en strategie 3 is onafhankelijk (groep 2). De in aanmerking komende aanbiedingen voor elke strategie en hun prioriteit (gebruikt bij de beoordeling van de rangorde) zijn als volgt:

   * Groep 1:
      * Strategie 1 - (Aanbieding 1, Aanbieding 2, Aanbieding 3) - Prioriteit 1
      * Strategie 2 - (Aanbieding 3, Aanbieding 4, Aanbieding 5) - Prioriteit 1

   * Groep 2:
      * Strategie 3 - (aanbod 5, aanbod 6) - Prioriteit 0

   De belangrijkste prioritaire strategische aanbiedingen worden eerst geëvalueerd en aan de gerangschikte biedingenlijst toegevoegd.

   * **Herhaling 1:**

     Aanbiedingen voor strategie 1 en strategie 2 worden samen geëvalueerd (Aanbieding 1, Aanbieding 2, Aanbieding 3, Aanbieding 4, Aanbieding 5). Laten we zeggen dat het resultaat:

     Aanbieding 1 - 10
Voorstel 2 - 20
Aanbieding 3 - 30 van strategie 1, 45 van strategie 2. Het hoogste van beide wordt in overweging genomen, dus er wordt rekening gehouden met 45.
Voorstel 4 - 40
Voorstel 5 - 50

     De gerangschikte voorstellen zijn nu als volgt: Voorstel 5, voorstel 3, voorstel 4, voorstel 2, voorstel 1.

   * **Herhaling 2:**

     Aanbiedingen voor strategie 3 worden geëvalueerd (voorstel 5, voorstel 6). Laten we zeggen dat het resultaat:

      * Voorstel 5 - Wordt niet geëvalueerd omdat dit al in het bovenstaande resultaat voorkomt.
      * Voorstel 6 - 60

     De gerangschikte voorstellen zijn nu als volgt: Voorstel 5, voorstel 3, voorstel 4, voorstel 2, voorstel 1, voorstel 6.

   +++

1. Klik op **[!UICONTROL Next]** als uw selectiestrategie gereed is.

## Extra voorstellen toevoegen {#fallback}

Nadat u de keuze hebt gemaakt voor de keuze van de onderdelen en/of de selectiestrategieën, kunt u terugvalvoorstellen toevoegen om weer te geven als geen van de bovenstaande items of selectiestrategieën gekwalificeerd zijn.

U kunt elk item in de lijst selecteren, waarin alle beslissingsitems worden weergegeven die in de huidige sandbox zijn gemaakt. Als geen selectiestrategie wordt gekwalificeerd, wordt fallback getoond aan de gebruiker ongeacht de data en de geschiktheidsbeperking die op het geselecteerde punt <!--nor frequency capping when available - TO CLARIFY--> wordt toegepast.

![](assets/decision-code-based-strategy-fallback.png)

>[!NOTE]
> Back-ups zijn optioneel. U kunt maximaal het aantal aangevraagde objecten selecteren. Als geen verkiesbaar zijn en geen reserve wordt geplaatst, zal niets worden getoond.

## Beslissingsbeleid bekijken en opslaan {#review}

Nadat u een selectiestrategie hebt geconfigureerd en fallback-voorstellen hebt toegevoegd, klikt u op **[!UICONTROL Next]** om uw beslissingsbeleid te bekijken en op te slaan. Klik vervolgens op **[!UICONTROL Create]** om het maken van het beleid te bevestigen.

U kunt een besluitbeleid op elk ogenblik uitgeven of schrappen gebruikend de ellipsieknoop in de verpersoonlijkingsredacteur, of in het **[!UICONTROL Decisioning]** menu binnen de ruit van componenteneigenschappen.

>[!BEGINTABS]

>[!TAB  geef uit of schrap een beleid van de verpersoonlijkingsredacteur ]

![](assets/decision-policy-edit.png)

>[!TAB  geef of schrap een beleid van de eigenschappen van de component uit ]

![](assets/decision-policy-edit-properties.png)

>[!ENDTABS]

## Plaatsing toewijzen (e-mail) {#placement}

Voor e-mailberichten moet u een plaatsing definiëren voor de component die aan het beslissingsbeleid is gekoppeld. Klik hiertoe op de knop **[!UICONTROL Decisioning]** in het deelvenster Eigenschappen van component en selecteer **[!UICONTROL Assign placement]** . [&#x200B; Leer hoe te met plaatsen &#x200B;](../experience-decisioning/placements.md) te werken

![](assets/decision-policy-rail.png)

## Volgende stappen {#next-steps}

Nu u weet hoe u een beslissingsbeleid kunt maken, kunt u dit beleid gebruiken in [!DNL Journey Optimizer] kanalen om aanbiedingen te leveren.

➡️ [&#x200B; Leer hoe te om besluitvormingsbeleid in berichten te gebruiken &#x200B;](../experience-decisioning/use-decision-policy.md)

