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
mini-toc-levels: 1
source-git-commit: 342df0950622de1c4c246bf624d05843671e199f
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---


# Taken maken {#create-tasks}

>[!BEGINSHADEBOX]

**de documentatie van de Uitdagingen van de Loyalty:**

* [Aan de slag met Loyalty Challenges](get-started.md)
* [Toegang tot en beheer uitdagingen en taken](access-loyalty-challenges.md)
* [Uitdagingen maken](create-challenges.md)
* **creeer taken** {2 }︎ ◀ u hier **bent**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Deze eigenschap is momenteel in **privé bèta**. Leer meer over [&#x200B; beschikbaarheidslabels &#x200B;](../rn/releases.md#availability-labels).

De taken bepalen de specifieke acties of de mijlpalen die de klanten moeten voltooien om beloningen in een loyaliteitsuitdaging te verdienen. U kunt taaktypes, hoeveelheden, en productvereisten vormen om het in dienst nemen en gepersonaliseerde loyaliteitservaringen tot stand te brengen.

Elke taak vertegenwoordigt een meetbare actie die tot uitdagingsvoltooiing bijdraagt. De taken zijn herbruikbare componenten die onafhankelijk kunnen worden tot stand gebracht en dan aan één of meerdere uitdagingen worden toegevoegd, of direct binnen een uitdaging worden gecreeerd.

## Een taak maken {#create-task}

U kunt taken maken op basis van twee invoerpunten. Het configuratieproces is het zelfde ongeacht waar u begint.

>[!BEGINTABS]

>[!TAB  van de inventaris van Taken ]

Selecteer de tab **[!UICONTROL Tasks]** en selecteer **[!UICONTROL Create Task]** . Taken die zijn gemaakt op basis van de inventaris, worden opgeslagen en beschikbaar voor hergebruik voor meerdere uitdagingen.

![](assets/task-create-inventory.png)

>[!TAB  van binnen een uitdaging ]

Open een bestaande uitdaging of maak een nieuwe. Selecteer **[!UICONTROL Add task]** en klik op de knop **[!UICONTROL New]** . Taken die op deze manier worden gemaakt, worden automatisch toegevoegd aan uw taak en worden ook opgeslagen in de takenvoorraad voor hergebruik in andere uitdagingen.

![](assets/task-create-challenge.png)

>[!ENDTABS]

## Klantenactiviteit kiezen {#choose-activity}

Selecteer het type activiteit dat klanten moeten uitvoeren om deze taak te voltooien:

* **[!UICONTROL Purchase]**: Klanten moeten een of meer items aanschaffen om deze taak te voltooien
* **[!UICONTROL Spend]**: Klanten moeten een opgegeven bedrag besteden om deze taak te voltooien

Als u een activiteit wilt selecteren, klikt u op het pictogram **+** en selecteert u de activiteit van de klant die het beste aansluit bij uw resultaatdoelstellingen. Elk activiteitstype heeft specifieke configureerbare attributen om de taakvereisten verder te bepalen en te vormen.
![](assets/task-create-activity.png)

## De taakkenmerken definiëren {#define-attributes}

Configureer de taakkenmerken op basis van het geselecteerde type activiteit. Blader op de onderstaande tabbladen naar de beschikbare kenmerken voor elk type activiteit:

>[!BEGINTABS]

>[!TAB  Activiteit van de Aankoop ]

Beschikbare attributen voor **activiteiten van de Aankoop 0&rbrace;:**

* **[!UICONTROL Quantity]**: voer het aantal items in dat moet worden aangeschaft om deze taak te voltooien.
* **[!UICONTROL Eligible items & exclusions]**: Definieer items of itemgroepen die tellen voor voltooiing van de taak en items die dat niet doen. [&#x200B; Leer meer op in aanmerking komende punten en uitsluitingen &#x200B;](#eligible-items-exclusions)
* **[!UICONTROL Minimum spend value amount]**: stel een minimale aanschafwaarde in.
* **[!UICONTROL Maximum number of transactions]**: Beperk het aantal transacties dat kan worden gebruikt om de taak te voltooien.

![](assets/task-create-purchase.png)

>[!TAB  uitgaven activiteit ]

Beschikbare attributen voor **uitgaven** activiteiten:

* **[!UICONTROL Amount]**: voer het totale bedrag in dat nodig is om de taak te voltooien.
* **[!UICONTROL Eligible items & exclusions]**: Definieer items of itemgroepen die tellen voor voltooiing van de taak en items die dat niet doen. [&#x200B; Leer meer op in aanmerking komende punten en uitsluitingen &#x200B;](#eligible-items-exclusions)
* **[!UICONTROL Maximum number of transactions]**: geef op hoeveel transacties zijn toegestaan om te voldoen aan de vereisten voor uitgaven. U kunt dit kenmerk activeren via het parameterpictogram.

![](assets/task-create-spend.png)

>[!ENDTABS]

## In aanmerking komende items en uitsluitingen definiëren {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Voor zowel **Aankoop** als **besteedt** activiteiten, kunt u het **[!UICONTROL Eligible items & exclusions]** attribuut gebruiken om te bepalen welke punten en groepen verkiesbaar zijn en die worden uitgesloten. Dit staat u toe om specifieke producten, categorieën, of plaatsen te richten aan uw uitdagingsdoelstellingen.

U kunt bijvoorbeeld een bestedingstaak beperken tot specifieke productcategorieën of cadeaukaarten of promotionele items uitsluiten van het aftellen naar het voltooien van de taak.

![](assets/tasks-create-eligible.png)

* Als u in aanmerking komende items wilt definiëren, voert u specifieke item-id&#39;s, categorieën of doel-id&#39;s in, gescheiden door komma&#39;s in het veld **[!UICONTROL Eligible task purchases are limited to the following]** . Als u dit veld leeg laat, zijn alle aankopen standaard subsidiabel. U kunt ook `*` invoeren om alle aankopen expliciet in aanmerking te laten komen.

  Voorbeeld: `SKU001, SKU002, CategoryA`

* Als u items wilt uitsluiten van de taak, voert u specifieke item-id&#39;s, categorieën of doel-id&#39;s in het veld **[!UICONTROL The following are excluded from this task]** in.

  Voorbeeld: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`

## Taakeigenschappen definiëren {#define-task-properties}

Configureer in het taakvenster **[!UICONTROL Properties]** de basistaakgegevens:

* **[!UICONTROL Task name]**: voer een beschrijvende naam in voor de taak.
* **[!UICONTROL Task description]**: De beschrijving wordt automatisch gegenereerd op basis van de geconfigureerde activiteit en kenmerken. Als u een aangepaste beschrijving wilt invoeren, schakelt u de optie Automatisch genereren uit en voert u uw beschrijving in het tekstveld in.

![](assets/tasks-create-properties.png)

Nadat u alle kenmerken en eigenschappen hebt geconfigureerd, selecteert u **[!UICONTROL Create]** om de taak op te slaan. De taak wordt bewaard aan uw inventaris van Taken en, als gecreeerd van binnen een uitdaging, automatisch toegevoegd aan die uitdaging.
