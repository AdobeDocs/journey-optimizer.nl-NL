---
solution: Journey Optimizer
product: journey optimizer
title: Integreren met Adobe Campaign Standard
description: Leer hoe u Journey Optimizer kunt integreren met Adobe Campaign Standard
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Engineer, Admin
level: Intermediate
keywords: campagne, standaard, integratie, plafonnering, actie
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# Integreren met Adobe Campaign Standard {#using_adobe_campaign_standard}

Als u Adobe Campaign Standard hebt, is er een ingebouwde actie beschikbaar waarmee u verbinding kunt maken met Adobe Campaign Standard. U kunt e-mails, pushberichten en SMS verzenden met de mogelijkheden voor Transactieberichten van Adobe Campaign Standard.

Het Campaign Standard-transactiebericht en de bijbehorende gebeurtenis moeten worden gepubliceerd om in Journey Optimizer te kunnen worden gebruikt. Als de gebeurtenis wordt gepubliceerd maar het bericht niet is, is het niet zichtbaar in de interface van Journey Optimizer. Als het bericht wordt gepubliceerd maar zijn bijbehorende gebeurtenis niet, zal het in de interface van Journey Optimizer zichtbaar zijn maar het zal niet bruikbaar zijn.

## Afvoerkanalen en beperkingen {#important-notes}

* Voor Adobe Campaign Standard-acties wordt automatisch een afluisterregel van 4.000 aanroepen per 5 minuten gedefinieerd. Lees meer over transactionele overseinen SLAs in [ de Beschrijving van het Product van Adobe Campaign Standard ](https://helpx.adobe.com/nl/legal/product-descriptions/campaign-standard.html){target="_blank"}.

* Adobe Campaign Standard-integratie wordt ingesteld door middel van een speciale ingebouwde actie in de lijst met acties. Dit moet voor elke zandbak worden gevormd.

* U kunt geen Campaign Standard-actie gebruiken met de kwalificatie Publiek of Lezen publieksactiviteit.

* Een reis kan niet zowel [ ingebouwde kanaalacties ](../building-journeys/journeys-message.md) als [ de acties van Campaign Standard ](../building-journeys/using-adobe-campaign-standard.md) gebruiken.

## De handeling configureren {#configure-action}

In Journey Optimizer moet u één actie per transactiemelding configureren.

Voer de volgende stappen uit om een Campaign Standard-actie te configureren:

1. Selecteer **[!UICONTROL Configurations]** in de sectie van het menu van het Beleid.

1. Klik in de sectie **[!UICONTROL Actions]** op **[!UICONTROL Manage]** . De lijst met handelingen wordt weergegeven.

1. Selecteer de ingebouwde handeling **[!UICONTROL AdobeCampaignStandard]** . Het deelvenster Handelingsconfiguratie wordt aan de rechterkant van het scherm geopend.

   ![](assets/actioncampaign.png)

1. Kopieer de Adobe Campaign Standard-instantie-URL en plak deze in het veld **[!UICONTROL URL]** .

1. Klik op **[!UICONTROL Test the instance URL]** om de geldigheid van de instantie te testen.

   >[!NOTE]
   >
   >Deze test verifieert dat:
   >
   >* De host is &quot;.campagne.adobe.com&quot;, &quot;.campagne-sandbox.adobe.com&quot;, &quot;.campagne-demo.adobe.com&quot;, &quot;.ats.adobe.com&quot; of &quot;.adls.adobe.com&quot;
   >
   >* De URL begint met https
   >
   >* De organisatie die aan dit Adobe Campaign Standard-exemplaar is gekoppeld, is hetzelfde als de Journey Optimizer-organisatie

Zodra deze configuratie is voltooid, zijn er drie acties beschikbaar in de categorie **[!UICONTROL Action]** wanneer u een rit ontwerpt: **[!UICONTROL Email]**, **[!UICONTROL Push]**, **[!UICONTROL SMS]** . [ leer hoe te om hen ](../building-journeys/using-adobe-campaign-standard.md) te gebruiken.

![](assets/journey58.png)

Gebruik de gebeurtenis van de Reacties van de a **** om op het volgen van gegevens met betrekking tot een bericht van Campaign Standard te reageren dat binnen de zelfde reis wordt verzonden:

* Voor pushberichten kunnen reizen reageren op geklikte, verzonden of mislukte berichten.

* Voor SMS-berichten kunnen reizen reageren op verzonden of mislukte berichten.

* Voor e-mailberichten kunnen reizen reageren op geklikte, verzonden, geopende of mislukte berichten. [ Leer meer over reactiegebeurtenissen ](../building-journeys/reaction-events.md).

Wanneer het gebruiken van een derdesysteem om berichten te verzenden, moet u een douaneactie toevoegen en vormen. [ Leer meer over de configuratie van de douaneactie ](../action/about-custom-action-configuration.md).