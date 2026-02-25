---
title: Rangschikkingsformules voor arbitrage over reizen
description: Leer hoe u formules maakt om reizen voor arbitrage te rangschikken, zodat de beste reis per profiel wordt geselecteerd op basis van regels en context.
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="Beperkte beschikbaarheid" type="Informative"
source-git-commit: fe6e8221201ee813251a46c6603d85f0803873c0
workflow-type: tm+mt
source-wordcount: '1065'
ht-degree: 0%

---

# Formules gebruiken om reizen te rangschikken {#journey-ranking-formulas}

>[!AVAILABILITY]
>
>Deze functie bevindt zich momenteel in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

Met [!DNL Adobe Journey Optimizer] kunt u bepalen welke ritten een profiel kan invoeren wanneer ze in aanmerking komen voor meer dan het systeem toestaat. Om dit te doen, kunt u [&#x200B; regelreeksen &#x200B;](rule-sets.md) gebruiken om caps op reisingang of gelijktijdig te bepalen. Wanneer een profiel voor meer reizen in aanmerking komt dan het maximum toestaat, bepaalt de prioriteit die aan elke reis wordt toegekend welke ritten worden gekozen.

In plaats van prioriteit te gebruiken, kunt u **het rangschikken formules** ook gebruiken om het rangschikken van reizen dynamisch aan te passen die op reisattributen, profielattributen, of AI modelscores worden gebaseerd.

Formules geven u meer flexibiliteit dan statische prioriteit. U kunt bijvoorbeeld een reis stimuleren voor leden van goudloyaliteit.

<!--
>[!NOTE]
>
>Journey ranking formulas follow the same guardrails as decisioning ranking formulas (nesting depth, rule string size). [Learn more about Decisioning guardrails & limitations](../experience-decisioning/decisioning-guardrails.md#ranking-formulas).-->

## Een waarderingsformule maken {#create-journey-ranking-formula}

Volg onderstaande stappen om een rangschikkingsformule voor uw reizen te maken.

1. Open de sectie **[!UICONTROL Orchestration ranking]** en selecteer vervolgens de tab **[!UICONTROL Ranking formulas]** . De lijst met eerder gemaakte formules wordt weergegeven.

1. Klik op **[!UICONTROL Create formula]**.

1. Geef de naam van de formule op en voeg desgewenst een beschrijving toe.

   ![&#x200B; de detailsruit van de Formule met naam en beschrijvingsgebieden &#x200B;](assets/journey-formula-details.png){width="80%"}


   >[!NOTE]
   >
   >Het rangschikkende object is de entiteit waarop de rangschikkingsformule van toepassing is. Standaard is de positie van het waarderingsobject ingesteld op **[!UICONTROL Journey]** .

   <!--
    Selecting a formula entity specifies which type of item—such as journeys or other entities—the ranking formula will apply to. This determines the context in which the formula operates, allowing you to define rules that influence how those items are ranked.-->

1. Klik optioneel op **[!UICONTROL Select AI model]** om het model in te stellen dat wordt gebruikt als referentie om uw waarderingsformule samen te stellen.

<!--
    >[!NOTE]
    >
    >[Personalized optimization models](../experience-decisioning/ranking/personalized-optimization-model.md) using continuous metrics are not supported with the AI formula builder.

    Every time you refer to a model score when defining your formula below, the AI model that you selected will be used. [Learn more on AI models](../experience-decisioning/ranking/ai-models.md)-->

1. Geef in de sectie **[!UICONTROL Criterion 1]** op op welke ritten u een waarderingsscore wilt toepassen door het volgende te doen:

   * Selecteer a [&#x200B; reisattributen &#x200B;](../building-journeys/journey-properties.md) (zoals reisnaam, markeringen, prioriteit, of andere reiseigenschappen);
   * een logische operator te selecteren;
   * Voeg een passende voorwaarde toe - u kunt of een waarde typen/selecteren, of een profielattribuut kiezen.

   ![&#x200B; Criterium 1 sectie met reisattributen, exploitant, en passende voorwaarde &#x200B;](assets/journey-formula-criterion-1.png){width="70%"}

1. U kunt desgewenst aanvullende elementen opgeven om de overeenkomende voorwaarden voor de geldigheid van de criteria te verfijnen.

   ![&#x200B; Aanvullende voorwaarde om passende criteria te verfijnen &#x200B;](assets/journey-formula-additional-condition.png){width="70%"}

   Bijvoorbeeld, bepaalde u *Criterium 1* zoals *de markeringen van de Reis* *Loyalty*. Bovendien, kunt u een andere voorwaarde toevoegen zoals als de *status van de Loyalty* *Goud* evenaart, dan *Criterium 1* waar is.

1. Maak een expressie waarmee een rangschikkingsscore wordt toegewezen aan de reizen die aan de hierboven gedefinieerde voorwaarde voldoen. U kunt naar elk van de volgende items verwijzen:
   * een variabele:
      * de reisprioriteit, die een handwaarde is die aan de reis wordt toegewezen wanneer [&#x200B; creërend een reis &#x200B;](../building-journeys/journey-gs.md);
      * de score die is behaald uit het AI-model dat u optioneel hierboven hebt geselecteerd;
   * een kenmerk:
      * alle kenmerken die in het profiel kunnen voorkomen, zoals een extern afgeleide vermogensscore;
      * een reiskenmerk;
   * een statische waarde die u in een vrije indeling kunt toewijzen;
   * een combinatie van alle bovenstaande elementen.

   ![&#x200B; Bouwer van de Uitdrukking om het rangschikken score toe te wijzen gebruikend variabelen, attributen, of statische waarden &#x200B;](assets/journey-formula-expression.png){width="70%"}

1. Klik op **[!UICONTROL Add criterion]** om een of meer criteria toe te voegen zo vaak als nodig is. De logica is als volgt:
   * Als het eerste criterium geldt voor een bepaald beslissingselement, heeft het voorrang op de volgende.
   * Indien niet waar (true), gaat de beslissingsengine door naar het tweede criterium, enzovoort.

1. Nadat u alle criteria hebt gedefinieerd, kunt u in het laatste veld een expressie maken die wordt toegewezen aan alle ritten die niet aan de bovenstaande criteria voldoen.

   ![&#x200B; gebied van de Uitdrukking voor reizen die om het even welke criteria niet voldoen &#x200B;](assets/journey-formula-criteria-not-met.png){width="70%"}

1. Klik op **[!UICONTROL Create]** om uw waarderingsformule te voltooien.

U kunt deze formule nu in de lijst selecteren om de details ervan weer te geven en deze te bewerken of te verwijderen. Het is dan beschikbaar wanneer u een regelreeks vormt. [&#x200B; leer hoe &#x200B;](#assign-formula-to-ruleset)

### Voorbeelden van willekeurige formules {#journey-ranking-formula-example}

Bekijk de onderstaande voorbeelden.

+++Voorbeeld 1: gebruik van reisprioriteit of AI-score op basis van transportlabels

![&#x200B; Rangschikkende formule: De markering van de marketing gebruikt reisprioriteit &#x200B;](assets/journey-formula-ex-1.png){width="60%"}

Als de reis een &quot;Marketing&quot;markering heeft, is de rangschikkingsscore de reisprioriteit.

![&#x200B; Willekeurige formule: De markering van de Promo gebruikt AI modelscore &#x200B;](assets/journey-formula-ex-2.png){width="60%"}

Als de reis een &quot;Promo&quot;markering heeft, is de rangschikkende score de AI modelscore.

+++

+++Voorbeeld 2: Meer loyaliteit per profielstatus


![&#x200B; Rangschikkende formule: De markering van de Loyalty met de status van het Goud gebruikt reis prioriteit plus 5 &#x200B;](assets/journey-formula-ex-3.png){width="60%"}

Als de reis een &quot;Loyalty&quot;markering heeft en de loyaliteitsstatus van het profiel Goud is, is de rangorde die wordt gebruikt de reisprioriteit plus 5.

![&#x200B; Willekeurige formule: De markering van de Loyalty met de status van de Zilver gebruikt reisprioriteit plus 2 &#x200B;](assets/journey-formula-ex-4.png){width="60%"}

Als de reis een &quot;Loyalty&quot;markering heeft en de status van de loyaliteit van het profiel Zilver is, is de rangschikkende score de reisprioriteit plus 2.

Als aan geen van de bovenstaande voorwaarden wordt voldaan, is de gebruikte rangorde de prioriteit van de reis.

+++

### De code-editor gebruiken {#journey-ranking-formula-code-editor}

Om rangschikkende formules in **syntaxis van PQL** uit te drukken, schakelaar aan de coderedacteur gebruikend de specifieke knoop op hoogste recht van het scherm. Voor meer op hoe te om de syntaxis van PQL te gebruiken, verwijs naar de [&#x200B; specifieke documentatie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html).

>[!CAUTION]
>
>Hierdoor kunt u niet terugkeren naar de standaardbuilderweergave voor deze formule.

Vervolgens kunt u reiskenmerken, profielkenmerken en statische waarden gebruiken om uw waarderingsformule samen te stellen.

<!--The code editor is similar to the one used in Decisioning ranking formulas. [Learn more](../experience-decisioning/ranking/ranking-formulas.md#ranking-code-editor)-->

## Wijs de formule aan een regelreeks toe {#assign-formula-to-ruleset}

Om een formule te gebruiken om uw reizen te rangschikken, moet u het aan een regelreeks toewijzen.

>[!NOTE]
>
>Formules worden toegewezen op het niveau van de regel, niet op individuele reizen.

1. Maak in het menu **[!UICONTROL Business rules]** een regelset die u wilt gebruiken voor arbitrage tijdens de rit. [&#x200B; leer hoe &#x200B;](rule-sets.md#Create)

1. Selecteer het domein **[!UICONTROL Journey]** .

   ![&#x200B; de vastgestelde eigenschappen van de Regel met geselecteerd domein van de Reis &#x200B;](assets/journey-formula-rule-set-journey.png){width="60%"}

1. Stel in de regelseteigenschappen de waarde **[!UICONTROL Ranking method]** in op **[!UICONTROL Formula]** (in plaats van de standaardwaarde **[!UICONTROL Priority]** ).

1. Selecteer de rangschikkingsformule die u van de drop-down lijst creeerde.

   ![&#x200B; Regel die met het rangschikken van geselecteerde formule van drop-down lijst &#x200B;](assets/journey-rule-set-formula.png){width="60%"} wordt geplaatst

1. Maak de regels voor het afdekken van de verplaatsingen die u aan de regelset wilt toevoegen. [&#x200B; leer hoe &#x200B;](journey-capping.md#create-rule)

1. Sla de regelset op.

Nu wordt de formule toegewezen aan de regelreeks. Vervolgens kunt u die regel op uw reizen toepassen.

## Pas de regel toe die op een reis is ingesteld {#assign-rule-set-to-journey}

Volg de onderstaande stappen om de regel toe te wijzen die aan een reis is ingesteld.

1. Maak of open de reis waaraan u de regel wilt toewijzen. [&#x200B; leer hoe te om een reis &#x200B;](../building-journeys/journey-gs.md) tot stand te brengen

1. Selecteer in de reiseigenschappen de regelset in de vervolgkeuzelijst.  [&#x200B; leer hoe &#x200B;](journey-capping.md#apply-capping).

   >[!NOTE]
   >
   >Er kan slechts één regelset tegelijk op een reis worden toegepast.

1. Bespaar de reis.

Alle ritten die van deze regel gebruik maken, worden gerangschikt met de geselecteerde formule wanneer de lampvoet wordt toegepast.

Om te controleren hoe uw regelreeksen en rangschikkende formules presteren, zie het [&#x200B; Afschilderen van de Reis en de sectie van Conflicten &#x200B;](../reports/channel-report-cja.md#rule-sets) in het Overzicht rapport.

<!--
## Reporting {#reporting}

Reporting for journey arbitration helps you understand how rule sets and ranking formulas perform:

* **Exclusions** – Whether journeys were excluded from users and which rule set (and reason) prevented entry.
* **Rule set performance** – For each rule set, metrics such as journey enters, journey exclusions, journey engagement, and other optimization metrics.
* **Cross-journey view** – Time-based view of profiles across journeys (e.g. journey enters, failures, exclusions) to see the impact of capping and ranking.

Use these reports to validate that your formulas and caps are behaving as intended and to tune ranking logic over time.-->

