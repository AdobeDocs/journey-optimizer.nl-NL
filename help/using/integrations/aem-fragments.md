---
solution: Journey Optimizer
product: journey optimizer
title: AEM-inhoudsfragmenten
description: Leer hoe u AEM Content Fragments kunt openen en beheren
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: 1af75a0e6bfc2c3b9c565c3190f46d137a68d32e
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Adobe Experience Manager-inhoudsfragmenten {#aem-fragments}

Door Adobe Experience Manager te integreren met Adobe Journey Optimizer, kunt u nu uw AEM Content Fragments naadloos opnemen in uw Journey Optimizer e-mailinhoud. Deze gestroomlijnde verbinding vereenvoudigt het proces van toegang tot en gebruik van AEM-inhoud, waardoor persoonlijke en dynamische campagnes en reizen kunnen worden gemaakt.

Meer over het Fragment van de Inhoud van AEM leren, verwijs naar [ documentatie van Experience Manager ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/sites/authoring/fragments/content-fragments).

## Beperkingen {#limitations}

* Alleen beschikbaar voor e-mailkanaal.

* Gebruikers kunnen momenteel niet schakelen tussen de AEM-instantie waarmee ze zijn verbonden, omdat elke sandbox tot één instantie is beperkt.

* Het wordt aanbevolen het aantal gebruikers dat toegang heeft tot het publiceren van inhoudsfragmenten te beperken om het risico op onopzettelijke fouten in e-mails te verminderen.

* Voor meertalige inhoud wordt alleen de handmatige stroom ondersteund.

* Varianten worden momenteel niet ondersteund.

* U moet een specifieke tag voor Journey Optimizer maken.

+++ Meer informatie over het maken van je Journey Optimizer-tag

   1. Heb toegang tot uw **milieu van Experience Manager**.

   1. Van het **menu van Hulpmiddelen**, navigeer aan het **Algemene** lusje en selecteer **Tags**.

   1. Klik **creeer een Nieuwe Markering**.

   1. Controleer of de id voldoet aan de volgende syntaxis: `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}` .

   1. Klik **creëren**.

  U kunt deze Journey Optimizer-tag nu toewijzen aan inhoudsfragmenten.
+++

## AEM-inhoudsfragmenten toevoegen {#aem-add}

Na het creëren van en het personaliseren van uw [ Fragmenten van de Inhoud van AEM ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/sites/authoring/fragments/content-fragments), kunt u het aan uw de optimaliseringscampagne of reis van de Reis nu invoeren.

1. Na het creëren van uw [ Campagne ](../email/create-email.md) of [ Reis ](../email/create-email.md) met een e-mailactie, heb toegang tot de e-mailontwerper om de e-mailinhoud te vormen. [Meer informatie](../email/get-started-email-design.md)

1. Klik in een tekstblok of in de onderwerpregel en selecteer **[!UICONTROL Add Personalization]** in de contextuele werkbalk.

   ![](assets/aem_campaign_2.png)

1. Klik in het menu **[!UICONTROL AEM Content Fragment]** in het linkerdeelvenster op **[!UICONTROL Open AEM CF selector]** .

   ![](assets/aem_campaign_3.png)

1. Selecteer een **[!UICONTROL Content Fragment]** in de lijst met beschikbare items om deze te importeren in uw Journey Optimizer-inhoud.

1. Klik op **[!UICONTROL Show filters]** om de lijst met inhoudsfragmenten te verfijnen.

   Standaard is het filter Inhoudsfragment vooraf ingesteld om alleen goedgekeurde inhoud weer te geven.

   ![](assets/aem_campaign_4.png)

1. Nadat u **[!UICONTROL Content Fragment]** hebt geselecteerd, klikt u op **[!UICONTROL Select]** om het te openen.

   ![](assets/aem_campaign_5.png)

1. Kies de gewenste velden in uw **[!UICONTROL Content Fragment]** om aan uw inhoud toe te voegen. U kunt inhoud toevoegen of de waarde ervan kopiëren.

   Als u ervoor kiest de waarde te kopiëren, worden toekomstige updates van **[!UICONTROL Content Fragment]** niet weerspiegeld in uw campagne of reis.

   ![](assets/aem_campaign_6.png)

1. Klik op **[!UICONTROL Save]** en controleer uw bericht in de voorvertoning. U kunt nu uw berichtinhoud zoals die in [ wordt gedetailleerd deze sectie ](../content-management/preview.md) testen en controleren.

Zodra u uw tests hebt uitgevoerd en de inhoud bevestigd, kunt u uw e-mail naar uw publiek met uw [ Campagne ](../campaigns/review-activate-campaign.md) of [ Reis ](../building-journeys/publishing-the-journey.md) verzenden.
