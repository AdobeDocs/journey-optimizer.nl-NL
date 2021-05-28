---
title: Subdomeinen delegeren
description: Leer hoe u uw subdomeinen kunt delegeren
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: da995c56b59fb191934788c7aea9048123a2fe6d
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 43%

---


# Aan de slag met subdomeindelegatie

## Uw merken isoleren om uw reputatie te beschermen

Een subdomein is een afdeling van uw domein dat kan worden gebruikt om uw merken of diverse typen van traffic (transactionele berichten, marketinginformatie, enzovoort) te isoleren.
Neem bijvoorbeeld het domein mybrand.com, dat wordt gebruikt om zowel transactionele als marketingmededelingen te verzenden. In dit geval kunt u twee subdomeinen instellen:

* Het subdomein info.mybrand.com voor uw transactionele mededelingen (bevestiging van aankopen, herstel van wachtwoorden, enz.)
* Het subdomein marketing.mybrand.com voor e-mails aan prospects

Op deze manier kunt u de reputatie van uw domein en andere subdomeinen beter in stand houden. Als de marketing.mybrand.com-subdomeinen bijvoorbeeld door internetproviders aan de lijst van afgewezen domeinen werden toegevoegd vanwege slechte leverbaarheid, zou dit voorkomen dat het hele domein mybrand.com en het subdomein info.mybrand.com aan de lijst van afgewezen domeinen worden toegevoegd.

## Zorg ervoor dat de URL&#39;s van uw bronnen transparant blijven voor klanten

Bij het implementeren van een oplossing gelden er vereisten voor naar buiten gerichte onderdelen: het gaat hierbij onder andere om het instellen van koppelingen en webpagina&#39;s die moeten worden bijgehouden, het weergeven van spiegelpagina&#39;s, enz.

Hoewel deze vereisten worden beheerd via componenten die door zowel Adobe als de klant worden gehost, bevatten ze URL&#39;s die door de ontvangers van de e-mails kunnen worden bekeken. Om te voorkomen dat URL&#39;s de onderliggende technische oplossing of hostingprovider aangeven, kunnen subdomeinen worden ingesteld om dit transparant te maken voor de ontvangers van de e-mails. [Meer informatie over domeindelegatie](https://helpx.adobe.com/nl/campaign/kb/domain-name-delegation.html).

## Subdomeindelegatie in Journey Optimizer

Journey Optimizer biedt verschillende functies om u te helpen subdomeinen te beheren:

* [Uw ](delegate-subdomain.md) subdomeinen rechtstreeks van de interface delegeren,
* [Voeg Google TXT-](google-txt.md) records toe aan uw subdomeinen om ervoor te zorgen dat e-mails naar Gmail-adressen worden verzonden,
* [Heb toegang tot PTR ](ptr-records.md) recordsdie voor uw subdomeinen worden geproduceerd, die hen toestaan om door postservers te worden geverifieerd.
