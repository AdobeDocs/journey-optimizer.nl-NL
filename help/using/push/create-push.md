---
solution: Journey Optimizer
product: journey optimizer
title: Een pushmelding configureren
description: Meer informatie over het maken van een pushmelding in Journey Optimizer
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 97fa287d94efb7fb95817fc15268e736517cb629
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 2%

---

# Een pushmelding maken {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="Push message creation"
>abstract="Voeg uw pushbericht toe en begin het aan te passen met de verpersoonlijkingseditor."

U kunt pushmeldingen maken voor mobiele apparaten (iOS en Android) en webbrowsers. Deze pagina begeleidt u door het proces om een pushmelding in een reis of campagne op te zetten.

## Maak de pushmelding tijdens een reis of campagne {#create}

Voer de onderstaande stappen uit om een pushmelding te maken:

>[!BEGINTABS]

>[!TAB voeg een Duw aan een Reis  toe]

1. Open uw reis en sleep een **[!UICONTROL Action]** activiteit van de **[!UICONTROL Actions]** sectie van het palet. Leer meer over de [&#x200B; activiteit van de Actie &#x200B;](../building-journeys/journey-action.md).

   >[!IMPORTANT]
   >
   >Alle native kanalen die nu toegankelijk zijn via de activiteit Handeling, verouderde native kanaalactiviteiten zijn vervangen door de release van maart. Bestaande reizen die oudere handelingen bevatten, blijven functioneren zoals ze zijn: er is geen migratie vereist.

1. Selecteer **[!UICONTROL Push]** als actietype.

   ![](assets/push_create_1.png)

1. Voer een **[!UICONTROL Label]** in om uw handeling op het canvas van de reis te identificeren.

1. Klik op de knop **[!UICONTROL Configure action]**.

1. U wordt naar het tabblad **[!UICONTROL Actions]** geleid. Selecteer of maak van daaruit de pushconfiguratie die u wilt gebruiken. [Meer informatie](push-configuration.md)

   ![](assets/push_create_2.png)

1. Daarnaast:

   * U kunt afkapregels toepassen op uw pushactie door een regel te selecteren die is ingesteld in de vervolgkeuzelijst **[!UICONTROL Business rules]** . [Meer informatie](../conflict-prioritization/channel-capping.md)

   * Met de optie **[!DNL Send time optimization]** kunt u het beste tijdstip voorspellen waarop het bericht wordt verzonden om de betrokkenheid te maximaliseren op basis van geopende historie en kliksnelheden. [&#x200B; leer hoe &#x200B;](../building-journeys/send-time-optimization.md)

1. Gebruik **[!UICONTROL Rapid delivery mode]** om uw pushmelding in grote hoeveelheden te verzenden. [&#x200B; leer hoe &#x200B;](#rapid-delivery)

1. Selecteer de knop **[!UICONTROL Edit content]** en maak de gewenste inhoud. [Meer informatie](design-push.md)

1. Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken of monsters nemen van invoergegevens die vanuit een CSV-/JSON-bestand zijn geüpload of die u handmatig hebt toegevoegd om een voorvertoning van de inhoud weer te geven. [&#x200B; leer hoe &#x200B;](send-push.md)

1. Ga terug naar het reiscanvas. Indien nodig voltooit u de reisflow door extra handelingen of gebeurtenissen te slepen en neer te zetten. [Meer informatie](../building-journeys/about-journey-activities.md)

   >[!NOTE]
   >
   >Om het gedrag van uw ontvangers door duw openingen en/of interactie te volgen, zorg ervoor dat de specifieke opties in de volgende sectie in de [&#x200B; e-mailactiviteit &#x200B;](../building-journeys/journey-action.md) worden toegelaten.

Voor meer informatie over om een reis tot stand te brengen te vormen en te publiceren, verwijs naar [&#x200B; deze pagina &#x200B;](../building-journeys/journey-gs.md).

>[!TAB  voeg een Duw aan een Campagne toe ]

1. Open het menu **[!UICONTROL Campaigns]** en klik op **[!UICONTROL Create campaign]** .

1. Selecteer het type campagne dat u wilt uitvoeren

   * **Gepland - Op de markt brengend**: voer onmiddellijk de campagne of op een gespecificeerde datum uit. Geplande campagnes zijn gericht op het verzenden van marketingberichten. Zij worden gevormd en uitgevoerd van het gebruikersinterface.

   * **API-teweeggebracht - Marketing/Transactioneel**: voer de campagne uit gebruikend een API vraag. API-getriggerde campagnes zijn gericht op het verzenden van marketingberichten of transactiemeldingen, d.w.z. berichten die worden verzonden na een actie van een individu: wachtwoordinstelling, winkelwagentje enz.

1. Bewerk in de sectie **[!UICONTROL Properties]** de items **[!UICONTROL Title]** en **[!UICONTROL Description]** van uw campagne.

1. Klik op de knop **[!UICONTROL Select audience]** om het doelpubliek in de lijst met beschikbare Adobe Experience Platform-soorten publiek te definiëren. [Meer info](../audience/about-audiences.md).

1. Kies in het veld **[!UICONTROL Identity namespace]** de naamruimte die u wilt gebruiken om de personen van het geselecteerde publiek te identificeren. [Meer info](../event/about-creating.md#select-the-namespace).

1. Kies in de sectie **[!UICONTROL Actions]** de **[!UICONTROL Push notification]** en selecteer of maak een nieuwe configuratie.

   Leer meer over de Duw configuratie voor mobiel op [&#x200B; deze pagina &#x200B;](push-configuration.md) en voor Web op [&#x200B; deze pagina &#x200B;](push-configuration-web.md).

   ![](assets/push_create_3.png)

1. Klik op **[!UICONTROL Create experiment]** om uw inhoudexperiment te configureren en behandelingen te maken om de prestaties te meten en de beste optie voor uw doelgroep te identificeren. [Meer informatie](../content-management/content-experiment.md)

1. Campagnes worden ontworpen om op een specifieke datum of op een terugkomende frequentie worden uitgevoerd. Leer hoe te om **[!UICONTROL Schedule]** van uw campagne in [&#x200B; te vormen deze sectie &#x200B;](../campaigns/create-campaign.md#schedule).

1. Kies in het menu **[!UICONTROL Action triggers]** de **[!UICONTROL Frequency]** van uw pushmelding:

   * Eenmaal
   * Dagelijks
   * Wekelijks
   * Maandelijks

1. Klik in het scherm Campagneconfiguratie op de knop **[!UICONTROL Edit content]** om de inhoud van de push te configureren. [&#x200B; Ontwerp een duw- bericht &#x200B;](design-push.md)

1. Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken of monsters nemen van invoergegevens die vanuit een CSV-/JSON-bestand zijn geüpload of die u handmatig hebt toegevoegd om een voorvertoning van de inhoud weer te geven. [&#x200B; leer hoe &#x200B;](send-push.md)

1. Wanneer uw duw klaar is, voltooi de configuratie van uw [&#x200B; campagne &#x200B;](../campaigns/create-campaign.md) om het te verzenden.

   Om het gedrag van uw ontvangers door duw openingen en/of interactie te volgen, zorg ervoor dat de specifieke opties in de volgende sectie in de [&#x200B; campagne &#x200B;](../campaigns/create-campaign.md) worden toegelaten.

Voor meer informatie over om een campagne tot stand te brengen te vormen en te activeren, verwijs naar [&#x200B; deze pagina &#x200B;](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

**Verwante onderwerpen**

* [Pushkanaal configureren](push-gs.md)
* [Een bericht toevoegen tijdens een rit](../building-journeys/journey-action.md)

## Snelle leveringsmodus {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="Snelle leveringsmodus"
>abstract="Met de modus voor snelle levering kunt u snelle berichten verzenden via een pushkanaal naar een publieksgrootte van minder dan 30 MB."

De snelle leveringswijze is een [!DNL Journey Optimizer] toe:voegen-op die zeer snelle pushbericht toestaat die in grote volumes door campagnes verzenden.

Snelle levering wordt gebruikt wanneer de vertraging in berichtlevering zaken-kritiek is, wanneer u een dringende duwalarm op mobiele telefoons wilt verzenden, bijvoorbeeld een breekbericht aan gebruikers die uw nieuwskanaal app hebben geïnstalleerd.

Voor meer informatie over prestaties wanneer het gebruiken van Snelle leveringswijze, verwijs naar [&#x200B; het productbeschrijving van Adobe Journey Optimizer &#x200B;](https://helpx.adobe.com/nl/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

### Vereisten {#prerequisites}

Snelle levering overseinen komt met de volgende vereisten:

* Snelle levering is alleen beschikbaar voor **[!UICONTROL Scheduled]** -campagnes en is niet beschikbaar voor API-gestuurde campagnes.
* In het pushbericht is geen personalisatie toegestaan.
* Het doelpubliek moet minder dan 30M profielen bevatten,
* U kunt tot 5 campagnes gelijktijdig uitvoeren gebruikend de Snelle leveringswijze.

### Modus Snelle levering activeren

1. Maak een pushmeldingscampagne en schakel de optie **[!UICONTROL Rapid delivery]** in.

   ![](assets/create-campaign-burst.png)

1. Vorm de berichtinhoud en selecteer het publiek om te richten. [&#x200B; Leer hoe te om een campagne &#x200B;](#create) tot stand te brengen

   >[!IMPORTANT]
   >
   >Zorg ervoor dat de inhoud van het bericht geen personalisatie omvat, en dat het publiek minder dan 30M profielen bevat.

1. Controleer en activeer uw campagne op de gebruikelijke manier. In de testmodus worden berichten niet verzonden via de snelle leveringsmodus.