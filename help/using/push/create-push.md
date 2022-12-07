---
solution: Journey Optimizer
product: journey optimizer
title: Een pushmelding configureren
description: Meer informatie over het maken van een pushmelding in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 4%

---

# Een pushmelding maken {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="Push message creation"
>abstract="Voeg uw pushbericht toe en pas het aan met de Expressieeditor."

## Maak de pushmelding tijdens een reis of campagne {#create}

Voer de onderstaande stappen uit om een pushmelding te maken:

>[!BEGINTABS]

>[!TAB Een duwtje toevoegen aan een reis]

1. Open de reis en sleep een duwactiviteit van de sectie van Acties van het palet.

   ![](assets/push_create_1.png)

1. Verstrek basisinformatie over uw bericht (etiket, beschrijving, categorie), dan kies de berichtoppervlakte aan gebruik.

   ![](assets/push_create_2.png)

   >[!NOTE]
   >
   >Als u een pushmelding verzendt van een reis, kunt u de functie voor Send-Time optimalisatie voor Adobe Journey Optimizer gebruiken om de beste tijd te voorspellen voor het verzenden van het bericht om de betrokkenheid te maximaliseren op basis van de historische open en kliksnelheden. [Leer hoe u met SendTime Optimization werkt](../building-journeys/journeys-message.md#send-time-optimization)

   Voor meer informatie over hoe te om een reis te vormen, verwijs naar [deze pagina](../building-journeys/journey-gs.md)

1. Van het scherm van de reisconfiguratie, klik **[!UICONTROL Edit content]** om de pushinhoud te configureren. [Een pushmelding ontwerpen](design-push.md)

1. Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om een voorbeeld van de inhoud weer te geven en deze te testen.

1. Wanneer uw duw klaar is, voltooi de configuratie van uw [reis](../building-journeys/journey-gs.md) om het te verzenden.

   Als u het gedrag van de ontvangers wilt bijhouden via pushopeningen en/of interacties, moet u ervoor zorgen dat de toegewezen opties in de sectie Tekstspatiëring zijn ingeschakeld in het dialoogvenster [e-mailactiviteit](../building-journeys/journeys-message.md).

>[!TAB Een duwtje toevoegen aan een campagne]

1. Maak een nieuwe geplande of door API geactiveerde campagne, selecteer **[!UICONTROL Push notification]** als uw actie en kies **[!UICONTROL App surface]** te gebruiken. [Meer informatie over de pushconfiguratie](push-configuration.md).

   ![](assets/push_create_3.png)

1. Klik op **[!UICONTROL Create]**.

1. Van de **[!UICONTROL Properties]** sectie, uw campagne bewerken **[!UICONTROL Title]** en **[!UICONTROL Description]**.

   ![](assets/push_create_4.png)

1. Klik op de knop **[!UICONTROL Select audience]** om het publiek te bepalen om van de lijst van beschikbare segmenten van Adobe Experience Platform te richten. [Meer informatie](../segment/about-segments.md).

1. In de **[!UICONTROL Identity namespace]** , kiest u de naamruimte die u wilt gebruiken om de personen van het geselecteerde segment te identificeren. [Meer informatie](../event/about-creating.md#select-the-namespace).

   ![](assets/push_create_5.png)

1. Campagnes worden ontworpen om op een specifieke datum of op een terugkomende frequentie worden uitgevoerd. Leer hoe u de **[!UICONTROL Schedule]** van uw campagne in [deze sectie](../campaigns/create-campaign.md#schedule).

1. Van de **[!UICONTROL Action triggers]** kiest u de **[!UICONTROL Frequency]** van uw pushmelding:

   * Eenmaal
   * Dagelijks
   * Wekelijks
   * Maandelijks

1. Van het scherm van de campagneconfiguratie, klik **[!UICONTROL Edit content]** om de pushinhoud te configureren. [Een pushmelding ontwerpen](design-push.md)

1. Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om een voorbeeld van de inhoud weer te geven en deze te testen.

1. Wanneer uw duw klaar is, voltooi de configuratie van uw [campagne](../campaigns/create-campaign.md) om het te verzenden.

   Als u het gedrag van de ontvangers wilt bijhouden via pushopeningen en/of interacties, moet u ervoor zorgen dat de toegewezen opties in de sectie Tekstspatiëring zijn ingeschakeld in het dialoogvenster [campagne](../campaigns/create-campaign.md).

>[!ENDTABS]

**Verwante onderwerpen**

* [Pushkanaal configureren](push-gs.md)
* [Een bericht toevoegen in een journey](../building-journeys/journeys-message.md)

## Snelle leveringsmodus {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="Snelle leveringsmodus"
>abstract="Met de modus voor snelle levering kunt u snelle berichten verzenden via een pushkanaal naar een publieksgrootte van minder dan 30 MB."

De snelle leveringswijze, die vroeger als wijze van de Borst bij reizen wordt bekend, is een [!DNL Journey Optimizer] een invoegtoepassing waarmee via campagnes zeer snel pushberichten op grote volumes kunnen worden verzonden.

Snelle levering wordt gebruikt wanneer de vertraging in berichtlevering zaken-kritiek is, wanneer u een dringende duwalarm op mobiele telefoons wilt verzenden, bijvoorbeeld een breekbericht aan gebruikers die uw nieuwskanaal app hebben geïnstalleerd.

Voor meer informatie over prestaties bij gebruik van de modus Snelle levering raadpleegt u [Adobe Journey Optimizer-productbeschrijving](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).

### Vereisten {#prerequisites}

Snelle levering overseinen komt met de volgende vereisten:

* Snelle levering is beschikbaar voor **[!UICONTROL Scheduled]** alleen campagnes, en niet beschikbaar voor API-gestuurde campagnes;
* In het pushbericht is geen personalisatie toegestaan.
* Het doelpubliek moet minder dan 30M profielen bevatten,
* U kunt tot 5 campagnes gelijktijdig uitvoeren gebruikend de Snelle leveringswijze.

### Modus Snelle levering activeren

1. Maak een pushmeldingscampagne en schakel de optie **[!UICONTROL Rapid delivery]** optie.

![](assets/create-campaign-burst.png)

1. Vorm de berichtinhoud en selecteer het publiek om te richten. [Leer een campagne maken](#create)

   >[!IMPORTANT]
   >
   >Zorg ervoor dat de inhoud van het bericht geen personalisatie omvat, en dat het publiek minder dan 30M profielen bevat.

1. Controleer en activeer uw campagne op de gebruikelijke manier. In de testmodus worden berichten niet verzonden via de snelle leveringsmodus.