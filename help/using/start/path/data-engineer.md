---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer Get Started for Data Engineer
description: Als gegevensengineer leert u meer hoe u met Journey Optimizer kunt werken
feature: Get Started
role: Data Engineer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: c2f32533027e374a1df26943e7c5acd4e1d13869
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 2%

---

# Aan de slag voor Data Engineer {#data-engineer}

Als **Ingenieur van de Gegevens van Adobe Journey Optimizer**, bereidt en handhaaft de gegevens van het klantenprofiel voor om de ervaringen aan te drijven die door [!DNL Journey Optimizer] worden georganiseerd, modelklant en bedrijfsgegevens in schema&#39;s en vormt bronschakelaars voor het opnemen van gegevens. U kunt met [!DNL Adobe Journey Optimizer] beginnen te werken zodra de [ Beheerder van het Systeem ](administrator.md) u toegang verleende en uw milieu voorbereidde.


Leer hoe te **gegevens identificeren en schema en dataset** tot stand brengen om uw gegevens in Adobe Experience Platform op deze pagina te krijgen.

>[!NOTE]
>
>Leer meer over **gegevensopname** in [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=nl-NL){target="_blank"} .

De stappen om een identiteitsnamespace en een dataset tot stand te brengen die voor profielen wordt toegelaten, en de testprofielen zijn gedetailleerd in de hieronder secties:

1. **creeer een identiteit namespace**. In Adobe [!DNL Journey Optimizer], **Identiteiten** verbind consumenten over apparaten en kanalen, is het resultaat een identiteitsgrafiek. De verbonden identiteitsgrafiek wordt gebruikt om ervaringen te personaliseren die op interactie over al uw bedrijfs touchpoints worden gebaseerd.  Leer meer over identiteiten en identiteit namespaces [ op deze pagina ](../../audience/get-started-identity.md).

1. **creeer een schema** en laat het voor profielen toe. Een schema is een set regels die de structuur en indeling van gegevens vertegenwoordigen en valideren. Op een hoog niveau, verstrekken de schema&#39;s een abstracte definitie van een real-world voorwerp (zoals een persoon) en schetsen welke gegevens in elke instantie van dat voorwerp (zoals voornaam, achternaam, verjaardag, etc.) zouden moeten worden omvat.  Leer meer over schema&#39;s [ op deze pagina ](../../data/get-started-schemas.md).

1. **creeer datasets** en laat het voor profielen toe. Een dataset is een opslag en beheersconstructie voor een inzameling van gegevens, typisch een lijst, die een schema (kolommen) en gebieden (rijen) bevat. Datasets bevatten ook metagegevens die verschillende aspecten van de gegevens beschrijven die ze opslaan. Zodra een dataset wordt gecreeerd, kunt u het aan een bestaand schema in kaart brengen en gegevens toevoegen in het. Leer meer over datasets [ op deze pagina ](../../data/get-started-datasets.md).

1. **vorm bronschakelaars**. Met Adobe Reis Optimzer kunt u gegevens uit externe bronnen innemen en binnenkomende gegevens structureren, labelen en verbeteren met behulp van de platformservices. U kunt gegevens invoeren uit verschillende bronnen, zoals Adobe-toepassingen, opslag in de cloud, databases en vele andere. Leer meer over de schakelaars van Source [ op deze pagina ](../get-started-sources.md).

1. **creeer testprofielen**. De profielen van de test worden vereist wanneer het gebruiken van de [ testwijze ](../../building-journeys/testing-the-journey.md) in een reis, en aan [ voorproef en test uw berichten ](../../content-management/preview-test.md) alvorens te verzenden. De stappen om testprofielen tot stand te brengen zijn gedetailleerd [ op deze pagina ](../../audience/creating-test-profiles.md).


Daarnaast moet u **[!UICONTROL Data Sources]** , **[!UICONTROL Events]** en **[!UICONTROL Actions]** configureren om berichten tijdens reizen te kunnen verzenden. Leer meer [ in deze sectie ](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* De **configuratie van Source van 0&rbrace; Gegevens &lbrace;staat u toe om een verbinding aan een systeem te bepalen om extra informatie terug te winnen die in uw reizen zal worden gebruikt.** Leer meer over Gegevensbronnen [ in deze sectie ](../../datasource/about-data-sources.md).

* **Gebeurtenissen** staan u toe om uw reizen unitatically te teweegbrengen om berichten, in real time, naar het individu te verzenden dat in de reis stroomt. In de gebeurtenisconfiguratie, vormt u de gebeurtenissen die in de reizen worden verwacht. De data van binnenkomende gebeurtenissen worden genormaliseerd volgens het Adobe Experience Data Model (XDM). Gebeurtenissen komen van de Streaming Ingestie-API&#39;s voor geverifieerde en niet-geverifieerde gebeurtenissen (zoals Adobe Mobile SDK-gebeurtenissen). Leer meer over gebeurtenissen [ in deze sectie ](../../event/about-events.md).

* [!DNL Journey Optimizer] wordt geleverd met ingebouwde berichtmogelijkheden: u kunt uw berichten binnen een reis maken en uw inhoud ontwerpen. Als u een derdesysteem gebruikt om uw berichten, bijvoorbeeld Adobe Campaign te verzenden, creeer a **douaneactie**. Leer meer over acties in dit [ in deze sectie ](../../action/action.md).
