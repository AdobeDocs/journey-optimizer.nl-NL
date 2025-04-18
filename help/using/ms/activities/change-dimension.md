---
solution: Journey Optimizer
product: journey optimizer
title: De activiteit Dimensie wijzigen gebruiken
description: Leer hoe u de activiteit Dimensie wijzigen gebruikt
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 94de60c33c7cf1d8956294aebb91d7533534088f
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# Dimensie wijzigen {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Een complement genereren"
>abstract="U kunt een extra uitgaande overgang met de resterende bevolking produceren, die als duplicaat werd uitgesloten. Om dit te doen, op **van een knevel voorzien produceer complement** optie"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Dimensieactiviteit wijzigen"
>abstract="Met deze activiteit kunt u de doeldimensie wijzigen terwijl u een publiek maakt. Het verschuift de as afhankelijk van het gegevensmalplaatje en de inputdimensie. U kunt bijvoorbeeld van de dimensie &quot;contracten&quot; naar de dimensie &quot;clients&quot; schakelen."

Als markeerteken, kunt u de het richten dimensie van één entiteit aan een andere verbonden entiteit binnen een georkestreerde campagne schakelen, en uw publiek verfijnen richtend op verschillende gegevensreeksen, zoals het bewegen van het profileren van gebruikers aan het richten van hun specifieke acties of het boeken.

Om dit uit te voeren, gebruik de **dimensie van de Verandering** richtend activiteit. Met deze activiteit kunt u de doeldimensie wijzigen terwijl u uw georkestreerde campagne ontwikkelt. Het verschuift de as afhankelijk van het gegevensmalplaatje en de inputdimensie.

U kunt bijvoorbeeld de doeldimensie van een georkestreerde campagne veranderen van &quot;Profiel&quot; in &quot;Contracten&quot; om berichten naar de doelcontracteigenaar te verzenden.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Vorm de de afmetingsactiviteit van de Verandering {#configure}

Volg deze stappen om de **dimensie van de Verandering** activiteit te vormen:

1. Voeg de dimensie van de a **Verandering** activiteit aan uw georkestreerde campagne toe.

   ![](../assets/change-dimension.png)

1. Bepaal de **Nieuwe doelafmeting**. Tijdens het wijzigen van de afmetingen worden alle records bewaard.

1. Voer de georkestreerde campagne uit om het resultaat te bekijken. Vergelijk de gegevens in de lijsten vóór en na de activiteit van de veranderingsdimensie, en vergelijk de structuur van de georkestreerde campagnetabellen.

## Voorbeeld {#example}

In dit voorbeeld willen we een SMS-levering verzenden naar alle profielen die een aankoop hebben gedaan. Hiervoor gebruiken we eerst een **[!UICONTROL Build audience]** -activiteit die gekoppeld is aan een aangepaste &#39;Aankoop&#39;-doeldimensie om alle aankopen te activeren.

Vervolgens gebruiken we een **[!UICONTROL Change dimension]** -activiteit om de georkestreerde campagne voor dimensie om te zetten in &quot;Ontvangers&quot;. Dit staat ons toe om de ontvangers te kunnen richten die de vraag aanpassen.

![](../assets/change-dimension-example.png)
