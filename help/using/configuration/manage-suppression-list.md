---
title: De vervolgkeuzelijst beheren
description: 'Leer hoe u de lijst met Journey Optimizer-suppressies kunt openen en beheren '
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Applicatie-instellingen
topic: Beheer
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 1%

---


# De vervolgkeuzelijst beheren {#manage-suppression-list}

Met [!DNL Journey Optimizer] kunt u alle e-mailadressen controleren die automatisch van het verzenden van een reis worden uitgesloten, zoals:

* Adressen die ongeldig (harde grenzen) zijn, of die constant zachte stuit, en zouden uw e-mailreputatie kunnen negatief beïnvloeden als u hen in uw leveringen blijft omvatten.
* Ontvangers die op een of andere manier een spamklacht indienen tegen een van uw e-mailberichten.

<!--Profiles who unsubscribe from your sendings. Learn more on [opting-out](../consent.md). NOT TRUE as confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

Dergelijke e-mailadressen worden automatisch verzameld in de Journey Optimizer **suppressielijst**. Meer informatie vindt u in [deze sectie](../suppression-list.md).

## De lijst met onderdrukking openen {#access-suppression-list}

Als u de gedetailleerde lijst met uitgesloten e-mailadressen wilt openen, opent u het menu **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]** en klikt u op de koppeling **[!UICONTROL View suppression lists]**.

![](../assets/suppression-list-link.png)

Er zijn filters beschikbaar waarmee u door de lijst kunt bladeren.

![](../assets/suppression-list-filters.png)

<!--suppression date,  category and reason, but on staging, only creation date filter is available-->

<!--You can also download the list as a CSV file for analysis and reporting purpose. Won't be available.-->

## Onderdrukkingscategorieën en redenen {#suppression-categories-and-reasons}

Wanneer een bericht niet aan een e-mailadres kan worden geleverd, bepaalt Journey Optimizer waarom de levering is mislukt en koppelt het aan een suppressiecategorie.

De onderdrukkingscategorieën zijn als volgt:

* **Hard**: Het e-mailadres wordt direct naar de onderdrukkingslijst verzonden.

* **Zacht**: Zachte fouten verzenden een adres naar de onderdrukkingslijst zodra de foutenteller de grensdrempel bereikt. [Meer informatie over opnieuw proberen](retries.md)

* **Genegeerd**:
   * Wanneer de fout voor een geldig e-mailadres maar waarvan bekend is dat deze tijdelijk is, zoals een mislukte verbindingspoging of een tijdelijk technisch probleem, is opgetreden, wordt het e-mailadres toegevoegd aan de suppressielijst zodra de foutenteller de limietdrempel bereikt. [Meer weten over nieuwe pogingen](retries.md)?
   * Wanneer de fout het resultaat is van een spamklacht, wordt het e-mailadres van de ontvanger die de klacht heeft ingediend onmiddellijk naar de onderdrukkingslijst verzonden.

<!--**Manual**: You can also manually add an email address to the suppression list. => Manual category will be available when manually adding an address to the suppression list (via API)-->

>[!NOTE]
>
>Meer informatie over zachte grenzen en harde stuitingen vindt u in de sectie [Typen leveringsfouten](../suppression-list.md#delivery-failures).

Voor elk e-mailadres dat wordt vermeld, kunt u **[!UICONTROL Reason]** ook controleren om het uit te sluiten en de datum/tijd het aan de onderdrukkingslijst werd toegevoegd.

![](../assets/suppression-list-temp.png)
<!--to replace with suppression-list.png when Manual category is available (through API)-->

De mogelijke redenen van een leveringsfout zijn:

| Reden | Beschrijving | Onderdrukkingscategorie |
---------|----------|--------- |
| **[!UICONTROL Undetermined]** | De stuitreden die van de ontvankelijke Agent van de Overdracht van het domeinbericht (MTA) werd ontvangen kon niet worden geïdentificeerd. | Genegeerd |
| **[!UICONTROL Invalid Recipient]** | De ontvanger is ongeldig of bestaat niet. | Hard |
| **[!UICONTROL Soft Bounce]** | De berichtzachte die tegen een andere reden dan de zachte fouten in deze lijst worden vermeld, zoals wanneer het verzenden over het toegestane tarief door ISP wordt geadviseerd. | Zacht |
| **[!UICONTROL DNS Failure]** | Het bericht dat als gevolg van een DNS-fout is teruggestuurd. | Zacht |
| **[!UICONTROL Mailbox Full]** | Het bericht dat door de brievenbus van de ontvanger wordt teruggestuurd die volledig is en niet meer berichten kan goedkeuren. | Zacht |
| **[!UICONTROL Too Large]** | Het bericht werd teruggestuurd omdat het te groot was voor de ontvanger. [Er worden ](retries.md) retriesets uitgevoerd: U kunt de berichtgrootte bewerken en opnieuw injecteren voor levering. | Genegeerd |
| **[!UICONTROL Timeout]** | Time-out van het bericht. Dit betekent dat het bericht &#39;soft&#39; wordt teruggedraaid en dat de limiet voor het opnieuw proberen van het bericht is bereikt (3,5 dagen). | Genegeerd |
| **[!UICONTROL Admin Failure]** | Het bericht werd ontbroken volgens het beleid dat door de verzendende systeembeheerder wordt gevormd. <!--For example, if emails are blackholed at the global, domain or binding level using the "blackhole" directive, this bounce code is used.--> | Genegeerd |
| **[!UICONTROL Generic Bounce: No RCPT]** | Geen ontvanger kon voor het bericht worden bepaald. | Genegeerd |
| **[!UICONTROL Generic Bounce]** | Het bericht is om niet-opgegeven redenen mislukt. | Genegeerd |
| **[!UICONTROL Mail Block]** | Het bericht werd geblokkeerd door de ontvanger (d.w.z. ontvanger MTA). | Genegeerd |
| **[!UICONTROL Spam Block]** | Het bericht werd geblokkeerd door de ontvanger zoals komend uit een bekende spambron. Het zou bijvoorbeeld een verzendend IP blok kunnen zijn. | Genegeerd |
| **[!UICONTROL Spam Content]** | De berichtinhoud werd geblokkeerd door de ontvanger (ontvanger MTA) als spam. | Genegeerd |
| **[!UICONTROL Prohibited Attachment]** | Het bericht werd geblokkeerd door de ontvanger omdat het een gehechtheid bevatte. | Genegeerd |
| **[!UICONTROL Relaying Denied]** | Het bericht is geblokkeerd door de ontvanger omdat het opnieuw afspelen niet is toegestaan. | Zacht |
| **[!UICONTROL Auto-Reply]** | Het bericht is een auto-antwoord/vakantie-post. | Genegeerd |
| **[!UICONTROL Transient Failure]** | De verzending van berichten is tijdelijk vertraagd. | Genegeerd |
| **[!UICONTROL Challenge-Response]** | De boodschap is een uitdaging-antwoord sonde. | Zacht |

>[!NOTE]
>
>Gebruikers met een abonnement ontvangen geen e-mails van [!DNL Journey Optimizer]. Daarom kunnen hun e-mailadressen niet naar de onderdrukkingslijst worden verzonden. Hun keuze wordt op het niveau van de Experience Platform behandeld. Meer informatie over [opting-out](../consent.md).

<!--
Removed from the table provided by SparkPost/Momentum:
| **[!UICONTROL Subscribe]** | The message is a subscribe request. | Ignored |
| **[!UICONTROL Unsubscribe]** | The message is an unsubscribe request. | Hard |
-->

<!--Note to add eventually: If a user is subscribed and [!DNL Journey Optimizer] fails to send emails to their subscribed email address, they will get added to the suppression list. (not sure it's possible to subscribe through AJO or need to find reference to Experience Platform doc?)-->


