---
product: experience platform
solution: Experience Platform
title: Een gegevensset maken om gebeurtenissen te verzamelen
description: Leer hoe u een gegevensset maakt om gebeurtenissen te verzamelen
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 59499dec7d15dd4565c7910d7b454d82243ff011
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 7%

---

# Een gegevensset maken om gebeurtenissen te verzamelen {#create-dataset}

Om ervaringsgebeurtenissen te verzamelen, moet u eerst een dataset tot stand brengen waar deze gebeurtenissen zullen worden verzonden.

Begin door het schema te creëren dat in uw dataset zal worden gebruikt:

1. Van de **[!UICONTROL Data Management]** menu, selecteert u **[!UICONTROL Schema]** en ga naar de **[!UICONTROL Browse]** tab.

1. Klikken **[!UICONTROL Create schema]** en kiest u **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Meer informatie over XDM-schema&#39;s en veldgroepen in de [Documentatie over XDM System-overzicht](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"}.

1. Van de **[!UICONTROL Field groups]** in het linkergedeelte selecteert u **[!UICONTROL Add]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. In de **[!UICONTROL Search]** veld, typ &quot;propositieinteractie&quot;.

1. Selecteer **[!UICONTROL Experience Event - Proposition Interactions]** veldgroep en klik op **[!UICONTROL Add field groups]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >Het schema dat in uw dataset zal worden gebruikt moet hebben **[!UICONTROL Experience Event - Proposition Interactions]** veldgroep die eraan is gekoppeld. Anders kunt u het niet gebruiken in uw waarderingsstrategie.

1. Typ een naam en sla het schema op.

>[!NOTE]
>
>Meer informatie over het samenstellen van schema&#39;s vindt u in [Basisbeginselen van de schemacompositie](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#understanding-schemas){target="_blank"}.

U bent nu bereid om een dataset tot stand te brengen gebruikend dit schema. Volg de onderstaande stappen om dit te doen:

1. Van de **[!UICONTROL Data Management]** menu, selecteert u **[!UICONTROL Datasets]** en ga naar de **[!UICONTROL Browse]** tab.

1. Klik op **[!UICONTROL Create dataset]** en selecteer **[!UICONTROL Create dataset from schema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Selecteer het net gemaakte schema in de lijst en klik op **[!UICONTROL Next]**.

1. Geef een unieke naam op voor de gegevensset in het dialoogvenster **[!UICONTROL Name]** veld en klik op **[!UICONTROL Finish]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>Deze dataset kan nu worden geselecteerd om gebeurtenisgegevens te verzamelen wanneer [het opstellen van een rangschikkingsstrategie](#create-ranking-strategy).
