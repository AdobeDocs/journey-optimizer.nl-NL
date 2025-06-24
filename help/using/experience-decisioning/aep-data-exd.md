---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform-gegevens gebruiken voor beslissingen (Beta)
description: Leer hoe u Adobe Experience Platform-gegevens kunt gebruiken voor beslissingen.
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expression, editor
exl-id: 46d868b3-01d2-49fa-852b-8c2e2f54292f
source-git-commit: ebefeb59a19e831ec7f86cee690a35fe71e14554
workflow-type: tm+mt
source-wordcount: '823'
ht-degree: 0%

---

# Adobe Experience Platform-gegevens gebruiken voor beslissingen {#aep-data}

>[!CONTEXTUALHELP]
>id="ajo_exd_rules_dataset_lookup"
>title="Gegevensset opzoeken"
>abstract="Door Adobe Experience Platform-gegevens in besluitvormingsregels te gebruiken, kunt u geschiktheidscriteria definiëren op basis van dynamische, externe kenmerken, zodat beslissingsitems alleen worden weergegeven wanneer dat relevant is. Maak een toewijzing om te definiëren hoe de Adobe Experience Platform-gegevensset wordt gekoppeld aan gegevens in [!DNL Journey Optimizer] . Selecteer de dataset met de attributen u nodig hebt en kies een het aansluiten van sleutel die in zowel de attributen van het besluitvormingspunt als de dataset bestaat."

>[!CONTEXTUALHELP]
>id="ajo_exd_formula_dataset_lookup"
>title="Gegevensset opzoeken"
>abstract="De rangschikkingsformules bepalen de prioriteit van besluitvormingspunten. Met de gegevenssetkenmerken van [!DNL Adobe Experience Platform] kunt u de waarderingslogica dynamisch aanpassen aan de omstandigheden in de praktijk. Maak een toewijzing om te definiëren hoe de Adobe Experience Platform-gegevensset wordt gekoppeld aan gegevens in [!DNL Journey Optimizer] . Selecteer de dataset met de attributen u nodig hebt en kies een het aansluiten sleutel die in zowel de attributen van het besluitvormingspunt als de dataset bestaat"

>[!AVAILABILITY]
>
>Deze mogelijkheid is momenteel beschikbaar voor alle klanten als een openbare bètaversie. Neem contact op met uw accountvertegenwoordiger als u toegang wilt.

Met [!DNL Journey Optimizer] kunt u gegevens van [!DNL Adobe Experience Platform] gebruiken om te beslissen. Dit staat u toe om de definitie van uw beslissingsattributen tot extra gegevens in datasets voor bulkupdates uit te breiden die periodiek veranderen zonder het moeten manueel de attributen één voor één bijwerken. Bijvoorbeeld beschikbaarheid, wachttijden, enz.

## Beperkingen en richtlijnen voor Beta {#guidelines}

Neem voordat u begint de volgende beperkingen en richtlijnen in acht:

* Een besluitvormingsbeleid kan tot 3 datasets totaal, over al zijn besluitvormingsregels en rangschikkingsformules samen verwijzen. Bijvoorbeeld, als uw regels 2 datasets gebruiken, kunnen uw formules slechts 1 extra dataset gebruiken.
* Een beslissingsregel kan 3 datasets gebruiken.
* Een rangschikkende formule kan 3 datasets gebruiken.
* Wanneer een besluitbeleid wordt geëvalueerd, zal het systeem tot 1000 datasetvragen (raadplegingen) in totaal uitvoeren. Elke datasetafbeelding die door een besluitpuntentellingen als één vraag wordt gebruikt. Voorbeeld: Als een besluitpunt 2 datasets gebruikt, evaluerend die aanbiedingen tellen als 2 vragen naar de 1000-vraaggrens.

## Een dataset inschakelen voor gegevensopzoekhandeling {#enable}

Als u gegevens uit een [!DNL Adobe Experience Platform] -dataset wilt gebruiken voor besluitvorming, moet u deze eerst inschakelen voor opzoeken via een API-aanroep. Voor gedetailleerde instructies, verwijs naar deze sectie: [ de datasets van Adobe Experience Platform van de Leverage in Journey Optimizer ](../data/lookup-aep-data.md).

## Adobe Experience Platform-gegevens gebruiken voor beslissingen

Zodra een dataset voor raadpleging wordt toegelaten, kunt u zijn attributen gebruiken om uw besluitvormingslogica met externe gegevens te verrijken. Dit is vooral nuttig voor attributen die vaak veranderen, zoals productbeschikbaarheid, of prijs in real time.

Kenmerken van Adobe Experience Platform-gegevenssets kunnen worden gebruikt in twee delen van besluitvormingslogica:

* **Regels van het Besluit**: Bepaal of een besluitvormingspunt verkiesbaar is om te worden getoond.
* **het Rangschikken Formulas**: Geef voorrang aan besluitvormingspunten die op externe gegevens worden gebaseerd.

In de volgende secties wordt uitgelegd hoe u Adobe Experience Platform-gegevens in beide contexten kunt gebruiken.

### Besluitvormingsregels {#rules}

Door Adobe Experience Platform-gegevens in besluitvormingsregels te gebruiken, kunt u geschiktheidscriteria definiëren op basis van dynamische, externe kenmerken, zodat beslissingsitems alleen worden weergegeven wanneer dat relevant is.

Een online retailer wil bijvoorbeeld productaanbevelingen promoten op basis van de lokale winkelvoorraad. Een product mag alleen voor een aanbeveling in aanmerking komen als het op de dichtstbijzijnde locatie in voorraad is. Een dataset met dagelijkse inventarisupdates wordt geüpload naar Adobe Experience Platform. De regellogica controleert of de `inventory_count` voor een bepaald product groter is dan 0 voor de voorkeurswinkel van de klant. Zo ja, dan is de beslissingspost subsidiabel.

Voer de volgende stappen uit om Adobe Experience Platform-gegevens te gebruiken voor besluitvormingsregels:

1. Ga naar **[!UICONTROL Strategy setup]** / **[!UICONTROL Decision rules]** en selecteer **[!UICONTROL Create rule with dataset]** .

   ![](assets/exd-lookup-rule.png)

1. Klik op **[!UICONTROL Create mapping]** om te definiëren hoe de Adobe Experience Platform-gegevensset wordt gekoppeld aan gegevens in [!DNL Journey Optimizer] .

   * Selecteer de dataset met de attributen u wenst.
   * Kies een verbindingssleutel (bijvoorbeeld product-id of winkel-id) die bestaat in zowel de kenmerken van het beslissingstitem als de gegevensset.

   ![](assets/exd-lookup-mapping.png)

   >[!NOTE]
   >
   >U kunt maximaal 3 toewijzingen per regel maken.

1. Klik op **[!UICONTROL Continue]**. U kunt nu de gegevenssetkenmerken openen in het menu **[!UICONTROL Dataset Lookup]** en deze gebruiken in uw regelvoorwaarden. [ Leer hoe te om een besluitvormingsregel ](../experience-decisioning/rules.md#create) tot stand te brengen

   ![](assets/exd-lookup-menu.png)

### Beoordelingsformule

De rangschikkingsformules bepalen de prioriteit van besluitvormingspunten. Met de gegevenssetkenmerken van [!DNL Adobe Experience Platform] kunt u de waarderingslogica dynamisch aanpassen aan de omstandigheden in de praktijk.

Stel bijvoorbeeld dat een luchtvaartmaatschappij een rangschikkingsformule gebruikt om upgradeaanbiedingen prioriteit te geven. Als een klant een hoge loyaliteitsrij heeft en de huidige zetelbeschikbaarheid laag is (die op een dataset wordt gebaseerd die uurs wordt bijgewerkt), worden zij hogere prioriteit gegeven. De dataset bevat velden zoals `flight_number` , `available_seats` en `loyalty_score` .

Voer de volgende stappen uit om Adobe Experience Platform-gegevens te gebruiken in rangschikkingsformules:

1. Een waarderingsformule maken of bewerken. Klik in de sectie **[!UICONTROL Dataset lookup]** op **[!UICONTROL Create mapping]** .

1. Bepaal de datasetafbeelding:

   * Selecteer de juiste gegevensset (bv. beschikbaarheid van de zitplaatsen via de vlucht).
   * Kies een verbindingssleutel (bijvoorbeeld vluchtnummer of klant-id) die in zowel de kenmerken van het beslissingspunt als de gegevensset bestaat.

   ![](assets/exd-lookup-formula-mapping.png)

   >[!NOTE]
   >
   >U kunt maximaal 3 toewijzingen per waarderingsformule maken.

1. Gebruik de datasetgebieden om uw het rangschikken formule zoals gebruikelijk te bouwen. [ Leer hoe te om een het rangschikken formule ](../experience-decisioning/exd-ranking-formulas.md#create-ranking-formula) tot stand te brengen

   ![](assets/exd-lookup-formula-criteria.png)
