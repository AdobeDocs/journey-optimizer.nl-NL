---
title: Je berichten bijhouden
description: Leer hoe u koppelingen toevoegt en verzonden berichten bijhoudt
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
source-git-commit: 6ff5d093bac20248106be1f4478102c29703cb1d
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Koppelingen toevoegen en berichten bijhouden {#tracking}

Gebruik [!DNL Journey Optimizer] om verbindingen aan uw inhoud toe te voegen en de berichten te volgen die worden verzonden om het gedrag van uw ontvangers te controleren.

## Tekstspatiëring inschakelen {#enable-tracking}

U kunt het volgen op het niveau van het e-mailbericht toelaten door **[!UICONTROL Open Tracking for email]** en/of **[!UICONTROL Click Tracking for email]** opties te controleren wanneer [het creëren van uw bericht](create-message.md).

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
>Wanneer [tracking is ingeschakeld](#enable-tracking), worden alle koppelingen in de berichtinhoud bijgehouden.

Volg onderstaande stappen om koppelingen in te voegen in uw e-mailinhoud:

1. Selecteer een element en klik **[!UICONTROL Insert link]** van de contextafhankelijke toolbar.

   ![](assets/message-tracking-insert-link.png)

1. Kies het type koppeling dat u wilt maken:

   * **[!UICONTROL External link]**: Voeg een koppeling naar een externe URL in.

   * **[!UICONTROL Unsubscription link]**: Voeg een koppeling in om uw abonnement op te zeggen dat u geen communicatie van uw merk wilt ontvangen. Meer informatie over opt-outbeheer in [deze sectie](consent.md#opt-out-management).

   * **[!UICONTROL Mirror page]**: Voeg een koppeling in om de e-mailinhoud in een webbrowser weer te geven. Meer informatie vindt u in [deze sectie](#mirror-page).

   * **[!UICONTROL Opt-out]**: Voeg een koppeling in om gebruikers in staat te stellen zich snel af te melden voor uw communicatie zonder dat ze hoeven te bevestigen dat ze het abonnement willen opzeggen. Meer informatie vindt u in [deze sectie](#one-click-opt-out-link).

   ![](assets/message-tracking-links.png)

1. U kunt uw koppelingen aanpassen. Meer informatie over gepersonaliseerde URL&#39;s vindt u in [deze sectie](personalization/personalization-syntax.md).

1. Sla uw wijzigingen op.

1. Zodra de verbinding wordt gecreeerd, kunt u het van **[!UICONTROL Component settings]** ruit op het recht nog wijzigen.

   * Klik op het potloodpictogram om de koppeling te bewerken.
   * U kunt de koppeling onderstrepen of niet door de bijbehorende optie in te schakelen.

   ![](assets/message-tracking-link-settings.png)

## Koppelen naar een spiegelpagina {#mirror-page}

De spiegelpagina is een HTML-pagina die online toegankelijk is via een webbrowser. De inhoud is identiek aan de inhoud van uw e-mail.

Als u een koppeling naar een spiegel in uw e-mail wilt toevoegen, voegt u [een koppeling in](#insert-links) en selecteert u **[!UICONTROL Mirror page]** als het type koppeling.

![](assets/message-tracking-mirror-page.png)

De spiegelpagina wordt automatisch gemaakt.

>[!NOTE]
>
>U kunt de automatisch gegenereerde koppeling niet bewerken.

Wanneer de e-mail is verzonden en de ontvangers op de koppeling voor de spiegelpagina klikken, wordt de inhoud van de e-mail in hun standaardwebbrowser weergegeven.

>[!NOTE]
>
>In de [proefdruk](preview.md#send-proofs) verzonden naar de testprofielen, is de verbinding aan de spiegelpagina niet actief. Deze wordt alleen geactiveerd in de laatste berichten.

De retentieperiode voor een spiegelpagina is 60 dagen. Na die vertraging is de spiegelpagina niet meer beschikbaar.

## Een-klik-koppeling voor weigeren {#one-click-opt-out-link}

Om uw ontvangers in staat te stellen om snel af te zien van het ontvangen van mededelingen van uw merk, kunt u een één-klik opt-out verbinding in uw e-mailinhoud opnemen. Hierdoor wordt voorkomen dat gebruikers worden omgeleid naar een bestemmingspagina waar ze hun keuze moeten bevestigen, waardoor het afwijzingsproces sneller verloopt.

Volg onderstaande stappen om een koppeling om te weigeren toe te voegen in uw e-mail.

1. [Voeg een ](#insert-links) koppeling in en selecteer  **[!UICONTROL Opt-out]** als het type koppeling.

   ![](assets/message-tracking-opt-out.png)

1. Selecteer hoe u de optie Weigeren wilt toepassen: op het kanaal, de identiteit, of abonnementsniveau.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Channel]**: De opt-out is van toepassing op toekomstige berichten die naar het doel van het profiel (d.w.z. e-mailadres) voor het huidige kanaal worden verzonden. Als er meerdere doelen aan een profiel zijn gekoppeld, geldt de opt-out voor alle doelen (e-mailadressen) in het profiel voor dat kanaal.
   * **[!UICONTROL Identity]**: De opt-out is van toepassing op toekomstige berichten die worden verzonden naar het specifieke doel (d.w.z. e-mailadres) dat voor het huidige bericht wordt gebruikt.
   * **[!UICONTROL Subscription]**: De opt-out is van toepassing op toekomstige berichten verbonden aan een specifieke abonnementenlijst. Deze optie kan alleen worden geselecteerd als het huidige bericht is gekoppeld aan een abonnementenlijst.

1. Voer de URL in van de bestemmingspagina waarop de gebruiker wordt omgeleid wanneer het abonnement wordt opgezegd. Deze pagina is alleen hier om te bevestigen dat de optie Weigeren is gelukt.

   ![](assets/message-tracking-opt-out-confirmation.png)

1. Klik op **[!UICONTROL Save]**.

Als een ontvanger op de koppeling om te weigeren klikt nadat het bericht is verzonden, wordt hij onmiddellijk uitgeschakeld.

## Beheer van bijhouden {#manage-tracking}

Met de [e-mailontwerper](create-email-content.md) kunt u de bijgehouden URL&#39;s beheren, zoals het type tekstspatiëring voor elke koppeling bewerken.

1. Klik op het pictogram **[!UICONTROL Links]** in het linkerdeelvenster om de lijst weer te geven met alle URL&#39;s van de inhoud die wordt bijgehouden.

   In deze lijst kunt u een gecentraliseerde weergave gebruiken en elke URL in de e-mailinhoud opzoeken.

1. Als u een koppeling wilt bewerken, klikt u op het bijbehorende potloodpictogram.

   ![](assets/message-tracking-edit-links.png)

1. U kunt **[!UICONTROL Tracking Type]** indien nodig wijzigen:


   ![](assets/message-tracking-edit-a-link.png)

   Voor elke bijgehouden URL kunt u de modus Tekstspatiëring instellen op een van de volgende waarden:

   * **[!UICONTROL Tracked]**: Hiermee activeert u het bijhouden van wijzigingen op deze URL.
   * **[!UICONTROL Opt out]**: beschouwt deze URL als een opt-out- of niet-abonnements-URL.
   * **[!UICONTROL Mirror page]**: beschouwt deze URL als een URL van een spiegelpagina.
   * **[!UICONTROL Never]**: Hiermee activeert u het bijhouden van deze URL nooit.  <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

Het aantal berichten dat is geopend en het aantal verbindingen die zijn geklikt zijn vermeld in [Uitvoeringen tabel](message-monitoring.md).

Rapportage over openingen en kliks is beschikbaar in [E-mail Live rapport](reports/email-live-report.md) en in [E-mail Globaal rapport](reports/email-global-report.md).


