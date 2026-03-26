---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met bestemmingspagina's
description: Meer informatie over bestemmingspagina's in Journey Optimizer
feature: Landing Pages, Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: landen, landingspagina, starten, starten
exl-id: 0da96e32-52ad-4cc3-bac4-844b1f39ed16
source-git-commit: d0dd382521aeb2c7e18dc547c2ec55fa1472ab8d
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 3%

---

# Aan de slag met bestemmingspagina&#39;s {#get-started-lp}

Een openingspagina is een zelfstandige webpagina waarnaar een gebruiker wordt verwezen nadat hij via een e-mail, website, advertentie of een andere digitale locatie heeft geklikt.

Met [!DNL Journey Optimizer] kunt u bestemmingspagina&#39;s maken en ontwerpen, zodat uw gebruikers naar onlineformulieren kunnen gaan waar ze zich kunnen aanmelden of afmelden voor het ontvangen van uw communicatie of een specifieke service zoals een nieuwsbrief.

➡️ [&#x200B; Leer meer over het vormen van abonnementen en het creëren van landende pagina&#39;s in deze video &#x200B;](#video)

## Wanneer moeten bestemmingspagina&#39;s worden gebruikt? {#when-to-use}

Gebruik openingspagina&#39;s als u wilt:

* Laat klanten **binnen kiezen of kiezen uit** van marketing mededelingen of een specifieke dienst of een nieuwsbrief van een verbinding in e-mail of campagne-met inbegrip van abonnementenlijsten voor de gerichte diensten. [Meer informatie](lp-use-cases.md#subscription-to-a-service)
* **verzamel toestemming** alvorens mededelingen te verzenden en a **bevestigingsE-mail** op opt-in of opt-out te verzenden. [Meer informatie](lp-use-cases.md#send-confirmation-email)
* **vangt of werkt profielgegevens** gebruikend vormen op **[!UICONTROL Data Capture]** het landen pagina-voor progressieve het profileren, voorkeur, registraties, en gelijkaardige scenario&#39;s bij. [Meer informatie](#data-capture-lp)
* Richt gebruikers aan a **specifieke Webvorm** zonder een externe pagina buiten [!DNL Journey Optimizer] te bouwen opnieuw
* Bouw **ontvankelijke het landen pagina&#39;s** gebruikend [!DNL Journey Optimizer] inhoudsontwerpmogelijkheden

### Gegevensvastlegging met bestemmingspagina&#39;s {#data-capture-lp}

Met landingspagina&#39;s van **[!UICONTROL Data Capture]** kunt u gepubliceerde formulieren insluiten, zodat bezoekers kenmerken kunnen verzenden die naar uw [!DNL Adobe Experience Platform] -gegevensset zijn geschreven via de streamingverbinding die in de formuliervoorinstelling is geconfigureerd. [&#x200B; Leer om vormen in een het landen pagina tot stand te brengen en in te bedden &#x200B;](lp-forms.md)

>[!NOTE]
>
>De vangst van gegevens door het landen van paginavormen wordt gesteund voor **gekende profielen** (bestaande die profielen in [!DNL Adobe Experience Platform] worden geïdentificeerd). De het landen pagina zou van a **gepersonaliseerde verbinding** (bijvoorbeeld van een e-mailcampagne) moeten worden geopend zodat kan de profielidentiteit worden opgelost wanneer de pagina laadt.

Hieronder vindt u voorbeelden van gebruiksgevallen:

1. **Progressieve profielverrijking** - verzamel extra attributen van bekende klanten-zoals telefoonaantal, geboortedatum, of plaats-door een gepersonaliseerde het landen pagina om hun bestaand [!DNL Experience Platform] profiel voor segmentatie en verpersoonlijking te verrijken.

2. **de update van het Centrum van de voorkeur** - sta bekende abonnees toe om hun communicatie voorkeur (kanaal, onderwerpbelangen) via een het landen pagina te beheren, met veranderingen typisch die in hun [!DNL Experience Platform] profiel binnen ongeveer 15 minuten worden weerspiegeld.

3. **Gebeurtenis of webinar registratie** — Vang gebeurtenis-specifieke gegevens van bekende profielen op een registratiepagina, werk het profiel met registratiekentekenmerken bij, en teweeg een bevestigingsreis.

4. **Loyalty of programmainschrijving** - laat bestaande klanten in loyaliteitsprogramma&#39;s of lidmaatschapsrijen inschrijven door extra details door een landende pagina voor te leggen, die het profiel voor stroomafwaarts richten verrijken.

5. **Mededinging of de ingang van de prijsvraag** — Laat bekende klanten wedstrijden of transporten via een het landen paginavorm ingaan; vang ingang-specifieke details (antwoorden, voorkeur, of verklaringen) en schrijf hen aan het profiel om verkiesbaarheid, winnaar selectie, en follow-up reizen te steunen.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-lp.md">
<img alt="Lood" src="../assets/do-not-localize/lp-subscription.jpeg">
</a>
<div><a href="create-lp.md"><strong> creeer het landen pagina's </strong>
</div>
<p>
</td>
<td>
<a href="subscription-list.md">
<img alt="Onfrequent" src="../assets/do-not-localize/lp-list.jpg">
</a>
<div>
<a href="subscription-list.md"><strong> creeer abonnementenlijsten </strong></a>
</div>
<p></td>
<td>
<a href="lp-forms.md">
<img alt="Forms-lijst voor bestemmingspagina&apos;s in Journey Optimizer" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong> de vormen van het gebruik in uw het landen pagina's </strong></a>
</div>
<p>
</td>
<td>
<a href="../reports/lp-report-live.md">
<img alt="Validatie" src="../assets/do-not-localize/lp-reporting.jpg">
</a>
<div>
<a href="../reports/lp-report-live.md"><strong> Meldend </strong></a>
</div>
<p>
</td>
</tr></table>

## Voordat u begint {#prerequisites}

Voer de volgende stappen uit voordat u een openingspagina maakt:

1. **vorm subdomain** — Opstelling subdomain specifiek aan het ontvangen van uw landende pagina&#39;s. [Meer informatie](lp-subdomains.md)
1. **creeer een het landen vooraf ingestelde pagina** - vooraf ingesteld bepaalt subdomain en andere montages die op uw het landen pagina&#39;s worden toegepast. [Meer informatie](lp-presets.md#lp-create-preset)
1. **creeer een abonnementenlijst** (voor de gevallen van het abonnementsgebruik) — Vereist als u klanten aan of zich van de specifieke dienst wilt intekenen. [Meer informatie](subscription-list.md)
1. **creeer een vorm** (voor gegevens vangt gebruiksgevallen) — Vereist wanneer u een vorm op een **[!UICONTROL Data Capture]** landende pagina wilt inbedden en bijdragen verzenden naar [!DNL Experience Platform]. [Meer informatie](lp-forms.md)

## Werking {#how-it-works}

Het creëren van en het opstellen van een het landen pagina volgen deze opeenvolging:

1. **creeer en vorm uw het landen pagina** — selecteer vooraf ingesteld, opstelling de primaire pagina, en voeg om het even welke vereiste subpages toe. [Meer informatie](create-lp.md#create-landing-page)
1. **Ontwerp de pagina** — Bouw de pagina inhoud en de vorm gebruikend [!DNL Journey Optimizer] belemmering-en-dalingsredacteur. [Meer informatie](design-lp.md)
1. **Test en publiceer uw het landen pagina** — Voorproef de pagina, test vormgedrag, dan publiceren om het levend te maken. [Meer informatie](create-lp.md#test-landing-page)
1. **Verbinding in een bericht of een reis** - voeg de het landen pagina URL aan een e-mail, een campagne, of een reisactie toe zodat de klanten het kunnen bereiken. [Meer informatie](../email/message-tracking.md#insert-links)

## Hoe kan ik-video{#video}

In de onderstaande video ziet u hoe u een abonnementenlijst kunt maken, bestemmingspagina&#39;s kunt instellen om in te schakelen op of te weigeren van een service, de optie om te weigeren of te weigeren kunt integreren in een bericht en relevante reizen kunt configureren.

>[!VIDEO](https://video.tv.adobe.com/v/341280?quality=12&learn=on)
