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
source-git-commit: 6386a5ee5a0d1f221beab67f43636c599531736a
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# Aan de slag met waarschuwingen {#alerts}

Journey Optimizer maakt gebruik van Adobe Experience Platform-alarmeringsmogelijkheden. Hierdoor hebt u via de gebruikersinterface toegang tot systeemwaarschuwingen. U kunt de beschikbare waarschuwingen weergeven en hierop een abonnement nemen.

Wanneer een bepaalde reeks voorwaarden in uw verrichtingen (zoals een potentieel probleem wanneer het systeem een drempel) overschrijdt wordt bereikt, worden de waakzame berichten geleverd aan om het even welke gebruikers in uw organisatie die aan hen hebben geabonneerd.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Meer informatie over berichten in Adobe Experience Platform [documentatie](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html).

Leren hoe te om aan alarm in te schrijven en hen te vormen, verwijs naar dit [page](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>Er worden enkele ontwerpwijzigingen uitgevoerd voor de waarschuwing &#39;Doelgroep lezen is mislukt&#39;. Deze waarschuwing wordt daarom voorlopig gepauzeerd en is tijdelijk verwijderd uit de gebruikersinterface. Zodra deze wijzigingen zijn vrijgegeven, wordt de waarschuwing opnieuw weergegeven en kunt u zich erop abonneren.

In het linkermenu, onder **Administratie**, klikt u op **Waarschuwingen**. Er is een vooraf geconfigureerde waarschuwing voor Journey Optimizer beschikbaar. Deze waarschuwing geeft een waarschuwing als een aangepaste handeling mislukt. Wij zijn van mening dat er sprake is van een mislukking waarbij de afgelopen vijf minuten meer dan 1 procent van de fouten is gemaakt bij een specifieke aangepaste actie. Dit wordt elke 30 seconden geëvalueerd.

![](assets/alerts-custom-action.png)


<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

Als een onverwacht gedrag optreedt, wordt een waarschuwingsbericht naar de abonnees van de waarschuwing verzonden via e-mail of rechtstreeks in Journey Optimizer, in de rechterbovenhoek van de interface, op basis van gebruikersvoorkeuren.

Wanneer een alarm wordt opgelost, ontvangt u een &quot;Opgelost&quot;bericht. Voor de aangepaste actieredeling kan dit om twee redenen gebeuren:
* In de afgelopen 5 minuten is er geen fout opgetreden bij die aangepaste handeling (of bij fouten onder de drempel van 1%).
* Er is geen profiel bereikt voor die aangepaste handeling.

Wanneer [waarschuwingsregels weergeven in gebruikersinterface van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), kunt u zich op elke regel afzonderlijk abonneren. Wanneer u zich abonneert op waarschuwingen via [I/O-gebeurtenismeldingen](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)De waarschuwingsregels zijn echter ingedeeld in verschillende abonnementspakketten. De abonnementsnaam voor de I/O-gebeurtenis die overeenkomt met de aangepaste actiedraag is: &quot;Aangepaste actiedout van reis&quot;.

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".-->

>[!WARNING]
>
>Deze waarschuwingen zijn alleen van toepassing op levende reizen. Er worden geen waarschuwingen gegeven voor ritten in testmodus.

