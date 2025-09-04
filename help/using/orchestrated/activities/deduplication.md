---
solution: Journey Optimizer
product: journey optimizer
title: De deduplicatieactiviteit gebruiken
description: Leer hoe u de deduplicatieactiviteit gebruikt
exl-id: 4aa79448-f75a-48d5-8819-f4cb4baad5c7
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---


# Deduplicatie {#deduplication}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_fields"
>title="Velden om duplicaten te identificeren"
>abstract="In de **Gebieden om duplicaten** sectie te identificeren, klik **voegt attribuut** knoop toe om de gebieden te specificeren waarvoor de identieke waarden toestaan om worden geïdentificeerd de duplicaten, zoals: e-mailadres, voornaam, achternaam, enz. In de volgorde van de velden kunt u opgeven welke velden eerst moeten worden verwerkt."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication"
>title="Deduplicatieactiviteit"
>abstract="De **Deduplicatie** activiteit staat u toe om duplicaten in de resultaten van de binnenkomende activiteiten te schrappen. Het wordt meestal gebruikt na doelgerichte activiteiten en vóór activiteiten die het gebruik van gerichte gegevens mogelijk maken."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_complement"
>title="Een complement genereren"
>abstract="U kunt een extra uitgaande overgang met de resterende bevolking produceren, die als duplicaat werd uitgesloten. Om dit te doen, op **van een knevel voorzien produceer complement** optie"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_settings"
>title="Instellingen voor deduplicatie"
>abstract="Als u duplicaten van binnenkomende gegevens wilt verwijderen, definieert u de deduplicatiemethode in de onderstaande velden. Standaard wordt slechts één record bewaard. U moet ook de deduplicatiemodus selecteren op basis van een expressie of een kenmerk. Standaard wordt de record die buiten de duplicaten moet blijven, willekeurig geselecteerd."

De **[!UICONTROL Deduplication]** -activiteit is een **[!UICONTROL Targeting]** -activiteit. Met deze activiteit kunt u duplicaten verwijderen uit het resultaat of de resultaten van de binnenkomende activiteiten, bijvoorbeeld gedupliceerde profielen in de lijst met ontvangers. De **[!UICONTROL Deduplication]** -activiteit wordt over het algemeen gebruikt na doelactiviteiten en vóór activiteiten die het gebruik van gerichte gegevens toestaan.

## De deduplicatieactiviteit configureren{#deduplication-configuration}

Voer de volgende stappen uit om de **[!UICONTROL Deduplication]** -activiteit te configureren:


1. Voeg een **[!UICONTROL Deduplication]** activiteit aan uw Geordende campagne toe.

1. Klik in de sectie **[!UICONTROL Fields to identify duplicates]** op de knop **[!UICONTROL Add attribute]** om de velden op te geven waarvoor de duplicaten met identieke waarden kunnen worden geïdentificeerd, zoals: e-mailadres, voornaam, achternaam, enz. In de volgorde van de velden kunt u opgeven welke velden eerst moeten worden verwerkt.

   ![](../assets/deduplication-1.png)

1. Kies in de sectie **[!UICONTROL Deduplication settings]** hoeveel unieke records u wilt behouden met de Duplicaten om het veld te behouden. De standaardwaarde is 1, die één record per gedupliceerde groep bijhoudt. Stel de waarde in op 0 om alle duplicaten te behouden.

   Bijvoorbeeld als de records A en B duplicaten van Y zijn en record C een duplicaat van Z is:

   * **als de waarde van het gebied 1** is: Slechts worden de verslagen van Y en van Z bewaard.
   * **als de waarde van het gebied 0** is: Alle verslagen (A, B, C, Y, Z) worden gehouden.
   * **als de waarde van het gebied 2** is: C en Z worden gehouden, plus twee waarden van A, B, en Y, willekeurig of gebaseerd op uw deduplicatiemethode.

1. Kies een **[!UICONTROL Deduplication Method]**, dit bepaalt hoe het systeem besluit welke records van elke groep duplicaten worden bewaard:

   * **[!UICONTROL Random selection]** - Hiermee selecteert u willekeurig de record die u uit de duplicaten wilt verwijderen.
   * **[!UICONTROL Using an expression]**: houdt records met de hoogste of laagste waarde op basis van een door u gedefinieerde expressie.
   * **[!UICONTROL Non-empty values]**: houdt records bij waar het geselecteerde veld niet leeg is, bijvoorbeeld alleen profielen met een telefoonnummer.
   * **[!UICONTROL Following a list of values]**: hiermee kunt u specifieke waarden voor een of meer velden prioriteren. U kunt bijvoorbeeld prioriteit geven aan records met &quot;Land&quot; ingesteld op Frankrijk. Klik op **[!UICONTROL Attribute]** om een veld te kiezen of een aangepaste expressie te maken. Gebruik **[!UICONTROL Add button]** om voorkeurwaarden in te voeren in de prioriteitsvolgorde.

   ![](../assets/deduplication-2.png)

1. Schakel de optie **[!UICONTROL Generate complement]** in als u de resterende populatie wilt benutten. Het complement bestaat uit alle duplicaten. Er wordt dan een aanvullende overgang toegevoegd aan de activiteit.

## Voorbeeld{#deduplication-example}

In het volgende voorbeeld wordt een **[!UICONTROL Deduplication]** -activiteit gebruikt om dubbele records uit het doelpubliek te verwijderen voordat een levering wordt verzonden. Het publiek wordt eerst gefilterd en worden alleen profielen met een niet-leeg veld E-mail opgenomen. Vervolgens gebruikt de activiteit **[!UICONTROL Deduplication]** het e-mailadres om dubbele gegevens te identificeren en uit te sluiten.

![](../assets/deduplication-3.png)
