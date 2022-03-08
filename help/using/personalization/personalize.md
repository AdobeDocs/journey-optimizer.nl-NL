---
title: Inhoud personaliseren in Journey Optimizer
description: Ga aan de slag met personalisatie.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 11%

---

# Aan de slag met personalisatie{#add-personalization}

Discover [!DNL Adobe Journey Optimizer] personaliseringsmogelijkheden om uw berichten aan elke specifieke ontvanger aan te passen door de gegevens en de informatie te gebruiken u over hen hebt. Het kan hun voornaam zijn, belangen, waar ze wonen, wat ze hebben gekocht, en meer.

➡️ [Leer hoe u een bericht in deze video&#39;s kunt aanpassen](#video-perso)
➡️ [Gebruiksscenario&#39;s detecteren door personalisatie te gebruiken](personalization-use-case.md)

## Verpersoonlijkingsexpressies maken met behulp van een speciale syntaxis {#syntax}

[!DNL Journey Optimizer] gebruikt een **inline** eenvoudige verpersoonlijkingssyntaxis die op Handlebars wordt gebaseerd die u toestaat om uitdrukkingen tot stand te brengen met inhoud die door dubbele krullende steunen wordt ingesloten **{{}**. U kunt meerdere expressies zonder beperkingen toevoegen in dezelfde inhoud of hetzelfde veld. Meer informatie in [Personalisatiesyntaxis](personalization-syntax.md).

**Voorbeelden:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Bij het verwerken van het bericht (e-mail en push) vervangt Journey Optimizer de expressie door de gegevens in de database van het Experience Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` wordt &quot;Hello John Doe&quot;.

## Gebruik profielgegevens om uw berichten aan te passen {#data}

De verpersoonlijking is gebaseerd op de profielgegevens die door **Afzonderlijk XDM-profiel** schema gedefinieerd in Adobe Experience Platform. Meer informatie in [Adobe Experience Platform Data Model (XDM)-documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target=&quot;_blank&quot;}.

>[!CAUTION]
>De **Afzonderlijk XDM-profiel** schema is het enige schema dat u kunt gebruiken om inhoud in te personaliseren [!DNL Journey Optimizer].

## Verpersoonlijking toevoegen in verschillende contexten {#contexts}

[!DNL Journey Optimizer] kunt u de inhoud en de weergave van berichten op verschillende manieren aanpassen. Meer informatie over de context waarin u personalisatie kunt uitvoeren in [deze sectie](personalization-contexts.md).

## Werken met de expressie-editor {#editor}

[!DNL Journey Optimizer] biedt een expressie-editor waarin u alle gegevens kunt selecteren, rangschikken, aanpassen en valideren om een aangepaste personalisatie voor uw inhoud te maken.

Er zijn verschillende gereedschappen beschikbaar waarmee u uw inhoud voor personalisatie (helperfuncties, vooraf gedefinieerde expressies, bibliotheek met kenmerken die u begunstigen...) kunt maken.

Meer informatie over [!DNL Journey Optimizer] expression editor in [deze sectie](personalization-build-expressions.md)

## Instructievideo&#39;s{#video-perso}

Leer hoe u contextuele gebeurtenisinformatie van een journey kunt gebruiken om een bericht te personaliseren.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Leer hoe u contextuele gebeurtenisinformatie van een journey kunt gebruiken om een bericht te personaliseren.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
