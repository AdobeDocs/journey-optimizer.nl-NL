---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Campaign Standard-acties
description: Meer informatie over Adobe Campaign Standard-acties
feature: Actions
topic: Administration
role: Admin
level: Intermediate
keywords: transport, integratie, standaard, campagne, ACS
exl-id: 50565cd9-7415-4c6a-9651-24fefeded3f5
source-git-commit: 417eea2a52d4fb38ae96cf74f90658f87694be5a
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 3%

---

# Adobe Campaign Standard-acties {#using_campaign_action}

Als u Adobe Campaign Standard hebt, zijn de volgende ingebouwde actieactiviteiten beschikbaar: **[!UICONTROL Email]**, **[!UICONTROL Push]** en **[!UICONTROL SMS]**.

>[!NOTE]
>
>Hiervoor moet u de ingebouwde actie configureren. Zie [deze pagina](../action/acs-action.md).

Voor elk van deze kanalen selecteert u een Adobe Campaign Standard Transaction Messaging **template**. Voor de ingebouwde e-mail, sms en duw kanalen, vertrouwen wij op Transactieoverseinen om bericht uit te voeren die verzenden. Het betekent dat als u een bepaald berichtmalplaatje in uw reizen wilt gebruiken, u het in Adobe Campaign Standard moet publiceren. Zie [deze pagina](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=nl) voor meer informatie over het gebruik van deze functie.

>[!NOTE]
>
>Het transactiebericht van Campaign Standard en de bijbehorende gebeurtenis moeten worden gepubliceerd om in Journey Optimizer te kunnen worden gebruikt. Als de gebeurtenis wordt gepubliceerd maar het bericht niet is, is het niet zichtbaar in de interface van Journey Optimizer. Als het bericht wordt gepubliceerd maar zijn bijbehorende gebeurtenis niet, zal het in de interface van Journey Optimizer zichtbaar zijn maar het zal niet bruikbaar zijn.

![](assets/journey59.png)

U kunt een gebeurtenis (die ook als Real-Time wordt bekend) of een malplaatje van het profieltransactie gebruiken.

>[!NOTE]
>
>Wanneer wij transactieberichten in real time (rtEvent) verzenden of wanneer wij berichten met een derdesysteem dankzij een douaneactie leiden, wordt een specifieke opstelling vereist voor moeheid, lijst van gewezen personen of unsubscription beheer. Als bijvoorbeeld een kenmerk &quot;unsubscribe&quot; in de Adobe Experience Platform of in een systeem van derden wordt opgeslagen, moet een voorwaarde worden toegevoegd vóór het bericht dat deze voorwaarde verzendt.

Wanneer u een sjabloon selecteert, worden alle velden die in de berichtlading worden verwacht, weergegeven in het deelvenster voor activiteitenconfiguratie onder **[!UICONTROL Address]** en **[!UICONTROL Personalization Data]**. U moet elk van deze gebieden met het gebied in kaart brengen u, of van de gebeurtenis of van de gegevensbron wilt gebruiken. U kunt de geavanceerde uitdrukkingsredacteur ook gebruiken om een waarde manueel over te gaan, gegevensmanipulatie op teruggewonnen informatie (bijvoorbeeld om een koord in hoofdletters om te zetten) uit te voeren of functies zoals &quot;als, toen, anders&quot;te gebruiken. Zie [deze pagina](expression/expressionadvanced.md).

![](assets/journey60.png)

## E-mail en sms {#section_asc_51g_nhb}

Voor **[!UICONTROL Email]** en **[!UICONTROL SMS]**, zijn de parameters identiek.

>[!NOTE]
>
>Als Adobe Campaign Standard de transactiesjabloon van een profiel gebruikt voor e-mail, wordt het systeem voor het opzeggen van abonnementen automatisch afgehandeld. Om dit uit te voeren, kunt u gemakkelijk omvatten **[!UICONTROL Unsubscription link]** inhoudsblok binnen [de transactiemalplaatje voor e-mail](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=nl). Nochtans, als u een op gebeurtenis-gebaseerde malplaatje (rtEvent) gebruikt, moet u een verbinding in het bericht opnemen die de e-mail van de ontvanger als parameter URL overgaat, en hen aan een unsubscription het landen pagina leidt. Deze landingspagina moet worden gemaakt en ervoor zorgen dat de beslissing van de ontvanger om af te zien, daadwerkelijk aan Adobe wordt toegezonden.

Eerst, moet u een transactioneel overseinensjabloon kiezen.

Er zijn twee categorieën beschikbaar: **[!UICONTROL Address]** en **[!UICONTROL Personalization Data]**.

U kunt gemakkelijk bepalen waar te om terug te winnen **[!UICONTROL Address]** of de **[!UICONTROL Personalization Data]** het gebruiken van de interface. U kunt door gebeurtenissen en beschikbare gebieden van de gegevensbron doorbladeren. U kunt de geavanceerde uitdrukkingsredacteur voor geavanceerdere gebruiksgevallen zoals het gebruiken van een gegevensbron ook gebruiken die de overgaan van parameters of het uitvoeren van manipulaties vereist. Zie [deze pagina](expression/expressionadvanced.md).

**[!UICONTROL Address]**

>[!NOTE]
>
>Deze categorie is alleen zichtbaar als u een transactiebericht voor een gebeurtenis selecteert. Voor &quot;profiel&quot;-berichten wordt **[!UICONTROL Address]** wordt automatisch door het systeem opgehaald uit Adobe Campaign Standard.

Dit zijn de gebieden het systeem vereist om te weten waar te om het bericht te verzenden. Voor een e-mailsjabloon is dit het e-mailadres. Voor een SMS is het het mobiele telefoonnummer.

![](assets/journey61.png)

**[!UICONTROL Personalization Data]**

>[!NOTE]
>
>U kunt geen inzameling in verpersoonlijkingsgegevens overgaan. Als de transactie-e-mail of SMS inzamelingen verwacht, zal het niet werken. Merk ook op dat de verpersoonlijkingsgegevens een verwacht formaat hebben (voorbeeld: tekenreeks, decimaal, enz.). U moet deze verwachte formaten zorgvuldig respecteren.

Dit zijn de velden die worden verwacht door het Adobe Campaign Standard-bericht. Deze velden kunnen worden gebruikt om het bericht aan te passen, voorwaardelijke opmaak toe te passen of een specifieke berichtvariant te kiezen.

![](assets/journey62.png)

## Push {#section_im3_hvf_nhb}

Voordat u de pushactiviteit kunt gebruiken, moet uw mobiele app samen met Campaign Standard worden geconfigureerd om pushmeldingen te verzenden. Gebruik deze [artikel](https://helpx.adobe.com/nl/campaign/kb/integrate-mobile-sdk.html) de nodige stappen voor de implementatie van mobiele apparatuur te ondernemen.

Eerst moet u een mobiele app kiezen in de vervolgkeuzelijst en een transactiebericht.

![](assets/journey62bis.png)

Er zijn twee categorieën beschikbaar: **[!UICONTROL Target]** en **[!UICONTROL Personalization Data]**.

**[!UICONTROL Target]**

>[!NOTE]
>
>Deze categorie is alleen zichtbaar als u een gebeurtenisbericht selecteert. Voor profielberichten, **[!UICONTROL Target]** velden worden automatisch door het systeem opgehaald met behulp van de afstemming die door Adobe Campaign Standard wordt uitgevoerd.

In deze sectie moet u de opdracht **[!UICONTROL Push platform]**. In de vervolgkeuzelijst kunt u **[!UICONTROL Apple Push Notification Server]** (iOS) of **[!UICONTROL Firebase Cloud Messaging]** (Android). U kunt ook een specifiek veld selecteren in een gebeurtenis of gegevensbron, of een geavanceerde expressie definiëren.

U moet ook de **[!UICONTROL Registration Token]**. De expressie hangt af van de manier waarop het token is gedefinieerd in de gebeurtenislading of in andere [!DNL Journey Optimizer] informatie. Het kan een eenvoudig veld of een complexere expressie zijn voor het geval het token bijvoorbeeld in een verzameling wordt gedefinieerd:

```
@{Event_push._experience.campaign.message.profileSnapshot.pushNotificationTokens.first().token}
```

**[!UICONTROL Personalization Data]**

>[!NOTE]
>
>U kunt geen inzameling in verpersoonlijkingsgegevens overgaan. Als de transactioneel duw inzamelingen verwacht, zal het niet werken. Merk ook op dat de verpersoonlijkingsgegevens een verwacht formaat hebben (voorbeeld: tekenreeks, decimaal, enz.). U moet deze verwachte formaten zorgvuldig respecteren.

Dit zijn de velden die worden verwacht door de transactiesjabloon die wordt gebruikt in je Adobe Campaign Standard-bericht. Deze velden kunnen worden gebruikt om uw bericht aan te passen, voorwaardelijke opmaak toe te passen of een specifieke berichtvariant te kiezen.
