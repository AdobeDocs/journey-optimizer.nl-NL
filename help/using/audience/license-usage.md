---
solution: Journey Optimizer
product: journey optimizer
title: Het gebruiksdashboard voor licenties
description: Meer informatie over het dashboard voor Journey Optimizer-licentiegebruik
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 7e91face-c8f4-4e70-9123-9e36bae7e67e
source-git-commit: db1e4ee5b2b4bb3a3d7d9e86aded14ad3c613765
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Het gebruiksdashboard voor licenties {#license-usage}

Het [!DNL Adobe Journey Optimizer] [ gebruikersinterface ](../start/user-interface.md) verstrekt een dashboard dat belangrijke informatie over het de vergunningsgebruik van uw organisatie toont, zoals die tijdens een dagelijkse momentopname wordt gevangen.

Ga naar **[!UICONTROL Administration]** > **[!UICONTROL License Usage]** om dit dashboard te openen. Hierdoor wordt het tabblad **[!UICONTROL Overview]** geopend, waarin het dashboard wordt weergegeven.

![ het dashboard van het gebruiksdashboard van de Vergunning ](assets/license-usage-dashboard.png)

>[!NOTE]
>
>* Om het dashboard te bekijken, moet u de [ toestemming hebben van het Gebruik Dashboard van het Gebruik van de Vergunning van 0} Mening.](https://experienceleague.adobe.com/docs/experience-platform/dashboards/permissions.html#available-permissions){target="_blank"}
>
>* Bepaalde metriek (bijvoorbeeld computeruren, e-mails) worden niet weergegeven voor ontwikkelingssandboxen, zoals aangegeven door `N/A` in de quotakolom. Alleen waarden die niet &#39;null&#39; zijn, worden weergegeven in het dashboard: als de waarden nul of dicht bij nul zijn, worden ze niet gevuld.


Voor [!DNL Adobe Journey Optimizer], staat het dashboard u toe om het aantal **toe te laten Profielen** te controleren.

## Wat is een Engageable Profiel? {#what-is-engageable-profile}

Een **Engageable Profiel** is een verslag van informatie die een individu vertegenwoordigt dat in de Dienst van het Profiel wordt opgeslagen en door reizen of campagnes is geëngageerd.

Belangrijkste kenmerken van Inschakelbare profielen:

* **12 maanden het rollen venster**: De toe te laten Profielen worden geteld gebaseerd op overeenkomst over de afgelopen 12 maanden. Deze metrisch toont het aantal unieke profielen u met het gebruiken van het schrijven van Journey Optimizer, het besluit, levering, het experimenteren, of orchestration mogelijkheden hebt geprobeerd in dienst te nemen.

* **Unieke telling per zandbak**: Als een profiel veelvoudige reizen of campagnes binnen een zandbak ingaat, wordt het slechts eenmaal geteld als één enkel Engageable Profiel voor die zandbak.

* **Gebaseerd op Adresseerbare Publiek**: De toe te laten Profielen worden berekend van uw Adresseerbare Publiek. De telling vertegenwoordigt het publiek betrokken in de afgelopen 12 maanden gebruikend om het even welk van Journey Optimizer mogelijkheden, van uw totaal Adresseerbare Publiek.

* **Metrisch gedrag**: De toe te voegen Aantal Profielen:
   * Kan toenemen wanneer nieuwe profielen worden gebruikt voor reizen of campagnes
   * Kan niet verkleinen tenzij er gedurende meer dan 12 maanden geen verbinding is met bepaalde profielen
   * Kan verminderen wanneer pseudoniem-profielen worden gekoppeld aan bekende profielen

>[!NOTE]
>
>Als u een plotselinge piek in uw Engageable Aantal Profielen waarneemt, verwijs naar de [ sectie van het Oplossen van problemen ](#troubleshooting-engageable-profiles) hieronder voor gedetailleerde begeleiding bij het begrijpen van en het oplossen van de kwestie.

## Problemen oplossen: aanzienlijke toename van het aantal inschrijfbare profielen {#troubleshooting-engageable-profiles}

Als u een plotselinge piek in het Engageable Aantal Profielen (bijvoorbeeld, stijgend profielen van honderdduizenden aan miljoenen binnen een dag) opmerkt, verstrekt deze sectie begeleiding om de kwestie te begrijpen en te behandelen.

### De verhoging begrijpen

De metrische waarde van Engageable Profiles geeft het aantal unieke profielen weer dat de afgelopen twaalf maanden door reizen of campagnes is gebruikt. Een plotselinge toename kan het gevolg zijn van:

* Grote doelgroepen van nieuwe reizen of campagnes
* Wijzigingen in gegevenssets die zijn ingeschakeld voor de profielservice
* Batchverwerking van publiek dat zich de laatste tijd niet heeft beziggehouden

### Oplossingsstappen

Ga als volgt te werk om dit probleem op te lossen:

1. **Begrijp profiel het tellen logica:**

   * Betrokkene profielen worden berekend op basis van unieke profielen die de afgelopen twaalf maanden zijn gebruikt tijdens reizen of campagnes.
   * Als een profiel meerdere reizen binnengaat, wordt het geteld als één Engageable Profiel voor die zandbak.
   * De waarde kan alleen dalen als bepaalde profielen gedurende meer dan 12 maanden niet worden gebruikt of als aan bekende profielen pseudoniem worden gehecht.
   * Engageable Profielen worden berekend gebruikend het Adresseerbare Publiek van een klant.
   * Het publiek dat in de afgelopen 12 maanden gebruikmaakte van om het even welke mogelijkheden van Journey Optimizer, van het totale Adresseerbare Publiek, bepaalt de telling van toe te laten Profielen.

2. **onderzoekt reizen, campagnes en het besluit gericht op grote publiek:**

   * Herzie recente reizen en campagnes richtend grote aantallen profielen gebruikend [ toe te laten vragen van Profielen ](../reports/query-examples.md#engageable-profiles-queries) of [ de Dienst van de Vraag ](https://experienceleague.adobe.com/en/docs/experience-platform/query/home){target="_blank"}.
   * Identificeer specifieke reisversies die tot de spike in profieltellingen bijdroegen.
   * Reizen, campagnes en besluitvorming met betrekking tot nieuwe profielen zullen waarschijnlijk leiden tot een toename van het aantal gebeurtenissen in de gegevensbestanden voor reizen, wat zal bijdragen aan de toename van het aantal Engageable Profiles.

3. **het publiek van de Filter op reis en campagnereniveau:**

   * Pas filters toe op het niveau van de doelgroep voordat u reizen of campagnes start om onnodige toenamen in Ingageable Profiles te voorkomen.
   * Ervoor zorgen dat alleen relevante doelgroepen tijdens de uitvoering van contracten worden aangewezen.

4. **Verminder adresseerbare publieksgrootte:**

   * Verwijder indien nodig pseudoniem-profielen. Deze actie is van invloed op zowel Journey Optimizer als Real-Time Customer Data Platform.
   * Leer meer over [ Pseudoniem de gegevensvervaldatum van het Profiel ](https://experienceleague.adobe.com/en/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"} in de Gids van het Profiel van de Klant in real time.
   * **Nota:** de Pseudoniem gegevensvervalsing van het Profiel kan niet door het Platform UI of APIs worden gevormd. U moet contact opnemen met de ondersteuningsafdeling om deze functie in te schakelen.

5. {de veranderingen van de 0} dataset van de Monitor:****

   * Verifieer datasets die voor het profileren worden toegelaten en zorg ervoor zij geen bovenmatige ECIDs (Experience Cloud IDs) bevatten.
   * Indien nodig, schrapt datasets met hoge aantallen ECID en ontspant hen met verminderde verslagen.

6. **ontwikkelt een strategie van de lange-termijnvermindering:**

   * Het aantal inschrijfbare profielen neemt natuurlijk af als bepaalde profielen langer dan twaalf maanden niet zijn ingeschakeld.

**zie ook:**

* [ Ingageable de vraagvoorbeelden van Profielen ](../reports/query-examples.md#engageable-profiles-queries) - de vragen van de steekproef om uw Ingageable Profielen te controleren en te analyseren
* [ overzicht van de Dienst van de Vraag van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/query/home){target="_blank"}

## Gerelateerde documentatie {#related-documentation}

Meer informatie vindt u in de documentatie van Adobe Experience Platform:

* [ het dashboard van het gebruiksdashboard van de Vergunning ](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html){target="_blank"}
* [ het onderzoeken van het dashboard van het vergunningsgebruik ](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html#exploring-the-license-usage-dashboard){target="_blank"}
* [ Beschikbare metriek ](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html#available-metrics){target="_blank"}
* [ Pseudoniem de gegevensvervalsing van het Profiel ](https://experienceleague.adobe.com/docs/experience-platform/profile/pseudonymous-profiles.html){target="_blank"}
