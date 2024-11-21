---
title: Aan de slag met beslissing
description: Meer informatie over beslissingen
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 6b0735f619379e01e87012ba4300c0ec41334fd4
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---

# Aan de slag met beslissing {#get-started-experience-decisioning}

## Wat is beslissend? {#about}

Beslissing vereenvoudigt personalisering door een gecentraliseerde catalogus van marketing aanbiedingen aan te bieden die als &quot;beslissingspunten&quot;en een geavanceerd besluitvormingsmotor worden bekend. Deze motor hanteert regels en rangschikkingscriteria om de meest relevante beslissingsitems te selecteren en aan elk individu voor te leggen.

Deze besluitpunten zijn naadloos geïntegreerd in een brede waaier van binnenkomende oppervlakten door het [ nieuwe code-gebaseerde ervaringskanaal ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/code-based-experience/get-started-code-based), nu toegankelijk binnen de campagnes van Journey Optimizer. Beslissingsbeleid is beschikbaar voor gebruik in code-gebaseerde ervaringscampagnes slechts.

## Afbeeldingen en beperkingen {#guardrails}

Houd de volgende instructies en beperkingen in acht om een optimaal gebruik van beslissingsbevoegdheid te waarborgen:

### Algemene scharrelingen {#general}

* **de punten van de Aanbieding**: Elke puntinzameling kan tot 500 aanbiedingspunten bevatten.
* **de attributen van de Douane**: Een besluitpunt kan een maximum van 100 douaneattributen omvatten.
* **de strategieën van de Selectie &amp; besluitvormingspunten per beleid**: Een besluitvormingsbeleid steunt tot 10 gecombineerde selectiestrategieën en besluitvormingspunten.

### Subsidiabiliteitsregels {#eligibility}

* **het Nesten niveaus**: De het nesten diepte is beperkt tot 30 niveaus. Dit wordt gemeten door de `)` haakjes sluiten in de PQL-tekenreeks te tellen.
* **het koordgrootte van de Regel**: Een regelkoord kan tot 15KB in grootte voor UTF-8 gecodeerde karakters zijn. Dit komt overeen met 15.000 ASCII-tekens (1 byte elk) of 3.750-7.500 niet-ASCII-tekens (2-4 bytes elk).

### Beoordelingsformule {#ranking}

* **het Nesten niveaus**: De het nesten diepte is beperkt tot 30 niveaus. Dit wordt gemeten door de `)` haakjes sluiten in de PQL-tekenreeks te tellen.
* **grootte van het koord van de Formule**: Een regelkoord kan tot 8KB in grootte voor UTF-8 gecodeerde karakters zijn. Dit komt overeen met 8.000 ASCII-tekens (1 byte elk) of 2.000-4.000 niet-ASCII-tekens (2-4 bytes elk).

## Belangrijke stappen voor besluitvorming {#steps}

De belangrijkste stappen om met Beslissing te werken zijn als volgt:

1. **wijs juiste toestemmingen** toe. Beslissingen zijn alleen beschikbaar voor gebruikers met toegang tot een besluit dat betrekking heeft op **[!UICONTROL role]** , zoals Beslissingsmanagers. Als u geen toegang hebt tot Beslissing, moeten uw toestemmingen worden uitgebreid.

   +++Leer hoe u de rol van beslissingsmanagers toewijst

   1. Als u een rol wilt toewijzen aan een gebruiker in het [!DNL Permissions] -product, navigeert u naar het tabblad **[!UICONTROL Roles]** en selecteert u Beslissingsmanagers.

      ![](assets/decision_permission_1.png)

   1. Klik op het tabblad **[!UICONTROL Users]** op **[!UICONTROL Add user]**.

      ![](assets/decision_permission_2.png)

   1. Typ de naam of het e-mailadres van de gebruiker of selecteer de gebruiker in de lijst en klik op **[!UICONTROL Save]** .

      Als de gebruiker niet eerder werd gecreeerd, verwijs naar [ gebruikersdocumentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/users) toevoegen.

      ![](assets/decision_permission_3.png)

   Uw gebruiker moet dan een e-mail ontvangen die aan uw instantie opnieuw richt.

+++

1. **vorm douanekenmerken**: Tailor de puntcatalogus aan uw specifieke vereisten door opstellingsdouaneattributen in het schema van de catalogus.

   ➡️ [ leren hoe te om de puntcatalogus ](catalogs.md) te vormen

1. **creeer besluitpunten** om aan uw gericht publiek te tonen.

   ➡️ [ leren hoe te om beslissende punten ](items.md) tot stand te brengen ([ API documentatie ](api-reference/decisions-items/create.md))

1. **organiseert zich met inzamelingen**: De inzamelingen van het gebruik om besluitpunten te categoriseren die op op attribuut-gebaseerde regels worden gebaseerd. Neem inzamelingen in uw selectiestrategieën op om te bepalen welke inzameling van besluitvormingspunten zou moeten worden overwogen.

   ➡️ [ leren hoe te om puntinzamelingen ](collections.md) te beheren ([ API documentatie ](api-reference/items-collections/create.md))

1. **creeer besluitvormingsregels**: De regels van het besluit worden gebruikt in besluitvormingspunten en/of selectiestrategieën om te bepalen aan wie een besluitpunt kan worden getoond.

   ➡️ [ leren hoe te om besluitvormingsregels tot stand te brengen ](rules.md)

1. **voert het rangschikken methodes** uit: Creeer het rangschikken methodes en pas hen binnen besluitvormingsstrategieën toe om de prioritaire orde te bepalen om besluitpunten te selecteren.

   ➡️ [ leren hoe te om het rangschikken methodes ](ranking.md) tot stand te brengen

1. **creeer selectiestrategieën**: Bouw selectiestrategieën die hefboominzamelingen, besluitvormingsregels, en het rangschikken methodes om de besluitpunten te identificeren geschikt voor het tonen aan profielen.

   ➡️ [ leren hoe te om selectiestrategieën ](selection-strategies.md) tot stand te brengen ([ API documentatie ](api-reference/selection-strategies/create.md))

1. **creeer een besluitvormingsbeleid en bedt het in uw op code-gebaseerde campagne** in: Het beleid van het besluit combineert veelvoudige selectiestrategieën om de in aanmerking komende besluitpunten te bepalen om aan het voorgenomen publiek te tonen.

   ➡️ [ leren hoe te met besluitvormingsbeleid ](create-decision.md) te werken
