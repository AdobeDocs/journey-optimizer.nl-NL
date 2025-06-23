---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform-gegevens gebruiken voor personalisatie (Beta)
description: Leer hoe u Adobe Experience Platform-gegevens kunt gebruiken voor personalisatie.
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expression, editor
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
source-git-commit: baca603427ebba9ecb843b3c8d219c40354dde0f
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---

# Adobe Experience Platform-gegevens gebruiken voor personalisatie{#aep-data}

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
>Deze functie is momenteel beschikbaar voor alle klanten als een openbare bètaversie.
>
>om dit vermogen te gebruiken, moet u bètatermijnen voor uw organisatie eerst goedkeuren die tonen wanneer het toevoegen van de nieuwe hulpfuncties &quot;datasetLookup&quot;in de verpersoonlijkingsredacteur.

Journey Optimizer staat u toe om gegevens van hefboomwerking van Adobe Experience Platform in de verpersoonlijkingsredacteur aan [ te personaliseren uw inhoud ](../personalization/personalize.md). Om dit te doen, moeten de datasets nodig voor raadplegingsverpersoonlijking eerst door een API vraag worden toegelaten zoals hieronder beschreven. Als u klaar bent, kunt u hun gegevens gebruiken om uw inhoud aan te passen aan [!DNL Journey Optimizer] .

## Beperkingen en richtlijnen voor Beta {#guidelines}

Controleer voordat u begint de volgende beperkingen en richtlijnen:

### Gegevensset inschakelen {#enablement}

* **grootte van de Dataset** is beperkt tot 5GB voor productiedatasets en 1GB voor dev zandbakdatasets
* **A maximum van 50 datasets kan** voor raadpleging per organisatie op elk ogenblik worden toegelaten.
* **Aantal verslagen** is beperkt tot 5M in productiedetecten en 1M in dev zandbakdatasets.
* **de Etikettering en de Handhaving van het Gebruik van Gegevens** wordt niet afgedwongen op dit ogenblik voor datasets die voor raadpleging worden toegelaten.
* **Datasets die voor raadpleging worden toegelaten en in verpersoonlijking worden gebruikt worden niet beschermd tegen schrapping**. Het is aan u om spoor te houden van welke datasets voor verpersoonlijking worden gebruikt om ervoor te zorgen zij niet worden geschrapt of worden verwijderd.

### Personalization gebruikt [!DNL Adobe Experience Platform] -gegevens {#perso}

* **Gesteunde kanalen**: Voor nu, is dit vermogen slechts beschikbaar voor gebruik binnen e-mail, SMS en direct-mailkanalen.
* **de Etikettering en de Handhaving van het Gebruik van Gegevens** wordt niet afgedwongen op dit ogenblik voor datasets die voor raadpleging worden toegelaten.
* **Fragments**: De verpersoonlijking van de raadpleging van de gegevensset kan niet binnen uitdrukking of visuele fragmenten op dit ogenblik worden geplaatst.

### Beslissing {#decisioning}

De mogelijkheid om [!DNL Adobe Experience Platform] datasets te gebruiken in Experience Decisioning-rangschikkingsformules en -regels komt binnenkort.

Wijzig in de tussentijd de onderstaande richtsnoeren:

* Een beslissingsbeleid is beperkt tot drie gegevensreeksen,
* Een besluitvormingsregel kan 3 datasets gebruiken,
* Een rangschikkingsformule kan 3 datasets gebruiken,
* Een besluitvormingsbeleid is beperkt tot 1000 verslagvragen.

>[!NOTE]
>
>Neem contact op met uw accountvertegenwoordiger als u toegang wilt tot deze functie

## Een dataset inschakelen voor gegevensopzoekhandeling {#enable}

Om gegevens van uw dataset voor verpersoonlijking te hefboomwerking, moet u een API vraag gebruiken om zijn status terug te winnen en de raadplegingsdienst toe te laten.

### Vereisten {#prerequisites-enable}

* Volg de richtingen die in [ worden gedetailleerd deze documentatie ](https://developer.adobe.com/journey-optimizer-apis/references/authentication/) om uw milieu te vormen om API bevelen te verzenden.
* De API&#39;s van Adobe Journey Optimizer en Adobe Experience Platform moeten aan het project worden toegevoegd.

  ![](assets/aep-data-api.png)

* U moet de toestemming van datasets als deel van uw rol leiden.
* Het schema waarvoor de dataset gebaseerd is moet a **primaire identiteit** bevatten die als raadplegingssleutel kan dienst doen.

### API-oproepstructuur {#call}

```
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}"
```

Waarbij:

* **URL** is `https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`
* **identiteitskaart van de Dataset** is de dataset waarvoor u wenst om toe te laten.
* **de Actie** laat OF onbruikbaar maakt toe.
* **het teken van de Toegang** kan van de ontwikkelaarsconsole worden teruggewonnen.
* **API sleutel** kan van de ontwikkelaarsconsole worden teruggewonnen.
* **IMS Org ID** is uw organisatie van Adobe.
* **Naam Sandbox** is de zandbaknaam de dataset in (d.w.z. prod, dev enz.) is.

>[!NOTE]
>
>Als u de hieronder weergegeven fout tegenkomt bij het proberen van een API-aanroep om gegevenssets in te schakelen, probeert u de Adobe Journey Optimizer API&#39;s uit uw project voor de ontwikkelaarsconsole te verwijderen en deze vervolgens opnieuw toe te voegen.
>
>```
>
>"error_code": "403003", 
>"message": "Api Key is invalid"
>
>```

## Gebruik een dataset voor verpersoonlijking {#leverage}

Zodra een dataset voor raadplegingsverpersoonlijking gebruikend een API vraag is toegelaten, kunt u zijn gegevens gebruiken om uw inhoud in [!DNL Journey Optimizer] te personaliseren.

1. Open de verpersoonlijkingsredacteur, die in elke context beschikbaar is waar u verpersoonlijking zoals berichten kunt bepalen. [ Leer hoe te met de verpersoonlijkingsredacteur ](../personalization/personalization-build-expressions.md) te werken

1. Navigeer aan de lijst van helperfuncties en voeg **datasetLookup** hulpfunctie aan de coderuit toe.

   ![](assets/aep-data-helper.png)

1. Deze functie verstrekt een vooraf bepaalde syntaxis om u toe te staan om gebieden van uw datasets van Adobe Experience Platform te roepen. De syntaxis is als volgt:

   ```
   {{datasetLookup datasetId="datasetId" id="key" result="store" required=false}}
   ```

   * **datasetId** is identiteitskaart van de dataset u met werkt.
   * **identiteitskaart** is identiteitskaart van de bronkolom die met de primaire identiteit van de opzoekdataset zou moeten worden aangesloten.

     >[!NOTE]
     >
     >De waarde ingegaan voor dit gebied kan of a gebied identiteitskaart (*profile.packages.packageSKU*) zijn, een gebied dat in een reisgebeurtenis (*context.trip.events.event_ID.productSKU*) wordt overgegaan, of een statische waarde (*sku007653*). In elk geval, zal het systeem de waarde en raadpleging in de dataset gebruiken om te controleren of het een sleutel aanpast.
     >
     >Als u een letterlijke tekenreekswaarde voor de toets gebruikt, moet u de tekst tussen aanhalingstekens plaatsen. Bijvoorbeeld: `{{datasetLookup datasetId="datasetId" id="SKU1234" result="store" required=false}}` . Als u een kenmerkwaarde gebruikt als een dynamische sleutel, verwijdert u de aanhalingstekens. Voorbeeld: `{{datasetLookup datasetId="datasetId" id=category.product.SKU result="SKU" required=false}}`

   * **resultaat** is een willekeurige naam die u moet verstrekken om alle gebiedswaarden van verwijzingen te voorzien u van de dataset gaat terugwinnen. Deze waarde wordt in de code gebruikt om elk veld aan te roepen.

   * **required=false**: Als vereist aan WAAR wordt geplaatst, zal het bericht slechts worden geleverd als een passende sleutel wordt gevonden. Indien ingesteld op false, is geen overeenkomende sleutel vereist en kan het bericht nog steeds worden bezorgd. Houd er rekening mee dat als de waarde false is, u in de berichtinhoud een back-up- of standaardwaarde moet opgeven.

   +++Waar om een dataset ID terug te winnen?

   Dataset-id&#39;s kunnen worden opgehaald in de gebruikersinterface van Adobe Experience Platform. Leer hoe te met datasets in de [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/nl/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"} te werken.

   ![](assets/aep-data-dataset.png)

   +++

1. Pas de syntaxis aan uw wensen aan. In dit voorbeeld willen we gegevens ophalen over de vluchten van passagiers. De syntaxis is als volgt:

   ```
   {{datasetLookup datasetId="1234567890abcdtId" id=profile.upcomingFlightId result="flight"}}
   ```

   * We werken in de dataset met als id &quot;1234567890abcdtId&quot;,
   * Het gebied wij willen gebruiken om zich aan te sluiten bij de blik omhoog dataset is *profile.upcomingFlightId*,
   * We willen alle veldwaarden opnemen onder de &quot;vlucht&quot;-referentie.

1. Zodra de syntaxis om in de dataset van Adobe Experience Platform te roepen is gevormd, kunt u specificeren welke gebieden u wilt terugwinnen. De syntaxis is als volgt:

   ```
   {{result.fieldId}}
   ```

   >[!NOTE]
   >
   >Wanneer het van verwijzingen voorzien van een datasetgebied, zorg ervoor dat u de volledige die gebiedspad zoals binnen het schema wordt bepaald aanpast.

   * **resultaat** is de waarde die u aan de **resultaat** parameter in de **MultiEntiteit** hulpfunctie hebt toegewezen. In dit voorbeeld &quot;vlucht&quot;.
   * **fieldID** is identiteitskaart van het gebied u wilt terugwinnen. Deze id is zichtbaar in de gebruikersinterface van [!DNL Adobe Experience Platform] wanneer het doorbladeren van het recordschema met betrekking tot uw dataset:

     +++Waar moet u een veld-id ophalen?

     Velden-id&#39;s kunnen worden opgehaald wanneer een voorbeeld van een gegevensset in de gebruikersinterface van Adobe Experience Platform wordt weergegeven. Leer hoe te voorproef datasets in de [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/nl/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}.

     ![](assets/aep-data-field.png)

     +++

   In dit voorbeeld willen we informatie gebruiken over de instaptijd en -poort van de passagiers. Daarom voegen wij deze twee lijnen toe:

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. Nu uw code klaar is, kunt u uw inhoud voltooien zoals gewoonlijk, en het testen gebruikend de **Simuleer inhoud** knoop om de verpersoonlijking te controleren. [ Leer hoe te om inhoud ](../content-management/preview-test.md) voor te vertonen en te testen


   ![](assets/aep-data-sample.png)
