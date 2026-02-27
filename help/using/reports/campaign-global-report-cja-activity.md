---
solution: Journey Optimizer
product: journey optimizer
title: Rapport Campagne Live-activiteit
description: Meer informatie over het gebruik van live-activiteitsgegevens in het campagnerapport
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 58034ec4-62dc-406c-99c4-d6b7aa107140
source-git-commit: 17f86c33f56b9855fa1d0f959aac8740ff2c2c2a
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---

# Rapport voor live-activiteitencampagne {#campaign-global-report-cja-activity}

>[!BEGINSHADEBOX]

U kunt het campagnerapport voor Live-activiteiten openen door in uw campagne op de knop **[!UICONTROL Reports]** te klikken en vervolgens **[!UICONTROL View all time report]** te selecteren. [Meer informatie](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Verzendstatistieken {#sending-statistics-mobile}

![](assets/sending-statistics-mobile-live.png)

De tabel **[!UICONTROL Sending Statistics]** bevat een gedetailleerd overzicht van de belangrijkste metriek voor uw Live-activiteiten-campagne. Het toont essentiële informatie zoals de grootte van het doelpubliek en het aantal met succes geleverde levende activiteit, die u helpen het algemene bereik en de prestaties van uw levende activiteit beoordelen.

+++ Meer informatie over het verzenden van statistieken

* **[!UICONTROL Targeted]**: Aantal profielen dat in aanmerking kwam voor het publiek voordat uitsluitingen, onderdrukkingen of toestemmingsverwijderingen werden toegepast.

* **[!UICONTROL Sends]**: Het totale aantal gebeurtenissen met betrekking tot live activiteiten dat naar doelprofielen is verzonden.

* **[!UICONTROL Delivered]**: Aantal gebeurtenissen met live-activiteit dat aan apparaten is geleverd, in verhouding tot het totale aantal pogingen dat is gedaan.

* **[!UICONTROL Send errors]**: Het totale aantal gebeurtenissen met betrekking tot live activiteiten dat niet kan worden verzonden vanwege fouten (bijvoorbeeld ongeldige tokens of connectiviteitsproblemen).

* **[!UICONTROL Send exclusions]**: aantal profielen dat door Adobe Journey Optimizer is uitgesloten van verzending (bijvoorbeeld vanwege de status van niet-deelname of de subsidiabiliteitsregels).

+++

## Levende levenscyclus van activiteiten {#lifecycle}

De tabel **[!UICONTROL Live activity lifecycle]** biedt een uitgebreide weergave van de voortgang van uw Live-activiteiten in de loop van de tijd. Het biedt zichtbaarheid in belangrijke gebeurtenissen, zoals wanneer de activiteit wordt gestart, bijgewerkt of beëindigd, zodat u een beter inzicht hebt in de betrokkenheid van gebruikers en de algemene levenscyclus van uw actieve-activiteitscampagne.

De rapportage is afhankelijk van of u transactiecampagnes of marketingcampagnes gebruikt.

### Transactionele Live-activiteit

![](assets/activity-lifecycle.png)

Voor de Transactionele campagne, toont het Levende campagnerapport van de Activiteiten alle levenscyclusgebeurtenissen met inbegrip van verre begin, lokale begin, updates, en einden.

+++ Meer informatie over levenscyclusmetriek van Live-activiteit met Transactiecampagnes

* **[!UICONTROL Remote starts]**: Het totale aantal livegebeurtenissen dat op afstand wordt gestart en doorgaans wordt geactiveerd door de server of de back-endsystemen.

* **[!UICONTROL Local starts]**: Het totale aantal Live-activiteiten dat lokaal op het apparaat van de gebruiker wordt gestart, vaak als gevolg van gebruikersinteractie of triggers aan de clientzijde.

* **[!UICONTROL Updates]**: Het totale aantal updates van Live-activiteit dat naar apparaten wordt verzonden. Updates kunnen statuswijzigingen, nieuwe inhoud of voortgangsmeldingen bevatten.

* **[!UICONTROL Ends]**: Het totale aantal beëindigingsgebeurtenissen van Live-activiteit dat naar apparaten wordt verzonden.

* **[!UICONTROL Totals count]**: totaal van alle Live activity life-levenscyclusgebeurtenissen, inclusief het starten, bijwerken en beëindigen van de levenscyclus, voor een volledige maat van het volume van de live activiteit.

+++

### Actieve marketingactiviteit

![](assets/activity-lifecycle-broadcast.png)

Marketingcampagnes gebruiken Live-activiteit voor het gebruik van uitzendingen, waarbij updates tegelijkertijd naar meerdere apparaten worden verzonden.

Voor iOS Live-activiteiten in marketingcampagnes geeft het rapport alleen **[!UICONTROL Remote Starts]** -gebeurtenissen en **[!UICONTROL Remote starts errors]** aan het begin weer. **[!UICONTROL Updates]** - en **[!UICONTROL Ends]** -gebeurtenissen worden niet bijgehouden, omdat APNs updates naar alle apparaten distribueert zonder feedback te geven. Om **[!UICONTROL Updates]** en **[!UICONTROL Ends]** gebeurtenissen te bekijken, gebruik [ de console van het Bericht van de Duw van Apple ](https://developer.apple.com/notifications/push-notifications-console/).

+++ Meer informatie over levenscyclusmetriek tijdens de levenscyclus van live activiteiten met marketingcampagnes

* **[!UICONTROL Remote starts]**: Het totale aantal livegebeurtenissen dat op afstand wordt gestart en doorgaans wordt geactiveerd door de server of de back-endsystemen.

* **[!UICONTROL Remote starts errors]**: Het totale aantal fouten dat is opgetreden bij een poging om Live-activiteiten op afstand te starten (bijvoorbeeld ongeldige tokens of connectiviteitsproblemen).

+++

#### Updates en eindversies ophalen via API {#retrieving-updates-end-api}

Als alternatief voor het gebruiken van de console van het Bericht van de Duw van Apple, kunnen de Updates en de tellingen van het Eind door hoofd-API vraag worden verkregen.

Wanneer het uitvoeren van update of eind API vraag voor uitzendingsgebruiksgevallen, omvat de reactie een `controlBreakdown` sectie die tellers erop wijst die wijzen die hoeveel update en eindvraag voor de levende activiteitenuitvoering werden uitgevoerd. Dit blok is niet beschikbaar voor oudere uitvoeringen zonder levenscyclusgegevens. De status van de uitvoering kan ook uitdrukkelijk worden teruggewonnen gebruikend het eindpunt van GET wanneer nodig.

**UPDATE/EIND Reactie (200 OK)**

```json
{
  "executionId": "HA-exec-abc",
  "campaignId": "campaign-abc-123",
  "campaignVersionId": "v1",
  "audienceId": "audience-segment-id",
  "status": "processing",
  "targetedProfileCount": 150000,
  "createdAt": "2026-02-27T10:00:00Z",
  "executionLifecycle": {
    "lastControlAt": "2026-02-27T10:45:00Z",
    "controlBreakdown": {
      "update": 5,
      "end": 1
    }
  }
}
```

**Status van de Uitvoering (GET)**

```
GET /im/executions/audience/{executionId}
```

## Foutredenen {#error-reasons}

![](assets/error-reasons-activity.png)

In de tabel **[!UICONTROL Error Reasons]** kunt u de specifieke fouten identificeren die zijn opgetreden tijdens het verzendproces van uw Live-activiteiten. Zo kunt u een grondige analyse van alle ondervonden problemen mogelijk maken.

## Uitgesloten redenen {#excluded-reasons}

![](assets/excluded-activity.png)

In de tabel **[!UICONTROL Excluded Reasons]** worden visueel de verschillende factoren weergegeven die ertoe hebben geleid dat gebruikersprofielen zijn uitgesloten van het doelpubliek, zodat gebruikers uw Live-activiteit niet kunnen ontvangen.
