---
solution: Journey Optimizer
product: journey optimizer
title: Een aangepaste handeling configureren
description: Leer hoe u een aangepaste handeling configureert
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: handeling, extern, aangepast, reizen, API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '1401'
ht-degree: 2%

---

# Een aangepaste handeling configureren {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Aangepaste acties"
>abstract="Als u een derdesysteem gebruikt om berichten te verzenden of als u reizen API vraag naar een derdesysteem wilt verzenden, gebruik douaneacties om zijn verbinding aan uw reis te vormen. U kunt bijvoorbeeld met aangepaste handelingen verbinding maken met de volgende systemen: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com), Firebase, enz."

Als u een derdesysteem gebruikt om berichten te verzenden of als u reizen API vraag naar een derdesysteem wilt verzenden, gebruik douaneacties om zijn verbinding aan uw reis te vormen. U kunt bijvoorbeeld met aangepaste handelingen verbinding maken met de volgende systemen: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase, enz.

Aangepaste acties zijn aanvullende acties die door technische gebruikers worden gedefinieerd en beschikbaar worden gesteld aan verkopers. Zodra gevormd, verschijnen zij in het linkerpalet van uw reis, in **[!UICONTROL Action]** categorie. Meer informatie vindt u [op deze pagina](../building-journeys/about-journey-activities.md#action-activities).

## Beperkingen{#custom-actions-limitations}

Aangepaste acties worden geleverd met enkele beperkingen die worden vermeld in [deze pagina](../start/guardrails.md).

In parameters voor aangepaste handelingen kunt u een eenvoudige verzameling en een verzameling objecten doorgeven. Meer informatie over verzamelingsbeperkingen vindt u in [deze pagina](../building-journeys/collections.md#limitations).

De parameters voor aangepaste handelingen hebben een verwachte indeling (bijvoorbeeld tekenreeks, decimaal, enz.). U moet deze verwachte formaten zorgvuldig respecteren. Meer informatie in deze [use case](../building-journeys/collections.md).

Aangepaste acties ondersteunen alleen de JSON-indeling bij gebruik van [verzoek](../action/about-custom-action-configuration.md#define-the-message-parameters) of [antwoordlading](../action/action-response.md).

## Best practices{#custom-action-enhancements-best-practices}

Wanneer het kiezen van een eindpunt om het gebruiken van een douaneactie te richten, ben zeker dat:

* Dit eindpunt kan de productie van de reis, gebruikend configuraties van steunen [Throttling API](../configuration/throttling.md) of [API voor uitlijnen](../configuration/capping.md) om het te beperken. Wees voorzichtig dat een snelheidsbegrenzingsconfiguratie niet lager kan zijn dan 200 TPS. Om het even welk gericht eindpunt zal minstens 200 TPS moeten steunen.
* Dit eindpunt moet een reactietijd hebben zo laag mogelijk. Afhankelijk van uw verwachte productie, zou het hebben van een hoge reactietijd de daadwerkelijke productie kunnen beïnvloeden.

Een maximum van 300.000 vraag over één minuut wordt bepaald voor alle douaneacties. Daarnaast wordt de standaarduitlijning uitgevoerd per host en per sandbox. Op een sandbox bijvoorbeeld als u twee eindpunten met dezelfde host hebt (bijvoorbeeld: `https://www.adobe.com/endpoint1` en `https://www.adobe.com/endpoint2`), wordt de aftopping toegepast op alle eindpunten onder de host adobe.com. De &quot;eindpunt1&quot;en &quot;eindpunt2&quot;zullen de zelfde het begrenzen configuratie delen en het hebben van één eindpunt bereikt de grens zal een effect op het andere eindpunt hebben.

Deze grens is geplaatst gebaseerd op klantengebruik, om externe eindpunten te beschermen die door douaneacties worden gericht. U moet hiermee rekening houden bij reizen voor uw publiek door een juiste leessnelheid te definiëren (5000 profielen/s wanneer aangepaste handelingen worden gebruikt). Indien nodig, kunt u deze het plaatsen met voeten treden door een grotere het maximum van het maximum of het vertragen grens door onze Capping/het Draaien APIs te bepalen. Zie [deze pagina](../configuration/external-systems.md).

U zou openbare eindpunten met douaneacties niet om verschillende redenen moeten richten:

* Zonder behoorlijk het in kaart brengen of het vertragen, is er een risico om teveel vraag naar een openbaar eindpunt te verzenden dat zulk volume niet kan steunen.
* De gegevens van het profiel kunnen door douaneacties worden verzonden, zodat het richten van een openbaar eindpunt tot onbedoeld het delen van persoonlijke informatie buiten zou kunnen leiden.
* U hebt geen controle over de gegevens die door openbare eindpunten worden teruggekeerd. Als een eindpunt zijn API verandert of onjuiste informatie begint te verzenden, zullen die in verzonden mededelingen, met potentiële negatieve gevolgen ter beschikking worden gesteld.

## Toestemming en gegevensbeheer {#privacy}

In Journey Optimizer kunt u beleid voor gegevensbeheer en toestemming toepassen op uw aangepaste acties om te voorkomen dat bepaalde velden worden geëxporteerd naar systemen van derden of om klanten uit te sluiten die niet hebben ingestemd met het ontvangen van e-mail, push- of SMS-berichten. Raadpleeg de volgende pagina&#39;s voor meer informatie:

* [Gegevensbeheer](../action/action-privacy.md).
* [Toestemming](../action/action-privacy.md).


## Configuratiestappen {#configuration-steps}

Hier zijn de belangrijkste stappen die worden vereist om een douaneactie te vormen:

1. Selecteer in de sectie van het menu ADMINISTRATIE de optie **[!UICONTROL Configurations]**. In de  **[!UICONTROL Actions]** sectie, klikken **[!UICONTROL Manage]**. Klikken **[!UICONTROL Create Action]** om een nieuwe handeling te maken. Het deelvenster Handelingsconfiguratie wordt aan de rechterkant van het scherm geopend.

   ![](assets/custom2.png)

1. Voer een naam in voor de handeling.

   >[!NOTE]
   >
   >Alleen alfanumerieke tekens en onderstrepingstekens zijn toegestaan. De maximumlengte is 30 tekens.

1. Voeg een beschrijving aan uw actie toe. Deze stap is optioneel.
1. Het aantal ritten dat deze handeling gebruikt, wordt weergegeven in het dialoogvenster **[!UICONTROL Used in]** veld. U kunt op de knop **[!UICONTROL View journeys]** om de lijst met reizen weer te geven die deze handeling gebruiken.
1. Verschillende definiëren **[!UICONTROL URL Configuration]** parameters. Zie [deze pagina](../action/about-custom-action-configuration.md#url-configuration).
1. Vorm **[!UICONTROL Authentication]** sectie. Deze configuratie is het zelfde als voor gegevensbronnen.  Zie [deze sectie](../datasource/external-data-sources.md#custom-authentication-mode).
1. Definieer de **[!UICONTROL Action parameters]**. Zie [deze pagina](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Klik op **[!UICONTROL Save]**.

   De aangepaste handeling is nu geconfigureerd en klaar om te worden gebruikt tijdens uw reizen. Zie [deze pagina](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Wanneer een douaneactie in een reis wordt gebruikt, zijn de meeste parameters read-only. U kunt alleen de **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** en de **[!UICONTROL Authentication]** sectie.

## Eindpuntconfiguratie {#url-configuration}

Wanneer het vormen van een douaneactie, moet u het volgende bepalen **[!UICONTROL Endpoint Configuration]** parameters:

![](assets/action-response1bis.png){width="70%" align="left"}

1. In de **[!UICONTROL URL]** -veld, geeft u de URL van de externe service op:

   * Als de URL statisch is, voert u de URL in dit veld in.

   * Als de URL een dynamisch pad bevat, voert u alleen het statische gedeelte van de URL in, dat wil zeggen het schema, de host, de poort en eventueel een statisch gedeelte van het pad.

     Voorbeeld: `https://xxx.yyy.com/somethingstatic/`

     U geeft het dynamische pad van de URL op wanneer u de aangepaste handeling aan een rit toevoegt. [Meer informatie](../building-journeys/using-custom-actions.md).

   >[!NOTE]
   >
   >Om veiligheidsredenen raden we u ten zeerste aan het HTTPS-schema te gebruiken voor de URL. Wij staan niet het gebruik van Adobe adressen toe die niet openbaar en het gebruik van IP adressen zijn.
   >
   >Alleen de standaardpoorten zijn toegestaan bij het definiëren van een aangepaste handeling: 80 voor http en 443 voor https.

1. Selecteer de vraag **[!UICONTROL Method]**: het kan **[!UICONTROL POST]**, **[!UICONTROL GET]** of **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > De **DELETE** methode wordt niet ondersteund. Als u een bestaande bron moet bijwerken, selecteert u de optie **PUT** methode.

1. Definieer de headers en queryparameters:

   * In de **[!UICONTROL Headers]** sectie, klikken **[!UICONTROL Add a header field]** om de kopballen van HTTP van het verzoekbericht te bepalen dat naar de externe dienst moet worden verzonden. De **[!UICONTROL Content-Type]** en **[!UICONTROL Charset]** koptekstvelden worden standaard ingesteld. U kunt deze velden niet verwijderen. Alleen de **[!UICONTROL Content-Type]** header kan worden gewijzigd. De waarde ervan moet de JSON-indeling respecteren. Hier is de standaardwaarde:

   ![](assets/content-type-header.png)

   * In de **[!UICONTROL Query parameters]** sectie, klikken **[!UICONTROL Add a Query parameter field]** om de parameters te bepalen u in URL wilt toevoegen.

   ![](assets/journeyurlconfiguration2bis.png)

1. Voer het label of de naam van het veld in.

1. Selecteer het type: **[!UICONTROL Constant]** of **[!UICONTROL Variable]**. Als u **[!UICONTROL Constant]** Voer vervolgens de constante waarde in het dialoogvenster **[!UICONTROL Value]** veld. Als u **[!UICONTROL Variable]**, dan zult u deze variabele specificeren wanneer het toevoegen van de douaneactie aan een reis. [Meer informatie](../building-journeys/using-custom-actions.md).

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >Nadat u de douaneactie aan een reis hebt toegevoegd, kunt u kopbal of vraagparametergebieden aan het nog toevoegen als de reis in ontwerpstatus is. Als u niet wilt dat de reis door configuratieveranderingen wordt beïnvloed, dupliceer de douaneactie en voeg de gebieden aan de nieuwe douaneactie toe.
   >
   >Kopteksten worden gevalideerd volgens veldparseringsregels. Meer informatie in [deze documentatie](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## De parameters voor de nuttige lading definiëren {#define-the-message-parameters}

1. In de **[!UICONTROL Request]** plakken, plakt u een voorbeeld van de JSON-payload die u naar de externe service wilt verzenden. Dit gebied is facultatief en slechts beschikbaar voor POST en PUT die methodes roepen.

1. In de **[!UICONTROL Response]** plakken, een voorbeeld van de lading die door de vraag is teruggekeerd. Dit veld is optioneel en beschikbaar voor alle aanroepmethoden. Voor gedetailleerde informatie over het gebruik van API-aanroepreacties in aangepaste handelingen raadpleegt u [deze pagina](../action/action-response.md).

>[!NOTE]
>
>De responscapaciteit is momenteel beschikbaar in bèta.

![](assets/action-response2bis.png){width="70%" align="left"}

>[!NOTE]
>
>Het voorbeeld voor de laadbewerking mag geen null-waarden bevatten. Veldnamen in de payload mogen geen &quot;.&quot; bevatten teken. Ze kunnen niet beginnen met het teken ‘$’.

U kunt het parametertype definiëren (bijvoorbeeld: tekenreeks, geheel getal, enz.).

U kunt ook opgeven of een parameter een constante of een variabele is.

* **Constante** betekent dat de waarde van de parameter in de ruit van de actieconfiguratie door een technische persoon wordt bepaald. De waarde zal altijd het zelfde over reizen zijn. Het zal niet variëren en de marktleider zal het niet zien wanneer het gebruiken van de douaneactie in de reis. Het kan bijvoorbeeld een id zijn die het externe systeem verwacht. In dat geval is het veld rechts van de schakelconstante/variabele de doorgegeven waarde.
* **Variabele** betekent dat de waarde van de parameter zal variëren. Marktdeelnemers die deze aangepaste handeling tijdens een reis gebruiken, kunnen de gewenste waarde doorgeven of opgeven waar de waarde voor deze parameter moet worden opgehaald (bijvoorbeeld vanaf het evenement, vanuit Adobe Experience Platform, enz.). In dat geval, is het gebied op het recht van de knevelconstante/variabele de etiketmarketers in de reis zullen zien om deze parameter te noemen.

![](assets/customactionpayloadmessage2.png)