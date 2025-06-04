---
solution: Journey Optimizer
product: journey optimizer
title: De afstemmingsactiviteit gebruiken
description: Leer hoe u de verzoeningsactiviteit kunt gebruiken in een georkestreerde campagne
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: 7f535b87e415ae9191199b34476adb5c977b66e9
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 6%

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

De **Verzoening** activiteit is a **richtend** activiteit die u toestaat om het verband tussen de gegevens in Adobe Journey Optimizer en de gegevens in een het werklijst te bepalen, bijvoorbeeld gegevens die van een extern dossier worden geladen.

## Best practices {#reconciliation-best-practices}

Terwijl de **Verrijking** activiteit u toestaat om extra gegevens te bepalen in uw georkestreerde campagne (u kunt een **Verrijking** activiteit gebruiken om gegevens te combineren die uit veelvoudige reeksen komen, of verbindingen tot stand te brengen aan een tijdelijk middel), staat de **Verzoening** activiteit u toe om ongeidentificeerde gegevens aan bestaande middelen te verbinden.

>[!NOTE]
>De afstemmingsoperatie houdt in dat de gegevens van de gekoppelde afmetingen al in de database staan.  Als u bijvoorbeeld een aankoopbestand importeert waarin wordt aangegeven welk product is gekocht, op welk moment, door welke klant, enzovoort, moeten het product en de klant al in de database aanwezig zijn.

## De afstemmingsactiviteit configureren {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="Doeldimensie"
>abstract="Selecteer de nieuwe doeldimensie. Met een dimensie kunt u de doelgroep definiëren: ontvangers, abonnees van apps, operators, abonnees, enzovoort. Standaard is de huidige doeldimensie geselecteerd."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="Afstemmingsregels"
>abstract="Selecteer afstemmingsregels die u wilt gebruiken voor de deduplicatie. Om attributen te gebruiken, selecteer de **Eenvoudige attributen** optie en kies de bron en bestemmingsgebieden. Om uw eigen verzoeningsvoorwaarde tot stand te brengen gebruikend de vraagmodeler, selecteer de **Geavanceerde verzoeningsvoorwaarden** optie."
>additional-url="https://experienceleague.adobe.com/en/docs/campaign-web/v8/query-database/query-modeler-overview" text="Werken met de querymodelfunctie"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting_selection"
>title="Doeldimensie selecteren"
>abstract="Selecteer het richten afmeting voor uw binnenkomende gegevens met elkaar in overeenstemming te brengen."
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html#targeting-dimensions" text="Doelafmetingen"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="Niet-compatibele gegevens behouden"
>abstract="Door gebrek, worden de niet in overeenstemming gebrachte gegevens gehouden in de uitgaande overgang en beschikbaar in de werklijst voor toekomstig gebruik. Om onverenigde gegevens te verwijderen, desactiveer **houden unconiled gegevens** optie."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="Afstemmingskenmerk"
>abstract="Selecteer het kenmerk dat u wilt gebruiken om gegevens op elkaar af te stemmen en klik op Bevestigen."

Volg deze stappen om de **Verzoening** activiteit te vormen:

1. Voeg de activiteit van de a **Verzoening** in uw georkestreerde campagne toe.

1. Selecteer de nieuwe doeldimensie. Met een dimensie kunt u de doelgroep definiëren: ontvangers, abonnees van apps, operators, abonnees, enzovoort.

1. Selecteer de velden die u wilt gebruiken voor de afstemming. U kunt een of meer verzoeningscriteria gebruiken.

   1. Om attributen te gebruiken om gegevens te combineren, selecteer de **Eenvoudige attributen** optie. Het **Source** gebied maakt een lijst van de gebieden beschikbaar in de inputovergang, die moeten worden in overeenstemming gebracht. Het **gebied van de Bestemming** beantwoordt aan de gebieden van geselecteerde het richten afmeting. De gegevens worden in overeenstemming gebracht wanneer bron en bestemming gelijk zijn. Bijvoorbeeld, selecteer de **E-mail** gebieden om profielen te dedupliceren die op hun e-mailadres worden gebaseerd.

      Om andere verzoeningscriteria toe te voegen, klik **regel** toevoegen knoop. Als er meerdere samenvoegvoorwaarden zijn opgegeven, moeten deze ALLES worden gecontroleerd zodat de gegevens aan elkaar kunnen worden gekoppeld.

      ![](../assets/workflow-reconciliation-criteria.png)

   1. Om andere attributen te gebruiken om gegevens te combineren, selecteer de **Geavanceerde verzoeningsvoorwaarden** optie. U kunt dan uw eigen verzoeningsvoorwaarde tot stand brengen gebruikend de vraagmodeler.

1. U kunt gegevens filtreren om het gebruiken van te verzoenen **creeer filterknoop**. Hiermee kunt u een aangepaste voorwaarde maken met behulp van de querymodelfunctie.

Door gebrek, worden de niet in overeenstemming gebrachte gegevens gehouden in de uitgaande overgang en beschikbaar in de werkbare lijst voor toekomstig gebruik. Om onverenigde gegevens te verwijderen, desactiveer **houden unconiled gegevens** optie.
