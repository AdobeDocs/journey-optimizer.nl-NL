---
solution: Journey Optimizer
product: journey optimizer
title: Een LIJNbericht maken
description: Leer hoe u een LINE-bericht maakt in Journey Optimizer
feature: Line
topic: Content Management
role: User
level: Beginner
exl-id: a93d4dc9-f0e9-400c-b9a4-6cdac84390fd
source-git-commit: 12dbe0031e9037d879e0d2309c7c26cc3c00cc4e
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 2%

---

# Een LIJNbericht maken {#create-line}

## Een LIJNbericht toevoegen {#create-line-journey-campaign}

Blader op de onderstaande tabbladen om te leren hoe u een LINE-bericht kunt toevoegen aan een campagne of een reis.

>[!BEGINTABS]

>[!TAB voeg een bericht van de LIJN aan een Reis  toe]

1. Open uw reis dan belemmering en laat vallen a **LIJN** activiteit van de **sectie van Acties** van het palet.

   ![](assets/jo-line-1.png)

1. Verstrek basisinformatie over uw bericht (etiket, beschrijving, categorie), dan kies de berichtconfiguratie aan gebruik.

   Voor meer informatie over hoe te om een reis te vormen, verwijs naar [&#x200B; deze pagina &#x200B;](../building-journeys/journey-gs.md)

   Het veld **[!UICONTROL configuration]** wordt standaard voorgevuld met de laatste configuratie die de gebruiker voor dat kanaal heeft gebruikt.

U kunt nu de inhoud van uw SMS-bericht ontwerpen via de knop **[!UICONTROL Edit content]** , zoals hieronder wordt beschreven.

>[!TAB  voeg een bericht van de LIJN aan een Campagne toe ]

1. Open het menu **[!UICONTROL Campaigns]** en klik op **[!UICONTROL Create campaign]** .

1. Selecteer het type campagne dat u wilt uitvoeren

   * **Gepland - Op de markt brengend**: voer onmiddellijk de campagne of op een gespecificeerde datum uit. Geplande campagnes zijn gericht op het verzenden van marketingberichten. Zij worden gevormd en uitgevoerd van het gebruikersinterface.

   * **API-teweeggebracht - Marketing/Transactioneel**: voer de campagne uit gebruikend een API vraag. API-getriggerde campagnes zijn gericht op het verzenden van marketingberichten of transactiemeldingen, d.w.z. berichten die worden verzonden na een actie van een individu: wachtwoordinstelling, winkelwagentje enz.

1. Bewerk in de sectie **[!UICONTROL Properties]** de items **[!UICONTROL Title]** en **[!UICONTROL Description]** van uw campagne.

1. Klik op de knop **[!UICONTROL Select audience]** om het doelpubliek in de lijst met beschikbare Adobe Experience Platform-soorten publiek te definiëren. [Meer informatie](../audience/about-audiences.md).

1. Kies in het veld **[!UICONTROL Identity namespace]** de naamruimte die u wilt gebruiken om de personen van het geselecteerde publiek te identificeren. [Meer informatie](../event/about-creating.md#select-the-namespace).

1. Kies in de sectie **[!UICONTROL Actions]** de **[!UICONTROL LINE]** en selecteer of maak een nieuwe configuratie.

   Leer meer over de configuratie van de LIJN in [&#x200B; deze pagina &#x200B;](line-configuration.md).

   ![](assets/campaign-line-1.png)

1. Klik op **[!UICONTROL Create experiment]** om uw inhoudexperiment te configureren en behandelingen te maken om de prestaties te meten en de beste optie voor uw doelgroep te identificeren. [Meer informatie](../content-management/content-experiment.md)

1. Geef in de sectie **[!UICONTROL Actions tracking]** op of u wilt bijhouden of er op koppelingen in uw SMS-bericht wordt geklikt.

1. Campagnes worden ontworpen om op een specifieke datum of op een terugkomende frequentie worden uitgevoerd. Leer hoe te om **[!UICONTROL Schedule]** van uw campagne in [&#x200B; te vormen deze sectie &#x200B;](../campaigns/create-campaign.md#schedule).

1. Kies in het menu **[!UICONTROL Action triggers]** de **[!UICONTROL Frequency]** van uw SMS-bericht:

   * Eenmaal
   * Dagelijks
   * Wekelijks
   * Maand

U kunt nu de inhoud van uw tekstbericht ontwerpen via de knop **[!UICONTROL Edit content]** , zoals hieronder wordt beschreven.

>[!ENDTABS]

## Regelinhoud definiëren{#line-content}

Adobe Journey Optimizer ondersteunt de volgende berichttypen voor LINE:

* **Tekst**: Verzend duidelijke of geformatteerde tekstberichten.
* **Stickers**: Bouw inheemse stickers van de LIJN op om karakter en uitdrukkingskracht toe te voegen.
* **Beelden**: Maak beelden vast om visueel beroep te verbeteren.
* **Video&#39;s**: Deel videoinhoud voor dynamische mededeling.
* **Plaatsen**: Verzend plaatsinformatie met kaarten.
* **Malplaatjes**: Gebruik vooraf bepaalde malplaatjes voor verenigbaar overseinen.
* **de Berichten van Flex**: Creeer complexe lay-outs met rijke inhoud gebruikend op JSON-Gebaseerde Berichten van Flex.

Deze berichttypes kunnen worden gevormd door de inhoud te uitgeven JSON direct, toestaand voor dynamische en gepersonaliseerde overseinenstrategieën.

Volg onderstaande stappen om uw LIJNinhoud te configureren.

1. Klik in het configuratiescherm van de reis of campagne op de knop **[!UICONTROL Edit content]** om de inhoud van het tekstbericht te configureren.

1. Klik op **[!UICONTROL Edit code]** om JSON-inhoud te bewerken.

1. Gebruik de verpersoonlijkingsredacteur om inhoud te bepalen, verpersoonlijking en dynamische inhoud toe te voegen. U kunt elk kenmerk gebruiken, bijvoorbeeld de profielnaam of plaats. U kunt ook voorwaardelijke regels definiëren. Blader naar de volgende pagina&#39;s om meer over [&#x200B; verpersoonlijking &#x200B;](../personalization/personalize.md) en [&#x200B; dynamische inhoud &#x200B;](../personalization/get-started-dynamic-content.md) in de verpersoonlijkingsredacteur te leren.

1. Klik op **[!UICONTROL Save]** en controleer uw bericht in de voorvertoning.

1. Gebruik de knop **[!UICONTROL Simulate content]** om een voorvertoning weer te geven van de inhoud van uw lijnbericht en de inhoud van uw persoonlijke gegevens.

Nadat u de tests hebt uitgevoerd en de inhoud hebt gevalideerd, kunt u het LINE-bericht naar het publiek sturen. Deze stappen zijn gedetailleerd in [&#x200B; deze pagina &#x200B;](send-line.md)

Zodra verzonden, kunt u het effect van uw LIJN binnen de Campagne of rapporten van de Reis meten. Raadpleeg [deze sectie](../reports/campaign-global-report-cja.md) voor meer informatie over rapporten.
