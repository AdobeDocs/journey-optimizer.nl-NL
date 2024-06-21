---
solution: Journey Optimizer
product: journey optimizer
title: Je berichten bijhouden
description: Leer hoe u koppelingen toevoegt en verzonden berichten bijhoudt
feature: Email Design, Monitoring
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: koppelingen, bijhouden, controleren, e-mail
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
source-git-commit: 4de37520b3ea7842d7f385f38c07cdf4984a5939
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 1%

---

# Koppelingen toevoegen en berichten bijhouden {#tracking}

Gebruiken [!DNL Journey Optimizer] om koppelingen naar uw inhoud toe te voegen en de verzonden berichten te volgen om het gedrag van de ontvangers te controleren.

## Tekstspatiëring inschakelen {#enable-tracking}

U kunt het bijhouden van wijzigingen op berichtniveau inschakelen door de optie **[!UICONTROL Email opens]** en/of **[!UICONTROL Click on email]** opties wanneer het creëren van uw bericht binnen een reis of een campagne.

>[!BEGINTABS]

>[!TAB Tekstspatiëring tijdens een reis inschakelen]

![](assets/message-tracking-journey.png)

>[!TAB Tekstspatiëring in een campagne inschakelen]

![](assets/message-tracking-campaign.png)

>[!ENDTABS]

>[!NOTE]
>
>Beide opties zijn standaard ingeschakeld.

Zo kunt u het gedrag van de ontvangers bijhouden via:

* **[!UICONTROL Email opens]**: Berichten die zijn geopend.
* **[!UICONTROL Click on email]**: Klik op koppelingen in een e-mail.

## Koppelingen invoegen {#insert-links}

Bij het ontwerpen van een bericht kunt u koppelingen naar uw inhoud toevoegen.

>[!NOTE]
>
>Wanneer [tracking is ingeschakeld](#enable-tracking), worden alle koppelingen in de inhoud van het bericht bijgehouden.

Volg onderstaande stappen om koppelingen in te voegen in uw e-mailinhoud:

1. Selecteer een element en klik op **[!UICONTROL Insert link]** in de contextuele werkbalk.

   ![](assets/message-tracking-insert-link.png)

1. Kies het type koppeling dat u wilt maken:

   * **[!UICONTROL External link]**: Voeg een koppeling naar een externe URL in.

   * **[!UICONTROL Landing page]**: Koppelingen naar bestemmingspagina&#39;s invoegen. [Meer informatie](../landing-pages/get-started-lp.md)

   * **[!UICONTROL One click Opt-out]**: Voeg een koppeling in om gebruikers in staat te stellen zich snel af te melden voor uw communicatie zonder dat ze hoeven te bevestigen dat ze het abonnement willen opzeggen. [Meer informatie](email-opt-out.md#one-click-opt-out).

   * **[!UICONTROL External Opt-in/Subscription]**: Voeg een koppeling in om het ontvangen van communicatie van uw merk te accepteren.

   * **[!UICONTROL External Opt-out/Unsubscription]**: Voeg een koppeling in om het abonnement op communicatie van uw merk op te zeggen. Meer informatie over beheer van opt-out in [deze sectie](email-opt-out.md#opt-out-management).

   * **[!UICONTROL Mirror page]**: Voeg een koppeling toe om de e-mailinhoud in een webbrowser weer te geven. [Meer informatie](#mirror-page)

1. Voer de gewenste URL in het desbetreffende veld in of selecteer een openingspagina en definieer de koppelingsinstellingen en -stijlen. [Meer informatie](#adjust-links)

   >[!NOTE]
   >
   >Voor het interpreteren van URL&#39;s [!DNL Journey Optimizer] voldoet aan de URI-syntaxis ([RFC 3986-standaard](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}), waardoor sommige speciale internationale tekens in URL&#39;s worden uitgeschakeld. Wanneer u de proefdruk of e-mail probeert te verzenden, kunt u de tekenreeks via URL coderen als tijdelijke oplossing als u een fout hebt geretourneerd met een URL die aan uw inhoud is toegevoegd.

1. U kunt uw koppelingen aanpassen. [Meer informatie](../personalization/personalization-syntax.md#perso-urls)

1. Sla uw wijzigingen op.

1. Als de koppeling eenmaal is gemaakt, kunt u deze nog steeds wijzigen in het menu **[!UICONTROL Settings]** en **[!UICONTROL Styles]** aan de rechterkant.

   ![](assets/message-tracking-link-settings.png)

>[!NOTE]
>
>E-mailberichten van het type Marketing moeten een [opt-out-koppeling](../privacy/opt-out.md#opt-out-management), die niet vereist is voor transactieberichten. De berichtcategorie (**[!UICONTROL Marketing]** of **[!UICONTROL Transactional]**) wordt gedefinieerd in de [kanaaloppervlak](../configuration/channel-surfaces.md#email-type) wanneer u het bericht maakt.

## Koppelingen aanpassen {#adjust-links}

U kunt uw koppelingen aanpassen met de opdracht **[!UICONTROL Settings]** en **[!UICONTROL Styles]** aan de rechterkant. U kunt een koppeling onderstrepen, de kleur ervan bewerken en het doel ervan selecteren.

1. In een **[!UICONTROL Text]** Selecteer de koppeling waar een koppeling wordt ingevoegd.

1. Van de **[!UICONTROL Settings]** , kiest u hoe de doelgroep wordt omgeleid met de **[!UICONTROL Target]** vervolgkeuzelijst:

   * **[!UICONTROL None]**: hiermee wordt de koppeling geopend in hetzelfde frame als waarop is geklikt (standaard).
   * **[!UICONTROL Blank]**: hiermee opent u de koppeling in een nieuw venster of op een nieuw tabblad.
   * **[!UICONTROL Self]**: hiermee opent u de koppeling in hetzelfde frame als waarop u hebt geklikt.
   * **[!UICONTROL Parent]**: hiermee opent u de koppeling in het bovenliggende frame.
   * **[!UICONTROL Top]**: hiermee opent u de koppeling in de volledige tekst van het venster.

   ![](assets/link_2.png)

1. Controleren **[!UICONTROL Underline link]** om de labeltekst van uw koppeling te onderstrepen.

   ![](assets/link_1.png)

1. Klik op **[!UICONTROL Link color]** van de **[!UICONTROL Styles]** tab.

   ![](assets/link_3.png)

1. Sla uw wijzigingen op.

## Koppelen naar een spiegelpagina {#mirror-page}

De spiegelpagina is een HTML-pagina die online toegankelijk is via een webbrowser. De inhoud is identiek aan de inhoud van uw e-mail.

Als u een koppeling wilt toevoegen aan een spiegel in uw e-mailbericht, [een koppeling invoegen](#insert-links) en selecteert u **[!UICONTROL Mirror page]** als het type koppeling.

![](assets/message-tracking-mirror-page.png)

De spiegelpagina wordt automatisch gemaakt.

>[!IMPORTANT]
>
>Koppelingen naar spiegelpagina&#39;s worden automatisch gegenereerd en kunnen niet worden bewerkt. Ze bevatten alle gecodeerde, gepersonaliseerde gegevens die nodig zijn om de oorspronkelijke e-mail te renderen. Als gevolg hiervan kan het gebruik van gepersonaliseerde kenmerken met grote waarden langdurige spiegel-pagina&#39;s-URL&#39;s genereren, waardoor de koppeling niet kan werken in webbrowsers met een maximale URL-lengte.

Wanneer de e-mail is verzonden en de ontvangers op de koppeling voor de spiegelpagina klikken, wordt de inhoud van de e-mail in hun standaardwebbrowser weergegeven.

>[!NOTE]
>
>In de [bewijs](../content-management/proofs.md) die naar de testprofielen worden verzonden, is de koppeling naar de spiegelpagina niet actief. Deze wordt alleen geactiveerd in de laatste berichten.

De retentieperiode voor een spiegelpagina is 60 dagen. Na die vertraging is de spiegelpagina niet meer beschikbaar.

## Beheer van bijhouden {#manage-tracking}

De [E-mailDesigner](content-from-scratch.md) Hiermee kunt u de bijgehouden URL&#39;s beheren, zoals het bewerken van het trackingtype voor elke koppeling.

1. Klik op de knop **[!UICONTROL Links]** in het linkerdeelvenster om de lijst weer te geven met alle URL&#39;s van de inhoud die wordt bijgehouden.

   In deze lijst kunt u een gecentraliseerde weergave gebruiken en elke URL in de e-mailinhoud opzoeken.

1. Als u een koppeling wilt bewerken, klikt u op het bijbehorende potloodpictogram.

1. U kunt de **[!UICONTROL Tracking Type]** indien nodig:

   ![](assets/message-tracking-edit-a-link.png)

   Voor elke bijgehouden URL kunt u de modus Tekstspatiëring instellen op een van de volgende waarden:

   * **[!UICONTROL Tracked]**: activeert tracering op deze URL.
   * **[!UICONTROL Opt out]**: beschouwt deze URL als een opt-out- of niet-abonnements-URL.
   * **[!UICONTROL Mirror page]**: beschouwt deze URL als een URL van een spiegelpagina.
   * **[!UICONTROL Never]**: activeert het bijhouden van deze URL nooit.

Rapportage over openingen en klikken is beschikbaar in de [Live-rapport](../reports/live-report.md) en in de [Algemeen rapport](../reports/global-report.md).

## URL-tracking aanpassen {#url-tracking}

Meestal [URL-tracking](email-settings.md#url-tracking) wordt beheerd op oppervlakniveau, maar de profielattributen worden niet gesteund. De enige manier om dit te doen is door [URL&#39;s aanpassen](../personalization/personalization-syntax.md#perso-urls) in de e-mailontwerper.

Volg onderstaande stappen om aangepaste URL-volgparameters toe te voegen aan uw koppelingen.

1. Selecteer een koppeling en klik op **[!UICONTROL Insert link]** in de contextuele werkbalk.

1. Selecteer het verpersoonlijkingspictogram. Deze optie is alleen beschikbaar voor de volgende typen koppelingen: **Externe koppeling**, **Koppeling met abonnement opheffen** en **Uitschakelen**.

   ![](assets/message-tracking-insert-link-perso.png)

1. Voeg de URL volgende parameter toe en selecteer het profielattribuut van uw keus van de verpersoonlijkingsredacteur.

   ![](assets/message-tracking-perso-parameter.png)

1. Sla uw wijzigingen op.

1. Herhaal bovenstaande stappen voor elke koppeling waaraan u deze parameter voor bijhouden wilt toevoegen.

Wanneer de e-mail wordt verzonden, wordt deze parameter automatisch toegevoegd aan het einde van de URL. U kunt deze parameter vervolgens vastleggen in hulpprogramma&#39;s voor webanalyse of in prestatierapporten.

>[!NOTE]
>
>U kunt de uiteindelijke URL controleren door [een bewijs verzenden](../content-management/preview-test.md#send-proofs) en klik op de koppeling in de inhoud van het e-mailbericht als u de proefdruk hebt ontvangen. De URL moet de parameter tracking weergeven. In het bovenstaande voorbeeld is de laatste URL: <https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number>
