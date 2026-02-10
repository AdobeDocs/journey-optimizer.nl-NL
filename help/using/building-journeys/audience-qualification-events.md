---
solution: Journey Optimizer
product: journey optimizer
title: Gebeurtenissen in verband met de kwalificatie van het publiek
description: Leer hoe u kwalificatiegebeurtenissen voor het publiek gebruikt en configureert
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: kwalificatie, evenementen, publiek, reis, platform
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '1449'
ht-degree: 0%

---

# Gebeurtenissen in verband met de kwalificatie van het publiek {#segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="kwalificatiegebeurtenissen voor het publiek"
>abstract="Deze activiteit luistert naar entry&#39;s en exits van profielen in [!DNL Adobe Experience Platform] publiek om individuen door een reis te bewegen."

## Informatie over publiekskwalificatiegebeurtenissen{#about-segment-qualification}

Deze activiteit luistert naar entry&#39;s en exits van profielen in [!DNL Adobe Experience Platform] publiek. Het kan individuen tot een reis maken of vooruit bewegen. Voor meer informatie over publieksverwezenlijking, verwijs naar deze [&#x200B; sectie &#x200B;](../audience/about-audiences.md).

Laten we zeggen dat je een &quot;zilveren klant&quot; publiek hebt. Met deze activiteit, kunt u alle nieuwe zilveren klanten een reis maken en hen een reeks gepersonaliseerde berichten verzenden.

Dit type gebeurtenis kan als eerste stap of later in de reis worden geplaatst.

➡️ [Ontdek deze functie in video](#video)


>[!CAUTION]
>
>Alvorens te beginnen om een kwalificatie van het Publiek te vormen, [&#x200B; lees de Grafieken en Beperkingen &#x200B;](#audience-qualification-guardrails).


## De activiteit configureren {#configure-segment-qualification}

Voer de volgende stappen uit om de **[!UICONTROL Audience Qualification]** -activiteit te configureren:

1. Ontvouw de categorie **[!UICONTROL Events]** en zet een **[!UICONTROL Audience Qualification]** -activiteit neer op uw canvas.

   ![&#x200B; de gebeurtenis van de Kwalificatie van het publiek in reispalet &#x200B;](assets/segment5.png)

1. Voeg een **[!UICONTROL Label]** toe aan de activiteit. Deze stap is optioneel.

1. Klik in het veld **[!UICONTROL Audience]** en selecteer het publiek dat u wilt gebruiken.

   >[!NOTE]
   >
   >U kunt de kolommen aanpassen die in de lijst worden weergegeven en ze sorteren.

   ![&#x200B; drop-down van de selectie van het publiek voor de configuratie van de kwalificatiegebeurtenis &#x200B;](assets/segment6.png)

   Nadat het publiek is toegevoegd, kunt u met de knop **[!UICONTROL Copy]** de naam en de id van het publiek kopiëren:

   `{"name":"Loyalty membership","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![&#x200B; knoop van het Exemplaar om publieksnaam en identiteitskaart in formaat te kopiëren JSON &#x200B;](assets/segment-copy.png)

1. Kies in het veld **[!UICONTROL Behaviour]** of u wilt luisteren naar de publieksinvoer, het afsluit of beide.

   >[!NOTE]
   >
   >**[!UICONTROL Enter]** en **[!UICONTROL Exit]** beantwoorden aan **gerealiseerde** en **Uitgegeven** status van de publieksparticipatie van [!DNL Adobe Experience Platform].
   >Zie de [&#x200B; documentatie van de Dienst van de Segmentatie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=nl-NL#interpret-segment-results){target="_blank"}.

1. Selecteer een naamruimte. Dit is alleen nodig als de gebeurtenis als eerste stap van de reis wordt geplaatst. Het veld wordt standaard voorgevuld met de laatst gebruikte naamruimte.

   >[!NOTE]
   >
   >U kunt alleen een naamruimte selecteren die is gebaseerd op personen.
   >De lijst van de opzoeklijst namespaces (bijvoorbeeld, ProductID voor een raadpleging van het Product) is niet beschikbaar in **Namespace** dropdown lijst.

   ![&#x200B; de selectie van Namespace voor de identiteit van de publiekskwalificatie &#x200B;](assets/segment7.png)

De nuttige lading bevat de volgende contextinformatie, die u in voorwaarden en acties kunt gebruiken:

* het gedrag (ingang, uitgang)
* het tijdstempel van de kwalificatie
* de publieks-id

Wanneer u de expressie-editor gebruikt in een voorwaarde of handeling die volgt op een **[!UICONTROL Audience Qualification]** -activiteit, hebt u toegang tot het **[!UICONTROL AudienceQualification]** -knooppunt. U kunt kiezen tussen **[!UICONTROL Last qualification time]** en **[!UICONTROL status]** (Enter of exit).

Zie [&#x200B; de activiteit van de Voorwaarde &#x200B;](../building-journeys/condition-activity.md#about_condition).

Een nieuwe reis die een **gebeurtenis van de Kwalificatie van het Publiek** omvat wordt operationeel tien minuten nadat u het publiceert. Dit interval past het geheime voorgeheugen aan verfrist interval van de specifieke dienst. Wacht tien minuten voordat u deze reis gebruikt.

## Best practices {#best-practices-segments}

Met de **[!UICONTROL Audience Qualification]** -activiteit kunnen personen die in aanmerking komen voor of die niet in aanmerking komen voor een [!DNL Adobe Experience Platform] -publiek, direct een reis maken.

De ontvangstsnelheid van deze informatie is hoog. Metingen tonen 10.000 ontvangen gebeurtenissen per seconde. Plan voor ingangspikes, vermijd hen wanneer mogelijk, en bereidt uw reis voor om hen te behandelen. Leer meer over de tarieven van de reisverwerking en productielimieten in [&#x200B; deze sectie &#x200B;](entry-management.md#journey-processing-rate).

### Batchpubliek {#batch-speed-segment-qualification}

Wanneer het gebruiken van de Kwalificatie van het Publiek voor een partijpubliek, merk op dat een piek van ingang op het tijdstip van de dagelijkse berekening voorkomt. De grootte van de piek is afhankelijk van het aantal personen dat het publiek binnenkomt of verlaat elke dag.

Bovendien, als het partijpubliek nieuw wordt gecreeerd en onmiddellijk in een reis gebruikt, kan de eerste partij van berekening vele ingangen drijven. Plan deze piek.

### Gestroomd publiek {#streamed-speed-segment-qualification}

Wanneer het gebruiken van de Kwalificatie van het Publiek voor gestroomd publiek, is er minder risico van grote ingang en uitgangspieken omdat de evaluatie ononderbroken is. Als de publieksdefinitie veel klanten in één keer kwalificeert, kan een piek nog voorkomen.

Vermijd het gebruik van open en verzend gebeurtenissen met streaming segmentatie. In plaats daarvan, gebruik echte user-activity signalen zoals kliks, aankopen, of baken gegevens. Voor frequentie of suppression logica, gebruik bedrijfsregels in plaats van gebeurtenissen te verzenden. [Meer informatie](../audience/about-audiences.md)

Zie [[!DNL Adobe Experience Platform]  het stromen segmentatiedocumentatie &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/segmentation/methods/streaming-segmentation){target="_blank"}.

>[!NOTE]
>
>Voor het stromen segmentatie, kunnen de onlangs opgenomen gegevens tot **2 uren** vergen om volledig binnen [!DNL Adobe Experience Platform] voor gebruik in real time te verspreiden. Soorten publiek dat afhankelijk is van op dag of tijd gebaseerde omstandigheden (bijvoorbeeld &quot;gebeurtenissen die zich vandaag hebben voorgedaan&quot;) kunnen extra complexiteit ervaren in het kwalificatietijdstip. Als uw reis van directe publiekskwalificatie afhangt, denk na toevoegend een korte [&#x200B; wacht activiteit &#x200B;](wait-activity.md) aan het begin. U kunt buffertijd ook toestaan om nauwkeurige kwalificatie te verzekeren.

#### Waarom niet alle gekwalificeerde profielen de reis kunnen betreden {#streaming-entry-caveats}

Wanneer het gebruiken van het stromen publiek met de **activiteit van de Kwalificatie van het publiek 0&rbrace;, niet zullen alle profielen die voor het publiek kwalificeren noodzakelijk de reis ingaan.** Dit gedrag kan om de volgende redenen optreden:

* **Profielen reeds in het publiek**: Slechts zullen de profielen die onlangs voor het publiek kwalificeren nadat de reis wordt gepubliceerd ingang teweegbrengen. Profielen die al in het publiek aanwezig waren voordat ze werden gepubliceerd, worden niet ingevoerd.

* **de activeringstijd van de Reis**: Wanneer u een reis publiceert, neemt de **Kwalificatie van het Publiek** activiteit tot **10 minuten** om actief te worden en beginnen te luisteren naar profielingangen en weggaan. [&#x200B; Leer meer over reisactivering &#x200B;](#configure-segment-qualification).

* **Snel weggaat uit publiek**: Als een profiel voor het publiek kwalificeert maar weggaat alvorens de reisingang wordt teweeggebracht, kan dat profiel niet de reis ingaan.

* **Tijd tussen kwalificatie en reisverwerking**: wegens de verdeelde aard van [!DNL Adobe Experience Platform], kunnen er tijdhiaten zijn. Een profiel kan in aanmerking komen voordat de reis de kwalificatiegebeurtenis verwerkt.

**Aanbevelingen:**

* Na het publiceren van een reis, wacht minstens 10 minuten alvorens gebeurtenissen of gegevens te verzenden die profielkwalificatie zullen teweegbrengen. Dit zorgt ervoor dat de reis volledig geactiveerd is en klaar is om items te verwerken.

* Voor kritieke gebruiksgevallen waar u alle gekwalificeerde profielen moet verzekeren ingaan, denk na gebruikend a [&#x200B; Gelezen de activiteit van het publiek &#x200B;](read-audience.md) in plaats daarvan. Alle profielen in een publiek worden op een bepaald moment verwerkt.

* Bewaak het van de de ingang van uw reis [&#x200B; tarief en productie &#x200B;](entry-management.md#profile-entrance-rate) om de patronen van de profielstroom te begrijpen.

* Als de profielen niet zoals verwacht ingaan, verwijs naar de [&#x200B; het oplossen van problemengids &#x200B;](troubleshooting-execution.md#checking-if-people-enter-the-journey) voor extra kenmerkende stappen.

### Overbelasting voorkomen {#overloads-speed-segment-qualification}

Hier volgen enkele aanbevolen procedures om overbelastingsystemen te vermijden die tijdens reizen worden gebruikt (gegevensbronnen, aangepaste acties, kanaalactiviteiten):

* Gebruik een batchpubliek niet direct na het maken ervan in een **[!UICONTROL Audience Qualification]** -activiteit. Hierdoor wordt de eerste rekenpiek vermeden. Er verschijnt een gele waarschuwing op het canvas als u een publiek wilt gebruiken dat nog nooit is berekend.

  ![&#x200B; Foutbericht wanneer publiek niet gevonden in [!DNL Adobe Experience Platform]](assets/segment-error.png)

* Plaats een plafondregel voor gegevensbronnen en handelingen die tijdens reizen worden gebruikt om overbelasting te voorkomen. Leer meer in [&#x200B; documentatie van Journey Orchestration &#x200B;](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html?lang=nl-NL){target="_blank"}. De bijschilderregel hoeft niet opnieuw te worden uitgevoerd. Als u het opnieuw moet proberen, gebruikt u een alternatief pad in de reis door het vakje **[!UICONTROL Add an alternative path in case of a timeout or an error]** in voorwaarden of handelingen in te schakelen.

* Voordat u het publiek in een productiereis gaat gebruiken, moet u het aantal personen dat dagelijks voor dit publiek in aanmerking komt, evalueren. Controleer hiertoe het menu **[!UICONTROL Audience]** , open het publiek en bekijk de grafiek van **[!UICONTROL Profiles over time]** .

  ![&#x200B; het Bericht van de Waarschuwing wanneer het publiek teveel gebeurtenissen voor verwerking in real time &#x200B;](assets/segment-overload.png) heeft

Leer meer over de grenzen van het ingangstarief en productie in [&#x200B; deze sectie &#x200B;](entry-management.md#profile-entrance-rate).

## Afvoerkanalen en beperkingen {#audience-qualification-guardrails}

Volg de instructies en aanbevelingen hieronder om de reizen van de Kwalificatie van het publiek te bouwen. Zie ook [&#x200B; beste praktijken van de Kwalificatie van het publiek &#x200B;](#best-practices-segments).


* De reizen van de Kwalificatie van het publiek worden hoofdzakelijk ontworpen om met het stromen publiek te werken. Deze combinatie garandeert een betere real-time ervaring. Het wordt sterk geadviseerd om **het stromen publiek** in de activiteit van de Kwalificatie van het Publiek te gebruiken.

  Nochtans, als u partij op ingestitie-gebaseerde attributen in uw het stromen publiek of een partijpubliek voor een reis van de Kwalificatie van het Publiek wilt gebruiken, overweeg de tijdspanwijdte voor publieksevaluatie/activering. Een partijpubliek of het stromen publiek die batch-ingegane attributen gebruiken wordt klaar voor gebruik in de **activiteit van de Kwalificatie van het publiek ongeveer** 2 uren **na de voltooiing van uw segmentatietaak.** Deze taak wordt één keer per dag uitgevoerd op het tijdstip dat door de beheerder van de Adobe-organisatie is gedefinieerd.

* [!DNL Adobe Experience Platform] het publiek wordt berekend of eens per dag (**partij** publiek) of in real time (voor **gestroomd** publiek, gebruikend de Hoge optie van het Publiek van de Frequentie van [!DNL Adobe Experience Platform]).

   * Als het geselecteerde publiek wordt gestreamd, kunnen individuen die tot dit publiek behoren de reis in real time betreden.
   * Als het publiek een batch is, kunnen personen die net voor dit publiek zijn gekwalificeerd de reis invoeren wanneer de publieksberekening wordt uitgevoerd op [!DNL Adobe Experience Platform] .

  Als beste praktijken, gebruik het stromen publiek in de activiteit van de Kwalificatie van het publiek van het a **&#x200B;**. Voor de gevallen van het partijgebruik, gelieve te gebruiken a **[gelezen publiek](read-audience.md)** activiteit.

  >[!NOTE]
  >
  >Vanwege het batchkarakter van publiek dat is gemaakt met gebruik van compositieworkflows en aangepaste uploads, kunnen deze doelgroepen niet worden gericht op een activiteit die onder &quot;Audience Qualification&quot; valt. Alleen publiek dat is gemaakt met behulp van segmentdefinities kan in deze activiteit worden gebruikt.


* De groepen van het de gebeurtenisgebied van de ervaring kunnen niet in ritten worden gebruikt die met a **Gelezen Publiek**, a **de Kwalificatie van het Publiek** of a **BedrijfsGebeurtenis** activiteit beginnen.

* Wanneer het gebruiken van de Kwalificatie van het publiek **activiteit van het 0&rbrace; &lbrace;in een reis, kan die activiteit tot 10 minuten duren om actief te zijn en aan profielen te luisteren die of het publiek ingaan weggaan.**


>[!CAUTION]
>
>[&#x200B; Guardrails voor gegevens en segmentatie van het Profiel van de Klant in real time &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=nl-NL){target="_blank"} zijn ook op [!DNL Adobe Journey Optimizer] van toepassing.



## Hoe kan ik-video {#video}

Begrijp de toepasselijke gebruiksgevallen voor reizen van de Kwalificatie van het Publiek in deze video. Leer hoe u een reis maakt met de kwalificatie &#39;Audience Qualification&#39; en welke best practices u kunt toepassen.

>[!VIDEO](https://video.tv.adobe.com/v/3425028?quality=12)
