---
title: Beoordelingsformule
description: Meer informatie over het maken van formules om aanbiedingen te beoordelen
feature: Ranking, Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 35d7488b-e7d8-402f-b337-28a0c869bff0
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---

# De AI-formulebuilder gebruiken {#create-ranking-formulas}

**Rangschikkende formules** staan u toe om regels te bepalen die welke aanbieding eerst, eerder dan rekening houdend met de prioritaire scores zullen bepalen.

Als u deze regels wilt maken, biedt de AI-formule builder in **[!UICONTROL Adobe Journey Optimizer]** meer flexibiliteit en controle voor de manier waarop aanbiedingen worden gerangschikt. In plaats van alleen te vertrouwen op een statische aanbiedingsprioriteit, kunt u nu aangepaste rangschikkingsformules definiëren die AI-modelscores combineren, prioriteiten, profielkenmerken bieden, kenmerken aanbieden en contextuele signalen via een geleide interface.

Deze benadering staat u toe om aanbiedingsrangschikking dynamisch aan te passen die op om het even welke combinatie van AI-gedreven neiging, bedrijfswaarde, en context in real time wordt gebaseerd, die het gemakkelijker maken om besluitvorming aan zowel marketing doelstellingen als klantenbehoeften te richten. De AI-formulebuilder ondersteunt eenvoudige of geavanceerde formules, afhankelijk van de mate van controle die u wilt toepassen.

Zodra een het rangschikken formule is gecreeerd, kunt u het aan a [ selectiestrategie ](selection-strategies.md) toewijzen. Als meerdere aanbiedingen in aanmerking komen om te worden gepresenteerd wanneer deze selectiestrategie wordt gebruikt, gebruikt de beslissingsmotor de geselecteerde formule om te berekenen welke aanbieding het eerst moet worden geleverd.

## Een waarderingsformule maken {#create-ranking-formula}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="Rangschikkingsformules maken"
>abstract="Met indelingen kunt u regels definiëren die bepalen welk beslissingsitem als eerste moet worden weergegeven, in plaats van rekening te houden met de prioriteitsscores van de items. Nadat u een rangschikkingsformule hebt gemaakt, kunt u deze toewijzen aan een selectiestrategie."

Volg de onderstaande stappen om een rangschikkingsformule te maken.

1. Open het menu **[!UICONTROL Strategy setup]** en selecteer vervolgens **[!UICONTROL Ranking formulas]** tab. De lijst met eerder gemaakte formules wordt weergegeven.

   ![](assets/ranking-formulas-list.png)

1. Klik op **[!UICONTROL Create formula]**.

1. Geef de naam van de formule op en voeg desgewenst een beschrijving toe.

   ![](assets/create-formula.png){width="80%"}

1. Klik optioneel op **[!UICONTROL Select AI model]** om het model in te stellen dat wordt gebruikt als referentie om uw waarderingsformule samen te stellen.

   >[!NOTE]
   >
   >[ Gepersonaliseerde optimalisatiemodellen ](../offers/ranking/personalized-optimization-model.md) die ononderbroken metriek gebruiken worden niet gesteund met de AI formule bouwer.

   Telkens wanneer u naar een modelscore verwijst wanneer u hieronder uw formule bepaalt, zal het AI model worden gebruikt dat u selecteerde.

   >[!CAUTION]
   >
   >Wanneer het gebruiken van een AI model in een rangschikkende formule wordt opgenomen, worden de gegevens niet weerspiegeld in het [ tarief van de Omzetting voor Holdout en Model Gedreven verkeer ](../reports/campaign-global-report-cja-code.md#conversion-rate) rapport.

1. Bepaal de voorwaarden die de rangschikkingsscore voor de passende besluitvormingspunten zullen bepalen. U kunt

   * vul de **[!UICONTROL Criteria]** sectie van het [ gebruikersinterface ](#ranking-select-criteria) in,
   * of schakelaar aan de [ coderedacteur ](#ranking-code-editor).

<!--## Select an ELS dataset {#els-dataset}

To leverage data from an AEP dataset, you can select it in the **[!UICONTROL ELS settings]** section.

1. Select an ELS dataset from the list.

1. Select a decision attribute. This action is mandatory.

![](assets/formula-els-settings.png){width="80%"}

-->

## Criteria definiëren met behulp van de formule builder {#ranking-select-criteria}

Met een intuïtieve interface kunt u de besluitvorming perfectioneren door AI-scores (eigenheid) aan te passen, waarde (prioriteit) aan te bieden, contextafhankelijke hefbomen en externe profieleigenschappen — afzonderlijk of in combinatie — om elke interactie te optimaliseren. <!--Whether you are maximizing revenue, promoting strategic offers, or balancing business goals with real-time context, the formula builder gives you total control in defining ranking strategies.-->

Volg de onderstaande stappen om criteria rechtstreeks vanuit de interface te definiëren.

<!--![](assets/ranking-formula-criteria.png){width="80%"}-->

1. Geef in de sectie **[!UICONTROL Criterion 1]** de beslissingsitems op waarop u een waarderingsscore wilt toepassen door het volgende te doen:
   * selecteer de attributen van het a [ besluitvormingspunt ](items.md#attributes),
   * een logische operator te selecteren,
   * Voeg een passende voorwaarde toe - u kunt of een waarde typen, of een profielattribuut of [ contextgegevens ](context-data.md) selecteren.

   ![](assets/ranking-formula-criterion-1.png){width="70%"}

1. U kunt desgewenst aanvullende elementen opgeven om de overeenkomende voorwaarden voor de geldigheid van de criteria te verfijnen.

   ![](assets/ranking-formula-addtional-conditions.png){width="80%"}

   Bijvoorbeeld, bepaalde u Criterium 1 zoals *Weather* douaneattribuut *evenaart* de *warme* voorwaarde. Bovendien, kunt u een andere voorwaarde toevoegen zoals als aan de eerste voorwaarde wordt voldaan en als de temperatuur 75 graden op het tijdstip van het verzoek overschrijdt, dan is Criterium 1 waar.<!--Add a screenshot with the example-->

1. Creeer een uitdrukking die een rangschikkingsscore aan de besluitpunten zal toewijzen die aan de hierboven bepaalde voorwaarde voldoen. U kunt naar elk van de volgende items verwijzen:

   * de score die uit het AI model kwam dat u naar keuze in de **[!UICONTROL Details]** sectie [ hierboven ](#create-ranking-formula) selecteerde;
   * de prioriteit van het besluitvormingspunt, die een waarde manueel wordt toegewezen wanneer [ creërend een besluitvormingspunt ](items.md#attributes); <!--If a profile qualifies for multiple decision items, a higher priority grants the item precedence over others.-->
   * alle kenmerken die in het profiel kunnen voorkomen, zoals een extern afgeleide vermogensscore;
   * een statische waarde die u in een vrije indeling kunt toewijzen;
   * een combinatie van alle bovenstaande punten.

   ![](assets/ranking-formula-expression.png){width="70%"}

   >[!NOTE]
   >
   >Klik op het pictogram naast het veld om vooraf gedefinieerde variabelen toe te voegen.

1. Klik op **[!UICONTROL Add criterion]** om een of meer criteria toe te voegen zo vaak als nodig is. De logica is als volgt:
   * Als het eerste criterium geldt voor een bepaald beslissingselement, heeft het voorrang op de volgende.
   * Indien niet waar (true), gaat de beslissingsengine door naar het tweede criterium, enzovoort.

1. In het laatste veld kunt u een expressie maken die wordt toegewezen aan alle beslissingsitems die niet aan de bovenstaande criteria voldoen.

   ![](assets/ranking-formula-criteria-not-met.png){width="70%"}

1. Klik op **[!UICONTROL Create]** om uw waarderingsformule te voltooien. U kunt deze nu in de lijst selecteren om de details weer te geven en vervolgens bewerken of verwijderen. Het is klaar om in a [ selectiestrategie ](selection-strategies.md) te worden gebruikt om in aanmerking komende besluitvormingspunten te rangschikken.

### Voorbeeld van een willekeurige formule

Bekijk het onderstaande voorbeeld:

![](assets/ranking-formula-example.png){width="80%"}

Als het gebied van het besluitpunt (douaneattribuut) het geografische etiket van het profiel (profielattributen) evenaart, zal de rangschikkingsscore die hier wordt uitgedrukt (die een combinatie van de prioriteit van het besluitpunt, de AI modelscore en een statische waarde) is worden toegepast op alle besluitvormingspunten die aan die voorwaarde voldoen.

## De code-editor gebruiken {#ranking-code-editor}

Om rangschikkende formules in **syntaxis van PQL** uit te drukken, schakelaar aan de coderedacteur gebruikend de specifieke knoop op hoogste recht van het scherm. Voor meer op hoe te om de syntaxis van PQL te gebruiken, verwijs naar de [ specifieke documentatie ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html).

>[!CAUTION]
>
>Hierdoor kunt u niet terugkeren naar de standaardbuilderweergave voor deze formule.

U kunt de attributen van het hefboomprofiel, [ contextgegevens ](context-data.md), en [ attributen van het besluitvormingspunt ](items.md#attributes) dan.

U wilt bijvoorbeeld de prioriteit van alle aanbiedingen verhogen met het kenmerk &quot;hot&quot; als het werkelijke weer heet is. Om dit te doen, werd **contextData.weather=hot** overgegaan in de beslissingsvraag. <!--[Learn how to work with context data](context-data.md)-->

![](assets/ranking-formula-code-editor.png){width="80%"}

>[!IMPORTANT]
>
>Wanneer u een rangschikkingsformule maakt, wordt terugkijken naar een vorige periode niet ondersteund, zoals het toevoegen van een ervaringsgebeurtenis die zich in de laatste maand heeft voorgedaan als een component van de formule. Elke poging om een terugzoekperiode op te nemen tijdens het maken van een formule, veroorzaakt een fout bij het opslaan ervan.

### PQL-voorbeelden met rangschikkingsformule {#ranking-formula-examples}

U kunt verschillende rangschikkingsformules naar wens maken. Hieronder volgen enkele voorbeelden.

+++Boost biedt aan met bepaald aanbiedingskenmerk op basis van profielkenmerk

Als het profiel in de stad woont die overeenkomt met het aanbod, dan verdubbelt de prioriteit voor alle aanbiedingen in die stad.

**Rangschikkende formule:**

```
if( offer.characteristics.get("city") = homeAddress.city, offer.rank.priority * 2, offer.rank.priority)
```

+++

+++Boost biedt aanbiedingen waarbij de einddatum minder dan 24 uur van nu is

**Rangschikkende formule:**

```
if( offer.selectionConstraint.endDate occurs <= 24 hours after now, offer.rank.priority * 3, offer.rank.priority)
```

+++

+++Boost-aanbiedingen op basis van de neiging van klanten om het aangeboden product aan te schaffen

U kunt de score voor een aanbieding verhogen op basis van een klantdichtheid-score.

In dit voorbeeld, is de instantiehuurder *_salesvelocity* en het profielschema bevat een waaier van scores die in een serie wordt opgeslagen:

![](../offers/assets/ranking-example-schema.png)

In dit geval geldt voor een profiel als:

```
{"_salesvelocity": {"individualScoring": [
                    {"core": {
                            "category":"insurance",
                            "propensityScore": 96.9
                        }},
                    {"core": {
                            "category":"personalLoan",
                            "propensityScore": 45.3
                        }},
                    {"core": {
                            "category":"creditCard",
                            "propensityScore": 78.1
                        }}
                    ]}
}
```

+++

+++Boost-aanbiedingen op basis van contextgegevens {#context-data}

Met [!DNL Journey Optimizer] kunt u bepaalde aanbiedingen verhogen op basis van de contextgegevens die in de aanroep worden doorgegeven. Als bijvoorbeeld `contextData.weather=hot` wordt doorgegeven, moet de prioriteit van alle aanbiedingen met `attribute=hot` worden verhoogd. Gedetailleerde informatie over hoe te om contextgegevens over te gaan gebruikend **Edge Beslissing** en **Beslissing** APIs, verwijs naar [ deze sectie ](context-data.md)

Merk op dat wanneer het gebruiken van **Beslissing** API, de contextgegevens aan het profielelement in het verzoeklichaam, zoals in het hieronder voorbeeld worden toegevoegd.

```
"xdm:profiles": [
{
    "xdm:identityMap": {
        "crmid": [
            {
            "xdm:id": "CRMID1"
            }
        ]
    },
    "xdm:contextData": [
        {
            "@type":"_xdm.context.additionalParameters;version=1",
            "xdm:data":{
                "xdm:weather":"hot"
            }
        }
    ]
    
}],
```

+++

