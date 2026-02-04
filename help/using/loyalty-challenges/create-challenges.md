---
solution: Journey Optimizer
product: journey optimizer
title: Beleidsuitdagingen maken
description: Leer hoe u in Adobe Journey Optimizer loyaliteitsuitdagingen kunt maken en configureren.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private bèta" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---


# Uitdagingen maken {#create-challenges}

>[!BEGINSHADEBOX]

**de documentatie van de Uitdagingen van de Loyalty:**

* [ wordt begonnen met de Uitdagingen van de Loyalty ](get-started.md) - Overzicht, werkschema, eerste vereisten
* [ de Uitdagingen van de Loyalty van de Toegang ](access-loyalty-challenges.md) - Inventaris en het filtreren
* **creeer uitdagingen** {2 }︎ ◀ u hier **bent - bouw en vorm uitdagingen**
* [ creeer taken ](create-tasks.md) - bepaal uitdagingstaken
* [ beheert uitdagingen ](manage-challenges.md) - geef uit, controleer, optimaliseer

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Deze eigenschap is momenteel in **privé bèta** en kan niet in uw milieu beschikbaar zijn. Neem contact op met uw Adobe-vertegenwoordiger als u toegang wilt aanvragen. Leer meer over [ beschikbaarheidslabels ](../rn/releases.md#availability-labels).

## Werking {#how-it-works}

<!-- SCHEMA: Visual workflow showing the 5 main steps with icons: Create challenge → Add tasks → Design content cards → Configure messaging → Review and publish -->

Het creëren en lanceren van een loyaliteitsuitdaging volgt deze werkschema:

1. **creeer een uitdaging** - bepaal de basisuitdagingseigenschappen met inbegrip van naam, type (Norm, Streak, of Opeenvolgend), publiek, en datumwaaier.

1. **voegt taken** toe - bepaal de specifieke acties klanten, met inbegrip van taaktypes (aankoop, uitgeven, bezoek, enz.), hoeveelheden, productfilters, en beloningen moeten voltooien.

1. **de inhoudskaarten van het Ontwerp** - creeer de visuele vertegenwoordiging van uw uitdaging gebruikend de inhoudskaarten van Journey Optimizer die op klantenapparaten tonen.

1. **vorm overseinen** (Facultatief) - Opstelling multi-kanaalberichten (in-app, e-mail, duw, SMS) voor zeer belangrijke stadia: lancering, lopend, en voltooiing.

1. **Overzicht en publiceer** - test uw uitdaging met testprofielen, dan publiceer het om het ter beschikking te stellen van uw doelpubliek.

## Maak de uitdaging {#create-challenge}

<!-- SCREENSHOT: Challenge creation screen showing challenge properties form with fields for name, type, audience, dates -->

Een nieuwe loyaliteitsuitdaging creëren:

1. Navigeer naar **[!UICONTROL Loyalty challenges]** in Journey Optimizer.

1. Selecteer het tabblad **[!UICONTROL Challenges]**. 

1. Selecteer **[!UICONTROL Create challenge]**.

1. Vorm de uitdagingseigenschappen:

   **de naam van de Uitdaging**: Ga een beschrijvende naam voor uw uitdaging in. Deze naam wordt weergegeven in de inventaris van uitdagingen en helpt u de uitdaging te identificeren.

   **Type van Uitdaging**: Selecteer één van de volgende types:
   * **[!UICONTROL Standard]**: klanten voltooien een opgegeven aantal taken in elke willekeurige volgorde
   * **[!UICONTROL Streak]**: klanten voltooien dezelfde taak meerdere keren achter elkaar
   * **[!UICONTROL Sequential]**: klanten voltooien taken in een gedefinieerde volgorde

   **het publiek van het Doel**: Selecteer het publiekssegment dat bepaalt wie aan deze uitdaging kan deelnemen. U moet een publiek maken in Experience Platform voordat u uitdagingen aanbrengt. Voor meer informatie, zie [ begonnen worden met publiek ](../audience/about-audiences.md).

   **datum van het Begin**: Plaats wanneer de uitdaging aan klanten beschikbaar wordt.

   **einddatum**: Plaats wanneer de uitdaging verloopt en niet meer nieuwe voltooide goedkeurt.

<!-- VISUAL: Comparison table or diagram showing the three challenge types (Standard, Streak, Sequential) with examples of each -->

### Taken toevoegen {#add-tasks}

De taken bepalen de specifieke acties of de mijlpalen die de klanten moeten voltooien om beloningen te verdienen. U configureert taaktypen (aanschaf, uitgave, bezoek, betrokkenheid, aangepaste gebeurtenissen), hoeveelheden, productfilters en beloningen.

Afhankelijk van uw uitdagingstype, voltooien de klanten verschillend taken:

* **Standaard uitdagingen**: Voltooi om het even welk gespecificeerd aantal taken in om het even welke orde
* **Streak uitdagingen**: Voltooi de zelfde taak veelvoudige tijden opeenvolgend
* **Opeenvolgende uitdagingen**: Volledige taken in een bepaalde orde

Als u taken wilt toevoegen aan uw taak, selecteert u **[!UICONTROL Add task]** in de sectie Taken en configureert u de taakeigenschappen.

Voor gedetailleerde instructies bij het creëren van en het vormen van taken, zie [ tot taken ](create-tasks.md) leiden.

### Inhoudskaarten configureren {#configure-content-cards}

<!-- SCREENSHOT: Content cards configuration section in the challenge editor -->

De kaarten van de inhoud verstrekken de visuele vertegenwoordiging van uw uitdaging op klantenapparaten, tonend uitdagingsinformatie, vooruitgang, en beloningen. Leer meer over [ inhoudskaarten ](../content-card/get-started-content-card.md).

<!-- VISUAL: Example content card designs showing different states: challenge start, in-progress with progress bar, completion with reward -->

Om inhoudskaarten voor uw uitdaging te vormen:

1. Navigeer in de uitdagingseditor naar de sectie **[!UICONTROL Content cards]** .

1. Selecteer **[!UICONTROL Create content card]** of kies een bestaande sjabloon.

1. Ontwerp uw inhoudskaart:
   * Afbeeldingen, tekst en branding toevoegen
   * Omvat [ personalisatietokens ](../personalization/personalization-syntax.md) om klant-specifieke informatie te tonen
   * Voortgangsindicatoren voor uitdagingen weergeven
   * Beloningen en stimulansen weergeven

1. Configureren wanneer de inhoudskaart wordt weergegeven:
   * **Begin van de Uitdaging**: Toon wanneer de uitdaging beschikbaar wordt
   * **Bezig**: Vertoning terwijl de klanten actief deelnemen
   * **Voltooiing**: Toon nadat de klanten alle taken voltooien

1. Bekijk een voorvertoning van de inhoudskaart op verschillende apparaten voor een correcte weergave.

1. Sla de configuratie van de inhoudskaart op.

Voor meer informatie bij het ontwerpen van en het aanpassen van inhoudskaarten, zie [ de inhoudskaarten van het Ontwerp ](../content-card/design-content-card.md).

### Berichten configureren {#configure-messaging}

<!-- SCREENSHOT: Messaging configuration section showing the three lifecycle stages: Launch, In-progress, Completion -->

De berichten van de opstelling multi-channel om klanten in belangrijkste stadia van de uitdagingslevenscyclus in dienst te nemen.

<!-- VISUAL: Timeline diagram showing when each message type is sent during the challenge lifecycle -->

Om overseinen voor uw uitdaging te vormen:

1. Navigeer in de uitdagingseditor naar de sectie **[!UICONTROL Messaging]** .

1. Berichten configureren voor elke levenscyclusfase:

   **de berichten van de Lancering** - breng klanten op de hoogte wanneer de uitdaging begint:
   * Selecteer kanalen: [ In-app ](../in-app/get-started-in-app.md), [ e-mail ](../email/get-started-email.md), [ duw bericht ](../push/get-started-push.md), of [ SMS ](../sms/get-started-sms.md)
   * Ontwerp het bericht met uitdagingsdetails en call-to-action
   * Stel timing in: Verzend onmiddellijk wanneer de uitdaging live gaat of een specifieke tijd plant

   **Op voortgang berichten** - houd klanten betrokken tijdens de uitdaging:
   * Definieer triggervoorwaarden (bijvoorbeeld 50% voltooiing, specifieke taak voltooid)
   * Herinneringsberichten maken om verdere deelname aan te moedigen
   * Updates en volgende stappen opnemen

   **de berichten van de Voltooiing** - vieren succes en leveren beloningen:
   * Gefeliciteerd klanten bij het voltooien van de uitdaging
   * Toekenning van beloning bevestigen
   * Instructies geven voor het opvragen van beloningen
   * Volgende uitdagingen of acties voorstellen

Raadpleeg voor meer informatie over het maken van berichten voor specifieke kanalen:

* [Documentatie voor in-app berichten](../in-app/get-started-in-app.md)
* [E-mailberichten](../email/get-started-email.md)
* [Documentatie voor pushmeldingen](../push/get-started-push.md)
* [Documentatie voor SMS-berichten](../sms/get-started-sms.md)

## De uitdaging bekijken en publiceren {#review-and-publish}

<!-- SCREENSHOT: Review screen showing summary of challenge configuration with all components listed -->

Voordat u uw uitdaging publiceert:

1. **Overzicht alle componenten**: Verifieer uitdagingseigenschappen, taken, beloningen, inhoudskaarten, en overseinenconfiguraties.

1. **Test de ervaring**: Gebruik [ testprofielen ](../test-approve/test-profiles.md) om de vertoning van de inhoudskaart en het gedrag van de taaktrekker te bevestigen.

1. **publiceer**: Selecteer **[!UICONTROL Publish]** om de uitdaging voor uw doelpubliek beschikbaar te maken.

<!-- SCREENSHOT: Journeys inventory showing the auto-generated journey in Draft status with name format "Challenge: [Challenge Name]" -->

Wanneer u een uitdaging publiceert, leidt Journey Optimizer automatisch tot a [ reis ](../building-journeys/journey-gs.md) in de status van het Ontwerp. De auto-geproduceerde reis verschijnt in uw reisinventaris met het naamformaat &quot;Uitdaging: [ Naam van de Uitdaging ]&quot;.

Om de uitdaging voor klanten beschikbaar te maken:

1. Navigeer naar de **[!UICONTROL Journeys]** -voorraad in Journey Optimizer.

1. Zoek de automatisch gegenereerde reis (deze heeft &#39;Uitdaging:&#39; als voorvoegsel in de naam).

1. [ activeer de reis ](../building-journeys/publishing-the-journey.md).

De reis begint automatisch op uw gespecificeerde datum van de uitdagingsaanvang.

>[!NOTE]
>
>De automatisch gegenereerde reis wordt weergegeven in uw reisvoorraad en kan indien nodig worden aangepast. Nochtans, synchroniseren de veranderingen die rechtstreeks aan de reis worden aangebracht niet terug naar de uitdagingsconfiguratie.

## Volgende stappen {#next-steps}

* [ beheert uitdagingen ](manage-challenges.md) - Leer hoe te, uitdagingen uit te geven te controleren en te optimaliseren
* [ Begrijp Loyalty Uitdagingen ](get-started.md) - de eigenschappen en de mogelijkheden van het overzicht

