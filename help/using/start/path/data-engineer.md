---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer Get Started for Data Engineer
description: Als gegevensengineer leert u meer hoe u met Journey Optimizer kunt werken
feature: Get Started
role: Developer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: ed3246d0bd552fee9c4df01babe18a5c1acd3b5f
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 1%

---

# Aan de slag voor Data Engineer {#data-engineer}

Als a **Architect van Gegevens** of **Ingenieur van Gegevens**, plaatst u en handhaaft de gegevens van het klantenprofiel en andere gegevensbronnen die de ervaringen aandrijven die door [!DNL Journey Optimizer] worden georkestreerd. Dit omvat het integreren van al uw klant en bedrijfsgegevens-of van Web, CRM, of off-line bron-in een verenigde 360 graadmening van de klant. U modelleert de gegevens van het klantenprofiel en bedrijfsgegevens in schema&#39;s, vormt bronschakelaars voor het opnemen van gegevens, en verzekert gegevensstromen regelmatig om klanteninzichten en overeenkomst in real time toe te laten. U kunt met [!DNL Adobe Journey Optimizer] beginnen te werken zodra de [ Beheerder van het Systeem ](administrator.md) u toegang verleende en uw milieu voorbereidde.

>[!NOTE]
>
>Leer meer over **gegevensopname** in [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html){target="_blank"}.

## Essentiële stappen voor gegevensconfiguratie

Voer de volgende stappen uit om de gegevensbasis voor Journey Optimizer in te stellen:

1. **creeer identiteitsnaamruimten**. In Adobe [!DNL Journey Optimizer], **Identiteiten** verbind consumenten over apparaten en kanalen, is het resultaat een identiteitsgrafiek. De verbonden identiteitsgrafiek wordt gebruikt om ervaringen te personaliseren die op interactie over al uw bedrijfs touchpoints worden gebaseerd. Leer meer over identiteiten en identiteit namespaces [ op deze pagina ](../../audience/get-started-identity.md).

   Bovendien vorm **supplementaire herkenningstekens** om het zelfde profiel toe te laten om veelvoudige reisinstanties in te gaan die op secundaire herkenningstekens zoals orde IDs of het boeken IDs worden gebaseerd. Leer over [ supplementaire herkenningstekens ](../../building-journeys/supplemental-identifier.md).

1. **creeer schema&#39;s** en laat hen voor profielen toe. Een schema is een set regels die de structuur en indeling van gegevens vertegenwoordigen en valideren. Op een hoog niveau, verstrekken de schema&#39;s een abstracte definitie van een echt-wereld voorwerp (zoals een persoon) en schetsen welke gegevens in elke instantie van dat voorwerp (zoals voornaam, achternaam, verjaardag, etc.) zouden moeten worden omvat.

   * Voor standaardreizen en campagnes: Gebruik [ schema&#39;s XDM ](../../data/get-started-schemas.md)
   * Voor Geordende campagnes: Creeer [ relationele schema&#39;s ](../../orchestrated/gs-schemas.md) om multi-entiteitsegmentatie toe te laten

1. **creeer datasets** en laat hen voor profielen toe. Een dataset is een opslag en beheersconstructie voor een inzameling van gegevens, typisch een lijst, die een schema (kolommen) en gebieden (rijen) bevat. Datasets bevatten ook metagegevens die verschillende aspecten van de gegevens beschrijven die ze opslaan. Zodra een dataset wordt gecreeerd, kunt u het aan een bestaand schema in kaart brengen en gegevens toevoegen in het. Leer meer over datasets [ op deze pagina ](../../data/get-started-datasets.md).

   Voor geavanceerde scenario&#39;s, bereidt **datasets voor runtime raadplegingen** voor om reisuitvoering met gegevens in real time van verslagdatasets te verrijken. Leer over [ datasetraadpleging ](../../building-journeys/dataset-lookup.md).

1. **vorm bronschakelaars**. Adobe Journey Optimizer staat toe dat gegevens uit externe bronnen worden opgenomen terwijl u de mogelijkheid krijgt om inkomende gegevens te structureren, te labelen en te verbeteren met behulp van de platformservices. U kunt gegevens invoeren uit verschillende bronnen, zoals Adobe-toepassingen, opslag in de cloud, databases en vele andere. Leer meer over de schakelaars van Source [ op deze pagina ](../get-started-sources.md).

1. **creeer testprofielen**. De profielen van de test worden vereist wanneer het gebruiken van de [ testwijze ](../../building-journeys/testing-the-journey.md) in een reis, en aan [ voorproef en test uw berichten ](../../content-management/preview-test.md) alvorens te verzenden. De stappen om testprofielen tot stand te brengen zijn gedetailleerd [ op deze pagina ](../../audience/creating-test-profiles.md).

1. **vorm gegevens verwerkte attributen** (facultatief). Maak afgeleide kenmerken van profielgegevens om segmentatie en personalisatie te vereenvoudigen. Berekende kenmerken berekenen automatisch complexe metingen zoals &quot;totale aankopen in de afgelopen 90 dagen&quot; of &quot;gemiddelde orderwaarde&quot;. Leer over [ gegevens verwerkte attributen ](../../audience/computed-attributes.md).

Daarnaast moet u **[!UICONTROL Data Sources]** , **[!UICONTROL Events]** en **[!UICONTROL Actions]** configureren om berichten tijdens reizen te kunnen verzenden. Leer meer [ in deze sectie ](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* De **configuratie van Source van 0} Gegevens {staat u toe om een verbinding aan een systeem te bepalen om extra informatie terug te winnen die in uw reizen zal worden gebruikt.** Leer meer over Gegevensbronnen [ in deze sectie ](../../datasource/about-data-sources.md).

* **Gebeurtenissen** staan u toe om uw reizen unitatically te teweegbrengen om berichten, in real time, naar het individu te verzenden dat in de reis stroomt. In de gebeurtenisconfiguratie, vormt u de gebeurtenissen die in de reizen worden verwacht. De data van binnenkomende gebeurtenissen worden genormaliseerd volgens het Adobe Experience Data Model (XDM). Gebeurtenissen komen van de Streaming Ingestie-API&#39;s voor geverifieerde en niet-geverifieerde gebeurtenissen (zoals Adobe Mobile SDK-gebeurtenissen). Leer meer over gebeurtenissen [ in deze sectie ](../../event/about-events.md).

* [!DNL Journey Optimizer] wordt geleverd met ingebouwde berichtmogelijkheden: u kunt uw berichten binnen een reis maken en uw inhoud ontwerpen. Als u een derdesysteem gebruikt om uw berichten, bijvoorbeeld Adobe Campaign te verzenden, creeer a **douaneactie**. Leer meer over acties [ in deze sectie ](../../action/action.md).

## Reisgegevens bewaken en analyseren

Zodra de reizen lopen, kunt u de gebeurtenissen van de reisstap in het meer van Gegevens vragen om prestaties te controleren, kwesties problemen op te lossen, en klantengedrag te analyseren. Gebruik SQL-query&#39;s om te analyseren:

* Invoer- en aflooppatronen van profielen
* Foutpercentages en redenen voor verwijderen
* Prestaties van exporttaken van het publiek lezen
* Eigen maatstaven voor handelingsprestaties
* Frames en knelpunten voor reisinstanties

Onderzoek klaar-aan-gebruiks [ vraagvoorbeelden voor reisanalyse ](../../reports/query-examples.md) om met gegevensanalyse en het oplossen van problemen begonnen te worden.

## Bijwerken

Houd up-to-date met de nieuwste Journey Optimizer-mogelijkheden en -verbeteringen:

* **[de Nota&#39;s van de Versie](../../rn/release-notes.md)**: De nieuwe eigenschappen van het overzicht, verhogingen, en moeilijke situaties die elke maand worden vrijgegeven
* **[Updates van de Documentatie](../../rn/documentation-updates.md)**: De recente veranderingen van het spoor in de documentatie met inbegrip van nieuwe pagina&#39;s en bijgewerkte inhoud
* **[Berichten van het Product](../../rn/releases.md#staying-informed)**: Leer hoe te om aan e-mail en in-productalarm voor updates van Journey Optimizer, met inbegrip van nieuwe eigenschappen, onderhoudsvensters, en belangrijke systeemveranderingen in te tekenen
