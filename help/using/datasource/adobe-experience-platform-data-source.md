---
title: Adobe Experience Platform-databron
description: Leer hoe u Adobe Experience Platform-gegevensbron configureert
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: bd35bf2ec4c1b2898007d670fc20626f06cc3750
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 11%

---

# Adobe Experience Platform-databron {#adobe-experience-platform-data-source}

Adobe Experience Platform-gegevensbron definieert de verbinding met de Real-Time Customer Profile Service. Deze gegevensbron is ingebouwd en vooraf geconfigureerd. Het kan niet worden verwijderd. Deze gegevensbron is ontworpen om gegevens van de Real-time Dienst van het Profiel van de Klant terug te winnen en te gebruiken (bijvoorbeeld, controleer of de persoon die een reis inging een vrouwelijk is). Hiermee kunt u de gegevens van het profiel en Events gebruiken. Raadpleeg voor meer informatie over de realtime klantenprofielservice de [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target=&quot;_blank&quot;}.

>[!NOTE]
>
>U kunt de 1000 meest recente ervaringsgebeurtenissen ophalen die minder dan een jaar geleden zijn gemaakt.

Om de verbinding aan de Dienst van het Profiel van de Klant in real time toe te staan, moeten wij een sleutel gebruiken om een persoon, en een namespace te identificeren die contextualizes de sleutel. Hierdoor kunt u deze gegevensbron alleen gebruiken als uw reizen beginnen met een gebeurtenis die een sleutel en een naamruimte bevat. Zie [deze pagina](../building-journeys/journey.md).

U kunt de vooraf geconfigureerde veldgroep met de naam &quot;ProfileFieldGroup&quot; bewerken, nieuwe veldgroepen toevoegen en de groepen verwijderen die niet worden gebruikt in concepten of livedagen. Zie [deze pagina](../datasource/configure-data-sources.md#define-field-groups).

Hier zijn de belangrijkste stappen om gebiedsgroepen aan de ingebouwde gegevensbron toe te voegen.

1. Selecteer de Adobe Experience Platform-gegevensbron voor de build-in in de lijst met gegevensbronnen.

   Hiermee opent u het configuratiedeelvenster voor de databron aan de rechterkant van het scherm.

   ![](assets/journey23.png)

1. Klikken **[!UICONTROL Add a New Field Group]** om een nieuwe reeks velden te definiëren die moet worden opgehaald. Zie [deze pagina](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Selecteer een schema in het menu **[!UICONTROL Schema]** vervolgkeuzelijst. In dit veld worden de schema&#39;s voor profiel- en ervaringsgebeurtenissen weergegeven die beschikbaar zijn in Adobe Experience Platform. Het maken van het schema wordt niet uitgevoerd in [!DNL Journey Optimizer]. Deze wordt uitgevoerd in Adobe Experience Platform.
1. Selecteer de velden die u wilt gebruiken.
1. Klikken op **[!UICONTROL Save]**.

Wanneer u de cursor op de naam van een veldgroep plaatst, ziet u rechts twee pictogrammen. Hiermee kunt u de veldgroep verwijderen en dupliceren. De **[!UICONTROL Delete]** pictogram is alleen beschikbaar als de veldgroep niet wordt gebruikt in een live of conceptrit (informatie weergegeven in de **[!UICONTROL Used in]** veld).
