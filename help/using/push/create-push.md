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
source-git-commit: 994eac32591f4ca352d310bc06057bd20ea03886
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 1%

---

# Een pushmelding maken {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="Push message creation"
>abstract="Voeg uw pushbericht toe en begin het aan te passen met de verpersoonlijkingseditor."

## Maak de pushmelding tijdens een reis of campagne {#create}

Voer de onderstaande stappen uit om een pushmelding te maken:

>[!BEGINTABS]

>[!TAB  voeg een Duw aan een Reis ] toe

1. Open de reis en sleep een duwactiviteit van de sectie van Acties van het palet.

   ![](assets/push_create_1.png)

1. Verstrek basisinformatie over uw bericht (etiket, beschrijving, categorie), dan kies de berichtconfiguratie aan gebruik.

   ![](assets/push_create_2.png)

   >[!NOTE]
   >
   >Als u een pushmelding verzendt van een reis, kunt u de functie voor Send-Time optimalisatie voor Adobe Journey Optimizer gebruiken om de beste tijd te voorspellen voor het verzenden van het bericht om de betrokkenheid te maximaliseren op basis van de historische open en kliksnelheden. [ Leer hoe te met Optimalisering Send-Time ](../building-journeys/send-time-optimization.md) te werken

   Voor meer informatie over hoe te om een reis te vormen, verwijs naar [ deze pagina ](../building-journeys/journey-gs.md)

1. Klik in het scherm met de reisconfiguratie op de knop **[!UICONTROL Edit content]** om de pushinhoud te configureren. [ Ontwerp een duw- bericht ](design-push.md)

1. Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken of monsters nemen van invoergegevens die vanuit een CSV-/JSON-bestand zijn geüpload of die u handmatig hebt toegevoegd om een voorvertoning van de inhoud weer te geven.

1. Wanneer uw duw klaar is, voltooi de configuratie van uw [ reis ](../building-journeys/journey-gs.md) om het te verzenden.

   Om het gedrag van uw ontvangers door duw openingen en/of interactie te volgen, zorg ervoor dat de specifieke opties in de volgende sectie in de [ e-mailactiviteit ](../building-journeys/journeys-message.md) worden toegelaten.

>[!TAB  voeg een Duw aan een Campagne toe ]

1. Open het menu **[!UICONTROL Campaigns]** en klik op **[!UICONTROL Create campaign]** .

1. Selecteer het type campagne dat u wilt uitvoeren

   * **Gepland - Op de markt brengend**: voer onmiddellijk de campagne of op een gespecificeerde datum uit. Geplande campagnes zijn gericht op het verzenden van marketingberichten. Zij worden gevormd en uitgevoerd van het gebruikersinterface.

   * **API-teweeggebracht - Marketing/Transactioneel**: voer de campagne uit gebruikend een API vraag. API-getriggerde campagnes zijn gericht op het verzenden van marketingberichten of transactiemeldingen, d.w.z. berichten die worden verzonden na een actie van een individu: wachtwoordinstelling, winkelwagentje enz.

1. Bewerk in de sectie **[!UICONTROL Properties]** de items **[!UICONTROL Title]** en **[!UICONTROL Description]** van uw campagne.

1. Klik op de knop **[!UICONTROL Select audience]** om het doelpubliek in de lijst met beschikbare Adobe Experience Platform-soorten publiek te definiëren. [Meer informatie](../audience/about-audiences.md).

1. Kies in het veld **[!UICONTROL Identity namespace]** de naamruimte die u wilt gebruiken om de personen van het geselecteerde publiek te identificeren. [Meer informatie](../event/about-creating.md#select-the-namespace).

1. Kies in de sectie **[!UICONTROL Actions]** de **[!UICONTROL Push notification]** en selecteer of maak een nieuwe configuratie.

   Leer meer over de configuratie van de Duw in [ deze pagina ](push-configuration.md).

   ![](assets/push_create_3.png)

1. Klik op **[!UICONTROL Create experiment]** om uw inhoudexperiment te configureren en behandelingen te maken om de prestaties te meten en de beste optie voor uw doelgroep te identificeren. [Meer informatie](../content-management/content-experiment.md)

1. Campagnes worden ontworpen om op een specifieke datum of op een terugkomende frequentie worden uitgevoerd. Leer hoe te om **[!UICONTROL Schedule]** van uw campagne in [ te vormen deze sectie ](../campaigns/create-campaign.md#schedule).

1. Kies in het menu **[!UICONTROL Action triggers]** de **[!UICONTROL Frequency]** van uw pushmelding:

   * Eenmaal
   * Dagelijks
   * Wekelijks
   * Maandelijks

1. Klik in het scherm Campagneconfiguratie op de knop **[!UICONTROL Edit content]** om de inhoud van de push te configureren. [ Ontwerp een duw- bericht ](design-push.md)

1. Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken of monsters nemen van invoergegevens die vanuit een CSV-/JSON-bestand zijn geüpload of die u handmatig hebt toegevoegd om een voorvertoning van de inhoud weer te geven.

1. Wanneer uw duw klaar is, voltooi de configuratie van uw [ campagne ](../campaigns/create-campaign.md) om het te verzenden.

   Om het gedrag van uw ontvangers door duw openingen en/of interactie te volgen, zorg ervoor dat de specifieke opties in de volgende sectie in de [ campagne ](../campaigns/create-campaign.md) worden toegelaten.

>[!ENDTABS]

**Verwante onderwerpen**

* [Pushkanaal configureren](push-gs.md)
* [Een bericht toevoegen tijdens een rit](../building-journeys/journeys-message.md)

## Snelle leveringsmodus {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="Snelle leveringsmodus"
>abstract="Met de modus voor snelle levering kunt u snelle berichten verzenden via een pushkanaal naar een publieksgrootte van minder dan 30 MB."

De snelle leveringswijze is een [!DNL Journey Optimizer] toe:voegen-op die zeer snelle pushbericht toestaat die in grote volumes door campagnes verzenden.

Snelle levering wordt gebruikt wanneer de vertraging in berichtlevering zaken-kritiek is, wanneer u een dringende duwalarm op mobiele telefoons wilt verzenden, bijvoorbeeld een breekbericht aan gebruikers die uw nieuwskanaal app hebben geïnstalleerd.

Voor meer informatie over prestaties wanneer het gebruiken van Snelle leveringswijze, verwijs naar [ het productbeschrijving van Adobe Journey Optimizer ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).

### Vereisten {#prerequisites}

Snelle levering overseinen komt met de volgende vereisten:

* Snelle levering is alleen beschikbaar voor **[!UICONTROL Scheduled]** -campagnes en is niet beschikbaar voor API-gestuurde campagnes.
* In het pushbericht is geen personalisatie toegestaan.
* Het doelpubliek moet minder dan 30M profielen bevatten,
* U kunt tot 5 campagnes gelijktijdig uitvoeren gebruikend de Snelle leveringswijze.

### Modus Snelle levering activeren

1. Maak een pushmeldingscampagne en schakel de optie **[!UICONTROL Rapid delivery]** in.

   ![](assets/create-campaign-burst.png)

1. Vorm de berichtinhoud en selecteer het publiek om te richten. [ Leer hoe te om een campagne ](#create) tot stand te brengen

   >[!IMPORTANT]
   >
   >Zorg ervoor dat de inhoud van het bericht geen personalisatie omvat, en dat het publiek minder dan 30M profielen bevat.

1. Controleer en activeer uw campagne op de gebruikelijke manier. In de testmodus worden berichten niet verzonden via de snelle leveringsmodus.