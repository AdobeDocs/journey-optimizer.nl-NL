---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform-databron
description: Leer hoe u Adobe Experience Platform-gegevensbron configureert
feature: Data Sources
topic: Administration
role: Admin, Developer
level: Intermediate
keywords: ingebouwd, bron, gegevens, platform, integratie
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 9%

---

# Adobe Experience Platform-databron {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Adobe Experience Platform-databron"
>abstract="De gegevensbron van Adobe Experience Platform bepaalt de verbinding aan Adobe Real-time het Profiel van de Klant. Deze gegevensbron is ingebouwd en vooraf geconfigureerd en kan niet worden verwijderd. Het is ontworpen om gegevens van de Real-time Dienst van het Profiel van de Klant terug te winnen en te gebruiken (bijvoorbeeld, controleer of de persoon die een reis inging een vrouwelijk is). Hiermee kunt u de gegevens van het profiel en de gegevens van Experience Events gebruiken."

De gegevensbron van Adobe Experience Platform bepaalt de verbinding aan Adobe Real-time het Profiel van de Klant. Deze gegevensbron is ingebouwd en vooraf geconfigureerd en kan niet worden verwijderd. Deze gegevensbron is ontworpen om gegevens van de Real-time Dienst van het Profiel van de Klant terug te winnen en te gebruiken (bijvoorbeeld, controleer of de persoon die een reis inging een vrouwelijk is). Hiermee kunt u de gegevens van het profiel en de gegevens van Experience Events gebruiken. Voor meer informatie over de Adobe van het Profiel van de Klant in real time, verwijs naar [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target="_blank"}.


Om de verbinding aan de Dienst van het Profiel van de Klant in real time toe te staan, moeten wij een sleutel gebruiken om een persoon, en een namespace te identificeren die contextualizes de sleutel. Hierdoor kunt u deze gegevensbron alleen gebruiken als uw reizen beginnen met een gebeurtenis die een sleutel en een naamruimte bevat. [Meer informatie](../building-journeys/journey.md).

U kunt de vooraf geconfigureerde veldgroep met de naam &quot;ProfileFieldGroup&quot; bewerken, nieuwe veldgroepen toevoegen en de groepen verwijderen die niet worden gebruikt in concepten of livedagen. [Meer informatie](../datasource/configure-data-sources.md#define-field-groups).


>[!NOTE]
>
>U kunt de 1000 meest recente ervaringsgebeurtenissen ophalen die minder dan een jaar geleden zijn gemaakt.

Hier zijn de belangrijkste stappen om gebiedsgroepen aan de ingebouwde gegevensbron toe te voegen.

1. Selecteer de Adobe Experience Platform-gegevensbron voor de build-in in de lijst met gegevensbronnen.

   Hiermee opent u het configuratiedeelvenster voor de databron aan de rechterkant van het scherm.

   ![](assets/journey23.png)

1. Klikken **[!UICONTROL Add a New Field Group]** om een nieuwe reeks velden te definiëren die moet worden opgehaald. [Meer informatie](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Selecteer een schema in het menu **[!UICONTROL Schema]** vervolgkeuzelijst. In dit veld worden de schema&#39;s voor profiel- en ervaringsgebeurtenissen weergegeven die beschikbaar zijn in Adobe Experience Platform. Het maken van het schema wordt niet uitgevoerd in [!DNL Journey Optimizer]. Deze wordt uitgevoerd in Adobe Experience Platform.
1. Selecteer de velden die u wilt gebruiken.
1. Klikken op **[!UICONTROL Save]**.

Wanneer u de cursor op de naam van een veldgroep plaatst, ziet u rechts twee pictogrammen. Hiermee kunt u de veldgroep verwijderen en dupliceren. Let erop dat de **[!UICONTROL Delete]** pictogram is alleen beschikbaar als de veldgroep niet wordt gebruikt in een live of conceptrit (informatie weergegeven in de **[!UICONTROL Used in]** veld).
