---
title: 'Adobe Experience Platform-databron '
description: Leer hoe u Adobe Experience Platform-gegevensbron configureert
feature: Databronnen
topic: Beheer
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 10%

---

# Adobe Experience Platform-databron {#concept_zrb_nqt_52b}

Adobe Experience Platform-gegevensbron definieert de verbinding met de Real-Time Customer Profile Service. Deze gegevensbron is ingebouwd en vooraf geconfigureerd. Het kan niet worden verwijderd. Deze gegevensbron is ontworpen om gegevens van de Real-time Dienst van het Profiel van de Klant terug te winnen en te gebruiken (bijvoorbeeld, controleer of de persoon die een reis inging een vrouwelijk is). Hiermee kunt u de gegevens van het profiel en Events gebruiken. Raadpleeg [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;} voor meer informatie over de realtime klantenprofielservice.

>[!NOTE]
>
>U kunt de 1000 meest recente ervaringsgebeurtenissen ophalen die minder dan een jaar geleden zijn gemaakt.

Om de verbinding aan de Dienst van het Profiel van de Klant in real time toe te staan, moeten wij een sleutel gebruiken om een persoon, en een namespace te identificeren die contextualizes de sleutel. Hierdoor kunt u deze gegevensbron alleen gebruiken als uw reizen beginnen met een gebeurtenis die een sleutel en een naamruimte bevat. Zie [deze pagina](../building-journeys/journey.md).

U kunt de vooraf geconfigureerde veldgroep met de naam &quot;ProfileFieldGroup&quot; bewerken, nieuwe veldgroepen toevoegen en de groepen verwijderen die niet worden gebruikt in concepten of livedagen. Zie [deze pagina](../datasource/configure-data-sources.md#define-field-groups).

Hier zijn de belangrijkste stappen om gebiedsgroepen aan de ingebouwde gegevensbron toe te voegen.

1. Selecteer de Adobe Experience Platform-gegevensbron voor de build-in in de lijst met gegevensbronnen.

   Hiermee opent u het configuratiedeelvenster voor de databron aan de rechterkant van het scherm.

   ![](../assets/journey23.png)

1. Klik op **[!UICONTROL Add a New Field Group]** om een nieuwe reeks velden op te halen. Zie [deze pagina](../datasource/configure-data-sources.md#define-field-groups).

   ![](../assets/journey24.png)

1. Selecteer een schema van **[!UICONTROL Schema]** drop-down. In dit veld worden de schema&#39;s voor profiel- en ervaringsgebeurtenissen weergegeven die beschikbaar zijn in Adobe Experience Platform. Schema&#39;s maken wordt niet uitgevoerd in [!DNL Journey Optimizer]. Deze wordt uitgevoerd in Adobe Experience Platform.
1. Selecteer de velden die u wilt gebruiken.
1. Definieer de duur van de cache.
1. Klik op **[!UICONTROL Save]**.

Wanneer u de cursor op de naam van een veldgroep plaatst, ziet u rechts twee pictogrammen. Hiermee kunt u de veldgroep verwijderen en dupliceren. Het pictogram **[!UICONTROL Delete]** is alleen beschikbaar als de veldgroep niet wordt gebruikt in een live of conceptreis (informatie in het veld **[!UICONTROL Used in]**).
