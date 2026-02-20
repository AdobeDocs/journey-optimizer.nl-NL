---
solution: Journey Optimizer
product: journey optimizer
title: Verzenden met gebruik van golven tijdens reizen
description: Plan uitgaande reisberichten die in gecontroleerde partijen (golven) in tijd moeten worden geleverd. Golf die in read-publiek reizen helpt lading en steunleverbaarheid in evenwicht brengen.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
mini-toc-levels: 1
keywords: golven, batches, planning, reis, leestoor, leverbaar
source-git-commit: 6c509ef134c4240b243d255fd1ab7ec6bb062bf0
workflow-type: tm+mt
source-wordcount: '875'
ht-degree: 0%

---

# Verzenden met gebruik van golven tijdens reizen {#send-using-waves-journeys}

>[!AVAILABILITY]
>
>Deze functie bevindt zich in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

U kunt uitgaande berichten van een reis in partijen (golven) in tijd in plaats van allen in één keer leveren. Golf die hulplading verzendt, vermijdt overweldigende stroomafwaartse systemen (zoals callcenters of landende pagina&#39;s), en steunt leverbaarheid en afzenderreputatie-vooral voor high-volume gelezen publiekstrajecten.

<!--
>[!CAUTION]
>
>Wave sending is available for read audience journeys only and applies to **outbound** actions only (Email, SMS, Push, Direct mail).-->

U vormt het op het reisniveau wanneer u bepaalt hoe het publiek ingaat en hoe de acties gepland zijn. U bepaalt het aantal golven, hun grootte (als percentage van het publiek of als absolute aantallen), en wanneer elke golf loopt.

## Beperkingen en geleiders {#limitations-guardrails}

* Golfverzending is alleen beschikbaar voor leestuisreizen met de plannertypen **[!DNL As soon as possible]** en **[!UICONTROL Once]** . Leer meer op het [ reisprogramma ](read-audience.md#schedule).
* De verzending van de golven is niet beschikbaar voor terugkomende, gebeurtenis-teweeggebrachte, zaken-gebeurtenis, testwijze of droge reizen.
* U moet minstens **2 golven** bepalen en u kunt tot **10 golven** toevoegen.
* Het minimuminterval tussen het begin van twee golven is **30 minuten**.
* Een golfstart kan niet vóór de start van de reis of in het verleden plaatsvinden.
* Het splitsen van het publiek in golven kan tot 1 uur duren. Profielen mogen pas op dat moment de reis betreden.
* Binnen één enkele reisversie, lopen twee golven nooit tezelfdertijd. De volgende golf begint slechts nadat de vorige golf is gebeëindigd. Bijvoorbeeld, als de golven 1 uur uit elkaar geprogrammeerd zijn maar de eerste golflooppas 2 uren, begint de tweede golf wanneer de eerste golf, niet bij zijn geplande tijd beëindigt.
* De golfslag kan worden vertraagd wanneer het platform quota&#39;s toepast of wanneer de systeemcapaciteit zwaar wordt belast.

## Vorm golf die in een reis verzendt {#configure-wave-sending}

1. Begin uw reis met a [ Gelezen de activiteit van het publiek ](read-audience.md).

1. Dubbelklik op de **[!UICONTROL Read Audience]** -activiteit om de eigenschappen ervan te openen en selecteer de optie **[!UICONTROL Deliver journey action in waves]** .

   ![](assets/journey-wave-option.png){width="100%"}

1. Plaats het **aantal golven** (bijvoorbeeld, 4).

   ![](assets/journey-wave-number.png){width="80%"}

   >[!NOTE]
   >
   >U moet minstens twee golven bepalen en kunt tot 10 golven toevoegen.

1. Kies hoe u de golfgrootte en timing definieert zoals hieronder wordt beschreven.

### Gelijke golven {#equal-waves}

Standaard wordt het publiek opgedeeld in golven van gelijke grootte. Stel een vast interval in tussen het begin van elke golf (bijvoorbeeld 2 uur).

![](assets/journey-equal-waves.png){width="70%"}

>[!NOTE]
>
>Het minimuminterval tussen het begin van twee golven is **30 minuten**.

Het systeem plant dan verdere golven automatisch (bijvoorbeeld, eerste golf bij 9 :00 AM, tweede bij 11 :00 AM, derde bij 1 :00 PM, vierde bij 3 :00 PM).

### Aangepaste distributie {#custom-distribution}

Selecteer de optie **[!UICONTROL Custom distribution]** om de grootte van elke golf als percentage van het totale publiek (bijvoorbeeld, 15%, 20%, 25%, 40%) te bepalen.

![](assets/journey-wave-percentage.png){width="70%"}

>[!NOTE]
>
>Het totaal voor alle golven moet gelijk zijn aan 100%. Als dit niet het geval is, wordt een waarschuwingsbericht getoond.<!--are the waves actually sent or does the system prevent user from saving the journey?-->

Selecteer **[!UICONTROL Numbers]** om de grootte van elke golf als een absoluut aantal profielen (bijvoorbeeld, 10.000; 50.000) te bepalen.

![](assets/journey-wave-numbers.png){width="70%"}

>[!NOTE]
>
>Wanneer het gebruiken van aantallen, bevestigt het systeem niet dat de som het volledige publiek-u moet ervoor zorgen dat uw golfgrootte het publiek behandelt u van plan bent te verzenden naar. Leer meer in de [ Veelgestelde vragen ](#faq).

### Aangepast schema {#custom-schedule}

Selecteer **[!UICONTROL Schedule each wave]** om een specifieke begindatum en tijd voor elke golf te bepalen. De golven hoeven niet gelijkmatig worden verdeeld (bijvoorbeeld, 9 :00 AM, 11 :00 AM, 5 :00 PM, 8 :30 PM).

![](assets/journey-wave-custom-schedule.png){width="70%"}

>[!NOTE]
>
>Het minimuminterval tussen het begin van twee golven is **30 minuten**.

## Gebruiksscenario’s {#use-cases}

Golf die hulp verzendt u controleert wanneer en hoeveel berichten uit gaan, die leveringscapaciteit kunnen verbeteren, afzenderreputatie beschermen, en richten verzendt met uw operationeel vermogen. Overweeg golven in deze scenario&#39;s te gebruiken:

* **het centrum van de Vraag of reactiebeheer:** Beperk hoeveel berichten per dag of per uur gaan zodat de stroomafwaartse teams (b.v., klantenzorg) reacties kunnen behandelen. Bijvoorbeeld, verzend 20 berichten per dag om de capaciteit van het vraagcentrum aan te passen.

  ![](assets/journey-waves-ex-call-center.png){width="55%"}

* **Hoog volume en leverability:** Vermijd verzendend een zeer grote reis in één schot verzendt. De levering van de spreiding in tijd helpen afzenderreputatie handhaven en het risico verminderen om als spam worden gemarkeerd.

  ![](assets/journey-waves-ex-high-volume.png){width="55%"}

* **Ramp-up:** wanneer het gebruiken van een nieuw platform of IP, verhoogt progressief volume (bijvoorbeeld, 10% in de eerste golf, toen 15%, 20%, etc.) om reputatie geleidelijk te bouwen.

  ![](assets/journey-waves-ex-ramp-up.png){width="55%"}

## Veelgestelde vragen {#faq}

+++ Wat gebeurt er als de som van de golfgrootten niet overeenkomt met uw totale publiek?

* Als de som van uw golfgrootte **** het publiek overschrijdt (bijvoorbeeld, plant u 100.000 in de eerste golf voor een publiek van 100.000), zal de eerste golf naar het volledige publiek verzenden en de resterende golven zullen geen één verlaten hebben naar-zij niet uitvoeren.
* Als de som **minder** dan het publiek is (bijvoorbeeld, bepaalt u vier golven in totaal 40.000 profielen voor een publiek van 100.000), slechts de profielen inbegrepen in die golven zullen het bericht ontvangen. De rest van het publiek zal niet de mededeling ontvangen en zal niet in recentere golven opnieuw worden geprobeerd.

+++

+++ Kan ik verschillende segmenten of criteria aan individuele golven toewijzen?

U kunt alleen de grootte en de timing van golven definiëren. Dezelfde doelgroep loopt door de reis; u kunt geen verschillende segmenten of criteria toewijzen aan afzonderlijke golven.

+++

## Zie ook {#see-also}

* [ gebruik een publiek in een reis ](read-audience.md) - vorm de Gelezen activiteit van het Publiek.
