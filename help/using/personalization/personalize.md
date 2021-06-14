---
title: Inhoud personaliseren in Journey Optimizer
description: Aan de slag met personalisatie
feature: Personalisatie
topic: Personalisatie
role: Data Engineer
level: Beginner
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 5%

---

# Aan de slag met personalisatie{#add-personalization}

![](../assets/do-not-localize/badge.png)

Ontdek de mogelijkheden van de Personalisatie van de Reis Optimaliseren om uw berichten aan elke specifieke ontvanger aan te passen door de gegevens en de informatie te gebruiken u over hem/haar hebt. Het kan zijn voornaam zijn, zijn belangen, waar hij woont, wat hij gekocht heeft, en meer.

Journey Optimizer gebruikt een **inline** eenvoudige verpersoonlijkingssyntaxis gebaseerd op Handlebars die u toestaat om uitdrukkingen met inhoud tot stand te brengen die door dubbele krullende steunen **{{}** wordt ingesloten. U kunt meerdere expressies zonder beperkingen toevoegen in dezelfde inhoud of hetzelfde veld. Meer informatie vindt u in [Persoonlijkheidssyntaxis](personalization-syntax.md).

De verpersoonlijking is gebaseerd op de profielgegevens die door **XDM Individual Profile** schema in Adobe Experience Platform wordt bepaald. Raadpleeg [Adobe Experience Platform Data Model (XDM)-documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) voor meer informatie.

>[!CAUTION]
>Het **XDM Individual Profile** schema is het enige schema u kunt gebruiken om inhoud in Journey Optimizer te personaliseren.

**Voorbeelden:**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

Bij het verwerken van het bericht (e-mail en push) vervangt Journey Optimizer de expressie door de gegevens in de database van het Experience Cloud Platform.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
