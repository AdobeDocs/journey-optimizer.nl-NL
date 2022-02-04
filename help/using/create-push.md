---
title: Een pushmelding configureren
description: Meer informatie over het maken van een pushmelding in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 6bb0248c8bd3c15ff28e841b06a413dca83b354f
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 10%

---

# Een pushmelding maken {#create-push-notification}

Eenmaal [een bericht gemaakt](create-message.md)klikt u op de knop **[!UICONTROL Push Notification]** om de instellingen en inhoud van de pushmelding te definiëren.

![](assets/create-content-push.png)

Gebruik de specifieke tabbladen om de instellingen voor pushmeldingen te definiëren voor **iOS** en **Android** besturingssystemen.

>[!NOTE]
>
>De **[!UICONTROL Compose Message]** deze sectie wordt door beide **[!UICONTROL iOS]** en **[!UICONTROL Android]** tabs. Elke wijziging in deze sectie is van toepassing op beide tabbladen.

## Titel en body

Als u uw bericht wilt samenstellen, klikt u op de knop **[!UICONTROL Title]** en **[!UICONTROL Body]** velden. Gebruik de Redacteur van de Uitdrukking om inhoud en verpersoonlijkingsgegevens te bepalen. Meer informatie over personalisatie in de Expressieeditor vindt u in [deze sectie](personalization/personalize.md)

In het gedeelte voor voorvertoning van apparaten kunt u visualiseren hoe de pushmelding wordt weergegeven op iOS- en Android-apparaten.

## Bij klikken, gedrag {#on-click-behavior}

Selecteer het gedrag wanneer een ontvanger op de hoofdtekst van het pushbericht klikt.

![](assets/title-body-push.png)

* Gebruik de **[!UICONTROL Open app]** optie om de toepassing te openen die aan het bericht is gekoppeld **[!UICONTROL Preset]**.
* Gebruik de **[!UICONTROL Deeplink]** optie om de ontvanger om te leiden naar specifieke inhoud binnen de toepassing. Voer de markering in het bijbehorende veld in.
* Gebruik de **[!UICONTROL Web URL]** om de ontvanger om te leiden naar een externe URL. Voer de URL in het bijbehorende veld in.

## Media toevoegen

In de iOS-versie van uw pushmelding kunt u een afbeelding, video of GIF toevoegen die binnen uw melding wordt weergegeven.

In de Android-versie kunt u alleen een afbeeldingspictogram en een afbeelding toevoegen voor uitgebreide berichten.

![](assets/push-config-add-media.png)

Er zijn twee opties beschikbaar. U kunt:

* Klik op de knop **[!UICONTROL Add media]** knop om een element te selecteren in **[!DNL Adobe Experience Manager Assets Essentials]**.

   Leren gebruiken **[!DNL Adobe Experience Manager Assets Essentials]** in [deze pagina](assets-essentials.md).

* U kunt ook de URL van het medium invoeren door op het tabblad **[!UICONTROL Add media]** veld. In dat geval kunt u personalisatie toevoegen.

Nadat de media zijn toegevoegd, worden deze rechts van de meldingsinstantie weergegeven.

## Knoppen toevoegen

U kunt een bericht maken dat u kunt activeren door knoppen toe te voegen aan uw inhoud.

Als het apparaatscherm vergrendeld is, worden de volgende knoppen niet weergegeven: alleen de **Titel** en de **Bericht** van de kennisgeving zichtbaar zijn. Als het apparaat ontgrendeld is, zien de ontvangers de knoppen.

In de iOS-versie kunt u maximaal vier knoppen toevoegen. In de Android-versie kunt u maximaal drie knoppen toevoegen.

>[!NOTE]
>
>Voor iOS gebruikt u de **[!UICONTROL iOS category]** veld voor het koppelen van handelingen aan een berichtencategorie.

Klikken **[!UICONTROL Add button]** instellingen definiëren: het label en de bijbehorende actie. Mogelijke acties zijn hetzelfde als voor [klikgedrag](#on-click-behavior).

Klikken **[!UICONTROL Expand view]** om een voorvertoning van uw aangepaste knoppen weer te geven.

![](assets/push_buttons.png)

## Een stille melding verzenden

Een stille pushmelding (of een achtergrondmelding) is een verborgen instructie die aan de toepassing wordt geleverd. Deze wordt bijvoorbeeld gebruikt om uw toepassing op de hoogte te stellen van de beschikbaarheid van nieuwe inhoud of om op de achtergrond een download te starten.

Selecteer **[!UICONTROL Silent Notification]** optie om de toepassing ongemerkt op de hoogte te stellen: in dit geval wordt de aanmelding rechtstreeks aan de toepassing overgedragen. Er wordt geen waarschuwing weergegeven op het scherm van het apparaat.

Gebruik de **[!UICONTROL Custom data]** om sleutelwaardeparen toe te voegen.

## Aangepaste gegevens

In de **[!UICONTROL Custom data]** kunt u aangepaste variabelen toevoegen aan de payload, afhankelijk van de configuratie van uw mobiele toepassing. Raadpleeg voor meer informatie over het instellen van pushmeldingen in Adobe Experience Platform en Adobe starten de opties voor [deze sectie](push-gs.md)

## Geavanceerde opties

U kunt configureren **[!UICONTROL Advanced options]** voor uw pushmelding. De beschikbare parameters worden hieronder weergegeven:

| Parameter | Beschrijving |
|---------|---------|
| **[!UICONTROL Collapsible]** (iOS / Android) | Een inklapbaar bericht is een bericht dat door een nieuw bericht kan worden vervangen als het verouderd is geworden. Een veelvoorkomend gebruik van samenvouwbare berichten is berichten die worden gebruikt om een mobiele toepassing te vertellen gegevens van de server te synchroniseren. Een voorbeeld hiervan is een sport-app waarmee gebruikers de laatste score krijgen. Alleen het meest recente bericht is relevant. Aan de andere kant is met niet-inklapbaar bericht zeer belangrijk voor de client-app en moet het worden afgeleverd. |
| **[!UICONTROL Custom sound]** (iOS / Android) | Het geluid dat door de mobiele terminal moet worden afgespeeld wanneer het bericht wordt ontvangen. Het geluid moet in de app worden gebundeld. |
| **[!UICONTROL Badges]** (iOS / Android) | Een badge wordt gebruikt om het aantal nieuwe ongelezen meldingen direct op het applicatiepictogram te tonen. <br/>De badgewaarde verdwijnt zodra de gebruiker de nieuwe content in de applicatie opent of leest. Wanneer een melding op een apparaat wordt ontvangen, kan de badgewaarde voor de desbetreffende app worden vernieuwd of toegevoegd.<br/>Als u bijvoorbeeld het aantal ongelezen artikelen van uw klanten opslaat, kunt u personalisatie gebruiken om de unieke ongelezen waarde van de artikelbadge voor elke klant te verzenden. Voor meer verpersoonlijking, verwijs naar [deze sectie](personalization/personalize.md). |
| **[!UICONTROL Notification group]**  (alleen iOS) | Koppel een berichtgroep aan de pushmelding.<br/>Beginnend met iOS 12, staan de berichtgroepen u toe om berichtdraden en berichtonderwerpen in draad IDs te consolideren. Een merk kan bijvoorbeeld marketingmeldingen verzenden onder één groep-id, terwijl meer meldingen over operationele typen onder een of meer verschillende id&#39;s worden bewaard.<br/>U kunt dit illustreren met groupID: 123 &quot;check out the new spring collection of sweaters&quot; en groupID: 456 &quot;je pakket is geleverd&quot; berichtgroepen. In dit voorbeeld worden alle leveringsmeldingen gebundeld onder groep-id: 456 |
| **[!UICONTROL Notification channel]** (alleen Android) | Koppel een berichtkanaal aan de pushmelding.<br/>Vanaf Android 8.0 (API-niveau 26) moeten alle meldingen aan een kanaal worden toegewezen om te worden weergegeven. Raadpleeg voor meer informatie de [Documentatie voor ontwikkelaars van Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Add content-availability flag]** (alleen iOS) | Verstuurt de markering voor de beschikbare inhoud in de pushlading om ervoor te zorgen dat de app wordt geactiveerd zodra deze de pushmelding ontvangt. Dit betekent dat de app toegang kan krijgen tot de payload-gegevens.<br/> Dit werkt zelfs als de app op de achtergrond wordt uitgevoerd en zonder tussenkomst van de gebruiker (bijvoorbeeld tikken op pushmeldingen). Dit is echter niet van toepassing als de app niet wordt uitgevoerd. Zie de [Apple Developer documentatie](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html) voor meer informatie hierover. |
| **[!UICONTROL Add mutable-content flag]** (alleen iOS) | Verzendt de markering voor gemuteerde inhoud in de pushlading en zorgt ervoor dat de inhoud van het pushbericht kan worden gewijzigd door een uitbreiding van de berichtgevingsservice die is opgegeven in iOS SDK. Zie [Apple Developer documentatie](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html) voor meer informatie hierover.<br/>Vervolgens kunt u uw mobiele app-extensies gebruiken om de inhoud of presentatie van aankomende pushmeldingen die zijn verzonden van [!DNL Journey Optimizer]. Gebruikers kunnen deze optie bijvoorbeeld gebruiken om gegevens te decoderen, de tekst van de hoofdtekst of titel van een melding te wijzigen, een thread-id aan een melding toe te voegen, enzovoort. |
| **[!UICONTROL Notification visibility]** (alleen Android) | Hiermee definieert u de zichtbaarheid van het pushbericht. <br/><b>Persoonlijk</b> toont de melding op alle vergrendelingsschermen, maar verbergt gevoelige of persoonlijke informatie op veilige vergrendelingsschermen. <br/><b>Openbaar</b> de volledige kennisgeving wordt op alle vergrendelingsschermen weergegeven. <br/><b>Geheim</b> geen enkel deel van de melding zichtbaar maken op een veilig vergrendelingssysteem. <br/>Raadpleeg voor meer informatie de [Documentatie voor ontwikkelaars van Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Notification priority]** (alleen Android) | Hiermee definieert u het belang van de pushmelding van Laag tot Max. Dit bepaalt hoe &quot;indringend&quot;de dupmelding zal zijn wanneer het wordt geleverd. Raadpleeg voor meer informatie de [Documentatie voor ontwikkelaars van Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** (alleen Android) | Hiermee stelt u een hoge of normale prioriteit in voor uw pushberichten. Zie de [Google Developer-documentatie](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message) voor meer informatie over de prioriteit van berichten. |

**Verwante onderwerpen**

<!--
* [Understand push notification flow](push-gs.md)
-->

* [Pushkanaal configureren](push-gs.md)
* [Een nieuw bericht maken](create-message.md)
* [Een bericht toevoegen in een journey](building-journeys/journeys-message.md)
