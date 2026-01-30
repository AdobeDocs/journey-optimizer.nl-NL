---
solution: Journey Optimizer
product: journey optimizer
title: Een pushmelding ontwerpen
description: Leer hoe u een pushmelding ontwerpt in Journey Optimizer
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: 6f6d693d-11f2-48b7-82a8-171829bf8045
source-git-commit: af40716070ab28001acb6f5c02f41a0ec3ad8258
workflow-type: tm+mt
source-wordcount: '1716'
ht-degree: 3%

---

# Een pushmelding ontwerpen {#design-push-notification}

Als u eenmaal een pushmelding hebt gemaakt, kunt u de inhoud ontwerpen voor iOS- en Android-platforms. Deze pagina begeleidt u door het samenstellen van uw bericht, het configureren van gedrag bij klikken, het toevoegen van media en knoppen en het instellen van geavanceerde opties om aansprekende pushberichten te maken die op uw publiek passen.

## Titel en body {#push-title-body}

>[!CONTEXTUALHELP]
>id="ajo-message-push-compose"
>title="Pas uw pushmelding aan."
>abstract="Om uw bericht samen te stellen, ga de inhoud in de **Titel** en **3&rbrace; gebieden van het Lichaam in.** Als u personalisatietokens wilt opnemen, opent u het dialoogvenster voor personalisatie."

![](assets/title-body.png)

Klik op de velden **[!UICONTROL Title]** en **[!UICONTROL Body]** om uw bericht samen te stellen. Gebruik de verpersoonlijkingsredacteur om inhoud te bepalen, gegevens te personaliseren en dynamische inhoud toe te voegen. Leer meer over [&#x200B; verpersoonlijking &#x200B;](../personalization/personalize.md) en [&#x200B; dynamische inhoud &#x200B;](../personalization/get-started-dynamic-content.md) in de verpersoonlijkingsredacteur.

In de sectie met voorvertoningen van apparaten kunt u visualiseren hoe de pushmelding wordt weergegeven op iOS en Android.

Versnel uw inhoudsverwezenlijking met AI Medewerker en produceer dwingende tekst van het pushbericht met [&#x200B; AI Medewerker voor tekstgeneratie &#x200B;](../content-management/generative-text.md) of creeer volledige duw berichten met [&#x200B; Medewerker AI voor volledige inhoudsgeneratie &#x200B;](../content-management/generative-full-content.md).

## Bij klikken, gedrag {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Informatie over klikgedrag"
>abstract="Selecteer het gedrag wanneer een ontvanger op de hoofdtekst van het pushbericht klikt."

Configureer de actie die plaatsvindt wanneer ontvangers op de hoofdtekst van uw pushmelding tikken. Kies een van de volgende opties:

![](assets/title-body-push.png)

* **[!UICONTROL Open app]**: hiermee wordt de toepassing gestart die aan het bericht is gekoppeld. App wordt gespecificeerd in uw [&#x200B; kanaalconfiguratie &#x200B;](../configuration/channel-surfaces.md) (d.w.z. vooraf ingesteld bericht).
* **[!UICONTROL Deeplink]**: hiermee worden gebruikers naar specifieke inhoud in uw app geleid, zoals een bepaalde weergave, paginasectie of tab. Voer in het opgegeven veld de verwijderings-URL in.
* **[!UICONTROL Web URL]**: hiermee stuurt u gebruikers naar een externe webpagina. Voer de doel-URL in het opgegeven veld in.

## Media toevoegen {#add-media-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-media"
>title="Media toevoegen aan uw pushmelding"
>abstract="U kunt een afbeelding, video of GIF toevoegen die in uw melding worden weergegeven."

Verbeter uw pushmelding door visuele media toe te voegen. De beschikbare mediatypen en implementatiemethoden variëren per besturingssysteem, zoals in de volgende tabbladen wordt beschreven.

>[!BEGINTABS]

>[!TAB  Android ]

In Android kunt u alleen een afbeeldingspictogram en een afbeelding voor uitgebreide berichten toevoegen.

![](assets/push-config-add-media.png)

U kunt media toevoegen met een van de volgende methoden:

* **[!UICONTROL Add media]** knoop: Selecteer een activa van [&#x200B; Adobe Experience Manager Assets &#x200B;](../integrations/assets.md) of toegang tot de Medewerker AI om [&#x200B; het in dienst nemen beelden &#x200B;](../content-management/generative-image.md) voor dupberichten te produceren.

* **[!UICONTROL Add media]** veld: voer de media-URL rechtstreeks in. U kunt personalisatietokens in URL omvatten.

Nadat de media zijn toegevoegd, worden deze rechts van de meldingsinstantie weergegeven.

>[!NOTE]
>
>Wanneer u mediabijlagen opneemt in de payload van pushberichten (zoals afbeeldingen in aangepaste gegevensvelden zoals `adb_media` ), moet uw mobiele toepassing specifieke clientverwerking implementeren om de afbeeldingen op apparaten te renderen. Uw app moet de [&#x200B; automatische vertoning en het volgen werkschema &#x200B;](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/push-notification/android/automatic-display-and-tracking/){target="_blank"} uitvoeren om beeldgehechtheid van de nuttige lading te behandelen.

>[!TAB  iOS ]

Voor iOS kunt u een afbeelding, video of GIF toevoegen om deze in uw melding weer te geven.

![](assets/push-config-add-media-ios.png)

U kunt media toevoegen met een van de volgende methoden:

* **[!UICONTROL Add media]** knop: selecteer een element in **[!DNL Adobe Experience Manager Assets]** . Leer meer over het gebruiken van **[!DNL Adobe Experience Manager Assets]** in [&#x200B; deze pagina &#x200B;](../integrations/assets.md).

* **[!UICONTROL Add media]** veld: voer de media-URL rechtstreeks in. U kunt personalisatietokens in URL omvatten.

Nadat de media zijn toegevoegd, worden deze rechts van de meldingsinstantie weergegeven.

>[!NOTE]
>
>Wanneer u mediabijlagen opneemt in de payload van pushberichten (zoals afbeeldingen in aangepaste gegevensvelden zoals `adb_media` ), moet uw mobiele toepassing specifieke clientverwerking implementeren om de afbeeldingen op apparaten te renderen. Uw app moet de Uitbreiding van de Dienst van het a [&#x200B; Bericht &#x200B;](https://developer.apple.com/documentation/usernotifications/modifying_content_in_newly_delivered_notifications){target="_blank"} uitvoeren om media inhoud van de nuttige lading te downloaden en te verwerken. Bovendien, moet de **[!UICONTROL Add mutable-content flag]** optie in de [&#x200B; Geavanceerde opties &#x200B;](#advanced-options-push) sectie worden toegelaten.

<!--
>[!TAB Web]

Enter the media URL in the **[!UICONTROL Add media]** field. You can also include personalization tokens in the URL to customize the content for each user.

Click ![Edit text with the AI assistant](assets/do-not-localize/Smock_ImageAdd_18_N.svg) to quickly generate media using the Journey Optimizer AI Assistant.

![](assets/web-media.png)
-->

>[!ENDTABS]

## Knoppen toevoegen {#add-buttons-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-buttons"
>title="Voeg knoppen toe waarmee gebruikers kunnen communiceren met uw pushmelding."
>abstract="Voeg vanuit deze sectie call-to-action-knoppen toe aan uw bericht. Geef voor Apple iOS een identificatiecode voor de berichtencategorie op. Voor Google Android kunt u aangepaste tekst en doelen voor elke knop opnemen."

Maak een actionable melding door knoppen toe te voegen aan uw pushinhoud. Blader op basis van uw besturingssysteem naar de onderstaande tabbladen.

Als het apparatenscherm wordt gesloten, worden deze knopen niet getoond: slechts dan is de **Titel** en het **Bericht** van het bericht zichtbaar. Als het apparaat ontgrendeld is, zien de ontvangers de knoppen.

>[!BEGINTABS]

>[!TAB  Android ]

Voor Android kunt u maximaal drie knoppen toevoegen.

1. Gebruik **[!UICONTROL Add button]** om instellingen te definiëren: het label en de bijbehorende actie. De mogelijke acties zijn het zelfde als voor [&#x200B; on-click gedrag &#x200B;](#on-click-behavior).

   ![](assets/push_buttons.png)

1. Gebruik het pictogram **[!UICONTROL Expand view]** onder de centrale voorvertoning om een voorvertoning van uw persoonlijke knoppen weer te geven.

>[!TAB  iOS ]

![](assets/push_buttons-ios.png)

Voor iOS wordt een id voor een berichtencategorie opgegeven. Meldingscategorieën moeten vooraf worden geconfigureerd in de iOS-app, waarin de knoppen worden gedefinieerd die moeten worden weergegeven en de acties die moeten worden ondernomen. Zie de [&#x200B; documentatie van Apple &#x200B;](https://developer.apple.com/documentation/usernotifications/declaring_your_actionable_notification_types) voor meer details.

<!--
>[!TAB Web]

![](assets/push_buttons-web.png)

Use the **[!UICONTROL Add Button]** option to define each button's label and associated action, as detailed below:

* **[!UICONTROL Deeplink]**: Redirect users to a specific view, section, or tab within your app. Enter the deeplink URL in the associated field.

* **[!UICONTROL Web URL]**: Redirect users to an external webpage. Enter the URL in the associated field.
-->

>[!ENDTABS]

## Een stille melding verzenden {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="Informatie over stille meldingen"
>abstract="Verzend berichten zonder de gebruiker te storen, worden de berichten niet getoond in het berichtcentrum of de berichtbar."

<!--
>[!AVAILABILITY]
>
>Web push notifications in Journey Optimizer do not support the **Silent Notification** feature.
-->

Een stille pushmelding (of een achtergrondmelding) is een verborgen instructie die aan de toepassing wordt geleverd. Deze wordt bijvoorbeeld gebruikt om uw toepassing op de hoogte te stellen van de beschikbaarheid van nieuwe inhoud of om op de achtergrond een download te starten.

Selecteer de optie **[!UICONTROL Silent Notification]** om de toepassing stil te melden: in dit geval wordt het bericht rechtstreeks naar de toepassing overgebracht. Er wordt geen waarschuwing weergegeven op het scherm van het apparaat.

Gebruik de sectie **[!UICONTROL Custom data]** om sleutelwaardeparen toe te voegen.

## Aangepaste gegevens {#custom-data}

>[!CONTEXTUALHELP]
>id="ajo-message-push-custom"
>title="Configureer aangepaste gegevens voor uw pushmelding."
>abstract="Voeg aangepaste variabelen toe aan de payload, afhankelijk van de configuratie van uw mobiele toepassing."

In de sectie **[!UICONTROL Custom data]** kunt u aangepaste variabelen toevoegen aan de payload, afhankelijk van de configuratie van uw mobiele toepassing. Voor meer op hoe te opstelling duwen berichten in Adobe Experience Platform, verwijs naar [&#x200B; deze sectie &#x200B;](push-gs.md)

## Geavanceerde opties {#advanced-options-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-advanced"
>title="Configureer geavanceerde opties voor uw pushmelding."
>abstract="In deze sectie kunt u de personalisatie van uw pushmelding verbeteren."

U kunt **[!UICONTROL Advanced options]** voor uw pushmelding configureren. De beschikbare parameters worden hieronder weergegeven:

| Parameter | Beschrijving |
|---------|---------|
| **[!UICONTROL Collapsible]** (iOS / Android) | Een inklapbaar bericht is een bericht dat door een nieuw bericht kan worden vervangen als het verouderd is geworden. Een veelvoorkomend gebruik van samenvouwbare berichten is berichten die worden gebruikt om een mobiele toepassing te vertellen gegevens van de server te synchroniseren. Een voorbeeld hiervan is een sport-app waarmee gebruikers de laatste score krijgen. Alleen het meest recente bericht is relevant. Aan de andere kant is elk bericht met een niet-inklapbaar bericht belangrijk voor de client-app en moet het worden bezorgd. |
| **[!UICONTROL Custom sound]** (iOS / Android) | Het geluid dat door de mobiele terminal moet worden afgespeeld wanneer het bericht wordt ontvangen. Het geluid moet in de app worden gebundeld. |
| **[!UICONTROL Badges]** (iOS / Android) | Een badge wordt gebruikt om het aantal nieuwe ongelezen meldingen direct op het applicatiepictogram te tonen. <br/> de merkwaarde zal verdwijnen zodra de gebruiker opent of de nieuwe inhoud van de toepassing leest. Wanneer een melding op een apparaat wordt ontvangen, kan het een merkwaarde voor de verwante app vernieuwen of toevoegen.<br/> Bijvoorbeeld, als u het aantal ongelezen artikelen van uw klanten opslaat, kunt u hefboomwerking verpersoonlijking om de unieke ongelezen waarde van de artikelbadge voor elke klant te verzenden. Voor meer verpersoonlijking, verwijs naar [&#x200B; deze sectie &#x200B;](../personalization/personalize.md). |
| **[!UICONTROL Notification group]** (alleen iOS) | Koppel een berichtgroep aan de pushmelding.<br/> Beginnend met iOS 12, staan de berichtgroepen u toe om berichtdraden en berichtonderwerpen in draad IDs te consolideren. Een merk kan bijvoorbeeld marketingmeldingen verzenden onder één groep-id, terwijl meer meldingen over operationele typen onder een of meer verschillende id&#39;s worden bewaard.<br/> om dit te illustreren, kunt u groupID hebben: 123 &quot;controleer de nieuwe lenteinzameling van sweaters&quot;en groupID: 456 &quot;uw pakket werd geleverd&quot;berichtgroepen. In dit voorbeeld worden alle leveringsmeldingen gebundeld onder groep ID: 456. |
| **[!UICONTROL Notification channel]** (alleen Android) | Koppel een berichtkanaal aan de pushmelding.<br/> Beginnend in Android 8.0 (API niveau 26), moeten alle berichten aan een kanaal worden toegewezen om te tonen. Voor meer op dit, verwijs naar de [&#x200B; de ontwikkelaarsdocumentatie van Android &#x200B;](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Add content-availability flag]** (alleen iOS) | Verstuurt de markering voor de beschikbare inhoud in de pushlading om ervoor te zorgen dat de app wordt geactiveerd zodra deze de pushmelding ontvangt. Dit betekent dat de app toegang kan krijgen tot de payload-gegevens.<br/> Dit werkt zelfs als de app op de achtergrond wordt uitgevoerd en zonder tussenkomst van de gebruiker (bijvoorbeeld tikken op pushmelding). Dit is echter niet van toepassing als de app niet wordt uitgevoerd. Zie de [Apple Developer documentatie](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html) voor meer informatie hierover. |
| **[!UICONTROL Add mutable-content flag]** (alleen iOS) | Verzendt de markering voor meerbare inhoud in de pushlading en zorgt ervoor dat de inhoud van het pushbericht kan worden gewijzigd door een uitbreiding van de berichtservice die in iOS SDK is opgegeven. Zie [Apple Developer documentatie](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html) voor meer informatie hierover.<br/> U kunt dan uw mobiele app-extensies gebruiken om de inhoud of presentatie van aankomende pushmeldingen die zijn verzonden vanuit [!DNL Journey Optimizer] , verder te wijzigen. Gebruikers kunnen deze optie bijvoorbeeld gebruiken om gegevens te decoderen, de tekst van de hoofdtekst of titel van een melding te wijzigen, een thread-id aan een melding toe te voegen, enzovoort.<br/>**Belangrijk**: Deze vlag moet worden toegelaten wanneer het omvatten van media gehechtheid (beelden, video&#39;s) via nuttige ladingsgebieden (zoals `adb_media`) voor hen om op de apparaten van iOS terug te geven. Uw app moet ook een uitbreiding van de Berichtenservice implementeren om de media-inhoud van de payload te downloaden en verwerken. |
| **[!UICONTROL Add Push expiration]** (alleen iOS) | Kies de **Datum en de Tijd** van uw Duw vervaldatum. Op iOS wordt de vervaldatum van een melding afgedwongen als een harde stop. Dit betekent dat elk bericht dat de Apple Push Notification Service (APNS) bereikt nadat de vervaldatum is verstreken, niet wordt afgeleverd, zodat klanten nooit verouderde of irrelevante berichten ontvangen. Zie de [Apple Developer documentatie](https://developer.apple.com/documentation/usernotifications/sending-notification-requests-to-apns) voor meer informatie hierover. |
| **[!UICONTROL Notification visibility]** (alleen Android) | Hiermee definieert u de zichtbaarheid van het pushbericht. <br/><b> Privé </b> zal het bericht op alle lockscreens tonen, maar verborgen gevoelige of privé informatie over veilige lockscreens. <br/><b> Openbaar </b> zal het bericht in zijn geheel op alle lockscreens tonen. <br/><b> Geheim </b> zal om het even welk deel van het bericht op veilig lockscreen niet openbaren. <br/> voor meer op dit, verwijs de [&#x200B; documentatie van de ontwikkelaar van Android &#x200B;](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Notification priority]** (alleen Android) | Hiermee definieert u het belang van de pushmelding van Laag tot Max. Dit bepaalt hoe &quot;indringend&quot;de dupmelding zal zijn wanneer het wordt geleverd. Voor meer op dit, verwijs naar de [&#x200B; de ontwikkelaarsdocumentatie van Android &#x200B;](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** (alleen Android) | Hiermee stelt u een hoge of normale prioriteit in voor uw pushberichten. Zie de [Google Developer-documentatie](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message) voor meer informatie over de prioriteit van berichten. |
| **[!UICONTROL Time to live]** (alleen Android) | Plaats het aantal seconden waarna uw bericht zal verlopen. In Android wordt verlopen beschouwd als een leveringsvenster: in Firebase Cloud Messaging (FCM) wordt de vervaltijd omgezet in een tijd-naar-live (TTL)-waarde die begint wanneer het bericht wordt ontvangen. Dit betekent dat niet-geleverde campagnes later kunnen worden verzonden dan verwacht of zelfs buiten het gewenste tijdsbestek. Voor meer op dit, verwijs de [&#x200B; de ontwikkelaarsdocumentatie van Android &#x200B;](https://firebase.google.com/docs/cloud-messaging/concept-options#ttl). |
