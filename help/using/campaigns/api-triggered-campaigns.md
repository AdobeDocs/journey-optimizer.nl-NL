---
solution: Journey Optimizer
product: journey optimizer
title: Campagnes activeren met API's
description: Leer hoe u campagnes kunt activeren met Journey Optimizer API's
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagnes, API-geactiveerd, REST, optimizer, berichten
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 0%

---

# Campagnes activeren met API&#39;s {#trigger-campaigns}

## Informatie over API-gestuurde campagnes {#about}

Met [!DNL Journey Optimizer]kunt u campagnes maken en deze vervolgens aanroepen vanuit een extern systeem op basis van een gebruikerstrigger met behulp van de [Interactive Message Execution REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). Dit staat u toe om diverse marketing en transactionele overseinenbehoeften zoals wachtwoordterugstellen, het teken van OTP, onder andere te behandelen.

Hiervoor moet u eerst een API-getriggerde campagne in Journey Optimizer maken en vervolgens de uitvoering starten via een API-aanroep.

![](../rn/assets/do-not-localize/api-triggered.gif)

Beschikbare kanalen voor API-getriggerde campagnes zijn E-mail, SMS en Push berichten.

>[!NOTE]
>
>Vanaf nu wordt de snelle leveringsmodus niet ondersteund voor door de pushmelding API-geactiveerde campagnes.

➡️ [Deze functie in video detecteren](#video)

## Een API-gestuurde campagne maken {#create}

### De campagne configureren en activeren {#create-activate}

Voer de onderstaande stappen uit om een API-gestuurde campagne te maken. Gedetailleerde informatie over het maken van een campagne is beschikbaar in [deze sectie](create-campaign.md).

1. Maak een nieuwe campagne met de **[!UICONTROL API-triggered]** type.

1. Kies de optie **[!UICONTROL Marketing]** of **[!UICONTROL Transactional]** afhankelijk van het type communicatie dat u wilt verzenden.

1. Kies een van de ondersteunde kanalen en het bijbehorende kanaaloppervlak voor het verzenden van uw bericht en klik op **[!UICONTROL Create]**.

   ![](assets/api-triggered-type.png)

1. Geef een titel en een beschrijving voor de campagne op en klik vervolgens op **[!UICONTROL Edit content]** om het te verzenden bericht te vormen.

   >[!NOTE]
   >
   >U kunt aanvullende gegevens doorgeven in de API-lading die u kunt gebruiken om uw bericht aan te passen. [Meer informatie](#contextual)
   >
   >Het gebruik van een groot aantal of zware contextafhankelijke gegevens in uw inhoud kan van invloed zijn op de prestaties.

1. In de **[!UICONTROL Audience]** in, geeft u de naamruimte op die moet worden gebruikt om de personen te identificeren.

   * Als u een **transactie**-type campagne, moeten de gerichte profielen in de API vraag worden bepaald. De **[!UICONTROL Create new profiles]** kunt u automatisch profielen maken die niet in de database voorkomen. [Meer informatie over het maken van profielen tijdens de uitvoering van de campagne](#profile-creation)

   * Voor **marketing**-type campagnes, klik **[!UICONTROL Audience]** om het publiek te kiezen waarop u zich wilt richten.

1. De begin- en einddatum van de campagne configureren.

   Als u een specifieke begin en/of einddatum voor een campagne vormt, zal het niet buiten deze data worden uitgevoerd, en API vraag zal ontbreken als de campagne door APIs teweeggebracht wordt.

1. Klikken **[!UICONTROL Review to activate]** om te controleren dat uw campagne correct wordt gevormd, dan activeer het.

U kunt de campagne nu uitvoeren vanuit de API&#39;s. [Meer informatie](#execute)

### De campagne uitvoeren {#execute}

Nadat de campagne is geactiveerd, moet u het gegenereerde voorbeeld-cURL-verzoek ophalen en deze in de API gebruiken om de payload te bouwen en de campagne te starten.

1. Open de campagne en kopieer vervolgens het laadverzoek van de **[!UICONTROL cURL request]** sectie. Deze nuttige lading omvat alle verpersoonlijkings (profiel en context) variabelen die in het bericht worden gebruikt. Het is beschikbaar zodra de campagne live is.

   ![](assets/api-triggered-curl.png)

1. Gebruik dit cURL-verzoek in de API&#39;s om de payload te bouwen en de campagne te starten. Raadpleeg voor meer informatie de [Interactieve API-documentatie voor berichtuitvoering](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).


   Voorbeelden van API-aanroepen zijn ook beschikbaar in [deze pagina](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).

   >[!NOTE]
   >
   >Als u een specifieke begin en/of einddatum toen het creëren van de campagne hebt gevormd, zal het niet buiten deze data worden uitgevoerd, en API vraag zal ontbreken.

## Contextafhankelijke kenmerken gebruiken in door API&#39;s geactiveerde campagnes {#contextual}

Met API-getriggerde campagnes kunt u aanvullende gegevens doorgeven in de API-lading en deze gebruiken in de campagne om uw bericht aan te passen.

Neem dit voorbeeld, waar de klanten hun wachtwoord willen terugstellen, en u hen een wachtwoord wilt verzenden terugstellen URL die in een derdehulpmiddel wordt geproduceerd. Met API-getriggerde campagnes kunt u deze gegenereerde URL doorgeven in de API-lading en deze gebruiken in de campagne om deze toe te voegen aan het bericht.

>[!NOTE]
>
>In tegenstelling tot voor profielen geschikte gebeurtenissen, worden de contextuele gegevens die in de REST API worden doorgegeven, gebruikt voor eenmalige communicatie en niet opgeslagen tegen profiel. Als er geen naamruimte is gevonden, wordt er maximaal een profiel gemaakt met de naamruimtedetails.

Om deze gegevens in uw campagnes te gebruiken, moet u hen in de API lading overgaan, en hen toevoegen in uw bericht gebruikend de verpersoonlijkingsredacteur. Om dit te doen, gebruik `{{context.<contextualAttribute>}}` syntaxis, waarbij `<contextualAttribute>` moet overeenkomen met de naam van de variabele in de API-lading die de gegevens bevat die u wilt doorgeven.

De `{{context.<contextualAttribute>}}` syntaxis wordt alleen toegewezen aan een gegevenstype String.

![](assets/api-triggered-context.png)


>[!IMPORTANT]
>
>De contextafhankelijke kenmerken die in de aanvraag worden doorgegeven, mogen niet groter zijn dan 50 kB en zijn altijd van het type tekenreeks.
>
>De `context.system` syntaxis is beperkt tot Adobe intern gebruik en mag niet worden gebruikt om contextafhankelijke kenmerken door te geven.

Let op: voorlopig is er geen contextueel kenmerk beschikbaar voor gebruik in het menu Linkerspoor. De attributen moeten direct in uw verpersoonlijkingsuitdrukking worden getypt, zonder controle die door [!DNL Journey Optimizer].

## Profiel maken tijdens uitvoering van de campagne {#profile-creation}

In sommige gevallen moet u mogelijk transactieberichten verzenden naar profielen die niet in het systeem bestaan. Bijvoorbeeld als een onbekende gebruiker het wachtwoord op uw website opnieuw probeert in te stellen.

Wanneer een profiel niet in de database bestaat, kunt u het door Journey Optimizer automatisch maken tijdens het uitvoeren van de campagne om het verzenden van het bericht naar dit profiel toe te staan.

>[!IMPORTANT]
>
>In het geval van transactieberichten, wordt deze eigenschap verstrekt **zeer kleine profielcreatie** in een grote transactie die gebruikscase verzendt, met het grootste deel van profielen reeds bestaand in platform.

Als u het maken van profielen wilt activeren tijdens de uitvoering van de campagne, schakelt u het **[!UICONTROL Create new profiles]** in de **[!UICONTROL Audience]** sectie. Als deze optie is uitgeschakeld, worden onbekende profielen voor verzending geweigerd en mislukt de API-aanroep.

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>Onbekende profielen worden gemaakt in het dialoogvenster **Gegevensset AJO Interactive Messaging Profile** dataset, in drie standaardnaamruimte (e-mail, telefoon en ECID) respectievelijk voor elke uitgaande kanalen (E-mail, SMS en Push). Als u echter een aangepaste naamruimte gebruikt, wordt de identiteit gemaakt met dezelfde aangepaste naamruimte.

## Hoe kan ik-video {#video}

Leer hoe te om een campagne tot stand te brengen en het van een extern systeem teweeg te brengen dat op gebruikersinteractie wordt gebaseerd, gebruikend de Interactieve REST API van de Uitvoering van het Bericht.

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)
