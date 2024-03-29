---
solution: Journey Optimizer
product: journey optimizer
title: Een testprofiel maken
description: Leer hoe u een testprofiel maakt
feature: Profiles, Test Profiles
topic: Content Management
role: User
level: Intermediate
exl-id: bd5e053a-69eb-463b-add3-8b9168c8e280
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '1317'
ht-degree: 2%

---

# Testprofielen maken {#create-test-profiles}

Testprofielen zijn vereist wanneer u de opdracht [testmodus](../building-journeys/testing-the-journey.md) op een reis en naar [inhoud voorvertonen en testen](../content-management/preview-test.md).

U kunt testprofielen op verschillende manieren maken. Op deze pagina vindt u meer informatie over:

* Een [bestaand profiel](#turning-profile-into-test) in een testprofiel

* Testprofielen maken door een [csv-bestand](#create-test-profiles-csv) of gebruiken [API-aanroepen](#create-test-profiles-api).

  Naast deze twee methoden wordt in Adobe Journey Optimizer een specifieke [geval van gebruik in producten](#use-case-1) om het maken van testprofielen te vergemakkelijken.

U kunt een jsdossier in een bestaande dataset ook uploaden. Raadpleeg voor meer informatie de [Documentatie over gegevensinname](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html#add-data-to-dataset){target="_blank"}.

Het maken van een testprofiel lijkt op het maken van gewone profielen in Adobe Experience Platform. Raadpleeg voor meer informatie de [Documentatie van het profiel van de klant in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target="_blank"}.

➡️ [Leer hoe u testprofielen maakt in deze video](#video)

## Vereisten {#test-profile-prerequisites}

Om profielen te kunnen tot stand brengen, moet u eerst een schema en een dataset in Adobe creëren [!DNL Journey Optimizer].

Naar **een schema maken** Voer de volgende stappen uit:

1. Klik in de menusectie GEGEVENSBEHEER op **[!UICONTROL Schemas]**.
   ![](assets/test-profiles-0.png)
1. Klikken **[!UICONTROL Create schema]** Selecteer in de rechterbovenhoek een schematype, bijvoorbeeld **Individueel profiel** en klik op **Volgende**.
   ![](assets/test-profiles-1.png)
1. Voer een naam voor het schema in en klik op **Voltooien**.
   ![](assets/test-profiles-1-bis.png)
1. In de **Veldgroepen** , klikt u links op **Toevoegen** en selecteert u de gewenste veldgroepen. Zorg ervoor dat u de **Details van de profieltest** veldgroep.
   ![](assets/test-profiles-1-ter.png)
Klik op **[!UICONTROL Add field groups]**: De lijst met veldgroepen wordt weergegeven in het scherm Schema-overzicht.
   ![](assets/test-profiles-2.png)

   >[!NOTE]
   >
   >Klik op de naam van het schema om de eigenschappen ervan bij te werken.

1. Klik in de lijst met velden op het veld dat u als primaire identiteit wilt definiëren.
   ![](assets/test-profiles-3.png)
1. In de **[!UICONTROL Field properties]** rechterdeelvenster, controleer het **[!UICONTROL Identity]** en **[!UICONTROL Primary Identity]** en selecteert u een naamruimte. Als u wilt dat de primaire identiteit een e-mailadres is, kiest u de optie **[!UICONTROL Email]** naamruimte. Klik op **[!UICONTROL Apply]**.
   ![](assets/test-profiles-4bis.png)
1. Selecteer het schema en schakel het **[!UICONTROL Profile]** in de **[!UICONTROL Schema properties]** venster.
   ![](assets/test-profiles-5.png)
1. Klikken **Opslaan**.

>[!NOTE]
>
>Raadpleeg voor meer informatie over het maken van schema&#39;s de [XDM-documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#prerequisites){target="_blank"}.

Vervolgens moet u **Maak de dataset** waarin de profielen worden geïmporteerd. Voer de volgende stappen uit:

1. Bladeren naar **[!UICONTROL Datasets]** en klik vervolgens op **[!UICONTROL Create dataset]**.
   ![](assets/test-profiles-6.png)
1. Kies **[!UICONTROL Create dataset from schema]**.
   ![](assets/test-profiles-7.png)
1. Selecteer het eerder gemaakte schema en klik op **[!UICONTROL Next]**.
   ![](assets/test-profiles-8.png)
1. Kies een naam en klik op **[!UICONTROL Finish]**.
   ![](assets/test-profiles-9.png)
1. De optie **[!UICONTROL Profile]** -optie.
   ![](assets/test-profiles-10.png)

>[!NOTE]
>
> Raadpleeg voor meer informatie over het maken van gegevenssets de [Documentatie Catalog Service](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#getting-started){target="_blank"}.

## Gebruiksscenario in het product{#use-case-1}

Op de homepage van Adobe Journey Optimizer kunt u de testprofielen gebruiken in het product. Met dit gebruiksgeval kunt u testprofielen maken die worden gebruikt voor het testen van reizen voordat ze worden gepubliceerd.

![](assets/use-cases-home.png)

Klik op de knop **[!UICONTROL Begin]** om het gebruik te starten.

De volgende informatie is vereist:

1. **Naamruimte identiteit**: De [naamruimte identity](../audience/get-started-identity.md) worden gebruikt om de testprofielen op unieke wijze te identificeren. Als e-mail bijvoorbeeld wordt gebruikt om de testprofielen te identificeren, wordt de naamruimte van de identiteit **E-mail** moet worden geselecteerd. Als het unieke herkenningsteken het telefoonaantal is, dan identiteit namespace **Telefoon** moet worden geselecteerd.

2. **CSV-bestand**: Een door komma&#39;s gescheiden bestand met de lijst testprofielen die moeten worden gemaakt. De gebruikscase verwacht een vooraf gedefinieerde indeling voor het CSV-bestand dat de lijst met testprofielen bevat die moet worden gemaakt. Elke rij in het bestand moet de volgende velden in de juiste volgorde bevatten:

   1. **Persoon-id**: Unieke id van het testprofiel. De waarden van dit veld moeten de naamruimte weerspiegelen die is geselecteerd. (Als voorbeeld: als **Telefoon** is geselecteerd voor de naamruimte van de identiteit. De waarden van dit veld moeten telefoonnummers zijn. Op dezelfde manier als **E-mail** is geselecteerd, dan moeten de waarden van dit veld e-mails zijn)
   1. **E-mailadres**: E-mailadres voor testprofiel. (De **Persoon-id** en de **E-mailadres** veld kan dezelfde waarden bevatten als **E-mail** is geselecteerd als naamruimte voor identiteit)
   1. **Voornaam**: Voornaam van testprofiel.
   1. **Achternaam**: Achternaam van testprofiel.
   1. **Plaats**: testprofiel stad van verblijf
   1. **Land**: Testprofiel land van verblijf
   1. **Geslacht**: sekse testprofiel. Beschikbare waarden zijn **mannetje**, **vrouwelijk** en **niet_opgegeven**

Nadat u de naamruimte Identiteit hebt geselecteerd en het CSV-bestand hebt opgegeven op basis van de bovenstaande indeling, klikt u op **[!UICONTROL Run]** aan de rechterbovenhoek. Het kan enkele minuten duren voordat de gebruiksaanwijzing is voltooid. Zodra het gebruik is voltooid en de testprofielen zijn gemaakt, wordt een melding verzonden om de gebruiker op de hoogte te stellen.

>[!NOTE]
>
>Testprofielen kunnen bestaande profielen overschrijven. Controleer voordat u het gebruiksscenario uitvoert of het CSV-bestand alleen testprofielen bevat en of het wordt uitgevoerd met de juiste sandbox.

## Een profiel omzetten in een testprofiel{#turning-profile-into-test}

U kunt een bestaand profiel omzetten in een testprofiel: u kunt profielkenmerken op dezelfde manier bijwerken als wanneer u een profiel maakt.

Een eenvoudige manier om dit te doen is door een **[!UICONTROL Update Profile]** de activiteit van de actie in een reis en verandert **testProfile** Booleaans veld van false naar true.

Uw reis zal bestaan uit een **[!UICONTROL Read Audience]** en **[!UICONTROL Update Profile]** activiteit. Eerst moet u een publiek maken dat zich richt op de profielen die u wilt omzetten in testprofielen.

>[!NOTE]
>
> Aangezien u de **testProfile** in de gekozen profielen moet dit veld worden opgenomen. Het gerelateerde schema moet de **Details van de profieltest** veldgroep. Zie [deze sectie](../audience/creating-test-profiles.md#test-profiles-prerequisites).

1. Bladeren naar **Soorten publiek** vervolgens **publiek maken**, rechtsboven.
   ![](assets/test-profiles-22.png)
1. Definieer een naam voor de doelgroep en stel de doelgroep samen: kies een of meer velden en waarden voor de gewenste profielen.
   ![](assets/test-profiles-23.png)
1. Klikken **Opslaan** en controleert u of de doelprofielen correct zijn ingesteld door de doelgroep.
   ![](assets/test-profiles-24.png)

   >[!NOTE]
   >
   > De berekening van het publiek kan wat tijd vergen. Meer informatie over publiek in [deze sectie](../audience/about-audiences.md).

1. Maak nu een nieuwe reis en begin met een **[!UICONTROL Read Audience]** orkestactiviteit.
1. Kies het eerder gemaakte publiek en de naamruimte die uw profielen gebruiken.
   ![](assets/test-profiles-25.png)
1. Een **[!UICONTROL Update Profile]** actieactiviteit.
1. Selecteer het schema, **testProfiles** veld, de gegevensset en de waarde instellen op **Waar**. Om dit uit te voeren, in **[!UICONTROL VALUE]** veld, klikt u op de knop **Pen** pictogram rechts, selecteert u **[!UICONTROL Advanced mode]** en betreden **true**.
   ![](assets/test-profiles-26.png)
1. Klik op **[!UICONTROL Publish]**.
1. In de **[!UICONTROL Audiences]** controleren of de profielen correct zijn bijgewerkt.
   ![](assets/test-profiles-28.png)

   >[!NOTE]
   >
   > Voor meer informatie over de **[!UICONTROL Update Profile]** activiteit, zie [deze sectie](../building-journeys/update-profiles.md).

## Een testprofiel maken met een CSV-bestand{#create-test-profiles-csv}

In Adobe Experience Platform kunt u profielen maken door een CSV-bestand met de verschillende profielvelden te uploaden naar uw gegevensset. Dit is de eenvoudigste methode.

1. Maak een eenvoudig CSV-bestand met behulp van een spreadsheetsoftware.
1. Voeg één kolom toe voor elk nodig veld. Voeg het primaire identiteitsveld (&quot;personID&quot; in het bovenstaande voorbeeld) en het veld &quot;testProfile&quot; toe op &quot;true&quot;.
   ![](assets/test-profiles-11.png)
1. Voeg één regel per profiel toe en vul de waarden voor elk veld in.
   ![](assets/test-profiles-12.png)
1. Sla het werkblad op als een CSV-bestand. Controleer of komma&#39;s als scheidingstekens worden gebruikt.
1. Bladeren naar Adobe Experience Platform **Workflows**.
   ![](assets/test-profiles-14.png)
1. Kies **CSV toewijzen aan XDM-schema** en klik vervolgens op **Starten**.
   ![](assets/test-profiles-16.png)
1. Selecteer de dataset u de profielen in wilt invoeren. Klik op **Next**.
   ![](assets/test-profiles-17.png)
1. Klikken **Bestanden kiezen** en selecteert u het CSV-bestand. Wanneer het bestand is geüpload, klikt u op **Volgende**.
   ![](assets/test-profiles-18.png)
1. Wijs de bronCSV gebieden aan de schemagebieden toe, dan klik **Voltooien**.
   ![](assets/test-profiles-19.png)
1. Het importeren van de gegevens begint. De status verandert van **Verwerking** tot **Succes**. Klikken **Gegevensset voorvertoning**, rechtsboven.
   ![](assets/test-profiles-20.png)
1. Controleer of de testprofielen correct zijn toegevoegd.
   ![](assets/test-profiles-21.png)

Uw testprofielen worden toegevoegd en kunnen nu worden gebruikt bij het testen van een reis. Zie [deze sectie](../building-journeys/testing-the-journey.md).
>[!NOTE]
>
> Raadpleeg voor meer informatie over CSV-import de [Documentatie over gegevensinname](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html#tutorials){target="_blank"}.

## Testprofielen maken met behulp van API-aanroepen{#create-test-profiles-api}

U kunt testprofielen ook maken via API-aanroepen. Meer informatie in [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target="_blank"}.

U moet een profielschema gebruiken dat de het gebiedsgroep van &quot;de testdetails van het Profiel&quot;bevat. De markering testProfile maakt deel uit van deze veldgroep.
Wanneer u een profiel maakt, moet u de waarde testProfile = true doorgeven.

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

## Hoe kan ik-video {#video}

Leer hoe u testprofielen maakt.

>[!VIDEO](https://video.tv.adobe.com/v/334236?quality=12)
