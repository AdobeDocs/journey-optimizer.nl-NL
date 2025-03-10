---
solution: Journey Optimizer
product: journey optimizer
title: De testactiviteit gebruiken in uw multi-step campagnes
description: Leer hoe u de testactiviteit gebruikt
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Testen {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="Testactiviteit"
>abstract="De **activiteit van de Test** is de controle **activiteit van de a** Stroom. Hiermee kunt u overgangen inschakelen op basis van opgegeven voorwaarden."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="Voorwaarden"
>abstract="De **activiteit van de Test** kan veelvoudige uitvoerovergangen hebben. Tijdens de uitvoering van meerdere stappen wordt elke voorwaarde opeenvolgend getest totdat aan een van deze voorwaarden is voldaan. Als aan geen van de voorwaarden wordt voldaan, gaat de campagne met meerdere stappen verder langs het pad van de **[!UICONTROL Default condition]** . Als geen standaardvoorwaarde wordt geactiveerd, stopt de campagne in meerdere stappen op dit punt."

De **activiteit van de Test** is de controle **activiteit van de a** Stroom. Hiermee kunt u overgangen inschakelen op basis van opgegeven voorwaarden.

## De testactiviteit configureren {#test-configuration}

Volg deze stappen om de **Test** activiteit te vormen:

1. Voeg de activiteit van de a **Test** aan uw multi-step campagne toe.

1. De **[!UICONTROL Test]** -activiteit geeft standaard een eenvoudige booleaanse test weer. Als aan de voorwaarde in de overgang &quot;Waar&quot; is voldaan, wordt deze overgang geactiveerd. Anders wordt een standaardovergang &quot;False&quot; geactiveerd.

1. Klik op het pictogram **[!UICONTROL Open personalization dialog]** om de voorwaarde te configureren die aan een overgang is gekoppeld. Gebruik de uitdrukkingsredacteur om de regels te bepalen die worden vereist om deze overgang te activeren. U kunt gebeurtenisvariabelen, voorwaarden en datum-/tijdfuncties ook gebruiken. [ Leer hoe te met gebeurtenisvariabelen en de uitdrukkingsredacteur te werken ](../event-variables.md)

   Bovendien kunt u het veld **[!UICONTROL Label]** aanpassen om de naam van de overgang aan te passen op het campagnecanvas met meerdere stappen.

   ![](../assets/workflow-test-default.png)

1. U kunt meerdere uitvoerovergangen toevoegen aan een **[!UICONTROL Test]** -activiteit. Klik hiertoe op de knop **[!UICONTROL Add condition]** en configureer het label en de bijbehorende voorwaarde voor elke overgang.
v
1. Tijdens de uitvoering van meerdere stappen wordt elke voorwaarde opeenvolgend getest totdat aan een van deze voorwaarden is voldaan. Als aan geen van de voorwaarden wordt voldaan, worden de campagnes met meerdere stappen voortgezet langs de weg van **[!UICONTROL Default condition]**. Als geen standaardvoorwaarde wordt geactiveerd, stoppen de workflows op dit punt.

## Voorbeeld {#example}

In dit voorbeeld worden verschillende overgangen geactiveerd op basis van het aantal profielen waarop een **[!UICONTROL Build audience]** -activiteit is gericht:

* Als er meer dan 10.000 profielen zijn bedoeld, wordt een e-mailbericht verzonden.
* Voor 1.000 tot 10.000 profielen, wordt SMS verzonden.
* Als de doelprofielen lager zijn dan 1.000, worden ze omgeleid naar een overgang &quot;neem geen contact op&quot;.

![](../assets/workflow-test-example.png)

Hiervoor is de gebeurtenisvariabele `vars.recCount` gebruikt in de voorwaarden &quot;email&quot; en &quot;sms&quot; om het aantal doelprofielen te tellen en de juiste overgang te activeren.

![](../assets/workflow-test-example-config.png)
