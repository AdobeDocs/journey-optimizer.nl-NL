---
title: Migreren naar inline authoring
description: Leer hoe u berichten kunt migreren
exl-id: accdebba-5322-401e-8a40-3e1539e65a7e
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '1734'
ht-degree: 0%

---


# Overzicht van inlineontwerpmigratie{#inline-authoring}

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_before"
>title="Meer informatie over de nieuwe inline ontwerpfunctie"
>abstract="Vanaf 25 juli 2022 worden berichten rechtstreeks vanuit een reis geschreven. Bestaande berichten worden automatisch naar het nieuwe model gemigreerd. Na de migratie zijn aanvullende acties vereist als u momenteel berichten gebruikt voor uw reizen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="Migratiestappen"

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_during"
>title="Leer wat er gebeurt"
>abstract="Vanaf 25 juli 2022 worden berichten rechtstreeks vanuit een reis geschreven. Uw omgeving wordt gemigreerd. Na de migratie zijn aanvullende acties vereist als u momenteel berichten gebruikt voor uw reizen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="Migratiestappen"

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_after"
>title="Leer hoe u berichten kunt migreren"
>abstract="Vanaf 25 juli 2022 worden berichten rechtstreeks vanuit een reis geschreven. Bestaande berichten zijn nu gemigreerd naar het nieuwe model. Als reisdeskundige zijn nu aanvullende maatregelen nodig voor reizen die gebruikmaken van berichten."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="Migratiestappen"

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Leer hoe u berichten kunt migreren"
>abstract="Vanaf 25 juli 2022 verdwijnt het menu Berichten en worden berichten rechtstreeks vanuit een Reis geschreven. Als u oude berichten tijdens reizen opnieuw wilt gebruiken, moet u ze opslaan als sjablonen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/design/email-templates.html#save-as-template" text="Berichten opslaan als sjablonen"

Adobe Journey Optimizer geeft een nieuwe functie uit die de manier verbetert waarop u inhoud ontwerpt voor Journey Optimizer-kanalen (e-mail, push, SMS). Als Journey Optimizer-expert kunt u nu uw berichten rechtstreeks maken en schrijven vanaf een reis.

Deze functie vereist een migratie van bestaande reizen die berichten gebruiken. Op deze pagina vindt u de benodigde informatie over deze wijziging en de stappen die u nodig hebt.

Raadpleeg deze voor meer informatie over uw rollen en verantwoordelijkheden als Journey Optimizer-expert [page](../start/path/marketer.md).

<!--
Here are the main changes in the interface:

* Messages are created direcly from journeys.
* The **Messages** entry in the left navigation menu has been removed. 
* There is no separate library of messages, the journey now centralizes all components.


-->

>[!VIDEO](https://video.tv.adobe.com/v/344698)


## Toetsgrepen{#keys}

* **Heb ik last van**: u wordt beïnvloed als u berichten van creeert **Berichten** in de linkernavigatie en gebruik hen in uw reizen. Als u een systeem van derden gebruikt (zoals Adobe Campaign), heeft deze migratie geen invloed op u.

* **Productwijzigingen**: bij GA (25 juli), wordt uw kanaalinhoud gecreeerd en binnen elke reis beheerd. De **Berichten** in de linkernavigatie niet meer beschikbaar is ([Meer informatie](../rn/inline-messages.md#change)). We gaan verder met een migratie voor uw bestaande reizen.

* **Tijdlijn**: migratie vindt plaats voor elk gebied bij nacht, door verscheidene [herhalingen](../rn/inline-messages.md#iterations).

   ![](assets/inline-migration-timeline.png)

* **Vereiste acties**: voor u wordt een automatische omzetting van de ritten uitgevoerd. Toch hebben we uw hulp nodig met een paar stappen. Meer informatie over de vereiste stappen in deze [page](../rn/inline-messages-steps.md).

* **Deprectie**: na 6 september worden alle reizen die nog steeds gebruikmaken van oude berichten stopgezet en later verwijderd.

## Voordelen en productwijzigingen{#change}

voortdurend Adobe om de productstromen te vereenvoudigen. Deze nieuwe manier om berichten te maken zorgt voor een gestroomlijnder gebruikersproces.

We hebben deze nieuwe workflow zo ontworpen dat inhoud op één locatie wordt gecentraliseerd, direct waar deze wordt gebruikt.

De creatie van inhoud wordt nu direct binnen de reis uitgevoerd. De **uitkeringen** je krijgt het volgende:

* Snellere trajecten met gebruik van Journey Optimizer-kanalen in een enkele flow.
* Snelle visualisatie van inhoud door naadloos over te schakelen tussen alle e-mail-, push- en SMS-inhoud op een reis.
* Verbeterde stroom voor e-mails en push-technologie met gebruik van contextafhankelijke personalisatie vanaf het canvas.
* Bij het rapporteren van reizen worden gedetailleerde kanaalrapportgegevens centraal gesteld.

Hier zijn de **productwijzigingen** met deze nieuwe functie :

<table>
<tr>
<th>Voor migratie</th>
<th>Na migratie</th>
</tr>
<tr>
<td><img src="assets/inline-migration-before.png"><p>Voor hebt u een bericht gemaakt op basis van de <strong>Berichten</strong> -menu. </p></td>
<td><img src="assets/inline-migration-after.png"><p>De <strong>Berichten</strong> in de linkernavigatie niet meer beschikbaar is. </p></td>
</tr>
<tr>
<td><img src="assets/inline-migration-before2.png"><p>Daarna hebt u een reis gemaakt, <strong>Bericht</strong> en selecteert u het eerder gemaakte bericht.</p></td>
<td><img src="assets/inline-migration-after2.png"><p>U voegt nu gewoon de gewenste actie voor het kanaal (e-mail, SMS, push) toe aan uw reis. In de activiteit, vormt u direct de berichtparameters en hebt toegang tot de inhoudsredacteur.</p></td>
</tr>
<tr>
<td><img src="assets/inline-migration-before3.png"><p>Voordien was de rapportage zowel op bericht- als op reisniveau toegankelijk. U moest tussen het lusje van de berichtuitvoering en het reisrapport navigeren.</p></td>
<td><img src="assets/inline-migration-after3.png"><p>Alle rapportages zijn nu gecentraliseerd op het niveau van de reis. Dit verbetert navigatie en gebruikerservaring. Als u meerdere e-mails onderweg hebt, kunt u de opdracht <strong>Handeling</strong> vervolgkeuzelijst om het verwante rapport weer te geven.
</p></td>
</tr>
</table>

Bij GA (25 juli) geldt deze nieuwe gebruikersstroom voor alle nieuwe reizen. De **Berichten** in de linkernavigatie niet meer beschikbaar is.

## Tijdlijn migratie{#iterations}

Een migratie is vereist om uw bestaande reizen om te zetten met **Berichten** in reizen met inline authored acties. Voor u wordt een automatische omzetting van reizen uitgevoerd. Toch hebben we uw hulp nodig met een paar stappen.

De migratie komt voor elk gebied bij nacht voor, door verscheidene herhalingen. Hier is de migratietijdlijn:

* 25 juli 2022: GA - 1e iteratie
* 1 augustus 2022: 2e herhaling
* 5 september 2022: 3e herhaling
* 6 september 2022: afkeer

Waarom hebben we meerdere herhalingen nodig?

Tijdens een herhaling gaan we elke reis door en migreren ze waar mogelijk. Er zijn gevallen waarin we niet automatisch willen migreren: wanneer de reis live of gesloten is (er kunnen nog profielen in staan). In deze gevallen vragen we je om een actie uit te voeren en dan zal de volgende herhaling deze reizen migreren die niet konden worden gemigreerd in vorige herhaling.

## Veelgestelde vragen {#faq}

### Hoe zal ik op de hoogte worden gesteld van deze wijziging?{#inform}

Adobe communiceert met u vóór de eerste herhaling.

De wijziging wordt &#39;s nachts geïmplementeerd, via verschillende herhalingen. Meer informatie over [herhalingen](../rn/inline-messages.md#inline-authoring).

U wordt ook op de hoogte gesteld van meldingen in het product, die worden weergegeven op de schermen Journalen:

* Voordat u de implementatie wijzigt

   ![](assets/inline-migration-banner1.png)

* Tijdens een herhaling

   ![](assets/inline-migration-banner2.png)

* Na een herhaling

   ![](assets/inline-migration-banner3.png)

   Na een herhaling **Status controleren** wordt weergegeven. Op deze manier kunt u al uw reizen bekijken in JSON-indeling en hun respectieve migratiestatus. Zie dit [sectie](../rn/inline-messages.md#status).

* Wanneer de banner verdwijnt, kunt u het beste gaan. U hoeft niets meer te doen.

### Wat is het migratieproces?{#process}

De migratie is volledig automatisch voor reizen die niet levend of gesloten zijn. We willen geen invloed uitoefenen op de rechtstreekse of gesloten reizen om te voorkomen dat de productie wordt beïnvloed. We vragen u de nieuwe versie te publiceren die we voor u hebben gemaakt.

Alle sandboxen van een ORG-klant worden tegelijkertijd verwerkt. Tijdens de veranderingsimplementatie, worden de volgende acties uitgevoerd:

**Elke reis zonder berichten**

Deze wijzigingen worden niet beïnvloed door de wijziging. Alleen reizen die berichten gebruiken, zijn het doelwit van de migratie. Nochtans, zult u tot berichten kunnen toegang hebben die niet in een reis via volgende URL worden gebruikt: https://experience.adobe.com/#/@[ORG]/naam:[SANDBOX]/transport-optimizer/messages/

**ONTWERP-reizen met behulp van ten minste één bericht**

Conceptversies van berichten worden tijdens de migratie gewijzigd. Ze verwijzen niet meer naar een bericht. De **Bericht** activiteiten worden vervangen door de passende kanaalactiviteiten. Elk van hen omvat de kanaalparameters en de inhoud.

Zoals gewoonlijk test u uw conceptreis voordat u deze publiceert.

**LIVE-reizen met ten minste één bericht**

De live versie van een reis wordt steeds opnieuw uitgevoerd om eventuele gevolgen voor de productie te voorkomen.

Tijdens de migratie wordt een nieuwe ontwerpversie van deze reis gemaakt. Deze nieuwe conceptversie is een kopie van uw live versie, maar berichten worden vervangen door inline authored channel-handelingen. Elke activiteit van de kanaalactie omvat de kanaalparameters en de inhoud. Inhoud gaat niet verloren. Rapportage gaat niet verloren.

We verwachten dat u deze conceptversie controleert, test en publiceert, zodat deze de live versie wordt.

**Voltooide of GESTOPT reizen met ten minste één bericht**

Deze reizen worden ook gemigreerd.

Wanneer het bekijken van het reisrapport, zijn de rapporten nu rijker en omvatten het niveau van informatie die eerder in berichtrapport beschikbaar was.

**GESLOTEN reizen met behulp van ten minste één bericht**

De gesloten versie van een reis blijft voor om het even welk profiel binnen lopen, om om het even welk effect van de productie te vermijden.

Gesloten reizen worden na 30 dagen automatisch overgeschakeld op de status &quot;Voltooid&quot;. Zij zullen in de volgende herhaling in aanmerking worden genomen, wanneer zij worden gebeëindigd.

**Meerkanaalsreizen**

Deze worden niet gemigreerd. Je moet ze opnieuw maken.

### Wat zijn mijn actiepunten als klant?{#actions}

U kunt de ritten automatisch omzetten, maar u hebt een paar stappen nodig. Meer informatie over de vereiste stappen in deze [page](../rn/inline-messages-steps.md).

<!--

The process timeline is indicated in a blue banner on the Journeys screen. See this [section](../rn/inline-messages.md#inform). 

**Before migration**

* Check the date indicated in the banner. 
* Stop non-critical journeys, on development, stage and production environments.
* If you have draft messages that you want to keep using, add them to a journey so they are migrated.

**During migration**

* Migration occurs at night-time
* Do not to create, edit or delete journeys.

**After migration**

* After each iteration, click the **Check status** button in the top banner. This page lists all journeys and their migration status. See this [section](../rn/inline-messages.md#status). 

* For each live journey, a new version is created. Review the new version, test it and publish it. 

* The **Messages** menu, in the left navigation is no longer available. You need to use the new in-line message feature. See this [section](../rn/inline-messages.md#change). 

* If you need to access a specific message which was not used in a journey, you can use this URL and save the content as a template: https://experience.adobe.com/#/@[ORG]/sname:[SANDBOX]/journey-optimizer/messages/

## How can I check the migration status?{#status}

Click the **Check status** button in the top banner. The following page is displayed.

![](assets/inline-migration-log.png)

The status report is at sandbox level. This report includes several useful sections:

**migrationStatus**

This section displays the migration information since the first iteration. Numbers are incremented after each iteration.

* MIGRATED: number of draft journeys migrated successfully.
* NEW_VERSION_CREATED: number of live journeys migrated. For each live journey, a new draft version is created: you must test and publish this version.
* ERROR: number of draft journeys not migrated because of a failure. You need to re-create them.
* ERROR_ON_NEW_VERSION_CREATION: number of live journeys not migrated because of a failure. new draft journey versions not migrated because of a failure. You need to re-create them.

**eligibilityStatus**

This section lists the remaining items after the last iteration:

* toMigrate: number of draft journeys that need to be migrated.
* createNewVersion: number of live journeys to migrate.
* noMigration_live: number of live journeys that do not need to be migrated
* noMigration: number of draft journeys that do not need to be migrated.

The **details** section gives, for each of the above indicators, the list of related journeys.

-->

### Hoe kan ik de migratiestatus controleren?{#status}

Klik op de knop **Status controleren** in de bovenste banner. De volgende pagina wordt weergegeven.

![](assets/inline-migration-log.png)

Het statusrapport bevindt zich op sandboxniveau. Dit rapport bevat verschillende nuttige secties:

**migrationStatus**

In deze sectie worden de migratiegegevens sinds de eerste herhaling weergegeven. De aantallen worden verhoogd na elke herhaling.

* GEMIGRATIEERD: aantal conceptreizen, voltooide en gestopt reizen is met succes gemigreerd.
* NEW_VERSION_CREATED: aantal gemigreerde levende reizen. Voor elke live reis wordt een nieuwe ontwerpversie gemaakt: u moet deze versie testen en publiceren.
* FOUT: aantal conceptuele, voltooide en gestopt reizen dat niet is gemigreerd vanwege een mislukking. U moet ze opnieuw maken.
* ERROR_ON_NEW_VERSION_CREATION: aantal niet-gemigreerde levende ritten als gevolg van een mislukking. nieuwe reisversies die niet zijn gemigreerd vanwege een fout. Er zijn geen nieuwe conceptversies voor gemaakt. U moet ze handmatig opnieuw maken.

**accessibilityStatus**

In deze sectie worden de resterende items na de laatste herhaling weergegeven:

* toMigrate: het aantal ritten voor concept-, voltooide en stilgelegde reizen dat moet worden gemigreerd.
* createNewVersion: aantal te migreren levende ritten.
* noMigration_live: het aantal levende ritten dat niet hoeft te worden gemigreerd. Hier worden ook afgesloten reizen vermeld.
* noMigration: aantal reizen dat niet hoeft te worden gemigreerd.

De **details** voor elk van de bovenstaande punten de lijst van de desbetreffende reizen.

### Zal deze verandering een onderbreking van de dienst veroorzaken?{#interruption}

De service wordt niet onderbroken.

* Op levende reizen: geen invloed , ze blijven actief .
* Op ritten zonder vergunning: tijdens de migratie (&#39;s nachts) raden we u ten zeerste aan geen reizen te maken, te bewerken of te verwijderen.

### Zullen er gegevens verloren gaan? {#data}

Er zullen geen gegevens verloren gaan en er zal geen invloed zijn op de live reizen. U hebt controle over het publiceren van bijgewerkte reisversies.

### Zullen er functionaliteiten verloren gaan?{#functionality}

De manier waarop u het bericht maakt, wordt gewijzigd. Er gaat geen functionaliteit verloren.

### Zal er tijdens het migratieproces toegang zijn tot het milieu?

Migratie vindt plaats &#39;s nachts. U kunt het product gebruiken. U moet echter geen reizen maken, bewerken of verwijderen.

### Zullen de berichten blijven worden verzonden?

Ja, er worden steeds meer rechtstreekse reizen gemaakt.

### Hoe weet ik dat de migratie voltooid is?

De migratie is voltooid wanneer de banner verdwijnt. Zie dit [sectie](../rn/inline-messages.md#inform).

### Hoe zullen de verwante toestemmingen van Berichten worden beïnvloed?

De functie voor inlineauteurs heeft invloed op machtigingen. Aan elk bericht gerelateerde machtigingen, zoals [!DNL View Messages] of [!DNL Manage Messages], worden automatisch opgenomen in de machtigingen die zijn gekoppeld aan de mogelijkheden voor reizen.

Meer informatie in deze [page](../administration/ootb-product-profiles.md).

<!--
* Improved authoring flow and navigation
* Personalization: improved contextual personalization flow
* Reporting: the message execution screen will no longer exist. Reporting is centralized in journeys.
* You will still be able to update content in a live journey.
->>
