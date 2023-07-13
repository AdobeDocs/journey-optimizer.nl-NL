---
solution: Journey Optimizer
product: journey optimizer
title: Waarschuwingen
description: Leer hoe u waarschuwingen beheert
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# Aan de slag met waarschuwingen {#alerts}

Journey Optimizer maakt gebruik van Adobe Experience Platform-waarschuwingsmogelijkheden. Hierdoor hebt u via de gebruikersinterface toegang tot systeemwaarschuwingen. U kunt de beschikbare waarschuwingen weergeven en hierop een abonnement nemen.

Wanneer een bepaalde reeks voorwaarden in uw verrichtingen (zoals een potentieel probleem wanneer het systeem een drempel) overschrijdt wordt bereikt, worden de waakzame berichten geleverd aan om het even welke gebruikers in uw organisatie die aan hen hebben geabonneerd. Deze berichten kunnen over een vooraf bepaald tijdinterval herhalen tot het alarm is opgelost.

Meer informatie over berichten in Adobe Experience Platform [documentatie](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html).
Leren hoe te om aan alarm in te schrijven en hen te vormen, verwijs naar dit [page](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>Er worden enkele ontwerpwijzigingen doorgevoerd voor de waarschuwing ‘Doelgroep lezen is mislukt’. Deze waarschuwing wordt daarom voorlopig gepauzeerd en is tijdelijk verwijderd uit de gebruikersinterface. Zodra deze wijzigingen zijn vrijgegeven, wordt de waarschuwing opnieuw weergegeven en kunt u zich erop abonneren.
>

In het linkermenu, onder **Beheer**, klikt u op **Waarschuwingen**.

<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

Als een onverwacht gedrag voorkomt, wordt een waakzaam bericht verzonden naar abonnees van het alarm door e-mail, in de hoogste juiste hoek van de interface.

<!--![](assets/alerts2.png)-->


Wanneer [waarschuwingsregels weergeven in gebruikersinterface van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), kunt u zich op elke regel afzonderlijk abonneren. Wanneer u zich abonneert op waarschuwingen via [I/O-gebeurtenismeldingen](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)De waarschuwingsregels zijn echter ingedeeld in verschillende abonnementspakketten.

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".

>[!WARNING]
>
>These alerts apply only to live journeys. Alerts will not be triggered for journeys in test mode.-->
