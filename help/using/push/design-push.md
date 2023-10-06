---
solution: Journey Optimizer
product: journey optimizer
title: Een pushmelding ontwerpen
description: Leer hoe u een pushmelding ontwerpt in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 6f6d693d-11f2-48b7-82a8-171829bf8045
source-git-commit: adcfff1cb8bb2ae98d41e4071f56a137e52ee56a
workflow-type: tm+mt
source-wordcount: '1364'
ht-degree: 8%

---

# Een pushmelding ontwerpen {#design-push-notification}

## Titel en body {#push-title-body}

>[!CONTEXTUALHELP]
>id="ajo-message-push-compose"
>title="Pas uw pushmelding aan."
>abstract="Als u uw bericht wilt samenstellen, voert u de inhoud in de velden Titel en Tekst in. Als u personalisatietokens wilt opnemen, opent u het dialoogvenster voor personalisatie."

Klik op de knop **[!UICONTROL Title]** en **[!UICONTROL Body]** velden. Gebruik de uitdrukkingsredacteur om inhoud te bepalen, gegevens te personaliseren en dynamische inhoud toe te voegen. Meer informatie over [personalisatie](../personalization/personalize.md) en [dynamische inhoud](../personalization/get-started-dynamic-content.md) in de Uitdrukking redacteur.

In het gedeelte voor voorvertoning van apparaat kunt u visualiseren hoe de pushmelding wordt weergegeven op iOS- en Android-apparaten.

## Bij klikken, gedrag {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Informatie over klikgedrag"
>abstract="Selecteer het gedrag wanneer een ontvanger op de hoofdtekst van het pushbericht klikt."

U kunt het gedrag selecteren wanneer een gebruiker op de hoofdtekst van het pushbericht klikt.

![](assets/title-body-push.png)

* Als u de app wilt openen, selecteert u de **[!UICONTROL Open app]** -optie. De toepassing die aan de melding is gekoppeld, wordt gedefinieerd in het dialoogvenster [kanaaloppervlak](../configuration/channel-surfaces.md) (d.w.z. voorinstelling bericht).
* Als u de gebruiker wilt omleiden naar een bepaald stuk inhoud in een app, selecteert u de optie **[!UICONTROL Deeplink]** -optie.  De specifieke inhoud kan een specifieke weergave, een bepaalde sectie van een pagina of een bepaald tabblad zijn. Als de optie is geselecteerd, voert u de koppeling in het bijbehorende veld in.
* Als u de gebruiker wilt omleiden naar een externe URL, gebruikt u de opdracht **[!UICONTROL Web URL]** -optie. Wanneer de optie is geselecteerd, voert u de URL in het bijbehorende veld in.

## Media toevoegen {#add-media-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-media"
>title="Media toevoegen aan uw pushmelding"
>abstract="U kunt een afbeelding, video of GIF toevoegen die in uw melding worden weergegeven."

In de iOS-versie van uw pushmelding kunt u een afbeelding, video of GIF toevoegen die in uw melding worden weergegeven.

In de Android-versie kunt u alleen een afbeeldingspictogram en een afbeelding toevoegen voor uitgebreide berichten.

![](assets/push-config-add-media.png)

Er zijn twee opties beschikbaar. U kunt:

* Gebruik de **[!UICONTROL Add media]** knop om een element te selecteren in **[!DNL Adobe Experience Manager Assets Essentials]**.

  Leren gebruiken **[!DNL Adobe Experience Manager Assets Essentials]** in [deze pagina](../content-management/assets-essentials.md).

* U kunt ook de URL van het medium invoeren in het dialoogvenster **[!UICONTROL Add media]** veld. In dat geval kunt u personalisatie toevoegen aan de URL.

Nadat de media zijn toegevoegd, worden deze rechts van de meldingsinstantie weergegeven.

## Knoppen toevoegen {#add-buttons-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-buttons"
>title="Voeg knoppen toe waarmee gebruikers kunnen communiceren met uw pushmelding."
>abstract="Deze sectie zal u toestaan om vraag-aan-actie knopen aan uw bericht toe te voegen. Geef voor iOS een identificatie voor de berichtencategorie op. Voor Android kunt u voor elke knop aangepaste tekst en doelen opnemen."

Maak een actionable melding door knoppen toe te voegen aan uw pushinhoud.

Als het apparaatscherm vergrendeld is, worden deze knoppen niet weergegeven: alleen de **Titel** en de **Bericht** van de kennisgeving zichtbaar zijn. Als het apparaat ontgrendeld is, zien de ontvangers de knoppen.

In de Android-versie kunt u maximaal drie knoppen toevoegen.

In de iOS-versie wordt een id voor een berichtencategorie opgegeven. Meldingscategorieën moeten vooraf worden geconfigureerd in de iOS-app, waarin de knoppen worden gedefinieerd die moeten worden weergegeven en de acties die moeten worden ondernomen. Zie de [Apple-documentatie](https://developer.apple.com/documentation/usernotifications/declaring_your_actionable_notification_types) voor meer informatie .

1. Gebruik de **[!UICONTROL Add button]** om instellingen te definiëren: het label en de bijbehorende actie. Mogelijke acties zijn hetzelfde als voor [klikgedrag](#on-click-behavior).

1. Gebruik de **[!UICONTROL Expand view]** onder de centrale voorvertoning om een voorvertoning van uw persoonlijke knoppen weer te geven.

   ![](assets/push_buttons.png)

## Een stille melding verzenden {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="Informatie over stille meldingen"
>abstract="Verzend berichten zonder de gebruiker te storen, worden de berichten niet getoond in het berichtcentrum of de berichtbar."

Een stille pushmelding (of een achtergrondmelding) is een verborgen instructie die aan de toepassing wordt geleverd. Deze wordt bijvoorbeeld gebruikt om uw toepassing op de hoogte te stellen van de beschikbaarheid van nieuwe inhoud of om op de achtergrond een download te starten.

Selecteer de **[!UICONTROL Silent Notification]** optie om de toepassing zonder toezicht op de hoogte te brengen: in dit geval wordt de melding rechtstreeks naar de toepassing overgedragen. Er wordt geen waarschuwing weergegeven op het scherm van het apparaat.

Gebruik de **[!UICONTROL Custom data]** om sleutelwaardeparen toe te voegen.

## Aangepaste gegevens {#custom-data}

>[!CONTEXTUALHELP]
>id="ajo-message-push-custom"
>title="Configureer aangepaste gegevens voor uw pushmelding."
>abstract="Voeg aangepaste variabelen toe aan de payload, afhankelijk van de configuratie van uw mobiele toepassing."

In de **[!UICONTROL Custom data]** kunt u aangepaste variabelen toevoegen aan de payload, afhankelijk van de configuratie van uw mobiele toepassing. Raadpleeg voor meer informatie over het instellen van pushmeldingen in Adobe Experience Platform en het starten van de Adobe [deze sectie](push-gs.md)

## Geavanceerde opties {#advanced-options-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-advanced"
>title="Configureer geavanceerde opties voor uw pushmelding."
>abstract="In deze sectie kunt u de personalisatie van uw pushmelding verbeteren."

U kunt **[!UICONTROL Advanced options]** voor uw pushmelding. De beschikbare parameters worden hieronder weergegeven:

| Parameter | Beschrijving |
|---------|---------|
| **[!UICONTROL Collapsible]** (iOS / Android) | Een inklapbaar bericht is een bericht dat door een nieuw bericht kan worden vervangen als het verouderd is geworden. Een veelvoorkomend gebruik van samenvouwbare berichten is berichten die worden gebruikt om een mobiele toepassing te vertellen gegevens van de server te synchroniseren. Een voorbeeld hiervan is een sport-app waarmee gebruikers de laatste score krijgen. Alleen het meest recente bericht is relevant. Aan de andere kant is met niet-inklapbaar bericht zeer belangrijk voor de client-app en moet het worden afgeleverd. |
| **[!UICONTROL Custom sound]** (iOS / Android) | Het geluid dat door de mobiele terminal moet worden afgespeeld wanneer het bericht wordt ontvangen. Het geluid moet in de app worden gebundeld. |
| **[!UICONTROL Badges]** (iOS / Android) | Een badge wordt gebruikt om het aantal nieuwe ongelezen meldingen direct op het applicatiepictogram te tonen. <br/>De badgewaarde verdwijnt zodra de gebruiker de nieuwe content in de applicatie opent of leest. Wanneer een melding op een apparaat wordt ontvangen, kan de badgewaarde voor de desbetreffende app worden vernieuwd of toegevoegd.<br/>Als u bijvoorbeeld het aantal ongelezen artikelen van uw klanten opslaat, kunt u personalisatie gebruiken om de unieke ongelezen waarde van de artikelbadge voor elke klant te verzenden. Voor meer verpersoonlijking, verwijs naar [deze sectie](../personalization/personalize.md). |
| **[!UICONTROL Notification group]**  (alleen iOS) | Koppel een berichtgroep aan de pushmelding.<br/>Beginnend met iOS 12, staan de berichtgroepen u toe om berichtdraden en berichtonderwerpen in draad IDs te consolideren. Een merk kan bijvoorbeeld marketingmeldingen verzenden onder één groep-id, terwijl meer meldingen over operationele typen onder een of meer verschillende id&#39;s worden bewaard.<br/>Om dit te illustreren, kunt u groupID hebben: 123 &quot;controleer de nieuwe lenteinzameling van sweaters&quot;en groupID: 456 &quot;uw pakket werd geleverd&quot;berichtgroepen. In dit voorbeeld worden alle leveringsmeldingen gebundeld onder groep ID: 456. |
| **[!UICONTROL Notification channel]** (alleen Android) | Koppel een berichtkanaal aan de pushmelding.<br/>Vanaf Android 8.0 (API-niveau 26) moeten alle meldingen aan een kanaal worden toegewezen om te worden weergegeven. Raadpleeg voor meer informatie de [Documentatie voor ontwikkelaars van Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Add content-availability flag]** (alleen iOS) | Verstuurt de markering voor de beschikbare inhoud in de pushlading om ervoor te zorgen dat de app wordt geactiveerd zodra deze de pushmelding ontvangt. Dit betekent dat de app toegang kan krijgen tot de payload-gegevens.<br/> Dit werkt zelfs als de app op de achtergrond wordt uitgevoerd en zonder tussenkomst van de gebruiker (bijvoorbeeld tikken op pushmeldingen). Dit is echter niet van toepassing als de app niet wordt uitgevoerd. Zie de [Apple Developer documentatie](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html) voor meer informatie hierover. |
| **[!UICONTROL Add mutable-content flag]** (alleen iOS) | Verzendt de markering voor gemuteerde inhoud in de pushlading en zorgt ervoor dat de inhoud van het pushbericht kan worden gewijzigd door een uitbreiding van de berichtgevingsservice die is opgegeven in iOS SDK. Zie [Apple Developer documentatie](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html) voor meer informatie hierover.<br/>Vervolgens kunt u uw mobiele app-extensies gebruiken om de inhoud of presentatie van aankomende pushmeldingen die zijn verzonden van [!DNL Journey Optimizer]. Gebruikers kunnen deze optie bijvoorbeeld gebruiken om gegevens te decoderen, de tekst van de hoofdtekst of titel van een melding te wijzigen, een thread-id aan een melding toe te voegen, enzovoort. |
| **[!UICONTROL Notification visibility]** (alleen Android) | Hiermee definieert u de zichtbaarheid van het pushbericht. <br/><b>Persoonlijk</b> toont de melding op alle vergrendelingsschermen, maar verbergt gevoelige of persoonlijke informatie op veilige vergrendelingsschermen. <br/><b>Openbaar</b> de volledige kennisgeving wordt op alle vergrendelingsschermen weergegeven. <br/><b>Geheim</b> geen enkel deel van de melding zichtbaar maken op een veilig vergrendelingssysteem. <br/>Raadpleeg voor meer informatie de [Documentatie voor ontwikkelaars van Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Notification priority]** (alleen Android) | Hiermee definieert u het belang van de pushmelding van Laag tot Max. Dit bepaalt hoe &quot;indringend&quot;de dupmelding zal zijn wanneer het wordt geleverd. Raadpleeg voor meer informatie de [Documentatie voor ontwikkelaars van Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** (alleen Android) | Hiermee stelt u een hoge of normale prioriteit in voor uw pushberichten. Zie de [Google Developer-documentatie](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message) voor meer informatie over de prioriteit van berichten. |
