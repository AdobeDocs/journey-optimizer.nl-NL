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
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 3%

---

# Aan de slag met personalisatie{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="Ervaringen personaliseren"
>abstract="Gebruiken **Adobe Journey Optimizer** om uw berichten aan elke specifieke ontvanger aan te passen door de gegevens en de informatie leveraging u over hen hebt. Het kan hun voornaam zijn, belangen, waar ze wonen, wat ze hebben gekocht, en meer."

Discover [!DNL Adobe Journey Optimizer] personaliseringsmogelijkheden om uw berichten aan elke specifieke ontvanger aan te passen door de gegevens en de informatie te gebruiken u over hen hebt. Het kan hun voornaam zijn, belangen, waar ze wonen, wat ze hebben gekocht, en meer.

➡️ [Leer hoe u een bericht in deze video&#39;s kunt aanpassen](#video-perso)
➡️ [Gebruiksscenario&#39;s detecteren door personalisatie te gebruiken](personalization-use-case.md)

## Verpersoonlijkingsexpressies maken met een speciale syntaxis {#syntax}

[!DNL Journey Optimizer] gebruikt een **inline** eenvoudige verpersoonlijkingssyntaxis die op Handlebars wordt gebaseerd die u toestaat om uitdrukkingen tot stand te brengen met inhoud die door dubbele krullende steunen wordt ingesloten **{{}}**. U kunt meerdere expressies zonder beperkingen toevoegen in dezelfde inhoud of hetzelfde veld. [Meer informatie over de personalisatiesyntaxis](personalization-syntax.md).

**Voorbeelden:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Bij het verwerken van het bericht (e-mail en push) vervangt Journey Optimizer de expressie door de gegevens in de database van het Experience Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` wordt &quot;Hello John Doe&quot;.

## Gebruik profielgegevens om uw berichten aan te passen {#data}

De personalisatie is gebaseerd op de profielgegevens die door **Afzonderlijk XDM-profiel** schema gedefinieerd in Adobe Experience Platform. Meer informatie in [Adobe Experience Platform Data Model (XDM)-documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target="_blank"}.

>[!CAUTION]
>De **Afzonderlijk XDM-profiel** schema is het enige schema dat u kunt gebruiken om inhoud in te personaliseren [!DNL Journey Optimizer].

Daarnaast kunt u ook gebruikmaken van **berekende kenmerken** om uw inhoud aan te passen. De berekende attributen zijn gebaseerd op profiel-Toegelaten Gegevensreeksen van de Gebeurtenis van de Ervaring die in Adobe Experience Platform worden opgenomen en dienen als samengevoegde gegevenspunten die binnen klantenprofielen worden opgeslagen die individuele gedragsgebeurtenissen samenvatten [Leer hoe u met berekende kenmerken werkt](../audience/computed-attributes.md)

## Werken met de verpersoonlijkingseditor {#editor}

[!DNL Journey Optimizer] biedt een verpersoonlijkingseditor waarin u alle gegevens kunt selecteren, rangschikken, aanpassen en valideren om een aangepaste verpersoonlijking voor uw inhoud te maken. Er zijn verschillende gereedschappen beschikbaar waarmee u uw personalisatie-inhoud kunt maken, zoals: felper-functies, vooraf gedefinieerde expressies-bibliotheek, kenmerken die de voorkeur geven en meer.

* [Leer hoe u met de verpersoonlijkingseditor werkt](personalization-build-expressions.md)
* [Leer waar u personalisatie kunt uitvoeren](personalization-contexts.md).

## Hoe kan ik-video&#39;s{#video-perso}

Leer hoe u contextuele gebeurtenisinformatie van een journey kunt gebruiken om een bericht te personaliseren.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Leer hoe u op profiel gebaseerde personalisatie aan een bericht toevoegt en hoe u het lidmaatschap van een publiek als voorwaarde aan een verpersoonlijkingsblok kunt gebruiken.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

