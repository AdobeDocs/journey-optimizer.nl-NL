---
solution: Journey Optimizer
product: journey optimizer
title: '[!DNL Adobe Campaign] Standaardhandelingen'
description: Leer over  [!DNL Adobe Campaign]  Standaardacties
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: transport, integratie, standaard, campagne, ACS
exl-id: 50565cd9-7415-4c6a-9651-24fefeded3f5
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 1%

---

# [!DNL Adobe Campaign] Standaardhandelingen {#using_campaign_action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acs"
>title="Aangepaste acties"
>abstract="Integratie is beschikbaar als u [!DNL Adobe Campaign] Standard hebt. Hiermee kunt u e-mails, pushberichten en SMS verzenden met de mogelijkheden van [!DNL Adobe Campaign] Transactieberichten."

Als u [!DNL Adobe Campaign] Standard hebt, zijn de volgende ingebouwde handelingen beschikbaar: **[!UICONTROL Email]** , **[!UICONTROL Push]** en **[!UICONTROL SMS]** .

>[!NOTE]
>
>Hiervoor moet u de ingebouwde actie configureren. Zie [deze pagina](../action/acs-action.md).

Voor elk van deze kanalen, selecteert u een [!DNL Adobe Campaign] Standaard Transactioneel Overseinen **malplaatje**. Voor de ingebouwde e-mail, sms en duw kanalen, vertrouwen wij op Transactieoverseinen om bericht uit te voeren die verzenden. Dit betekent dat als u een bepaalde berichtsjabloon wilt gebruiken voor uw reizen, u deze moet publiceren in [!DNL Adobe Campaign] Standard. Verwijs naar [&#x200B; deze pagina &#x200B;](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=nl) om te leren hoe te om deze eigenschap te gebruiken.

>[!NOTE]
>
>Het Campaign Standard-transactiebericht en de bijbehorende gebeurtenis moeten worden gepubliceerd om in Journey Optimizer te kunnen worden gebruikt. Als de gebeurtenis wordt gepubliceerd maar het bericht niet is, is het niet zichtbaar in de interface van Journey Optimizer. Als het bericht wordt gepubliceerd maar zijn bijbehorende gebeurtenis niet, zal het in de interface van Journey Optimizer zichtbaar zijn maar het zal niet bruikbaar zijn.

![[!DNL Adobe Campaign] Standaardactieconfiguratie tijdens de rit &#x200B;](assets/journey59.png)

U kunt een gebeurtenis (die ook als Real-Time wordt bekend) of een malplaatje van het profieltransactie gebruiken.

>[!NOTE]
>
>Wanneer wij transactieberichten in real time (rtEvent) verzenden of wanneer wij berichten met een derdesysteem dankzij een douaneactie leiden, wordt een specifieke opstelling vereist voor moeheid, lijst van gewezen personen of unsubscription beheer. Als een kenmerk &quot;unsubscribe&quot; bijvoorbeeld wordt opgeslagen in [!DNL Adobe Experience Platform] of in een systeem van derden, moet een voorwaarde worden toegevoegd voordat het bericht wordt verzonden om deze voorwaarde te controleren.

Wanneer u een sjabloon selecteert, worden alle velden die in de berichtlading worden verwacht, weergegeven in het deelvenster Activiteitsconfiguratie onder **[!UICONTROL Address]** en **[!UICONTROL Personalization Data]** . U moet elk van deze gebieden met het gebied in kaart brengen u, of van de gebeurtenis of van de gegevensbron wilt gebruiken. U kunt de geavanceerde uitdrukkingsredacteur ook gebruiken om een waarde manueel over te gaan, gegevensmanipulatie op teruggewonnen informatie (bijvoorbeeld om een koord in hoofdletters om te zetten) uit te voeren of functies zoals &quot;als, toen, anders&quot;te gebruiken. Zie [deze pagina](expression/expressionadvanced.md).

![&#x200B; de selectieinterface van het het berichtmalplaatje van Campaign Standard &#x200B;](assets/journey60.png)

## E-mail en sms {#section_asc_51g_nhb}

Voor **[!UICONTROL Email]** en **[!UICONTROL SMS]** zijn de parameters identiek.

>[!NOTE]
>
>Als u de transactiesjabloon van een profiel gebruikt voor e-mail, wordt het mechanisme voor het opzeggen van abonnementen automatisch afgehandeld door [!DNL Adobe Campaign] Standard.
>Omvat een **[!UICONTROL Unsubscription link]** inhoudsblok binnen [&#x200B; het transactionele e-mailmalplaatje &#x200B;](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=nl).
>Als u een op een gebeurtenis gebaseerde sjabloon (rtEvent) gebruikt, neemt u een koppeling op in het bericht die de e-mail van de ontvanger doorgeeft als een URL-parameter en stuurt u deze naar een bestemmingspagina zonder abonnement.
>Maak de landingspagina en zorg ervoor dat het afwijzingsbesluit van de ontvanger naar Adobe wordt gezonden.

Eerst, moet u een transactioneel overseinensjabloon kiezen.

Er zijn twee categorieën beschikbaar: **[!UICONTROL Address]** en **[!UICONTROL Personalization Data]** .

Met de interface kunt u eenvoudig bepalen waar de **[!UICONTROL Address]** - of **[!UICONTROL Personalization Data]** -code moet worden opgehaald. U kunt door gebeurtenissen en beschikbare gebieden van de gegevensbron doorbladeren. U kunt de geavanceerde uitdrukkingsredacteur voor geavanceerdere gebruiksgevallen zoals het gebruiken van een gegevensbron ook gebruiken die de overgaan van parameters of het uitvoeren van manipulaties vereist. Zie [deze pagina](expression/expressionadvanced.md).

**[!UICONTROL Address]**

>[!NOTE]
>
>Deze categorie is alleen zichtbaar als u een transactiebericht voor een gebeurtenis selecteert. Voor profielberichten wordt het veld **[!UICONTROL Address]** automatisch door het systeem opgehaald uit [!DNL Adobe Campaign] Standard.

Dit zijn de gebieden het systeem vereist om te weten waar te om het bericht te verzenden. Voor een e-mailsjabloon is dit het e-mailadres. Voor een SMS is het het mobiele telefoonnummer.

![&#x200B; de parameterconfiguratie van het Bericht voor de integratie van Campaign Standard &#x200B;](assets/journey61.png)

**[!UICONTROL Personalization Data]**

>[!NOTE]
>
>U kunt geen inzameling in verpersoonlijkingsgegevens overgaan. Als de transactie-e-mail of SMS inzamelingen verwacht, zal het niet werken. Houd er ook rekening mee dat de aanpassingsgegevens een verwachte indeling hebben (bijvoorbeeld tekenreeks, decimaal, enz.). U moet deze verwachte formaten zorgvuldig respecteren.

Dit zijn de velden die worden verwacht door het standaardbericht van [!DNL Adobe Campaign] . Deze velden kunnen worden gebruikt om het bericht aan te passen, voorwaardelijke opmaak toe te passen of een specifieke berichtvariant te kiezen.

![&#x200B; afbeelding van het Gebied tussen Journey Optimizer en Campaign Standard &#x200B;](assets/journey62.png)

## Push {#section_im3_hvf_nhb}

Voordat u de pushactiviteit kunt gebruiken, moet uw mobiele app samen met Campaign Standard worden geconfigureerd om pushberichten te verzenden. Gebruik dit [&#x200B; artikel &#x200B;](https://helpx.adobe.com/nl/campaign/kb/integrate-mobile-sdk.html) om de noodzakelijke implementatiestappen voor mobiel te nemen.

Eerst moet u een mobiele app kiezen in de vervolgkeuzelijst en een transactiebericht.

![&#x200B; Geavanceerde uitdrukkingsredacteur voor de parameterafbeelding van Campaign Standard &#x200B;](assets/journey62bis.png)

Er zijn twee categorieën beschikbaar: **[!UICONTROL Target]** en **[!UICONTROL Personalization Data]** .

**[!UICONTROL Target]**

>[!NOTE]
>
>Deze categorie is alleen zichtbaar als u een gebeurtenisbericht selecteert. Voor profielberichten worden de **[!UICONTROL Target]** -velden automatisch opgehaald door het systeem met behulp van de afstemming die wordt uitgevoerd door [!DNL Adobe Campaign] Standard.

In deze sectie moet u de **[!UICONTROL Push platform]** definiëren. In de vervolgkeuzelijst kunt u **[!UICONTROL Apple Push Notification Server]** (iOS) of **[!UICONTROL Firebase Cloud Messaging]** (Android) selecteren. U kunt ook een specifiek veld selecteren in een gebeurtenis of gegevensbron, of een geavanceerde expressie definiëren.

U moet ook de **[!UICONTROL Registration Token]** definiëren. De expressie hangt af van de manier waarop het token wordt gedefinieerd in de gebeurtenislading of in andere [!DNL Journey Optimizer] -informatie. Het kan een eenvoudig veld of een complexere expressie zijn voor het geval het token bijvoorbeeld in een verzameling wordt gedefinieerd:

```
@event{Event_push._experience.campaign.message.profileSnapshot.pushNotificationTokens.first().token}
```

**[!UICONTROL Personalization Data]**

>[!NOTE]
>
>U kunt geen inzameling in verpersoonlijkingsgegevens overgaan. Als de transactioneel duw inzamelingen verwacht, zal het niet werken. Houd er ook rekening mee dat de aanpassingsgegevens een verwachte indeling hebben (bijvoorbeeld tekenreeks, decimaal, enz.). U moet deze verwachte formaten zorgvuldig respecteren.

Dit zijn de velden die worden verwacht door de transactiesjabloon die wordt gebruikt in het standaardbericht van [!DNL Adobe Campaign] . Deze velden kunnen worden gebruikt om uw bericht aan te passen, voorwaardelijke opmaak toe te passen of een specifieke berichtvariant te kiezen.
