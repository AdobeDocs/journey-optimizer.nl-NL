---
solution: Journey Optimizer
product: journey optimizer
title: Een eenheidsgebeurtenis configureren
description: Leer hoe u een eenheidsgebeurtenis configureert
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: evenement, eenheidsprijs, creëren, reis
exl-id: e22e2bc7-0c15-457a-8980-97bea5da7784
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '1645'
ht-degree: 7%

---

# Een eenheidsgebeurtenis configureren {#configure-an-event}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_unitary"
>title="Unitaire gebeurtenissen"
>abstract="Met de gebeurtenisconfiguratie kunt u de informatie definiëren die Journey Optimizer ontvangt als gebeurtenissen. U kunt meerdere gebeurtenissen gebruiken (in verschillende stappen van een reis) en verschillende reizen kunnen dezelfde gebeurtenis gebruiken. Eenheidsgebeurtenissen zijn gekoppeld aan een specifiek profiel. Zij kunnen op regel-gebaseerd of systeem-geproduceerd zijn."

>[!CONTEXTUALHELP]
>id="ajo_journey_event_parameters"
>title="Parameters"
>abstract="Definieer de parameters van de gebeurtenis, zoals het schema en de payload-velden. Voor op regel-gebaseerde gebeurtenissen, gebruik het **[!UICONTROL Event ID condition]** gebied om de voorwaarde te bepalen die door het systeem zal worden gebruikt om de gebeurtenissen te identificeren die uw reis zullen teweegbrengen. Voeg een identiteitstype en een profiel-id toe die u voor de gebeurtenis wilt gebruiken."

Eenheidsgebeurtenissen zijn gekoppeld aan een specifiek profiel. Zij kunnen op regel-gebaseerd of systeem-geproduceerd zijn.  Lees meer over unitaire gebeurtenis [&#x200B; deze sectie &#x200B;](../event/about-events.md).

Hieronder vindt u de eerste stappen voor het configureren van een nieuwe gebeurtenis:

1. Blader in de menusectie BEHEER naar **[!UICONTROL Configurations]** en klik in de sectie **[!UICONTROL Events]** op **[!UICONTROL Manage]** . De lijst met gebeurtenissen wordt weergegeven.

   ![](assets/jo-event1.png)

1. Klik op **[!UICONTROL Create Event]** om een nieuwe gebeurtenis te maken. Het deelvenster voor gebeurtenisconfiguratie wordt aan de rechterkant van het scherm geopend.

   ![](assets/jo-event2.png)

1. Voer de naam van de gebeurtenis in. U kunt ook een beschrijving toevoegen.

   ![](assets/jo-event3.png)

   >[!NOTE]
   >
   >Alleen alfanumerieke tekens en onderstrepingstekens zijn toegestaan. De maximumlengte is 30 tekens.

1. Op het **[!UICONTROL Type]** gebied, kies **Eenheids**.

   ![](assets/jo-event3bis.png)

1. Op het **[!UICONTROL Event ID type]** gebied, selecteer het type van gebeurtenisidentiteitskaart u wilt gebruiken: **Gebaseerde Regel** of **Gegenereerd Systeem**. Lees meer op de types van gebeurtenisidentiteitskaart in [&#x200B; deze sectie &#x200B;](../event/about-events.md#event-id-type).

   ![](assets/jo-event4.png)

1. Het aantal journey’s dat deze gebeurtenis gebruikt, wordt in het veld **[!UICONTROL Used in]** weergegeven. U kunt klikken op het pictogram **[!UICONTROL View journeys]** om de lijst weer te geven met journey’s die deze gebeurtenis gebruiken.

1. Definieer het schema en de payload-velden: hier selecteert u de gebeurtenisgegevens (gewoonlijk een payload genoemd) die de reis verwacht te ontvangen. U kunt deze informatie vervolgens gebruiken tijdens uw journey. Zie [deze sectie](../event/about-creating.md#define-the-payload-fields).

   ![](assets/jo-event5.png)

   >[!NOTE]
   >
   >Wanneer u het type **[!UICONTROL System Generated]** selecteert, zijn alleen schema&#39;s beschikbaar die het veld voor het type eventID hebben. Wanneer u het type **[!UICONTROL Rule Based]** selecteert, zijn alle schema&#39;s voor Experience Event beschikbaar.

1. Voor op regel-gebaseerde gebeurtenissen, klik binnen het **[!UICONTROL Event ID condition]** gebied. Gebruikend de eenvoudige of geavanceerde uitdrukkingsredacteur, bepaal de voorwaarde die door het systeem zal worden gebruikt om de gebeurtenissen te identificeren die uw reis zullen teweegbrengen.

   ![](assets/jo-event6.png)

   In ons voorbeeld schreven we een voorwaarde op basis van de stad van het profiel. Dit betekent dat wanneer het systeem een gebeurtenis ontvangt die overeenkomt met deze voorwaarde (**[!UICONTROL City]** field en **[!UICONTROL Paris]** value), het deze aan reizen zal doorgeven.

   >[!NOTE]
   >
   >In de eenvoudige expressie-editor zijn niet alle operatoren beschikbaar, maar zijn ze afhankelijk van het gegevenstype. Voor een tekenreekstype kunt u bijvoorbeeld &quot;contains&quot; of &quot;equal to&quot; gebruiken.
   >
   >Als u na het maken van de gebeurtenis uw schema met nieuwe opsomwaarden wijzigt, moet u de volgende stappen volgen om de wijzigingen toe te passen op de bestaande gebeurtenis: schakel het opsomveld uit de gebeurtenisvelden uit, bevestig de selectie en selecteer vervolgens nogmaals het opsomveld. De nieuwe opsommingswaarde wordt nu weergegeven.

1. Voeg een identiteitstype toe. Deze stap is optioneel, maar wordt aanbevolen als u een identiteitstype toevoegt, zodat u gegevens die zijn opgeslagen in de realtime service voor klantprofielen, kunt gebruiken. U definieert zo het type sleutel van de gebeurtenis. Lees meer in [deze sectie](../event/about-creating.md#select-the-namespace).

1. Definieer de profiel-id: kies een veld in uw payload-velden of definieer een formule om de persoon te identificeren die aan de gebeurtenis is gekoppeld. Deze sleutel wordt automatisch ingesteld (maar kan nog steeds worden bewerkt) als u een identiteitstype selecteert. Reizen kiezen immers de sleutel die moet overeenkomen met het identiteitstype (als u bijvoorbeeld een e-mailidentiteitstype selecteert, wordt de e-mailsleutel geselecteerd). Lees meer in [deze sectie](../event/about-creating.md#define-the-event-key).

   ![](assets/jo-event7.png)

1. Klik op **[!UICONTROL Save]**.

   De gebeurtenis is nu geconfigureerd en klaar om in een journey worden gezet. Er zijn aanvullende configuratiestappen nodig om gebeurtenissen te ontvangen. Zie [deze pagina](../event/additional-steps-to-send-events-to-journey.md).

## De laadvelden definiëren {#define-the-payload-fields}

De ladingsdefinitie staat u toe om de informatie te kiezen het systeem van de gebeurtenis in uw reis verwacht te ontvangen en de sleutel om te identificeren welke persoon aan de gebeurtenis wordt geassocieerd. De nuttige lading is gebaseerd op de Experience Cloud XDM gebiedsdefinitie. Voor meer informatie over XDM, verwijs naar [&#x200B; documentatie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"}.

1. Selecteer een XDM-schema in de lijst en klik op het veld **[!UICONTROL Fields]** of op het pictogram **[!UICONTROL Edit]** .

   ![](assets/journey8.png)

   Alle velden die in het schema zijn gedefinieerd, worden weergegeven. De lijst met velden verschilt per schema. U kunt naar een specifiek veld zoeken of de filters gebruiken om alle knooppunten en velden of alleen de geselecteerde velden weer te geven. Volgens de schemadefinitie zijn sommige velden mogelijk verplicht en vooraf geselecteerd. U kunt de selectie niet opheffen. Alle velden die verplicht zijn voor een goede ontvangst van de gebeurtenis tijdens de reis, zijn standaard geselecteerd.

   >[!NOTE]
   >
   >Voor systeem-geproduceerde gebeurtenissen, zorg ervoor dat u de &quot;orchestration&quot;gebiedsgroep aan het schema XDM hebt toegevoegd. Zo zorgt u ervoor dat het schema alle vereiste gegevens bevat om met [!DNL Journey Optimizer] te werken.

   ![](assets/journey9.png)

1. Selecteer de velden die u van de gebeurtenis wilt ontvangen. Dit zijn de gebieden die de bedrijfsgebruiker in de reis zal hefboomwerking hebben. Zij moeten ook de sleutel omvatten die zal worden gebruikt om de persoon te identificeren verbonden aan de gebeurtenis (zie [&#x200B; deze sectie &#x200B;](../event/about-creating.md#define-the-event-key)).

   >[!NOTE]
   >
   >Voor door het systeem gegenereerde gebeurtenissen wordt het veld **[!UICONTROL eventID]** automatisch toegevoegd aan de lijst met geselecteerde velden, zodat [!DNL Journey Optimizer] de gebeurtenis kan identificeren. Het systeem dat de gebeurtenis duwt zou geen identiteitskaart moeten produceren, zou het moeten gebruiken beschikbaar in de voorproef van de lading. Zie [deze sectie](../event/about-creating.md#preview-the-payload).

1. Klik op **[!UICONTROL Ok]** of druk op **[!UICONTROL Enter]** wanneer u klaar bent met het selecteren van de benodigde velden.

   Het aantal geselecteerde velden wordt weergegeven in het veld **[!UICONTROL Fields]** .

   ![](assets/journey12.png)

## Selecteer het identiteitstype {#select-the-namespace}

>[!CONTEXTUALHELP]
>id="ajo_journey_namespace"
>title="Identiteitstype"
>abstract="Selecteer de sleutel om het klantenprofiel te identificeren verbonden aan de gebeurtenis."

Met het identiteitstype (voorheen &#39;naamruimte&#39; genoemd) kunt u het type sleutel definiëren waarmee de persoon wordt geïdentificeerd die aan de gebeurtenis is gekoppeld. De configuratie is optioneel. Het wordt vereist als u, in uw reizen, extra informatie wilt terugwinnen die uit het [&#x200B; Real-time Profiel van de Klant &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target="_blank"} komt. De definitie van het identiteitstype is niet nodig als u slechts gegevens gebruikt die uit een derdesysteem door een douanegegevensbron komen.

U kunt een bestaand identiteitstype gebruiken of een nieuw type maken met de Adobe Experience Platform Identity Service. Leer meer in de [&#x200B; documentatie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=nl){target="_blank"}.

Als u een schema met een primaire identiteit selecteert, worden de velden **[!UICONTROL Profiler identifier]** en **[!UICONTROL Identity type]** vooraf ingevuld. Als er geen bepaalde identiteit is, selecteren wij _identityMap > identiteitskaart_ als primaire sleutel. Dan moet u een identiteitstype selecteren en de sleutel zal (onder het **[!UICONTROL Identity type]** gebied) worden ingevuld gebruikend _identityMap > identiteitskaart_.

Wanneer u velden selecteert, worden primaire identiteitsvelden gecodeerd.

![](assets/primary-identity.png)

Selecteer een identiteitstype in de vervolgkeuzelijst.

![](assets/journey17.png)

Per reis is slechts één identiteitstype toegestaan. Als u meerdere gebeurtenissen gebruikt op dezelfde reis, moeten ze hetzelfde identiteitstype gebruiken. Zie [deze pagina](../building-journeys/journey.md).

>[!NOTE]
>
>U kunt alleen een op personen gebaseerd identiteitstype selecteren. Als u een identiteitstype voor een raadplegingslijst (bijvoorbeeld: Het identiteitstype ProductID voor een raadpleging van het Product) hebt bepaald, zal het niet in de **het type van Identiteit** dropdown lijst beschikbaar zijn.

## De profiel-id definiëren {#define-the-event-key}

De sleutel is het veld, of de combinatie van velden, dat deel uitmaakt van de gegevens voor gebeurtenislading en waarmee het systeem de persoon kan identificeren die aan de gebeurtenis is gekoppeld. De sleutel kan bijvoorbeeld de Experience Cloud-id, een CRM-id of een e-mailadres zijn.

Om gegevens te gebruiken die in het gegevensbestand van het Profiel van de Klant in real time van Adobe worden opgeslagen, moet de gebeurtenissleutel de informatie zijn u als identiteit van een profiel in de [&#x200B; Real-time Dienst van het Profiel van de Klant &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl){target="_blank"} bepaalde.

Met de profiel-id kan het systeem de afstemming tussen de gebeurtenis en het profiel van de persoon uitvoeren. Als u een schema met een primaire identiteit selecteert, worden de velden **[!UICONTROL Profile identifier]** en **[!UICONTROL Identity type]** vooraf ingevuld. Als er geen bepaalde identiteit is, is _identityMap > identiteitskaart_ de primaire sleutel. Dan moet u een identiteitstype selecteren, en de sleutel is automatisch voorgevuld gebruikend _identityMap > identiteitskaart_.

Wanneer u velden selecteert, worden primaire identiteitsvelden gecodeerd.

![](assets/primary-identity.png)

Als u een andere sleutel moet gebruiken, zoals een CRM-id of een e-mailadres, moet u deze handmatig toevoegen, zoals hieronder wordt uitgelegd:

1. Klik in het veld **[!UICONTROL Profile identifier]** of op het potloodpictogram.

   ![](assets/journey16.png)

1. Selecteer het veld dat u als de sleutel hebt gekozen in de lijst met ladingsvelden.

Wanneer de gebeurtenis wordt ontvangen, laat de waarde van de sleutel het systeem toe om de persoon te identificeren verbonden aan de gebeurtenis. Verbonden aan een [&#x200B; identiteitstype &#x200B;](../event/about-creating.md#select-the-namespace), kan de sleutel worden gebruikt om vragen op Adobe Experience Platform uit te voeren. Zie [&#x200B; deze pagina &#x200B;](../building-journeys/about-journey-activities.md#orchestration-activities).
De sleutel wordt ook gebruikt om te controleren of een persoon op reis is. Een persoon kan namelijk niet op twee verschillende plaatsen op dezelfde reis zijn. Als gevolg hiervan staat het systeem niet toe dat dezelfde sleutel, bijvoorbeeld de sleutel CRMID=3224, zich op verschillende plaatsen op dezelfde reis bevindt.

## Geavanceerde expressie-editor {#adv-exp-editor}

Wanneer u de voorwaarde van de gebeurtenis-id of de profielid definieert, kunt u overschakelen naar de geavanceerde expressie-editor om complexere sleutels te maken (bijvoorbeeld een samenvoeging van twee velden van de gebeurtenissen).

![](assets/journey20.png)

U hebt via de knop **[!UICONTROL Advanced mode]** toegang tot de geavanceerde expressiefuncties als u aanvullende bewerkingen wilt uitvoeren. Met deze functies kunt u de waarden manipuleren die worden gebruikt voor het uitvoeren van specifieke query&#39;s, zoals het wijzigen van de opmaak, het uitvoeren van veldsamenvoegingen, waarbij alleen rekening wordt gehouden met een deel van een veld (bijvoorbeeld de eerste 10 tekens). Zie deze [pagina](../building-journeys/expression/expressionadvanced.md).


## Een voorvertoning van de lading weergeven {#preview-the-payload}

Met de voorvertoning van de lading kunt u de definitie van de lading valideren.

>[!NOTE]
>
>Wanneer u een gebeurtenis maakt die door het systeem wordt gegenereerd, slaat u de gebeurtenis op voordat u deze weergeeft. Deze stap is nodig om een gebeurtenis-id te genereren in de payload.

1. Klik op het pictogram **[!UICONTROL View Payload]** om een voorvertoning weer te geven van de lading die door het systeem wordt verwacht.

   ![](assets/journey13.png)

   U ziet dat de geselecteerde velden worden weergegeven.

   ![](assets/journey14.png)

1. Controleer de voorvertoning om de definitie van de payload te valideren.

1. Vervolgens kunt u de voorvertoning van de lading delen met de persoon die verantwoordelijk is voor het verzenden van de gebeurtenis. Deze lading kan hen helpen de opstelling van een gebeurtenis ontwerpen die aan [!DNL Journey Optimizer] duwt. Zie [deze pagina](../event/additional-steps-to-send-events-to-journey.md).
