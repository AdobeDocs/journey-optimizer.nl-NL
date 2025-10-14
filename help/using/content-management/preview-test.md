---
title: Inhoud voorvertonen en testen
description: Leer hoe u uw inhoud kunt voorvertonen en testen.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: aa28d13b2ad874e4dc61510bfdc250415e8e8be1
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# Inhoud voorvertonen en testen {#preview-test}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="Controleren hoe uw inhoud wordt gerenderd"
>abstract="Nadat de inhoud is gedefinieerd, kunt u testprofielen gebruiken om deze voor te vertonen en te controleren of de rendering correct is volgens het kanaal dat u gebruikt."

>[!CONTEXTUALHELP]
>id="ajo_preview_simulate"
>title="Controleren hoe uw inhoud wordt gerenderd"
>abstract="Nadat u de inhoud hebt gedefinieerd, kunt u deze voorvertonen en controleren of de rendering correct is volgens het kanaal dat u gebruikt."

Nadat u de inhoud hebt gedefinieerd, kunt u de inhoud ervan voorvertonen voordat u het bericht verzendt. Dit is een cruciale stap om ervoor te zorgen dat deze accuraat is, maar ook vrij van fouten in zowel de inhoud als de personalisatie-instellingen.

U kunt ook testleveringen van uw e-mailberichten naar specifieke ontvangers of abonnees verzenden voor tests en validatie, en hun rendering controleren bij populaire desktops, mobiele en webclients.

Al deze handelingen kunnen worden uitgevoerd met de knop **[!UICONTROL Simulate Content]** , die toegankelijk is vanuit het scherm Inhoud bewerken van uw bericht of vanuit de ontwerpers van de e-mail en het web voor de e-mail en webkanalen.

![](../email/assets/email-preview-button.png)

## Testen met behulp van testprofielen, gegevens of gegevens uit de voorbeeldinvoer {#methods}

Journey Optimizer biedt twee mogelijkheden om uw inhoud te testen:

* **het Testen inhoud gebruikend de gegevens van testprofielen**

  U kunt testprofielen gebruiken om een voorvertoning van uw inhoud weer te geven, e-mailproefdrukken te verzenden en het renderen van e-mail te controleren. Als u persoonlijke velden hebt toegevoegd, kunt u controleren hoe deze worden weergegeven met de gegevens van het testprofiel. Raadpleeg de volgende secties voor meer informatie:

  ➡️ [&#x200B; Uitgezochte testprofielen &#x200B;](test-profiles.md)
➡️ [&#x200B; Voorproef gebruikend testprofielen &#x200B;](preview.md)
➡️ [&#x200B; verzend e-mailproef &#x200B;](proofs.md)
➡️ [&#x200B; e-mailteruggave van de Controle &#x200B;](rendering.md)
➡️ [&#x200B; Voorproef &amp; proef uw e-mail (video) &#x200B;](#video-preview)

* **het Testen inhoudsvariaties gebruikend de gegevens van de steekproefinput**

  Met [!DNL Journey optimizer] kunt u proefdrukken voor verschillende variaties van uw inhoud weergeven en verzenden met voorbeeldinvoergegevens die vanuit een CSV-/JSON-bestand zijn geüpload of handmatig zijn toegevoegd.

  Alle profielkenmerken die in de inhoud worden gebruikt voor personalisatie worden automatisch gedetecteerd door het systeem en kunnen worden gebruikt voor uw tests om meerdere varianten te maken.

  ➡️ [&#x200B; simuleer inhoudsvariaties &#x200B;](../test-approve/simulate-sample-input.md)

## Lees hier meer

* **Vereiste toestemmingen** - u moet de **[!DNL Manage Simulate Content]** toestemming hebben inbegrepen in het **[!DNL Content Library Manager]** productprofiel. [Meer informatie](../administration/ootb-product-profiles.md#content-library-manager).

  Om proeven te verzenden, moet u **toestemmingen voor het specifieke middel (campagne of reis) verbonden aan e-mail goedkeuren en hebben publiceren.** Bovendien om proeven in een reis te verzenden, wordt de **Publish reis** toestemming ook vereist. [&#x200B; leer meer over toestemmingen &#x200B;](../administration/ootb-permissions.md).

* **Personalization met contextgegevens** - wanneer het previewing van een bericht of het verzenden van proeven, slechts worden de gegevens van de profielverpersoonlijking getoond. Personalization op basis van contextgegevens, zoals informatie over gebeurtenissen, kan alleen worden getest in het kader van een reis. Leer hoe in [&#x200B; dit gebruiksgeval &#x200B;](../personalization/personalization-use-case.md).

* **inhoud van de Voorproef met veelvoudige voorwaardelijke varianten** - wanneer het simuleren of het teruggeven van proeven voor e-mail die veelvoudige voorwaardelijke varianten bevatten, Journey Optimizer kan meer verwerkingstijd vereisen. Als u time-outs of foutberichten ervaart, kunt u overwegen het totale aantal varianten te verminderen of voorwaardelijke regels te vereenvoudigen. Leer meer over voorwaardelijke inhoud op [&#x200B; deze pagina &#x200B;](../personalization/dynamic-content.md).

## Hoe kan ik-video {#video-preview}

Leer hoe u testprofielen kunt gebruiken om het renderen van e-mail in verschillende vakken te testen, een voorbeeld van uw persoonlijke e-mails te bekijken op basis van testprofielen en proefdrukken te verzenden.

>[!VIDEO](https://video.tv.adobe.com/v/3430341?quality=12&captions=dut)
