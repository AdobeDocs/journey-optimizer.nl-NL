---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform-gegevens gebruiken voor personalisatie (bèta)
description: Leer hoe u Adobe Experience Platform-gegevens kunt gebruiken voor personalisatie.
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expression, editor
hidefromtoc: true
hide: true
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
source-git-commit: a03541b5f1d9c799c30bf1d38b6f187d94c21dff
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 0%

---

# Adobe Experience Platform-gegevens gebruiken voor personalisatie (bèta) {#aep-data}

>[!AVAILABILITY]
>
>Deze functie is momenteel alleen beschikbaar als een persoonlijke bètaversie.
>
>Voor nu, is het slechts beschikbaar voor het **e-mailkanaal** en voor testende doeleinden in de niet-productie zandbak u aan Adobe en voor de datasets die voor bèta wordt gevraagd hebt verstrekt.

Journey Optimizer staat u toe om gegevens van hefboomwerking van Adobe Experience Platform in de verpersoonlijkingsredacteur aan [ te personaliseren uw inhoud ](../personalization/personalize.md). De stappen zijn als volgt:

1. Open de verpersoonlijkingsredacteur, die in elke context beschikbaar is waar u verpersoonlijking zoals berichten kunt bepalen. [ Leer hoe te met de verpersoonlijkingsredacteur ](../personalization/personalization-build-expressions.md) te werken

1. Navigeer aan de lijst van helperfuncties en voeg **datasetLookup** hulpfunctie aan de coderuit toe.

   ![](assets/aep-data-helper.png)

1. Deze functie verstrekt een vooraf bepaalde syntaxis om u toe te staan om gebieden van uw datasets van Adobe Experience Platform te roepen. De syntaxis is als volgt:

   ```
   {{entity.datasetId="datasetId" id="key" result="store"}}
   ```

   * **entiteit.datasetId** is identiteitskaart van de dataset u met werkt.
   * **identiteitskaart** is identiteitskaart van de bronkolom die met de primaire identiteit van de opzoekdataset zou moeten worden aangesloten.

     >[!NOTE]
     >
     >De waarde ingegaan voor dit gebied kan of a gebied identiteitskaart (*profile.couponValue*) zijn, een gebied dat in een reisgebeurtenis (*context.trip.events.event_ID.couponValue*) wordt overgegaan, of een statische waarde (*couponAbcd*). In elk geval, zal het systeem de waarde en raadpleging in de dataset gebruiken om te controleren of het een sleutel aanpast.

   * **resultaat** is een willekeurige naam die u moet verstrekken om alle gebiedswaarden van verwijzingen te voorzien u van de dataset gaat terugwinnen. Deze waarde wordt in de code gebruikt om elk veld aan te roepen.

   +++Waar om een dataset ID terug te winnen?

   Dataset-id&#39;s kunnen worden opgehaald in de gebruikersinterface van Adobe Experience Platform. Leer hoe te met datasets in de [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets) te werken {target="_blank"}.

   ![](assets/aep-data-dataset.png)

+++

1. Pas de syntaxis aan uw wensen aan. In dit voorbeeld willen we gegevens ophalen over de vluchten van passagiers. De syntaxis is als volgt:

   ```
   {{entity.datasetId="1234567890abcdtId" id=profile.upcomingFlightId result="flight"}}
   ```

   * We werken in de dataset met als id &quot;1234567890abcdtId&quot;,
   * Het gebied wij willen gebruiken om zich aan te sluiten bij de blik omhoog dataset is *profile.upcomingFlightId*,
   * We willen alle veldwaarden opnemen onder de &quot;vlucht&quot;-referentie.

1. Zodra de syntaxis om in de dataset van Adobe Experience Platform te roepen is gevormd, kunt u specificeren welke gebieden u wilt terugwinnen. De syntaxis is als volgt:

   ```
   {{result.fieldId}}
   ```

   * **resultaat** is de waarde die u aan de **resultaat** parameter in de **MultiEntiteit** hulpfunctie hebt toegewezen. In dit voorbeeld &quot;vlucht&quot;.
   * **fieldID** is identiteitskaart van het gebied u wilt terugwinnen. Deze id is zichtbaar in de gebruikersinterface van Adobe Experience Platform wanneer het doorbladeren van uw dataset. Vouw de onderstaande sectie uit om een voorbeeld weer te geven:

     +++Waar moet u een veld-id ophalen?

     Velden-id&#39;s kunnen worden opgehaald wanneer een voorbeeld van een gegevensset in de gebruikersinterface van Adobe Experience Platform wordt weergegeven. Leer hoe te voorproef datasets in de [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#preview) {target="_blank"}.

     ![](assets/aep-data-field.png)

+++

   In dit voorbeeld willen we informatie gebruiken over de instaptijd en -poort van de passagiers. Daarom voegen wij deze twee lijnen toe:

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. Nu uw code klaar is, kunt u uw inhoud voltooien zoals gewoonlijk, en het testen gebruikend de **Simuleer inhoud** knoop om de verpersoonlijking te controleren. [ Leer hoe te om inhoud ](../content-management/preview-test.md) voor te vertonen en te testen


   ![](assets/aep-data-sample.png)
