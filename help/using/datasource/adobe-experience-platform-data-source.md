---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform-databron
description: Leer hoe u Adobe Experience Platform-gegevensbron configureert
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: ingebouwd, bron, gegevens, platform, integratie
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: e45ec5f0e1bbcc73892f9cde5923627886f44ef6
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 8%

---

# Adobe Experience Platform-databron {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Adobe Experience Platform-databron"
>abstract="Adobe Experience Platform-gegevensbron definieert de verbinding met Adobe Real-time klantprofiel. Deze gegevensbron is ingebouwd en vooraf geconfigureerd en kan niet worden verwijderd. Het is ontworpen om gegevens van de Real-time Dienst van het Profiel van de Klant terug te winnen en te gebruiken (bijvoorbeeld, controleer of de persoon die een reis inging een vrouwelijk is). Hiermee kunt u de gegevens van het profiel en de gegevens van Experience Events gebruiken."

Adobe Experience Platform-gegevensbron definieert de verbinding met Adobe Real-time klantprofiel. Deze gegevensbron is ingebouwd en vooraf geconfigureerd en kan niet worden verwijderd. Deze gegevensbron is ontworpen om gegevens van de Real-time Dienst van het Profiel van de Klant terug te winnen en te gebruiken (bijvoorbeeld, controleer of de persoon die een reis inging een vrouwelijk is). Hiermee kunt u de gegevens van het profiel en de gegevens van Experience Events gebruiken. Voor meer informatie over het Profiel van de Klant in real time van Adobe, verwijs naar [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl) {target="_blank"}.

Om de verbinding aan de Dienst van het Profiel van de Klant in real time toe te staan, moeten wij een sleutel gebruiken om een persoon, en een namespace te identificeren die contextualizes de sleutel. Hierdoor kunt u deze gegevensbron alleen gebruiken als uw reizen beginnen met een gebeurtenis die een sleutel en een naamruimte bevat. [Meer informatie](../building-journeys/journey.md).

U kunt de vooraf geconfigureerde veldgroep met de naam &quot;ProfileFieldGroup&quot; bewerken, nieuwe veldgroepen toevoegen en de groepen verwijderen die niet worden gebruikt in concepten of livedagen. [Meer informatie](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>U kunt de 1000 meest recente ervaringsgebeurtenissen ophalen die minder dan een jaar geleden zijn gemaakt.

Hier zijn de belangrijkste stappen om gebiedsgroepen aan de ingebouwde gegevensbron toe te voegen.

1. Selecteer de Adobe Experience Platform-gegevensbron voor de build-in in de lijst met gegevensbronnen.

   Hiermee opent u het configuratiedeelvenster voor de databron aan de rechterkant van het scherm.

   ![](assets/journey23.png)

1. Klik op **[!UICONTROL Add a New Field Group]** om een nieuwe reeks velden op te halen. [Meer informatie](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Selecteer een schema in de vervolgkeuzelijst **[!UICONTROL Schema]** . In dit veld worden de schema&#39;s voor profiel- en ervaringsgebeurtenissen weergegeven die beschikbaar zijn in Adobe Experience Platform. Schema&#39;s maken wordt niet uitgevoerd in [!DNL Journey Optimizer] . Deze wordt uitgevoerd in Adobe Experience Platform.
1. Selecteer de velden die u wilt gebruiken.
1. Klik op **[!UICONTROL Save]** .

Wanneer u de cursor op de naam van een veldgroep plaatst, ziet u rechts twee pictogrammen. Hiermee kunt u de veldgroep verwijderen en dupliceren. Het pictogram **[!UICONTROL Delete]** is alleen beschikbaar als de veldgroep niet wordt gebruikt tijdens een live of conceptrit (informatie wordt weergegeven in het veld **[!UICONTROL Used in]** ).
