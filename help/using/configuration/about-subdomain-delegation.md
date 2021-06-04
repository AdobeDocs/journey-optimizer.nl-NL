---
title: Subdomeinen delegeren
description: Leer hoe u uw subdomeinen kunt delegeren
internal: n
snippet: y
source-git-commit: e569e992530df5429ffb96f78ba28b53de0ded81
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 26%

---


# Subdomeindelegatie in [!DNL Journey Optimizer]

Het creëren van subdomain voor e-mailcampagnes staat merken toe om verschillende types van verkeer (marketing versus collectief bijvoorbeeld) in specifieke IP groepen en met specifieke domeinen te isoleren, die het IP opwarmingsproces zullen versnellen en leveringscapaciteit over het algemeen zullen verbeteren. Als u een domein deelt en het wordt geblokkeerd of aan de lijst van gewezen personen toegevoegd, zou het uw collectieve postlevering kunnen beïnvloeden. Nochtans, zullen de kwesties van de reputatie of de blokken op een domein specifiek voor uw e-mailmarketing mededelingen enkel die stroom van e-mail beïnvloeden. Als u uw hoofddomein als afzender of het adres &#39;Van&#39; voor meerdere e-mailstreams gebruikt, kan de e-mailverificatie ook worden verbroken, waardoor uw berichten worden geblokkeerd of in de spammap worden geplaatst.

Een subdomein is een afdeling van uw domein dat kan worden gebruikt om uw merken, of diverse soorten verkeer - bijvoorbeeld transactionele berichten en marketing mededelingen te isoleren.

Neem bijvoorbeeld het domein mybrand.com, dat wordt gebruikt om zowel transactionele als marketingmededelingen te verzenden. In dit geval kunt u twee subdomeinen instellen:

* Het subdomein info.mybrand.com voor uw transactionele mededelingen (bevestiging van aankopen, herstel van wachtwoorden, enz.)
* Het subdomein marketing.mybrand.com voor e-mails aan prospects

Op deze manier kunt u de reputatie van uw domein en andere subdomeinen beter in stand houden. Als de marketing.mybrand.com-subdomeinen bijvoorbeeld door internetproviders aan de lijst van afgewezen domeinen werden toegevoegd vanwege slechte leverbaarheid, zou dit voorkomen dat het hele domein mybrand.com en het subdomein info.mybrand.com aan de lijst van afgewezen domeinen worden toegevoegd.

Bij het implementeren van een oplossing gelden er vereisten voor naar buiten gerichte onderdelen: het gaat hierbij onder andere om het instellen van koppelingen en webpagina&#39;s die moeten worden bijgehouden, het weergeven van spiegelpagina&#39;s, enz.

Hoewel deze vereisten worden beheerd via componenten die door zowel Adobe als de klant worden gehost, bevatten ze URL&#39;s die door de ontvangers van de e-mails kunnen worden bekeken. Om te voorkomen dat URL&#39;s de onderliggende technische oplossing of hostingprovider aangeven, kunnen subdomeinen worden ingesteld om dit transparant te maken voor de ontvangers van de e-mails.

**Meer informatie**

* Leer hoe te om [uw subdomeinen](delegate-subdomain.md) direct van de interface te delegeren
* Leer hoe u Google TXT-records](google-txt.md) aan uw subdomeinen kunt toevoegen om ervoor te zorgen dat e-mails naar Gmail-adressen worden verzonden[
* Leer hoe te om tot de PTR- verslagen ](ptr-records.md) toegang te hebben die voor uw subdomeinen worden geproduceerd, die hen toestaan om door het verzenden van postservers te worden geverifieerd[
