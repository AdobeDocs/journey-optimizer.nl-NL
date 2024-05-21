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
source-git-commit: 4d4ce1e892d51393972973950e8e03259e16c204
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Adobe Experience Platform-gegevens gebruiken voor personalisatie (bèta) {#aep-data}

>[!AVAILABILITY]
>
>Deze functie is momenteel alleen beschikbaar als een persoonlijke bètaversie.
>
>Momenteel is deze alleen beschikbaar voor testdoeleinden in de niet-productiesandbox die u aan de Adobe hebt geleverd en voor de gegevenssets die voor de bètaversie zijn aangevraagd.

Met Journey Optimizer kunt u gegevens van Adobe Experience Platform in de expressieeditor benutten voor [uw inhoud personaliseren](../personalization/personalize.md). De stappen zijn als volgt:

1. Open de uitdrukkingsredacteur, die in elke context beschikbaar is waar u verpersoonlijking zoals berichten kunt bepalen. [Leer hoe u met de expressieeditor werkt](../personalization/personalization-build-expressions.md)

1. Ga naar de lijst met hulpfuncties en voeg de **datasetLookup** hulpfunctie aan de coderuit.

   ![](assets/aep-data-helper.png)

1. Deze functie verstrekt een vooraf bepaalde syntaxis om u toe te staan om gebieden van uw datasets van Adobe Experience Platform te roepen. De syntaxis is als volgt:

   ```
   {{entity.datasetId="datasetId" id="key" result="store"}}
   ```

   * **entiteit.datasetId** is identiteitskaart van de dataset u met werkt;
   * **id** het veld dat als primaire identiteit in de gegevensset wordt gebruikt;

     >[!NOTE]
     >
     >De ingevoerde waarde voor dit veld kan de veld-id (*profile.couponValue*), een veld dat wordt doorgegeven tijdens een reisgebeurtenis (*context.trip.events.event_ID.couponValue*), of een statische waarde (*couponAbcd*). In elk geval, zal het systeem de waarde en raadpleging in de dataset gebruiken om te controleren of het een sleutel aanpast).

   * **resultaat** is een willekeurige naam die u moet opgeven om naar alle veldwaarden te verwijzen die u van de dataset gaat ophalen. Deze waarde wordt in de code gebruikt om elk veld aan te roepen.

   +++Waar om een dataset ID terug te winnen?

   Dataset-id&#39;s kunnen worden opgehaald in de gebruikersinterface van Adobe Experience Platform. Leer hoe te met datasets in te werken [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"}.

   ![](assets/aep-data-dataset.png)

+++

   +++Hoe te om een primair identiteitsgebied in een dataset te identificeren?

   Het gebied dat als primaire identiteit voor een bepaalde dataset is bepaald kan in het schema worden gevonden verbonden aan de dataset. Leer hoe u met identiteitsvelden werkt in het dialoogvenster [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity){target="_blank"}.

   ![](assets/aep-data-identity.png)

+++

1. Pas de syntaxis aan uw wensen aan. In dit voorbeeld willen we gegevens ophalen over de vluchten van passagiers. De syntaxis is als volgt:

   ```
   {{entity.datasetId="1234567890abcdtId" id="profile.personalEmail.address" result="flight"}}
   ```

   * We werken in de dataset met als id &quot;1234567890abcdtId&quot;,
   * Het veld dat als primaire sleutel in deze gegevensset wordt gebruikt, is het e-mailadres.
   * We willen alle veldwaarden opnemen onder de &quot;vlucht&quot;-referentie.

1. Zodra de syntaxis om in de dataset van Adobe Experience Platform te roepen is gevormd, kunt u specificeren welke gebieden u wilt terugwinnen. De syntaxis is als volgt:

   ```
   {{result.fieldId}}
   ```

   * **resultaat** is de waarde die u hebt toegewezen aan de **resultaat** in de **MultiEntiteit** helperfunctie. In dit voorbeeld &quot;vlucht&quot;.
   * **fieldID** Dit is de id van het veld dat u wilt ophalen. Deze id is zichtbaar in de gebruikersinterface van Adobe Experience Platform wanneer het doorbladeren van uw dataset. Vouw de onderstaande sectie uit om een voorbeeld weer te geven:

     +++Waar moet u een veld-id ophalen?

     Velden-id&#39;s kunnen worden opgehaald wanneer een voorbeeld van een gegevensset in de gebruikersinterface van Adobe Experience Platform wordt weergegeven. Leer hoe u een voorvertoning van gegevenssets kunt weergeven in het dialoogvenster [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}.

     ![](assets/aep-data-field.png)

+++

   In dit voorbeeld willen we informatie gebruiken over de instaptijd en -poort van de passagiers. Daarom voegen wij deze twee lijnen toe:

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. Nu de code gereed is, kunt u de inhoud op de gebruikelijke wijze voltooien en testen met de opdracht **Inhoud simuleren** om de personalisatie te controleren. [Leer hoe u inhoud kunt voorvertonen en testen](../content-management/preview-test.md)


   ![](assets/aep-data-sample.png)
