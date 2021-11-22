---
title: Je berichten bijhouden
description: Leer hoe u koppelingen toevoegt en verzonden berichten bijhoudt
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
source-git-commit: c6db89093e1ec5b7d9fe084cec58b8b7664c6ab2
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 1%

---

# Koppelingen toevoegen en berichten bijhouden {#tracking}

Gebruiken [!DNL Journey Optimizer] om koppelingen naar uw inhoud toe te voegen en de verzonden berichten te volgen om het gedrag van de ontvangers te controleren.

## Tekstspatiëring inschakelen {#enable-tracking}

U kunt het bijhouden van wijzigingen op berichtniveau inschakelen door de optie **[!UICONTROL Open Tracking for email]** en/of **[!UICONTROL Click Tracking for email]** opties wanneer [uw bericht maken](create-message.md).

![](assets/message-tracking.png)

>[!NOTE]
>
>Beide opties zijn standaard ingeschakeld.

Zo kunt u het gedrag van de ontvangers bijhouden via:

* **[!UICONTROL Open Tracking for email]**: Berichten die zijn geopend.
* **[!UICONTROL Click Tracking for email]**: Klik op koppelingen in een e-mail.

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

   * **[!UICONTROL Unsubscription link]**: Voeg een koppeling in om uw abonnement op te zeggen dat u geen communicatie van uw merk wilt ontvangen. Meer informatie over beheer van opt-out in [deze sectie](consent.md#opt-out-management).

   * **[!UICONTROL Mirror page]**: Voeg een koppeling in om de e-mailinhoud in een webbrowser weer te geven. Meer informatie in [deze sectie](#mirror-page).

   * **[!UICONTROL Opt-out]**: Voeg een koppeling in om gebruikers in staat te stellen zich snel af te melden voor uw communicatie zonder dat ze hoeven te bevestigen dat ze het abonnement willen opzeggen. Meer informatie in [deze sectie](#one-click-opt-out-link).

   ![](assets/message-tracking-links.png)

1. U kunt uw koppelingen aanpassen. Meer informatie over gepersonaliseerde URL&#39;s vindt u in [deze sectie](personalization/personalization-syntax.md#perso-urls).

1. Sla uw wijzigingen op.

1. Als de koppeling eenmaal is gemaakt, kunt u deze nog steeds wijzigen in het menu **[!UICONTROL Component settings]** aan de rechterkant.

   * Klik op het potloodpictogram om de koppeling te bewerken.
   * U kunt de koppeling onderstrepen of niet door de bijbehorende optie in te schakelen.

   ![](assets/message-tracking-link-settings.png)

## Koppelen naar een spiegelpagina {#mirror-page}

De spiegelpagina is een HTML-pagina die online toegankelijk is via een webbrowser. De inhoud is identiek aan de inhoud van uw e-mail.

Als u een koppeling wilt toevoegen aan een spiegel in uw e-mailbericht, [een koppeling invoegen](#insert-links) en selecteert u **[!UICONTROL Mirror page]** als het type koppeling.

![](assets/message-tracking-mirror-page.png)

De spiegelpagina wordt automatisch gemaakt.

>[!NOTE]
>
>U kunt de automatisch gegenereerde koppeling niet bewerken.

Wanneer de e-mail is verzonden en de ontvangers op de koppeling voor de spiegelpagina klikken, wordt de inhoud van de e-mail in hun standaardwebbrowser weergegeven.

>[!NOTE]
>
>In de [bewijs](preview.md#send-proofs) die naar de testprofielen worden verzonden, is de koppeling naar de spiegelpagina niet actief. Deze wordt alleen geactiveerd in de laatste berichten.

De retentieperiode voor een spiegelpagina is 60 dagen. Na die vertraging is de spiegelpagina niet meer beschikbaar.

## Een-klik-koppeling voor weigeren {#one-click-opt-out-link}

Om uw ontvangers in staat te stellen om snel af te zien van het ontvangen van mededelingen van uw merk, kunt u een één-klik opt-out verbinding in uw e-mailinhoud opnemen. Hierdoor wordt voorkomen dat gebruikers worden omgeleid naar een bestemmingspagina waar ze hun keuze moeten bevestigen, waardoor het afmeldingsproces wordt versneld.

Volg onderstaande stappen om een koppeling om te weigeren toe te voegen in uw e-mail.

1. [Een koppeling invoegen](#insert-links) en selecteert u **[!UICONTROL Opt-out]** als het type koppeling.

   ![](assets/message-tracking-opt-out.png)

1. Selecteer hoe u de optie Weigeren wilt toepassen: op het kanaal, de identiteit, of abonnementsniveau.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Channel]**: De opt-out is van toepassing op toekomstige berichten die naar het doel van het profiel (d.w.z. e-mailadres) voor het huidige kanaal worden verzonden. Als er meerdere doelen aan een profiel zijn gekoppeld, geldt de opt-out voor alle doelen (e-mailadressen) in het profiel voor dat kanaal.
   * **[!UICONTROL Identity]**: De opt-out is van toepassing op toekomstige berichten die worden verzonden naar het specifieke doel (d.w.z. e-mailadres) dat voor het huidige bericht wordt gebruikt.
   * **[!UICONTROL Subscription]**: De opt-out is van toepassing op toekomstige berichten verbonden aan een specifieke abonnementenlijst. Deze optie kan alleen worden geselecteerd als het huidige bericht is gekoppeld aan een abonnementenlijst.

1. Voer de URL in van de bestemmingspagina waarop de gebruiker wordt omgeleid wanneer het abonnement wordt opgezegd. Deze pagina is alleen hier om te bevestigen dat de optie Weigeren is gelukt.

   ![](assets/message-tracking-opt-out-confirmation.png)

   U kunt uw koppelingen aanpassen. Meer informatie over gepersonaliseerde URL&#39;s vindt u in [deze sectie](personalization/personalization-syntax.md).

1. Sla uw wijzigingen op.

Als ontvangers op de koppeling Weigeren klikken en uw bericht eenmaal zijn verzonden, worden ze direct uitgeschakeld.

## Beheer van bijhouden {#manage-tracking}

De [E-mailontwerper](create-email-content.md) Hiermee kunt u de bijgehouden URL&#39;s beheren, zoals het bewerken van het trackingtype voor elke koppeling.

1. Klik op de knop **[!UICONTROL Links]** in het linkerdeelvenster om de lijst weer te geven met alle URL&#39;s van de inhoud die wordt bijgehouden.

   In deze lijst kunt u een gecentraliseerde weergave gebruiken en elke URL in de e-mailinhoud opzoeken.

1. Als u een koppeling wilt bewerken, klikt u op het bijbehorende potloodpictogram.

   ![](assets/message-tracking-edit-links.png)

1. U kunt de **[!UICONTROL Tracking Type]** indien nodig:


   ![](assets/message-tracking-edit-a-link.png)

   Voor elke bijgehouden URL kunt u de modus Tekstspatiëring instellen op een van de volgende waarden:

   * **[!UICONTROL Tracked]**: Hiermee activeert u het bijhouden van wijzigingen op deze URL.
   * **[!UICONTROL Opt out]**: beschouwt deze URL als een opt-out- of niet-abonnements-URL.
   * **[!UICONTROL Mirror page]**: beschouwt deze URL als een URL van een spiegelpagina.
   * **[!UICONTROL Never]**: Hiermee activeert u het bijhouden van deze URL nooit. <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

Het aantal berichten dat is geopend en het aantal koppelingen waarop is geklikt, worden vermeld in het dialoogvenster [Tabblad Uitvoeringen](message-monitoring.md).

Rapportage over openingen en klikken is beschikbaar in de [E-mailLive-rapport](reports/email-live-report.md) en in de [E-mailglobaal rapport](reports/email-global-report.md).
