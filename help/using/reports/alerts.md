---
solution: Journey Optimizer
product: journey optimizer
title: Waarschuwingen
description: Leer hoe u waarschuwingen beheert
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Aan de slag met waarschuwingen {#alerts}

Journey Optimizer maakt gebruik van Adobe Experience Platform-waarschuwingsmogelijkheden. Hierdoor hebt u via de gebruikersinterface toegang tot systeemwaarschuwingen. U kunt de beschikbare waarschuwingen weergeven en hierop een abonnement nemen. Wanneer een bepaalde reeks voorwaarden in uw verrichtingen (zoals een potentieel probleem wanneer het systeem een drempel) overschrijdt wordt bereikt, worden de waakzame berichten geleverd aan om het even welke gebruikers in uw organisatie die aan hen hebben geabonneerd. Deze berichten kunnen over een vooraf bepaald tijdinterval herhalen tot het alarm is opgelost.

Meer informatie over berichten in Adobe Experience Platform [documentatie](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html).
Leren hoe te om aan alarm in te schrijven en hen te vormen, verwijs naar dit [page](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

In het linkermenu, onder **Beheer**, klikt u op **Waarschuwingen**. Er is een vooraf geconfigureerde waarschuwing voor Journey Optimizer beschikbaar. Deze waarschuwing waarschuwt u als een read segment knoop geen profiel tijdens het bepaalde tijdkader heeft verwerkt.

![](assets/alerts1.png)

Als een dergelijk onverwacht gedrag zich voordoet, wordt een waarschuwingsbericht verzonden naar abonnees van de waarschuwing via e-mail, in de rechterbovenhoek van de interface.

![](assets/alerts2.png)

Wanneer [het bekijken alarmregels in UI van het Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), kunt u zich op elke regel afzonderlijk abonneren. Wanneer u zich abonneert op waarschuwingen via [I/O-gebeurtenismeldingen](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)De waarschuwingsregels zijn echter ingedeeld in verschillende abonnementspakketten. De naam van het I/O-gebeurtenisabonnement die overeenkomt met de waarschuwing van het Leessegment is: &quot;Reis read segment Delays, Failures and Errors&quot;.

>[!WARNING]
>
>Deze waarschuwingen zijn alleen van toepassing op levende reizen. Er worden geen waarschuwingen gegeven voor reizen in testmodus.