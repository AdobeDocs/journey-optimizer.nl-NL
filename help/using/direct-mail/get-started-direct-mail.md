---
title: Aan de slag met direct mail
description: Leer hoe u een e-mailbericht maakt en stuurt naar Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: direct mail, bericht, campagne
source-git-commit: 40cd058475b37b8fa7d5c0286ad230422e027cf8
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# Een direct-mailbericht maken {#create-direct}

>[!AVAILABILITY]
>
>Direct mail channel is momenteel niet beschikbaar voor organisaties die de Adobe Healthcare Shield Add-on-aanbieding hebben aangeschaft.

Directe post is een off-line kanaal dat u toestaat om de extractiedossiers te personaliseren en te produceren die door directe postleveranciers worden vereist om post naar uw klanten te verzenden.

Bij het maken van een campagne voor direct mail genereert Journey Optimizer automatisch een bestand met alle doelprofielen en geselecteerde gegevens, zoals postadressen en profielkenmerken. Dit bestand wordt naar de server van uw keuze verzonden, zodat het toegankelijk is voor uw gekozen directe-mailprovider, die het eigenlijke mailingproces voor u afhandelt.

De belangrijkste stappen voor het verzenden van direct-mailberichten zijn als volgt:

![](assets/dm-creation-process.png)

Directe-mailberichten kunnen alleen worden gemaakt in het kader van geplande campagnes. Ze zijn niet beschikbaar voor gebruik in API-getriggerde campagnes of reizen.

>[!IMPORTANT]
>
>Alvorens een direct-mailbericht te verzenden, zorg ervoor u hebt gevormd:
>
>1. A [bestand dat configuratie verplettert](../direct-mail/direct-mail-configuration.md#file-routing-configuration) die de server aangeeft waar het extractiebestand moet worden geüpload en opgeslagen,
>1. A [direct-mailberichtoppervlak](../direct-mail/direct-mail-configuration.md#direct-mail-surface) die naar het dossier zal verwijzen dat configuratie verplettert.
