---
solution: Journey Optimizer
product: journey optimizer
title: Reisrapport
description: Leer hoe u e-mailgegevens uit het reisrapport kunt gebruiken
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 82558447-9d42-4fac-8fc1-fded9bf4bfcc
source-git-commit: 7945ab9369498f23685aa2f727542c7367c2d830
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# E-mailreisrapport {#journey-global-report}

>[!INFO]
>
>Aangezien Apple nieuwe privacybeschermingsfuncties heeft geïntroduceerd voor de native e-mailtoepassing, waaronder Mail Privacy Protection, kunnen afzenders geen pixels voor het bijhouden van gegevens meer gebruiken om gegevens te verzamelen over profielen die de bescherming van de privacy van Apple-mail hebben ingeschakeld. Het is dan ook mogelijk dat de mogelijkheid van Adobe Journey Optimizer om e-mailberichten te volgen met behulp van trackingpixels wordt beïnvloed.
> [Meer informatie &#x200B;](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-classic-blogs/the-impact-of-apple-ios-privacy-changes-on-email-marketing-and/ba-p/699780) over de invloed van privacywijzigingen in Apple iOS op e-mailmarketing.
> 
> We raden u aan de focus op kliks en conversiemetriek te richten in plaats van op open koersen voor nauwkeurigere inzichten.

>[!BEGINSHADEBOX]

U kunt uw rapport over de e-mailreis openen door op de knop **[!UICONTROL View report]** te klikken. [Meer informatie](report-gs-cja.md)

![](assets/report-access-jo.png)

>[!ENDSHADEBOX]

## Geleverde versus klik trend {#delivered-click}

![](assets/cja-journey-email-delivered.png)

In de grafiek van **[!UICONTROL Delivered vs Click trend]** wordt een gedetailleerde analyse gegeven van de betrokkenheid van uw profielen bij uw e-mails. Deze grafiek biedt waardevolle inzichten in de interactie tussen verschillende domeinen en uw inhoud.

+++ Meer informatie over cijfers voor trends in geleverd en klik op trend

* **[!UICONTROL Delivered]**: Aantal verzonden e-mailberichten in verhouding tot het totale aantal verzonden e-mails.

* **[!UICONTROL Clicks]**: Het aantal keer dat er op de inhoud in uw e-mails is geklikt.

+++

## Leveringsstatus {#delivery-status}

![](assets/cja-journey-email-delivery-stat.png)

In de grafiek van **[!UICONTROL Delivery status]** kunt u in één oogopslag zien hoe uw e-mails werken. Houd belangrijke metriek bij, zoals leveringen en golven, zodat u snel inzicht hebt in de efficiëntie van uw e-mailreis.

+++ Meer informatie over de metriek van de leveringsstatus

* **[!UICONTROL Delivered]**: Aantal verzonden e-mailberichten in verhouding tot het totale aantal verzonden e-mails.

* **[!UICONTROL Bounces for outbound channels]**: het totaal aan fouten dat tijdens het verzendproces is gecumuleerd en de automatische retourverwerking in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Outbound errors]**: het totale aantal fouten dat is opgetreden tijdens het verzendingsproces waardoor het niet naar profielen kan worden verzonden.

* **[!UICONTROL Excluded]**: aantal profielen dat door Adobe Journey Optimizer is uitgesloten.

+++

## Verzendstatistieken {#email-sending-statistics}

![](assets/cja-journey-email-sending-stat.png)

De tabel **[!UICONTROL Sending Statistics]** geeft een duidelijk overzicht van de manier waarop uw e-mails tijdens uw reizen worden uitgevoerd. Het volgt belangrijke metriek zoals leveringstarieven en interactie, die u waardevolle inzichten geven om uw e-mailstrategie voor betere bereik en betrokkenheid te optimaliseren.

+++ Meer informatie over het verzenden van statistieken

* **[!UICONTROL Targeted]**: Aantal profielen dat in aanmerking kwam voor het publiek voordat uitsluitingen, onderdrukkingen of toestemmingsverwijderingen werden toegepast. Bij ritten waarbij terugkeer is ingeschakeld, kan een profiel meerdere keren worden aangewezen.

* **[!UICONTROL Sends]**: Het totale aantal verzendingen voor uw e-mail.

* **[!UICONTROL Delivered]**: Aantal verzonden e-mailberichten in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Unique Delivered]**: Aantal profielen dat ten minste één e-mail heeft ontvangen.

* **[!UICONTROL Bounces for outbound channels]**: het totaal aan fouten dat tijdens het verzendproces is gecumuleerd en de automatische retourverwerking in verhouding tot het totale aantal verzonden berichten.

* **[!UICONTROL Outbound Errors]**: het totale aantal fouten dat is opgetreden tijdens het verzendproces waardoor het niet naar profielen kan worden verzonden.

* **[!UICONTROL Outbound Exclusions]**: aantal profielen dat door Adobe Journey Optimizer is uitgesloten.

+++

## E-mail - Trackingstatistieken {#email-tracking}

![](assets/cja-journey-email-track-stat.png)

De tabel **[!UICONTROL Email - Tracking statistics]** bevat een gedetailleerd overzicht van de profielactiviteiten met betrekking tot e-mails die u onderweg hebt. Dit omvat cijfers over het openen, klikken en andere relevante betrokkenheidsindicatoren, die een uitgebreid overzicht bieden van hoe profielen met uw e-mailinhoud communiceren.

+++ Meer informatie over statistieken bijhouden

* **[!UICONTROL Click through rate (CTR)]**: percentage gebruikers dat interactie heeft gehad met het e-mailbericht.

* **[!UICONTROL Click through open rate (CTOR)]**: Het aantal keren dat de e-mail is geopend.

* **[!UICONTROL Clicks]**: Het aantal keer dat er op de inhoud in uw e-mails is geklikt.

* **[!UICONTROL Unique Clicks]**: Aantal profielen dat op de inhoud van een e-mail heeft geklikt.

* **[!UICONTROL Email Opens]**: Het aantal keren dat uw e-mails zijn geopend in een campagne.

* **[!UICONTROL Unique Email Opens]**: Aantal profielen dat e-mailberichten heeft geopend.

* **[!UICONTROL Spam complaints]**: Het aantal keren dat een bericht is gedeclareerd als spam of junk.

* **[!UICONTROL Unsubscribes]**: Het aantal klikken op de koppeling voor het opzeggen van abonnementen.

* **[!UICONTROL Unique Email Unsubscribes]**: aantal profielen dat zich niet meer heeft geabonneerd op uw e-mails.
+++

## E-maildomeinen {#email-domains}

![](assets/cja-email-email-domains.png)

De tabel van **[!UICONTROL Email Domains]** bevat een diepgaande uitsplitsing van e-mails die zijn gecategoriseerd op domein. Hiermee krijgt u uitgebreide inzicht in de prestaties van uw e-mailreizen. Met deze uitgebreide analyse kunt u het gedrag van verschillende domeinen begrijpen als reactie op uw e-mailinhoud.

+++ Meer informatie over metrische gegevens van e-maildomeinen

* **[!UICONTROL Sends]**: Het totale aantal verzendingen voor uw e-mail.

* **[!UICONTROL Delivered]**: Aantal verzonden e-mailberichten in verhouding tot het totale aantal verzonden e-mails.

* **[!UICONTROL Email Opens]**: Het aantal keren dat uw e-mails zijn geopend tijdens een rit.

* **[!UICONTROL Clicks]**: Het aantal keer dat er op de inhoud in uw e-mails is geklikt.

* **[!UICONTROL Bounces for outbound channels]**: Het totale aantal fouten dat tijdens het verzendproces is gecumuleerd en de automatische retourverwerking in verhouding tot het totale aantal verzonden e-mails.

* **[!UICONTROL Outbound Errors]**: het totale aantal fouten dat is opgetreden tijdens het verzendproces waardoor het niet naar profielen kan worden verzonden.

* **[!UICONTROL Outbound Exclusions]**: aantal profielen dat door Adobe Journey Optimizer is uitgesloten.

+++

## Labels voor bijgehouden koppelingen {#track-link-label}

![](assets/cja-journey-tracked-link-labels.png)

De tabel **[!UICONTROL Tracked link labels]** bevat een uitgebreid overzicht van de koppelingslabels in uw e-mails, waarin de labels worden gemarkeerd die het hoogste bezoekersverkeer genereren. Met deze functie kunt u de populairste koppelingen identificeren en er prioriteiten aan stellen.

+++ Meer informatie over metriek van tracklabels

* **[!UICONTROL Unique Clicks]**: Aantal profielen dat op de inhoud van een e-mail heeft geklikt.

* **[!UICONTROL Clicks]**: Het aantal keer dat er op de inhoud in uw e-mails is geklikt.

+++

## URL&#39;s van bijgehouden koppeling {#track-link-url}

![](assets/cja-journey-tracked-link-urls.png)

De tabel **[!UICONTROL Tracked link URLs]** bevat een uitgebreid overzicht van de URL&#39;s in uw e-mail die het hoogste bezoekersverkeer aantrekken. Hierdoor kunt u de populairste koppelingen identificeren en er prioriteiten aan stellen, zodat u meer inzicht krijgt in de betrokkenheid bij profielen met specifieke inhoud in uw e-mails.

+++ Meer informatie over URL&#39;s met gekoppelde koppelingen

* **[!UICONTROL Unique Clicks]**: Aantal profielen dat op de inhoud van een e-mail heeft geklikt.

* **[!UICONTROL Clicks]**: Het aantal keer dat er op de inhoud in uw e-mails is geklikt.

+++


## E-mailonderwerpen {#email-subject}

![](assets/cja-email-subject.png)

De tabel **[!UICONTROL Email subjects]** bevat een uitgebreid overzicht van e-mailonderwerpen die het hoogste bezoekersverkeer hebben aangetrokken. Deze bron biedt waardevolle inzichten in de dynamiek van de betrokkenheid van het publiek.

+++ Meer informatie over metrische gegevens over e-mailonderwerpen

* **[!UICONTROL Delivered]**: Aantal verzonden e-mailberichten in verhouding tot het totale aantal verzonden e-mails.

* **[!UICONTROL Unique Delivered]**: Aantal verschillende profielen dat ten minste één e-mail heeft ontvangen, zodat dubbele gegevens niet worden meegeteld.
+++

## Stuitingsredenen {#email-bounce-reasons}

![](assets/cja-journey-email-bounce.png)

In de tabel **[!UICONTROL Bounce Reasons]** worden de beschikbare gegevens met betrekking tot teruggestuurde berichten gecompileerd, zodat u gedetailleerde informatie krijgt over de specifieke redenen voor e-mailblokkeringen.

Voor meer informatie over grenzen, verwijs naar de [&#x200B; lijst van de Onderdrukking &#x200B;](../reports/suppression-list.md) pagina.

## Uitgesloten redenen {#email-excluded}

![](assets/cja-journey-email-excluded.png)

De tabel **[!UICONTROL Excluded reasons]** bevat een uitgebreide weergave van de verschillende factoren die ertoe hebben geleid dat gebruikersprofielen zijn uitgesloten van het doelpubliek, waardoor het bericht niet is ontvangen.

Verwijs naar [&#x200B; deze pagina &#x200B;](exclusion-list.md) voor de uitvoerige lijst van uitsluitingsredenen.

## Foutredenen {#email-errors}

De tabel **[!UICONTROL Error Reasons]** biedt zichtbaarheid in de specifieke fouten die tijdens het verzendproces zijn opgetreden en biedt waardevolle informatie over de aard en het optreden van fouten.
