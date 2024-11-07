---
solution: Journey Optimizer
product: journey optimizer
title: Informatie over Adobe Experience Platform-publiek
description: Leer hoe u met het publiek van Adobe Experience Platform kunt werken
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 26d311802236a1f9e8f6273c1291bcb54138aad2
workflow-type: tm+mt
source-wordcount: '2048'
ht-degree: 0%

---

# Aan de slag met Adobe Experience Platform-publiek {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Doelgroep"
>abstract="Met Adobe Experience Platform kunt u eenvoudig segmentdefinities maken door gebruik te maken van realtime klantprofielgegevens. Zo kunt u doelgroepen maken die de unieke gedragingen en voorkeuren van uw klanten vastleggen."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="Selecteer het campagnepubliek"
>abstract="In deze lijst worden alle beschikbare Adobe Experience Platform-soorten publiek weergegeven. Selecteer het publiek voor uw campagne. Het bericht dat in de campagne wordt gevormd zal naar alle individuen worden verzonden die tot het geselecteerde publiek behoren. [ leer meer op publiek ](../audience/about-audiences.md)"

Een publiek is een groep personen die vergelijkbare gedragingen en/of kenmerken delen. Leer meer over publiek in de [ documentatie van de Dienst van de Segmentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html) {target="_blank"}.

Met [!DNL Journey Optimizer] kunt u rechtstreeks vanuit het menu **[!UICONTROL Audiences]** een Adobe Experience Platform-publiek maken en dit gebruiken voor reizen of campagnes.

Soorten publiek kan op verschillende manieren worden gegenereerd:

* **de definities van het Segment**: Creeer een nieuwe publieksdefinitie gebruikend de Dienst van de Segmentatie van Adobe Experience Platform. [ leer hoe te om segmentdefinities te bouwen ](creating-a-segment-definition.md)

* **Douane uploadt**: Invoer een publiek gebruikend een Csv- dossier. Leer hoe te om publiek in de documentatie van de Dienst van de Segmentatie van Adobe Experience Platform [ in te voeren ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience) {target="_blank"}.

* **samenstelling van het publiek**: Creeer een samenstellingswerkschema om bestaand publiek van Adobe Experience Platform in een visueel canvas te combineren en hefboomwerking diverse activiteiten (spleet, sluit uit...) om nieuw publiek tot stand te brengen. [ worden begonnen met publiekssamenstelling ](get-started-audience-orchestration.md)

* **Federated Audience Composition**: De datasets van de federatie direct van uw bestaand gegevenspakhuis om het publiek en de attributen van Adobe Experience Platform allen in één systeem te bouwen en te verrijken. Gelieve te lezen de gids op [ Federated de Samenstelling van het Publiek ](https://experienceleague.adobe.com/en/docs/federated-audience-composition/using/home).

  >[!AVAILABILITY]
  >
  >Federated Audience Composition is momenteel alleen beschikbaar voor een set organisaties (beperkte beschikbaarheid). Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

Voor meer informatie over het gebruik van Douane uploadt en Federated publiek van de Samenstelling van het Publiek in [!DNL Journey Optimizer], verwijs naar [ deze sectie ](custom-upload-fac.md).

## Doelpubliek in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

U kunt in campagnes selecteren en reizen om het even welk publiek dat gebruikend segmentdefinities, douane wordt geproduceerd uploadt, samenstellingswerkschema&#39;s of Federated de Samenstelling van de Publiek wordt geproduceerd.

>[!AVAILABILITY]
>
>Het gebruik van soorten publiek en kenmerken van de samenstelling van het publiek is momenteel niet beschikbaar voor gebruik met het gezondheidsschild of het privacyschild. [ Leer hoe te om de attributen van de kijkverrijking in Journey Optimizer te gebruiken ](../audience/about-audiences.md#enrichment)

U kunt het publiek op verschillende manieren gebruiken in **[!DNL Journey Optimizer]** :

* Kies een publiek voor a **campagne**, waar het bericht wordt verzonden naar alle individuen die tot het geselecteerde publiek behoren. [ Leer hoe te om het publiek van een campagne ](../campaigns/create-campaign.md#define-the-audience-audience) te bepalen.

* Gebruik a **Gelezen publiek** orkestactiviteit in een reis om alle individuen in het publiek te maken de reis ingaan en de berichten ontvangen inbegrepen in uw reis. Laten we zeggen dat je een &quot;zilveren klant&quot; publiek hebt. Met deze activiteit, kunt u alle zilveren klanten een reis maken en hen een reeks gepersonaliseerde berichten verzenden. [ Leer hoe te om Gelezen publieksactiviteit ](../building-journeys/read-audience.md#configuring-segment-trigger-activity) te vormen.

* Gebruik de **activiteit van de Voorwaarde** in een reis om voorwaarden te bouwen die op publiekslidmaatschap worden gebaseerd. [ leer hoe te om publiek in voorwaarden ](../building-journeys/condition-activity.md#using-a-segment) te gebruiken.

* Gebruik de **gebeurtenisactiviteit van de kwalificatie van het publiek 0} {in een reis om individuen te maken ingaan of zich voorwaarts in de reis die op de kijkposten van Adobe Experience Platform en uitgang wordt gebaseerd.** U kunt bijvoorbeeld alle nieuwe zilverklanten een reis laten maken en hun berichten sturen. Voor meer op hoe te om deze activiteit te gebruiken, verwijs naar [ hoe te om een de kwalificatieactiviteit van het Publiek te vormen ](../building-journeys/audience-qualification-events.md).

  >[!NOTE]
  >
  >Vanwege het batchkarakter van publiek dat is gemaakt met gebruik van compositieworkflows, aangepaste upload of Federated Audience Composition, kunt u deze soorten publiek niet als doelgroep instellen in een &#39;Audience Qualification&#39;-activiteit. Alleen publiek dat is gemaakt met behulp van segmentdefinities kan in deze activiteit worden gebruikt.

## Verrijkingskenmerken van soorten publiek gebruiken {#enrichment}

Wanneer het richten van een publiek dat gebruikend samenstellingswerkschema&#39;s, het publiek van het douane (Csv- dossier), of Federated de Samenstelling van het Publiek wordt geproduceerd, kunt u hefboomwerkingsattributen van deze publiek gebruiken om uw reis te bouwen en uw berichten te personaliseren.

>[!NOTE]
>
>Soorten publiek dat vóór 1 oktober 2024 via aangepaste upload naar CSV-bestanden is gemaakt, komen niet in aanmerking voor personalisatie. Als u kenmerken van deze doelgroepen wilt gebruiken en ten volle wilt profiteren van deze functie, maakt u een extern CSV-publiek dat u vóór deze datum hebt geïmporteerd, opnieuw en uploadt u het opnieuw.
>
>Het beleid van de toestemming steunt geen verrijkingsattributen. Daarom moeten regels voor het toestemmingsbeleid alleen gebaseerd zijn op kenmerken in het profiel.

Hier volgen de acties die u kunt uitvoeren met de verrijkingskenmerken van het publiek:

* **creeer veelvoudige weg in een reis** die op regels wordt gebaseerd die hefboomwerking de de verrijkingsattributen van het doelpubliek. Om dit te doen, richt het publiek dat a [ gebruikt gelezen publiek ](../building-journeys/read-audience.md) activiteit dan tot regels in de activiteit van de Voorwaarde van a [ ](../building-journeys/condition-activity.md) leidt die op de verrijkingsattributen van het publiek wordt gebaseerd.

  ![](assets/audience-enrichment-attribute-condition.png){width="70%" zoomable="yes"}

* **personaliseer uw berichten** in reizen of campagnes door verrijkingsattributen van het gerichte publiek in de verpersoonlijkingsredacteur toe te voegen. [ Leer hoe te met de verpersoonlijkingsredacteur ](../personalization/personalization-build-expressions.md) te werken

  ![](assets/audience-enrichment-attribute-perso.png){width="70%" zoomable="yes"}

>[!IMPORTANT]
>
>Om verrijkingsattributen van publiek te gebruiken creeerde het gebruiken van samenstellingswerkschema&#39;s, zorg ervoor dat zij aan een Groep van het Gebied binnen &quot;ExperiencePlatform&quot;Gegevens Source worden toegevoegd.
>
+++ Leer hoe u verrijkingskenmerken aan een veldgroep kunt toevoegen>
>
1. Navigeer naar &quot;Beheer&quot; > &quot;Configuratie&quot; > &quot;Gegevensbronnen&quot;.
1. Selecteer Experience Platform en maak of bewerk een veldgroep.
1. Selecteer het gewenste schema in de schemaselector. De naam van het schema heeft de volgende indeling: &#39;Schema voor publiek-id:&#39; + de id van het publiek. U kunt de id van het publiek vinden op het scherm met publieksdetails in de publieksinventaris.
1. Open de veldkiezer, zoek de verrijkingskenmerken die u wilt toevoegen en selecteer het selectievakje naast deze kenmerken.
1. Sla uw wijzigingen op.
1. Nadat verrijkingskenmerken aan een veldgroep zijn toegevoegd, kunt u deze op de hierboven vermelde locaties benutten in Journey Optimizer.
>
Gedetailleerde informatie over gegevensbronnen is beschikbaar in deze secties:
>
* [ Werk met de gegevensbron van Adobe Experience Platform ](../datasource/adobe-experience-platform-data-source.md)
* [ vorm een gegevensbron ](../datasource/configure-data-sources.md)
>
+++

## Methoden voor de evaluatie van het publiek {#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer wordt het publiek gegenereerd op basis van segmentdefinities aan de hand van een van de drie onderstaande evaluatiemethoden.

+++ Streaming segmentering

De profiellijst voor het publiek wordt bijgewerkt in real time aangezien de nieuwe gegevens in het systeem stromen.

Streaming segmentatie is een doorlopend proces voor gegevensselectie dat uw publiek bijwerkt als reactie op gebruikersactiviteit. Zodra een segmentdefinitie is gebouwd en het resulterende publiek is bewaard, wordt de segmentdefinitie toegepast op inkomende gegevens aan Journey Optimizer. Dit betekent dat individuen worden toegevoegd of uit het publiek verwijderd aangezien hun profielgegevens veranderen, ervoor zorgen dat uw doelpubliek altijd relevant is. [ leer meer ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html) {target="_blank"}

>[!NOTE]
>
Zorg ervoor dat u de juiste gebeurtenissen gebruikt als criteria voor streamingsegmentatie. [Meer informatie](#streaming-segmentation-events-guardrails)

+++

+++ Batchsegmentatie

De profiellijst voor het publiek wordt om de 24 uur geëvalueerd.

De segmentatie van de partij is een alternatief aan het stromen segmentatie die alle profielgegevens in één keer door segmentdefinities verwerkt. Zo maakt u een momentopname van het publiek die u kunt opslaan en exporteren voor gebruik. Nochtans, in tegenstelling tot het stromen segmentatie, werkt de partijsegmentatie niet onophoudelijk de publiekslijst in real time bij, en de nieuwe gegevens die binnen na het partijproces komen zullen niet in het publiek tot het volgende partijproces worden weerspiegeld. [ leer meer ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#batch) {target="_blank"}

+++

+++ Edge-segmentatie

De segmentatie van Edge is de capaciteit om segmenten in Adobe Experience Platform onmiddellijk [ op de rand ](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) {target="_blank"} te evalueren, toelatend zelfde-pagina en volgende-pagina verpersoonlijkingsgebruiksgevallen. Momenteel kunnen alleen bepaalde querytypen worden geëvalueerd met randsegmentatie. [ leer meer ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/edge-segmentation.html#query-types) {target="_blank"}

+++

Als u weet welke evaluatiemethode u wilt gebruiken, selecteer het gebruikend de drop-down lijst. U kunt ook op het pictogram van de bladerpictogrammap met een vergrootglas klikken om een lijst met de beschikbare evaluatiemethoden voor segmentdefinitie weer te geven. [ leer meer ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#segment-properties) {target="_blank"}

![](assets/evaluation-methods.png)

<!--The determination between batch segmentation and streaming segmentation is made by the system for each audience, based on the complexity and the cost of evaluating the segment definition rule. You can view the evaluation method for each audience in the **[!UICONTROL Evaluation method]** column of the audience list.
    
![](assets/evaluation-method.png)

>[!NOTE]
>
>If the **[!UICONTROL Evaluation method]** column does not display, you  need to add it using configuration button on the top right of the list.-->

Nadat u een publiek voor het eerst hebt gedefinieerd, worden profielen toegevoegd aan het publiek wanneer deze in aanmerking komen.

Het ondersteunen van het publiek op basis van eerdere gegevens kan 24 uur in beslag nemen. Nadat het publiek is teruggevuld, wordt het publiek voortdurend bijgewerkt en is altijd klaar om zich te richten.

### Gebeurtenisgebruik met streaming segmentatie {#streaming-segmentation-events-guardrails}

Streaming segmentatie is handig voor realtime personalisatie met gebruik van hoge waarden. Nochtans, is het belangrijk om de juiste [ gebeurtenissen ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#events) te kiezen {target="_blank"} om als segmenteringscriteria te gebruiken.

Voor het streamen van segmentatie zijn optimale prestaties dus beter geen gebruik te maken van de volgende gebeurtenissen:

* **Geopend Bericht** gebeurtenis van het Type van Interactie

  Wanneer het bouwen van uw publiek, werd het gebruik van **Geopende** interactiegebeurtenissen van het Bericht onbetrouwbaar, omdat zij geen daadwerkelijke indicatoren van gebruikersactiviteit zijn en segmentatieprestaties negatief kunnen beïnvloeden. Leer waarom in deze [ post van Blog van de Adobe ](https://blog.adobe.com/en/publish/2021/06/24/what-apples-mail-privacy-protection-means-for-email-marketers) {target="_blank"}. Vandaar, adviseert de Adobe niet het gebruiken van **Geopend Bericht** interactiegebeurtenissen met het stromen segmentatie. In plaats daarvan, gebruik echte user-activity signalen zoals kliks, aankopen, of baken gegevens.

* **Bericht verzonden** gebeurtenis van de Status van de Terugkoppeling

  Het **verzonden Bericht** terugkoppelt gebeurtenis wordt vaak gebruikt voor frequentie of onderdrukking die voorafgaand aan het verzenden van een e-mail controleert. Adobe beveelt aan dit te vermijden omdat dit de prestaties onder druk zet en het systeem kan aantasten. Daarom voor frequentie of suppressielogica, gebruiks bedrijfsregels eerder dan **verzonden Bericht** terugkoppelt gebeurtenissen. Merk op dat de dagelijkse frequentiecijfers voor individuele profielen binnenkort beschikbaar zullen zijn, als aanvulling op de bestaande maandelijkse wachttijden voor bedrijfsregels.

>[!NOTE]
>
U kunt **Geopend Bericht gebruiken** en **Bericht Verzonden** gebeurtenissen in partijsegmentatie zonder enige prestatieszorgen.

## Samenstelling publiek en Veelgestelde vragen over aangepaste upload {#faq}

In de volgende sectie worden vaak gestelde vragen weergegeven over het gebruik in Journey Optimizer van soorten publiek dat is gemaakt met compositieworkflows en aangepaste upload (CSV-bestanden).

+++ Waar kan ik publiek van publiekssamenstelling en douane uploaden binnen Journey Optimizer gebruiken?

De doelgroepen van de samenstelling van de doelgroep en de aangepaste upload kunnen worden gericht of van campagnes en reizen. [ leer hoe te om publiek in  [!DNL Journey Optimizer]](#segments-in-journey-optimizer) te richten

* In **Campagnes**, verschijnen deze publiek in de publieksplukker na het klikken van de &quot;Uitgezochte publieksknoop&quot;.

* In **Weizen**, kunt u deze toehoorders in een &quot;Gelezen activiteit van het Publiek&quot;tijdens publieksselectie, en in een &quot;Voorwaarde&quot;activiteit voor de controles van het publiekslidmaatschap gebruiken. Wegens hun partijdige aard komen deze soorten publiek echter niet voor in de activiteit &quot;Audience Qualification&quot;.

  >[!NOTE]
  >
  Als &#39;Incrementeel lezen&#39; tijdens een terugkerende rit is ingeschakeld voor een aangepast uploadpubliek, worden profielen alleen bij de eerste terugkerende actie opgehaald, omdat deze doelgroepen vast zijn.

Bovendien, zijn deze publiek beschikbaar voor gebruik in de verpersoonlijkingsredacteur om uw berichten in reizen en campagnes te personaliseren. [ Leer hoe te met de verpersoonlijkingsredacteur ](../personalization/personalization-build-expressions.md) te werken

+++

+++ Wat zijn verrijkingskenmerken?

Verrijkingskenmerken zijn aanvullende kenmerken die contextueel zijn en specifiek zijn voor een publiek. Ze zijn niet gekoppeld aan het profiel en worden doorgaans gebruikt voor personalisatiedoeleinden.

De attributen van de verrijking zijn verbonden met een publiek via [ verrijken ](composition-canvas.md#enrich) activiteit in publiekssamenstelling of door het douane uploadt proces.

+++

+++ Waar kan ik verrijkingskenmerken gebruiken in Journey Optimizer?

De attributen van de verrijking van publiekssamenstelling kunnen in de volgende gebieden worden gebruikt. [ Leer hoe te om de attributen van de kijkverrijking ](#enrichment) te gebruiken

* Condition activity (Reizen)
* Aangepaste actiekenmerken (reizen)
* Berichten personaliseren (reizen en campagnes)

+++

+++ Hoe laat ik verrijkingskenmerken toe in Reizen?

Om verrijkingsattributen van publiek te gebruiken creeerde het gebruiken van samenstellingswerkschema&#39;s, zorg ervoor zij aan een Groep van het Gebied binnen &quot;ExperiencePlatform&quot;Gegevens Source worden toegevoegd. De informatie over hoe te om verrijkingsattributen aan een Groep van het Gebied toe te voegen is beschikbaar in [ deze sectie ](#enrichment)

+++

+++ Hoe snel kan ik het in Journey Optimizer gebruiken nadat ik een publiek heb gepubliceerd vanuit de compositie van het publiek of aangepaste upload?

* Het publiek van **publiekssamenstelling** wordt dagelijks uitgevoerd, zodat kunt u tot 24 uren moeten wachten om hen in Journey Optimizer te gebruiken.
* Het publiek van **douane uploadt** wordt beschikbaar in Journey Optimizer ongeveer 2 uur na publicatie.

+++

+++ Zijn de waarden van verrijkingsattributen bijgewerkt nadat een reis begint?

Neen. Zelfs na wachttijden of gebeurtenisknopen, blijven de waarden van de verrijkingsattributen het zelfde als zij toen de reis begon.

+++

+++ Hoe voegen aangepaste uploadgroepen zich aan bij profielen?

Tijdens het aangepaste uploadproces geeft u het CSV-kenmerk op dat u wilt gebruiken als de identiteit en de profielidentiteit waarnaar het verwijst. Hiermee wordt een koppeling tot stand gebracht tussen de publieksgegevens en het profiel. Als het CSV-bestand een identiteitswaarde bevat die niet wordt gevonden in het profiel, wordt een nieuw profiel met die identiteitswaarde gemaakt.

De gedetailleerde informatie over het douane uploadt proces is beschikbaar in de documentatie van de Dienst van de Segmentatie van Adobe Experience Platform [ ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience) {target="_blank"}.

+++

+++ Hoe vers zijn mijn gegevens in Journey Optimizer?

De gegevens in publiek van publiekssamenstelling en douane uploadt worden bevolkt door de Dienst van de Uitvoer van het Publiek (AES). AES leest profielattributen en publiekslidmaatschap, die het aan deze publiek met de volgende chronologie ter beschikking stelt:

* **de samenstelling van het publiek**: Dagelijkse uitvoer (~24 uren)
* **Aangepaste upload**: Specifieke de uitvoerbaan (~2 uren)

Elke reis die een publiek van publiekssamenstelling of douane uploadt in de activiteit van het &quot;Gelezen publiek&quot;gebruikt zal profielattributen zo vers zoals de laatste partijevaluatie hebben. Dit omvat toestemming/onderdrukking tijdens de reis.

Bovendien, zijn de verrijkte attributen in publiek samenstellingspubliek zo vers zoals de laatste samenstellingslooppas, die tot 24 uren in het verleden kan zijn.

+++

## Hoe kan ik-video {#video}

Meer informatie over uniforme klantprofielen en soorten publiek in Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3432671?quality=12)
