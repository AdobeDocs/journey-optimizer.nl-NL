---
title: Een testprofiel maken
description: Leer hoe u een testprofiel maakt
feature: Journeys
topic: Contentmanagement
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 1%

---

# Testprofielen maken {#create-test-profiles}

![](../assets/do-not-localize/badge.png)

Testprofielen zijn vereist wanneer de testmodus op een reis wordt gebruikt. U kunt een [bestaand profiel](../building-journeys/creating-test-profiles.md#turning-profile-into-test) omzetten in een testprofiel of [een testprofiel maken](../building-journeys/creating-test-profiles.md#create-test-profiles-csv). Raadpleeg [deze sectie](../building-journeys/testing-the-journey.md) voor meer informatie over het gebruik van de testmodus.

Er zijn verschillende manieren om een testprofiel te maken in Adobe Experience Platform. In deze documentatie richten wij ons op twee methodes: uploaden van een [csv-bestand](../building-journeys/creating-test-profiles.md#create-test-profiles-csv) en gebruiken van [API-aanroepen](../building-journeys/creating-test-profiles.md#create-test-profiles-api). U kunt een jsdossier in een dataset ook uploaden, verwijs naar [de documentatie van de Ingestie van Gegevens](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html#add-data-to-dataset).

Het maken van een testprofiel lijkt op het maken van gewone profielen in Adobe Experience Platform. Raadpleeg de documentatie [Real-time Klantprofiel](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html) voor meer informatie.

## Vereisten{#test-profile-prerequisites}

Om profielen te kunnen tot stand brengen, moet u eerst een schema en een dataset in Adobe [!DNL Journey Optimizer] tot stand brengen.

Eerst, moet u **een schema** creëren. Voer de volgende stappen uit:

1. Klik in de sectie ADMINISTRATIE op **[!UICONTROL Schemas]**.
   ![](../assets/test-profiles-0.png)
1. Klik **[!UICONTROL Create schema]**, in het hoogste recht, dan selecteer een schematype, bijvoorbeeld **XDM Individual Profile**.
   ![](../assets/test-profiles-1.png)
1. Selecteer de juiste veldgroepen. Voeg de **Profieltestdetails** veldgroep toe.
   ![](../assets/test-profiles-1-ter.png)
Klik eenmaal op  **[!UICONTROL Add field groups]**: de lijst van gebiedsgroepen wordt getoond op het schema overzichtsscherm.
   ![](../assets/test-profiles-2.png)

   >[!NOTE]
   >
   >* Klik op de naam van het schema om het te wijzigen en de eigenschappen ervan bij te werken.
      >
      >
   * Klik op de knop **[!UICONTROL Add]** in de sectie Veldgroepen om andere veldgroepen te selecteren die u wilt toevoegen in het schema


1. Klik in de lijst met velden op het veld dat u als primaire identiteit wilt definiëren.
   ![](../assets/test-profiles-3.png)
1. Controleer in het rechterdeelvenster **[!UICONTROL Field properties]** de opties ****[!UICONTROL Identity]** en ****[!UICONTROL Primary Identity]** en selecteer een naamruimte. Als u wilt dat de primaire identiteit een e-mailadres is, kiest u de naamruimte **E-mail**. Klik **Toepassen**.
   ![](../assets/test-profiles-4.png)
1. Selecteer het schema en schakel de optie **[!UICONTROL Profile]** in **[!UICONTROL Schema properties]** in.
   ![](../assets/test-profiles-5.png)
1. Klik **Opslaan**.

>[!NOTE]
>
>Voor meer informatie over schemaverwezenlijking, verwijs naar [XDM documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#prerequisites).

Dan moet u **de dataset** creëren waarin de profielen zullen worden ingevoerd. Voer de volgende stappen uit:

1. Blader naar **[!UICONTROL Datasets]** en klik vervolgens op **[!UICONTROL Create dataset]**.
   ![](../assets/test-profiles-6.png)
1. Kies **[!UICONTROL Create dataset from schema]**.
   ![](../assets/test-profiles-7.png)
1. Selecteer het eerder gemaakte schema en klik op **[!UICONTROL Next]**.
   ![](../assets/test-profiles-8.png)
1. Kies een naam en klik op **[!UICONTROL Finish]**.
   ![](../assets/test-profiles-9.png)
1. Schakel de optie **[!UICONTROL Profile]** in.
   ![](../assets/test-profiles-10.png)

>[!NOTE]
>
> Raadpleeg de documentatie [Catalog Service](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#getting-started) voor meer informatie over het maken van gegevenssets.

## Een profiel omzetten in een testprofiel{#turning-profile-into-test}

U kunt een bestaand profiel omzetten in een testprofiel: u kunt profielkenmerken op dezelfde manier bijwerken als wanneer u een profiel maakt.

Een eenvoudige manier om dit te doen is door een **[!UICONTROL Update profile]** actieactiviteit in een reis te gebruiken en het testProfile booleaanse gebied te veranderen van vals in waar.

Uw reis zal bestaan uit een **[!UICONTROL Read segment]** en een **[!UICONTROL Update profile]** activiteit. Eerst moet u een segment maken dat zich richt op de profielen die u wilt omzetten in testprofielen.

>[!NOTE]
>
> Aangezien u het veld **testProfile** bijwerkt, moeten de gekozen profielen dit veld bevatten. Het verwante schema moet de **Proefdetails van het Profiel** mengen hebben. Zie [deze sectie](../building-journeys/creating-test-profiles.md#test-profiles-prerequisites).

1. Blader naar **Segmenten** en **Segment maken** in de rechterbovenhoek.
   ![](../assets/test-profiles-22.png)
1. Bepaal een naam voor uw segment en bouw het segment: Selecteer de velden en de waarden die u als doel wilt instellen.
   ![](../assets/test-profiles-23.png)
1. Klik op **Opslaan** en controleer of de profielen correct zijn ingesteld door het segment.
   ![](../assets/test-profiles-24.png)

   >[!NOTE]
   >
   > Het berekenen van segmenten kan enige tijd in beslag nemen. Leer meer op segmenten in [deze sectie](../segment/about-segments.md).

1. Maak nu een nieuwe reis en begin met een orkestactiviteit **[!UICONTROL Read segment]**.
1. Kies het eerder gemaakte segment en de naamruimte die uw profielen gebruiken.
   ![](../assets/test-profiles-25.png)
1. Voeg een **[!UICONTROL Update profile]** actieactiviteit toe.
1. Selecteer het schema, het **testProfiles** gebied, de dataset en de waarde plaatsen aan **True**. Om dit, op het **[!UICONTROL VALUE]** gebied uit te voeren, klik **Pen** pictogram op het recht, selecteer **[!UICONTROL Advanced mode]** en ga **true** in.
   ![](../assets/test-profiles-26.png)
1. Voeg een **End** activiteit toe en klik **[!UICONTROL Publish]**.
1. Controleer in de sectie **[!UICONTROL Segments]** of de profielen correct zijn bijgewerkt.
   ![](../assets/test-profiles-28.png)

   >[!NOTE]
   >
   > Raadpleeg [deze sectie](../building-journeys/update-profiles.md) voor meer informatie over de **[!UICONTROL Update profile]**-activiteit.

## Een testprofiel maken met een CSV-bestand{#create-test-profiles-csv}

In Adobe Experience Platform kunt u profielen maken door een CSV-bestand met de verschillende profielvelden te uploaden naar uw gegevensset. Dit is de eenvoudigste methode.

1. Maak een eenvoudig CSV-bestand met behulp van een spreadsheetsoftware.
1. Voeg één kolom toe voor elk nodig veld. Voeg het primaire identiteitsveld (&quot;personID&quot; in het bovenstaande voorbeeld) en het veld &quot;testProfile&quot; toe op &quot;true&quot;.
   ![](../assets/test-profiles-11.png)
1. Voeg één regel per profiel toe en vul de waarden voor elk veld in.
   ![](../assets/test-profiles-12.png)
1. Sla het werkblad op als een CSV-bestand. Controleer of komma&#39;s als scheidingstekens worden gebruikt.
1. Blader naar Adobe Experience Platform **Workflows**.
   ![](../assets/test-profiles-14.png)
1. Kies **CSV toewijzen aan XDM-schema** en klik vervolgens op **Starten**.
   ![](../assets/test-profiles-16.png)
1. Selecteer de dataset u de profielen in wilt invoeren. Klik op **Next**.
   ![](../assets/test-profiles-17.png)
1. Klik **Kies bestanden** en selecteer het CSV-bestand. Wanneer het bestand is geüpload, klikt u op **Volgende**.
   ![](../assets/test-profiles-18.png)
1. Wijs de bronCSV gebieden aan de schemagebieden toe, dan klik **Afwerking**.
   ![](../assets/test-profiles-19.png)
1. Het importeren van de gegevens begint. De status wordt verplaatst van **Verwerking** naar **Succes**. Klik **Voorvertoning gegevensset**, rechtsboven.
   ![](../assets/test-profiles-20.png)
1. Controleer of de testprofielen correct zijn toegevoegd.
   ![](../assets/test-profiles-21.png)

Uw testprofielen worden toegevoegd en kunnen nu worden gebruikt bij het testen van een reis. Zie [deze sectie](../building-journeys/testing-the-journey.md).
>[!NOTE]
>
> Raadpleeg de [documentatie over gegevensinname](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html#tutorials) voor meer informatie over csv-import.

## Testprofielen maken met behulp van API-aanroepen{#create-test-profiles-api}

U kunt testprofielen ook maken via API-aanroepen. Meer informatie vindt u op deze [pagina](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html).

U moet een profielschema gebruiken dat de &quot;de testdetails van het Profiel&quot;mengen bevat. De markering testProfile maakt deel uit van deze mix.

Wanneer u een profiel maakt, moet u de waarde doorgeven: testProfile = true.

U kunt een bestaand profiel ook bijwerken en de markering testProfile wijzigen in &quot;true&quot;.

Hier volgt een voorbeeld van een API-aanroep om een testprofiel te maken:

```
curl -X POST \
'https://dcs.adobedc.net/collection/xxxxxxxxxxxxxx' \
-H 'Cache-Control: no-cache' \
-H 'Content-Type: application/json' \
-H 'Postman-Token: xxxxx' \
-H 'cache-control: no-cache' \
-H 'x-api-key: xxxxx' \
-H 'x-gw-ims-org-id: xxxxx' \
-d '{
"header": {
"msgType": "xdmEntityCreate",
"msgId": "xxxxx",
"msgVersion": "xxxxx",
"xactionid":"xxxxx",
"datasetId": "xxxxx",
"imsOrgId": "xxxxx",
"source": {
"name": "Postman"
},
"schemaRef": {
"id": "https://example.adobe.com/mobile/schemas/xxxxx",
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"xdmEntity": {
"_id": "xxxxx",
"_mobile":{
"ECID": "xxxxx"
},
"testProfile":true
}
}
}'
```
