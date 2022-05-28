---
product: experience platform
solution: Experience Platform
title: Een gegevensset maken om gebeurtenissen te verzamelen
description: Leer hoe u een gegevensset maakt om gebeurtenissen te verzamelen
feature: Ranking Formulas
role: User
level: Intermediate
source-git-commit: 12b01cb9de84399e5ede987866609acc10b64c5f
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 7%

---

# Een gegevensset maken om gebeurtenissen te verzamelen {#create-dataset}

Voordat u een AI-model maakt, moet u een gegevensset maken waarin conversiegebeurtenissen worden verzameld. Begin door het schema te creëren dat in uw dataset zal worden gebruikt:

1. Van de **[!UICONTROL Data Management]** menu, selecteert u **[!UICONTROL Schema]**, ga naar de **[!UICONTROL Browse]** en klik op **[!UICONTROL Create schema]**.

   ![](../assets/ai-ranking-create-schema.png)

1. Kies **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >    Meer informatie over XDM-schema&#39;s en veldgroepen in de [Documentatie over XDM System-overzicht](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl).


1. In de **[!UICONTROL Search]** veld, typt u &quot;propositieinteractie&quot; en selecteert u de **[!UICONTROL Experience Event - Proposition Interactions]** veldgroep.

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >    Het schema dat in uw dataset zal worden gebruikt moet hebben **[!UICONTROL Experience Event - Proposition Interactions]** veldgroep die eraan is gekoppeld. Anders kunt u het niet gebruiken in uw waarderingsstrategie.

1. Klik op **[!UICONTROL Add field groups]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >Veldgroep werd voorheen mixin genoemd.

1. Typ een naam en sla het schema op.<!--How do you edit the fields in this new schema? Examples?-->

>[!NOTE]
>
>    Meer informatie over het samenstellen van schema&#39;s vindt u in [Basisbeginselen van de schemacompositie](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas).

U bent nu bereid om een dataset tot stand te brengen gebruikend dit schema. Volg de onderstaande stappen om dit te doen:

1. Van de **[!UICONTROL Data Management]** menu, selecteert u **[!UICONTROL Datasets]**, ga naar de **[!UICONTROL Browse]** en klik op **[!UICONTROL Create dataset]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. Selecteer **[!UICONTROL Create dataset from schema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Selecteer het schema dat u zojuist hebt gemaakt in de lijst.

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. Klik op **[!UICONTROL Next]**.

1. Geef een unieke naam op voor de gegevensset in het dialoogvenster **[!UICONTROL Name]** veld en klik op **[!UICONTROL Finish]**.

   ![](../assets/ai-ranking-dataset-name.png)

De dataset is nu klaar om te worden geselecteerd om gebeurtenisgegevens te verzamelen wanneer [het opstellen van een rangschikkingsstrategie](#create-ranking-strategy).
