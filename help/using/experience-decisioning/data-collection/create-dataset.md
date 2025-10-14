---
product: experience platform
solution: Experience Platform
title: Een gegevensset maken om gebeurtenissen te verzamelen
description: Leer hoe u een gegevensset maakt om gebeurtenissen te verzamelen
feature: Ranking, Decision Management, Datasets
role: Data Engineer, Developer
level: Experienced
hide: true
hidefromtoc: true
exl-id: 96c1326f-be40-4738-8997-a67dc14872bb
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Een gegevensset maken om gebeurtenissen te verzamelen {#create-dataset}

Om ervaringsgebeurtenissen te verzamelen, moet u eerst een dataset tot stand brengen waar deze gebeurtenissen zullen worden verzonden.

Begin door het schema te creëren dat in uw dataset zal worden gebruikt:

1. Selecteer **[!UICONTROL Schema]** in het menu **[!UICONTROL Data Management]** .

1. Klik **[!UICONTROL Create schema]**, in het hoogste recht, selecteer **[!UICONTROL Experience Event]** en klik **daarna**.

   ![](../../offers/assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Leer meer over schema&#39;s XDM en gebiedsgroepen in de [&#x200B; XDM het overzichtsdocumentatie van het Systeem &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"}.

1. Ga een naam en een beschrijving voor uw schema in en klik **Afwerking**.
   ![](../../offers/assets/ai-ranking-xdm-event-2.png)

1. Selecteer in de sectie **[!UICONTROL Field groups]** aan de linkerkant de optie **[!UICONTROL Add]** .

   ![](../../offers/assets/ai-ranking-fields-groups.png)

1. Typ &quot;propositieinteractie&quot; in het veld **[!UICONTROL Search]** .

1. Selecteer de veldgroep **[!UICONTROL Experience Event - Proposition Interactions]** en klik op **[!UICONTROL Add field groups]** .

   ![](../../offers/assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >Het schema dat in uw dataset zal worden gebruikt moet de **[!UICONTROL Experience Event - Proposition Interactions]** gebiedsgroep hebben verbonden aan het. Anders kunt u het niet gebruiken in uw AI-model.

1. Sla het schema op.

>[!NOTE]
>
>Leer meer over het bouwen van schema&#39;s in [&#x200B; Grondbeginselen van schemacompositie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=nl-NL#understanding-schemas){target="_blank"}.

U bent nu klaar om een dataset tot stand te brengen gebruikend dit schema. Hiervoor voert u de volgende stappen uit:

1. Selecteer **[!UICONTROL Datasets]** in het menu **[!UICONTROL Data Management]** en ga naar de tab **[!UICONTROL Browse]** .

1. Klik op **[!UICONTROL Create dataset]** en selecteer **[!UICONTROL Create dataset from schema]** .

   ![](../../offers/assets/ai-ranking-create-dataset-from-schema.png)

1. Selecteer het schema dat u zojuist hebt gemaakt in de lijst en klik op **[!UICONTROL Next]** .

1. Geef een unieke naam voor de gegevensset op in het veld **[!UICONTROL Name]** en klik op **[!UICONTROL Finish]** .

   ![](../../offers/assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>Deze dataset kan nu worden geselecteerd om gebeurtenisgegevens te verzamelen wanneer het creëren van een [&#x200B; AI model &#x200B;](../ranking/create-ai-models.md).
