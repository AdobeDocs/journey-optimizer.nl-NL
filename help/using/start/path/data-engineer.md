---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer Get Started for Data Engineer
description: Als gegevensengineer leert u meer hoe u met Journey Optimizer kunt werken
feature: Get Started
role: Data Engineer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 1a2c6e97fcd30245cff1bf08fd5771ce8bc84ddc
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 2%

---

# Aan de slag voor Data Engineer {#data-engineer}

Als **Ingenieur van de Gegevens van Adobe Journey Optimizer**, bereidt en handhaaft de gegevens van het klantenprofiel voor om de ervaringen aan te drijven die door [!DNL Journey Optimizer] worden georganiseerd, modelklant en bedrijfsgegevens in schema&#39;s en vormt bronschakelaars voor het opnemen van gegevens. U kunt met [!DNL Adobe Journey Optimizer] beginnen te werken zodra de [&#x200B; Beheerder van het Systeem &#x200B;](administrator.md) u toegang verleende en uw milieu voorbereidde.


Leer hoe te **gegevens identificeren en schema en dataset** tot stand brengen om uw gegevens in Adobe Experience Platform op deze pagina te krijgen.

>[!NOTE]
>
>Leer meer over **gegevensopname** in [&#x200B; documentatie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=nl-NL){target="_blank"}.

De stappen om een identiteitsnamespace en een dataset tot stand te brengen die voor profielen wordt toegelaten, en de testprofielen zijn gedetailleerd in de hieronder secties:

1. **creeer een identiteit namespace**. In Adobe [!DNL Journey Optimizer], **Identiteiten** verbind consumenten over apparaten en kanalen, is het resultaat een identiteitsgrafiek. De verbonden identiteitsgrafiek wordt gebruikt om ervaringen te personaliseren die op interactie over al uw bedrijfs touchpoints worden gebaseerd.  Leer meer over identiteiten en identiteit namespaces [&#x200B; op deze pagina &#x200B;](../../audience/get-started-identity.md).

1. **creeer een schema** en laat het voor profielen toe. Een schema is een set regels die de structuur en indeling van gegevens vertegenwoordigen en valideren. Op een hoog niveau, verstrekken de schema&#39;s een abstracte definitie van een echt-wereld voorwerp (zoals een persoon) en schetsen welke gegevens in elke instantie van dat voorwerp (zoals voornaam, achternaam, verjaardag, etc.) zouden moeten worden omvat.  Leer meer over schema&#39;s [&#x200B; op deze pagina &#x200B;](../../data/get-started-schemas.md).

1. **creeer datasets** en laat het voor profielen toe. Een dataset is een opslag en beheersconstructie voor een inzameling van gegevens, typisch een lijst, die een schema (kolommen) en gebieden (rijen) bevat. Datasets bevatten ook metagegevens die verschillende aspecten van de gegevens beschrijven die ze opslaan. Zodra een dataset wordt gecreeerd, kunt u het aan een bestaand schema in kaart brengen en gegevens toevoegen in het. Leer meer over datasets [&#x200B; op deze pagina &#x200B;](../../data/get-started-datasets.md).

1. **vorm bronschakelaars**. Met Adobe Reis Optimzer kunt u gegevens uit externe bronnen innemen en binnenkomende gegevens structureren, labelen en verbeteren met behulp van de platformservices. U kunt gegevens invoeren uit verschillende bronnen, zoals Adobe-toepassingen, opslag in de cloud, databases en vele andere. Leer meer over de schakelaars van Source [&#x200B; op deze pagina &#x200B;](../get-started-sources.md).

1. **creeer testprofielen**. De profielen van de test worden vereist wanneer het gebruiken van de [&#x200B; testwijze &#x200B;](../../building-journeys/testing-the-journey.md) in een reis, en aan [&#x200B; voorproef en test uw berichten &#x200B;](../../content-management/preview-test.md) alvorens te verzenden. De stappen om testprofielen tot stand te brengen zijn gedetailleerd [&#x200B; op deze pagina &#x200B;](../../audience/creating-test-profiles.md).


Daarnaast moet u **[!UICONTROL Data Sources]** , **[!UICONTROL Events]** en **[!UICONTROL Actions]** configureren om berichten tijdens reizen te kunnen verzenden. Leer meer [&#x200B; in deze sectie &#x200B;](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* De **configuratie van Source van 0&rbrace; Gegevens &lbrace;staat u toe om een verbinding aan een systeem te bepalen om extra informatie terug te winnen die in uw reizen zal worden gebruikt.** Leer meer over Gegevensbronnen [&#x200B; in deze sectie &#x200B;](../../datasource/about-data-sources.md).

* **Gebeurtenissen** staan u toe om uw reizen unitatically te teweegbrengen om berichten, in real time, naar het individu te verzenden dat in de reis stroomt. In de gebeurtenisconfiguratie, vormt u de gebeurtenissen die in de reizen worden verwacht. De data van binnenkomende gebeurtenissen worden genormaliseerd volgens het Adobe Experience Data Model (XDM). Gebeurtenissen komen van de Streaming Ingestie-API&#39;s voor geverifieerde en niet-geverifieerde gebeurtenissen (zoals Adobe Mobile SDK-gebeurtenissen). Leer meer over gebeurtenissen [&#x200B; in deze sectie &#x200B;](../../event/about-events.md).

* [!DNL Journey Optimizer] wordt geleverd met ingebouwde berichtmogelijkheden: u kunt uw berichten binnen een reis maken en uw inhoud ontwerpen. Als u een derdesysteem gebruikt om uw berichten, bijvoorbeeld Adobe Campaign te verzenden, creeer a **douaneactie**. Leer meer over acties in dit [&#x200B; in deze sectie &#x200B;](../../action/action.md).
