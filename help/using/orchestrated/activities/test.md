---
solution: Journey Optimizer
product: journey optimizer
title: Gebruik de activiteit van de Test in uw Geordende campagnes
description: Leer hoe u de testactiviteit gebruikt
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
version: Campaign Orchestration
source-git-commit: b6b74e357029f4924f9699c05af3a0fcd7fcefd6
workflow-type: tm+mt
source-wordcount: '365'
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
>abstract="De **activiteit van de Test** kan veelvoudige uitvoerovergangen hebben. Tijdens de uitvoering van de geordende campagne wordt elke voorwaarde opeenvolgend getest totdat aan een van deze voorwaarden is voldaan. Als aan geen van de voorwaarden wordt voldaan, gaat de geordende campagne verder langs de weg van **[!UICONTROL Default condition]**. Als geen standaardvoorwaarde wordt geactiveerd, stopt de geordende campagne op dit punt."

De **[!UICONTROL Test]** -activiteit is een **[!UICONTROL Flow control]** -activiteit. Gebruik dit schema om de campagnestroom af te takken door verschillende overgangen te activeren, afhankelijk van de voorwaarden die u definieert. Elke voorwaarde kan gegevens van de binnenkomende overgang evalueren en u kunt kiezen welke overgang eerst door de orde loopt waarin de voorwaarden worden geëvalueerd.

## De testactiviteit configureren {#test-configuration}

U stelt de **[!UICONTROL Test]** -activiteit als volgt in:

1. Zet een **[!UICONTROL Test]** -activiteit neer in uw geordende campagnecanvas.

1. Standaard biedt de activiteit één booleaanse test: wanneer aan de voorwaarde &quot;Waar&quot; wordt voldaan, wordt die overgang geactiveerd; anders wordt de overgang &quot;Onwaar&quot; (standaard) geactiveerd.

   ![](../assets/test-1.png)

1. Definieer de voorwaarde voor een overgang door de volgende velden in te vullen:

   * **Etiket**: Een naam voor de overgang zodat kunt u het op het canvas identificeren.

   * **Type van Voorwaarde**: De gegevens, door gebrek, bevolkingstelling te evalueren.

   * **Exploitant**: De vergelijking om van toepassing te zijn, b.v. gelijk aan, groter dan, minder dan. De lijst met operatoren is afhankelijk van het gegevenstype van het voorwaarde.

   * **Waarde**: De waarde om het voorwaardetype tegen te vergelijken.

   ![](../assets/test-2.png)

1. Als u op meer dan twee resultaten wilt vertakken, klikt u op **[!UICONTROL Add condition]** en definieert u een label en een voorwaarde voor elke aanvullende overgang.

1. Tijdens de uitvoering worden de voorwaarden op volgorde geëvalueerd en wordt de eerste campagne gevolgd die overeenkomt. Wanneer geen voorwaarde overeenkomt, volgt de uitvoering **[!UICONTROL Default condition]** als er een is ingesteld; anders stopt de campagne bij de **[!UICONTROL Test]** -activiteit.

## Voorbeeld {#example}

In dit voorbeeld worden verschillende overgangen geactiveerd op basis van het aantal profielen waarop een **[!UICONTROL Build audience]** -activiteit is gericht. De voorwaarden worden geëvalueerd in orde; de laatste overgang is het gebrek en wordt gebruikt wanneer geen vorige voorwaarde aanpast.

* Als er meer dan 10.000 profielen zijn bedoeld, wordt een e-mailbericht verzonden.
* Standaardwaarde (geen voorwaarde die wordt gematcht): wanneer het aantal 10.000 of minder is, wordt de populatie omgeleid naar een overgang die niet in contact komt met.

![](../assets/workflow-test-example.png)
