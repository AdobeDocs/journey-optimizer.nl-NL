---
solution: Journey Optimizer
product: journey optimizer
title: Reisrapport
description: Leer hoe u pushberichtgegevens uit het reisrapport kunt gebruiken
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 6d4b7669-7852-42f0-9347-399a3994011f
source-git-commit: 7945ab9369498f23685aa2f727542c7367c2d830
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Reizigersrapport {#journey-global-report}

>[!BEGINSHADEBOX]

U hebt toegang tot het rapport van de pushmelding door op de knop **[!UICONTROL View report]** te klikken tijdens de reis. [Meer informatie](report-gs-cja.md)

![](assets/report-access-jo.png)

>[!ENDSHADEBOX]

## Verzendstatistieken {#sending-statistics-push}

![](assets/cja-campaign-push-sending-stat.png)

De tabel **[!UICONTROL Sending Statistics]** helpt u te begrijpen hoe uw pushmeldingen worden uitgevoerd. Het omvat belangrijke metriek zoals leverings tarief en publieksgrootte, die u waardevolle inzichten in de doeltreffendheid en het bereik van uw reizen geven.

+++ Meer informatie over het verzenden van statistieken

* **[!UICONTROL People]**: Aantal gebruikersprofielen dat in aanmerking komt als doelprofielen voor uw SMS-berichten.

* **[!UICONTROL Targeted]**: Aantal profielen dat in aanmerking kwam voor het publiek voordat uitsluitingen, onderdrukkingen of toestemmingsverwijderingen werden toegepast. Bij ritten waarbij terugkeer is ingeschakeld, kan een profiel meerdere keren worden aangewezen.

* **[!UICONTROL Sends]**: Het totale aantal verzendingen voor de pushmelding.

* **[!UICONTROL Delivered]**: Het aantal pushmeldingen dat is verzonden, in verhouding tot het totale aantal verzonden pushmeldingen.

* **[!UICONTROL Bounces for outbound channels]**: het totaal aan fouten dat tijdens het verzendproces is gecumuleerd en de automatische retourverwerking in verhouding tot het totale aantal pushmeldingen.

* **[!UICONTROL Outbound errors]**: het totale aantal fouten dat is opgetreden om te voorkomen dat deze naar profielen werd verzonden.

* **[!UICONTROL Outbound exclusions]**: aantal profielen dat door Adobe Journey Optimizer is uitgesloten.

+++

## Trackingstatistieken {#tracking-statistics-push}

![](assets/cja-campaign-push-track-stat.png)

De tabel van **[!UICONTROL Tracking statistics]** biedt een gedetailleerde momentopname van profielactiviteiten die aan uw pushmeldingen zijn gekoppeld, die essentiële inzichten in de doeltreffendheid van betrokkenheid en pushmeldingen biedt.

+++ Meer informatie over statistieken bijhouden

* **[!UICONTROL Click through rate (CTR)]**: percentage gebruikers dat interactie had met de pushmelding.

* **[!UICONTROL Clickthrough open rate (CTOR)]**: Het aantal keren dat de pushmelding is geopend.

* **[!UICONTROL Clicks]**: Het aantal keer dat er op de inhoud is geklikt in de pushmelding.

* **[!UICONTROL Unique Clicks]**: Aantal profielen dat op een inhoud in uw pushmelding heeft geklikt.

* **[!UICONTROL Push custom actions]**: aantal aangepaste acties die door profielen zijn uitgevoerd als reactie op de pushberichten.
+++

## Labels voor bijgehouden koppelingen {#track-link-label-push}

![](assets/cja-campaign-push-link-labels.png)

De tabel **[!UICONTROL Tracked link labels]** bevat een uitgebreid overzicht van de koppelingslabels in uw pushberichten, waarin de labels worden gemarkeerd die het hoogste bezoekersverkeer genereren. Met deze functie kunt u de populairste koppelingen identificeren en er prioriteiten aan stellen.

+++ Meer informatie over metriek van tracklabels

* **[!UICONTROL Unique Clicks]**: Aantal profielen dat op een inhoud in uw pushberichten heeft geklikt.

* **[!UICONTROL Clicks]**: Het aantal keer dat er op de inhoud is geklikt in uw pushberichten.

+++

## URL&#39;s van bijgehouden koppeling {#track-link-url-push}

![](assets/cja-campaign-push-link-urls.png)

De tabel **[!UICONTROL Tracked link URLs]** bevat een uitgebreid overzicht van de URL&#39;s in uw pushberichten die het hoogste bezoekersverkeer aantrekken. Hierdoor kunt u de populairste koppelingen identificeren en er prioriteiten aan stellen, zodat u meer inzicht krijgt in de betrokkenheid bij profielen met specifieke inhoud in uw pushberichten.

+++ Meer informatie over URL&#39;s met gekoppelde koppelingen

* **[!UICONTROL Unique Clicks]**: Aantal profielen dat op een inhoud in uw pushberichten heeft geklikt.

* **[!UICONTROL Clicks]**: Het aantal keer dat er op de inhoud is geklikt in uw pushberichten.

+++

## Stuitingsredenen {#bounce-reasons-push}

De tabel van **[!UICONTROL Bounces Reasons]** biedt een uitgebreid overzicht van gegevens met betrekking tot gepushte pushberichten, waarmee u waardevolle inzichten krijgt over de specifieke redenen voor het wegvallen van pushberichten.

## Foutredenen {#error-reasons-push}

In de tabel **[!UICONTROL Error Reasons]** kunt u de specifieke fouten identificeren die zijn opgetreden tijdens het verzenden van uw pushberichten. Zo kunt u een grondige analyse van alle ondervonden problemen mogelijk maken.

## Uitgesloten redenen {#exclude-reasons-push}

![](assets/cja-campaign-push-excluded.png)

In de tabel **[!UICONTROL Exclude Reasons]** worden visueel de verschillende factoren weergegeven die ertoe hebben geleid dat gebruikersprofielen zijn uitgesloten van het doelpubliek, zodat gebruikers uw pushberichten niet kunnen ontvangen.

Verwijs naar [&#x200B; deze pagina &#x200B;](exclusion-list.md) voor de uitvoerige lijst van uitsluitingsredenen.
