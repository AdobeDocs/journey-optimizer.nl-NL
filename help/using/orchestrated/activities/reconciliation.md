---
solution: Journey Optimizer
product: journey optimizer
title: De afstemmingsactiviteit gebruiken
description: Leer hoe u de verzoeningsactiviteit kunt gebruiken in een geordende campagne
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---


# Afstemming {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation"
>title="Afstemmingsactiviteit"
>abstract="De **Verzoening** activiteit is a **richtend** activiteit die u toestaat om het verband tussen Adobe Journey Optimizer en de gegevens in een het werklijst te bepalen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_field"
>title="Selectieveld Afstemmen"
>abstract="Selectieveld Afstemmen"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_condition"
>title="Afstemming maken, voorwaarde"
>abstract="Afstemming maken, voorwaarde"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_complement"
>title="Afstemming genereren"
>abstract="Afstemming genereren"

De **[!UICONTROL Reconciliation]** -activiteit is een **[!UICONTROL Targeting]** -activiteit waarmee u de koppeling kunt definiëren tussen de gegevens in Adobe Journey Optimizer en de gegevens in een werktabel, bijvoorbeeld gegevens die uit een extern bestand zijn geladen.

Met de activiteit **[!UICONTROL Enrichment]** kunt u aanvullende gegevens toevoegen aan uw geordende campagne, bijvoorbeeld door gegevens uit meerdere bronnen te combineren of door een koppeling naar een tijdelijke bron te maken. De **[!UICONTROL Reconciliation]** -activiteit wordt daarentegen gebruikt om niet-geïdentificeerde of externe gegevens te koppelen aan bestaande bronnen in de database.

**[!UICONTROL Reconciliation]** vereist dat de verwante records al in het systeem bestaan. Als u bijvoorbeeld een aankoopbestand importeert waarin producten, tijdstempels en klantgegevens worden vermeld, moeten zowel de producten als de klanten al aanwezig zijn in de database om de koppeling tot stand te brengen.

## De afstemmingsactiviteit configureren {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="Doeldimensie"
>abstract="Selecteer de nieuwe doeldimensie. Met een dimensie kunt u de doelgroep definiëren: ontvangers, abonnees van apps, operators, abonnees, enzovoort. Standaard is de huidige doeldimensie geselecteerd."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="Afstemmingsregels"
>abstract="Selecteer afstemmingsregels die u wilt gebruiken voor de deduplicatie. Om attributen te gebruiken, selecteer de **Eenvoudige attributen** optie en kies de bron en bestemmingsgebieden. Om uw eigen verzoeningsvoorwaarde tot stand te brengen gebruikend de regelbouwer, selecteer de **Geavanceerde verzoeningsvoorwaarden** optie."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting_selection"
>title="Doeldimensie selecteren"
>abstract="Selecteer het richten afmeting voor uw binnenkomende gegevens met elkaar in overeenstemming te brengen."
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html?lang=nl-NL#targeting-dimensions" text="Doelafmetingen"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="Niet-compatibele gegevens behouden"
>abstract="Door gebrek, worden de niet in overeenstemming gebrachte gegevens gehouden in de uitgaande overgang en beschikbaar in de werklijst voor toekomstig gebruik. Om onverenigde gegevens te verwijderen, desactiveer **houden unconiled gegevens** optie."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="Afstemmingskenmerk"
>abstract="Selecteer het kenmerk dat u wilt gebruiken om gegevens op elkaar af te stemmen en klik op Bevestigen."

Voer de volgende stappen uit om de **[!UICONTROL Reconciliation]** -activiteit te configureren:

1. Voeg een **[!UICONTROL Reconciliation]** -activiteit toe aan het canvas.

1. Kies een nieuwe doeldimensie om te bepalen wie u richt zoals ontvangers of abonnees.

1. Stel de velden in die u wilt gebruiken om inkomende gegevens af te stemmen op bestaande profielen.

1. Selecteer **[!UICONTROL Simple attributes]** als u gegevens met behulp van basisvelden wilt afstemmen.

1. Stel de overeenkomende velden in:

   * **[!UICONTROL Source]**: geeft een lijst weer van de binnenkomende gegevensvelden.

   * **[!UICONTROL Destination]**: verwijst naar velden in de geselecteerde doeldimensie.

   Er treedt een overeenkomst op wanneer beide waarden gelijk zijn, bijvoorbeeld wanneer **[!UICONTROL Email]** de profielen definieert.

   ![](../assets/workflow-reconciliation-criteria.png)

1. Klik op **[!UICONTROL Add rule]** als u meer overeenkomende regels wilt toevoegen. Er moet aan alle voorwaarden worden voldaan voordat een overeenkomst plaatsvindt.

1. Kies **[!UICONTROL Advanced reconciliation conditions]** voor complexere voorwaarden. Gebruik de [&#x200B; regelbouwer &#x200B;](../orchestrated-rule-builder.md) om douanelogica te bepalen.

1. Als u wilt filteren welke gegevens moeten worden afgestemd, klikt u op **[!UICONTROL Create filter]** en definieert u de voorwaarde in de regelbouwer.

1. Door gebrek, worden de niet afgedekte verslagen gehouden in de uitgaande overgang en in de werklijst opgeslagen. Schakel de optie **[!UICONTROL Keep unreconciled data]** in als u deze wilt verwijderen.

## Voorbeeld {#example-reconciliation}

In dit voorbeeld wordt de **[!UICONTROL Reconciliation]** -activiteit in Adobe Journey Optimizer gebruikt om ervoor te zorgen dat e-mails alleen naar herkende klanten worden verzonden. De gegevens lopen door een **[!UICONTROL Read Audience]** -activiteit die gericht is op gebruikers met eerdere bestellingen. De **[!UICONTROL Reconciliation]** -activiteit komt deze inkomende gegevens vervolgens overeen met de bestaande profielen in de database via het e-mailveld.

![](../assets/workflow-reconciliation-sample-1.0.png)
