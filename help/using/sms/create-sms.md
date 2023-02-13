---
solution: Journey Optimizer
product: journey optimizer
title: Een SMS-bericht maken
description: Meer informatie over het maken van een SMS-bericht in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 5%

---

# Een SMS-bericht maken {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Een SMS-bericht maken"
>abstract="Voeg uw SMS-bericht toe en pas het aan met de Expressieeditor."

## Een SMS-bericht toevoegen {#create-sms-journey-campaign}

Blader op de onderstaande tabbladen om te leren hoe u een SMS-bericht kunt toevoegen aan een campagne of een reis.

>[!BEGINTABS]

>[!TAB Een SMS-bericht toevoegen aan een reis]

1. Open uw reis en sleep een activiteit van SMS van **Handelingen** in het palet.

   ![](assets/sms_create_1.png)

1. Verstrek basisinformatie over uw bericht (etiket, beschrijving, categorie), dan kies de berichtoppervlakte aan gebruik.

   ![](assets/sms_create_2.png)

   Voor meer informatie over hoe te om een reis te vormen, verwijs naar [deze pagina](../building-journeys/journey-gs.md)

U kunt nu de inhoud van uw SMS-bericht ontwerpen via het **[!UICONTROL Edit content]** knop. [Je SMS-inhoud definiëren](#sms-content)

>[!TAB Een SMS-bericht toevoegen aan een campagne]

1. Maak een nieuwe geplande of door API geactiveerde campagne, selecteer **[!UICONTROL SMS]** als uw actie en kies **[!UICONTROL App surface]** te gebruiken. [Meer informatie over de SMS-configuratie](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. Klik op **[!UICONTROL Create]**.

1. Van de **[!UICONTROL Properties]** sectie, uw campagne bewerken **[!UICONTROL Title]** en **[!UICONTROL Description]**.

   ![](assets/sms_create_4.png)

1. In de **[!UICONTROL Actions tracking]** in, geeft u op of u wilt bijhouden of er op koppelingen in uw SMS-bericht wordt geklikt.

1. Klik op de knop **[!UICONTROL Select audience]** om het publiek te bepalen om van de lijst van beschikbare segmenten van Adobe Experience Platform te richten. [Meer informatie](../segment/about-segments.md).

1. In de **[!UICONTROL Identity namespace]** , kiest u de naamruimte die u wilt gebruiken om de personen van het geselecteerde segment te identificeren. [Meer informatie](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. Campagnes worden ontworpen om op een specifieke datum of op een terugkomende frequentie worden uitgevoerd. Leer hoe u de **[!UICONTROL Schedule]** van uw campagne in [deze sectie](../campaigns/create-campaign.md#schedule).

1. Van de **[!UICONTROL Action triggers]** kiest u de **[!UICONTROL Frequency]** van je SMS-bericht:

   * Eenmaal
   * Dagelijks
   * Wekelijks
   * Month

U kunt nu de inhoud van uw SMS-bericht ontwerpen via het **[!UICONTROL Edit content]** knop. [Ontwerp uw SMS-inhoud](#sms-content)

>[!ENDTABS]


## Je SMS-inhoud definiëren{#sms-content}

1. Van het reis of scherm van de campagneconfiguratie, klik **[!UICONTROL Edit content]** om de inhoud van SMS te vormen.

1. Klik op de knop **[!UICONTROL Message]** om de Expressieeditor te openen.

   ![](assets/sms-content.png)

1. Gebruik de expressie-editor om inhoud te definiëren en dynamische inhoud toe te voegen. U kunt elk kenmerk gebruiken, zoals de profielnaam of plaats. Meer informatie over [personalisatie](../personalization/personalize.md) en [dynamische inhoud](../personalization/get-started-dynamic-content.md) in de Uitdrukking redacteur.

1. Klikken **[!UICONTROL Save]** en controleer uw bericht in de voorvertoning. [Meer informatie](send-sms.md)

   ![](assets/sms-content-preview.png)

>[!NOTE]
>
>In overeenstemming met de industriestandaarden en -voorschriften moeten alle SMS-marketingberichten een manier bevatten waarop de ontvangers hun abonnement gemakkelijk kunnen opzeggen. Om dit te doen, kunnen de ontvangers van SMS met opt-in en opt-out sleutelwoorden antwoorden. [Meer informatie over het beheren van opt-out](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**Verwante onderwerpen**

* [Sms-kanaal configureren](sms-configuration.md)
* [Sms-rapport](../reports/journey-global-report.md#sms-global)
* [Een bericht toevoegen in een journey](../building-journeys/journeys-message.md)
* [Een bericht toevoegen aan een campagne](../campaigns/create-campaign.md)
