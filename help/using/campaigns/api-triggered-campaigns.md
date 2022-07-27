---
title: Campagnes activeren met API's
description: Leer hoe u campagnes kunt activeren met [!DNL Journey Optimizer] API's
hide: true
hidefromtoc: true
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 1%

---

# Campagnes activeren met API&#39;s {#trigger-campaigns}

## Informatie over API-gestuurde campagnes {#about}

>[!NOTE]
>
>De API voor het uitvoeren van interactieve berichten bevindt zich momenteel in de bètaversie, die vaak en zonder kennisgeving kan worden bijgewerkt.


Met [!DNL Journey Optimizer]kunt u campagnes maken en deze vervolgens aanroepen vanuit een extern systeem op basis van een gebruikerstrigger met behulp van de [Interactive Message Execution REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). Dit staat u toe om diverse operationele en transactionele overseinenbehoeften zoals wachtwoordterugstellen, het teken van OTP, onder andere te behandelen.

Hiervoor moet u eerst een API-getriggerde campagne in Journey Optimizer maken en vervolgens de uitvoering starten via een API-aanroep.

Beschikbare kanalen voor API-getriggerde campagnes zijn E-mail, SMS en Push berichten.

## Een API-gestuurde campagne maken {#create}

Het proces om API-teweeggebrachte campagnes te creëren blijft het zelfde als geplande campagnes, behalve voor de publieksselectie die in de API lading wordt uitgevoerd. Gedetailleerde informatie over het maken van een campagne is beschikbaar in [deze sectie](create-campaign.md).

Voer de volgende stappen uit om een API-gestuurde campagne te maken:

1. Maak een nieuwe campagne met de **[!UICONTROL API-triggered]** type.

1. Kies het kanaal en de kanaaloppervlakte om uw bericht te verzenden, dan klik **[!UICONTROL Create]**.

   ![](assets/api-triggered-type.png)

1. Specificeer een titel en een beschrijving voor de campagne, dan vorm het te verzenden bericht.

   ![](assets/api-triggered-properties.png)

   >[!NOTE]
   >
   >U kunt aanvullende gegevens doorgeven in de API-lading die u kunt gebruiken om uw bericht aan te passen. [Meer informatie](#contextual)

1. Geef de naamruimte op die moet worden gebruikt om de personen van het segment te identificeren.

1. De begin- en einddatum van de campagne configureren.

   Als u een specifieke begin en/of einddatum voor een campagne vormt, zal het niet buiten deze data worden uitgevoerd, en API vraag zal ontbreken als de campagne door APIs teweeggebracht wordt.

1. In de **[!UICONTROL cURL request]** van de **[!UICONTROL Campaign ID]** gebruiken in de API-payload.

   ![](assets/api-triggered-curl.png)

1. Klikken **[!UICONTROL Review to activate]** om te controleren dat uw campagne correct wordt gevormd, dan activeer het.

## Contextafhankelijke kenmerken gebruiken in door API&#39;s geactiveerde campagnes {#contextual}

Met API-getriggerde campagnes kunt u aanvullende gegevens doorgeven in de API-lading en deze gebruiken in de campagne om uw bericht aan te passen.

Neem dit voorbeeld, waar de klanten hun wachtwoord willen terugstellen, en u hen een wachtwoord wilt verzenden terugstellen URL die in een derdehulpmiddel wordt geproduceerd. Met API-getriggerde campagnes kunt u deze gegenereerde URL doorgeven in de API-lading en deze gebruiken in de campagne om deze toe te voegen aan het bericht.

>[!NOTE]
>
>In tegenstelling tot voor profielen geschikte gebeurtenissen, worden de contextuele gegevens die in de REST API worden doorgegeven, gebruikt voor eenmalige communicatie en niet opgeslagen tegen profiel. Als er geen naamruimte is gevonden, wordt er maximaal een profiel gemaakt met de naamruimtedetails.

Als u deze gegevens in uw campagnes wilt gebruiken, moet u ze doorgeven aan de API-payload en ze in uw bericht toevoegen met de Expressieeditor. Om dit te doen, gebruik `{{context.<contextualAttribute>}}` syntaxis, waarbij `<contextualAttribute>` moet overeenkomen met de naam van de variabele in de API-lading die de gegevens bevat die u wilt doorgeven.

De `{{context.<contextualAttribute>}}` syntaxis wordt alleen toegewezen aan een gegevenstype String.

![](assets/api-triggered-context.png)

>[!IMPORTANT]
>
>De `context.system` syntaxis is beperkt tot Adobe intern gebruik en mag niet worden gebruikt om contextuele kenmerken door te geven.
Let op: voorlopig is er geen contextueel kenmerk beschikbaar voor gebruik in het menu Linkerspoor. De attributen moeten direct in uw verpersoonlijkingsuitdrukking worden getypt, zonder controle die door wordt uitgevoerd [!DNL Journey Optimizer].

## De campagne uitvoeren {#execute}

Om een API-teweeggebrachte campagne uit te voeren, moet u eerst zijn identiteitskaart terugwinnen en het in de API lading overgaan. Om dit te doen, open de campagne, dan kopieer-kleef identiteitskaart van **[!UICONTROL cURL request]** sectie.

![](assets/api-triggered-id.png)

Vervolgens kunt u deze id in uw API-payload gebruiken om de campagne te starten. Zie de [Interactieve API-documentatie voor berichtuitvoering](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution) voor meer informatie .

Merk op dat als u een specifieke begin en/of einddatum toen het creëren van de campagne hebt gevormd, het niet buiten deze data zal worden uitgevoerd, en API vraag zal ontbreken.

>[!NOTE]
>
>In sommige gevallen moet u mogelijk transactieberichten verzenden naar profielen die niet in het systeem bestaan. Bijvoorbeeld als een onbekende gebruiker zich probeert aan te melden bij uw website. In dat geval wordt het corresponderende profiel automatisch gemaakt in Adobe Experience Platform, in het dialoogvenster **Gegevensset AJO Interactive Messaging Profile** dataset.

## Aanvullende bronnen

* [Aan de slag met campagnes](get-started-with-campaigns.md)
* [Een campagne maken](create-campaign.md)
* [Een campagne wijzigen of stoppen](modify-stop-campaign.md)
* [Campagne live-rapport](campaign-live-report.md)
* [Globaal verslag campagne voeren](campaign-global-report.md)
