---
solution: Journey Optimizer
product: journey optimizer
title: Inhoud personaliseren in Journey Optimizer
description: Ga aan de slag met personalisatie.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
keywords: expressie, editor, start, personalisatie
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: e19a85d05fcb7727c3086f16e2e4f066a5ecd55c
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 3%

---

# Aan de slag met personalisatie{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="Ervaringen personaliseren"
>abstract="Het gebruik **Adobe Journey Optimizer** om uw berichten aan elke specifieke ontvanger aan te passen door de gegevens en de informatie leveraging u over hen hebt. Het kan hun voornaam zijn, belangen, waar ze wonen, wat ze hebben gekocht, en meer."

Met de aanpassingsmogelijkheden van [!DNL Adobe Journey Optimizer] kunt u uw berichten aanpassen aan elke specifieke ontvanger door de gegevens en informatie waarover u beschikt, te benutten. Het kan hun voornaam zijn, belangen, waar ze wonen, wat ze hebben gekocht, en meer.

## Hoe verpersoonlijking werkt

Gebruikend de **verpersoonlijkingsredacteur**, kunt u selecteren, rangschikken, aanpassen en bevestigen alle gegevens om een aangepaste verpersoonlijking voor uw inhoud tot stand te brengen, en hefboomwerking diverse hulpmiddelen zoals helperfuncties of vooraf bepaalde uitdrukkingen om berichten effectief aan te passen.

Journey Optimizer past een inline verpersoonlijkingssyntaxis toe die op Handlebars wordt gebaseerd die u toestaat om uitdrukkingen met inhoud tot stand te brengen die door dubbele krullende steunen **{{}}{{}}** wordt ingesloten.

Bij het verwerken van het bericht vervangt Journey Optimizer de expressie door de gegevens in de Experience Platform-gegevensset. `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` wordt bijvoorbeeld dynamisch `Hello John Doe` .

Met deze syntaxis kunt u berichten in meerdere velden personaliseren, zoals onderwerpregel e-mail, berichttekst, pushberichten of URL&#39;s.

## Gegevens gebruikt voor personalisatie

Personalization is gebaseerd op de profielgegevens die door het **worden geleid XDM Individuele die schema van het Profiel** in Adobe Experience Platform wordt bepaald. Het **schema van het Profiel van 0&rbrace; XDM Individuele is het enige schema u kunt gebruiken om inhoud in [!DNL Journey Optimizer] te personaliseren.** Leer meer in [ het Model van Gegevens van Adobe Experience Platform (XDM) documentatie ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"}.

U kunt hefboomwerking **gegevens verwerkte attributen** ook gebruiken om uw inhoud te personaliseren. Met berekende kenmerken kunt u afzonderlijke gedragsgebeurtenissen samenvatten in berekende profielkenmerken die beschikbaar zijn op Adobe Experience Platform. [ leer hoe te met gegevens verwerkte attributen ](../audience/computed-attributes.md) werken

Bovendien kunt u met [!DNL Journey Optimizer] gegevens van Adobe Experience Platform in de personalisatie-editor gebruiken om uw inhoud aan te passen. Om dit te doen, moeten de datasets nodig voor raadplegingsverpersoonlijking eerst door een API vraag worden toegelaten. Zodra u klaar bent, kunt u hun gegevens gebruiken om uw inhoud aan te passen aan Journey Optimizer. THis-functie is momenteel beschikbaar in bèta. [Meer informatie](../personalization/lookup-aep-data.md)

## Leer en experimenteer met personalisatie {#playground}

**[!DNL Adobe Journey Optimizer]** bevat een interactief programma dat u helpt te leren werken en te experimenteren met mogelijkheden voor personalisatie.

Deze playground verstrekt een gesimuleerd milieu om verpersoonlijkingscode te schrijven en te testen gebruikend steekproefgegevens zonder levende datasets te vereisen. U kunt vooraf gedefinieerde codevoorbeelden gebruiken, dummy-profielladingen bewerken en de uitvoer van uw personalisatiecode in real-time voorvertonen.

![ verpersoonlijkings playground ](assets/playground.png)

➡️ [ toegang tot de verpersoonlijkings playground ](https://experienceleague.adobe.com/nl/apps/journey-optimizer/ajo-personalization){target="_blank"}

## Laten we dieper duiken

Nu u in **[!DNL Journey Optimizer]** inzicht hebt in personalisatie, is het tijd om dieper in deze documentatiegedeelten te duiken om met de eigenschap te beginnen werken.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="personalization-build-expressions.md">
<img alt="personalisatie toevoegen" src="assets/do-not-localize/add.png">
</a>
<div>
<a href="personalization-build-expressions.md"><strong> voeg verpersoonlijking </strong></a> toe
</div>
<p>
</td>
<td>
<a href="../personalization/personalization-syntax.md">
<img alt="Lood" src="assets/do-not-localize/syntax.png">
</a>
<div><a href="../personalization/personalization-syntax.md"><strong> syntaxis van Personalization </strong>
</div>
<p>
</td>
<td>
<a href="../personalization/functions/functions.md">
<img alt="Onfrequent" src="assets/do-not-localize/functions.png">
</a>
<div>
<a href="../personalization/functions/functions.md"><strong> de functielijst van de Helper </strong></a>
</div>
<p></td>
<td>
<a href="../personalization/personalization-use-case.md">
<img alt="Onfrequent" src="assets/do-not-localize/uc.png">
</a>
<div>
<a href="../personalization/personalization-use-case.md"><strong> Personalization gebruiksgevallen </strong></a>
</div>
<p></td>
</tr></table>

## Hoe kan ik-video&#39;s{#video-perso}

Leer hoe u contextuele gebeurtenisinformatie van een journey kunt gebruiken om een bericht te personaliseren.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Leer hoe u op profiel gebaseerde personalisatie aan een bericht toevoegt en hoe u het lidmaatschap van een publiek als voorwaarde aan een verpersoonlijkingsblok kunt gebruiken.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

