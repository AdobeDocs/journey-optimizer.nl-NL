---
solution: Journey Optimizer
product: journey optimizer
title: Integreren met Adobe Campaign Standard
description: Leer hoe u Journey Optimizer kunt integreren met Adobe Campaign Standard
feature: Actions
topic: Administration
role: Admin,Developer
level: Intermediate
keywords: campagne, standaard, integratie, plafonnering, actie
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 3%

---

# Integreren met Adobe Campaign Standard {#using_adobe_campaign_standard}

U kunt e-mails, pushberichten en SMS verzenden met de mogelijkheden voor Transactieberichten van Adobe Campaign Standard.

Als u Adobe Campaign Standard hebt, is er een ingebouwde actie beschikbaar waarmee u verbinding kunt maken met Adobe Campaign Standard.

Het transactiebericht van Campaign Standard en de bijbehorende gebeurtenis moeten worden gepubliceerd om in Journey Optimizer te kunnen worden gebruikt. Als de gebeurtenis wordt gepubliceerd maar het bericht niet is, is het niet zichtbaar in de interface van Journey Optimizer. Als het bericht wordt gepubliceerd maar zijn bijbehorende gebeurtenis niet, zal het in de interface van Journey Optimizer zichtbaar zijn maar het zal niet bruikbaar zijn.

## Belangrijke opmerkingen {#important-notes}

* Voor Adobe Campaign Standard-acties wordt automatisch een afluisterregel van 4000 aanroepen per 5 minuten gedefinieerd. Dit komt overeen met de officiële schaal van Transactioneel Overseinen van Adobe Campaign Standard. Lees meer over transactie overseinen SLAs in [Adobe Campaign Standard-productbeschrijving](https://helpx.adobe.com/nl/legal/product-descriptions/campaign-standard.html).

* Adobe Campaign Standard-integratie wordt ingesteld door middel van een speciale ingebouwde actie in de lijst met acties. Dit moet voor elke zandbak worden gevormd.

* U kunt geen actie van de Campaign Standard met een kwalificatie van het Segment of Gelezen segmentactiviteit gebruiken.

* Een reis kan niet zowel Berichten als Campaign Standard acties gebruiken.

## De handeling configureren {#configure-action}

Hier volgen de stappen om het te configureren:

1. Selecteren **[!UICONTROL Configurations]** in de sectie van het menu van het BEHEER. In de  **[!UICONTROL Actions]** sectie, klikt u op **[!UICONTROL Manage]**. De lijst met acties wordt weergegeven.

1. De ingebouwde **[!UICONTROL AdobeCampaignStandard]** handeling. Het deelvenster Handelingsconfiguratie wordt aan de rechterkant van het scherm geopend.

   ![](assets/actioncampaign.png)

1. Kopieer de Adobe Campaign Standard-instantie-URL en plak deze in het dialoogvenster **[!UICONTROL URL]** veld.

1. Klik op de knop **[!UICONTROL Test the instance URL]** om de geldigheid van de instantie te testen.

   >[!NOTE]
   >
   >Deze test verifieert dat:
   >
   >De host is &quot;.campagne.adobe.com&quot;, &quot;.campagne-sandbox.adobe.com&quot;, &quot;.campagne-demo.adobe.com&quot;, &quot;.ats.adobe.com&quot; of &quot;.adls.adobe.com&quot;.
   >
   >De URL begint met https.
   >
   >De ORG die aan deze Adobe Campaign Standard-instantie is gekoppeld, is gelijk aan de Journey Optimizer ORG.

Wanneer u uw reis ontwerpt, zijn er drie acties beschikbaar in de **[!UICONTROL Action]** categorie: **[!UICONTROL Email]**, **[!UICONTROL Push]**, **[!UICONTROL SMS]** (zie [Adobe Campaign-handelingen gebruiken](../building-journeys/using-adobe-campaign-standard.md)).

![](assets/journey58.png)

U kunt een **Reacties** gebeurtenis die moet reageren op volggegevens met betrekking tot een Campaign Standard-bericht dat binnen dezelfde reis wordt verzonden. Voor pushberichten kunt u reageren op geklikte, verzonden of mislukte berichten. Voor SMS-berichten kunt u reageren op verzonden of mislukte berichten. Voor e-mailberichten kunt u reageren op geklikte, verzonden, geopende of mislukte berichten. Zie [Gebeurtenissen van Reacties](../building-journeys/reaction-events.md).

Als u een derdesysteem gebruikt om berichten te verzenden, moet u een douaneactie toevoegen en vormen. Zie [Aangepaste actieconfiguratie](../action/about-custom-action-configuration.md).
