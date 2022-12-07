---
solution: Journey Optimizer
product: journey optimizer
title: Een pushmelding ontwerpen
description: Leer hoe u een pushmelding ontwerpt in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1215'
ht-degree: 9%

---

# Een pushmelding ontwerpen {#design-push-notification}

## Titel en body {#push-title-body}

Als u uw bericht wilt samenstellen, klikt u op de knop **[!UICONTROL Title]** en **[!UICONTROL Body]** velden. Gebruik de uitdrukkingsredacteur om inhoud te bepalen, gegevens te personaliseren en dynamische inhoud toe te voegen. Meer informatie over [personalisatie](../personalization/personalize.md) en [dynamische inhoud](../personalization/get-started-dynamic-content.md) in de Uitdrukking redacteur.

In het gedeelte voor voorvertoning van apparaten kunt u visualiseren hoe de pushmelding wordt weergegeven op iOS- en Android-apparaten.

## Bij klikken, gedrag {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Informatie over klikgedrag"
>abstract="Selecteer het gedrag wanneer een ontvanger op de hoofdtekst van het pushbericht klikt."

U kunt het gedrag selecteren wanneer een gebruiker op de hoofdtekst van het pushbericht klikt.

![](assets/title-body-push.png)

* Selecteer de optie **[!UICONTROL Open app]** optie. De toepassing die aan de melding is gekoppeld, wordt gedefinieerd in het dialoogvenster [kanaaloppervlak](../configuration/channel-surfaces.md) (d.w.z. voorinstelling bericht).
* Als u de gebruiker wilt omleiden naar een bepaald stuk inhoud in een app, selecteert u de optie **[!UICONTROL Deeplink]** optie.  De specifieke inhoud kan een specifieke weergave, een bepaalde sectie van een pagina of een bepaald tabblad zijn. Als de optie is geselecteerd, voert u de koppeling in het bijbehorende veld in.
* Als u de gebruiker wilt omleiden naar een externe URL, gebruikt u de opdracht **[!UICONTROL Web URL]** optie. Wanneer de optie is geselecteerd, voert u de URL in het bijbehorende veld in.

## Media toevoegen {#add-media-push}

In de iOS-versie van uw pushmelding kunt u een afbeelding, video of GIF toevoegen die binnen uw melding wordt weergegeven.

In de Android-versie kunt u alleen een afbeeldingspictogram en een afbeelding toevoegen voor uitgebreide berichten.

![](assets/push-config-add-media.png)

Er zijn twee opties beschikbaar. U kunt:

* Gebruik de **[!UICONTROL Add media]** knop om een element te selecteren in **[!DNL Adobe Experience Manager Assets Essentials]**.

   Leren gebruiken **[!DNL Adobe Experience Manager Assets Essentials]** in [deze pagina](../email/assets-essentials.md).

* U kunt ook de URL van het medium invoeren in het dialoogvenster **[!UICONTROL Add media]** veld. In dat geval kunt u personalisatie toevoegen aan de URL.

Nadat de media zijn toegevoegd, worden deze rechts van de meldingsinstantie weergegeven.

## Knoppen toevoegen {#add-buttons-push}

Maak een actionable melding door knoppen toe te voegen aan uw pushinhoud.

Als het apparaatscherm vergrendeld is, worden de volgende knoppen niet weergegeven: alleen de **Titel** en de **Bericht** van de kennisgeving zichtbaar zijn. Als het apparaat ontgrendeld is, zien de ontvangers de knoppen.

In de iOS-versie kunt u maximaal vier knoppen toevoegen. In de Android-versie kunt u maximaal drie knoppen toevoegen.

>[!NOTE]
>
>Voor iOS gebruikt u de **[!UICONTROL iOS category]** veld voor het koppelen van handelingen aan een berichtencategorie.

1. Gebruik de **[!UICONTROL Add button]** instellingen definiëren: het label en de bijbehorende actie. Mogelijke acties zijn hetzelfde als voor [klikgedrag](#on-click-behavior).

1. Gebruik de **[!UICONTROL Expand view]** onder de centrale voorvertoning om een voorvertoning van uw persoonlijke knoppen weer te geven.

![](assets/push_buttons.png)

## Een stille melding verzenden {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="Informatie over stille meldingen"
>abstract="Verzend berichten zonder de gebruiker te storen, worden de berichten niet getoond in het berichtcentrum of de berichtbar."

Een stille pushmelding (of een achtergrondmelding) is een verborgen instructie die aan de toepassing wordt geleverd. Deze wordt bijvoorbeeld gebruikt om uw toepassing op de hoogte te stellen van de beschikbaarheid van nieuwe inhoud of om op de achtergrond een download te starten.

Selecteer **[!UICONTROL Silent Notification]** optie om de toepassing ongemerkt op de hoogte te stellen: in dit geval wordt de aanmelding rechtstreeks aan de toepassing overgedragen. Er wordt geen waarschuwing weergegeven op het scherm van het apparaat.

Gebruik de **[!UICONTROL Custom data]** om sleutelwaardeparen toe te voegen.

## Aangepaste gegevens

In de **[!UICONTROL Custom data]** kunt u aangepaste variabelen toevoegen aan de payload, afhankelijk van de configuratie van uw mobiele toepassing. Raadpleeg voor meer informatie over het instellen van pushmeldingen in Adobe Experience Platform en Adobe starten de opties voor [deze sectie](push-gs.md)

## Geavanceerde opties {#advanced-options-push}

U kunt configureren **[!UICONTROL Advanced options]** voor uw pushmelding. De beschikbare parameters worden hieronder weergegeven:

| Parameter | Beschrijving |
|---------|---------|
| **[!UICONTROL Collapsible]** (iOS / Android) | Een inklapbaar bericht is een bericht dat door een nieuw bericht kan worden vervangen als het verouderd is geworden. Een veelvoorkomend gebruik van samenvouwbare berichten is berichten die worden gebruikt om een mobiele toepassing te vertellen gegevens van de server te synchroniseren. Een voorbeeld hiervan is een sport-app waarmee gebruikers de laatste score krijgen. Alleen het meest recente bericht is relevant. Aan de andere kant is met niet-inklapbaar bericht zeer belangrijk voor de client-app en moet het worden afgeleverd. |
| **[!UICONTROL Custom sound]** (iOS / Android) | Het geluid dat door de mobiele terminal moet worden afgespeeld wanneer het bericht wordt ontvangen. Het geluid moet in de app worden gebundeld. |
| **[!UICONTROL Badges]** (iOS / Android) | Een badge wordt gebruikt om het aantal nieuwe ongelezen meldingen direct op het applicatiepictogram te tonen. <br/>De badgewaarde verdwijnt zodra de gebruiker de nieuwe content in de applicatie opent of leest. Wanneer een melding op een apparaat wordt ontvangen, kan de badgewaarde voor de desbetreffende app worden vernieuwd of toegevoegd.<br/>Als u bijvoorbeeld het aantal ongelezen artikelen van uw klanten opslaat, kunt u personalisatie gebruiken om de unieke ongelezen waarde van de artikelbadge voor elke klant te verzenden. Voor meer verpersoonlijking, verwijs naar [deze sectie](../personalization/personalize.md). |
| **[!UICONTROL Notification group]**  (alleen iOS) | Koppel een berichtgroep aan de pushmelding.<br/>Beginnend met iOS 12, staan de berichtgroepen u toe om berichtdraden en berichtonderwerpen in draad IDs te consolideren. Een merk kan bijvoorbeeld marketingmeldingen verzenden onder één groep-id, terwijl meer meldingen over operationele typen onder een of meer verschillende id&#39;s worden bewaard.<br/>U kunt dit illustreren met groupID: 123 &quot;check out the new spring collection of sweaters&quot; en groupID: 456 &quot;je pakket is geleverd&quot; berichtgroepen. In dit voorbeeld worden alle leveringsmeldingen gebundeld onder groep-id: 456 |
| **[!UICONTROL Notification channel]** (alleen Android) | Koppel een berichtkanaal aan de pushmelding.<br/>Vanaf Android 8.0 (API-niveau 26) moeten alle meldingen aan een kanaal worden toegewezen om te worden weergegeven. Raadpleeg voor meer informatie de [Documentatie voor ontwikkelaars van Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Add content-availability flag]** (alleen iOS) | Verstuurt de markering voor de beschikbare inhoud in de pushlading om ervoor te zorgen dat de app wordt geactiveerd zodra deze de pushmelding ontvangt. Dit betekent dat de app toegang kan krijgen tot de payload-gegevens.<br/> Dit werkt zelfs als de app op de achtergrond wordt uitgevoerd en zonder tussenkomst van de gebruiker (bijvoorbeeld tikken op pushmeldingen). Dit is echter niet van toepassing als de app niet wordt uitgevoerd. Zie de [Apple Developer documentatie](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html) voor meer informatie hierover. |
| **[!UICONTROL Add mutable-content flag]** (alleen iOS) | Verzendt de markering voor gemuteerde inhoud in de pushlading en zorgt ervoor dat de inhoud van het pushbericht kan worden gewijzigd door een uitbreiding van de berichtgevingsservice die is opgegeven in iOS SDK. Zie [Apple Developer documentatie](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html) voor meer informatie hierover.<br/>Vervolgens kunt u uw mobiele app-extensies gebruiken om de inhoud of presentatie van aankomende pushmeldingen die zijn verzonden van [!DNL Journey Optimizer]. Gebruikers kunnen deze optie bijvoorbeeld gebruiken om gegevens te decoderen, de tekst van de hoofdtekst of titel van een melding te wijzigen, een thread-id aan een melding toe te voegen, enzovoort. |
| **[!UICONTROL Notification visibility]** (alleen Android) | Hiermee definieert u de zichtbaarheid van het pushbericht. <br/><b>Persoonlijk</b> toont de melding op alle vergrendelingsschermen, maar verbergt gevoelige of persoonlijke informatie op veilige vergrendelingsschermen. <br/><b>Openbaar</b> de volledige kennisgeving wordt op alle vergrendelingsschermen weergegeven. <br/><b>Geheim</b> geen enkel deel van de melding zichtbaar maken op een veilig vergrendelingssysteem. <br/>Raadpleeg voor meer informatie de [Documentatie voor ontwikkelaars van Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Notification priority]** (alleen Android) | Hiermee definieert u het belang van de pushmelding van Laag tot Max. Dit bepaalt hoe &quot;indringend&quot;de dupmelding zal zijn wanneer het wordt geleverd. Raadpleeg voor meer informatie de [Documentatie voor ontwikkelaars van Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** (alleen Android) | Hiermee stelt u een hoge of normale prioriteit in voor uw pushberichten. Zie de [Google Developer-documentatie](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message) voor meer informatie over de prioriteit van berichten. |


