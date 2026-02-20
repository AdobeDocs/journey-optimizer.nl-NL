---
solution: Journey Optimizer
product: journey optimizer
title: Verzenden met gebruik van golven
description: Plan uitgaande campagneberichten die in gecontroleerde partijen in tijd moeten worden geleverd. Golf die steunt leverbaarheid verzendt en helpt afzenderreputatie handhaven.
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: golven, batches, planning, campagne, transport, leverbaarheid
source-git-commit: 7df05e41b086c60724576328c5bcfee47cab65ca
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# Verzenden met gebruik van golven in campagnes {#send-using-waves}

U kunt de levering van uitgaande campagneberichten in verscheidene partijen (golven) verdelen en hen in tijd plannen. Golf die hulplading verzendt, vermijdt overweldigende stroomafwaartse systemen (zoals vraagcentra of landende pagina&#39;s), en steun leverbaarheid en afzenderreputatie-vooral voor hoog-volume verzendt.

<!--
>[!CAUTION]
>
>Wave sending applies to **outbound** actions only (Email, SMS, Push, Direct mail).-->

Met Journey Optimizer kunt u het aantal golven, de grootte ervan (als percentage van het publiek of als absolute getallen) en het tijdstip bepalen waarop elke golf wordt uitgevoerd.

## Beperkingen en geleiders {#limitations-guardrails}

* Het verzenden van de golf is op **uitgaande** acties slechts (E-mail, SMS, Duw, Directe post) van toepassing.
* U moet minstens **2 golven** bepalen en u kunt tot **10 golven** toevoegen.
* Het minimuminterval tussen het begin van twee golven is **30 minuten**.
* Een golfbegin kan niet vóór de campagnestart of in het verleden zijn.

## Vorm golf die {#configure-wave-sending}

Volg de onderstaande stappen om te configureren hoe en wanneer u golven wilt verzenden in een campagne.

1. Creeer of open een [&#x200B; campagne van de Actie &#x200B;](create-campaign.md) die een uitgaande actie (bijvoorbeeld, E-mail, SMS, Duw) bevat.

1. Selecteer **[!UICONTROL Schedule]** op het tabblad **[!UICONTROL Deliver campaign actions in waves]** van uw campagne.

   ![](assets/campaign-wave-option.png){width="100%"}

   >[!NOTE]
   >
   >De optie **[!UICONTROL Deliver campaign actions in waves]** wordt alleen weergegeven wanneer een uitgaande actie is geselecteerd op het tabblad **[!UICONTROL Actions]** van de campagne. [Meer informatie](campaign-action.md)

1. Stel het aantal golven in dat u wilt verzenden (bijvoorbeeld 4).

   >[!NOTE]
   >
   >U moet minstens twee golven bepalen en kunt tot 10 golven toevoegen.

1. Kies hoe u de golfgrootte en timing definieert zoals hieronder wordt beschreven.

### Gelijke golven {#equal-waves}

Standaard wordt het publiek opgedeeld in golven van gelijke grootte. Plan de tijd voor de eerste golf en plaats een vast interval tussen het begin van elke golf (bijvoorbeeld, 2 uren).

![](assets/campaign-equal-waves.png){width="80%"}

>[!NOTE]
>
>Het minimuminterval tussen het begin van twee golven is **30 minuten**.

Het systeem plant dan verdere golven automatisch (bijvoorbeeld, eerste golf bij 9 :00 AM, tweede bij 11 :00 AM, derde bij 1 :00 PM, vierde bij 3 :00 PM).

### Aangepaste distributie {#custom-distribution}

Selecteer de optie **[!UICONTROL Custom distribution]** om de grootte van elke golf als percentage van het totale publiek (bijvoorbeeld, 15%, 20%, 25%, 40%) te bepalen.

![](assets/campaign-wave-percentage.png){width="80%"}

>[!NOTE]
>
>Het totaal voor alle golven moet gelijk zijn aan 100%. Als dit niet het geval is, wordt een waarschuwingsbericht getoond.<!--are the waves actually sent or does the system prevent user from saving the campaign?-->

Selecteer **[!UICONTROL Numbers]** om de grootte van elke golf als een absoluut aantal profielen (bijvoorbeeld, 10.000; 50.000) te bepalen.

![](assets/campaign-wave-numbers.png){width="80%"}

>[!NOTE]
>
>Wanneer het gebruiken van aantallen, bevestigt het systeem niet dat de som het volledige publiek-u moet ervoor zorgen dat uw golfgrootte het publiek behandelt u van plan bent te verzenden naar. Leer meer in de [&#x200B; Veelgestelde vragen &#x200B;](#faq).

### Aangepast schema {#custom-schedule}

Selecteer **[!UICONTROL Schedule each wave]** om een specifieke begindatum en tijd voor elke golf te bepalen. De golven hoeven niet gelijkmatig worden verdeeld (bijvoorbeeld, 9 :00 AM, 11 :00 AM, 5 :00 PM, 8 :30 PM).

![](assets/campaign-wave-custom-schedule.png){width="80%"}

>[!NOTE]
>
>Het minimuminterval tussen het begin van twee golven is **30 minuten**.

## Gebruiksscenario’s {#use-cases}

Golf die hulp verzendt u controleert wanneer en hoeveel berichten uit gaan, die leveringscapaciteit kunnen verbeteren, afzenderreputatie beschermen, en richten verzendt met uw operationeel vermogen. Overweeg golven in deze scenario&#39;s te gebruiken:

* **het centrum van de Vraag of reactiebeheer:** Beperk hoeveel berichten per dag of per uur gaan zodat de stroomafwaartse teams (b.v., klantenzorg) reacties kunnen behandelen. Bijvoorbeeld, verzend 20 berichten per dag om de capaciteit van het vraagcentrum aan te passen.

  ![](assets/campaign-waves-ex-call-center.png){width="75%"}

* **Hoog volume en leverability:** vermijd verzendend een zeer grote campagne in één schot. De levering van de spreiding in tijd helpen afzenderreputatie handhaven en het risico verminderen om als spam worden gemarkeerd.

  ![](assets/campaign-waves-ex-high-volume.png){width="75%"}

* **Ramp-up:** wanneer het gebruiken van een nieuw platform of IP, verhoogt progressief volume (bijvoorbeeld, 10% in de eerste golf, toen 15%, 20%, etc.) om reputatie geleidelijk te bouwen.

  ![](assets/campaign-waves-ex-ramp-up.png){width="75%"}

## Veelgestelde vragen {#faq}

+++ Wat gebeurt er als de som van de golfgrootten niet overeenkomt met uw totale publiek?

* Als de som van uw golfgrootte **&#x200B;**&#x200B;het publiek overschrijdt (bijvoorbeeld, plant u 100.000 in de eerste golf voor een publiek van 100.000), zal de eerste golf naar het volledige publiek verzenden en de resterende golven zullen geen één verlaten hebben naar-zij niet uitvoeren.
* Als de som **minder** dan het publiek is (bijvoorbeeld, bepaalt u vier golven in totaal 40.000 profielen voor een publiek van 100.000), slechts de profielen inbegrepen in die golven zullen het bericht ontvangen. De rest van het publiek zal niet de mededeling ontvangen en zal niet in recentere golven opnieuw worden geprobeerd.

+++

+++ Kan ik verschillende segmenten of criteria aan individuele golven toewijzen?

U kunt alleen de grootte en de timing van golven definiëren. De selectie van ontvangers is hetzelfde voor de hele campagne. U kunt geen verschillende segmenten of criteria toewijzen aan afzonderlijke golven.

+++

## Volgende stappen {#next}

* [&#x200B; Plan de campagne van de Actie &#x200B;](campaign-schedule.md) - vastgestelde begindatum, einddatum, frequentie, en tariefcontrole.
* [&#x200B; Overzicht en activeer de campagne &#x200B;](review-activate-campaign.md) - controleer de campagne en ga levend.
