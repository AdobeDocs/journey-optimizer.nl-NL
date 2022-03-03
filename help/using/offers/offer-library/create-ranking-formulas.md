---
title: Rangschikkingsformules maken
description: Meer informatie over het maken van formules om aanbiedingen te beoordelen
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8bc808da-4796-4767-9433-71f1f2f0a432
source-git-commit: 14ab70aa32f4f7978b8c72b3981d3b55f56fd08b
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 1%

---

# Rangschikkingsformules maken {#create-ranking-formulas}

## Rangschikkingsformules {#about-ranking-formulas}

**Beoordelingsformule** kunt u regels definiëren die bepalen welke aanbieding eerst voor een bepaalde plaatsing moet worden gepresenteerd, in plaats van rekening te houden met de prioriteitsscores van de aanbiedingen.

De rangschikkingsformules worden uitgedrukt in **PQL-syntaxis** en kan profielkenmerken, contextgegevens en kenmerken gebruiken. Raadpleeg voor meer informatie over het gebruik van de PQL-syntaxis de [speciale documentatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html).

Nadat u een rangschikkingsformule hebt gemaakt, kunt u deze toewijzen aan een plaatsing in een beslissing. Zie voor meer informatie [Aanbiedingen selecteren in beslissingen configureren](../offer-activities/configure-offer-selection.md).

## Een waarderingsformule maken {#create-ranking-formula}

Voer de volgende stappen uit om een rangschikkingsformule te maken:

1. Toegang krijgen tot **[!UICONTROL Components]** en selecteert u vervolgens de **[!UICONTROL Rankings]** tab. De eerder gemaakte lijst met waarderingen wordt weergegeven.

   ![](../assets/rankings-list.png)

1. Klikken **[!UICONTROL Create ranking]** om een nieuwe rangschikkingsformule te creëren.

   ![](../assets/ranking-create-formula.png)

1. Geef de naam, beschrijving en formule van de waarderingsformule op.

   In dit voorbeeld willen we de prioriteit van alle aanbiedingen verhogen met het kenmerk &quot;hot&quot; als het werkelijke weer heet is. Om dit te doen, **contextData.weather=hot** werd overgegaan in de beslissingsvraag.

   ![](../assets/ranking-syntax.png)

1. Klik op **[!UICONTROL Save]**. Uw rangschikkingsformule wordt gecreeerd, kunt u het van de lijst selecteren om details te krijgen en het uit te geven of te schrappen.

   Het is nu klaar om te worden gebruikt in een besluit om in aanmerking komende aanbiedingen voor plaatsing in aanmerking te nemen (zie [Aanbiedingen selecteren in beslissingen configureren](../offer-activities/configure-offer-selection.md)).

   ![](../assets/ranking-formula-created.png)

## Voorbeelden van willekeurige formules {#ranking-formula-examples}

U kunt verschillende rangschikkingsformules naar wens maken. Hieronder volgen enkele voorbeelden.

<!--
Boost by offer ID

Boost the priority of an offer with the offer ID *xcore:personalized-offer:13d213cd4cb328ec* by 5.

**Ranking formula:**

```
if( offer._id = "xcore:personalized-offer:13d213cd4cb328ec", offer.rank.priority + 5, offer.rank.priority)
```

Change the offer priority based on a certain profile attribute

Set the offer priority to 30 for offer *xcore:personalized-offer:13d213cd4cb328ec* if the user lives in the city of Bondi.

**Ranking formula:**

```
if( offer._id = "xcore:personalized-offer:13d213cd4cb328ec" and homeAddress.city.equals("Bondi", false), 30, offer.rank.priority)
```

Boost multiple offers by offer ID based on the presence of a profile's segment membership

Boost the priority of offers based on whether the user is a member of a priority segment, which is configured as an attribute in the offer.

**Ranking formula:**

```
if( segmentMembership.get("ups").get(offer.characteristics.prioritySegmentId).status in (["realized","existing"]), offer.rank.priority + 10, offer.rank.priority)
```
-->

### Verhoog aanbiedingen met bepaald aanbiedingskenmerk op basis van profielkenmerk

Als het profiel in de stad woont die overeenkomt met het aanbod, dan verdubbelt de prioriteit voor alle aanbiedingen in die stad.

**Willekeurige formule:**

```
if( offer.characteristics.city = homeAddress.city, offer.rank.priority * 2, offer.rank.priority)
```

### Verhoog aanbiedingen waarbij de einddatum minder dan 24 uur is.

**Willekeurige formule:**

```
if( offer.selectionConstraint.endDate occurs <= 24 hours after now, offer.rank.priority * 3, offer.rank.priority)
```

### De aanbiedingen van de verhoging met bepaalde aanbiedingsattributen die op contextgegevens worden gebaseerd

Verhoog bepaalde aanbiedingen die op de contextgegevens worden gebaseerd die in de beslissingsvraag worden overgegaan. Als de `contextData.weather=hot` wordt overgegaan in de besluitvormingsvraag, de prioriteit van alle aanbiedingen met `attribute=hot` moet worden versterkt.

**Willekeurige formule:**

```
if (@{_xdm.context.additionalParameters;version=1}.weather.isNotNull()
and offer.characteristics.weather=@{_xdm.context.additionalParameters;version=1}.weather, offer.rank.priority + 5, offer.rank.priority)
```

Wanneer u de API voor besluitvorming gebruikt, worden de contextgegevens toegevoegd aan het profielelement in de aanvraaginstantie, zoals in het onderstaande voorbeeld.

**Fragment van aanvraaginstantie:**

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

### Verhoog de aanbiedingen op basis van de neiging van klanten om het aangeboden product te kopen

Als we twee gevallen van *CustomerAI* berekening van de koopkracht *travelInsurance* en *extraBaggage* voor een luchtvaartmaatschappij zal de volgende rangschikkingsformule de prioriteit ( met 50 punten ) verhogen van het aanbod dat specifiek is voor verzekeringen of bagage indien de klantennevenscore om dat product te kopen hoger is dan 90 .

Maar omdat elk *CustomerAI* instantie maakt een eigen object binnen het schema voor het uniforme profiel. Het is niet mogelijk de score dynamisch te selecteren op basis van het type aanbiedingsvorm. U moet dus de `if` instructies om eerst het type aanbiedingsvorm te controleren en de score vervolgens uit het desbetreffende profielveld te halen.

**Willekeurige formule:**

```
if ( offer.characteristics.propensityType = "extraBaggagePropensity" and _salesvelocity.CustomerAI.extraBaggagePropensity.score > 90, offer.rank.priority + 50,
    (
        if ( offer.characteristics.propensityType = "travelInsurancePropensity" and _salesvelocity.CustomerAI.insurancePropensity.score > 90, offer.rank.priority + 50, offer.rank.priority )
    )
)
```

Een betere oplossing is om de scores op te slaan in een array van het profiel. In het volgende voorbeeld worden verschillende populatiescore&#39;s gebruikt met behulp van een eenvoudige rangschikkingsformule. De verwachting is dat u een profielschema met een serie van scores hebt. In dit voorbeeld is de instantiekant *_verkoopsnelheid* en het profielschema bevat het volgende:

![](../assets/ranking-example-schema.png)

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

De aanbiedingen bevatten een kenmerk voor *propensityType* die overeenkomt met de categorie uit de scores:

![](../assets/ranking-example-propensityType.png)

Uw rangschikkingsformule kan dan de prioriteit van elk aanbod aan gelijke klanten plaatsen *propensityScore* voor *propensityType*. Als geen score wordt gevonden, gebruik de statische prioriteit op de aanbieding wordt geplaatst:

```
let score = (select _Individual_Scoring1 from _salesvelocity.individualScoring
             where _Individual_Scoring1.core.category.equals(offer.characteristics.propensityType, false)).head().core.propensityScore
in if(score.isNotNull(), score, offer.rank.priority)
```
