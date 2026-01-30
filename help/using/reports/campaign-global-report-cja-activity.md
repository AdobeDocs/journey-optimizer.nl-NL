---
solution: Journey Optimizer
product: journey optimizer
title: Campagnerapport
description: Meer informatie over het gebruik van live-activiteitsgegevens in het campagnerapport
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 7945ab9369498f23685aa2f727542c7367c2d830
workflow-type: tm+mt
source-wordcount: '378'
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

![](assets/activity-lifecycle.png)

De tabel **[!UICONTROL Live activity lifecycle]** biedt een uitgebreide weergave van de voortgang van uw Live-activiteiten in de loop van de tijd. Het biedt zichtbaarheid in belangrijke gebeurtenissen, zoals wanneer activiteiten worden gestart, bijgewerkt of beëindigd, zodat u een beter inzicht hebt in de betrokkenheid van gebruikers en in de algemene levenscyclus van uw Live-activiteitencampagnes.

+++ Meer informatie over levenscyclusmetriek van Live-activiteit

* **[!UICONTROL Remote starts]**: Aantal Live-activiteiten dat extern wordt gestart, doorgaans geactiveerd door de server of het back-end systeem.

* **[!UICONTROL Local starts]**: Het aantal Live-activiteiten dat lokaal op het apparaat van een gebruiker is gestart, is vaak het gevolg van gebruikersinteractie of triggers aan de clientzijde.

**[!UICONTROL Updates]**: Het totale aantal updates van Live-activiteit dat naar apparaten wordt verzonden. Updates kunnen statuswijzigingen, nieuwe inhoud of voortgangsmeldingen bevatten.

**[!UICONTROL Ends]**: Aantal Live-activiteiten dat is beëindigd, automatisch na voltooiing of handmatig via een gedefinieerde trigger of time-out.

**[!UICONTROL Totals count]**: totaal van alle Live activity life-levenscyclusgebeurtenissen, inclusief het starten, bijwerken en beëindigen van de levenscyclus, voor een volledige maat van het volume van de live activiteit.

+++

## Foutredenen {#error-reasons}

![](assets/error-reasons-activity.png)

In de tabel **[!UICONTROL Error Reasons]** kunt u de specifieke fouten identificeren die zijn opgetreden tijdens het verzendproces van uw Live-activiteiten. Zo kunt u een grondige analyse van alle ondervonden problemen mogelijk maken.

## Uitgesloten redenen {#excluded-reasons}

![](assets/excluded-activity.png)

In de tabel **[!UICONTROL Excluded Reasons]** worden visueel de verschillende factoren weergegeven die ertoe hebben geleid dat gebruikersprofielen zijn uitgesloten van het doelpubliek, zodat gebruikers uw Live-activiteit niet kunnen ontvangen.
