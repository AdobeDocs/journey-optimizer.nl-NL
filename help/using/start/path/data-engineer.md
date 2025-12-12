---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer Get Started for Data Engineer
description: Als gegevensengineer leert u meer hoe u met Journey Optimizer kunt werken
feature: Get Started
role: Developer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 1%

---

# Aan de slag voor Data Engineer {#data-engineer}

Als **Ingenieur van de Gegevens van Adobe Journey Optimizer**, bereidt u en handhaaft de gegevens van het klantenprofiel voor om de ervaringen aan te drijven die door [!DNL Journey Optimizer] worden georganiseerd, modelklant en bedrijfsgegevens in schema&#39;s en vormt bronschakelaars voor het opnemen van gegevens. U kunt met [!DNL Adobe Journey Optimizer] beginnen te werken zodra de [&#x200B; Beheerder van het Systeem &#x200B;](administrator.md) u toegang verleende en uw milieu voorbereidde.

>[!NOTE]
>
>Leer meer over **gegevensopname** in [&#x200B; documentatie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html){target="_blank"}.

## Essentiële stappen voor gegevensconfiguratie

Voer de volgende stappen uit om de gegevensbasis voor Journey Optimizer in te stellen:

1. **creeer identiteitsnaamruimten**. In Adobe [!DNL Journey Optimizer], **Identiteiten** verbind consumenten over apparaten en kanalen, is het resultaat een identiteitsgrafiek. De verbonden identiteitsgrafiek wordt gebruikt om ervaringen te personaliseren die op interactie over al uw bedrijfs touchpoints worden gebaseerd. Leer meer over identiteiten en identiteit namespaces [&#x200B; op deze pagina &#x200B;](../../audience/get-started-identity.md).

   Bovendien vorm **supplementaire herkenningstekens** om het zelfde profiel toe te laten om veelvoudige reisinstanties in te gaan die op secundaire herkenningstekens zoals orde IDs of het boeken IDs worden gebaseerd. Leer over [&#x200B; supplementaire herkenningstekens &#x200B;](../../building-journeys/supplemental-identifier.md).

1. **creeer schema&#39;s** en laat hen voor profielen toe. Een schema is een set regels die de structuur en indeling van gegevens vertegenwoordigen en valideren. Op een hoog niveau, verstrekken de schema&#39;s een abstracte definitie van een echt-wereld voorwerp (zoals een persoon) en schetsen welke gegevens in elke instantie van dat voorwerp (zoals voornaam, achternaam, verjaardag, etc.) zouden moeten worden omvat.

   * Voor standaardreizen en campagnes: Gebruik [&#x200B; schema&#39;s XDM &#x200B;](../../data/get-started-schemas.md)
   * Voor Geordende campagnes: Creeer [&#x200B; relationele schema&#39;s &#x200B;](../../orchestrated/gs-schemas.md) om multi-entiteitsegmentatie toe te laten

1. **creeer datasets** en laat hen voor profielen toe. Een dataset is een opslag en beheersconstructie voor een inzameling van gegevens, typisch een lijst, die een schema (kolommen) en gebieden (rijen) bevat. Datasets bevatten ook metagegevens die verschillende aspecten van de gegevens beschrijven die ze opslaan. Zodra een dataset wordt gecreeerd, kunt u het aan een bestaand schema in kaart brengen en gegevens toevoegen in het. Leer meer over datasets [&#x200B; op deze pagina &#x200B;](../../data/get-started-datasets.md).

   Voor geavanceerde scenario&#39;s, bereidt **datasets voor runtime raadplegingen** voor om reisuitvoering met gegevens in real time van verslagdatasets te verrijken. Leer over [&#x200B; datasetraadpleging &#x200B;](../../building-journeys/dataset-lookup.md).

1. **vorm bronschakelaars**. Adobe Journey Optimizer staat toe dat gegevens uit externe bronnen worden opgenomen terwijl u de mogelijkheid krijgt om inkomende gegevens te structureren, te labelen en te verbeteren met behulp van de platformservices. U kunt gegevens invoeren uit verschillende bronnen, zoals Adobe-toepassingen, opslag in de cloud, databases en vele andere. Leer meer over de schakelaars van Source [&#x200B; op deze pagina &#x200B;](../get-started-sources.md).

1. **creeer testprofielen**. De profielen van de test worden vereist wanneer het gebruiken van de [&#x200B; testwijze &#x200B;](../../building-journeys/testing-the-journey.md) in een reis, en aan [&#x200B; voorproef en test uw berichten &#x200B;](../../content-management/preview-test.md) alvorens te verzenden. De stappen om testprofielen tot stand te brengen zijn gedetailleerd [&#x200B; op deze pagina &#x200B;](../../audience/creating-test-profiles.md).

1. **vorm gegevens verwerkte attributen** (facultatief). Maak afgeleide kenmerken van profielgegevens om segmentatie en personalisatie te vereenvoudigen. Berekende kenmerken berekenen automatisch complexe metingen zoals &quot;totale aankopen in de afgelopen 90 dagen&quot; of &quot;gemiddelde orderwaarde&quot;. Leer over [&#x200B; gegevens verwerkte attributen &#x200B;](../../audience/computed-attributes.md).

Daarnaast moet u **[!UICONTROL Data Sources]** , **[!UICONTROL Events]** en **[!UICONTROL Actions]** configureren om berichten tijdens reizen te kunnen verzenden. Leer meer [&#x200B; in deze sectie &#x200B;](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* De **configuratie van Source van 0&rbrace; Gegevens &lbrace;staat u toe om een verbinding aan een systeem te bepalen om extra informatie terug te winnen die in uw reizen zal worden gebruikt.** Leer meer over Gegevensbronnen [&#x200B; in deze sectie &#x200B;](../../datasource/about-data-sources.md).

* **Gebeurtenissen** staan u toe om uw reizen unitatically te teweegbrengen om berichten, in real time, naar het individu te verzenden dat in de reis stroomt. In de gebeurtenisconfiguratie, vormt u de gebeurtenissen die in de reizen worden verwacht. De data van binnenkomende gebeurtenissen worden genormaliseerd volgens het Adobe Experience Data Model (XDM). Gebeurtenissen komen van de Streaming Ingestie-API&#39;s voor geverifieerde en niet-geverifieerde gebeurtenissen (zoals Adobe Mobile SDK-gebeurtenissen). Leer meer over gebeurtenissen [&#x200B; in deze sectie &#x200B;](../../event/about-events.md).

* [!DNL Journey Optimizer] wordt geleverd met ingebouwde berichtmogelijkheden: u kunt uw berichten binnen een reis maken en uw inhoud ontwerpen. Als u een derdesysteem gebruikt om uw berichten, bijvoorbeeld Adobe Campaign te verzenden, creeer a **douaneactie**. Leer meer over acties [&#x200B; in deze sectie &#x200B;](../../action/action.md).

## Reisgegevens bewaken en analyseren

Zodra de reizen lopen, kunt u de gebeurtenissen van de reisstap in het meer van Gegevens vragen om prestaties te controleren, kwesties problemen op te lossen, en klantengedrag te analyseren. Gebruik SQL-query&#39;s om te analyseren:

* Invoer- en aflooppatronen van profielen
* Foutpercentages en redenen voor verwijderen
* Prestaties van exporttaken van het publiek lezen
* Eigen maatstaven voor handelingsprestaties
* Frames en knelpunten voor reisinstanties

Onderzoek klaar-aan-gebruiks [&#x200B; vraagvoorbeelden voor reisanalyse &#x200B;](../../reports/query-examples.md) om met gegevensanalyse en het oplossen van problemen begonnen te worden.

## Bijwerken

Houd up-to-date met de nieuwste Journey Optimizer-mogelijkheden en -verbeteringen:

* **[de Nota&#39;s van de Versie](../../rn/release-notes.md)**: De nieuwe eigenschappen van het overzicht, verhogingen, en moeilijke situaties die elke maand worden vrijgegeven
* **[Updates van de Documentatie](../../rn/documentation-updates.md)**: De recente veranderingen van het spoor in de documentatie met inbegrip van nieuwe pagina&#39;s en bijgewerkte inhoud
* **Berichten van het Product**: Laat berichten in uw [&#x200B; profiel van Adobe Experience Cloud &#x200B;](https://experience.adobe.com/preferences){target="_blank"} toe om alarm over te ontvangen:
   * Nieuwe productreleases en -functies
   * Onderhoudsvensters en systeemupdates
   * Belangrijke aankondigingen en wijzigingen

  Om berichten toe te laten, klik uw profielpictogram in het hoogste recht van Adobe Experience Cloud, ga naar **Voorkeur > Meldingen**, en vorm uw het berichtvoorkeur van Journey Optimizer.
