---
solution: Journey Optimizer
product: journey optimizer
title: IP de gids van de warmtegeleidbaarheid
description: Leer over leverbaarheidsgrondbeginselen en beste praktijken voor IP warmup
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, leverbaarheid, reputatie, ISP, overeenkomst
source-git-commit: 5dd6ebadd7b8c7490cb10496282697ce32ff3693
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 2%

---

# IP de gids van de warmtegeleidbaarheid {#ip-warmup-deliverability-guide}

Wanneer het lanceren van e-mailcampagnes met nieuwe IP adressen of domeinen in Adobe Journey Optimizer, is het begrip van leverbaarheidsgrondbeginselen essentieel voor de bouw van een sterke afzenderreputatie. Deze gids behandelt de belangrijkste concepten, voorbereidingsstappen, en beste praktijken om u te helpen overgang van nul reputatie aan succesvolle inbox plaatsing.

➡️ Leer over leverbaarheidsgrondbeginselen, reputatie het opbouwen, en beste praktijken voor IP warmup in de video van dit [&#x200B; Adobe blogpost &#x200B;](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950?profile.language=nl){target="_blank"}.

>[!NOTE]
>
>Voor geleidelijke instructies bij het uitvoeren van IP warmteoptieplannen in Adobe Journey Optimizer, verwijs naar [&#x200B; begonnen wordt met IP warmtekrachtplannen &#x200B;](ip-warmup-gs.md).

## Waarom IP en de kwestie van de domeinreputatie {#reputation-matters}

De leveranciers van de brievenbus (Gmail, Yahoo, Microsoft, Apple Mail, en anderen) evalueren elke afzender die op vier zeer belangrijke pijlers wordt gebaseerd:

* **Klachten**: Hebben de ontvangers uw berichten als spam gemerkt?
* **Betrokkenheid**: Zijn de ontvangers open, klikken, of antwoord aan uw e-mails?
* **Infrastructuur**: Is uw verzendende infrastructuur voor authentiek verklaard, stabiel, en betrouwbaar?
* **Inhoud**: Ziet uw berichtinhoud wettig en waardevol?

IP warmup richt hoofdzakelijk de eerste drie pijlers door aan brievenbusleveranciers geleidelijk aan te tonen dat uw nieuwe infrastructuur wettig is en gewild alvorens u aan volledig verzendend volume schrapt.

## Controlelijst vóór de vlucht {#pre-flight-checklist}

Voordat u begint met het opwarmen van uw IP-adressen, moet u ervoor zorgen dat alle basiselementen aanwezig zijn. De lijst beschrijft hieronder de essentiële taken om te voltooien alvorens uw IP warmlopingsplan te beginnen.

| Taak | Waarom het belangrijk is | Procedure |
|------|----------------|-------------------|
| Vaste IP&#39;s en gedelegeerde subdomeinen in AJO reserveren | Alle toekomstige reputatie hecht aan deze infrastructuurelementen. | Navigeer naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** > **[!UICONTROL Subdomains]** . [Meer informatie](delegate-subdomain.md) |
| SPF en DKIM configureren | Bevestigt uw verzendende server wettig en gemachtigd is. | Automatisch behandeld door Adobe na [&#x200B; subdomain delegatie &#x200B;](delegate-subdomain.md) en [&#x200B; de verwezenlijking van de kanaalconfiguratie &#x200B;](channel-surfaces.md). |
| Controleer of DMARC-record is geconfigureerd (p=none) | Hiermee schakelt u rapportage van e-mailverificatie en het toekomstige handhavingsbeleid in. | Controleer of DMARC-record is ingesteld voor alle gedelegeerde subdomeinen. Wanneer u een nieuw subdomein delegeert, kunt u DMARC rechtstreeks in de interface instellen. [Meer informatie](dmarc-record.md) |
| Bewaking van zaadlijst configureren | Detecteert problemen met plaatsing van postvakken in een vroeg stadium van het opwarmingsproces. | Voeg zaadadressen toe wanneer het creëren van uw kanaalconfiguratie. [Meer informatie](seed-lists.md) |
| Fase 1 publiek met hoge betrokkenheid samenstellen | Verhoogt vroege betrokkenheidsmetriek met uw meest actieve ontvangers. | Creeer een publiek van minder dan 5.000 contacten die in de laatste 30 dagen opende of klikte. [Meer informatie](../audience/creating-a-segment-definition.md) |

>[!CAUTION]
>
>Verificatiekwesties (SPF, DKIM, DMARC) kunnen niet worden opgelost door het volume te verhogen. Zorg ervoor dat deze correct zijn geconfigureerd voordat u begint met verzenden.

## Monster van vier weken warmtekalender {#warmup-calendar}

Deze voorbeeldkalender biedt een progressieve volumegrafiek op basis van het percentage van uw uiteindelijke dagelijkse volume (UDV). Pas deze nummers aan uw specifieke verzendingsvereisten aan en werk samen met uw leverancier-consultant om een aangepast abonnement te maken.

| Dagen | % van UDV | Doelgroep | Aanbevelingen voor inhoud |
|------|----------|-----------------|------------------------|
| 1-3 | 0,5% | Uw meest betrokken ontvangers | Gebruik een korte, onbewerkte indeling met een duidelijke call-to-action boven de vouw. |
| 4-7 | 1% | Betrokken gebruikers plus recente kopers | Voeg een lichtgewicht hoofdafbeelding toe en gebruik maximaal 3 koppelingen. |
| 8-14 | 5% | Broader actieve abonneelijst | Introduceer uw standaard e-mailsjabloon, maar vermijd veel promotionele inhoud. |
| 15-21 | 25% | Actief plus lichtelijk inactieve abonnees | Gebruik normale marketinginhoud terwijl u de klachtenpercentages nauwlettend in de gaten houdt. |
| 22-28 | 50-100% | Volledige lijst (suppressielijsten respecteren) | Overgang naar uw stationaire verzendende kadentie. |

## Het gebruiken van de IP eigenschap van de warmup plannen {#ajo-warmup-feature}

Adobe Journey Optimizer omvat een gestroomlijnde [&#x200B; IP warmup plannen &#x200B;](ip-warmup-gs.md) eigenschap die de behoefte aan het handvolume dat door complexe reismontages wordt begrensd elimineert. Deze functionaliteit verzekert een gestandaardiseerde benadering van de reputatie van de bouwer afzenders.

### Werking

1. **creeer IP warmup campagnes**: Bouw één of meerdere campagnes met de **[!UICONTROL IP warmup plan activation]** toegelaten optie. [Meer informatie](ip-warmup-campaign.md)

1. **opstelling uw plan**: Toegang **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** > **[!UICONTROL IP warmup plans]** en upload uw gefaseerde warmlopjabloon die met uw leverancier wordt voorbereid. [Meer informatie](ip-warmup-plan.md)

1. **voert fasen** uit: Selecteer een campagne voor elke fase en activeer de overeenkomstige looppas. Het systeem sluit profielen automatisch uit van vorige looppas om te verhinderen over-contacting. [Meer informatie](ip-warmup-execution.md)

1. **Monitor en pas** aan: Gebruik het geconsolideerde rapporteringsdashboard om vooruitgang te volgen, looppas statussen te controleren, en uw plan te wijzigen als de kwesties zich voordoen. [Meer informatie](ip-warmup-execution.md#monitor-plan)

## Realtime controle en belangrijkste metriek {#monitoring}

Adobe Journey Optimizer biedt ingebouwde rapporteringsmogelijkheden om uw opwarmingsprestaties van IP te volgen:

* **Levende rapporten**: De meting en visualisatie van de toegang in real time van uw campagnes van het **[!UICONTROL Last 24hrs]** lusje. [Meer informatie](../reports/campaign-live-report.md#email-live)

* **Al tijdrapporten**: Voor diepgaande inzichten, hefboomwerking Customer Journey Analytics om gegevens van Adobe Experience Platform te analyseren en douanevisualisaties tot stand te brengen. [Meer informatie](../reports/report-gs-cja.md)

### Doelwaarden

Volg deze belangrijke prestatie-indicatoren tijdens uw opwarmingsproject:

| Metrisch | Doeldrempel | Correctie |
|--------|-----------------|-------------------|
| Klachtsnelheid | ≤ 0,1% | Indien overschreden, controleer segment en onderdruk chronische klagers. |
| Harde stuitsnelheid | ≤ 2% | Indien overschreden, herzie de kwaliteits- en hygiënepraktijken. |
| Open rate | ≥ 10% | Als te laag, verifieer u doelgericht betrokken publiek bent. |

## Problemen met afspeelboek oplossen {#troubleshooting}

Gebruik deze beslissingsmatrix om algemene problemen tijdens uw opwarming aan te pakken:

| Symptoom | Waarschijnlijk oorzaak | Aanbevolen actie |
|---------|--------------|-------------------|
| Yahoo tijdelijke fouten (421 fouten) | Volume wordt te snel verhoogd | Het verzenden van de pauze gedurende 24 uren, dan begin bij de vorige rij opnieuw. |
| Open rate minder dan 2% op zaadrekeningen | IP VOEGEND OP LIJST VAN GEWENSTE PERSONEN | Controle [&#x200B; de Hulpmiddelen van Postmaster van Google &#x200B;](https://postmaster.google.com/) en [&#x200B; SNDS van Microsoft &#x200B;](https://sendersupport.olc.protection.outlook.com/snds/); open een leverbaarheidskaartje indien nodig. |
| De klachtensnelheid is hoger dan 0,3% | Mis-doelgroep of stijldoelgroep | De segmentdefinities van de controle en sluit chronische klagers van uw [&#x200B; suppressielijst &#x200B;](manage-suppression-list.md) uit. |

>[!IMPORTANT]
>
>Het is beter om je warmte te vertragen dan om later te proberen om een beschadigde sender reputatie te herstellen. Geef altijd prioriteit aan het behouden van gezonde meetwaarden boven agressieve volumesnelheid.

## Aanbevolen werkwijzen na opwarmen {#post-warmup}

Zodra u uw warmtingsplan hebt voltooid en de metriek hebben gestabiliseerd:

* **handhaaf consistentie**: houd dagelijkse volumetoename onder 30% week-over-week om uw gevestigde reputatie te bewaren.

* **Ononderbroken Monitor**: Plan driemaandelijkse controles van de reputatie om kwesties proactively te identificeren en te richten.

* **respecteer betrokkenheidssignalen**: Ga verder om betrokken ontvangers voorrang te geven en re-engagement campagnes voor inactieve abonnees uit te voeren.

* **houd authentificatie huidig**: verifieer regelmatig dat uw SPF, DKIM, en verslagen van DMARC behoorlijk gevormd blijven.

## Toetsen {#key-takeaways}

* **IP warmte-up is essentieel**: Het overslaan van het warmup proces kost meer tijd en reputatie dan de inspanning wordt vereist om het behoorlijk te doen.

* **gegevens-gedreven besluiten**: De klacht van het spoor, stuiteren, en betrokkenheidstarieven dagelijks en passen uw strategie aan alvorens ISPs u bestraft.

* **Authentificatie eerst, volume tweede**: Los alle SPF, DKIM, en de kwesties van DMARC vóór het beginnen aan platformafzetvolume op.

* **Consistentie doet zich voor**: De leveranciers van de brievenbus gunnen voorspelbare verzendende patronen; vermijd plotselinge volumepieken of onregelmatige verzendende programma&#39;s.

<!--
>[!NOTE]
>
>For more guidance, explore the [Adobe Journey Optimizer Deliverability Guide blog post](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950?profile.language=nl).-->

## Verwante onderwerpen {#related-topics}

* [Ga aan de slag met IP-opwarmingsplannen](ip-warmup-gs.md)
* [IP-warmtecampagnes maken](ip-warmup-campaign.md)
* [Creeer een IP warmlopingsplan](ip-warmup-plan.md)
* [Voer het IP warmlopingsplan uit](ip-warmup-execution.md)
* [Kanaalconfiguraties instellen](channel-surfaces.md)
* [Subdomeinen delegeren](delegate-subdomain.md)
* [Onderdrukkingslijst beheren](manage-suppression-list.md)
* {de Gids van de Beste praktijken van 0} Levering [&#128279;](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=nl)

