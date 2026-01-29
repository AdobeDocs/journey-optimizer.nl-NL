---
solution: Journey Optimizer
product: journey optimizer
title: De actiecampagne plannen
description: Leer hoe u de campagne Handelingen kunt plannen.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: maken, optimaliseren, campagne, oppervlak, berichten
exl-id: b183eeb8-606f-444d-9302-274f159c3847
source-git-commit: e6aa361229f068c475732c715160b7c644189e51
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 0%

---

# De actiecampagne plannen {#action-campaign-schedule}

Gebruik het tabblad **[!UICONTROL Schedule]** om het campagneschema te definiëren.

## Begindatum van campagne instellen

Standaard worden actiecampagnes gestart als ze handmatig zijn geactiveerd en eindigen als het bericht eenmaal is verzonden. Als u uw campagne niet meteen na activering wilt uitvoeren, kunt u in de sectie **[!UICONTROL Campaign start]** een datum en tijd opgeven waarop het bericht moet worden verzonden.

Wanneer u campagnes in [!DNL Adobe Journey Optimizer] plant, moet u ervoor zorgen dat de begindatum/tijd wordt uitgelijnd op de gewenste eerste levering. Voor terugkerende campagnes, als de aanvankelijke geplande tijd reeds is overgegaan, zullen de campagnes aan de volgende beschikbare tijdgroef volgens hun terugkeringsregels rollen.

![](assets/campaign-start.png)

## Verzenden op lokale tijd van ontvanger {#profile-timezone}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_profile_timezone"
>title="Tijdzone profiel gebruiken"
>abstract="Verzend berichten die op de het profieltijdzone van elke ontvanger worden gebaseerd. Alle ontvangers ontvangen het bericht op hetzelfde lokale tijdstip, ongeacht hun geografische locatie. Het systeem gebruikt het veld &quot;timeZone&quot; uit Adobe Experience Platform-profielen, waarbij de tijdzone van de maker van de campagne als fallback wordt gebruikt."

Wanneer het plannen van een campagne voor een specifieke datum en een tijd, kunt u verkiezen om berichten te verzenden die op de het profieltijdzone van elke ontvanger worden gebaseerd. Dit zorgt ervoor dat alle ontvangers het bericht gelijktijdig, ongeacht hun geografische plaats ontvangen.

Bijvoorbeeld, als u een campagne plant om op 9 AM te verzenden gebruikend profieltimezone, zullen de ontvangers in New York (ET) het ontvangen om 9 AM ET, terwijl de ontvangers in Los Angeles (PT) het om 9 AM PT zullen ontvangen.

>[!AVAILABILITY]
>
>Deze functie bevindt zich in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.
>
>De planning die de streken van de profieltijd gebruikt is beschikbaar voor deze uitgaande kanalen slechts: E-mail, Duw, SMS, WhatsApp, en LIJN.

Tijdzoneplanning voor profielen inschakelen:

1. Geef in de sectie **[!UICONTROL Campaign start]** de datum en tijd op waarop het bericht moet worden verzonden.

1. Schakel de optie **[!UICONTROL Use profile timezone]** in.

   ![](assets/campaign-profile-timezone.png)

**hoe het werkt:**

Het systeem gebruikt het veld `profile.timeZone` van het Adobe Experience Platform-profiel van elke ontvanger om de lokale tijdzone te bepalen. Als een profiel geen tijdzonewaarde heeft, gebruikt het systeem timezone waarin de campagne als fallback werd gecreeerd.

De campagne blijft in **Levende** status terwijl de berichten over alle tijdzones worden geleverd. Zodra alle tijdzones zijn verwerkt, verandert de campagnestatus in **Voltooid**.

**Gesteunde herkenningstekens van de tijdzone:**

Journey Optimizer valideert de `profile.timeZone` -waarde aan de hand van standaard-IANA-tijdzone-id&#39;s. Identificatoren zijn hoofdlettergevoelig en moeten overeenkomen met de officiële IANA-naamgeving. Verschuivingen kunnen na verloop van tijd veranderen als gevolg van zomertijd en historische updates. Verwijs naar het [ Gegevensbestand van de Tijdzone van 0} IANA {voor de officiële lijst van herkenningstekens.](https://www.iana.org/time-zones){_blank}

## Een uitvoeringsfrequentie instellen

Voor **E-mail**, **SMS**, en **Push bericht** acties, kunt u een frequentie bepalen waarbij het bericht van de campagne zou moeten worden verzonden. Hiervoor gebruikt u de **[!UICONTROL Action triggers]** -opties in het scherm voor het maken van campagnes om op te geven of de campagne dagelijks, wekelijks of maandelijks moet worden uitgevoerd.

![](assets/campaign-frequency.png)

>[!NOTE]
>
>Voor **e-mail** acties, kunt u specifieke IP campagnes van de opwarmingsPlan tot stand brengen. Het campagneschema zal door het IP warmup plan worden gedreven het zal worden geassocieerd met, betekenend dat het programma niet meer in de campagne zelf wordt bepaald. [ Leer hoe te om IP warmup campagnes ](../configuration/ip-warmup-campaign.md) tot stand te brengen.

## Einddatum instellen

In de sectie **[!UICONTROL Campaign end]** kunt u opgeven wanneer een campagne moet stoppen met uitvoeren. Buiten de opgegeven datums wordt de campagne niet uitgevoerd.

![](assets/campaign-end.png)

## Snelheidbeheersing instellen

Met [!DNL Journey Optimizer] kunt u tariefcontrole inschakelen voor uitgaande acties (e-mail, SMS, pushberichten).

Deze functie is vooral handig om overbelasting op downstreamsystemen, zoals pagina&#39;s voor landingen of platforms voor klantenservice, te voorkomen. Bijvoorbeeld, kunt u een tariefgrens van 165 berichten per seconde plaatsen om constante levering zonder overweldigende stroomafwaartse systemen te verzekeren.

Als u de snelheidsregeling wilt instellen, schakelt u de optie **[!UICONTROL Throttle delivery]** in de **[!UICONTROL Delivery settings]** -sectie in en geeft u de gewenste **[!UICONTROL Delivery rate]** per seconde op.

* Minimaal ondersteunde leveringspercentage: 1 per seconde.
* Maximale ondersteunde leversnelheid: 2000 per seconde wanneer de optie &quot;Throttle delivery&quot; is ingeschakeld.

![](assets/throttling-rate-control.png)

>[!IMPORTANT]
>
>Bij het instellen van een leveringstarief is de maximale tijdlijn waarvoor het campagnepubliek kan worden uitgevoerd 12 uur. Als de leveringstarief aan een waarde wordt geplaatst die niet alle publiek toestaat om het bericht in het 12 uurstijdsbestek te worden verzonden, dan zouden de resterende profielen van de campagne worden uitgesloten. U kunt de telling van deze uitgesloten profielen in het campagnerapport zien.

## Volgende stappen {#next}

Zodra uw campagnemodel klaar is, kunt u de campagne beoordelen en activeren. [Meer informatie](review-activate-campaign.md)
