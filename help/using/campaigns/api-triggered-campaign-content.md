---
solution: Journey Optimizer
product: journey optimizer
title: De inhoud van de door de API geactiveerde campagne bewerken
description: Leer hoe u de inhoud van de door de API geactiveerde campagne kunt bewerken.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagnes, API-geactiveerd, REST, optimizer, berichten
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---


# De inhoud van de door de API geactiveerde campagne bewerken {#api-content}

Als u de inhoud van het bericht wilt configureren, navigeert u naar de tab **[!UICONTROL Content]** of klikt u op de knop **[!UICONTROL Edit content]** .

![](assets/campaign-content.png)

## De inhoud ontwerpen {#design}

Het proces voor het maken van inhoud is afhankelijk van het kanaal dat u hebt geselecteerd. Leer gedetailleerde stappen om uw berichtinhoud op de volgende pagina&#39;s tot stand te brengen:

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/create-email.md"><img alt="email" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/create-email.md"><strong> E-mail </strong></a></div></td>
<td><a href="../sms/create-sms.md"><img alt="sms" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../sms/create-sms.md"><strong> SMS </strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="duwen" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../push/create-push.md"><strong> Push bericht </strong></a></div></td>
</tr></table>

## Inhoud aanpassen met contextafhankelijke gegevens {#contextual}

U kunt aanvullende gegevens doorgeven in de API-lading die u kunt gebruiken om uw bericht aan te passen.

Neem dit voorbeeld, waar de klanten hun wachtwoord willen terugstellen, en u hen een wachtwoord wilt verzenden terugstellen URL die in een derdehulpmiddel wordt geproduceerd. Met API-getriggerde campagnes kunt u deze gegenereerde URL doorgeven in de API-lading en deze gebruiken in de campagne om deze toe te voegen aan het bericht.

Hiervoor moet u ze doorgeven in de API-payload en ze toevoegen in uw bericht met de personalisatie-editor. Gebruik de syntaxis `{{context.<contextualAttribute>}}` , waarbij `<contextualAttribute>` moet overeenkomen met de naam van de variabele in de API-lading die de gegevens bevat die u wilt doorgeven.

Let op: voorlopig is er geen contextueel kenmerk beschikbaar voor gebruik in het menu Linkerspoor. Kenmerken moeten rechtstreeks in uw personalisatie-expressie worden getypt, zonder dat er een controle door [!DNL Journey Optimizer] wordt uitgevoerd.

![](assets/api-triggered-context.png)

**moet** lezen

* De contextafhankelijke kenmerken die in de aanvraag worden doorgegeven, mogen niet groter zijn dan 200 kB en houden altijd rekening met het type tekenreeks.
* De syntaxis van `context.system` is beperkt tot intern gebruik van Adobe en mag niet worden gebruikt om contextuele kenmerken door te geven.
* In tegenstelling tot voor profielen geschikte gebeurtenissen, worden de contextuele gegevens die in de REST API worden doorgegeven, gebruikt voor eenmalige communicatie en niet opgeslagen tegen profiel. Als er geen naamruimte is gevonden, wordt er maximaal een profiel gemaakt met de naamruimtedetails.
* Het gebruik van een groot aantal of zware contextafhankelijke gegevens in uw inhoud kan van invloed zijn op de prestaties.

## Inhoud testen en controleren

Zodra de inhoud is gedefinieerd, gebruikt u de knop **[!UICONTROL Simulate content]** om een voorvertoning van uw inhoud weer te geven en deze te testen met testprofielen of voorbeeldinvoergegevens die vanuit een CSV-/JSON-bestand zijn geüpload of handmatig zijn toegevoegd. [&#x200B; Leer hoe te om inhoud &#x200B;](../content-management/preview-test.md) voor te vertonen en te testen. Klik op de linkerpijl om terug te bladeren naar het scherm Campagne maken.

![](assets/create-campaign-design.png)

## Volgende stappen {#next}

Zodra uw campagneconfiguratie en inhoud klaar zijn, kunt u het campagnepubliek bepalen. [Meer informatie](api-triggered-campaign-audience.md)
