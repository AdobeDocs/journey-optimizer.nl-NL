---
solution: Journey Optimizer
product: journey optimizer
title: Taken maken voor loyaliteitsuitdagingen
description: Leer hoe u taken voor loyaliteitsuitdagingen in Adobe Journey Optimizer kunt maken en configureren.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private bèta" type="Informative"
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---


# Taken maken {#create-tasks}

>[!BEGINSHADEBOX]

**de documentatie van de Uitdagingen van de Loyalty:**

* [&#x200B; wordt begonnen met de Uitdagingen van de Loyalty &#x200B;](get-started.md) - Overzicht, werkschema, eerste vereisten
* [&#x200B; toegang en beheer de Uitdagingen van de Loyalty &#x200B;](access-loyalty-challenges.md) - Overzicht, uitdagingen en taakbeheer
* [&#x200B; creeer uitdagingen &#x200B;](create-challenges.md) - bouw en vorm uitdagingen
* **creeer taken** {2 }︎ ◀ u hier **bent - bepaal uitdagingstaken**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Deze eigenschap is momenteel in **privé bèta** en kan niet in uw milieu beschikbaar zijn. Neem contact op met uw Adobe-vertegenwoordiger als u toegang wilt aanvragen. Leer meer over [&#x200B; beschikbaarheidslabels &#x200B;](../rn/releases.md#availability-labels).

De taken bepalen de specifieke acties of de mijlpalen die de klanten moeten voltooien om beloningen in een loyaliteitsuitdaging te verdienen. U kunt taaktypes, hoeveelheden, en productvereisten vormen om het in dienst nemen en gepersonaliseerde loyaliteitservaringen tot stand te brengen.

Elke taak vertegenwoordigt een meetbare actie die tot uitdagingsvoltooiing bijdraagt. De taken zijn herbruikbare componenten die onafhankelijk kunnen worden tot stand gebracht en dan aan één of meerdere uitdagingen worden toegevoegd, of direct binnen een uitdaging worden gecreeerd.

## Een taak maken {#create-task}

U kunt taken maken op basis van twee invoerpunten. Het configuratieproces is het zelfde ongeacht waar u begint.

>[!BEGINTABS]

>[!TAB  van de inventaris van Taken ]

Selecteer de tab **[!UICONTROL Tasks]** en selecteer **[!UICONTROL Create Task]** .

![](assets/task-create-inventory.png)

Taken die zijn gemaakt op basis van de inventaris, worden opgeslagen en beschikbaar voor hergebruik voor meerdere uitdagingen.

>[!TAB  van binnen een uitdaging ]

Open een bestaande uitdaging of maak een nieuwe. Selecteer **[!UICONTROL Add task]** en klik op de knop **[!UICONTROL New]** .

![](assets/task-create-challenge.png)

Taken die op deze manier worden gemaakt, worden automatisch toegevoegd aan uw taak en worden ook opgeslagen in de takenvoorraad voor hergebruik in andere uitdagingen.

>[!ENDTABS]

## Klantenactiviteit kiezen {#choose-activity}

Selecteer het type activiteit dat klanten moeten uitvoeren om deze taak te voltooien:

* **[!UICONTROL Purchase]**: Klanten moeten een of meer items aanschaffen om deze taak te voltooien
* **[!UICONTROL Spend]**: Klanten moeten een opgegeven bedrag besteden om deze taak te voltooien

Als u een type activiteit wilt selecteren, klikt u op het pictogram `+` en selecteert u de activiteit van de klant die het beste aansluit bij uw resultaatdoelstellingen. Elk activiteitstype heeft specifieke configureerbare attributen om de taakvereisten verder te bepalen en te vormen.

![](assets/task-create-activitiy.png)

## Kenmerken definiëren {#define-attributes}

Configureer de taakkenmerken op basis van het geselecteerde type activiteit:

>[!BEGINTABS]

>[!TAB  Activiteit van de Aankoop ]

![](assets/task-create-purchase.png)

Configureer de volgende kenmerken:

* **[!UICONTROL Quantity]**: voer het aantal items in dat moet worden aangeschaft om deze taak te voltooien
* **[!UICONTROL Eligible items & exclusions]**: Definieer items of itemgroepen die tellen voor voltooiing van de taak en items die dat niet doen. Leer meer over [&#x200B; het bepalen van in aanmerking komende punten en uitsluitingen &#x200B;](#eligible-items-exclusions)

**Facultatieve attributen** (geactiveerd via het parameterpictogram):

* **[!UICONTROL Minimum spend value amount]**: een vereiste voor een minimaal aankoopbedrag instellen
* **[!UICONTROL Maximum number of transactions]**: Beperk het aantal transacties dat kan worden gebruikt om de taak te voltooien

>[!TAB  uitgaven activiteit ]

![](assets/task-create-spend.png)

Configureer de volgende kenmerken:

* **[!UICONTROL Amount]**: voer het totale bedrag in dat nodig is om de taak te voltooien.
* **[!UICONTROL Maximum number of transactions]**: geef op hoeveel transacties zijn toegestaan om te voldoen aan de vereisten voor uitgaven. U kunt dit kenmerk deactiveren via het parameterpictogram als u het aantal transacties niet wilt beperken.
* **[!UICONTROL Eligible items & exclusions]**: (Optioneel) Definieer items of itemgroepen die tellen voor het voltooien van taken en items die dat niet doen. Leer meer over [&#x200B; het bepalen van in aanmerking komende punten en uitsluitingen &#x200B;](#eligible-items-exclusions)

>[!ENDTABS]

## In aanmerking komende items en uitsluitingen definiëren {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Voor zowel **Aankoop** als **besteedt** activiteiten, kunt u het **[!UICONTROL Eligible items & exclusions]** attribuut gebruiken om te bepalen welke punten en groepen verkiesbaar zijn en die worden uitgesloten. Dit staat u toe om specifieke producten, categorieën, of plaatsen te richten aan uw uitdagingsdoelstellingen.

De gevallen van het gebruik omvatten: het beperken van een bestedingstaak tot specifieke productcategorieën, of het uitsluiten van geschenkkaarten of promotionele punten van het tellen naar taakvoltooiing.

![](assets/tasks-create-eligible.png)

* Gebruik de sectie **[!UICONTROL Eligible task purchases are limited to the following]** om in aanmerking komende items te definiëren. Voer specifieke item-id&#39;s, categorieën of doel-id&#39;s in, gescheiden door komma&#39;s.

  Voorbeeld: `SKU001, SKU002, CategoryA`

  Voer `*` in om alle aankopen subsidiabel te maken (standaardgedrag indien leeg).

* Gebruik de sectie **[!UICONTROL The following are excluded from this task]** om items uit te sluiten van de taak. Voer specifieke item-id&#39;s, categorieën of doel-id&#39;s in die niet moeten worden meegerekend voor het voltooien van de taak.

  Voorbeeld: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`

  >[!NOTE]
  >
  >Uitsluitingen hebben voorrang op in aanmerking komende items. Als een item overeenkomt met zowel een in aanmerking komend als een uitgesloten item, wordt het van de taak uitgesloten.

## Taakeigenschappen definiëren {#define-task-properties}

Configureer in het taakvenster **[!UICONTROL Properties]** de basistaakgegevens:

* **[!UICONTROL Task name]**: voer een beschrijvende naam in voor de taak. Deze naam is zichtbaar voor u en uw team, maar wordt mogelijk niet weergegeven aan klanten, afhankelijk van het ontwerp van uw inhoudskaart.
* **[!UICONTROL Task description]**: De beschrijving wordt automatisch gegenereerd op basis van het type activiteit en de kenmerken die u voor de taak configureert. U kunt automatisch genereren uitschakelen en desgewenst een aangepaste beschrijving invoeren.

![](assets/tasks-create-properties.png)

Nadat u alle kenmerken en eigenschappen hebt geconfigureerd, selecteert u **[!UICONTROL Create]** om de taak op te slaan. De taak wordt bewaard aan uw inventaris van Taken en, als gecreeerd van binnen een uitdaging, automatisch toegevoegd aan die uitdaging.
