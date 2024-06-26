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
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '1854'
ht-degree: 0%

---

# Aan de slag met Adobe Experience Platform-publiek {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Publiek"
>abstract="Met Adobe Experience Platform kunt u eenvoudig segmentdefinities maken door gebruik te maken van realtime klantprofielgegevens. Zo kunt u doelgroepen maken die de unieke gedragingen en voorkeuren van uw klanten vastleggen."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="Selecteer het campagnepubliek"
>abstract="In deze lijst worden alle beschikbare Adobe Experience Platform-soorten publiek weergegeven. Selecteer het publiek voor uw campagne. Het bericht dat in de campagne wordt gevormd zal naar alle individuen worden verzonden die tot het geselecteerde publiek behoren. [Meer informatie over publiek](../audience/about-audiences.md)"

Een publiek is een groep personen die vergelijkbare gedragingen en/of kenmerken delen. Meer informatie over het publiek in de [Adobe Experience Platform Segmentation Service-documentatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target="_blank"}.

[!DNL Journey Optimizer] biedt u de mogelijkheid om Adobe Experience Platform-publiek rechtstreeks te maken vanuit de **[!UICONTROL Audiences]** en gebruikt u deze voor reizen of campagnes.

Soorten publiek kan op verschillende manieren worden gegenereerd:

* **Segmentdefinities**: Maak een nieuwe publieksdefinitie met Adobe Experience Platform Segmentation Service. [Leer hoe te om segmentdefinities te bouwen](creating-a-segment-definition.md)
* **Aangepaste upload**: Importeer een publiek met een CSV-bestand. Meer informatie over het importeren van soorten publiek in Adobe Experience Platform [Documentatie voor segmentatieservice](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}.
* **Samenstelling publiek**: Maak een compositieworkflow om bestaande Adobe Experience Platform-soorten publiek te combineren tot een visueel canvas en gebruik verschillende activiteiten (splitsen, uitsluiten...) om een nieuw publiek te maken. [Aan de slag met publiekscompositie](get-started-audience-orchestration.md)

## Doelpubliek in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

U kunt in campagnes selecteren en reizen om het even welk publiek dat gebruikend segmentdefinities, douane wordt geproduceerd uploadt of samenstellingswerkschema&#39;s.

>[!AVAILABILITY]
>
>Het gebruik van soorten publiek en kenmerken van publiek compositie en aangepast uploadpubliek (CSV-bestand) is momenteel niet beschikbaar voor gebruik met Healthcare Shield of Privacy and Security Shield. [Meer informatie over het gebruik van verrijkingskenmerken voor doelgroepen in Journey Optimizer](../audience/about-audiences.md#enrichment)

U kunt het publiek benutten in **[!DNL Journey Optimizer]** op verschillende manieren:

* Kies een publiek voor een **campagne**, waarbij het bericht wordt verzonden naar alle personen die tot het geselecteerde publiek behoren. [Leer hoe u het publiek van een campagne definieert](../campaigns/create-campaign.md#define-the-audience-audience).

* Een **Lees publiek** Orchestratie-activiteit op een reis om ervoor te zorgen dat alle individuen in het publiek de reis betreden en de berichten ontvangen inbegrepen in uw reis. Laten we zeggen dat je een &quot;zilveren klant&quot; publiek hebt. Met deze activiteit, kunt u alle zilveren klanten een reis maken en hen een reeks gepersonaliseerde berichten verzenden. [Leer hoe te om een Gelezen publieksactiviteit te vormen](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Gebruik de **Voorwaarde** activiteit op een reis om voorwaarden op te bouwen die op het lidmaatschap van het publiek worden gebaseerd. [Meer informatie over het gebruik van soorten publiek in omstandigheden](../building-journeys/condition-activity.md#using-a-segment).

* Gebruik de **kwalificatie publiek** gebeurtenisactiviteit op een reis om ervoor te zorgen dat individuen de reis betreden of vooruit gaan op basis van de toegang tot en het vertrek van Adobe Experience Platform-gebruikers. U kunt bijvoorbeeld alle nieuwe zilverklanten een reis laten maken en hun berichten sturen. Raadpleeg voor meer informatie over het gebruik van deze activiteit [Leer hoe te om een de kwalificatieactiviteit van het Publiek te vormen](../building-journeys/audience-qualification-events.md).

  >[!NOTE]
  >
  >Vanwege de batchaard van publiek dat is gemaakt met gebruik van compositieworkflows en aangepaste upload, kunt u deze soorten publiek niet als doelgroep instellen in de activiteit ‘Kwalificatie van publiek’. Alleen publiek dat is gemaakt met behulp van segmentdefinities kan in deze activiteit worden gebruikt.

## Verrijkingskenmerken van soorten publiek gebruiken {#enrichment}

Wanneer het richten van een publiek dat gebruikend samenstellingswerkschema&#39;s wordt geproduceerd, kunt u verrijkingsattributen van deze publiek gebruiken om uw reis te bouwen en uw berichten te personaliseren.

Als u verrijkingskenmerken wilt gebruiken in een reis, moet u ervoor zorgen dat deze worden toegevoegd aan een veldgroep binnen de gegevensbron &quot;ExperiencePlatform&quot;.

+++ Leer hoe u verrijkingskenmerken aan een veldgroep kunt toevoegen

1. Navigeer naar &quot;Beheer&quot; > &quot;Configuratie&quot; > &quot;Gegevensbronnen&quot;.
1. Selecteer Experience Platform en maak of bewerk een veldgroep.
1. Open de veldkiezer, zoek de verrijkingskenmerken die u wilt toevoegen en selecteer het selectievakje naast deze kenmerken.
1. Sla uw wijzigingen op.

Gedetailleerde informatie over gegevensbronnen is beschikbaar in deze secties:

* [Werken met de Adobe Experience Platform-gegevensbron](../datasource/adobe-experience-platform-data-source.md)
* [Een gegevensbron configureren](../datasource/configure-data-sources.md)

+++

Nadat verrijkingskenmerken aan een veldgroep zijn toegevoegd, kunt u deze op verschillende locaties in Journey Optimizer benutten:

* **Meerdere paden maken voor een rit** gebaseerd op regels die de verrijkingskenmerken van het doelpubliek benutten. Als u dit wilt doen, richt u de doelgroep op met een [Lees publiek](../building-journeys/read-audience.md) activiteit creeert dan regels in [Voorwaarde](../building-journeys/condition-activity.md) activiteit op basis van de verrijkingskenmerken van het publiek .

  ![](assets/audience-enrichment-attribute-condition.png){width="70%" zoomable="yes"}

* **Je berichten personaliseren** bij reizen of campagnes door verrijkingskenmerken van het doelpubliek toe te voegen in de personalisatie-editor. [Leer hoe u met de verpersoonlijkingseditor werkt](../personalization/personalization-build-expressions.md)

  ![](assets/audience-enrichment-attribute-perso.png){width="70%" zoomable="yes"}

>[!AVAILABILITY]
>
>Aangepaste verrijkingskenmerken voor uploaden zijn nog niet beschikbaar voor gebruik in Journey Optimizer.

## Methoden voor de evaluatie van het publiek {#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer wordt het publiek gegenereerd op basis van segmentdefinities aan de hand van een van de drie onderstaande evaluatiemethoden.

+++ Streaming segmentering

De profiellijst voor het publiek wordt bijgewerkt in real time aangezien de nieuwe gegevens in het systeem stromen.

Streaming segmentatie is een doorlopend proces voor gegevensselectie dat uw publiek bijwerkt als reactie op gebruikersactiviteit. Zodra een segmentdefinitie is gebouwd en het resulterende publiek is bewaard, wordt de segmentdefinitie toegepast op inkomende gegevens aan Journey Optimizer. Dit betekent dat individuen worden toegevoegd of uit het publiek verwijderd aangezien hun profielgegevens veranderen, ervoor zorgen dat uw doelpubliek altijd relevant is. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"}

>[!NOTE]
>
>Zorg ervoor dat u de juiste gebeurtenissen gebruikt als criteria voor streamingsegmentatie. [Meer informatie](#streaming-segmentation-events-guardrails)

+++

+++ Batchsegmentatie

De profiellijst voor het publiek wordt om de 24 uur geëvalueerd.

De segmentatie van de partij is een alternatief aan het stromen segmentatie die alle profielgegevens in één keer door segmentdefinities verwerkt. Zo maakt u een momentopname van het publiek die u kunt opslaan en exporteren voor gebruik. Nochtans, in tegenstelling tot het stromen segmentatie, werkt de partijsegmentatie niet onophoudelijk de publiekslijst in real time bij, en de nieuwe gegevens die binnen na het partijproces komen zullen niet in het publiek tot het volgende partijproces worden weerspiegeld. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#batch){target="_blank"}

+++

+++ Randsegmentatie

Randsegmentatie is de mogelijkheid om segmenten in Adobe Experience Platform ogenblikkelijk te evalueren [op de rand](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"}en maakt het gebruik van hoofdletters en kleine letters mogelijk voor het aanpassen van pagina&#39;s. Momenteel kunnen alleen bepaalde querytypen worden geëvalueerd met randsegmentatie. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/edge-segmentation.html#query-types){target="_blank"}

+++

Als u weet welke evaluatiemethode u wilt gebruiken, selecteer het gebruikend de drop-down lijst. U kunt ook op het pictogram van de bladerpictogrammap met een vergrootglas klikken om een lijst met de beschikbare evaluatiemethoden voor segmentdefinitie weer te geven. [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#segment-properties){target="_blank"}

![](assets/evaluation-methods.png)

<!--The determination between batch segmentation and streaming segmentation is made by the system for each audience, based on the complexity and the cost of evaluating the segment definition rule. You can view the evaluation method for each audience in the **[!UICONTROL Evaluation method]** column of the audience list.
    
![](assets/evaluation-method.png)

>[!NOTE]
>
>If the **[!UICONTROL Evaluation method]** column does not display, you  need to add it using configuration button on the top right of the list.-->

Nadat u een publiek voor het eerst hebt gedefinieerd, worden profielen toegevoegd aan het publiek wanneer deze in aanmerking komen.

Het ondersteunen van het publiek op basis van eerdere gegevens kan 24 uur in beslag nemen. Nadat het publiek is teruggevuld, wordt het publiek voortdurend bijgewerkt en is altijd klaar om zich te richten.

### Gebeurtenisgebruik met streaming segmentatie {#streaming-segmentation-events-guardrails}

Streaming segmentatie is handig voor realtime personalisatie met gebruik van hoge waarden. Het is echter belangrijk dat u het recht kiest [gebeurtenissen](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#events){target="_blank"} als segmenteringscriteria te gebruiken.

Voor het streamen van segmentatie zijn optimale prestaties dus beter geen gebruik te maken van de volgende gebeurtenissen:

* **Bericht geopend** Interactietype, gebeurtenis

  Wanneer het opbouwen van uw publiek, gebruik van **Bericht geopend** interactiegebeurtenissen werden onbetrouwbaar omdat ze geen werkelijke indicatoren van gebruikersactiviteit zijn en de segmentatieprestaties negatief kunnen beïnvloeden. Meer weten waarom in dit [Blogbericht Adobe](https://blog.adobe.com/en/publish/2021/06/24/what-apples-mail-privacy-protection-means-for-email-marketers){target="_blank"}. Daarom beveelt de Adobe aan geen gebruik te maken van **Bericht geopend** interactiegebeurtenissen met streaming segmentatie. In plaats daarvan, gebruik echte user-activity signalen zoals kliks, aankopen, of baken gegevens.

* **Bericht verzonden** Feedbackstatus, gebeurtenis

  De **Bericht verzonden** feedbackgebeurtenis wordt vaak gebruikt voor frequentie- of suppressiecontroles voordat een e-mail wordt verzonden. Adobe beveelt aan dit te vermijden omdat dit de prestaties onder druk zet en het systeem kan aantasten. Daarom voor frequentie of suppression logica, gebruiks bedrijfsregels eerder dan **Bericht verzonden** feedbackgebeurtenissen. Merk op dat de dagelijkse frequentiecijfers voor individuele profielen binnenkort beschikbaar zullen zijn, als aanvulling op de bestaande maandelijkse wachttijden voor bedrijfsregels.

>[!NOTE]
>
>U kunt **Bericht geopend** en **Bericht verzonden** gebeurtenissen in batchsegmentatie zonder prestatieproblemen.


## Samenstelling publiek en Veelgestelde vragen over aangepaste upload {#faq}

In de volgende sectie worden vaak gestelde vragen weergegeven over het gebruik in Journey Optimizer van soorten publiek dat is gemaakt met compositieworkflows en aangepaste upload (CSV-bestanden).

+++ Waar kan ik publiek van publiekssamenstelling en douane uploaden binnen Journey Optimizer gebruiken?

De doelgroepen van de samenstelling van de doelgroep en de aangepaste upload kunnen worden gericht of van campagnes en reizen. [Leer hoe u doelgroepen kunt maken in [!DNL Journey Optimizer]](#segments-in-journey-optimizer)

* In **Campagnes**, worden deze soorten publiek weergegeven in de publiekskiezer nadat u op de knop voor het selecteren van het publiek hebt geklikt.

* In **Reizen** kunt u deze doelgroepen gebruiken in een activiteit &#39;Publiek lezen&#39; tijdens de selectie van het publiek en in een activiteit &#39;Voorwaarde&#39; voor de controles van het publiekslidmaatschap. Wegens hun partijdige aard komen deze soorten publiek echter niet voor in de activiteit &quot;Audience Qualification&quot;.

  >[!NOTE]
  >
  >Als &#39;Incrementeel lezen&#39; tijdens een terugkerende rit is ingeschakeld voor een aangepast uploadpubliek, worden profielen alleen bij de eerste terugkerende actie opgehaald, omdat deze doelgroepen vast zijn.

Bovendien, zijn deze publiek beschikbaar voor gebruik in de verpersoonlijkingsredacteur om uw berichten in reizen en campagnes te personaliseren. [Leer hoe u met de verpersoonlijkingseditor werkt](../personalization/personalization-build-expressions.md)

+++

+++ Wat zijn verrijkingskenmerken?

Verrijkingskenmerken zijn aanvullende kenmerken die contextueel zijn en specifiek zijn voor een publiek. Ze zijn niet gekoppeld aan het profiel en worden doorgaans gebruikt voor personalisatiedoeleinden.

Verrijkingskenmerken zijn gekoppeld aan een publiek via een [Verrijken](composition-canvas.md#enrich) activiteit in publiekssamenstelling of door het douane uploadproces.

+++

+++ Waar kan ik verrijkingskenmerken gebruiken in Journey Optimizer?

De attributen van de verrijking van publiekssamenstelling kunnen in de volgende gebieden worden gebruikt. [Leer hoe u verrijkingskenmerken voor het publiek kunt gebruiken](#enrichment)

* Condition activity (Reizen)
* Aangepaste actiekenmerken (reizen)
* Berichten personaliseren (reizen en campagnes)

>[!AVAILABILITY]
>
>Aangepaste verrijkingskenmerken voor uploaden zijn nog niet beschikbaar voor gebruik in Journey Optimizer.

+++

+++ Hoe laat ik verrijkingskenmerken toe in Reizen?

Als u verrijkingskenmerken wilt gebruiken in een reis, moet u ervoor zorgen dat deze worden toegevoegd aan een veldgroep binnen de gegevensbron &quot;ExperiencePlatform&quot;. Informatie over het toevoegen van verrijkingskenmerken aan een veldgroep vindt u in [deze sectie](#enrichment)

+++

+++ Hoe snel kan ik het in Journey Optimizer gebruiken nadat ik een publiek heb gepubliceerd vanuit de compositie van het publiek of aangepaste upload?

* Soorten publiek van **publiekscompositie** worden dagelijks uitgevoerd, dus u moet mogelijk tot 24 uur wachten om ze in Journey Optimizer te gebruiken.
* Soorten publiek van **aangepaste upload** ongeveer 2 uur na publicatie beschikbaar worden in Journey Optimizer.

+++

+++ Zijn de waarden van verrijkingsattributen bijgewerkt nadat een reis begint?

Neen. Zelfs na wachttijden of gebeurtenisknopen, blijven de waarden van de verrijkingsattributen het zelfde als zij toen de reis begon.

+++

+++ Hoe voegen aangepaste uploadgroepen zich aan bij profielen?

Tijdens het aangepaste uploadproces geeft u het CSV-kenmerk op dat u wilt gebruiken als de identiteit en de profielidentiteit waarnaar het verwijst. Hiermee wordt een koppeling tot stand gebracht tussen de publieksgegevens en het profiel. Als het CSV-bestand een identiteitswaarde bevat die niet wordt gevonden in het profiel, wordt een nieuw profiel met die identiteitswaarde gemaakt.

In Adobe Experience Platform is gedetailleerde informatie beschikbaar over het aangepaste uploadproces [Documentatie voor segmentatieservice](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}.

+++

+++ Hoe vers zijn mijn gegevens in Journey Optimizer?

De gegevens in publiek van publiekssamenstelling en douane uploadt worden bevolkt door de Dienst van de Uitvoer van het Publiek (AES). AES leest profielattributen en publiekslidmaatschap, die het aan deze publiek met de volgende chronologie ter beschikking stelt:

* **Samenstelling publiek**: Dagelijkse export (~24 uur)
* **Aangepaste upload**: Specifieke exporttaak (~2 uur)

Elke reis die een publiek van publiekssamenstelling of douane uploadt in de activiteit van het &quot;Gelezen publiek&quot;gebruikt zal profielattributen zo vers zoals de laatste partijevaluatie hebben. Dit omvat toestemming/onderdrukking tijdens de reis.

Bovendien, zijn de verrijkte attributen in publiek samenstellingspubliek zo vers zoals de laatste samenstellingslooppas, die tot 24 uren in het verleden kan zijn.

+++

