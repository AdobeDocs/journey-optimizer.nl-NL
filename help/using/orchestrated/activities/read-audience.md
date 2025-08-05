---
solution: Journey Optimizer
product: journey optimizer
title: De publieksactiviteit Lezen gebruiken
description: Leer hoe u de Lees-publieksactiviteit gebruikt in een geordende campagne
exl-id: ef8eba57-cd33-4746-8eb4-5214ef9cbe2f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---


# Doelgroep lezen {#read-audience}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_read_audience"
>title="Activiteit voor publiek opbouwen"
>abstract="De **gelezen publiek** activiteit staat u toe om het publiek te selecteren dat de Geordende campagne zal ingaan. Dit publiek kan een bestaand Adobe Experience Platform-publiek zijn of een publiek dat uit een CSV-bestand is opgehaald. Wanneer het verzenden van berichten in de context van een Geordende campagne, wordt het berichtpubliek niet bepaald in de kanaalactiviteit, maar in a **gelezen publiek** of a **bouwt publiek** activiteit."

Met de **[!UICONTROL Read audience]** -activiteit kunt u een bestaand publiek ophalen (dat eerder is opgeslagen of geïmporteerd) en dit opnieuw gebruiken in een geordende campagne. Deze activiteit is vooral nuttig voor het richten van een vooraf bepaalde reeks profielen zonder de behoefte om een nieuw segmenteringsproces uit te voeren.

Wanneer het publiek is geladen, kunt u dit optioneel verfijnen door een uniek identiteitsveld te selecteren en het publiek te verrijken met extra profielkenmerken voor doelgerichte, personalisatie- of rapportagedoeleinden.

## De activiteit voor het lezen van het publiek configureren {#read-audience-configuration}

Voer de volgende stappen uit om de **[!UICONTROL Read audience]** -activiteit te configureren:

1. Voordat u de **[!UICONTROL Read audience]** -activiteit toevoegt, moet u eerst een **[!UICONTROL Merge policy]** selecteren in de campagne-instellingen.

   ![](../assets/read-audience-6.png)

1. Voeg een **[!UICONTROL Read audience]** activiteit aan uw Geordende campagne toe.

   ![](../assets/read-audience-1.png)

1. Voer een **[!UICONTROL Label]** in voor uw activiteit. Dit label wordt gebruikt als de naam van uw publiek.

1. Klik ![ pictogram van het omslagonderzoek ](../assets/do-not-localize/folder-search.svg) om het publiek te selecteren u wenst om voor uw Geordende campagne te richten.

   ![](../assets/read-audience-2.png)

1. Kies een **[!UICONTROL Entity&#x200B;]** optie in de doeldimensie van uw campagne. Deze instelling definieert de doelentiteit en het kenmerk dat wordt gebruikt om het publiek te combineren met de doeldimensie.

   ➡️ [ volg de stappen in deze pagina worden gedetailleerd om uw Campagne te creëren richtend afmeting ](../target-dimension.md)

   ![](../assets/read-audience-3.png)

1. Selecteer [!UICONTROL Add attribute] om het geselecteerde publiek te verrijken met extra gegevens. Met deze stap kunt u profielkenmerken toevoegen aan het publiek. Dit resulteert in een lijst met ontvangers die met deze kenmerken zijn verbeterd.

1. Kies **[!UICONTROL Attributes]** u aan uw publiek wilt toevoegen. De attributenkiezer toont gebieden van het **Schema van het Profiel van de Unie**:

   * Voor op CSV-Gebaseerd publiek, omvat dit zowel **attributen van het Profiel** en douane publiek-vlakke attributen. Deze kenmerken vindt u in het volgende schemapad:

     `<audienceid> > _ajobatchjourneystage > audienceEnrichment > CustomerAudienceUpload > <audienceid>`

   * Voor standaardAEP publiek, slechts zijn de **attributen van het Profiel** beschikbaar, aangezien zij ingebedde publiek-specifieke gebieden niet dragen.

   >[!NOTE]
   >
   > Terwijl sommige attributen in de plukker kunnen verschijnen, hangt hun beschikbaarheid bij runtime af van of de publieksgegevens met succes zijn in overeenstemming gebracht en met het **Profiel van Adobe Experience Platform** samengevoegd.

   ![](../assets/read-audience-4.png)

Wanneer een publiek is gemaakt, is het alleen-lezen en kan het niet meer worden bewerkt. Deze kan alleen worden gebruikt nadat het ontwerpproces volledig is voltooid.

## Voorbeeld

In het onderstaande voorbeeld wordt de **[!UICONTROL Read audience]** -activiteit gebruikt om een eerder gemaakt en opgeslagen publiek op te halen van profielen die zijn geabonneerd op de nieuwsbrief. Het publiek wordt dan verrijkt met het **1} attribuut van het Loyalty lidmaatschap {om het richten van gebruikers toe te laten die lid van het loyaliteitsprogramma zijn.**

![](../assets/read-audience-5.png)
