---
solution: Journey Optimizer
product: journey optimizer
title: Informatie over Adobe Experience Platform-publiek
description: Leer hoe u met het publiek van Adobe Experience Platform kunt werken
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 3ec496ba-7555-49e2-992c-403c33302a90
source-git-commit: f99ba639b5d47fa334741b7e55e7bce83697626d
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Verrijkingskenmerken van soorten publiek gebruiken {#enrichment}

Wanneer het richten van een publiek dat gebruikend samenstellingswerkschema&#39;s, het publiek van het douane (Csv- dossier), of Federated de Samenstelling van het Publiek wordt geproduceerd, kunt u hefboomwerkingsattributen van deze publiek gebruiken om uw reis te bouwen en uw berichten te personaliseren.

>[!NOTE]
>
>Soorten publiek dat vóór 1 oktober 2024 via aangepaste upload naar CSV-bestanden is gemaakt, komen niet in aanmerking voor personalisatie. Als u kenmerken van deze doelgroepen wilt gebruiken en ten volle wilt profiteren van deze functie, maakt u een extern CSV-publiek dat u vóór deze datum hebt geïmporteerd, opnieuw en uploadt u het opnieuw.
>
>Het beleid van de toestemming steunt geen verrijkingsattributen. Daarom moeten regels voor het toestemmingsbeleid alleen gebaseerd zijn op kenmerken in het profiel.

Hier volgen de acties die u kunt uitvoeren met de verrijkingskenmerken van het publiek:

* **creeer veelvoudige weg in een reis** die op regels wordt gebaseerd die hefboomwerking de de verrijkingsattributen van het doelpubliek. Om dit te doen, richt het publiek dat a [ gebruikt gelezen publiek ](../building-journeys/read-audience.md) activiteit dan tot regels in de activiteit van de Voorwaarde van a [ ](../building-journeys/condition-activity.md) leidt die op de verrijkingsattributen van het publiek wordt gebaseerd.

  ![](assets/audience-enrichment-attribute-condition.png){width="70%" zoomable="yes"}

* **personaliseer uw berichten** in reizen of campagnes door verrijkingsattributen van het gerichte publiek in de verpersoonlijkingsredacteur toe te voegen. [ Leer hoe te met de verpersoonlijkingsredacteur ](../personalization/personalization-build-expressions.md) te werken

  ![](assets/audience-enrichment-attribute-perso.png){width="70%" zoomable="yes"}

>[!IMPORTANT]
>
>Om verrijkingsattributen van publiek te gebruiken creeerde het gebruiken van samenstellingswerkschema&#39;s, zorg ervoor dat zij aan een Groep van het Gebied binnen &quot;ExperiencePlatform&quot;Gegevens Source worden toegevoegd.
>
+++ Leer hoe u verrijkingskenmerken aan een veldgroep kunt toevoegen>
>
1. Navigeer naar &quot;Beheer&quot; > &quot;Configuratie&quot; > &quot;Gegevensbronnen&quot;.
1. Selecteer &quot;Experience Platform&quot; en maak of bewerk een veldgroep.
1. Selecteer het gewenste schema in de schemaselector. De naam van het schema heeft de volgende indeling: &#39;Schema voor publiek-id:&#39; + de id van het publiek. U kunt de id van het publiek vinden op het scherm met publieksdetails in de publieksinventaris.
1. Open de veldkiezer, zoek de verrijkingskenmerken die u wilt toevoegen en selecteer het selectievakje naast deze kenmerken.
1. Sla uw wijzigingen op.
1. Nadat verrijkingskenmerken aan een veldgroep zijn toegevoegd, kunt u deze op de hierboven vermelde locaties benutten in Journey Optimizer.
>
Gedetailleerde informatie over gegevensbronnen is beschikbaar in deze secties:
>
* [ Werk met de gegevensbron van Adobe Experience Platform ](../datasource/adobe-experience-platform-data-source.md)
* [ vorm een gegevensbron ](../datasource/configure-data-sources.md)
>
+++







+++ Wat zijn verrijkingskenmerken?

Verrijkingskenmerken zijn aanvullende kenmerken die contextueel zijn en specifiek zijn voor een publiek. Ze zijn niet gekoppeld aan het profiel en worden doorgaans gebruikt voor personalisatiedoeleinden.

De attributen van de verrijking zijn verbonden aan een publiek via een Verrijken activiteit in publiekssamenstelling of door het douaneuploadproces.

+++

+++ Waar kan ik verrijkingskenmerken gebruiken in Journey Optimizer?

De attributen van de verrijking van publiekssamenstelling kunnen in de volgende gebieden worden gebruikt. [ Leer hoe te om de attributen van de kijkverrijking ](#enrichment) te gebruiken

* Condition activity (Reizen)
* Aangepaste actiekenmerken (reizen)
* Berichten personaliseren (reizen en campagnes)

+++

+++ Hoe laat ik verrijkingskenmerken toe in Reizen?

Om verrijkingsattributen van publiek te gebruiken creeerde het gebruiken van samenstellingswerkschema&#39;s, zorg ervoor zij aan een Groep van het Gebied binnen &quot;ExperiencePlatform&quot;Gegevens Source worden toegevoegd. De informatie over hoe te om verrijkingsattributen aan een Groep van het Gebied toe te voegen is beschikbaar in [ deze sectie ](#enrichment)

+++

+++ Zijn de waarden van verrijkingsattributen bijgewerkt nadat een reis begint?

Neen. Zelfs na wachttijden of gebeurtenisknopen, blijven de waarden van de verrijkingsattributen het zelfde als zij toen de reis begon.

+++
