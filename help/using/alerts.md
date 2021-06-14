---
title: Waarschuwingen in berichten
description: Leer hoe te om berichtinhoudbevestiging te controleren en problemen op te lossen
feature: Journeys
topic: Contentmanagement
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# Waarschuwingen {#publish-manage-messages}

![](assets/do-not-localize/badge.png)

## Controleert vóór publicatie {#message-alerting}

Terwijl u uw bericht creeert, alarm u wanneer u belangrijke acties moet voeren alvorens uw bericht te publiceren.

Waarschuwingen worden rechtsboven op het scherm weergegeven, zoals hieronder wordt getoond:

![](assets/message-alerts.png)

>[!NOTE]
>
>Als deze knop niet wordt weergegeven, is er geen melding gevonden.

Er kunnen twee typen waarschuwingen optreden:

* **De** waarschuwingen verwijzen naar aanbevelingen en beste praktijken. Er wordt bijvoorbeeld een bericht weergegeven als de koppeling om te weigeren ontbreekt.

* **** Errorsprevent u van het publiceren van het bericht zolang zij niet worden opgelost. U wordt bijvoorbeeld in een bericht gewaarschuwd dat de onderwerpregel ontbreekt.

Alle mogelijke waarschuwingen en fouten worden gedetailleerd [hieronder](#alerts-and-warnings).

>[!CAUTION]
>
> U moet alle **error** alarm vóór publicatie oplossen.

## Lijst met waarschuwingen en fouten {#alerts-and-warnings}

De instellingen en elementen die door het systeem zijn gecontroleerd, worden hieronder weergegeven. U zult ook informatie over hoe te om uw configuratie aan te passen om de overeenkomstige kwesties op te lossen vinden.

**Waarschuwingen**:

* **[!UICONTROL Opt out link not present in the email body]**: u kunt het beste een koppeling zonder abonnement toevoegen aan uw e-mailadres. Leer hoe te om het in [deze sectie](consent.md) te vormen.

* **[!UICONTROL Text version of html is empty]**: Vergeet niet een tekstversie van uw e-mailhoofdtekst te definiëren, omdat deze wordt gebruikt wanneer HTML-inhoud niet kan worden weergegeven. Leer hoe u de tekstversie maakt in [deze sectie](create-email-content.md#generate-text-version).

* **[!UICONTROL Empty link is present in email body]**: controleer of alle koppelingen in uw e-mail juist zijn. Leer hoe te om inhoud en verbindingen in [deze sectie](create-email-content.md) te beheren.

* **[!UICONTROL Email size has exceeded the limit of 100KB]**: voor een optimale aflevering moet u ervoor zorgen dat de e-mailgrootte niet groter is dan 100 kB. Leer hoe u e-mailinhoud kunt bewerken in [deze sectie](create-email-content.md).

**Fouten**:

* **[!UICONTROL Subject Line Not Present]**: e-mailonderwerpregel is verplicht. Leer hoe te om het in [deze sectie ](create-email.md) te bepalen en te personaliseren.

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL Push Variant is empty]**: deze fout wordt weergegeven wanneer de hoofdtekst of titel van het pushbericht ontbreekt. Leer hoe u inhoud van pushberichten definieert in [deze sectie](create-push.md).

* **[!UICONTROL Email Variant is empty]**: deze fout wordt weergegeven wanneer de e-mailinhoud niet is geconfigureerd. Leer hoe u e-mailinhoud ontwerpt in [deze sectie](design-emails.md).

* **[!UICONTROL Preset doesn’t exist]**: U kunt uw bericht niet publiceren als de voorinstelling die u hebt geselecteerd, wordt verwijderd nadat het bericht is gemaakt. Als deze fout optreedt, selecteert u een andere voorinstelling in het bericht **[!UICONTROL Properties]**. Meer informatie over branding in [deze sectie](configuration/about-subdomain-delegation.md).

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**: de grootte van de pushmelding mag niet groter zijn dan 4 kB. U kunt deze limiet in acht nemen door het gebruik van afbeeldingen of emojis te beperken. Leer hoe u de inhoud van uw pushmelding beheert in [deze sectie](create-push.md).

>[!CAUTION]
>
> Om uw bericht te kunnen publiceren, moet u alle **error** alarm oplossen.

<!--Other issues can stop publication such as:
* The push notification title is empty-->
