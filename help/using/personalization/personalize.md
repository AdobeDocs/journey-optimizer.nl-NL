---
title: Inhoud personaliseren in Journey Optimizer
description: Aan de slag met personalisatie
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: bd4a66d4d0c280c83b37241ccba53843b9442509
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 17%

---

# Aan de slag met personalisatie{#add-personalization}

Discover [!DNL Adobe Journey Optimizer] personaliseringsmogelijkheden om uw berichten aan elke specifieke ontvanger aan te passen door de gegevens en de informatie te gebruiken u over hen hebt. Het kan hun voornaam zijn, belangen, waar ze wonen, wat ze hebben gekocht, en meer.

➡️ [Leer hoe u een bericht in deze video&#39;s kunt aanpassen](#video-perso)

[!DNL Journey Optimizer] gebruikt een **inline** eenvoudige verpersoonlijkingssyntaxis die op Handlebars wordt gebaseerd die u toestaat om uitdrukkingen tot stand te brengen met inhoud die door dubbele krullende steunen wordt ingesloten **{{}**. U kunt meerdere expressies zonder beperkingen toevoegen in dezelfde inhoud of hetzelfde veld. Meer informatie in [Personalisatiesyntaxis](personalization-syntax.md).

De verpersoonlijking is gebaseerd op de profielgegevens die door **Afzonderlijk XDM-profiel** schema gedefinieerd in Adobe Experience Platform. Meer informatie in [Adobe Experience Platform Data Model (XDM)-documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target=&quot;_blank&quot;}.

>[!CAUTION]
>De **Afzonderlijk XDM-profiel** schema is het enige schema dat u kunt gebruiken om inhoud in te personaliseren [!DNL Journey Optimizer].

**Voorbeelden:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Bij het verwerken van het bericht (e-mail en push) vervangt Journey Optimizer de expressie door de gegevens in de database van het Experience Cloud Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` wordt &quot;Hello John Doe&quot;.

## Instructievideo&#39;s{#video-perso}

Leer hoe u contextuele gebeurtenisinformatie van een journey kunt gebruiken om een bericht te personaliseren.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Leer hoe u contextuele gebeurtenisinformatie van een journey kunt gebruiken om een bericht te personaliseren.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
