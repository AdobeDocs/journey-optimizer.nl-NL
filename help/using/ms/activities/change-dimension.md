---
solution: Journey Optimizer
product: journey optimizer
title: De activiteit Dimensie wijzigen gebruiken
description: Leer hoe u de activiteit Dimensie wijzigen gebruikt
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '330'
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

De **dimensie van de Verandering** activiteit is a **richtend** activiteit. Met deze activiteit kunt u de doeldimensie wijzigen terwijl u uw campagne met meerdere stappen ontwikkelt. Het verschuift de as afhankelijk van het gegevensmalplaatje en de inputdimensie.

U kunt bijvoorbeeld de doeldimensie van een campagne in meerdere stappen overschakelen van &quot;Ontvangers&quot; naar &quot;Abonnees&quot; om pushberichten naar de beoogde ontvangers te verzenden.

>[!IMPORTANT]
>
>De activiteiten **[!UICONTROL Change Dimension]** en **[!UICONTROL Change Data source]** mogen niet in één rij worden toegevoegd. Als u beide activiteiten opeenvolgend moet gebruiken, zorg ervoor u een **[!UICONTROL Enrichement]** activiteit binnen tussen hen omvat. Dit zorgt voor een correcte uitvoering en voorkomt mogelijke conflicten of fouten.

## Vorm de de afmetingsactiviteit van de Verandering {#configure}

Volg deze stappen om de **dimensie van de Verandering** activiteit te vormen:

1. Voeg de dimensie van de a **Verandering** activiteit aan uw multi-step campagne toe.

   ![](../assets/workflow-change-dimension.png)

1. Bepaal de **Nieuwe doelafmeting**. Tijdens het wijzigen van de afmetingen worden alle records bewaard. Andere opties zijn nog niet beschikbaar.

1. Voer de campagne met meerdere stappen uit om het resultaat te bekijken. Vergelijk de gegevens in de lijsten vóór en na de activiteit van de veranderingsdimensie, en vergelijk de structuur van de multi-step campagnemodules.

## Voorbeeld {#example}

In dit voorbeeld willen we een SMS-levering verzenden naar alle profielen die een aankoop hebben gedaan. Hiervoor gebruiken we eerst een **[!UICONTROL Build audience]** -activiteit die gekoppeld is aan een aangepaste &#39;Aankoop&#39;-doeldimensie om alle aankopen te activeren.

Vervolgens gebruiken we een **[!UICONTROL Change dimension]** -activiteit om de meerstapse campagne gericht op &#39;Ontvangers&#39; om te zetten. Dit staat ons toe om de ontvangers te kunnen richten die de vraag aanpassen.

![](../assets/workflow-change-dimension-example.png)
