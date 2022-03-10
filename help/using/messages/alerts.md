---
title: Waarschuwingen in berichten
description: Leer hoe te om berichtinhoudbevestiging te controleren en problemen op te lossen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: f5b629d5e413a3ffc037af959c5e16b9a47e8a0e
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Waarschuwingen bij uw berichten controleren {#publish-manage-messages}

## Controles vóór publicatie {#message-alerting}

Terwijl u uw bericht creeert, alarm u wanneer u belangrijke acties moet voeren alvorens uw bericht te publiceren.

Waarschuwingen worden rechtsboven op het scherm weergegeven, zoals hieronder wordt getoond:

![](assets/message-alerts.png)

>[!NOTE]
>
>Als deze knop niet wordt weergegeven, is er geen melding gevonden.

Er kunnen twee typen waarschuwingen optreden:

* **Waarschuwingen** verwijzen naar aanbevelingen en beste praktijken. Er wordt bijvoorbeeld een bericht weergegeven als de koppeling om te weigeren ontbreekt.

* **Fouten** voorkomt u dat u het bericht publiceert zolang deze niet zijn opgelost. U wordt bijvoorbeeld in een bericht gewaarschuwd dat de onderwerpregel ontbreekt.

Alle mogelijke waarschuwingen en fouten zijn gedetailleerd [onder](#alerts-and-warnings).

>[!CAUTION]
>
> U moet alles oplossen **fout** waarschuwingen vóór publicatie.

## Lijst met waarschuwingen en fouten {#alerts-and-warnings}

De instellingen en elementen die door het systeem zijn gecontroleerd, worden hieronder weergegeven. U zult ook informatie over hoe te om uw configuratie aan te passen om de overeenkomstige kwesties op te lossen vinden.

**Waarschuwingen**:

* **[!UICONTROL The opt-out link is not present in the email body.]**: u kunt het beste een koppeling zonder abonnement toevoegen aan uw e-mailadres. Leer hoe u deze kunt configureren in [deze sectie](consent.md).

* **[!UICONTROL Text version of HTML is empty.]**: vergeet niet een tekstversie van uw e-mailhoofdtekst te definiëren, omdat deze wordt gebruikt wanneer HTML-inhoud niet kan worden weergegeven. Leer hoe u de tekstversie maakt in [deze sectie](create-email-content.md#generate-text-version).

* **[!UICONTROL Empty link is present in email body.]**: controleer of alle koppelingen in uw e-mail juist zijn. Leer hoe u inhoud en koppelingen kunt beheren in [deze sectie](create-email-content.md).

* **[!UICONTROL Email size has exceeded the limit of 100KB.]**: voor een optimale aflevering moet u ervoor zorgen dat de e-mailgrootte niet groter is dan 100 kB. Leer hoe u e-mailinhoud kunt bewerken in [deze sectie](create-email-content.md).

**Fouten**:

* **[!UICONTROL The subject line is missing.]**: e-mailonderwerpregel is verplicht. Leer hoe u het kunt definiëren en personaliseren in [deze sectie](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL The push version of the message is empty.]**: deze fout wordt weergegeven wanneer de hoofdtekst of titel van het pushbericht ontbreekt. Leer hoe u inhoud voor pushmeldingen definieert in [deze sectie](create-push.md).

* **[!UICONTROL The email version of the message is empty.]**: deze fout wordt weergegeven wanneer de e-mailinhoud niet is geconfigureerd. Leer hoe u e-mailinhoud ontwerpt in [deze sectie](design-emails.md).

* **[!UICONTROL Preset doesn’t exist.]**: U kunt uw bericht niet publiceren als de voorinstelling die u hebt geselecteerd, wordt verwijderd nadat het bericht is gemaakt. Als deze fout optreedt, selecteert u een andere voorinstelling in het bericht **[!UICONTROL Properties]**. Meer informatie over branding in [deze sectie](../configuration/about-subdomain-delegation.md).

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB.]**: de grootte van de pushmelding mag niet groter zijn dan 4 kB. U kunt deze limiet in acht nemen door het gebruik van afbeeldingen of emojis te beperken. Leer hoe u de inhoud van uw pushmelding beheert in [deze sectie](create-push.md).

>[!CAUTION]
>
> Als u uw bericht wilt publiceren, moet u alles oplossen **fout** waarschuwingen.

<!--Other issues can stop publication such as:
* The push notification title is empty-->
