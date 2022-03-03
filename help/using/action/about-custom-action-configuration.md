---
solution: Journey Orchestration
title: Een aangepaste handeling configureren
description: Leer hoe u een aangepaste handeling configureert
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 7c00fcf72ba001005b8e4ac548b789f37f9039a3
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 5%

---

# Een aangepaste handeling configureren {#configure-an-action}

Als u een derdesysteem gebruikt om berichten te verzenden of als u reizen API vraag naar een derdesysteem wilt verzenden, gebruik douaneacties om zijn verbinding aan uw reis te vormen. U kunt bijvoorbeeld met aangepaste handelingen verbinding maken met de volgende systemen: Epsilon, Slack, Adobe.io, Firebase, enz.

Aangepaste acties zijn aanvullende acties die door technische gebruikers worden gedefinieerd en beschikbaar worden gesteld aan verkopers. Zodra gevormd, verschijnen zij in het linkerpalet van uw reis, in **[!UICONTROL Action]** categorie. Meer informatie in [deze pagina](../building-journeys/about-journey-activities.md#action-activities).

## Beperkingen{#custom-actions-limitations}

Aangepaste acties worden geleverd met enkele beperkingen die worden vermeld in [deze pagina](../start/limitations.md).

In parameters voor aangepaste handelingen kunt u een eenvoudige verzameling en een verzameling objecten doorgeven. Meer informatie over verzamelingsbeperkingen vindt u in [deze pagina](../building-journeys/collections.md#limitations).

Houd er ook rekening mee dat de parameters voor aangepaste handelingen een verwachte indeling hebben (bijvoorbeeld: tekenreeks, decimaal, enz.). U moet deze verwachte formaten zorgvuldig respecteren. Meer informatie in deze [use case](../building-journeys/collections.md).


## Configuratiestappen {#configuration-steps}

Hier zijn de belangrijkste stappen die worden vereist om een douaneactie te vormen:

1. Selecteer in de sectie van het menu ADMINISTRATIE de optie **[!UICONTROL Configurations]**. In de  **[!UICONTROL Actions]** sectie, klikt u op **[!UICONTROL Manage]**. Klikken **[!UICONTROL Create Action]** om een nieuwe handeling te maken. Het deelvenster Handelingsconfiguratie wordt aan de rechterkant van het scherm geopend.

   ![](assets/custom2.png)

1. Voer een naam in voor de handeling.

   >[!NOTE]
   >
   >Gebruik geen spaties of speciale tekens. Gebruik niet meer dan 30 tekens.

1. Voeg een beschrijving aan uw actie toe. Deze stap is optioneel.
1. Het aantal ritten dat deze handeling gebruikt, wordt weergegeven in het dialoogvenster **[!UICONTROL Used in]** veld. U kunt op de knop **[!UICONTROL View journeys]** om de lijst met reizen weer te geven die deze handeling gebruiken.
1. Verschillende definiëren **[!UICONTROL URL Configuration]** parameters. Zie [deze pagina](../action/about-custom-action-configuration.md#url-configuration).
1. Configureer de **[!UICONTROL Authentication]** sectie. Deze configuratie is het zelfde als voor gegevensbronnen.  Zie [deze sectie](../datasource/external-data-sources.md#custom-authentication-mode).
1. Definieer de **[!UICONTROL Action parameters]**. Zie [deze pagina](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Klik op **[!UICONTROL Save]**.

   De aangepaste handeling is nu geconfigureerd en klaar om te worden gebruikt tijdens uw reizen. Zie [deze pagina](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Wanneer een douaneactie in een reis wordt gebruikt, zijn de meeste parameters read-only. U kunt de **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** en de **[!UICONTROL Authentication]** sectie.

## URL-configuratie {#url-configuration}

Wanneer het vormen van een douaneactie, moet u het volgende bepalen **[!UICONTROL URL Configuration]** parameters:

![](assets/journeyurlconfiguration.png)

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

1. Selecteer de vraag **[!UICONTROL Method]**: het kan **[!UICONTROL POST]** of **[!UICONTROL PUT]**.
1. In de **[!UICONTROL Headers]** in, definieert u de HTTP-headers van het aanvraagbericht dat naar de externe service moet worden verzonden:
   1. Als u een koptekstveld wilt toevoegen, klikt u op **[!UICONTROL Add a header field]**.
   1. Voer de sleutel van het headerveld in.
   1. Als u een dynamische waarde voor het sleutelwaardepaar wilt instellen, selecteert u **[!UICONTROL Variable]**. Anders selecteert u **[!UICONTROL Constant]**.

      Voor een tijdstempel kunt u bijvoorbeeld een dynamische waarde instellen.

   1. Als u **[!UICONTROL Constant]** Voer vervolgens de constante waarde in.

      Als u **[!UICONTROL Variable]**, dan zult u deze variabele specificeren wanneer het toevoegen van de douaneactie aan een reis. [Meer informatie](../building-journeys/using-custom-actions.md).

      ![](assets/journeyurlconfiguration2.png)

   1. Als u een koptekstveld wilt verwijderen, wijst u naar het koptekstveld en klikt u op de knop **[!UICONTROL Delete]** pictogram.
   De **[!UICONTROL Content-Type]** en **[!UICONTROL Charset]** koptekstvelden worden standaard ingesteld. U kunt deze velden niet wijzigen of verwijderen.

   Nadat u de douaneactie aan een reis hebt toegevoegd, kunt u nog kopbalgebieden aan het toevoegen als de reis in ontwerpstatus is. Als u niet wilt dat de reis door configuratieveranderingen wordt beïnvloed, dupliceer de douaneactie en voeg de kopbalgebieden aan de nieuwe douaneactie toe.

   >[!NOTE]
   >
   >Kopteksten worden gevalideerd volgens veldparseringsregels. [Meer informatie](https://tools.ietf.org/html/rfc7230#section-3.2.4).

## De actieparameters definiëren {#define-the-message-parameters}

![](assets/messageparameterssection.png)

In de **[!UICONTROL Action parameters]** plakken, plakt u een voorbeeld van de JSON-payload die u naar de externe service wilt verzenden.

![](assets/customactionpayloadmessage.png)

>[!NOTE]
>
>Veldnamen in de payload mogen geen &quot;.&quot; bevatten teken. Ze kunnen niet beginnen met het teken ‘$’.

U kunt het parametertype definiëren (bijvoorbeeld: tekenreeks, geheel getal, enz.).

U kunt ook opgeven of een parameter een constante of een variabele is.

* Constante betekent dat de waarde van de parameter in de ruit van de actieconfiguratie door een technische persoon wordt bepaald. De waarde zal altijd het zelfde over reizen zijn. De kleur verandert niet en de markeerstift ziet deze niet wanneer u de aangepaste handeling voor de reis gebruikt. Het kan bijvoorbeeld een id zijn die het externe systeem verwacht. In dat geval is het veld rechts van de schakelconstante/variabele de doorgegeven waarde.
* Variabele betekent dat de waarde van de parameter varieert. Marktdeelnemers die deze aangepaste handeling tijdens een reis gebruiken, kunnen de gewenste waarde doorgeven of opgeven waar de waarde voor deze parameter moet worden opgehaald (bijvoorbeeld van het evenement, van de Adobe Experience Platform, enz.). In dat geval, is het gebied op het recht van de knevelconstante/variabele de etiketmarketers in de reis zullen zien om deze parameter te noemen.

![](assets/customactionpayloadmessage2.png)

