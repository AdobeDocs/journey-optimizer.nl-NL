---
solution: Journey Optimizer
product: journey optimizer
title: Campagnerapport
description: Meer informatie over het gebruik van live-activiteitsgegevens in het campagnerapport
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 58034ec4-62dc-406c-99c4-d6b7aa107140
source-git-commit: 6b4e3a6c32d24861f1ea8df54fc2e4fbb19d0ce7
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Rapport voor live-activiteitencampagne {#campaign-global-report-cja-activity}

>[!BEGINSHADEBOX]

U kunt het campagnerapport voor Live-activiteiten openen door in uw campagne op de knop **[!UICONTROL Reports]** te klikken en vervolgens **[!UICONTROL View all time report]** te selecteren. [Meer informatie](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Verzendstatistieken {#sending-statistics-mobile}

![](assets/sending-statistics-mobile-live.png)

De tabel **[!UICONTROL Sending Statistics]** bevat een gedetailleerd overzicht van de belangrijkste meetgegevens voor live-activiteitencampagnes. Het bevat essentiële informatie zoals de grootte van het doelpubliek en het aantal pushmeldingen dat succesvol is geleverd, zodat u het algemene bereik en de prestaties van uw live pushberichten kunt beoordelen.

+++ Meer informatie over het verzenden van statistieken

* **[!UICONTROL Targeted]**: Aantal profielen dat in aanmerking kwam voor het publiek voordat uitsluitingen, onderdrukkingen of toestemmingsverwijderingen werden toegepast.

* **[!UICONTROL Sends]**: Het totale aantal pushmeldingen dat is verzonden naar doelprofielen.

* **[!UICONTROL Delivered]**: Het aantal pushmeldingen dat naar apparaten is verzonden, in verhouding tot het totale aantal pogingen dat is verzonden.

* **[!UICONTROL Send errors]**: Het totale aantal pushmeldingen dat niet kon worden verzonden vanwege fouten (bijvoorbeeld ongeldige tokens of connectiviteitsproblemen).

* **[!UICONTROL Send exclusions]**: aantal profielen dat door Adobe Journey Optimizer is uitgesloten van verzending (bijvoorbeeld vanwege de status van niet-deelname of de subsidiabiliteitsregels).

+++

## Levende levenscyclus van activiteiten {#lifecycle}

De tabel **[!UICONTROL Live activity lifecycle]** biedt een uitgebreide weergave van de voortgang van uw Live-activiteiten in de loop van de tijd. Het biedt zichtbaarheid in belangrijke gebeurtenissen, zoals wanneer activiteiten worden gestart, bijgewerkt of beëindigd, zodat u een beter inzicht hebt in de betrokkenheid van gebruikers en in de algemene levenscyclus van uw Live-activiteitencampagnes.

De rapportage is afhankelijk van of u transactiecampagnes of marketingcampagnes gebruikt.

### Transactionele Live-activiteiten

![](assets/activity-lifecycle.png)

Voor de Transactionele campagne, toont het Levende campagnerapport van Activiteiten alle levenscyclusgebeurtenissen met inbegrip van verre begin, lokale begin, updates, en einden.

+++ Meer informatie over levenscyclusmetriek van Live-activiteit met Transactiecampagnes

* **[!UICONTROL Remote starts]**: Het totale aantal Live-activiteiten start gebeurtenissen die op afstand worden gestart, doorgaans geactiveerd door de server of de back-endsystemen.

* **[!UICONTROL Local starts]**: Het totale aantal Live-activiteiten start gebeurtenissen die lokaal op het apparaat van de gebruiker worden gestart, vaak als gevolg van gebruikersinteractie of triggers aan de clientzijde.

* **[!UICONTROL Updates]**: Het totale aantal updates van Live-activiteit dat naar apparaten wordt verzonden. Updates kunnen statuswijzigingen, nieuwe inhoud of voortgangsmeldingen bevatten.

* **[!UICONTROL Ends]**: Het totale aantal Live-activiteiten dat naar apparaten wordt verzonden.

* **[!UICONTROL Totals count]**: totaal van alle Live activity life-levenscyclusgebeurtenissen, inclusief het starten, bijwerken en beëindigen van de levenscyclus, voor een volledige maat van het volume van de live activiteit.

+++

### Handelsactiviteiten

![](assets/activity-lifecycle-broadcast.png)

Marketingcampagnes gebruiken Live-activiteiten voor het gebruik van uitzendingen, waarbij updates tegelijkertijd naar meerdere apparaten worden verzonden.

Voor iOS Live-activiteiten in marketingcampagnes geeft het rapport alleen **[!UICONTROL Remote Starts]** -gebeurtenissen en **[!UICONTROL Remote starts errors]** aan het begin weer. **[!UICONTROL Updates]** - en **[!UICONTROL Ends]** -gebeurtenissen worden niet bijgehouden, omdat APNs updates naar alle apparaten distribueert zonder feedback te geven. Om **[!UICONTROL Updates]** en **[!UICONTROL Ends]** gebeurtenissen te bekijken, gebruik [&#x200B; de console van het Bericht van de Duw van Apple &#x200B;](https://developer.apple.com/notifications/push-notifications-console/).

+++ Meer informatie over levenscyclusmetriek tijdens de levenscyclus van live activiteiten met marketingcampagnes

* **[!UICONTROL Remote starts]**: Het totale aantal Live-activiteiten start gebeurtenissen die op afstand worden gestart, doorgaans geactiveerd door de server of de back-endsystemen.

* **[!UICONTROL Remote starts errors]**: Het totale aantal fouten dat is opgetreden bij een poging om Live-activiteiten op afstand te starten (bijvoorbeeld ongeldige tokens of connectiviteitsproblemen).

+++

## Foutredenen {#error-reasons}

![](assets/error-reasons-activity.png)

In de tabel **[!UICONTROL Error Reasons]** kunt u de specifieke fouten identificeren die zijn opgetreden tijdens het verzendproces van uw Live-activiteiten. Zo kunt u een grondige analyse van alle ondervonden problemen mogelijk maken.

## Uitgesloten redenen {#excluded-reasons}

![](assets/excluded-activity.png)

In de tabel **[!UICONTROL Excluded Reasons]** worden visueel de verschillende factoren weergegeven die ertoe hebben geleid dat gebruikersprofielen zijn uitgesloten van het doelpubliek, zodat gebruikers uw Live-activiteit niet kunnen ontvangen.
