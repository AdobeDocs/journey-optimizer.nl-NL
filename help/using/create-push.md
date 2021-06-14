---
title: Een pushmelding configureren
description: Meer informatie over het maken van een pushmelding in Journey Optimizer
feature: Overzicht
topic: Contentmanagement
role: User
level: Beginner
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 10%

---

# Een pushmelding maken {#create-push-notification}

![](assets/do-not-localize/badge.png)

Als u [een bericht](create-message.md) hebt gemaakt, klikt u op het tabblad **[!UICONTROL Push Notification]** om de instellingen en inhoud van het pushbericht te definiëren.

![](assets/create-content-push.png)

Gebruik de specifieke tabbladen om de instellingen voor pushmeldingen te definiëren voor besturingssystemen **iOS** en **Android**.

>[!NOTE]
>
>De sectie **[!UICONTROL Compose Message]** wordt gebruikt voor zowel de tabbladen **[!UICONTROL iOS]** als **[!UICONTROL Android]**. Elke wijziging in deze sectie is van toepassing op beide tabbladen.

## Titel en body

Als u uw bericht wilt samenstellen, klikt u op de velden **[!UICONTROL Title]** en **[!UICONTROL Body]**. Gebruik de Redacteur van de Uitdrukking om inhoud en verpersoonlijkingsgegevens te bepalen. Meer informatie over personalisatie in de Redacteur van de Uitdrukking in [deze sectie](personalization/personalize.md)

In het centrale gedeelte kunt u visualiseren hoe de pushmelding wordt weergegeven in iOS- en Android-apparaten.

## Bij klikken gedrag {#on-click-behavior}

Selecteer het gedrag wanneer een ontvanger op de hoofdtekst van het pushbericht klikt.

![](assets/title-body-push.png)

* Gebruik de optie **[!UICONTROL Open app]** om de toepassing te openen die is gekoppeld aan het bericht **[!UICONTROL Preset]**.
* Gebruik de optie **[!UICONTROL Deeplink]** om de ontvanger om te leiden naar een specifieke inhoud die zich binnen de toepassing bevindt. Voer de markering in het bijbehorende veld in.
* Gebruik de optie **[!UICONTROL Web URL]** om de ontvanger om te leiden naar een externe URL. Voer de URL in het bijbehorende veld in.

## Media toevoegen

In de iOS-versie van uw pushmelding kunt u een afbeelding, video of GIF toevoegen die binnen uw melding wordt weergegeven.

In de Android-versie kunt u alleen een afbeeldingspictogram en een afbeelding toevoegen voor uitgebreide berichten.

![](assets/push-config-add-media.png)

Er zijn twee opties beschikbaar. U kunt:

* Klik op de knop **[!UICONTROL Add media]** om een element te selecteren in **[!DNL Adobe Experience Manager Assets Essentials]**.

   Leer hoe u **[!DNL Adobe Experience Manager Assets Essentials]** in [deze pagina](assets-essentials.md) gebruikt.

* U kunt ook de URL van het medium invoeren door in het veld **[!UICONTROL Add media]** te klikken. In dat geval kunt u personalisatie toevoegen.

Nadat de media zijn toegevoegd, worden deze rechts van de meldingsinstantie weergegeven.


## Knoppen toevoegen

U kunt een bericht maken dat u kunt activeren door knoppen toe te voegen aan uw inhoud.

Als het apparaatscherm vergrendeld is, worden de volgende knoppen niet weergegeven: alleen de **Title** en het **Message** van de melding zijn zichtbaar. Als het apparaat ontgrendeld is, zien de ontvangers de knoppen.

In de iOS-versie kunt u maximaal vier knoppen toevoegen. In de Android-versie kunt u maximaal drie knoppen toevoegen.

Klik **[!UICONTROL Add button]** om instellingen te definiëren: het label en de bijbehorende actie. Mogelijke acties zijn hetzelfde als voor [gedrag bij klikken](#on-click-behavior).


>[!NOTE]
>
>Voor iOS gebruikt u het veld **[!UICONTROL iOS category]** om handelingen te koppelen aan een berichtencategorie.


## Een stille melding verzenden

Een stille pushmelding (of een achtergrondmelding) is een verborgen instructie die aan de toepassing wordt geleverd. Deze wordt bijvoorbeeld gebruikt om uw toepassing op de hoogte te stellen van de beschikbaarheid van nieuwe inhoud of om op de achtergrond een download te starten.

Selecteer de optie **[!UICONTROL Silent Notification]** om de toepassing stil te melden: in dit geval wordt de aanmelding rechtstreeks aan de toepassing overgedragen. Er wordt geen waarschuwing weergegeven op het scherm van het apparaat.

Gebruik de sectie **[!UICONTROL Custom data]** om sleutel-/waardeparen toe te voegen.

## Aangepaste gegevens

In **[!UICONTROL Custom data]** sectie, kunt u douanevariabelen aan de lading toevoegen, afhankelijk van uw mobiele toepassingsconfiguratie. Raadpleeg [deze sectie](push-gs.md) voor meer informatie over het instellen van pushmeldingen in Adobe Experience Platform en Adobe starten

## Geavanceerde opties

U kunt **[!UICONTROL Advanced options]** voor uw dupmelding vormen. De beschikbare parameters worden hieronder weergegeven:

| Parameter | Beschrijving |
|---------|---------|
| **[!UICONTROL Collapsible]** (iOS / Android) | Een inklapbaar bericht is een bericht dat door een nieuwe kan worden vervangen. Bijvoorbeeld, een toepassing die gebruikers met het recentste nieuws over een onderwerp bijwerkt. In dat geval is alleen het meest recente bericht relevant. Anderzijds is met niet-inklapbare berichten elk bericht belangrijk voor de client-app en moet het worden afgeleverd. |
| **[!UICONTROL Custom sound]** (iOS / Android) | Het geluid dat door de mobiele terminal moet worden afgespeeld wanneer het bericht wordt ontvangen. Het geluid moet in de app worden gebundeld. |
| **[!UICONTROL Badges]** (iOS / Android) | Een badge wordt gebruikt om het aantal nieuwe ongelezen meldingen direct op het applicatiepictogram te tonen. <br/>De badgewaarde verdwijnt zodra de gebruiker de nieuwe content in de applicatie opent of leest. Wanneer een melding op een apparaat wordt ontvangen, kan de badgewaarde voor de desbetreffende app worden vernieuwd of toegevoegd.<br/>Als u bijvoorbeeld het aantal ongelezen artikelen van uw klanten opslaat, kunt u personalisatie gebruiken om de unieke ongelezen waarde van de artikelbadge voor elke klant te verzenden. Voor meer verpersoonlijking, verwijs naar [deze sectie](personalization/personalize.md). |
| **[!UICONTROL Notification group]**  (alleen iOS) | Koppel een berichtgroep aan de pushmelding.<br/>Beginnend met iOS 12, staan de berichtgroepen u toe om berichtdraden en berichtonderwerpen in draad IDs te consolideren. Een merk kan bijvoorbeeld marketingmeldingen verzenden onder één groep-id, terwijl meer meldingen over operationele typen onder een of meer verschillende id&#39;s worden bewaard.<br/>U kunt dit illustreren met groupID: 123 &quot;check out the new spring collection of sweaters&quot; en groupID: 456 &quot;je pakket is geleverd&quot; berichtgroepen. In dit voorbeeld worden alle leveringsmeldingen gebundeld onder groep-id: 456 |
| **[!UICONTROL Notification channel]** (alleen Android) | Koppel een berichtkanaal aan de pushmelding.<br/>Vanaf Android 8.0 (API-niveau 26) moeten alle meldingen aan een kanaal worden toegewezen om te worden weergegeven. Raadpleeg de [documentatie voor Android-ontwikkelaars](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels) voor meer informatie. |
| **[!UICONTROL Add content-availability flag]** (alleen iOS) | Verstuurt de markering voor de beschikbare inhoud in de pushlading om ervoor te zorgen dat de app wordt geactiveerd zodra deze de pushmelding ontvangt. Dit betekent dat de app toegang kan krijgen tot de payload-gegevens.<br/> Dit werkt zelfs als de app op de achtergrond wordt uitgevoerd en zonder tussenkomst van de gebruiker (bijvoorbeeld tikken op pushmeldingen). Dit is echter niet van toepassing als de app niet wordt uitgevoerd. Zie de [Apple Developer documentatie](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html) voor meer informatie hierover. |
| **[!UICONTROL Add mutable-content flag]** (alleen iOS) | Verzendt de markering voor meerbare inhoud in de pushlading en zorgt ervoor dat de inhoud van het pushbericht kan worden gewijzigd door een uitbreiding van de berichtservice die in iOS SDK is opgegeven. Zie [Apple Developer documentatie](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html) voor meer informatie hierover.<br/>Vervolgens kunt u uw mobiele app-extensies gebruiken om de inhoud of presentatie van aankomende pushberichten die zijn verzonden van  [!DNL Journey Optimizer] bijvoorbeeld, verder te wijzigen. Gebruikers kunnen deze optie gebruiken om gegevens te decoderen, de tekst van de hoofdtekst of titel van een melding te wijzigen, een thread-id aan een melding toe te voegen, enz. |
| **[!UICONTROL Notification visibility]** (alleen Android) | Hiermee definieert u de zichtbaarheid van het pushbericht. <br/><b>De </b> private zal het bericht op alle lockscreens tonen, maar verborgen gevoelige of privé informatie over veilige lockscreens. <br/><b>In </b> Publications wordt de volledige kennisgeving op alle schermen weergegeven. <br/><b></b> Secretaris zal geen enkel deel van het bericht op een veilig sluitscherm openbaren. <br/>Raadpleeg de documentatie bij [ Android-ontwikkelaars voor meer informatie hierover](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Notification priority]** (alleen Android) | Hiermee definieert u het belang van de pushmelding van Laag tot Max. Dit bepaalt hoe &quot;indringend&quot;de dupmelding zal zijn wanneer het wordt geleverd. Raadpleeg voor meer informatie de [documentatie voor Android-ontwikkelaars](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** (alleen Android) | Hiermee stelt u een hoge of normale prioriteit in voor uw pushberichten. Zie de [Google Developer-documentatie](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message) voor meer informatie over de prioriteit van berichten. |


**Verwante onderwerpen**

<!--
* [Understand push notification flow](push-gs.md)
-->

* [Pushkanaal configureren](push-gs.md)
* [Een nieuw bericht maken](create-message.md)
* [Een bericht toevoegen tijdens een rit](building-journeys/journeys-message.md)

