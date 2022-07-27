---
title: Waarschuwingen in berichten
description: Leer hoe te om berichtinhoudbevestiging te controleren en problemen op te lossen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---

# Waarschuwingen bij uw berichten controleren {#messages-alerts}

## Controleert vóór verzending {#message-alerting}

Terwijl u uw berichten ontwerpt, worden waarschuwingen weergegeven in de interface wanneer er geen sleutelinstellingen aanwezig zijn.

Waarschuwingen worden rechtsboven in het scherm weergegeven wanneer u de inhoud van het bericht bewerkt.

![](assets/alerts-details.png)

>[!NOTE]
>
>Als deze knop niet wordt weergegeven, is er geen melding gevonden.

Er kunnen twee typen waarschuwingen optreden:

* **Waarschuwingen** verwijzen naar aanbevelingen en beste praktijken. Er wordt bijvoorbeeld een bericht weergegeven als de koppeling om te weigeren ontbreekt.

* **Fouten** voorkomt dat u de reis test of activeert zolang deze niet is opgelost. U wordt bijvoorbeeld in een bericht gewaarschuwd dat de onderwerpregel ontbreekt.

Alle mogelijke waarschuwingen en fouten zijn gedetailleerd [onder](#alerts-and-warnings).

>[!CAUTION]
>
> U moet alles oplossen **fout** signaleert alvorens de reis te testen of te activeren gebruikend het bericht.

## Lijst met waarschuwingen en fouten {#alerts-and-warnings}

De instellingen en elementen die door het systeem zijn gecontroleerd, worden hieronder weergegeven. U zult ook informatie over hoe te om uw configuratie aan te passen om de overeenkomstige kwesties op te lossen vinden.

**Waarschuwingen**:

* **[!UICONTROL The opt-out link is not present in the email body]**: u kunt het beste een koppeling zonder abonnement toevoegen aan uw e-mailadres. Leer hoe u deze kunt configureren in [deze sectie](consent.md#opt-out-management).

   >[!NOTE]
   >
   >E-mailberichten van het type Marketing moeten een opt-out-koppeling bevatten, die niet vereist is voor transactiemeldingen. De berichtcategorie (**[!UICONTROL Marketing]** of **[!UICONTROL Transactional]**) wordt gedefinieerd op de [kanaaloppervlak](../configuration/channel-surfaces.md#email-type) (d.w.z. vooraf ingestelde berichten) en wanneer [het bericht maken](get-started-content.md#create-new-message).

* **[!UICONTROL Text version of HTML is empty]**: vergeet niet een tekstversie van uw e-mailhoofdtekst te definiëren, omdat deze wordt gebruikt wanneer HTML-inhoud niet kan worden weergegeven. Leer hoe u de tekstversie maakt in [deze sectie](../design/text-version-email.md).

* **[!UICONTROL Empty link is present in email body]**: controleer of alle koppelingen in uw e-mail juist zijn. Leer hoe u inhoud en koppelingen kunt beheren in [deze sectie](../design/create-email-content.md).

* **[!UICONTROL Email size has exceeded the limit of 100KB]**: voor een optimale aflevering moet u ervoor zorgen dat de e-mailgrootte niet groter is dan 100 kB. Leer hoe u e-mailinhoud kunt bewerken in [deze sectie](../design/create-email-content.md).

**Fouten**:

* **[!UICONTROL The subject line is missing]**: e-mailonderwerpregel is verplicht. Leer hoe u het kunt definiëren en personaliseren in [deze sectie](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL The push version of the message is empty]**: deze fout wordt weergegeven wanneer de hoofdtekst of titel van het pushbericht ontbreekt. Leer hoe u inhoud voor pushmeldingen definieert in [deze sectie](create-push.md).

* **[!UICONTROL The email version of the message is empty]**: deze fout wordt weergegeven wanneer de e-mailinhoud niet is geconfigureerd. Leer hoe u e-mailinhoud ontwerpt in [deze sectie](../design/design-emails.md).

* **[!UICONTROL Surface doesn’t exist]**: U kunt uw bericht niet gebruiken als het geselecteerde oppervlak wordt verwijderd na het maken van het bericht. Als deze fout optreedt, selecteert u een ander oppervlak in het bericht **[!UICONTROL Properties]**. Meer informatie over kanaaloppervlakken in [deze sectie](../configuration/channel-surfaces.md).

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**: de grootte van de pushmelding mag niet groter zijn dan 4 kB. U kunt deze limiet in acht nemen door het gebruik van afbeeldingen of emojis te beperken. Leer hoe u de inhoud van uw pushmelding beheert in [deze sectie](create-push.md).

>[!CAUTION]
>
> Als je je bericht wilt gebruiken, moet je alles oplossen **fout** waarschuwingen.

<!--Other issues can stop publication such as:
* The push notification title is empty-->
